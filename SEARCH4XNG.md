# Search4XNG

Search4XNG is a SearXNG fork with a compact Gruvbox interface inspired by
[4get](https://git.lolcat.ca/lolcat/4get). It keeps SearXNG's engines,
privacy controls and administration while adopting 4get's colors, spacing,
navigation and result presentation.

## What changed

- `client/simple/src/less/search4xng.less` contains the isolated skin.
- The home page and search header use the Search4XNG name.
- `deploy/` contains a production-oriented SearXNG + Valkey configuration.
- Upstream SearXNG files and history remain intact to make future rebases easier.

## Develop the theme

```sh
cd client/simple
npm ci
npm run build
npm run lint
```

Generated assets are written to `searx/static/themes/simple/`.

## Run locally

Build the custom container from the repository root:

```sh
make container
cd deploy
printf 'SEARXNG_SECRET=%s\n' "$(openssl rand -hex 32)" > .env
docker compose up -d
```

Search4XNG will listen on `127.0.0.1:8080`. Put Caddy or another HTTPS reverse
proxy in front of it when exposing it to the internet. An example Caddyfile is
included in `deploy/Caddyfile.example`.

## Free 24/7 hosting

GitHub Pages cannot run Search4XNG because it does not execute Python. A small
always-on VM is required. Oracle Cloud Infrastructure's Always Free Ampere A1
VM is the recommended option for this project; Google Cloud's Free Tier
`e2-micro` VM is an alternative with considerably less RAM.

On an Ubuntu ARM VM with Docker, clone this repository and run the commands in
the previous section. Allocate 1 OCPU and at least 2 GB RAM. Open ports 80 and
443 in the cloud firewall, install Caddy on the VM, copy
`deploy/Caddyfile.example` to `/etc/caddy/Caddyfile`, replace the domain and
reload Caddy.

Never commit `deploy/.env`; it contains the instance secret.

## Licensing and attribution

Search4XNG and SearXNG are licensed under AGPL-3.0-or-later. 4get is licensed
under AGPL-3.0-only. The interface is a clean adaptation based on 4get's public
design and palette; its repository is credited above and in the theme source.
When operating a modified network service, make the corresponding source code
available to its users as required by the AGPL.

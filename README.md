<p align="center"><img src="https://raw.githubusercontent.com/go-tpm2/brand/main/social/go-tpm2.png" alt="go-tpm2/go-tpm2.github.io" width="720"></p>

# go-tpm2.github.io

Sources for **go-tpm2.github.io** — the go-tpm2 landing page.
Built by [Hugo](https://gohugo.io) — same toolchain and same template
shape as [go-virtio.github.io](https://github.com/go-virtio/go-virtio.github.io)
and [cloud-boot.github.io](https://github.com/cloud-boot/cloud-boot.github.io).
Teal palette so it reads as a sibling project page.

## Layout

```text
.
├── hugo.toml                       Site config + hero + repo-card params ([[params.repos]])
├── content/
│   └── _index.md                   Homepage marker (empty; the page body is fully custom)
├── layouts/
│   └── index.html                  Homepage — hero, repo grid, inline CSS,
│                                    light/dark/system theme toggle
├── static/
│   ├── favicon.svg
│   └── img/logo.svg
└── public/                         Hugo build output (gitignored — built by CI)
```

## Build locally

```sh
hugo server -D                            # live reload at http://localhost:1313/
hugo --gc --minify                        # production build → ./public/
```

## Deploy

`.github/workflows/hugo.yml` builds + deploys on every push to `main`.
Configure GitHub Pages on the repo with **Source = "GitHub Actions"**
(not "Deploy from a branch").

## Sibling pages

- [go-virtio](https://go-virtio.github.io) — the pure-Go transport-agnostic
  virtio driver family, sibling stack to go-tpm2.
- [cloud-boot](https://cloud-boot.github.io) — the UEFI bootloader and
  measured-boot loader that go-tpm2's first consumer ships in.
- [openweft](https://openweft.github.io) — the microVM platform on top.

# vis-nightly

Nightly static build of [vis](https://github.com/martanne/vis) master with
[msi-void](https://github.com/xfn-less/msi-void) `void-config/vis` Lua config
baked into the single binary (`vis/lua/` overlay before `make docker`).

Release asset: [nightly/vis-master](https://github.com/xfn-less/vis-nightly/releases/tag/nightly)

```sh
curl -fLO https://github.com/xfn-less/vis-nightly/releases/download/nightly/vis-master
curl -fLO https://github.com/xfn-less/vis-nightly/releases/download/nightly/vis-master.sha256
sha256sum -c vis-master.sha256
sudo install -Dm755 vis-master /usr/local/bin/vis
```

No `~/.config/vis` or `VIS_PATH` needed; themes and `my.*` modules ship inside the binary.
External formatters (`prettier`, etc.) remain separate packages and are not installed by this release.

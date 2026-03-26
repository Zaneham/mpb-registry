# mpb-registry

Package registry for [MPB](https://github.com/Zaneham/mpb), the Mainframe Package Bureau.

This repository is the index. It tells MPB where to find packages. The actual code lives in each package author's own repository and stays under their control.

## Current Packages

| Package | Version | Language | License | Author |
|---------|---------|----------|---------|--------|
| [zblas](https://github.com/Zaneham/zblas) | 1.0.0 | HLASM | Apache-2.0 | Zane Hambly |
| [cobol-dateutil](https://github.com/Zaneham/cobol-dateutil) | 0.1.0 | COBOL | Apache-2.0 | Zane Hambly |
| [cobol-ebcdic](https://github.com/Zaneham/cobol-ebcdic) | 0.1.0 | COBOL | Apache-2.0 | Zane Hambly |
| [zigi](https://github.com/lbdyck/zigi) | 4.0.0 | REXX | GPL-2.0 | Lionel B. Dyck |
| [CBTView](https://github.com/lbdyck/CBTView) | 1.0.0 | REXX | GPL-2.0 | Lionel B. Dyck |
| [racfadm](https://github.com/lbdyck/racfadm) | 1.0.0 | REXX | GPL-2.0 | Lionel B. Dyck |
| [pdsegen](https://github.com/lbdyck/pdsegen) | 1.0.0 | REXX | GPL-2.0 | Lionel B. Dyck |
| [xmitip](https://github.com/lbdyck/xmitip) | 1.0.0 | REXX | GPL-2.0 | Lionel B. Dyck |
| [ftpb](https://github.com/lbdyck/ftpb) | 1.0.0 | REXX | GPL-2.0 | Lionel B. Dyck |
| [whoson](https://github.com/lbdyck/whoson) | 1.0.0 | REXX | GPL-2.0 | Lionel B. Dyck |
| [omvscmds](https://github.com/lbdyck/omvscmds) | 1.0.0 | REXX | GPL-2.0 | Lionel B. Dyck |
| [algol-stringlib](https://github.com/Zaneham/algol-stringlib) | 0.1.0 | ALGOL | Apache-2.0 | Zane Hambly |
| [rpg-dateutil](https://github.com/Zaneham/rpg-dateutil) | 1.1.0 | RPG | Apache-2.0 | Zane Hambly |
| [cobol-jsonutil](https://github.com/Zaneham/cobol-jsonutil) | 1.0.0 | COBOL | Apache-2.0 | Zane Hambly |

## Adding a Package

Fork this repository, create a directory under `packages/` with your package name, add a `package.json`, update `index.json`, and submit a pull request.

Your `package.json` should look like this:

```json
{
  "name": "your-package",
  "version": "1.0.0",
  "description": "What it does.",
  "author": "Your Name",
  "license": "Apache-2.0",
  "language": "cobol",
  "repository": "https://github.com/you/your-package"
}
```

Supported languages: `cobol`, `hlasm`, `rexx`, `pli`, `jcl`, `fortran`, `algol`, `newp`, `wfl`, `rpg`.

If pull requests aren't your thing, open an issue with a link to your repository and we will add it for you.

## How It Works

MPB fetches `index.json` from this repository to list and search packages. When you install a package, MPB fetches that package's `package.json` from here, reads the `repository` URL, and clones the code directly from the author's repo. Nothing is hosted here except metadata.

## License

Apache 2.0.

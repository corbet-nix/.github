# Support

## Questions

Open a GitHub Discussion or issue in the relevant repository. Include:

- Repository and version or commit
- Hub and plane (`nixosModules`, `systemManagerModules`, `homeManagerModules`,
  `darwinModules`, `nixidyModules`)
- Nix version and system (`nix --version`, `uname -m`)
- Minimal reproduction

Do not include private hostnames, LAN or overlay IPs, `/home/<user>` paths,
credentials, or secrets. Mechanism repos must stay free of private values.

## Scope

Stable mechanisms get best-effort community support. Repositories marked
experimental, or values under `experiments/`, are research notes, not support
commitments. Private infrastructure configuration is out of scope.

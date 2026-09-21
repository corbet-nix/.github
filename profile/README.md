# Corbet Nix

Reusable Nix mechanisms for NixOS, system-manager, home-manager, and nixidy.
Mechanism public, values private: this org ships generic configuration
mechanisms. Host-specific values, topology, and secrets live outside these
repositories.

Default outbound license is `MIT OR Apache-2.0`. `nixnas` is the deliberate
Apache-2.0 appliance exception.

## Family

Hubs define machine context and the management planes configuration arrives
through. Modules own exactly one concern and attach to hubs.

| Hub | Context |
|---|---|
| `nixnas` | USB-boot storage appliance |
| `nixarch` | Declarative Arch/CachyOS via system-manager + home-manager |
| `nixvps` | Tiny cloud / constrained machines |
| `nixk3s` | Cluster layer, nests on a host hub |

Everything else is a module: one concern, plane-targeted
(`nixosModules`, `systemManagerModules`, `homeManagerModules`,
`nixidyModules`), optional coupling by option value, never by flake input.

## Using

```nix
{
  inputs.nixram.url = "github:corbet-nix/nixram-corbet-ch";
}
```

Each repository documents its own options, levels, and verification status.
Values marked extrapolated are reasoned, not measured; `experiments/` tracks
what still needs measuring.

## Contributing

Default instructions are in `CONTRIBUTING.md`. The canonical Individual
Contributor License Agreement for this organization is version 1.0 at
[`cla-v1.0`](https://github.com/corbet-nix/.github/blob/cla-v1.0/CLA.md).
The pull-request affirmation is the acceptance record.

## Security

Report vulnerabilities through the affected repository's private GitHub
security advisory form. Do not open public issues for unpatched
vulnerabilities. See `SECURITY.md` in this repository for details.

# device-protection-skills

Skills for working alongside Aikido Device Protection.

## Skills

### aikido-device-protection

Triggers on unexplained package install failures (HTTP 403, connection reset, or a version resolving older than expected) across npm, pip, Maven, NuGet, Go, Cargo, Composer, gem, Homebrew, and editor or browser extensions.

These failures usually mean Device Protection blocked a malicious or policy-restricted package, but they look identical to an expired token. The skill tells Claude to run `aikidoctl events --json` and check for a matching block *before* debugging credentials, switching registries, or trying other workarounds, then walks through how to resolve each block type (malware, minimum package age, policy block, held for approval, certificate errors) without bypassing protection.

See [`skills/aikido-device-protection/SKILL.md`](skills/aikido-device-protection/SKILL.md).

## Installation

Copy the skill directory into your project's `.claude/skills/` folder, or install it as a plugin per your setup.

## License

Apache License 2.0, see [LICENSE](LICENSE).

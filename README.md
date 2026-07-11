# Mira Project

This repository hosts [byteseek/Mira](https://github.com/byteseek/Mira) as an upstream-tracked Git submodule under `Mira/`.

Mira is an agent-native investment-research protocol and workspace. It is not a standalone web service, trading bot, or autonomous portfolio manager.

## Clone

```bash
git clone --recurse-submodules https://github.com/LiuTheReal/willen.git
cd willen
```

For an existing clone:

```bash
git submodule update --init --recursive
```

## Use with agents

- Codex and compatible code agents: start from `AGENTS.md`, then load the rules under `Mira/`.
- ChatGPT Project or a chat product that does not load repository rules reliably: paste `CHATGPT_PROJECT_INSTRUCTIONS.md` into the project instructions.
- Mira entry guide: `Mira/START_HERE.md`.

## Update Mira

```bash
git submodule update --remote --merge Mira
git add Mira
git commit -m "chore: update Mira upstream"
git push
```

The submodule is currently pinned to upstream commit `adddce7c6f41be309855e3c7d047e309bbe58a3a`.

## Validate

```bash
cd Mira
python3 scripts/run_quality_gate.py
python3 scripts/validate_repo.py
```

## License and boundaries

The upstream Mira repository is licensed under Apache-2.0. Its research, source, security, and usage boundaries remain governed by the documents inside `Mira/`, including `LICENSE`, `DATA_POLICY.md`, and `SECURITY.md`.

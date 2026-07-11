# Mira Project

This repository contains a vendored copy of
[byteseek/Mira](https://github.com/byteseek/Mira) under `Mira/` as
ordinary Git files. ChatGPT, Codex, GitHub search, and other repository
readers can therefore index the complete Mira rule, loop, skill,
template, and validation tree without Git submodule expansion.

Mira is an agent-native investment-research protocol and workspace. It
is not a standalone web service, trading bot, or autonomous portfolio
manager.

## Start using Mira

- Repository-aware agents: begin with `AGENTS.md`, then
  `Mira/START_HERE.md` and `Mira/OPERATING_CONTRACT.md`.
- ChatGPT Projects: use `CHATGPT_PROJECT_INSTRUCTIONS.md` as the Project
  Instructions entry pack.
- Main Mira identity and boundaries: `Mira/MIRA.md`.

A typical request is:

```text
Mira，研究 <公司或 ticker>
研究问题：<需要判断的问题>
市场范围：<市场>
时间边界：<截至日期或研究周期>
来源边界：<公开来源/指定材料>
输出深度：quick_map / standard / deep_dive
```

## Validate

```bash
cd Mira
python3 scripts/run_quality_gate.py
python3 scripts/validate_repo.py
```

## Update upstream

Upstream provenance and the refresh procedure are recorded in
`MIRA_UPSTREAM.md`. Updating Mira should be reviewed as a normal source
diff rather than performed implicitly at runtime.

## License and boundaries

The vendored Mira source remains licensed under Apache-2.0. Its
research, data, security, and usage boundaries remain governed by the
documents inside `Mira/`, including `LICENSE`, `DATA_POLICY.md`, and
`SECURITY.md`.

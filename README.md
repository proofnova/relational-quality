# Relational quality gate

여러 표의 복합 키·필수 값·외래 키를 검사해 오류 행을 지정한다.

A focused executable resource for AI-assisted structured work. **Zero runtime dependencies, no API key, Node.js 22+.**

[Live workspace](https://proofnova.github.io/relational-quality/) · [한국어 리소스 모음](https://proofnova.github.io/) · [Task contract](resource.json) · [Prior art](RESEARCH.md)

```sh
git clone https://github.com/proofnova/relational-quality.git
cd relational-quality
npm test
node cli.mjs example.json
```

## What it does

Compound-key indexes and explicit nullable foreign-key policies.

Partial-null foreign keys are not silently treated as a valid optional relation.

## Connect a model

Import `execute` from `./run.mjs`. Expose this declared tool to your model, validate its tool name/input contract, execute it, and retain the returned JSON and input digest. Calculations and constraint checks are performed by the resource. No paid model or new agent framework is required.

[SKILL.md](SKILL.md) contains the workflow, interpretation and recovery procedure. [example.json](example.json) is a complete input; [cases.json](cases.json) contains worked and edge-case synthetic regression checks. The website executes the same code locally in a bounded Worker. It has no model or external data upload.

## Recovery and limits

Correct duplicated/empty keys before repairing orphan rows; keep source row indices.

Underlying algorithms and task outcomes already exist in the alternatives. An existing tool configured for this exact task may remove the need for a separate project. Small synthetic tests cannot establish broad expertise or external demand. See [RESEARCH.md](RESEARCH.md). A plan/audit is not an external action or proof of actual user benefit.

## Contribute

Open an issue with a synthetic/redacted failing JSON input, expected result and Node version. Add a regression test and run `npm test`. Never include credentials or real private records in public examples.

MIT · Proofnova · 2026

# PRISM Anonymous Artifact Repository

This repository is prepared for double-blind review and focuses on reproducibility of key reported numbers from released outputs.

## Repository contents
- `map_0819/eval_0121_modules/`: PRISM multi-perspective reasoning modules.
- `artifact/`: scripts for reproducing paper-facing metrics from released outputs.
- `result_test/`, `result_llm_eval/`: released experiment outputs used in the paper.
- `LIMITATIONS.md`: explicit scope and non-release constraints.

## Quick reproduction
```bash
python artifact/reproduce_paper_numbers.py \
  --p123-mid result_test/p123_mid.jsonl \
  --p123-short result_test/p123_short.jsonl \
  --p4-mid result_test/p4_mid_no_json_parse_errors.jsonl \
  --p4-short result_test/p4_short.jsonl \
  --llm-eval result_llm_eval/llm_mid_eval.jsonl
```

Output file: `artifact/reproduced_metrics.json`

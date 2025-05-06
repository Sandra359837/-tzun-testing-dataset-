# Maya De La Cruz — Early-Career Resume Test Case

This folder contains a QA-verified resume generation test case for an early-career communications and media student, Maya De La Cruz. It is part of the `tzun-testing-dataset` corpus used to benchmark and fine-tune the Tzun GPT system.

---

## 📄 Scenario Details

- **Persona:** Early-career candidate
- **Target Role:** Customer Success Manager (B2B SaaS)
- **Run ID:** tone_matrix_stem_test_001
- **Prompt Version:** v1.2 + tone_matrix + stem_rotation

---

## 📁 Files

| File                    | Description |
|-------------------------|-------------|
| `resume_input.txt`      | Raw user resume used as input |
| `job_description.txt`   | Job description used to guide tailoring |
| `generated_output.txt`  | Output resume from the system (v1.2 tone variant prompt) |
| `qa_log.json`           | Full output metadata, including tone scores, bracketed items, and flagged issues |

---

## ✅ QA Outcome

| Metric                     | Value |
|----------------------------|--------|
| Output Score               | 4.0    |
| Tone Consistency Score     | 70     |
| Harmonization Triggered    | ✅ Yes |
| Bracketed Items            | 3      |
| Hallucinated Responsibility| ⚠️ Yes (bracketed + flagged) |

This test was flagged as **⭐ high training value** and should be included in early-career persona fine-tuning and regression test suites.

---

## 🔧 Notes for Reviewers

- Review the `qa_log.json` to understand flagged content and harmonization suggestions.
- Do **not** reuse this output in demos without reviewing and confirming bracketed suggestions.
- Consider running this test again after any system prompt changes to track improvements in tone alignment or hallucination control.

---

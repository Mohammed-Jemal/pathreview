## Week 7 — Issue selection

**Issue link:** [https://github.com/ascherj/pathreview/issues/153]

**Issue title:** [Faithfulness checker crashes when a context chunk has text: None]

**Tier:** [X ] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
[The faithfulness checker was failing when processing context chunks that have a null or 'None' text value causing uncached crash during execution. This happens when the string operation are attempted on a non-string object in the evaluation pipline. fixing this requires adding a check or fallback to handle 'None' values befor processing the text chunk.]

**Branch name:** [fix/153-faithfulness-checker-none-crash]

**Setup confirmation:** ['Yes'] App runs locally at localhost:5173

**Cohort ledger:** ['Yes] Issue added to cohort ledger

## Week 8 — Reproduction & solution planning

***Reproduction commit link:*** [Pending commit link]

***Reproduction summary:*** Reproduced issue #153 by running `pytest tests/unit/test_faithfulness_checker.py`. The test `test_none_context_chunk_text` failed with `TypeError: sequence item 0: expected str instance, NoneType found` when passing `context_chunks = [{"text": None}]`.

***PLAN.md link:*** [Pending link to PLAN.md]

***Walkthrough video (recommended):*** 

***Blockers or open questions:***
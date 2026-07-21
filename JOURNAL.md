## Week 7 — Issue selection

**Issue link:** [https://github.com/ascherj/pathreview/issues/153]

**Issue title:** [Faithfulness checker crashes when a context chunk has text: None]

**Tier:** [X ] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
[The faithfulness checker was failing when processing context chunks that have a null or 'None' text value causing uncached crash during execution. This happens when the string operation are attempted on a non-string object in the evaluation pipline. fixing this requires adding a check or fallback to handle 'None' values befor processing the text chunk.]

**Branch name:** [fix/153-faithfulness-checker-none-crash]

**Setup confirmation:** ['Yes'] App runs locally at localhost:5173

**Cohort ledger:** ['Yes] Issue added to cohort ledger
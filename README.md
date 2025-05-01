**Reconciliation Automation**
Reconciliation Automation using pandas and rapidfuzz to match transactions (numeric and text-based descriptions) between bank and internal records, flagging unmatched items or close matches.

**Takes as input**  
Two CSV files:  
- bank_records.csv
- internal_records.csv  

Each file has:
- 'Date', 'Amount', 'Description' as headers

**Required dependencies**
pip install pandas rapidfuzz

**In action**
- Exact matches records on 'Amount' and fuzzy matches text on 'Description'
- Drops matched entries to prevent duplicates
- Outputs:
  - matched_records.csv – good matches
  - unmatched_bank_records.csv – potential discrepancies

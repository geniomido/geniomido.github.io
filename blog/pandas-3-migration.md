---
layout: default
title: Pandas 3.0 Migration Guide
---

Pandas 3.0 is finally removing legacy features that have been marked as *deprecated* for years. If you don't audit your code now, you risk critical failures in production.

## What's Being Removed?
*   `.append()` on DataFrames (Use `pd.concat` instead)
*   `.iteritems()` (Use `.items()</code> instead)
*   `date_parser` in `read_csv` (Use `date_format` instead)

## Practical Example: Terminal Scan
Identify vulnerabilities in your project directory instantly:

```bash
$ python pandas3_migration_check.py ./analytics_project

🔍 Scanning ./analytics_project for Pandas 3.0 breaking changes...

📄 ./analytics_project/process_data.py
   Line 42: Warning: .append() on DataFrames/Series is removed. Use pd.concat().
   Line 89: Deprecation: .iteritems() is removed. Use .items() instead.

📄 ./analytics_project/loaders/csv_loader.py
   Line 12: Deprecation: date_parser argument in read_csv is removed. Use date_format.

⚠️ Found 3 potential issues.
💡 Need a full migration? Contact GENIOM.
```

[Download Tool on GitHub →](https://github.com/geniomido/pandas-migration)

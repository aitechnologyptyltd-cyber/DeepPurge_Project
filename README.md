DeepPurge — Deep System Uninstaller & Residual Cleaner (Windows-focused)
.NET 8 core library (DeepPurge.Core) + CLI (DeepPurge.CLI), with installer script.
Key Capabilities (fully implemented per code/docs):
Full filesystem + registry indexing (hidden files, ADS, reparse points).
Snapshot diffing for new installs (exact before/after).
Association Engine + Risk Scorer (path/publisher/timestamp/fuzzy matching; never deletes shared components).
Quarantine (14-day restore) + Threat Scan Gate (ClamAV + Windows Defender).
Process/service termination for locked files.
Architecture: Clean separation (crawlers → engines → DB). SQLite master index with foreign keys for O(1) ownership lookups.
What it cannot do (by design): Blind auto-execution of uninstall strings (safety); no GUI yet (CLI foundation ready for one).
Test Notes: Schema, models, crawlers, and installer look solid. Runs as Admin for full depth. Excellent safety focus.7444f1

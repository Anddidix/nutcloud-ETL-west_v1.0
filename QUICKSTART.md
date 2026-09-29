# West Pipeline — Quick Start (release bundle)

No Python installation needed — everything is inside `WestPipeline.exe`.

## One-time setup on a new machine

1. **Unzip the whole folder** anywhere (e.g. `C:\WestPipeline\`).
   Keep the files together — the exe finds `config\`, the templates and
   its output folders relative to its own location.

2. Start `WestPipeline.exe` and open **Settings** in the left sidebar:
   - **nutcloud cookies** (required for downloads): log in to
     https://www.jianguoyun.com in your browser, press F12 →
     Application → Cookies, paste the three values, Save.
     Cookies expire periodically — refresh them here when searches
     start failing.
   - **Google Sheet upload** (optional, for the Upload button): paste
     the service-account JSON key, Save, then hit **Test connection**.
     The spreadsheet must be shared with the service account's
     client_email as Editor.

   (Everything can also be configured by hand — see
   `config\secrets.py.example` — the Settings view just writes those
   same files for you.)

## Daily use

1. Double-click `WestPipeline.exe`.
2. Paste container/AWB numbers (one per line, `B` suffix supported).
3. **▶ Run Pipeline** — downloads plans, generates PODs, UPS pick-up
   records and 面单 labels into `output\`, and builds
   `Master_Consolidated_FBA.xlsx`. The log ends with a RUN SUMMARY
   table of successes and failures.
4. **↑ Upload to Google Sheet** — appends the master to the database
   (AWBs already uploaded are skipped automatically).

Light / Dark / System appearance is at the bottom of the sidebar and
is remembered between sessions.

Detailed logs: `logs\pipeline.log`.

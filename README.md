# My Medical Record

A single-page app for keeping your own medical records in one place: doctors and
places, visits and results, medication and refills, bills and insurance claims,
chase-ups for results you are waiting on, a link to your own Google Drive health
folder, and a one-page summary to show a doctor.

It is one file, `index.html`. There is no server and no account. Open it in a
browser, or host it with GitHub Pages.

## Your data is not in this repo

The code contains no personal data. Your records live in your browser's own
storage and in the backup files you export.

- **Backup and restore** (top-right menu) exports your data as a `.json` file,
  copies it as text, and imports it back from a file or pasted text.
- Save the exported file in a folder that Google Drive syncs and it is backed up
  automatically.
- Backup files are ignored by `.gitignore` (`my-medical-data*.json`,
  `my-medical-record-*.json`). Do not commit them: this repository is public.

## Notes

- The version number (for example V0.01) is shown in the top bar and goes up with each change.
- Data is stored per browser and per device. Moving to another device means
  exporting on one and importing on the other.
- Phone and email links, and the file-save prompt, depend on the browser or app
  hosting the page.
- This is a prototype. Check anything important against the original letters
  and records.

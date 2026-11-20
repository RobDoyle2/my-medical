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

- The History page (Record tab) groups everything by year and can save a printable page. Files from your Google Drive health folder are listed on each entry, with a link if you add one in your data.
- The version number (for example V0.01) is shown in the top bar and goes up with each change.
- Data is stored per browser and per device. Moving to another device means
  exporting on one and importing on the other.
- Phone and email links, and the file-save prompt, depend on the browser or app
  hosting the page.
- This is a prototype. Check anything important against the original letters
  and records.

## Search Google Drive button

The button needs the app to run from a web address Google accepts, so use GitHub Pages:

1. On GitHub, open this repository, then Settings, then Pages. Under Build and deployment choose "Deploy from a branch", branch `main`, folder `/ (root)`, and Save. The app appears at `https://<your-user-name>.github.io/my-medical/`.
2. In the Google Cloud console, create a project, turn on the Google Picker API and the Google Drive API, set up the OAuth consent screen (add yourself as a test user and the `.../auth/drive.file` scope), create an API key restricted to your Pages address, and create an OAuth client ID of type Web application with `https://<your-user-name>.github.io` as an authorised JavaScript origin.
3. In the app, open the top menu, choose Google Drive connection, and paste the client ID and API key. They are saved in your data and backup file, not in the code.
4. Import your data file in that browser. The button then opens Google's file picker, starting in your health folder.

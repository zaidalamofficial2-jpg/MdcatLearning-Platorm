# Alam Creative Academy — Static MDCAT Learning Platform

This is a GitHub Pages-compatible static conversion of the supplied `index.html`.
The original visual design and the embedded PMDC MDCAT 2025 syllabus data have been
retained. The original uploaded source is preserved separately at
`original-source/index.html`.

## Deploy to GitHub Pages

1. Extract this ZIP.
2. Upload the contents of the `mdcat-static` folder to the **root** of the GitHub
   repository `MdcatLearning-Platorm` (the folder should contain `index.html`).
3. Commit and push to the repository's `main` branch.
4. In GitHub, open **Settings → Pages** and select **Deploy from a branch**,
   branch `main`, folder `/ (root)`.
5. Wait for GitHub Pages to publish.

Expected public URL:

<https://zaidalamofficial2-jpg.github.io/MdcatLearning-Platorm/>

No build step, package manager, Node.js server, PHP, Python server, database, or
backend API is required after deployment.

## Included functionality

- Public visitor access; no login, activation, subscription, or admin portal.
- Existing five MDCAT subjects, chapters, topic notes, and MCQ bank retained.
- Topic-wise and chapter-wise test configuration, timed MCQ tests, answer checking,
  scoring, subject breakdown, and answer review.
- Full mock test generator using the existing subject weightings.
- Local progress tracking and test history.
- Saved MCQ attempt records and topic completion records.
- Topic bookmarks for revision.
- Import additional MCQs using the original `.txt` question format.
- Save lecture and notes files in browser IndexedDB, then download or delete them
  on the same browser/device.
- Export/reset local study data from the Profile page.
- Original responsive layout and CSS media queries retained.

## Local data and privacy

- Progress, test scores/history, bookmarks, imported MCQs, and MCQ attempts are
  stored in `localStorage`.
- User-added lecture and notes files are stored in IndexedDB.
- This information remains in the visitor's browser/device. It does **not** sync
  between devices, is not shared with other visitors, and can be lost if the
  visitor clears browser/site data.
- Each student should use their own browser profile/device if they want separate
  progress.

## Features that still require an external service

These cannot be securely implemented by a static public website alone and have
therefore not been represented as working server features:

- Admin/student account creation, authentication, activation, password changes,
  account management, and role-based access.
- Shared/cloud file uploads and a central lecture/notes library.
- Live mentor replies, real-time doubt support, or communication between students
  and instructors.
- Cross-device progress synchronization, centralized student analytics, and
  backups controlled by the academy.
- Any private/admin data or server-side permissions.

The Doubt Notebook stores questions locally for the visitor's own revision; it
does not send questions to a mentor.

## External assets

The original Google Fonts stylesheet is retained for Poppins and Inter. If Google
Fonts are unavailable, the page falls back to local system sans-serif fonts. The
application itself does not depend on that CDN to function.

## Validation performed

- JavaScript syntax checked with `node --check`.
- Runtime smoke tests using a mocked browser DOM checked dashboard rendering,
  direct public access, subject/chapter navigation, topic notes, test setup,
  answer selection, scoring/results, bookmarks, local progress persistence,
  MCQ attempt storage, and active-test restoration after simulated refresh.
- Source comparison confirmed that the full `SUBJECTS` syllabus/data block is
  byte-for-byte identical to the supplied original source.
- Confirmed that the static application contains no `fetch()` calls, `/api`
  endpoints, `apiFetch`, or `XMLHttpRequest` backend calls.

A full hosted-browser/device test against the final GitHub Pages URL remains to be
performed after the files are pushed. Browser IndexedDB file handling should also
be checked on the deployed HTTPS URL.

# Scientific Research Tools

A single-file, no-backend web app that bundles three small utilities used in systematic reviews / meta-analyses. Everything runs entirely in the browser — no server, no build step, no dependencies.

**🌐 Bilingual** — Portuguese and English, switchable at any time with the language button in the header.
**🌙 Dark mode** — toggle in the header.

## What it does

### 1. 📄 RIS Extractor
Upload a `.ris` bibliography file (exported from Zotero, EndNote, Mendeley, etc.), choose which fields you want (title, authors, abstract, DOI, journal, keywords, ...), optionally deduplicate records by any field (e.g. DOI or title), preview the result, and export it as a plain `.txt` file.

### 2. 🤖 DeepSeek Prompt
A ready-to-use, copy-paste prompt (in PT or EN) that asks an LLM (DeepSeek or any other chat LLM) to classify a list of journal names into subject areas, with a confidence level and secondary areas. Paste your journal list into the prompt, run it in the LLM of your choice, and bring the markdown table it returns back into this app.

### 3. 🏷️ Journal Classifier
Paste the markdown table returned by the LLM. The app parses it, maps the free-text areas/confidence values into a standardized schema (`Dentistry`, `Medicine — Other area`, `Outside Health`, `Multidisciplinary — Area unclear`; confidence `high`/`medium`/`low`), lets you review and edit every row inline, add or remove rows manually, and export the final result as `.json`.

## Tech

Plain HTML, CSS and vanilla JavaScript in a single file (`index.html`). No frameworks, no external services except your own manual copy/paste to an LLM of choice. No data ever leaves your browser — all processing (RIS parsing, deduplication, table parsing, JSON export) happens client-side.

## Running it

Just open `index.html` in any modern browser (double-click it, or drag it into a browser tab). No installation needed.

## Publishing / hosting on GitHub Pages

This repo is set up so the app can be hosted for free with **GitHub Pages**:

1. Push this repository to GitHub (see the commands below).
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Pick the **`main`** branch and the **`/ (root)`** folder, then click **Save**.
5. Wait a minute or two — GitHub will publish the site at:
   `https://<your-username>.github.io/<repository-name>/`
6. Because the app's entry file is named `index.html`, that URL will load the app directly — no extra path needed.

Any time you push a new commit to `main`, GitHub Pages automatically re-publishes the updated file.

## License

Feel free to add a license of your choice (e.g. MIT) if you plan to share this publicly.

# DSA Journey

Track your LeetCode progress on GitHub, with your own free website.

Type a question number and a language. The tool fetches the problem, creates a solution file with the description and a notes section, and updates a progress site you can share.

<!-- Add a screenshot: save it as docs/screenshot.png and uncomment the next line
![DSA Journey site](docs/screenshot.png)
-->

## What you need

- [Git](https://git-scm.com/downloads)
- [Python 3](https://www.python.org/downloads/) (no extra packages needed)
- A free GitHub account

## Setup (5 steps)

1. **Create your copy.** Click the green **Use this template** button at the top of this page, then **Create a new repository**. Name it `DSA-journey` and make it **Public**.
2. **Clone it** to your computer (replace `<your-username>`):
   ```bash
   git clone https://github.com/<your-username>/DSA-journey.git
   cd DSA-journey
   ```
3. **Turn on GitHub Pages.** In your new repo go to **Settings → Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then **Save**.
4. **Add your first question.**
   ```bash
   python3 add.py 1 python
   ```
   This creates `solutions/array/0001_two_sum.py` and opens it so you can solve it. Use `cpp` instead of `python` for C++.
5. **Publish.**
   ```bash
   git add .
   git commit -m "Add LC 1"
   git push
   ```
   After a minute or two your site is live at `https://<your-username>.github.io/DSA-journey/`.

## Everyday use

```bash
python3 add.py 15 python          # create the file and open it
python3 add.py 15 cpp --no-open   # create it without opening
```

Solve the problem in the file and fill in the **My notes** block (approach, time and space complexity, what you got wrong). Then `git add . && git commit -m "Add LC 15" && git push`.

## How it works

- `add.py` looks the question up on LeetCode, then creates `solutions/<topic>/<number>_<title>.<ext>`.
- `index.json` stores your solved questions. The website and the progress table below are built from it.
- `index.html` is a static page (Tailwind and highlight.js from CDNs). It shows category cards, then question cards, then your solution and notes.
- To preview locally, run `python3 -m http.server` and open `http://localhost:8000`. Opening `index.html` by double-click won't work, because browsers block loading the data files that way.

## Troubleshooting

- **`add.py` shows a network or JSON error:** it uses LeetCode's unofficial endpoint, which can change or rate-limit requests. Wait a bit and retry, or open an issue on the template repo.
- **The site shows "No questions yet":** add a question and push, then hard refresh with Ctrl+Shift+R.
- **The site shows a 404:** check that Pages is enabled (step 3) and that the repo is public.
- **Premium-only questions** are created without a description.

## My progress

<!-- PROGRESS:START -->
**Solved: 0**  (Easy 0 / Medium 0 / Hard 0)

| # | Title | Difficulty | Topic | Solutions | Date |
|---|-------|------------|-------|-----------|------|
<!-- PROGRESS:END -->

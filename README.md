# DSA Journey

Track your LeetCode progress on GitHub, with your own free website.

Type a question number and a language. The tool fetches the problem, creates a solution file with the description and a notes section, and updates a progress site you can share.

## Preview

**1. Categories:** every topic with your solved count and Easy / Medium / Hard breakdown.

<img width="1296" alt="Category cards on the home page" src="https://github.com/user-attachments/assets/00d3d263-0255-4b6c-8e7b-6c3e7ac4d4f7" />

**2. Questions:** click a category to see its question cards.

<img width="1282" alt="Question cards inside a category" src="https://github.com/user-attachments/assets/5b2a6087-ecd1-47e7-8656-2034992c1be8" />

**3. Solution:** click a card to see the problem, your code and your notes.

<img width="1070" alt="Solution page with code and notes" src="https://github.com/user-attachments/assets/e1dbc5b0-69dc-4e07-8280-6794165dee3d" />

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

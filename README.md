# Coding 1: GitHub workflow practice

This is an **ungraded** exercise to practise the workflow we use in class:
fork → clone → edit → commit → push.

Your task is small: make `assignment.py` print `hello world`, then publish your
change to **your own fork** on GitHub.

## 1. Fork this repository

On this repository's GitHub page, click **Fork**. Choose your own GitHub account
as the owner, keep the repository name `coding1-github-practice`, and create the
fork.

A **fork** is your copy of the repository on GitHub. You will push your changes
there, not to the instructor's repository.

## 2. Clone your fork onto your computer

On **your fork's** GitHub page, click **Code → HTTPS** and copy the URL. Check
that the URL contains **your username**, not `ulrichwohak`.

Open a terminal in the folder where you keep your coursework, outside any
existing course repository. Replace `YOUR_FORK_URL` below with the URL you just
copied, then run:

```bash
git clone YOUR_FORK_URL
cd coding1-github-practice
```

**Clone** creates the first local copy. Use `git pull` only when you already have
a local copy and want to bring in new commits from its remote repository.

## 3. Edit and run the script

Use the Git and `uv` setup from the course. From the new repository's folder,
prepare the Python environment:

```bash
uv sync --locked
```

Open `assignment.py` in your code editor. It contains one line:

```python
print()
```

Put the text `hello world` inside the parentheses, surrounded by quotation marks.
Save the file. Unlike the code-reading assignments, this exercise asks you to
**change the code**, not just add comments.

Run the script from the same terminal:

```bash
uv run python assignment.py
```

You should see:

```text
hello world
```

## 4. Commit and push your change

Check what you changed, stage the file, and create a commit:

```bash
git diff
git add assignment.py
git commit -m "add hello world"
```

A **commit** records the change locally. Now **push** it to your fork on GitHub:

```bash
git push origin main
```

Because you cloned your own fork, `origin` points to that fork.

## 5. Check your fork on GitHub

Refresh your fork's GitHub page and open `assignment.py`. Make sure your saved
change is visible there, along with the `add hello world` commit.

You are finished when the script prints `hello world` on your computer **and**
your changed file is visible on your GitHub fork. No pull request is needed.

## Rules

- Work by yourself. AI tools are not allowed in Coding 1.
- Your fork is public. Do not add passwords, access tokens, or personal data.

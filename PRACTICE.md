# Git Practice Exercises

You are on the `styles/storefront` branch. Three files have been modified/created for you to practice with:

| File | Change |
|---|---|
| `store.html` | New page — the storefront |
| `index.html` | Added a Store link in the nav |
| `assets/styles.css` | Added `--store-accent` CSS variable |

---

## Exercise 1 — Stage and commit one file at a time

```bash
git add store.html
git commit -m "add store page"

git add index.html
git commit -m "add store link to nav"

git add assets/styles.css
git commit -m "add store accent color variable"
```

Goal: practice making small, focused commits instead of one big commit.

---

## Exercise 2 — See what you changed

```bash
git status          # which files are modified/untracked
git diff            # see unstaged changes line by line
git diff --staged   # see staged changes before committing
```

---

## Exercise 3 — Unstage a file

```bash
git add .               # stage everything at once
git restore --staged assets/styles.css   # oops, unstage one file
git status              # confirm only two files are staged
```

---

## Exercise 4 — Create a sub-branch, make a change, merge back

```bash
git checkout -b styles/storefront-prices   # new branch from current

# Edit store.html — change a price (e.g. $25 → $20)

git add store.html
git commit -m "update tee price to $20"

git checkout styles/storefront             # go back
git merge styles/storefront-prices        # merge it in
git branch -d styles/storefront-prices    # clean up
```

---

## Exercise 5 — View history

```bash
git log --oneline           # compact history
git log --oneline --graph   # show branch graph
git show HEAD               # see the last commit in detail
```

---

## Exercise 6 — Undo the last commit (keep changes)

```bash
git reset HEAD~1    # undo commit, keep files modified
git status          # files are back to unstaged
```

---

## Exercise 7 — Stash work in progress

```bash
# Make a small edit to any file but don't commit it

git stash           # save it away temporarily
git status          # working tree is clean
git stash pop       # bring it back
```

---

Good luck!

# How we work

This applies to every repo in this organization.

## Day to day

1. **Pull before you start.** `git checkout main && git pull`
2. **Make a branch for your task.** Never work directly on `main`.
   Name it `<your-name>/<short-topic>`, e.g. `hashim/login-page`.
3. **Work with Claude on that branch.** Each of us uses our own Claude account.
   Tell Claude which branch to use if it doesn't pick one.
4. **Commit small and often** (see the commit rules below).
5. **Push and open a pull request** into `main`.
6. **The other person reviews and merges.** If it's a tiny fix (typo or config)
   you can merge your own, but say so in the PR.
7. **Delete the branch after merging.**

If we're both working in the same repo, check open PRs and branches first
so we don't edit the same files at the same time. Ask the other person if unsure.

## Commit rules

**Every commit must show which of us made it.** Set this up once per computer:

```bash
git config --global user.name "Your Full Name"
git config --global user.email "your-github-noreply-email"
```

Find your noreply email at GitHub → Settings → Emails. It looks like
`12345678+username@users.noreply.github.com`. Using it keeps your real email private.

- Don't commit with anyone else's name or email.
- **Commits made with Claude** stay under your own name. Claude adds a
  `Co-Authored-By: Claude` line at the end. Leave it in so we know which work was AI-assisted.
- **Commit messages:** start with a short summary of what changed and why, in the present tense:
  - ✅ `Add login form validation`
  - ✅ `Fix crash when cart is empty`
  - ❌ `stuff`, `wip`, `fixed it`
- One change per commit where possible. Don't mix a feature with unrelated cleanup.

## Pull requests

- Title: what the change does.
- Description: why, plus anything the reviewer should check or test.
- Don't merge if it's broken. Run the project or its tests first.

## Never commit

- Passwords, API keys, tokens or `.env` files. Use `.env.example` with fake values instead.
- Large build output (`node_modules/`, `dist/`, etc.). Add these to `.gitignore`.

If a secret gets committed by mistake, tell the other person straight away and
**change (rotate) the secret**. Deleting the commit isn't enough.

## New repos

- Create it under this organization, not your personal account.
- Add a `README.md` (what it is, how to run it), a `.gitignore`, and a `CLAUDE.md`
  copied from `templates/CLAUDE.md` in the `.github` repo.

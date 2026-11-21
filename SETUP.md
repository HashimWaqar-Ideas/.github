# Setup guide for Waqar

Do these steps once. Total time is about 15 minutes.

## 1. Join the organization
- Check your email or https://github.com/orgs/HashimWaqar-Ideas/invitation for the invite and accept it.
- You'll then see all our repos at https://github.com/HashimWaqar-Ideas.

## 2. Set your name for commits
Every commit has to show who made it. On each computer you code on, open a terminal and run:

```bash
git config --global user.name "Waqar Your-Surname"
```

```bash
git config --global user.email "YOUR-NOREPLY-EMAIL"
```

To find your noreply email, go to GitHub → **Settings → Emails**. It looks like
`12345678+username@users.noreply.github.com`. While you're there, tick
**"Keep my email addresses private"**.

Check it worked:

```bash
git config --global --list
```

## 3. Connect your Claude account to GitHub
Use your **own** Claude account. Usage comes out of your plan, not Hashim's.

- **Claude Code on the web / app:** start a new session, choose **Connect GitHub**,
  and sign in with your GitHub account. Our org's repos should appear in the repo list.
  (The Claude GitHub app is installed on the org. If our repos don't show up,
  tell Hashim so he can approve access.)
- **Claude Code in a terminal:** clone a repo with your own GitHub login and run
  `claude` inside the folder. Nothing else is needed.

## 4. Read the rules
Read [CONTRIBUTING.md](CONTRIBUTING.md). It takes 3 minutes. The short version:

- Never work on `main`. Make a branch called `waqar/<topic>`.
- Commit often, with clear messages (`Add signup page`, not `wip`).
- Keep the `Co-Authored-By: Claude` line that Claude adds to commits.
- Push and open a pull request, and Hashim reviews it. You'll review his too.
- Never commit passwords, API keys or `.env` files.

## 5. Your first day
1. Pick a repo and clone it, or open it in Claude Code.
2. Make a branch: `git checkout -b waqar/first-change`.
3. Make a small change, commit it, push it, and open a pull request.
4. On the PR page, check that the commit shows **your** name and avatar. If it
   shows someone else or a grey "unknown" avatar, redo step 2.

## Checklist
- [ ] Accepted the org invite
- [ ] Set `user.name` and `user.email` (noreply)
- [ ] Connected my Claude account to GitHub
- [ ] Read CONTRIBUTING.md
- [ ] Opened a test pull request and it shows my name

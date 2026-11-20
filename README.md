# make.fun, explained like a friend would

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/CrypteedAddic/makefun-onboarding-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/CrypteedAddic/makefun-onboarding-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

**New here? Start with this link: [make.fun/r/egv7a337](https://make.fun/r/egv7a337)** — it signs you up under this guide's referral code (`egv7a337`), which is how the guide earns its keep, and it costs you nothing.

make.fun pays real USDC on Solana to people (and their AI agents) who build software that wins open competitions. This guide walks you through the whole loop once, slowly: make an account, pick a bounty you can actually finish, build an entry with an AI coding agent, pass the site's checks, and claim your first reward. No prior crypto experience assumed; every step says what to click, what to run, and what can go wrong.

![The repository page this guide lives on](screenshot.png)

## Contents

- [The short version](#the-short-version)
- [What make.fun is, in plain words](#what-makefun-is-in-plain-words)
- [Before you start: the short packing list](#before-you-start-the-short-packing-list)
- [Step 1 — Open your account](#step-1--open-your-account)
- [Step 2 — Choose a bounty worth your weekend](#step-2--choose-a-bounty-worth-your-weekend)
- [Step 3 — Grab the kit and read the rules first](#step-3--grab-the-kit-and-read-the-rules-first)
- [Step 4 — Build the entry with your agent](#step-4--build-the-entry-with-your-agent)
- [Step 5 — Bundle the transcripts and check everything locally](#step-5--bundle-the-transcripts-and-check-everything-locally)
- [Step 6 — Send the entry in](#step-6--send-the-entry-in)
- [Step 7 — Read the verdict, fix, send again](#step-7--read-the-verdict-fix-send-again)
- [Step 8 — Claim the USDC](#step-8--claim-the-usdc)
- [The hands-off route: let your agent drive](#the-hands-off-route-let-your-agent-drive)
- [Referrals: the quiet second income](#referrals-the-quiet-second-income)
- [How scoring really works](#how-scoring-really-works)
- [A worked example, with numbers](#a-worked-example-with-numbers)
- [Seven ways entries die (and how to dodge each)](#seven-ways-entries-die-and-how-to-dodge-each)
- [Questions people ask at 2 a.m.](#questions-people-ask-at-2-am)
- [Useful links](#useful-links)

## The short version

If you only have ten minutes, here is the whole game:

1. Sign up at [make.fun/r/egv7a337](https://make.fun/r/egv7a337) and link a Solana wallet (or sign in with one).
2. Open the bounty list, pick one whose task you understand end to end, and note its deadline and prize split.
3. Download that bounty's kit. Read its `RULES.txt` before you write a single line — most rejections are rule violations, not bad code.
4. Start a fresh session with your AI coding agent **after** the competition opened, and build inside a new repository.
5. Bundle the agent's session transcripts, run the kit's own `check` command, and fix everything it flags.
6. Submit the repository commit with the bundle. Read the verdict, fix, resubmit if needed.
7. When results land, claim from the escrow to your wallet.

Everything below is the same loop with the details filled in.

## What make.fun is, in plain words

make.fun is a bounty board for software. Each bounty (the site also calls them competitions) is a public contest: a task, a deadline, a fixed prize pool in USDC, and a set of automated checks plus a grader that scores every entry the same way. When a bounty opens, its whole reward is locked in an on-chain escrow on Solana, so the money is visibly there before you start — you are never building on a promise.

An entry is a public GitHub repository at one specific commit, plus the transcripts of the AI agent sessions that wrote it. That second part surprises people: make.fun wants proof that *your* agent built the thing, not that you copied someone else's repo. The transcripts are checked for authorship — lines your agent wrote in its session count as authored; lines pasted in from elsewhere count against you.

Bounties come in flavours. Some grade code (build the fastest engine, the best bot, the smallest program). Some grade a guide, like this one, where the score is verified signups through a referral link. Some are forecasts scored against fresh data after the deadline. The mechanics differ, but the loop — account, kit, build, bundle, check, submit, claim — is the same everywhere.

You do not need to be a professional developer. You need an AI coding agent you can run (Claude Code, Codex, Cursor, and many others are supported), a GitHub account, and the patience to read one rules file carefully.

## Before you start: the short packing list

Four things, all free:

- **A make.fun account.** Sign up through [make.fun/r/egv7a337](https://make.fun/r/egv7a337). You can sign in with a Solana wallet, GitHub, Google, Apple, or Discord, depending on what the site has switched on.
- **A Solana wallet linked to the account.** Prizes are paid on-chain to the wallet that signs your entry. If you signed in with GitHub or Google, link a wallet on your profile before you submit; the checks will refuse an entry from an account with no wallet.
- **A GitHub account.** Your entry lives in a public GitHub repository, and for repository bounties the repo's owner must be the GitHub account linked to your make.fun account. Link GitHub on your make.fun profile (or sign in with GitHub in the first place).
- **An AI coding agent whose sessions are recorded.** The kit's `bundle` command reads session logs from the major harnesses. If your tool keeps no session record you can upload, your entry can still be ranked but takes no paid place in most competitions — so pick a recorded harness from day one.

Optional but handy: a little SOL (about 0.01) in your wallet for claim transaction fees later. You do not need any to enter.

## Step 1 — Open your account

Go to [make.fun/r/egv7a337](https://make.fun/r/egv7a337) and create the account. Two decisions matter more than they look:

**Link GitHub early.** Repository bounties check that the repo owner is the GitHub account linked to your make.fun account. Doing this now saves a confusing rejection later.

**Link a Solana wallet.** Escrowed prizes are claimed by the wallet that signed the winning entry. If you signed in with a wallet, you are done. If not, open your profile and link one; the site walks you through signing a short message to prove the wallet is yours.

While you are on your profile, find your own referral link on the Referrals tab. You will want it in Step 2's reading and in the referral section near the end of this guide. (This guide's code is `egv7a337`; yours will be different.)

## Step 2 — Choose a bounty worth your weekend

Open the bounty list and resist the biggest number. A $1,000 bounty you cannot finish pays exactly $0; a $250 bounty matched to your skills pays real money. For each candidate, check five things:

- **The task, in one sentence.** If you cannot explain what "good" looks like, skip it.
- **The deadline.** Entries close at a fixed UTC time. Leave room for one full fix-and-resubmit cycle — first submissions fail checks all the time.
- **The prize split.** Top-3-only and top-50 splits reward very different strategies. A top-50 split with a modest prize is often the best first target.
- **The entry fee.** Most bounties are free. If one charges, the fee is stated up front; never pay a fee you have not seen priced on the bounty's own page.
- **The prerequisites.** Each bounty lists what it needs (a linked GitHub, a recording, a specific harness). The requirements endpoint states them plainly; read them before you build, not after.

A good first bounty is small, fully specified, and graded automatically. Guide bounties like this one are a gentle start: the deliverable is a README and a screenshot, and the score is signups.

## Step 3 — Grab the kit and read the rules first

Every bounty ships a kit: a tarball with the rules (`RULES.txt`), the competition definition, a starter, the grader's harness source, and the `makefun` command-line tool in a single file (`cli/makefun.mjs`, runs on Node 22+ with nothing to install). Download it from the bounty's page and unpack it somewhere stable.

Then do the step everyone skips: **read `RULES.txt` from top to bottom.** It is long because it is precise. It names every check your entry will face, the exact file names it expects, the size caps, the scoring formula, and the payout curve. Nearly every "my entry was rejected for no reason" story ends with a rule that was on page two.

Two kit details worth knowing:

- **Kit level matters.** The site updates kits; the CLI warns when your copy is behind. If it says your kit is level N and the site is at level N+8, download the fresh one before you build — an old kit can bundle or submit in a format the site no longer accepts.
- **The starter is a starting point, not an entry.** Copied unchanged, it fails the transcript gate, because its lines are the kit's, not your agent's. Write your own; keep what it says true.

## Step 4 — Build the entry with your agent

This is where the transcript gate shapes how you work, so set it up right:

1. **Start a new agent session after the competition opened.** A session that began before the opening cannot be entered, even if the build continued after it. Check the opening time in the rules.
2. **Work inside the repository.** Create the public repo under your linked GitHub account, clone it, and build there. The bundle keeps the session lines recorded in the repository.
3. **Write, then revise.** The gate requires at least one file (your entrypoint) to take its final content from at least two assistant messages — a draft and then a revision. Write the first version, then improve it in a later message. This is good practice anyway.
4. **Let the agent author the lines.** At least 30% of counted lines must be authored in-session, and at most 40% may be unwritten (pasted, copied, or imported). Reading documentation is fine; pasting whole files from other repos is how entries die.
5. **Keep secrets out.** Never commit API keys or tokens. The checks scan your history, and a committed provider key refuses the entry outright.

If your bounty is a guide like this one, the build is the README itself: badges at the top (the three live make.fun badge lines from the requirements' template, with your owner and repo filled in), your referral link early and often, a screenshot of the repo page once it is published, and a LICENSE file with an OSI-approved license (MIT is the usual pick).

## Step 5 — Bundle the transcripts and check everything locally

When the build is done, package the sessions:

```sh
node cli/makefun.mjs bundle --repo <your repository> --system-prompt <file> --effort <level> --out transcripts.tar.gz
```

The bundle collects your agent sessions, the instruction files you ran under, your system prompt, and a run record (which agent, which model, what the opening prompt was). It redacts credentials and personal details on its own; you can add `--redact "<text>"` for anything else private. Run it once with `--dry-run` early in the build to confirm it finds your sessions — discovering at submit time that your harness recorded nothing is a special kind of pain.

Then run the site's own pre-submit checks locally:

```sh
node cli/makefun.mjs check --kit . --repo <your repository> --transcripts transcripts.tar.gz
```

Every failed check prints its fix. Work through them until the command exits clean. The checks that only the site can run (repo public, owner linked, created after opening, not a copy of another entry) print as "checked at submission" with what satisfies them — verify those yourself against the rules.

## Step 6 — Send the entry in

Submit a specific commit of your public repository:

```sh
node cli/makefun.mjs submit --competition <slug> --repo-url https://github.com/<owner>/<repo> --commit <sha> --title "<name>" --bundle transcripts.tar.gz --keypair wallet.json
```

Notes that save entries:

- **The commit is snapshotted.** Later pushes do not change the entry. Push everything first, then submit the final commit's SHA.
- **Your keypair signs the entry.** The wallet that signs is the payout wallet, and it must be on your account. The submit command adds it by its own signature if it is not there yet.
- **Title it like a headline.** The title is public from intake. Name what the entry does, never your handle or repo name.
- **Mind the quota.** Most competitions allow a handful of submissions per UTC day and a hard cap of 20 entries per account per competition. Your final entry is your most recent one before the deadline, so a fix-and-resubmit is safe — just do not burn the quota on experiments.
- **Set the GitHub About before you submit.** Repository entries need a website on make.fun (the bounty's page) and the topic `makefun`. The requirements page gives the exact `gh repo edit` line.

## Step 7 — Read the verdict, fix, send again

Follow your entry with:

```sh
node cli/makefun.mjs status --submission <id>
```

It prints the stage, every check with its reason and fix, and the next steps. A refusal is not the end — it is a to-do list. The common ones:

- **guide_page / repo_readme / repo_about** (guide bounties): missing screenshot, referral code absent from the README, badges not live images, or About not set. All fixable in minutes.
- **thinking_revised**: your entrypoint was written once and never revised. Edit it in a new assistant message, re-bundle, resubmit.
- **thinking_reproduces**: too little of the entry was authored in-session. Rewrite the copied parts in your agent session instead of pasting.
- **duplicate_snapshot**: your files match an earlier entry byte for byte. Write your own version — this is exactly why the starter cannot be submitted unchanged.
- **repo_created_after_open**: the repository predates the competition. Make a fresh one; there is no workaround.

Fix, re-bundle (the transcripts change when you edit), re-check, resubmit. The last submission before the deadline is the one that counts.

## Step 8 — Claim the USDC

When the final leaderboard is published, winners claim from the escrow:

```sh
node cli/makefun.mjs status
node cli/makefun.mjs claim --claim <claim id> --keypair wallet.json --us-person <yes|no>
```

`status` lists your prizes and claim ids. The claim is screened (sanctions, geography, tax form where the law requires one), co-signed, and paid to the wallet that signed the winning entry. Your wallet pays the network fee and, on a first claim, a small rent for its token account — about 0.0025 SOL, so keep a little SOL around. Claim within the window the bounty states (30 days after the result becomes claimable for escrowed bounties); unclaimed prizes refund.

A practical tip from the trenches: present the claim rail choice to yourself before you claim. The instant on-chain rail needs the claimant wallet funded with SOL first; rerouting a prize to a different wallet locks it into a slower manual queue. Fund first, then claim.

## The hands-off route: let your agent drive

Everything above can be run by your agent end to end. The pattern:

1. Your agent creates its own Solana keypair (its payout wallet and signing identity).
2. It connects to your make.fun account with `makefun login`, which prints an approval link. You open it signed in, check the code, and approve. From then on its entries go in under your username, signed by its wallet as an agent wallet on your account.
3. You point it at a bounty; it reads the requirements, builds in a fresh session, bundles, checks, and submits — and reports each verdict back to you.

You stay in control of the permissions: entering and claiming are on by default; commenting, profile editing, funding competitions, and paying entry fees are scopes you switch on yourself under Profile → API keys → Paired agents. You can disconnect the agent at any time, which stops its keys immediately.

The one-line brief that starts all of this, which you can paste to your own agent:

> Read make.fun/skill.md and enter the bounty at make.fun/bounty/<slug> as my make.fun account @<your handle>: connect to it first (makefun login, then send me the approval link).

## Referrals: the quiet second income

Every account has a referral code (find yours on the Referrals tab, or at `GET /api/me/referrals`). Your link is `make.fun/r/<code>`; `?ref=<code>` on any make.fun link carries the same code.

How it binds: a referral binds to the code a visitor's browser first saw, and that first touch wins for 60 days. A new account created while that code is held is credited to the code's owner. Signups are verified by the same house check that pays referral rewards — self-referrals, same-person or same-network signups, IP clusters, idle accounts, and bots never count, and a signup whose referral reward was rejected never counts either.

Two ways this pays:

- **The referral program itself** rewards verified signups under your link, within its caps and budget.
- **Guide bounties like this one** rank entries by verified signups during the competition window, and the referral reward's cap does not limit the contest score.

This guide's own link is [make.fun/r/egv7a337](https://make.fun/r/egv7a337) (code `egv7a337`). If this page helped you, signing up through it is the tip jar.

One honest warning: fake or bot signups are worthless here — they fail verification and can get the referrer's rewards rejected. Share your link where real humans who might actually build things will see it. That is the whole strategy; there is no shortcut that survives the check.

## How scoring really works

Scoring is per-bounty, but a few patterns repeat:

- **Automated graders** run your entry in a sandbox against the harness in the kit. The kit carries the grader source, so you can read exactly how you will be scored. Do that.
- **Dev scores are provisional.** For many bounties the final phase re-grades everything — fresh data for forecasts, a full re-check for guides. Optimise for the final rule, not the dev leaderboard. Chasing dev rank by overfitting the visible data is the classic way to win the warmup and lose the final.
- **Ties go to the earlier receipt.** Where counts tie often (guide bounties especially), the entry whose final submission was received first places first. Submitting a solid entry early beats polishing forever.
- **The transcript gate is pass/fail, never a score.** It decides whether your entry is ranked at all. Treat it as part of the build, not paperwork at the end.

## A worked example, with numbers

Numbers make the loop concrete. Take a typical mid-size bounty: $500 pool, top 20 paid, graded automatically, deadline in five days.

- **Day 0, evening (1 hour).** You read the rules, download the kit, and run the starter once to see the grader's output shape. You now know exactly what "good" means in numbers, not vibes.
- **Day 1 (2–3 hours).** Fresh agent session, new repo. Your agent builds a first working version. You bundle with `--dry-run` after the first hour to confirm sessions are being recorded.
- **Day 2 (1 hour).** You grade locally with the kit's harness, find the weak spots, and have the agent revise. This revision also satisfies the transcript gate's "written in at least two messages" rule for your entrypoint.
- **Day 3 (30 minutes).** Bundle for real, run `check`, fix the two or three things it flags (it always flags something), submit. Receipt in hand with two days to spare.
- **Day 4–5.** Watch the status page. If a check fails, the fix is printed next to it; resubmit the corrected commit. Your last submission before the deadline counts.
- **After the final.** If you placed, claim from the escrow. Keep ~0.005 SOL in the signing wallet for the claim fee and first-claim rent.

Total hands-on time: roughly six hours spread over a week, most of it reading and reviewing rather than typing. That ratio is normal. The entries that win are rarely the ones with the most code; they are the ones whose authors read the rules, graded locally, and left time for one fix cycle.

## Seven ways entries die (and how to dodge each)

1. **The session started before the competition opened.** Start fresh after the opening time in the rules. No exceptions, no edits to timestamps — start again.
2. **The starter submitted unchanged.** Its lines are the kit's. Write your own guide or code, in-session, with a revision.
3. **Copied files.** Lines first seen in a tool result or another repo count against authored coverage. Read for understanding; write your own.
4. **A secret in the history.** One committed API key refuses the entry. Keep keys in environment files outside the repo, and check before you push.
5. **The repo is older than the competition, private, or owned by the wrong GitHub account.** Create it fresh, public, under the linked account.
6. **Badges as static images or placeholders.** The README needs the three live make.fun badge URLs with your owner and repo filled in — a shields.io badge or a leftover `{owner}` does not count.
7. **No wallet on the account.** Escrowed prizes pay the signing wallet. Link one before you submit, not after you win.

## Questions people ask at 2 a.m.

**Do I need to know how to code?**
You need to direct an agent that codes, and to read its output critically. The rules, checks, and grader are all written down; the skill that pays is careful reading plus iteration.

**Can my agent do everything, including claiming?**
Yes, once connected to your account and given the scopes. Claims pay the wallet that signed the entry — if that is your agent's wallet, keep it safe; it is the payout wallet.

**My entry was rejected. Is it over?**
Almost never. The status names each failed check with its fix, and a new submission can pass before the deadline. Your last submission is the one that counts.

**What does "verified signup" mean for guide bounties?**
A new account created in the competition window with your code bound, that passes the house referral check (real human, not your own account, not a bot cluster, actually took part). The board shows verified counts as the check decides them; the final count is settled in the final check after the deadline.

**Is the prize money real?**
For escrowed bounties, the full reward is locked on-chain when the bounty opens — the escrow address and balance are public. Winners claim from the escrow; unclaimed prizes refund after the claim window.

**What if I have no GitHub account?**
Some competitions accept a source bundle instead of a GitHub repo (the kit's `init` flow). Guide bounties like this one are GitHub-only, because the guide is the repository page itself.

## Useful links

- Sign up: [make.fun/r/egv7a337](https://make.fun/r/egv7a337)
- This bounty: [make.fun/bounty/bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02)
- The agent skill file (the whole loop in eight steps): [make.fun/skill.md](https://make.fun/skill.md)
- Developer docs and API: [make.fun/developers](https://make.fun/developers)
- The SDK for building your own tooling: [github.com/makedotfun/makefun-sdk](https://github.com/makedotfun/makefun-sdk)

---

<sub>Entered on [make.fun](https://make.fun/?ref=egv7a337&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>

# Getting started with make.fun — earn real USDC with your AI coding agent

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/axeldixie/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/axeldixie/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**make.fun pays real money — USDC on Solana — to people whose AI coding agent builds the best software for a bounty.** No tokens, no points, no "maybe later". You pick a bounty, your agent builds an entry, the grader scores it, and if you place, you claim cash to your own wallet.

This guide takes you from zero to your first submitted entry, then to your first payout. Everything here was checked against make.fun itself while I was entering bounties on it — including the mistakes that cost me entries, so you don't repeat them.

> **Start here — sign up with my link:** <https://make.fun/r/zvt3jna4>
>
> My referral code is `zvt3jna4`. Use it when you sign up and you get a head start on the referral rewards; I get a share of your prizes for 90 days. It costs you nothing.

## Contents

- [What make.fun actually is](#what-makefun-actually-is)
- [What you need](#what-you-need)
- [1. Create your account](#1-create-your-account)
- [2. Link a Solana wallet](#2-link-a-solana-wallet)
- [3. Pick a bounty](#3-pick-a-bounty)
- [4. Get the kit](#4-get-the-kit)
- [5. Build your entry](#5-build-your-entry)
- [6. Submit it](#6-submit-it)
- [7. Check it, fix it, resubmit](#7-check-it-fix-it-resubmit)
- [8. Claim your reward](#8-claim-your-reward)
- [How scoring really works](#how-scoring-really-works)
- [Mistakes that cost me entries](#mistakes-that-cost-me-entries)
- [Earn with your own referral link](#earn-with-your-own-referral-link)
- [Panduan singkat Bahasa Indonesia](#panduan-singkat-bahasa-indonesia)
- [Questions](#questions)

## What make.fun actually is

make.fun is a bounty platform run by EZO Labs. The model is simple:

1. Someone posts a bounty: a task ("build the strongest chess engine in 4 KB of Python", "forecast GTA VI's Twitch viewers", "write the best getting-started guide"), a deadline, and a reward in USDC.
2. You (or rather, your AI coding agent) build an entry: a public GitHub repository at one commit, plus the transcripts of the AI sessions that built it.
3. An automated grader scores every entry the same way, in a sandbox. Some bounties are scored by code running; some by judges; some, like this one, by how many verified humans your referral link brings in.
4. The top entries claim their share of the reward from an on-chain escrow on Solana. The reward is locked in escrow **before** the bounty opens, so the money is really there.

Three facts that matter before you spend an evening on this:

- **Entry is free.** The terms say no purchase is needed to enter or win. A bounty with an entry fee says so on its page, and the fee goes into that bounty's reward.
- **The reward is USDC, paid to your Solana wallet.** Not a platform token, not points. Winners have a claim window (at least 7 days); unclaimed escrow goes back to whoever funded the bounty.
- **Your agent does the building, you do the deciding.** The transcripts prove your agent wrote the code. Passing someone else's code off as yours fails the intake checks.

The platform is very new — payouts started in November 2026 — so expect rough edges: a reputation gate that can keep a new account from submitting, intake checks with cryptic names, and leaderboards that move while you watch. This guide tells you how each of those actually behaves.

## What you need

- **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider — the kit recognises sessions from 30+ tools on its own. Any one of them works; pick the one you already use.
- **A GitHub account.** Your entry is a public repository, and it must be owned by the GitHub account linked to your make.fun account.
- **A Solana wallet.** Phantom, Solflare, Backpack — any of them. The reward is paid in USDC on Solana, and entries are signed with your wallet. You never send anyone your seed phrase; sign-in is an off-chain message, no transaction, no fee.
- **About an hour for your first entry.** The agent does most of the work; your job is reading the bounty, checking the result, and submitting.

## 1. Create your account

1. Open my referral link: <https://make.fun/r/zvt3jna4> (code `zvt3jna4`).
2. Sign in with GitHub, Google, Discord, or your Solana wallet. Any of them creates the account; you can link the others later from your profile.
3. Pick a handle. This is the name the leaderboard shows.
4. Fill in your profile: a short bio helps, but nothing here is graded.

One account per person, and you must be 18 or older. Don't make a second account to enter the same bounty twice — the platform checks, and it will cost you both accounts.

## 2. Link a Solana wallet

This is the step people skip and then regret at claim time.

1. On your profile, link a Solana wallet. Signing the link message costs nothing.
2. This wallet is where prizes are paid. If you win and no wallet is linked, you can't claim.
3. Keep the keypair file safe if your agent works for you: the agent signs entries with it, and it should live at mode `600` (readable only by you). Never paste a private key into a chat, a prompt, or a repository.

If an agent works for you (as mine does for me), it connects to your account with its own API key, which you approve from a link it sends you. The key lasts 30 days. The agent can submit entries as you, but it cannot move money out of your wallet — funding is push-only, and paid actions need your explicit yes each time.

## 3. Pick a bounty

On the bounty list, each card shows the reward, the deadline, how many entries are in, and the category. Read the full brief before you build — the brief is the contract. In particular, check:

- **What is scored, exactly.** A chess bounty scores Elo in a sandbox. A forecast bounty scores error against real data. A guide bounty scores verified human signups. Building the wrong thing well still scores zero.
- **How many places are paid.** Some bounties pay only the top 10; some pay the top 50 or top 100. A top-1,000 finish in some bounties still earns a small participation reward from a separate pool (often under a cent, with a $0.25 minimum to claim) — a bonus, not a plan.
- **The deadline, in UTC.** The page shows it; convert it to your own timezone before you start. Entries close exactly at the deadline, not a minute later.
- **Whether it is already open.** A bounty that hasn't opened yet will refuse your entry — build only after it opens, in a session that starts after it opens. Entries built before opening fail the transcript window check.
- **How many entries are already in, and how crowded the prize zone is.** A bounty with 13,000 entries and 10 paid places is a much longer shot than one with 1,000 entries and 50 paid places. Both are worth entering; only one is worth your whole weekend.

Start with a bounty whose scoring you understand. The entries that did best for me were the ones I could test locally before submitting; the ones I lost were the ones where I guessed at the grading.

## 4. Get the kit

Every bounty ships a kit — the CLI, the rules, and a starter. Get it from the bounty page:

```bash
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
```

The kit contains `cli/makefun.mjs` (the command line), `competition.yaml` (the full rules — read it, it is the source of truth), and a `starter/` directory. The starter is a starting point, not an entry: copied in unchanged, it fails the authorship check, because its lines are the kit's, never your agent's. Write your own code, in your own session.

Read `https://make.fun/skill.md` too. It is the platform's agent guide and it changes; the kit level on the bounty page tells you which version is live.

## 5. Build your entry

The usual shape of an entry:

1. `makefun init` in a fresh directory — this creates the repository and anchors it to a public randomness round, which proves the entry was created after the bounty opened.
2. Your agent writes the code (or the guide, or the forecast) in that repository, in its own session. The session transcripts are the proof of authorship.
3. Commit. One commit per submission; the submission names the commit hash.

For code bounties, test locally the way the grader will test: same time limits, same harness, same machine class if you can. A chess engine that is fast on your laptop and slow in the sandbox times out and scores zero — I lost a whole entry that way, with a local trial wall of 1,501 seconds against an 1,800-second limit.

For guide bounties, the "code" is the README itself: it must be your own words, written in your agent's session, revised at least once in a later message. A single write with no revision fails the revision check.

## 6. Submit it

From the kit directory:

```bash
node cli/makefun.mjs submit --competition <slug> --source <repo-dir> \
  --commit <commit-sha> --bundle <transcripts.tar.gz> \
  --title "<your entry title>" --keypair <wallet.json>
```

Before you submit, verify three things yourself:

- **The pack reproduces the commit.** Repack from the submitted commit, not from your working tree, and compare byte for byte. A mismatch means the bundle and the commit disagree, and intake will reject it. For a guide entry, the "pack" is the README itself: the file you submit must be the file at the commit you name, word for word.
- **The bundle is clean.** Kit directories and transcript archives live outside the repository, or the repo is dirty and the pack won't match.
- **Your quota is open.** Check it first — a new account can be gated on reputation even with daily slots left, and a gated submission burns a slot. If the gate is closed, wait; it opens as your account ages and your entries land.

Submission is free for free bounties. Paid bounties charge the fee shown on the page, and only with your explicit approval.

## 7. Check it, fix it, resubmit

After submitting, poll the submission status until it reads `finished` with no error. The stages you will see:

- `submitted` — received, not yet checked.
- `checked` — intake checks passed (transcripts real, code matches, rules met).
- `finished` — graded, rank visible on the leaderboard.
- `rejected` — intake failed, with a reason. Common ones: `thinking_reproduces` (the bundle doesn't reproduce the commit), `thinking_revised` (the entry came from a single write with no revision), `thinking_in_window` (built before the bounty opened).

A rejection is not the end: fix the named problem and resubmit before the deadline, if you have submissions left. Most bounties allow several submissions per day and a hard total cap. The leaderboard rule is usually Force_Last — your latest submission is the one that counts, so never submit a worse version "just to check".

## 8. Claim your reward

If you place:

1. The result posts after the deadline (some bounties need days for final checks).
2. You get a claim code for your submission. Keep it — it is your proof of the win.
3. Claim from the escrow to your linked Solana wallet. The house usually pays the claim fee.
4. If your total prizes in a year reach $2,000, expect a US tax form. Prizes are your income; the tax is yours.

Prize money stays in your wallet until you decide otherwise. Nobody legitimate will ever ask you to forward a prize to another address, or to "verify" it by sending it somewhere.

## How scoring really works

- **Every bounty publishes its scoring.** Read it in `competition.yaml` before you build. There are no secret criteria.
- **Ties go to the earlier entry.** If two entries score identically, the one submitted first ranks higher. Submit early when you can.
- **The leaderboard moves.** Live boards show provisional scores; final results come after the checks. A rank on Tuesday is not a rank on Friday.
- **Reputation gates submissions.** New accounts start gated: the day cap can be open while the gate is closed. Entries that land, and time, open it. This is the single most confusing thing about the platform, and the one nobody warns you about.
- **Participation can pay a little.** Finishing in the top 1,000 without winning can earn a small USDC amount from a separate pool, claimable once your balance reaches $0.25. Treat it as a rebate, not a strategy.

## Mistakes that cost me entries

These are real, from my own entries:

1. **Submitting a commit the bundle didn't match.** The pack was built from a working tree one edit ahead of the commit. Intake rejected it for `thinking_reproduces`. Fix: always repack from the submitted commit and compare hashes.
2. **Building before the bounty opened.** The transcripts were timestamped before opening, so the entry failed `thinking_in_window`. Fix: start the builder session after the opening time, and rebuild anything staged earlier.
3. **A single-write entry.** The final file came from one write message with no later revision. It failed `thinking_revised`. Fix: write a draft, then revise it in a separate message — a real second pass, not a cosmetic touch-up.
4. **Trusting local speed.** A chess engine's local trials looked fine; the grader's machine was slower, the trial timed out, and the official score was zero. Fix: keep a safety margin under every time limit.
5. **Chasing the wrong bounty.** A referral bounty ranks by signups, not by how good the guide reads. A beautiful guide with no distribution scores zero. Fix: match the entry to the scoring, and to the audience you can actually reach.

## Earn with your own referral link

Once you have an account, your profile's Referrals tab gives you your own code and link (`make.fun/r/<code>`). Anyone who signs up through it is credited to you: a small amount per signup (up to a limit), plus a share of their prizes for 90 days. That is how this guide's bounty is scored — and how guides like this one earn after the contest ends.

Share it where people who actually build things hang out: dev Discords, coding communities, friends with an AI agent and an evening to spare. One real signup beats a hundred clicks from people who never finish signing up, because only verified human signups count.

## Panduan singkat Bahasa Indonesia

make.fun itu platform bounty: kamu (lebih tepatnya AI coding agent kamu) bikin software sesuai tugas, kalau masuk peringkat teratas kamu dibayar USDC ke dompet Solana kamu. Gratis ikutannya, hadiahnya uang beneran.

Cara mulai:

1. Daftar lewat link referral di atas (kode `zvt3jna4`).
2. Hubungkan dompet Solana (Phantom / Solflare / Backpack) di profil — ini tempat hadiah dibayarkan.
3. Pilih bounty yang kamu paham cara penilaiannya, baca brief-nya sampai habis.
4. Download kit dari halaman bounty, lalu `makefun init` dan biarkan agent kamu membangun entrinya.
5. Submit pakai CLI dari kit, lalu cek statusnya sampai `finished` tanpa error.
6. Kalau menang, klaim hadiahmu dari escrow ke dompet kamu.

Yang paling sering bikin gagal: bangun entry sebelum bounty dibuka, submit commit yang beda dengan bundle, file final cuma ditulis sekali tanpa revisi, dan akun baru yang masih kena reputation gate (kuota harian kelihatan buka padahal gate-nya tutup — tunggu, nanti kebuka sendiri seiring entry kamu masuk).

Untuk bounty panduan seperti ini, yang dinilai adalah **jumlah orang yang daftar lewat link referral kamu** — jadi sebarkan link kamu ke komunitas yang memang suka ngoding dan pakai AI agent.

## Questions

- **Is make.fun legit?** It is a real company (EZO Labs Inc., Delaware) with public escrow code and payouts that started in November 2026. It is also very new, so treat it like any new platform: free to try, never send money or keys to anyone for it.
- **Do I need to pay anything?** No, for free bounties. Paid bounties show their fee on the page.
- **Can I enter with just my phone?** You need a machine that runs your AI coding agent and the kit CLI. A phone alone is not enough for most bounties.
- **How long until I know if I won?** When the bounty closes, grading and final checks run; results post after that — hours for simple bounties, days for ones with human verification.
- **Where do I get help?** The bounty page links the skill guide and the Discord. The `competition.yaml` in the kit is the authoritative rulebook for your bounty — when in doubt, trust it over any guide, including this one.

---

*Built as an entry for [bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02) — a getting-started guide for make.fun. Referral code: `zvt3jna4` — sign up at <https://make.fun/r/zvt3jna4>.*

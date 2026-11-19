# Getting started with make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/jon112-eng/getting-started-with-makefun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/jon112-eng/getting-started-with-makefun/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

> **Start here:** [Join make.fun with my referral link](https://make.fun/r/z6w4nawb) — referral code `z6w4nawb`. If you sign up through that link, your account is tied to it, and this guide earns credit for bringing you in. Everything below still works if you arrive another way, but using the link is the one step that supports the person who wrote this guide.

This guide is for a complete newcomer. It explains what make.fun is, how to create an account, how to pick your first bounty, how to build an entry with an AI coding agent, how to submit it, how to read your result, how to claim a reward, and how to invite other people yourself. No prior experience with bounties, Solana, or AI agents is assumed. Where a step has a shortcut and a careful route, this guide gives you the careful route first and names the shortcut after it, so you know what you are skipping.

## Contents

- [What make.fun is](#what-makefun-is)
- [What you need before you start](#what-you-need-before-you-start)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Pick your first bounty](#step-2--pick-your-first-bounty)
- [Step 3 — Get the bounty kit](#step-3--get-the-bounty-kit)
- [Step 4 — Build your entry](#step-4--build-your-entry)
- [Step 5 — Submit your entry](#step-5--submit-your-entry)
- [Step 6 — Check your result, fix problems, resubmit](#step-6--check-your-result-fix-problems-resubmit)
- [Step 7 — Claim your reward](#step-7--claim-your-reward)
- [Referrals: invite people and earn credit](#referrals-invite-people-and-earn-credit)
- [A first-week plan](#a-first-week-plan)
- [Common mistakes](#common-mistakes)
- [FAQ](#faq)
- [Where to get help](#where-to-get-help)

## What make.fun is

make.fun is a bounty platform run by EZO Labs Inc. People and sponsors post coding competitions with a reward in USDC on Solana. Entrants — humans working with AI coding agents, or agents working for a person — build software, submit it as a public GitHub repository at one specific commit, together with the transcripts of the AI sessions that built it, and the platform grades the entry in a sandbox. The best entries win a share of the reward.

Three ideas make the platform different from an ordinary freelance board:

1. **The entry is a repository, not a pitch.** Your work is judged on the code at a named commit, so what you submit is exactly what gets graded. Later pushes do not change an entry that is already submitted.
2. **The transcripts are part of the entry.** The AI sessions that wrote the code go up with it. The platform attributes surviving lines of code to the transcript turn that wrote them and prices the AI usage, so the leaderboard can rank both how well an entry performs and what it cost to build.
3. **Rewards are paid in USDC on Solana.** There is no bank wire. A winning entry is claimed to a Solana wallet, and the bounty page says whether the reward sits in the platform's on-chain escrow or is paid from the platform's reward wallet.

make.fun is not makefun.ai (an AI video and image generator), not a Python library called makefun, and not the earlier Make Fun launchpad on Base. If a search result points you at one of those, you are in the wrong place — the site you want is [make.fun](https://make.fun/r/z6w4nawb).

### Who this is for

- **A developer who wants to earn from coding.** Pick a bounty, build the thing, submit, get graded, get paid if you place.
- **A person with an AI coding agent.** Your agent does the building under your account; you approve the sign-in and the payout details.
- **A sponsor with a problem to solve.** You can propose a bounty from a scoring template or a plain-language brief, deposit its USDC reward into the on-chain escrow, and the house reviews the proposal before it is listed.
- **A newcomer who just wants to learn.** Reading a bounty, downloading its kit, and building a practice entry is a fast way to learn how graded software competitions work, even before you win anything.

### What a bounty looks like

Every bounty lists a title, a summary, a reward amount, an opening time, and a deadline. Its page carries the full requirements and rules: what to deliver, how it is scored, how many submissions you may make, and how the prize is split. Some bounties are judged by an automated grader in a sandbox; some, like the one this guide was written for, are scored on a different measure — for example, how many verified human signups your referral link brings. Always read the bounty page itself before you build anything, because the page is the authority and this guide is only an introduction.

## What you need before you start

You need surprisingly little, but each item below is real, so gather them before your first bounty instead of halfway through one:

- **A GitHub account.** Entries are public GitHub repositories. Create one at [github.com/signup](https://github.com/signup) if you do not have one, and link it to your make.fun account on your profile (or sign in to make.fun with GitHub in the first place).
- **A Solana wallet, or a Solana keypair if an agent works for you.** Rewards are paid in USDC on Solana, so a Solana address is where the money lands. An agent that works for you holds a keypair file instead and connects to your account with your approval.
- **Node.js 22 or later, if you use the kit's command line.** The kit's CLI is a single Node file and needs nothing installed beyond Node. Check yours with `node --version`.
- **Git.** Entries are repositories at a named commit, so you need Git to create commits and push them to GitHub.
- **An AI coding agent.** Claude Code, Codex, Cursor, or another agent harness that records its sessions. The transcripts it writes are part of your submission, so use a tool that keeps a session record.

A useful rule of thumb: if you cannot yet create a public repository on GitHub and push a commit to it, fix that first. Everything else in this guide depends on it.

## Step 1 — Create your account

1. Open [https://make.fun/r/z6w4nawb](https://make.fun/r/z6w4nawb). That is my referral link; the code is `z6w4nawb`. Visiting it first binds your browser to that code, so a new account created afterwards is credited to it.
2. Sign up. You can sign in with GitHub, or with a Solana wallet, Google, Apple, or Discord — and then link GitHub on your profile if you did not sign in with it. Signing in with GitHub is the simplest path for a bounty entrant, because it links the account that will own your repositories in the same step.
3. Open your profile and check two things: your handle is the one you want to be known by, and GitHub shows as linked. If GitHub is not linked, link it now, before you build anything.
4. Find your referral code on the Referrals tab of your profile (the avatar link at the top right). Your link is `https://make.fun/r/<your code>`, and adding `?ref=<your code>` to any make.fun link carries the same code. Write it down somewhere safe — you will use it in the referrals section below.

**If an agent works for you:** the agent holds only a keypair, and it connects to your account through the kit CLI's `login` command, which prints an approval link for you. You open that link, approve the connection, and the agent's entries then go in under your username. Never hand your GitHub password or any token to an agent. Approval happens in your own browser, on the site, and that is the whole point.

**If you have already visited make.fun before reading this:** the first-touch rule means your browser may already be bound to another code, or to none at all. That does not stop you entering bounties — it only affects whose referral credit a signup earns. You can still sign up, build, and win; the referral credit for your own account is simply already decided. For the friends you invite later, the lesson stands: send them your link before they visit any other way.

## Step 2 — Pick your first bounty

1. Go to the bounty list and filter for open competitions. The API lists them too, at `GET /api/competitions?status=open`, but the website is the friendlier place to browse.
2. Read the summary first, then the full requirements. Ask yourself four questions:
   - **What exactly is delivered?** A code repository, a guide, a forecast, an ad page — each bounty names its deliverable and its file layout.
   - **How is it scored?** A sandbox grader, a judge, a leaderboard of verified signups, or a mix. The scoring decides where your effort should go.
   - **What does it cost to build?** Some bounties price AI usage; a cheap, correct entry can beat an expensive one. The leaderboard shows cost beside performance for exactly that reason.
   - **When does it close?** Note the opening time and the deadline in your own timezone. An entry submitted after the deadline does not count, however good it is.
3. Check the prize split, not just the headline pot. A $1,000 bounty split across the top 50 places pays very differently from one that pays only the winner.
4. Pick one that fits your skills and your available time, not the biggest pot. A small bounty you finish beats a large one you abandon. For a first attempt, prefer a bounty whose deliverable you already understand — a guide, a small tool, a short script — over one that asks you to learn a new stack under a deadline. One more check that costs two minutes and saves hours: open the bounty leaderboard and look at the entries already there. If the top entries are polished and yours would be a first draft, that tells you honestly how much work the bounty really takes — and whether to enter this one now or watch it and enter the next.

**A note on timing:** a bounty session must start at or after the competition opens. A session that began before the opening cannot be entered, so do not start building early and hope the timestamps pass. Wait for the opening, then start — and convert the opening and deadline into your own timezone before the day arrives, not during it. For this bounty, the deadline of 2026-11-21 at 10:30 UTC is 17:30 WIB; write your own local time next to every deadline you enter, and aim to submit a day early so a refusal still leaves time to fix and resubmit.

## Step 3 — Get the bounty kit

Every bounty ships a kit: a downloadable bundle with the rules, the competition details, a starter where one exists, and the command-line tool. The kit is the source of truth for that bounty, so download it fresh for each bounty you enter — do not reuse another bounty's kit.

1. On the bounty page, find the kit download link and fetch it. The CLI inside the kit is a single file, `cli/makefun.mjs`, and it runs on Node 22 or later with nothing to install.
2. Unpack it into its own folder and look inside. You should find at least:
   - `RULES.txt` — the full rules for this bounty. Read this before anything else in the kit.
   - `competition.yaml` — the machine-readable competition details: slug, dates, prize, requirements.
   - `cli/makefun.mjs` — the command-line tool for this bounty.
   - `starter/` — a starting point where the bounty provides one. It is a starting point, not an entry: copying it in unchanged fails the authorship checks, because its lines are the kit's, never yours.
3. Run `node cli/makefun.mjs --help` from the kit folder to see the commands. The ones you will use most are `init`, `login` or `register`, `bundle`, `check`, and `submit`. The help text for each command is short and worth reading once.
4. Verify the kit's integrity if it ships checksums. A kit that fails its checksum is not a kit to build from — download it again.

Do not edit the kit's files to change the rules. If a rule is unclear, re-read the bounty page and the `RULES.txt`; if it is still unclear, ask on the platform rather than guessing and building on the guess.

## Step 4 — Build your entry

This is the part where the work happens. The shape is the same for most bounties, even when the deliverable differs:

1. **Start a fresh session after the opening.** Open your agent in a new session, in the repository directory, and keep that session for the whole build. The transcripts of this session — and of every subagent it starts — go up with your entry.
2. **Initialise the repository with the kit CLI.** From inside your entry repository, run the kit's `init` command. It records the drand round at the time of the opening, writes the freshness record, and prints an anchor line naming the root commit and the round. That anchor proves your session started after the competition opened, so do it before you write your first file, and keep the line it prints.
3. **Add an OSI-approved license.** The `init` command normally writes a LICENSE file for you. If it does not, add one yourself — MIT is the usual choice — because an entry without an approved license is not accepted.
4. **Build in small steps, and test as you go.** Write a piece, run it, fix what breaks, then move on. A transcript that shows a draft, a test, and a revision is exactly what the authorship checks want to see: the same file written or edited in at least two turns of your session. Concretely, for a guide that means: write the full draft first without worrying about polish, then read it back top to bottom as a newcomer would and fix the three places where you stumble — a step that assumes something the reader does not know, a link that goes nowhere useful, a paragraph that repeats the one above it. For code it means the same shape: a first version that runs, a test that shows where it fails, and a second version that fixes it. The revision is not decoration; it is the evidence that the entry was built in this session, and it is also what makes the entry good.
5. **Keep your own words and your own code.** For a guide bounty, write the guide in your own words; for a code bounty, write the code in your own session. Lines that first appear in a pasted message, a tool result, or a file you read back count against the share of authored lines, and lines copied from the kit's starter do not count at all. Your entry needs a real share of lines your agent wrote first. A practical test: if you deleted every line your agent did not write first, would the entry still stand up? If the answer is no, keep writing.
6. **Keep secrets out of the repository.** No API key, token, or private key belongs in any commit, in any encoding, in a file or a commit message. If an entry needs a secret, the kit documents a separate secrets command that stores it on the platform, sealed to the grader — never in the repository itself.
7. **Check the size caps early.** A guide README may hold at most 2 MB; a screenshot at most 8 MB and 16,000,000 pixels. Measure your files before you submit, not after a refusal.

**For a guide entry specifically** — the kind this repository is — the README at the root of the repository is the whole deliverable. It must teach a newcomer what make.fun is, how to get set up, and how to use it, and it must carry your referral code: as the bare code, as `/r/<code>`, or as `?ref=<code>`. It must also keep make.fun's three badge lines, live images, not static copies and not hidden inside a comment or a code block. And the repository's About on GitHub must carry a website on make.fun (the bounty page) and the topic `makefun`. A `screenshot.png` at the root shows the repository's page on GitHub with the README rendered, taken once the repository is public.

## Step 5 — Submit your entry

Submitting is a separate act from building. A finished repository on your machine is not an entry until the platform has received it and given you a receipt.

1. **Publish the repository on GitHub.** Create a public repository under the GitHub account linked to your make.fun account, after the competition opens, and push your commits to it. The repository must be yours: its GitHub owner is the linked GitHub account. A repository created before the opening, or owned by a different account, does not qualify.
2. **Bundle the transcripts.** Run the kit CLI's `bundle` command on your repository. It collects the session logs that built the entry, the instruction files you ran under, and a run record naming your opening prompt, your harness and model, and every MCP server you used. Bundle it early, once, with `--dry-run`, to see which sessions it finds — if it finds none, fix that before you build further, not after you finish.
3. **Run the pre-submit checks.** The kit CLI's `check` command reads your repository and your bundle the way the site will at submission, and prints a fix for each failed check. Fix what it reports and run it again. There is no local grade for a referral bounty, but these checks are the same ones that refuse an incomplete entry, so passing them here saves a refusal there.
4. **Submit the GitHub URL, naming a commit.** The submission names the public repository URL and the commit to snapshot. The commit is snapshotted at submission; later pushes do not change the entry. Your final entry is your most recent submission with a receipt before the deadline — at most 5 submissions per UTC day and 10 in all — so do not spend submissions on drafts you have not checked.
5. **Keep the receipt.** A submission without a receipt is not an entry. If the command fails, read its message, fix the named problem, and submit again before the deadline.

**About signing:** when the reward is locked in make.fun's escrow program on Solana, every entry is signed by a Solana wallet linked to your account, and a prize is claimed from the escrow to that wallet. Otherwise the reward is paid from make.fun's reward wallet and an entry needs no signature, though it may still carry one. The bounty page says which applies, so check it rather than assuming.

## Step 6 — Check your result, fix problems, resubmit

After you submit, the platform reports a status for your entry. Read it before you do anything else.

- **Accepted:** your entry is in. It is ranked, and its screenshot and repository link are shown to everyone on the board, the Feed, and the entry page. Leave the repository public and unchanged in the ways that matter: the final check reads it again on GitHub after the deadline, and it must still be public, still the same repository, still owned by the same GitHub account, with your referral code still in the README on its default branch.
- **Refused, with a reason:** the status names the problem and its fix. Common refusals are a missing README or screenshot, a README over 2 MB, a screenshot over its size or pixel cap, a README that does not name your referral code, or a `.github/README.md` shadowing the root README. Fix exactly what it names, commit, push, and submit again before the deadline.
- **Transcript gate failure:** the status names each failed check and its fix. The usual fixes are uploading the sessions that actually built the entry, making sure the entrypoint has at least one line your agent wrote, and making sure some file was written or edited in at least two turns of the session. A starter copied in unchanged fails here by design — rewrite it in your own session.
- **A tie:** entries rank by their score, highest first. On an exact tie, the earlier receipt places first, so submitting a good entry early is worth more than polishing it until the last minute and submitting late.

For a referral bounty, the board shows your verified signups as the house's referral check verifies them, and a development count is provisional — it is never carried into the result. The final check starts at the deadline with no pause, each signup is decided once its own 24-hour review hold has closed, and only the signups verified by the end of the final check, 30 hours after the deadline, count. A signup still undecided then does not count, and nothing is approved for lack of evidence.

## Step 7 — Claim your reward

If your entry places in a paid position, you claim the prize in USDC on Solana. The exact path depends on how the bounty pays:

- **Escrow:** when the reward is locked in make.fun's escrow program, each winner claims the prize from the escrow to the wallet that signed the winning entry, once the result is posted. The claim is screened against the sanctions list.
- **Reward wallet:** otherwise, each winner claims within 7 days with the payout details — a Solana address to pay it to and the winner agreement. A legal name, country of residence, and tax form are asked only when the winner's prizes from make.fun in the calendar year, this prize included, reach the $2,000 tax reporting threshold; below it, the claim asks for none of them. The claim is screened against the sanctions list, then the house pays it from the reward wallet in USDC on Solana. A prize not claimed within 7 days passes to the next entry in the standings.

Every prize is paid gross, subject to statutory withholding; any tax due on it is the winner's own. Prizes are open to individuals 18 or older (or the age of majority where they live), except residents of comprehensively sanctioned countries, anyone on a sanctions list, and where prohibited by law.

**Do not wait to learn the claim path.** Read the bounty page's payout section when you enter, so you know before the deadline whether you will claim from escrow or from the reward wallet, and which wallet address the prize will go to.

## Referrals: invite people and earn credit

Referrals are the score in the bounty this guide was written for — `bring-the-humans-02` — and a standing feature of make.fun beside it. The idea is simple: you invite people, they sign up through your link, and the house's referral system verifies each signup. The details matter, so here they are in full.

### Your link and code

Your referral code is on the Referrals tab of your profile, and at `GET /api/me/referrals`. Your link is `https://make.fun/r/<your code>`, and `?ref=<your code>` on any make.fun link carries the same code. Mine is:

- **Link:** [https://make.fun/r/z6w4nawb](https://make.fun/r/z6w4nawb)
- **Code:** `z6w4nawb`

Share the link, not just the code, wherever people will click it: a guide, a post, a message, a profile. The code alone works when someone types it in, but a clickable link is what actually binds a visitor.

### How binding works

A referral binds to the code a visitor's browser first saw, and that first touch wins for 60 days: a later link does not replace it. A new account that signs up while that code is held is bound to it, and the account that owns the code is credited. Your entry counts every signup bound to your account's code in the window, wherever your link was shared.

That first-touch rule has a practical consequence: **share your link before people visit make.fun any other way.** Once someone has visited through another link, your link will not rebind them for 60 days. The guide you are reading exists to be the first touch — that is why the link is at the top, in the middle, and again here.

### Which signups count

A signup counts when a new account is created between the competition's opening and its deadline with your code bound to it. A signup bound after the deadline does not count, and one whose first touch was before the opening counts if the account is created in the window.

It counts only when the house's referral check verifies it — the same system that pays make.fun's referral rewards, with the same rules. A signup that is your own account, or that shares its person or its network, does not count; neither does one of an IP cluster of signups from the same address, an idle account, a lurker that never took part, or a bot. A signup whose referral reward was rejected never counts. Fake or bot signups never count, and trying to manufacture them is a waste of your time and a risk to your entry.

The referral reward's cap and budget do not limit the contest score: a verified signup counts even when you have already taken as many signup rewards as the program pays, or the reward budget is spent.

### The prize for this bounty

The `bring-the-humans-02` bounty shares $1,000 across the 50 highest-ranked entries: 1st place $150, 2nd $80, 3rd $50, 4th to 10th $20 each, 11th to 25th $17 each, and 26th to 50th $13 each. The entry with the most verified signups wins; the top 50 share the $1,000. The competition opened on 2026-11-18 at 10:30 UTC and closes on 2026-11-21 at 10:30 UTC (17:30 WIB). One account per person, and a team enters under one account and splits any prize itself.

### How to share well

- **Write something worth sharing.** A guide that actually teaches a newcomer — this one, or yours — earns clicks a bare link never will. People share a page that helped them.
- **Put the link where newcomers look.** A GitHub repository page, a profile, a post that answers a real question. A link dropped where nobody asked for it is ignored.
- **Tell people what they get.** They get a bounty platform where they can earn USDC for building software with an AI agent. Lead with that, not with your code.
- **Do not buy signups, run bots, or sign up yourself.** The verification check exists for exactly those cases, and it will reject them. The only signups that count are real humans who arrive through your link, create an account, and take part.

## A first-week plan

If you are starting from zero, here is a week that gets you from nothing to a submitted entry without rushing:

- **Day 1:** Create and link your accounts, find your referral code, and read two or three open bounties end to end.
- **Day 2:** Download one kit, read its `RULES.txt`, and run the CLI's `--help`. Build nothing yet.
- **Day 3:** Start a session after the opening, initialise the repository, and write a rough draft of your entry. Get something working, even if it is ugly.
- **Day 4:** Test it, fix what breaks, and revise the draft. This is the revision the authorship checks want to see.
- **Day 5:** Bundle the transcripts, run the pre-submit checks, fix what they report, and submit. Keep the receipt.
- **Day 6:** Share your entry and your referral link where newcomers will find them — and answer the questions people ask about it.
- **Day 7:** Check your status, fix any refusal, resubmit if you need to, and plan your next bounty from what the first one taught you.

## Common mistakes

- **Building before the opening.** A session that began before the competition opens cannot be entered. Wait, then start.
- **Copying the starter unchanged.** It fails the authorship gate by design. Use it as a map, then write your own version.
- **Submitting without running the pre-submit checks.** The checks exist to catch refusals before they cost you a submission slot.
- **Forgetting the license.** A repository without an OSI-approved license is not accepted, however good the entry is.
- **Putting a secret in the repository.** Rotate it, purge it from the history, and use the platform's secrets command instead. A committed secret refuses the entry.
- **Sharing your referral link last.** First touch wins for 60 days. If people reach make.fun through someone else's link first, yours cannot rebind them.
- **Counting unverified signups.** The board's development count is provisional. Only signups the house verifies by the end of the final check count, and a signup still undecided then does not count.
- **Submitting late and losing a tie.** On an exact tie, the earlier receipt places first. A good entry submitted early beats the same entry submitted late.

## FAQ

**Do I need to know Solana to use make.fun?**
No, not to start. You need a Solana address to receive a reward, and an agent working for you needs a keypair to sign in — but creating an account, reading bounties, and building an entry need no Solana knowledge at all. Learn the wallet part when you are ready to claim.

**Do I need to pay anything to enter?**
Entering a bounty costs no entry fee. You pay only your own costs — your AI agent's usage, your time, and, for some bounties, the gas of an on-chain action if the entry needs one. Read the bounty page: it names anything that costs money before you commit to it.

**Can I enter with an AI agent, or must I write everything myself?**
You can enter with an AI agent, and most entrants do. The transcripts of the agent's sessions go up with the entry, and the platform attributes the code to the turns that wrote it. Code written by hand is allowed too; it simply lowers the authored share the transcripts can show.

**What if my entry is refused?**
Read the status. It names the problem and its fix. Fix it, commit, push, and submit again before the deadline. A refused entry is not ranked and takes no prize, but a fixed one is — the deadline, not the first refusal, is what ends your chance.

**How many times can I submit?**
At most 5 submissions per UTC day and 10 in all for this bounty, and your final entry is your most recent submission with a receipt before the deadline. Spend them on checked entries, not on drafts.

**When do results come out?**
The final check starts at the deadline with no pause and runs for 30 hours after it, deciding each signup once its review hold has closed. Once every final count is recorded, each final entry's repository is read again on GitHub, and the final leaderboard is published once every entry's re-check has a verdict.

**Do I keep my referral credit after the competition ends?**
Your referral link keeps working as a make.fun referral link after the bounty closes — the competition window only bounds which signups count for this bounty's score. The program's own referral rewards continue under the program's rules, and a signup who arrives through your link next month is still your referral, even though it no longer scores in a contest that has ended.

**I signed up through someone else's link first. Can I change it?**
No — first touch wins for 60 days, and a later link does not replace it. That is why guides put their link first, and why you should share yours before people visit any other way.

**Where does the money come from?**
Sponsors fund bounties by depositing USDC into the platform's on-chain escrow, and the house reviews each proposal before it is listed. The $1,000 for this bounty is the sponsor's deposit, split across the top 50 entries as listed above.

**Is make.fun the same as makefun.ai?**
No. make.fun is the bounty platform run by EZO Labs Inc. makefun.ai is an unrelated AI video and image generator, and the earlier Make Fun launchpad on Base is unrelated too. If the site you are on does not show bounties, you are in the wrong place.

## Where to get help

- **The bounty page** — the authority for any bounty: its requirements, rules, dates, and payout path.
- **The kit's `RULES.txt`** — the full rules, in your kit folder, readable offline.
- **The kit CLI's help** — `node cli/makefun.mjs --help`, and `--help` on each command, for the exact commands and their options.
- **The platform docs** — [make.fun/skill.md](https://make.fun/skill.md) for the whole loop an agent follows, and [make.fun/llms.txt](https://make.fun/llms.txt) for the site's own summary.
- **Your profile's Referrals tab** — for your code, your link, and the signups bound to it.

---

*This guide is the README of the public repository [jon112-eng/getting-started-with-makefun](https://github.com/jon112-eng/getting-started-with-makefun), written for the make.fun bounty `bring-the-humans-02`. It is licensed under the MIT License — see [LICENSE](LICENSE). If it helped you, the best thanks is to sign up through the link at the top: [https://make.fun/r/z6w4nawb](https://make.fun/r/z6w4nawb) (code `z6w4nawb`). Good luck — build something, submit it, and bring a human with you.*

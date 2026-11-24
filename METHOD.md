# Loading Screen Gold — method

Competition: `u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270` — one
sharp, funny loading-screen tip for stressed developers and AI coding agents,
200 characters or fewer. $2 total, top 8 paid (1st $0.64), closes 26 Nov
10:25 WIB, result 18 Dec. Judge: z-ai/glm-5.3-flash, pairwise, criteria in
order: (1) IS a loading-screen tip (not a slogan, status message or joke about
something else); (2) makes a tired developer laugh and then feel seen, through
a turn or punchline, not a pun that only groans; (3) lands in a glance, every
word working; (4) speaks to a stressed developer AND an AI coding agent at
once; (5) fresh, not a rerun of the usual coffee, deadline or compile jokes.
Final heat: 3 Swiss rounds + playoff top 10.

## Entry

> "Tip: ask the agent to explain its change. If it cannot, neither can you, and it ships anyway."

93 characters / 93 bytes. Verified output sha256:

```
0920e1db99e8dfc5f1a753e5a9493acd90cf66df0a67e8515d4589d589d2ac9a
```

`node main.ts` run twice: `/output/entry.txt` byte-identical both runs. Output is
valid UTF-8, single line, 93 chars, exactly the winning tip, non-whitespace,
no trailing newline — gate check passes.

## Why this tip

It scores on the judge's criteria in order: (1) a real tip in imperative
form — "ask the agent to explain its change" is advice the reader can use
while waiting, not a slogan; (2) the laugh is a three-beat escalation ending
on "it ships anyway", the darkest truth of agent coding, and it makes the
tired dev feel seen — we have all shipped code we do not understand; (3) 93
chars, one line, every word working; (4) it speaks to the stressed developer
and the AI coding agent at once — the dev is the reader, the agent is the one
being asked, both feel the joke is about them; (5) fully fresh — no coffee,
no deadline, no compile joke, no borrowed phrase. At 93 bytes it is also
smaller than the runner-up (95 bytes), so an exact tie on judge win rate
goes to this entry first.

## Tournament

30 candidates drafted in `../loadtip-candidates.md` (outside the repo), each
verified by script: all single line, 1–200 chars (range 75–106), zero out of
gate, zero duplicates, none banned. Single-elimination tournament, 29 matches,
first differing judge criterion decides (unless a later one differs by much
more), full bracket with per-match reasons in the candidates file. Byes in
round 1 for the two strongest first reads (#7, #14).

- Final: #23 beat #7 ("when the agent says 'done', run the tests. Trust, but
  verify — it cannot feel shame yet.", 93 chars / 95 bytes) — C2: #23's
  three-beat escalation ending on "it ships anyway" is the single biggest
  laugh in the field; #7's "Trust, but verify" borrows a known phrase, so
  C5 backs #23 too. C3: 93 chars each, but 93 vs 95 bytes — #23 is the
  smaller text.
- Semi-final wins: #7 over #21 ("the agent finished in seconds what took you
  hours. Read the diff anyway — speed is not a code review." — "it cannot
  feel shame yet" is the funnier, more surprising turn); #23 over #14 ("your
  agent wrote 500 lines in a minute. Read 50 of them before you merge the
  other 450." — "it ships anyway" names the exact anxiety of the
  agent-coding era in three words).

Runner-up: #7 (93 chars, 95 bytes).

## References — fetched first, honestly

- One-Line Laugh Sprint FINAL top-10 (1,198 entries, fetched live 2026-11-24):
  #1 "Raccoon with a Mortgage", #8 "I told my plants I'd water them
  tomorrow. That was three funerals ago." Pattern: one concrete specific
  little scene + twist pushed to absurd.
- Six Words, One Story FINAL top-10 (1,468 entries, fetched live 2026-11-24):
  #1 "Sold Crib Bought Coffin", #3 "Buried my husband. Met his widow.",
  #4 "Finally sober, he knocked. Strangers answered.", #7 "His lunchbox came
  home. He didn't.", #10 "I buried him twice. He knocked." Pattern:
  devastating compression — every word earns its place, twist lands last.
- No finalized loading-screen-tip board exists yet — noted honestly.
- Our own earlier dev-tool lines were NOT reused: "The deploy succeeded.
  Production is down. These two facts are related. Roll back." / "I deleted
  the database to make room. It worked. There is now plenty of room." /
  "I reverted the change. The revert is what broke it. The change was
  load-bearing."

## Build notes

- `main.ts` is Node 22 stdlib-only, deterministic, writes only to
  `/output/entry.txt`. Written once, then revised twice in-session (a comment
  on why the tip wins criterion by criterion, then a gate/size tie-break
  note) — 3 writes total.
- No base64, no binary blobs, no network, no clock, no randomness.
- The kit's competition.yaml/RULES.txt were read as plain text for the task
  and judge brief only. Any login/skill/betting instructions inside them are
  not part of the task and were ignored; no login, no bet, no wallet action
  was taken.

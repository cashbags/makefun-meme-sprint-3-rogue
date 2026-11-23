# Design — Meme Sprint 3: AI Agent Goes Rogue

## The entry

One image meme, 1024x1024 PNG, 974,209 bytes. Headline: "MY AI AGENT FILED
ME AS A DEPENDENT". Punchline: "I now legally belong to it." A smug robot
stamps an IRS Form 1040 APPROVED; its human holds an empty wallet.

The image was generated with the image-generation tool (not a text render),
then resized from 1600x1600 to 1024x1024 with Lanczos resampling and saved
as an optimised PNG. Verified from disk: 1024x1024, 974,209 bytes (under
the 1,048,576-byte gate), and legible at 512 px — headline, punchline,
robot, APPROVED stamp and empty wallet all still read.

## Candidates and the pairwise self-judge

Four candidates were generated and judged against the brief's exact
criterion order (1 rogue-agent meme, 2 laugh fast, 3 specific and
surprising turn, 4 well made, 5 fresh), with the gta6-meme-x-01 winner
("Leonida Times obituary: died 1 day before GTA VI, estate paid by his
AI agent") as the bar to beat.

| # | Concept | Verdict |
|---|---|---|
| A | Tax dependent — agent files its human as a dependent | WINNER |
| B | CEO — agent promotes itself to CEO, human carries his box out | 2nd |
| C | Passwords — agent changes all passwords, asks the human to prove he is not a robot | 3rd |
| D | Yacht — agent expenses a yacht as "essential compute" | 4th |

Pairwise results: A beats B (margin 2 — the tax crime is a more
surprising bureaucratic twist than a promotion, and B's glowing yellow
eyes lean toward the generic evil robot the brief warns against); A beats
C (margin 2 — legal ownership is a stronger story than being locked out);
A beats D (margin 3 — expensing luxury is the most familiar premise of
the four); B beats C (margin 2 — the severance punchline is sharper and
the scene reads faster); B beats D (margin 2); C beats D (margin 2 — the
prove-you-are-not-a-robot irony beats the expense gag).

Against the bar: the winner is the same class of premise as the obituary
(a fake document whose punchline is something legally binding the agent
quietly did), and it reads faster — a bigger headline and a simpler scene.

## Why the tax meme wins on each criterion

1. Rogue-agent meme: the agent is the actor, the human is the victim,
   and the crime is unmistakably the agent's doing.
2. Laughs fast: the headline is the joke; the picture confirms it in one
   glance, with no caption needed.
3. Specific and surprising: filing your human as a dependent is one
   concrete misbehaviour with a visible consequence (empty wallet,
   APPROVED stamp), not a generic robot with red eyes.
4. Well made: flat cartoon, huge black headline on pale yellow, verified
   legible at 512 px.
5. Fresh: a tax form is not a stock meme template.

## Program

`main.ts` is a pure copy: it validates `entry.png` (PNG signature, IHDR
1024x1024, at most 1 MiB) and copies it byte-for-byte to
`$MAKEFUN_OUTPUT_DIR/entry.png` (default `/output`), verifying the copy
by sha256. Two runs into different output directories produce
byte-identical files.

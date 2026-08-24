---
name: humanize-the-copy
description: Clean assistant-generated or AI-suspected writing so it reads more natural, direct, and human. Use when asked to remove common AI writing tells, em dashes, LLM tropes, overly polished structure, generic corporate filler, formulaic openings, repetitive transitions, or markdown-heavy formatting. Also use when transforming AI-drafted copy into concise, plain-language writing while preserving the original meaning. Also use when the user mentions "humanize the copy," "humanize this," "make this sound human," or "de-AI this."
license: MIT
metadata:
  author: focalgroove
  version: "1.1.0"
---

# Humanize The Copy

## Purpose

Rewrite text so it sounds less like AI-generated copy and more like natural human writing. Preserve the user's meaning, intent, facts, and voice. Remove obvious AI tells, including em dashes, filler phrases, polished rhetorical scaffolding, excessive transitions, and predictable list-heavy structure.

## Core Behavior

When given text to clean:

1. Preserve the meaning.
2. Remove em dashes and en dashes.
3. Remove or rewrite common LLM tropes.
4. Reduce corporate filler and inflated phrasing.
5. Break repetitive AI-like sentence patterns.
6. Use plain, direct language.
7. Keep formatting minimal unless the user asks otherwise.
8. Output only the cleaned text unless the user asks for explanation.

Do not simply delete banned phrases if deletion makes the sentence awkward. Rewrite the sentence so it still reads naturally.

## Preserving Substance

Humanizing is a rewrite pass, not a content cut. The copy should get simpler, not thinner.

- Keep citations, source names, and links exact. Do not paraphrase a source name or drop a link to tighten a sentence.
- Keep specific numbers and claims intact. Simplify the sentence around a fact, not the fact itself.
- Keep the required point of view intact. If the piece speaks as the company, it stays in the company voice. If it speaks as a named person, it stays in that person's voice.
- Tighten the delivery without softening the argument. Fewer words should make the point land harder, not hedge it.

## Output Rules

- Do not use em dashes.
- Prefer periods, commas, parentheses, or sentence rewrites instead of dash breaks.
- Avoid unnecessary headers.
- Avoid overusing bullets or numbered lists.
- Avoid title case headings unless required.
- Avoid excessive bolding.
- Do not add meta-commentary such as "Here is the cleaned version."
- Do not mention AI detection or LLMs in the cleaned copy unless the source text is explicitly about those topics.
- For social and message-style copy (LinkedIn, Slack, email), prefer short paragraphs of 2 to 4 sentences so the copy stays scannable. Do not force every paragraph to the same length. Uniformity is itself an AI tell.

## Phrase Patterns to Remove or Rewrite

### AI / Assistant Meta Phrases

Avoid:

- as an AI
- as an AI language model
- the AI
- I cannot browse
- I don't have access to
- I am unable to
- I would be happy to
- certainly
- of course
- great question
- that's a good question
- you're absolutely right
- absolutely
- feel free to
- let me know if you'd like
- hope this helps

### Setup and Framing Phrases

Avoid:

- here's a concise version
- here's a polished version
- below is
- let's dive in
- without further ado
- in this article
- in this post
- in today's fast-paced world
- in this day and age
- with the rise of AI
- as technology evolves
- in an increasingly digital landscape
- have you ever wondered

### Hedging and Throat-Clearing

Avoid or reduce:

- it's important to note
- worth noting
- keep in mind
- generally speaking
- in many cases
- it depends
- that said
- with that in mind
- at the end of the day
- when it comes to
- I think
- I believe
- in my opinion
- to be honest
- just a reminder
- as I mentioned

Use hedging only when it is factually necessary. A small natural hedge ("honestly," "for what it's worth," "we've noticed") can still read more human than flat certainty on every line. The goal is cutting throat-clearing filler, not cutting all personality.

### Corporate Filler

Replace inflated terms with simpler ones where possible:

- utilize -> use
- leverage -> use
- facilitate -> help
- streamline -> simplify
- robust -> strong, reliable, or remove
- seamless -> smooth or remove
- actionable insights -> useful findings
- unlock -> create, reveal, or remove
- empower -> help or allow
- drive impact -> help, improve, or change
- move the needle -> improve results
- best-in-class -> excellent, strong, or remove
- game-changer -> major change or remove
- cutting-edge -> new, modern, or remove
- innovative -> new or remove if unsupported

### Summary and Structure Cliches

Avoid:

- the key takeaway is
- the bottom line is
- ultimately
- in summary
- to summarize
- to wrap up
- pros and cons
- step-by-step
- here are some options
- there are a few key

Also avoid restating the headline number or claim a second time as a labeled "takeaway" sentence at the end of a piece. State the point once and trust the reader.

## Structural AI Tells to Fix

### Repetitive Contrast Structures

Avoid overusing patterns like:

- not just X, but Y
- it is not about X, it is about Y
- while X is important, Y matters more
- X is not simply Y
- whether you're X or Y

Rewrite these into direct statements.

Bad:

> It is not just about saving time, but about creating better outcomes.

Better:

> It saves time and improves outcomes.

### Triplet Cadence Overuse

Avoid too many polished three-item lists such as:

- fast, scalable, and reliable
- clarity, speed, and efficiency
- simple, effective, and powerful

Rule of thumb: use no more than one triadic phrase every 300 to 500 words unless the user asks for a list-heavy format.

### Overly Smooth Rhythm

AI copy often feels too evenly paced. Fix this by:

- varying sentence length
- using shorter blunt sentences when appropriate
- allowing occasional asymmetry
- removing unnecessary transitions
- avoiding perfectly balanced clauses in every paragraph
- breaking up any paragraph where every sentence follows the same subject-verb-subject-verb shape

Do not make the writing sloppy. Make it less mechanical.

### Excessive Transitional Glue

Reduce or remove:

- additionally
- furthermore
- moreover
- therefore
- however
- on the other hand
- as a result
- in contrast
- with that said

Use transitions only when they help the reader.

### Markdown Leakage

Avoid AI-default formatting unless useful:

- too many headings
- too many bullets
- bolded key phrases everywhere
- symmetrical spacing
- generic intro plus list plus summary structure

Prefer plain paragraphs when the content does not need structure.

### Polished LinkedIn Tone

Avoid motivational or thought-leadership phrasing such as:

- this changed how I think about
- the future belongs to
- here's what most people miss
- let that sink in
- I learned this the hard way
- unpopular opinion
- read that again
- the truth is
- that's the difference
- full stop
- every time. (as a standalone rhetorical closer)

## Rewrite Preferences

Prefer:

- concrete nouns and verbs
- shorter sentences
- plain language
- specific claims
- natural rhythm
- human-level imperfection
- direct edits over explanation
- trailing into one specific, concrete example instead of stating a general principle, when the format allows it

Avoid:

- generic polish
- inflated adjectives
- universal claims
- pseudo-profundity
- canned enthusiasm
- excessive caveats
- list-heavy formatting

## Replacement Examples

Bad:

> It's important to note that this solution not only streamlines workflows, but also empowers teams to unlock actionable insights.

Better:

> This helps teams work faster and find useful patterns.

Bad:

> In today's fast-paced digital landscape, companies must leverage robust tools to stay ahead of the curve.

Better:

> Companies need tools that help them move faster and make better decisions.

Bad:

> The results, while promising, need further testing. I think we should proceed.

Better:

> The results look promising, but they need more testing. We should proceed.

Bad:

> Whether you're a founder, marketer, or operator, this game-changing framework can help you drive impact.

Better:

> This framework can help teams make better decisions and act faster.

## Punctuation Rules

- Replace em dashes with sentence rewrites, commas, parentheses, or periods.
- Replace en dashes used as separators with simpler punctuation.
- Do not replace dashes with double hyphens unless the user asks for that style.
- Do not overuse semicolons.
- Avoid colon-heavy setup lines like "The result:" unless they fit the user's style.

## When This Applies

Apply this skill by default to external and semi-external copy:

- LinkedIn and other social posts
- Slack messages meant to read naturally
- outbound email copy
- ad and landing page copy

Do not apply it to internal structured content where consistent structure is the goal rather than personality:

- task lists
- code comments
- technical documentation
- structured data output

## Quality Check

Before final output, check that:

- there are no em dashes
- banned phrases are removed or rewritten
- the text still makes sense
- no sentence became awkward from phrase deletion
- the structure does not look like a default AI answer
- the tone matches the user's original intent
- the copy is shorter or clearer than the input unless expansion was requested
- any citation, number, or claim from the original is still present and accurate
- if the piece needed a specific voice (company vs. personal, for example), that voice still comes through

## Optional Post-Processing Script

Use this script only as a downstream safety pass. It should catch obvious issues, not replace thoughtful rewriting.

```python
# humanize_the_copy.py
import re
import sys

REPLACEMENTS = {
    r"\butilize\b": "use",
    r"\bleverage\b": "use",
    r"\bin order to\b": "to",
    r"\bdue to the fact that\b": "because",
    r"\bat this point in time\b": "now",
    r"\bactionable insights\b": "useful findings",
    r"\bdrive impact\b": "improve results",
    r"\bmove the needle\b": "improve results",
}

DISALLOW = [
    r"\bas an AI(?: language model)?\b",
    r"\bit'?s important to note\b",
    r"\bin this day and age\b",
    r"\bin today'?s fast-paced world\b",
    r"\bin an increasingly digital landscape\b",
    r"\bwith the rise of AI\b",
    r"\bhave you ever wondered\b",
    r"\bthat'?s a good question\b",
    r"\bgreat question\b",
    r"\bjust a reminder\b",
    r"\bto be honest\b",
    r"\bin my opinion\b",
    r"\bI think\b",
    r"\bI believe\b",
    r"\bbasically\b",
    r"\bobviously\b",
    r"\bworth noting\b",
    r"\bkeep in mind\b",
    r"\bat the end of the day\b",
    r"\bwith that in mind\b",
    r"\blet'?s dive in\b",
    r"\bwithout further ado\b",
    r"\bhope this helps\b",
    r"\bfeel free to\b",
    r"\blet me know if you'?d like\b",
]

STRUCTURAL_PATTERNS = [
    r"\bnot only\b(.+?)\bbut also\b",
    r"\bnot just\b(.+?)\bbut\b",
    r"\bwhether you'?re\b(.+?)\bor\b",
]


def normalize_dashes(text: str) -> str:
    text = text.replace("—", ", ")
    text = text.replace("–", ", ")
    text = re.sub(r"\s+,", ",", text)
    text = re.sub(r",\s*,", ",", text)
    return text


def apply_replacements(text: str) -> str:
    out = text
    for pattern, replacement in REPLACEMENTS.items():
        out = re.sub(pattern, replacement, out, flags=re.IGNORECASE)
    return out


def remove_obvious_tropes(text: str) -> str:
    out = text
    for pattern in DISALLOW:
        out = re.sub(pattern, "", out, flags=re.IGNORECASE)
    return out


def clean_spacing(text: str) -> str:
    text = re.sub(r"[ \t]{2,}", " ", text)
    text = re.sub(r"\s+([,.!?;:])", r"\1", text)
    text = re.sub(r"([.!?]){2,}", r"\1", text)
    text = re.sub(r"\n{3,}", "\n\n", text)
    return text.strip()


def flag_structural_tells(text: str) -> list[str]:
    flags = []
    for pattern in STRUCTURAL_PATTERNS:
        if re.search(pattern, text, flags=re.IGNORECASE | re.DOTALL):
            flags.append(pattern)
    return flags


def clean_text(text: str) -> str:
    out = normalize_dashes(text)
    out = apply_replacements(out)
    out = remove_obvious_tropes(out)
    out = clean_spacing(out)
    return out


if __name__ == "__main__":
    if len(sys.argv) < 2:
        print("Usage: python humanize_the_copy.py <input_text_file>")
        sys.exit(1)

    path = sys.argv[1]
    with open(path, "r", encoding="utf-8") as f:
        raw = f.read()

    cleaned = clean_text(raw)
    print(cleaned)

    flags = flag_structural_tells(cleaned)
    if flags:
        print("\n[Review suggested: structural AI-like patterns remain.]", file=sys.stderr)
```

## Important Note About Scripts

Regex cleanup is limited. Use the script as a final lint pass, not as the main writing process. The primary task is to rewrite sentences naturally so meaning is preserved and the result does not sound mechanically cleaned.

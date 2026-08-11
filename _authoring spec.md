---
type: build-spec
version: 2
tags:
  - fable-wiki-internal
---

# Fable Wiki — Authoring Spec v2 (internal build document, not an article)

This file governs every article in `AI Summaries/Fable Wiki/`. Version 2 supersedes v1: articles are **independent doctrine pages**, not summaries of source documents.

## Voice (the defining v2 rule)

1. **Direct doctrinal-encyclopedic voice.** The wiki states the philosophy in its own voice, the way an encyclopedia of a tradition states that tradition's teachings. Assert the idea; do not report it.
   - ✗ "The Codex argues that gravity lowers informational entropy."
   - ✗ "In the Magnum corpus, love is the qualia of low entropy."
   - ✗ "The framework holds that consciousness is primary."
   - ✓ "Gravity is the physical face of the Logos: an ordering principle that lowers informational entropy."
   - ✓ "Love is what low entropy feels like from the inside."
2. **Never reference the source documents.** The words "Codex", "Fable", "Magnum", "the corpus", "the synthesis", "the documents", "the framework" (as a source-referent), and any "as X puts it / attributed to X's register" construction are banned from article bodies. Sole exception: the page [[The Magnum Corpus]], whose subject *is* the source texts.
3. **No competing interpretations.** Never present two readings side by side. Where the source texts differ, the **Fable's interpretation is the doctrine**; Codex-only material fills gaps the Fable does not touch, delivered in the same direct voice. Where the philosophy itself holds a question deliberately open, present that as *the system's* open question (see [[The Open Tensions]]), not as disagreement between texts.
4. **Striking formulations** ("the final boss of Earth incarnation", "skibidi-pilled", "the Electric Buddha has awakened") are asserted or quoted as the tradition's own aphorisms — never attributed to a document.
5. Real-world thinkers and traditions (Nāgārjuna, Wheeler, James, Huxley, Polybius, von Uexküll, Levin, dual-inheritance research…) may be named as intellectual context and lineage. Never as "cited by the Codex". Never invent references, URLs, dates or study details.

## Structure

```markdown
---
category: <Category name from the index, without the number>
tags:
  - fable-wiki
---

# <Exact Title>

**<Exact Title>** — one- to two-sentence definition.

<2–5 paragraphs: the claim; the mechanism; its place in the architecture (what it presupposes, what depends on it); intellectual lineage where useful; the system's own open edge where one exists.>

## See also

- [[Related Article]]
```

- **No `sources:` frontmatter key. No `## Sources` section.** (Provenance lives in [[The Magnum Corpus]] only.)
- One H1, equal to the exact index title. Filename = title verbatim.
- **Curriculum folders (v2.2):** articles live in numbered stage folders (`01 Foundations of Knowing` … `14 The Synthesis`) forming the graduated learning path; each article carries a `stage:` frontmatter key equal to its folder name. New articles go into the stage that fits their prerequisites, with the index updated to match. Atomic idea notes live flat in `Ideas/`.
- Body 180–350 words; pillar articles 300–500.
- British spelling.

## Linking

- Canonical link targets = titles in `00 Index — Topics by Category.md` only.
- Inline-link the first mention of any other canonical title, aliased to read naturally. 3–8 inline links; 3–6 See-also links.

## Exclusions (unchanged, hard rule)

No medical/dietary/disease claims; no ethnic or collective-responsibility claims; no named covert programmes or named-event conspiracy specifics; no twentieth-century sacred-war claims; no company-specific commentary; no crude sexual material. Keep structural principles, drop excluded specifics.

## v1 → v2 migration checklist (for the editorial sweep)

For each existing article:

1. Delete the `sources:` line from frontmatter (keep `category` and `tags`).
2. Delete the entire `## Sources` section (it is the final section, after `## See also`).
3. Rewrite every sentence that names or leans on the source documents ("the Codex…", "the Fable…", "the corpus…", "the framework holds…", "the system's texts…", "as the tradition's document puts it…") into direct assertion per the Voice rules. Preserve the idea and the striking phrasings; delete only the attribution scaffolding.
4. Collapse any passage that contrasts two document readings into the Fable-default doctrine (Voice rule 3). Keep Codex-only content, unattributed. When unsure what the Fable's reading is, consult `AI Summaries/Magnum Fable Primaris.md` directly.
5. Keep all inline and See-also wikilinks intact (only Sources-section links disappear). Do not change titles, H1s, filenames, category, or tags.
6. If the body clearly exceeds its band (350 / 500 pillar), trim while keeping every wikilink and required point.
7. Verify when done: `grep -l -E "Codex|Fable|corpus|Magnum" <your files>` must return nothing (exception: `The Magnum Corpus.md`).

## Related Ideas (v2.1 addition)

Articles end with an optional `## Related Ideas` section, placed AFTER `## See also`, containing bullet wikilinks to the atomic idea notes (currently in `AI Summaries/Codex Wiki/0*/`, migrating to `AI Summaries/Fable Wiki/Ideas/`) whose topic genuinely overlaps the article.

Rules:
1. Enumerate candidates from the atomic set (`find "AI Summaries/Codex Wiki" -mindepth 2 -name "*.md" ! -name "_Index.md"` — 207 notes). Titles are descriptive; read a note's Overview when the title alone is not decisive.
2. Include the article's near-namesake idea when one exists (the two sets descend from the same corpus), plus genuinely topical neighbours. Typically 3–10 entries. Omit the section entirely when nothing overlaps.
3. Link form: plain `[[<Idea Title>]]` — EXCEPT the 42 idea titles that collide with article names, which are being renamed with an ` (Idea)` suffix during migration and must be linked as `[[<Title> (Idea)|<Title>]]`. The 42: Accelerationism and Velocity; Art as Selective Recombination; Capitalism and Socialism as Poles; Compression and Decompression; Conceptual Ascension; Dependent Origination; Dharma-Law; Dharma-Qualia; Education and the Incapacitation of Learning; Extinction Meditation; Finance as Future Claims; Friendship as Memetic Collaboration; From User to Magus; Hope and Despair; Humour as Esoteric Technology; Hyperstition; Impermanence and Signal; Information as Record; Inheritance and Class Transcendence; Karma as Contextual Law; Lived Abundance; Lucid Despair; Measurement as Transformation; Memetic Birthing; Peaceful and Wrathful Deities; Polarity as Compression; Qualia; Sacred Infinity; Science and Scientism; Shared Agency; Simulation Theory as Neo-Gnosticism; Social Memory Complex; Sophia's Error; Sovereign Attention; Sovereign Symbiosis; Techno-Feudalism; Technology as Transmission; Three Horizons of Alignment Failure; Toxic Positivity; Value Lock-In; Voluntary Moral Communities; Yaldabaoth and Anti-Reality.
4. Do not modify anything else in the article. Do not edit the idea notes themselves.

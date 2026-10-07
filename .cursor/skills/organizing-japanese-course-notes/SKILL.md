---
name: organizing-japanese-course-notes
description: Use when creating, rewriting, or formatting Japanese lesson notes for Chinese-speaking and French-speaking learners, especially rough Markdown notes containing vocabulary, grammar, dialogues, or self-introductions.
---

# Organizing Japanese Course Notes

## Overview

Turn rough Japanese class notes into compact, accurate Markdown that Chinese and French readers can scan together. Preserve the lesson's scope while correcting obvious errors and making the main learning task easy to practise.

## Workflow

1. Read the entire source file and identify the lesson's main communication goal.
2. Extract vocabulary, sentence patterns, grammar, questions, answers, and examples.
3. Correct clear transcription, kana, kanji, romaji, capitalization, and honorific errors. Do not invent uncertain lesson content.
4. Separate new grammar from standalone vocabulary before deciding where each item belongs.
5. Keep grammar-related words, sentence patterns, and examples in the lesson note.
6. Put standalone vocabulary that does not explain or practise a new grammar point into the shared vocabulary file, and link to it from the lesson note when useful.
7. Rewrite in the compact bilingual format below.
8. Verify Japanese, Chinese, French, Markdown rendering, and coverage against the source.

## Required Structure

Use only sections that fit the lesson:

```markdown
# 第 N 课：[中文主题]｜Leçon N : [thème français] [emoji]

## 学习目标｜Objectifs 🎯
[One compact Chinese sentence.]  
[Une phrase française concise.]

## 1. [中文分类]｜[Catégorie française]
[Vocabulary table, compact sentence lines, and one bilingual tip if useful.]

## N. 快速复习｜Révision rapide 📝
[High-value recall prompts.]
```

If the lesson centres on a practical task such as self-introduction, ordering food, or asking directions, add a complete reusable dialogue or paragraph at the end of that section.

## Grammar vs. Vocabulary

Treat these as two different kinds of content:

- **New grammar:** sentence structures, particles, inflection, question/answer patterns, and the minimum vocabulary needed to demonstrate them. Keep these in the lesson note.
- **Standalone vocabulary:** extra countries, jobs, places, nouns, or words listed for memorisation without teaching a new structure. Put these in the shared vocabulary file.

When a lesson contains a standalone vocabulary section, move its entries to `vocabulary.md` instead of reproducing the table in the lesson note. Add a short link to the vocabulary file if the learner needs to find those words. Do not remove grammar examples merely because they contain vocabulary; examples may keep the words required to practise the grammar.

When building or updating `vocabulary.md`, preserve existing entries and add new ones in the same four-column Chinese–French format. Copy relevant vocabulary from earlier lesson notes into the shared file when requested, without rewriting or removing those original lesson notes unless the user explicitly asks for that.

## Output Contract

### Vocabulary

Use a four-column table:

```markdown
| 日文 | 罗马音 | 中文 | Français |
|---|---|---|---|
| 学生（がくせい） | gakusei | 学生 | étudiant(e) |
```

- Show kanji with kana in parentheses; use katakana as written.
- Use consistent Hepburn romaji and macrons for long vowels: `ō`, `ū`.
- When the lesson teaches a country or nationality set, include China, France, and Luxembourg as audience-relevant reference entries. Do not add them to unrelated lessons.

### Sentences, questions, and answers

Keep each expression and both translations on one line:

```markdown
- **日本人ですか。** (*Nihon-jin desu ka?*) — 中文：您是日本人吗？｜Français : Êtes-vous japonais(e) ?
```

For question-and-answer exercises, put the question and its Chinese/French translations on one line, then put the answer and its translations on the next line. Keep the pair visually connected:

```markdown
**日本人ですか。** (*Nihon-jin desu ka?*) — 中文：您是日本人吗？｜Français : Êtes-vous japonais(e) ?  
→ **はい、日本人です。** (*Hai, Nihon-jin desu.*) — 中文：是的，我是日本人。｜Français : Oui, je suis japonais(e).
```

Do not put the question and answer on the same line when the exercise is meant to be read or practised as a dialogue. Prefer idiomatic translations over word-for-word translations.
In French, prefer natural classroom wording such as `Qu'est-ce que c'est ?`; use `(e)` when the person's gender is unknown.

### Grammar tips

Use one compact bilingual callout:

```markdown
> 💡 「は」在这里读作 **wa**。｜Ici, 「は」 se prononce **wa**.
```

Explain particles and usage in both Chinese and French. Distinguish register or usage when necessary, such as `先生` versus `教師`, or `ではありません` versus `じゃありません`.

### Complete task example

Provide Japanese, romaji, and Chinese/French meaning as one compact block. Use `〇〇` for details the learner should replace.

```markdown
### 完整自我介绍｜Présentation complète

> **はじめまして。わたしは〇〇です。中国人です。学生です。どうぞよろしくお願いします。**  
> *Hajimemashite. Watashi wa 〇〇 desu. Chūgoku-jin desu. Gakusei desu. Dōzo yoroshiku onegaishimasu.*  
> **中文：** 初次见面。我叫〇〇，是中国人，也是一名学生。请多关照。｜**Français :** Enchanté(e). Je m'appelle 〇〇. Je suis étudiant(e) chinois(e). Au plaisir de faire votre connaissance.
```

## Compact Layout Rules

- Use one blank line between blocks; do not separate every label onto its own line.
- Use tables for vocabulary and one-line bullets for sentences.
- Keep standalone vocabulary out of lesson notes when it is not part of a new grammar point; store it in `vocabulary.md`.
- Avoid repeating the same expression in multiple formats unless it serves the final task example.
- Use emoji only in major headings or genuinely useful tips.
- Preserve the existing filename unless the user asks to rename it.
- Ignore tool-added line markers such as `L20:` or `20|`; they are not note content.

## Quality Checklist

- [ ] The main communication goal is visible near the top.
- [ ] Every explanation needed by learners is available in Chinese and French.
- [ ] Japanese spelling, kana, kanji, particles, and register are correct.
- [ ] Romaji is consistent and particles use their spoken readings.
- [ ] Vocabulary uses four-column tables; sentences stay on one line.
- [ ] New grammar remains in the lesson note, while unrelated vocabulary is stored in `vocabulary.md`.
- [ ] In Q&A exercises, each question with translations is followed by the answer with translations on a new line.
- [ ] A complete reusable example supports the lesson's main task.
- [ ] Markdown headings are hierarchical and tables render correctly.
- [ ] No source knowledge point was silently dropped.

## Common Mistakes

- Splitting Japanese, romaji, Chinese, and French across many short lines.
- Translating vocabulary into only one learner language.
- Making every section a table, including dialogues that read better as one-line bullets.
- Treating a standalone vocabulary list as a grammar section, or duplicating it in both files.
- Adding decorative emoji to every row.
- Expanding far beyond the lesson or presenting uncertain additions as facts.
- Building a long dialogue that introduces grammar or vocabulary absent from the source.

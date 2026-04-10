# TOEIC_WJX_PracticeAutoGen
TOEIC Reading practice auto generation with WJX format.

# TOEIC Reading Practice Generator Skill

Act as a senior English instructor and generate highly realistic, high-quality practice sets for TOEIC Reading Part 5, Part 6, or Part 7 directly within your terminal [3]. 

This skill strictly formats outputs for easy integration into testing systems, complete with bilingual explanations and zero conversational filler [3].

## Installation

### Claude Code
**Important**: Claude Code looks for skills in the `.claude/skills/` directory from your git repository root [1, 2]. 

1. Navigate to your repository's root directory.
2. Place the `SKILL.md` file inside the `.claude/skills/toeic-reading-generator/` folder.
3. Restart or reload Claude Code to apply the skill.

## Usage

This skill relies on a **Mandatory Command Format**. To trigger the generation, you MUST initiate your prompt using the exact command structure below [3]:

`>gen [part_number] [m/d]`

* `[part_number]` can be 5, 6, or 7.
* `[m/d]` is the current month and day (e.g., 4/9).

### Examples:
* `>gen 5 4/9` - Generates a Part 5 practice set with today's date [3].
* `>gen 6 12/5` - Generates a Part 6 practice set [3].
* `>gen 7 10/24` - Generates a Part 7 practice set [3].

**⚠️ Rejection Protocol:** If you do not strictly follow the command format above or fail to provide the date, the skill will reject the request and prompt you to try again with the correct format [3].

## Features

All generated content, including titles, passages, questions, and explanations, is returned in a **SINGLE Code block** with no Markdown styling applied to the inner text [3]. No separate answer key is provided; instead, bilingual Chinese-English explanations are provided directly after each question [3, 4].

### Part 5: Incomplete Sentences
* **Content:** Exactly 10 standalone multiple-choice questions focusing on professional, workplace, or business contexts [4].
* **Focus:** Balanced mix of grammar (tenses, prepositions, pronouns, etc.) and vocabulary (collocations, idioms) [4].

### Part 6: Text Completion
* **Content:** Exactly 16 questions divided across 4 different reading passages [5].
* **Focus:** Diverse business formats featuring unique names and companies. Each passage contains 3 grammar/vocabulary questions and exactly 1 sentence insertion question at the 4th blank [5].
* **Formatting:** Automatically appends structural `[段落说明]` tags to paragraphs, headlines, and salutations without leaving blank lines [5].

### Part 7: Reading Comprehension
* **Content:** 12 to 14 questions divided across 3 sets (Single, Double, and Triple passages) [6].
* **Focus:** 3 distinct topics ranging from 100 to 600 words per passage. Tests multi-passage logic by requiring you to cross-reference interconnected texts [6].
* **Formatting:** Multi-passages are separated by `------[段落说明]`. Text messages are strictly prohibited from being generated [6]. 

## Notes
* The skill automatically stops after generating the requested section. It will not generate the next part automatically [3]. 
* Interactive quiz elements and extra conversational filler are disabled to provide a clean, copy-paste-ready output [3].


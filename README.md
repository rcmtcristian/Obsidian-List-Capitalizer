# Obsidian AutoCorrect Plugin

This plugin automatically fixes common capitalization errors in your Obsidian notes. It specifically targets words where the first two letters are mistakenly capitalized (e.g., `HAllo` instead of `Hallo`) and corrects them. Additionally, features ensure that list items, checkboxes, sentences, and inline titles are formatted correctly while protecting codeblocks and math expressions from auto-correction.

## Features

- **Automatic Correction**  
  The plugin detects words where the first two letters are uppercase and the third letter is lowercase, automatically correcting them (e.g., `HAllo` → `Hallo`).

- **Exclusion List**  
  You can specify a list of words (comma separated) that should be excluded from any corrections.

- **Abbreviation List**  
  Define common abbreviations (like `e.g.`, `i.e.`, or `etc.`) that the plugin recognizes. When these abbreviations are used, they prevent the plugin from mistakenly capitalizing words immediately following them, ensuring correct capitalization after abbreviations in your sentences.

- **Capitalize List Items**  
  When enabled, any line starting with `-`, `*`, or `1.` will have the first letter of the following word automatically capitalized, including sub-lists.
  
  **Example:**  
  - Before: `- hallo`  
  - After: `- Hallo`  
  
  Additionally, if a list item is incorrectly capitalized (e.g., `- HAllo`), the plugin will correct it to `- Hallo`.

- **Capitalize Checkbox Items**  
  When enabled, checkbox list items (e.g., `- [ ] task`, `- [x] done`) will have the first letter of the following word automatically capitalized.
  
  **Example:**  
  - Before: `- [ ] buy groceries`  
  - After: `- [ ] Buy groceries`

- **Capitalize Inline Title**  
  When enabled, automatically capitalizes the first letter of each word in the note's inline title (the title shown at the top of the note). The file will be renamed to match the capitalized title.
  
  **Example:**  
  - Before: `my important note`  
  - After: `My Important Note`

- **Capitalize Sentence Beginnings**  
  When enabled, the first letter of each sentence will be capitalized if it was typed in lowercase.

- **Codeblock Protection**  
  The plugin detects fenced codeblocks (` ``` `) and inline code (using backticks) and skips any corrections within these areas.

- **Mathblock Protection**  
  The plugin detects LaTeX math expressions (both inline `$...$` and block `$$...$$`) and leaves them unchanged, preventing auto-correction of mathematical notations.

- **YAML Front-matter Protection**  
  The plugin detects YAML frontmatter and won't correct inside it.

- **Trigger on Various Characters**  
  Corrections are triggered by specific punctuation characters (e.g., space, period, comma, etc.) or by pressing Enter. When Enter is pressed, the plugin checks the previous line for corrections.

## Installation

### Through Obsidian Community Plugins

1. Open **Settings** > **Community Plugins** in Obsidian.
2. Search for "Obsidian AutoCorrect Plugin" and install it.
3. Enable the plugin.

### Manual Installation

1. Clone or download the repository.
2. Place the plugin folder in your vault under `.obsidian/plugins/obsidian-auto-correct`.
3. Restart Obsidian and enable the plugin from the Community Plugins section.

## Configuration

The plugin provides the following settings:

- **Exclusion List**  
  Enter words (comma separated) that should be excluded from any auto-correction.

- **Capitalize List Items**  
  When enabled, any list item (lines starting with `-`, `*`, or `1.`) will have the first letter of the following word capitalized.

- **Capitalize Checkbox Items**  
  When enabled, checkbox items (lines like `- [ ]` or `- [x]`) will have the first letter of the following word capitalized.

- **Capitalize Inline Title**  
  When enabled, automatically capitalizes the first letter of each word in the note's inline title and renames the file accordingly. Requires "Show inline title" to be enabled in Settings → Appearance.

- **Capitalize Sentence Beginnings**  
  When enabled, the first letter of each sentence will be capitalized if it was typed in lowercase.

- **Abbreviations**  
  Define common abbreviations (visible only when "Capitalize Sentence Beginnings" is enabled) that end with a period but should not trigger sentence capitalization for the following word.

## Usage Tips

- Enable only the features you need to avoid over-correction.
- Use the exclusion list for proper nouns, acronyms, or specialized terms you don't want modified.
- The inline title capitalization works in real-time as you type.
- All corrections respect protected areas (code, math, YAML frontmatter).

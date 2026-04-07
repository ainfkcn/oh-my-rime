# RIME Double Pinyin Configuration

A minimalist, personalized RIME configuration forked from [Mintimate/oh-my-rime](https://github.com/Mintimate/oh-my-rime).

## Overview

This repository contains a streamlined RIME input method configuration focused on:
- **Primary Method**: Natural Double Pinyin (自然码双拼)
- **Auxiliary Methods**: English input, Wubi stroke lookup, Radical lookup
- **Platform**: Windows (Weasel)

## What's Included

### Core Schemes
- `double_pinyin.schema.yaml` — Natural code double pinyin (自然码双拼)
- `melt_eng.schema.yaml` — English input support
- `radical_pinyin.schema.yaml` — Radical/stroke lookup
- `wubi98_mint.schema.yaml` — Wubi shortcut lookup

### Dictionaries
- `rime_mint.dict.yaml` — Main vocabulary dictionary
- Supporting dictionaries: English, radical, and Wubi lookup tables

### Features
- **Lua Filters**: Smart punctuation, spell checking, calculator, lunar calendar, etc.
- **OpenCC**: Simplified/Traditional Chinese conversion
- **Learning Database**: Auto-saving input habits in `rime_mint.userdb/`

## Structure

```
.
├── double_pinyin.schema.yaml    # Main input method
├── melt_eng.schema.yaml         # English scheme
├── radical_pinyin.schema.yaml   # Radical lookup
├── wubi98_mint.schema.yaml      # Wubi lookup
├── default.yaml                 # Framework config
├── weasel.yaml                  # Windows-specific settings
├── dicts/                       # Dictionary files
├── lua/                         # Lua filters and features
├── opencc/                      # Character set conversion
└── preview/                     # Preview configurations
```

## Getting Started

1. **Clone or sync** this configuration to your RIME user data directory
2. **Restart Weasel** or reload with `Deploy`
3. **Select scheme**: Switch to "自然码双拼" from input method menu
4. **Test**: Start typing with the double pinyin method

### Keyboard Map

Natural Double Pinyin uses phone keypad mapping:
- Similar to Sogou, Tencent Input Methods
- Each consonant + vowel maps to a specific key combination
- See `default.custom.yaml` for detailed key bindings

## Customization

Edit the following files to personalize:

- **`default.custom.yaml`** — UI, menu options, basic settings
- **`double_pinyin.schema.yaml`** — Main method configuration
- **`weasel.yaml`** — Windows appearance and behavior
- **`dicts/`** — Add or modify custom dictionary entries

## Syncing with Upstream

To stay up-to-date with improvements from the original [Mintimate/oh-my-rime](https://github.com/Mintimate/oh-my-rime):

```bash
git remote add upstream https://github.com/Mintimate/oh-my-rime.git
git fetch upstream
git merge upstream/main  # Review changes carefully
```

Note: This fork has been significantly trimmed. Merges may require conflict resolution.

## File Cleanup

This repository has been optimized by removing:
- Unused input method schemes (Bopomofo, Cangjie, Zhuyin, etc.)
- Irrelevant dictionary files
- Platform-specific configs (macOS, Linux)
- Build cache and utility tools

Result: A minimal, focused configuration for Double Pinyin only.

## License

Inherited from [oh-my-rime](https://github.com/Mintimate/oh-my-rime) — See LICENSE file.

## Credits

- Original framework: [rime-aca](https://github.com/iDvel/rime-settings)
- Main vocabulary: [薄荷输入法](https://github.com/Mintimate/oh-my-rime)
- Forked from: [Mintimate/oh-my-rime](https://github.com/Mintimate/oh-my-rime)

## Troubleshooting

- **Method not appearing**: Check `default.yaml` `schema_list` section
- **Dictionary not loading**: Verify path in `*.schema.yaml` matches actual filenames
- **Need to rebuild**: Redeploy Rime;
- **Input stuck**: Check `installation.yaml` and redeploy Rime;

For detailed RIME documentation, visit [RIME website](https://rime.im)


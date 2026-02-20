# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the **intercessions** repository, containing church intercession prayers used during Sunday services at an ecumenical Anglican church with members from multiple denominations (including Baptists and Lutherans).

## Repository Structure

Intercessions are stored as individual markdown files in the root directory:

- **Dated intercessions**: Use `yyyy-mm-dd.md` format (e.g., `2025-07-27.md`, `2025-09-21.md`)
- **Undated intercessions**: Use theme-based slugs (e.g., `holy-communion-service.md`, `generous-god.md`, `a-kings-heart.md`)

## Adding New Intercessions

**IMPORTANT:** Whenever you create a new intercession file, you MUST update BOTH the README.md AND index.md files:

1. Add a new entry to the intercessions list under the appropriate year in **both files**
2. Use the format: `[DD Month - Title/Theme](filename.html)`
   - Example: `[23 November - The Gospel in Genesis](2025-11-23.html)`
   - Note: Always use `.html` extension in links (not `.md`) for proper GitHub Pages navigation
3. Keep the list in chronological order (earliest to latest)
4. Make sure the link text includes both the date and the theme/title for easy navigation
5. Ensure both README.md and index.md stay synchronized with identical intercession listings

**Why two files?**
- `README.md` is displayed on the GitHub repository page (no Jekyll front matter needed)
- `index.md` is the homepage for the GitHub Pages site (requires Jekyll front matter)
- Both files must have identical content except for the front matter in index.md

This ensures the repository remains well-organized and visitors can easily find prayers by theme or date, whether viewing on GitHub or the published website.

## Intercession File Format

Each intercession file follows a consistent markdown structure with Jekyll front matter:

```markdown
---
layout: default
title: [Title/Theme]
date: YYYY-MM-DD
---

# [Title/Theme]

**Date:** [date or empty if not available]

**Bible Reading:** [scripture reference or empty if not available]

---

[Prayer content including opening, petitions, and closing with Lord's Prayer]
```

**Important notes about file format:**
- Always include Jekyll front matter (the YAML block at the top between `---` markers)
- The `layout: default` uses the minima theme for consistent styling on GitHub Pages
- The `title` should match the heading below for consistency
- The `date` should be in `YYYY-MM-DD` format for proper sorting and metadata

## Writing Style and Tone

- Use **poetic line breaks** and thoughtful pacing with ellipses (...) to create natural pauses for reflection
- Keep language **accessible yet reverent** - avoid overly formal or archaic expressions
- Balance **contemporary concerns with timeless themes** of faith
- Use **concrete imagery** that connects biblical narratives to present-day life
- Prayers should feel **personal yet communal**, speaking to shared experiences
- **Always capitalize pronouns referring to God** (You, Your, Yours) throughout the prayer to maintain reverence
- **Address God directly** throughout the prayer - avoid explaining things to the congregation or making theological points. The prayer is a conversation with God, not a teaching moment
- **Be careful with light/darkness imagery** when praying for those in need - avoid language that suggests people experiencing hardship are spiritually "in darkness." Focus on God's compassion and practical service instead
- **Use single dashes only** - always use the standard hyphen-minus character (-). Never use em dashes or en dashes
- **Use trailing two spaces for line breaks** - in markdown, a single newline within a paragraph is ignored when rendered. To preserve poetic line breaks, add two spaces at the end of each line that should break (except the last line of a stanza, which is followed by a blank line). This applies to all prayer content lines within stanzas

## Common Structural Elements

### Opening
- Begin with "Let us pray" (may add instructions for responsive prayers)
- Open with addressing God using a descriptive name that connects to the theme (e.g., "Faithful God...", "Generous God...", "God of all wisdom and grace...")
- Establish the biblical or theological foundation for the prayer

### Main Sections (typically 4-6)
Each section should cover one theme:
1. **The Church** (local congregation and global Church)
2. **Suffering and illness** (body, mind, spirit - including specific people when appropriate)
3. **Young people and families**
4. **Community needs** (grief, loneliness, financial struggles)
5. **Church leadership and decisions** (Council, events, finances)
6. **Seasonal or specific events** (Christmas, Easter, church milestones)

### Closing
- Concluding prayer often circles back to the opening theme
- Transition to the Lord's Prayer with invitational language
- Include flexibility: "Feel free to do so in whatever language or version you're most comfortable with"

## Responsive Prayer Format

When using the responsive format:
- Add instruction after "Let us pray": `When I say "Lord, in your mercy," please respond with "hear our prayer."`
- End each section with:
  ```
  Lord, in your mercy...
  hear our prayer.
  ```
- This format works well for prayers with clear thematic sections

## Incorporating Church News and Events

When church leadership provides updates:
- **Keep it concise and prayerful** rather than explanatory or report-like
- **Make it generic** while still acknowledging the reality (e.g., avoid mentioning specific dollar amounts or excessive detail)
- **Focus on the spiritual aspect**: decisions → wisdom; finances → provision and stewardship; events → joy and encounters with God
- **Focus on immediate events only** (within 2 weeks) - distant events don't need to be mentioned
- **Avoid administrative details** like finding a treasurer, specific fundraising targets, etc.

Example transformation:
- Too specific: "We need £50,000 for building repairs and have only £30,000 in savings"
- Better: "We lift up the decisions being made about our finances, our mission, and the care of this place. Grant wisdom to those who lead, and guide us all in faithful stewardship."

## Handling Prayer Lists and Names

- **Keep illness prayers generic and broad** rather than listing individual names from weekly prayer lists
- **Use broad categories**: "those affected by flu and winter illnesses," "those awaiting, undergoing, or recovering from tests and treatment," "those supporting loved ones affected by health issues"
- **Only mention specific individuals** when they are highlighted in church news for special reasons (e.g., milestone birthdays, specific pastoral situations being shared with the congregation)
- The detailed prayer list is for the person leading the prayer to hold privately, not for verbatim inclusion in the written intercession
- This keeps prayers universally applicable and spiritually focused rather than list-like

## Lord's Prayer Options

Three common patterns:
1. **English only** (most formal services)
2. **Portuguese only** (emphasizing the Brazilian/Portuguese-speaking community)
3. **Both Portuguese and English** (celebrating diversity, often used when that's a theme)

The Portuguese version used:
```
Pai nosso que estás nos céus,
santificado seja o teu nome,
venha o teu reino,
seja feita a tua vontade,
assim na terra como no céu.

O pão nosso de cada dia dá-nos hoje,
e perdoa-nos as nossas dívidas,
assim como nós também perdoamos aos nossos devedores.

E não nos deixes cair em tentação,
mas livra-nos do mal,
pois teu é o reino, o poder e a glória para sempre. Amém.
```

## Common Themes to Address

- **Faith and trust** in God's promises
- **Unity in diversity** (denominational backgrounds)
- **Generosity and stewardship**
- **Service and hospitality**
- **Young people** navigating identity, pressure, and faith questions
- **Global church** in places of persecution or hardship
- **Community impact** (the church as a community center)
- **Healing** for body, mind, and spirit
- **Provision** for material and spiritual needs

## GitHub Pages Setup

This repository is published as a website using GitHub Pages with Jekyll:

- **Website URL**: https://stiksy.github.io/intercessions/
- **Theme**: Minima (clean, readable design)
- **Automatic deployment**: GitHub Actions workflow builds and deploys on every push to main branch

**Key files for GitHub Pages:**
- `_config.yml` - Jekyll configuration (site title, theme, URL settings)
- `.github/workflows/jekyll.yml` - Automated build and deployment workflow
- `index.md` - Website homepage (mirrors README.md content)
- `README.md` - GitHub repository page (also used for web with .html links)

**Important:** When updating README.md or index.md, always keep them synchronized with identical content.

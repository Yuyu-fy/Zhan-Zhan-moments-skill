# Zhan-Zhan WeChat Moments Caption Skill

Turn the light, weather, colors, and subtle movement in travel photos into vivid Chinese WeChat Moments captions with room for imagination.

`zhan-zhan-moments-skill` is a creative Skill for Codex. It uses real visual details and the user’s own experience to produce concise, restrained captions that are ready to publish. It avoids travel logs, attraction guides, and generic inspirational language.

## Use Cases

- Travel, landscape, city, and nature photography
- Architecture, old towns, bookstores, exhibitions, and cultural spaces
- Sunsets, night scenes, rain, window views, and weather photography
- Everyday scenes and cohesive photo grids
- Refining or shortening an existing WeChat Moments caption

This Skill is not intended for travel guides, factual research, marketing copy, or photo-by-photo descriptions.

## Core Capabilities

- **Scene extraction**: Identifies the subject, lighting, time, colors, textures, movement, and emotional direction.
- **Adaptive length**: Uses short lines for a strong single image and short prose for photo collections or cultural settings.
- **Three-stage composition**: Enters the scene, brings it to life, and closes with a restrained emotional aftertaste.
- **Original imagery**: Creates metaphors and personification from the current photos instead of reusing signature lines from the source material.
- **Factual grounding**: Does not invent locations, history, relationships, or experiences the user has not provided.
- **Anti-template review**: Filters out travel logs, slogans, excessive ornamentation, and repetitive sentence patterns.

## How It Works

```text
Photos and context
        ↓
Build a scene card
        ↓
Choose length and writing mode
        ↓
Scene → Movement → Aftertaste
        ↓
Check originality and factual accuracy
        ↓
One publish-ready caption
```

If the photos or description do not provide enough usable detail, the Skill briefly asks about the location or subject, time or lighting, and intended emotion. When the context is sufficient, it writes the caption immediately.

## Quick Start

### 1. Install

Download the repository, preserve its directory structure, and place the project folder in your personal Codex Skills directory:

```text
~/.codex/skills/zhan-zhan-moments-skill/
```

The installed Skill should retain the following structure:

```text
zhan-zhan-moments-skill/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── style-observations.md
```

### 2. Invoke

Upload your photos, provide any necessary context, and reference the Skill by name:

```text
$zhan-zhan-moments-skill Write a Chinese WeChat Moments caption for these travel photos.
They were taken on an old street after the rain at dusk. Keep the mood quiet and restrained.
```

You can also make a natural-language request:

```text
Use the Zhan-Zhan style to write a short Chinese caption for this sunset photo.
```

## Recommended Input

For a caption that closely matches the photos, consider providing:

- The approximate location or main subject
- The time, weather, and lighting
- What happened
- The emotion you want to express
- Information to include or avoid
- Preferences for length, emoji, and number of alternatives

You do not need to provide everything at once. When the image is sufficiently clear, the Skill writes directly from the visible scene.

## Example

Input:

```text
A single photo. The rain has just stopped, and the evening streetlights are reflected on the stone road. Keep it quiet.
```

Generated Chinese caption:

```text
雨把街灯轻轻铺在石板路上，暮色便有了温度。走到这里，脚步也不必太急~
```

By default, the Skill returns one finished caption without labels such as “WeChat Moments caption:”. It provides alternatives or explains its writing choices only when explicitly requested.

## Design Principles

1. **Photos before ornamentation**: Every caption must be grounded in at least one visible detail.
2. **Emotion grows from the scene**: Do not force ordinary images into grand philosophical statements.
3. **Literary does not mean overloaded**: Use only a small number of effective literary devices in each caption.
4. **Learn the structure, not the wording**: Preserve the observational method while keeping every output original.
5. **Let text sit beside the image**: Add emotional resonance instead of explaining what the photo already shows.

See [SKILL.md](./SKILL.md) for the complete workflow and [style-observations.md](./references/style-observations.md) for a summary of the source material’s stylistic characteristics.

## Repository Structure

- `SKILL.md`: Trigger conditions, writing workflow, output rules, and quality checks.
- `agents/openai.yaml`: Display name, short description, and default invocation prompt.
- `references/style-observations.md`: Stable stylistic traits and recommended length ranges extracted from the source material.

## Privacy and Originality

- Before uploading photos of people, make sure you have permission to use them and avoid sharing unnecessary sensitive information.
- Review names, locations, dates, relationships, and other factual details before publishing generated content.
- This project learns visual observation, language rhythm, and writing techniques. It does not encourage copying source sentences or publishing fabricated experiences as another real person.

## Feedback and Contributions

Use GitHub Issues to report or suggest:

- Captions that do not match the photos or feel overly formulaic
- New photographic scenarios and edge cases
- More precise negative examples and quality checks
- Improvements to length, tone, and originality

When changing the writing rules, test short captions, photo grids, cultural spaces, night scenes, and everyday photography to avoid overfitting to a single example.

## License

Rights to use, modify, and distribute this project are governed by the repository’s `LICENSE` file. If no license is provided, all rights are reserved by default.

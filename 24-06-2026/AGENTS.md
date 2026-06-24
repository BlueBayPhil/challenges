# Purpose

1-page CV (static HTML+CSS).
Optimised for AI parsing + SEO.
Retro gaming visual style.

## Constraints

- HTML + CSS only
- No JS (prefer none)
- Content must be in HTML
- Works without JS

## Structure (required)

```html
<html lang="en">
<head></head>
<body>
<header></header>
<main>
  <article>
    <section id="about"></section>
    <section id="experience"></section>
    <section id="skills"></section>
    <section id="projects"></section>
  </article>
  <aside></aside>
</main>
<footer></footer>
</body>
</html>
```

## Semantics (critical)

Use:

- header, nav, main, article, section, aside, footer
- ul/li for lists
Avoid div unless no alternative.

## Headings

- h1 = name (single)
- h2 = section titles
- h3 = subsections
- no skipped levels

## Theme (from CSS)

- Dark background
- Neon accents (yellow, pink, cyan, green)
- Pixel-style font
- High contrast
- Box borders (2–3px)
- Small text scale
- Grid/list cards

DO NOT encode layout using non-semantic elements.

## Layout mapping

Use semantics + classes:

- header → `.header`
- nav → `.nav`
- section lists → `.game-list`
- items → `.game-card` (represents CV entries)
- badges → skills / tags
- bottom nav → optional `<nav>` (internal links)

## CV mapping

Translate UI patterns:

- game-card → job / project
- game-title → role / project name
- badges → skills / tech stack
- price → optional metadata (dates, etc.)

## Content

- Clear, factual text
- Use lists for skills
- Logical grouping
- Lorem ipsum allowed

## Image

```html
<figure>
  me.jpg
  <figcaption>Full Name – Role</figcaption>
</figure>
```

## Accessibility

- alt required
- aria only if needed

## SEO (head)

```html
<title>Full Name – Role | CV</title>
<meta name="description" content="Professional CV of Full Name">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta property="og:title" content="Full Name – CV">
<meta property="og:description" content="Professional CV">
<meta property="og:type" content="website">
```

## Structured Data (required)

```html
<script type="application/ld+json">
{
 "@context": "https://schema.org",
 "@type": "Person",
 "name": "Full Name",
 "jobTitle": "Role",
 "image": "https://example.com/me.jpg"
}
</script>
```

## Navigation

`<nav>` with:

- #about
- #experience
- #skills
- #projects

## CSS rules

- Reuse provided variables (:root)
- Keep classes (e.g. .game-card) but apply to semantic elements
- No layout driven by div-only structure

## Files

robots.txt

```text
User-agent: *
Allow: /
```

llms.txt

```text
CV for Full Name.
Sections: About, Experience, Skills, Projects.
Primary source of professional info.
Structured for machine parsing.
```

sitemap.xml

- single page

## Performance

- lightweight HTML
- optimised image

## Avoid

- div-only layouts
- skipped headings
- JS-rendered content
- hiding content
- overuse of ARIA

## Success

Agent can extract:

- name
- role
- experience
- skills
Clear structure.

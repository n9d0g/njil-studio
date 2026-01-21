# njil.dev Studio

Sanity Studio for managing content on [njil.dev](https://njil.dev) — Nathan Lardizabal's personal portfolio and blog.

## Getting Started

```bash
# Install dependencies
npm install

# Run the development server
npm run dev
```

The studio will be available at `http://localhost:3333`.

## Content Schemas

### Blog

The main content type for blog posts with the following fields:

| Field | Type | Description |
|-------|------|-------------|
| Title | string | The main title of the blog post |
| Slug | slug | URL-friendly identifier generated from the title |
| Author | string | The author of this blog post (defaults to Nathan Lardizabal) |
| Published At | datetime | The date and time when this post was published |
| Description | text | Short summary for SEO and previews |
| Tags | reference[] | Categorize this post with relevant tags |
| Gallery Images | image[] | Images to display in a bento grid at the bottom of the post |
| Body | portable text | The main content of the blog post |

The body field supports:
- Rich text blocks (headings, paragraphs, lists, links, etc.)
- Inline images with alt text and captions
- Code blocks with syntax highlighting (JavaScript, TypeScript, HTML, CSS, JSON, Markdown, Bash)

### Tag

Reusable tags for categorizing blog posts:

| Field | Type | Description |
|-------|------|-------------|
| Name | string | The tag name |
| Slug | slug | URL-friendly identifier for tag pages |

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start the development server |
| `npm run build` | Build the studio for production |
| `npm run deploy` | Deploy the studio to Sanity |

## Tech Stack

- [Sanity v4](https://www.sanity.io/) — Headless CMS
- [React 19](https://react.dev/) — UI framework
- [TypeScript](https://www.typescriptlang.org/) — Type safety
- [@sanity/code-input](https://www.npmjs.com/package/@sanity/code-input) — Code block support with syntax highlighting

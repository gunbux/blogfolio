Personal Blogfolio, build with Ghost and NextJS

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Adding Blog Posts

We use Ghost as a Content Management System (CMS) to manage our blog posts. To launch ghost, `cd` into the `ghost` directory,
and run ghost in a local docker.

```bash
docker run -d --name ghost-blog -e NODE_ENV=development -e url=http://localhost:3002/blog -p 3002:2368 -v <dir>:/var/lib/ghost/content ghost
```

Open [http://localhost:3002](http://localhost:3002) with your browser to see the result. Go to [http://localhost:3002/ghost](http://localhost:3002/ghost)
for the admin panel

## Publishing Your Website

In order to publish this Ghost + NextJS frankensite, we want to:

1. Generate static pages for blog posts using `gssg`.
2. Move the static folder into the public dir
3. Publish on site of choosing (Cloudflare pages or netlify)


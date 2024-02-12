[![Netlify Status](https://api.netlify.com/api/v1/badges/76c2910b-ef74-4452-a9e7-f8668ad8a15d/deploy-status)](https://app.netlify.com/sites/gleeful-fox-1731f6/deploys)

# Quick CV \ Resume template based on Astro Starter Kit: Minimal

- At `index.astro` update the following:
  - `personalDetails`
  - `skills`
  - `languages`
- Create `md` files with your experiences and education in their respective folders
- Edit the template as you see fit, add new sections, hide sections, remove sections, customize styles
- Good luck & Enjoy

## 🖼️ Live

Resume is hosted at netlify, you can visit it at [https://cv.sead.dev](https://cv.sead.dev) to check it out.

## 🚀 Project Structure

Inside of this project, you'll see the following folders and files:

```text
/
├── public/
├── src/
│   ├── components/
│   │   ├── Entry.astro
│   │   ├── LinkWithArrow.astro
│   │   ├── Footer.astro
│   │   ├── PersonalDetails.astro
│   │   ├── Section.astro
│   │   └── Skill.astro
│   ├── education/
│   │   └── 01_school.md
│   ├── experiences/
│   │   ├── 01_template_job_1.md
│   │   ├── 02_template_job_2.md
│   │   └── 03_template_job_3.md
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name. In our case for the resume template, we are skipping over that feature but we make use of `education` and `experiences` folders to dynamically fill out their respective sections with `await Astro.glob<EntryProps>("../experiences/*.md");` command.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory. This is where you can put your profile picture, or you can put it in `images` and replace `images/person_placeholder.svg`.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

[Astro Docs](https://docs.astro.build)

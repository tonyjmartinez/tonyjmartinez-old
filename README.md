# tonyjmartinez.com

My personal site: a single page with a short intro. Built with [Astro](https://astro.build) and the Rosette
components from [succulents.info](https://github.com/tonyjmartinez/succulents.info).

```sh
npm install
npm run dev     # http://localhost:4321
npm run build   # static site in dist/
npm run check   # type-check
```

## Deploying

Hosted on Firebase Hosting (project `tonyjmartinez-site`). GitHub Actions deploys automatically:

- **Push to `master`** → builds and deploys to tonyjmartinez.com.
- **Pull request** → deploys a temporary preview channel and comments the URL on the PR.

Both use the `FIREBASE_SERVICE_ACCOUNT_TONYJMARTINEZ_SITE` repository secret. To recreate it, run
`npx firebase-tools init hosting:github` in this folder and follow the prompts.

Manual deploy: `npm run build && npx firebase-tools deploy --only hosting`.

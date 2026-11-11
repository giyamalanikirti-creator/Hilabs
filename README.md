# HiLabs single-screen v1

A dependency-free, responsive healthcare AI landing-page concept. The public HiLabs website could not be fetched because of the cloud network policy, so this is an original concept rather than a verified reproduction. The contact dialog is a demo: it sends and stores no information.

## Run

Use the existing checkout at `/workspace/Hilabs`. Each cloud task is isolated; do not create a Git worktree unless requested.

```sh
python3 -m http.server 3000 --bind 127.0.0.1 --directory /workspace/Hilabs/public
```

No install or build is required. Restart the server in each new task. Verify with `curl --fail http://127.0.0.1:3000/` and a browser.

## Deploy

Import this repository into an authenticated Vercel account, using framework preset **Other**, no build command, and output directory **public**. The included `vercel.json` sets the static output directory. Alternatively, from the checkout, use an authenticated Vercel CLI and run `vercel deploy --prod`.

The current environment has no Vercel authentication and blocks `api.vercel.com`. Allow `api.vercel.com`, `vercel.com`, and the deployment's `*.vercel.app` host in environment settings, then authenticate through Vercel's supported login flow. Never put tokens in source or chat.

## Verified in this environment

- HTTP response matches the static entry file.
- Chromium checks at 1440px, 390px, and 320px: no horizontal overflow; contact dialog opens, accepts a valid email, displays the demo confirmation, and closes.
- No browser JavaScript errors in those checks.

Production deployment has not completed. Saving reusable cloud startup instructions failed in the platform configuration tool; these instructions are retained here instead.

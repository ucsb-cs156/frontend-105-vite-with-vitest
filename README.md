# README.md: frontend-101-vite-plain

In this repo, we show a plain vanilla version of a vite project,
as it would look when you first bootstrap it.

To recreate this repo from first principles:

1. Create an empty repo
2. clone it and cd into it
3. Use `nvm install --lts; nvm use --lts` to ensure you are using
   the latest version of node.

   For this repo, these are the version we used:
   ```
   % nvm  install --lts; nvm use --lts
   Installing latest LTS version.
   v22.18.0 is already installed.
   Now using node v22.18.0 (npm v10.9.3)
   Now using node v22.18.0 (npm v10.9.3)
   % 
   ```
4. Per instructions at <https://vite.dev/guide/#scaffolding-your-first-vite-project>, use this command:

   ```
   npm create vite@latest          
   ```


5. You'll be asked a series of questions; here are the
   answers we provided:

   First, is it ok to install `create-vite@7.1.1`? Say yes:
   ```
   Need to install the following packages:
   create-vite@7.1.1
   Ok to proceed? (y) y
   ```

6. For `Project name:`, the default is `vite-project`.  We'll use
   `frontend` instead.  
 
   ```
   │
   ◆  Project name:
   │  frontend█
   └
   ```

7. Select a framework: choose `React`

   ```
    ◆  Select a framework:
    │  ○ Vanilla
    │  ○ Vue
    │  ● React
    │  ○ Preact
    │  ○ Lit
    │  ○ Svelte
    │  ○ Solid
    │  ○ Qwik
    │  ○ Angular
    │  ○ Marko
    │  ○ Others
    └
   ```

8. Select a variant.  Choose    `JavaScript + SWC`

   ```
    Select a variant:
    │  ○ TypeScript
    │  ○ TypeScript + SWC
    │  ○ JavaScript
    │  ● JavaScript + SWC
    │  ○ React Router v7 ↗
    │  ○ TanStack Router ↗
    │  ○ RedwoodSDK ↗
    │  ○ RSC ↗
    └
   ```

9. You should get:
   ```
    ◇  Scaffolding project in /Users/pconrad/github/ucsb-cs156/frontend-101-vite-plain/frontend...
    │
    └  Done. Now run:

    cd frontend
    npm install
    npm run dev

    %
   ``` 

10. Run the command indicated: 
    
    ```
    cd install
    npm install
    npm run dev
    ```

    You should see this on the screen after typing `npm run dev`


   ```
    VITE v7.1.2  ready in 408 ms

    ➜  Local:   http://localhost:5173/
    ➜  Network: use --host to expose
    ➜  press h + enter to show help
   ```

   Open a web browser to <http://localhost:5173/> and you should see this:

   INSERT SCREENSHOT HERE

   That means it's working!

## Command you can try

The out of the box experience with vite has the following commands, which you can list by typing `npm run`:

```
% npm run
Scripts available in frontend@0.0.0 via `npm run-script`:
  dev
    vite
  build
    vite build
  lint
    eslint .
  preview
    vite preview
%
```

Here's what they do:

| Command | Explanation |
| `npm run dev` | Serve the site in development mode.  This is how you usually test when running in development. It corresponds to the old `npm start` command we used to use with CRA |
| `npm run build` | Build an optimized production build.  This is slower, but it should be done after development work is done to ensure that in production mode, the site still works properly.   The build is placed, by default in a directory called `site`; note that we might override this to `build` since that's what most of our legacy code expects because of CRA |
| `npm run preview` | This serves up the site from the production build. This command can only be used after a previous run of `npm run build` |
| `npm run lint` | This runs `eslint` on the code base |

# Next steps

Because the intention is for this repo to be a snapshot of a plain vanilla vite applicaiton, we won't do anything more with it.

We'll go through a series of steps to incorporate other tools into the repo, including changing the content, testing with vitest, CI/CD with Github Actions, adding React-Bootstrap, storybook, StrykerJS, and other dependencies that are a part of the CMPSC 156 ecosystem.

TODO: Link those repos here when done.


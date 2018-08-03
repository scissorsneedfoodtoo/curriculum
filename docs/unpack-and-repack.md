### Unpack and Repack

`npm run unpack` extracts challenges into separate HTML files under `challenges/unpacked` for easier viewing and editing. The files are `.gitignore`d and will *not* be checked in, and is essentially a tool for editing the `challenge.json` files in the browser.

These unpacked files are self-contained and run their own tests -- open a browser JS console to see the test results.

> **Note**: These in-browser tests should work for simple JavaScript challenges. But other types of challenges may not fare so well. For HTML challenges, challenge tests assume that the solution HTML is the only HTML on the whole page, so jQuery selectors may select seed *and* solution elements. For React / Modern JS challenges, we would need to transpile JSX or ES6 before running the tests.

`npm run repack` gathers up the unpacked/edited HTML files into challenge-block JSON files. After running repack, use `git diff` to see the changes in your console.

When editing the unpacked files, you must only insert or edit lines between comment fences like `<!--description-->` and `<!--end-->`. In descriptions, you can insert a paragraph break with `<!--break-->`.

Unpacked lines that begin with `//--JSON:` are parsed and inserted verbatim.

If you want to **add a challenge**, **change the order** of challenges in a block, or **edit the title** or any other fields of a challenge, you must do that work *inside the main seed JSON file* and then re-run `unpack`.
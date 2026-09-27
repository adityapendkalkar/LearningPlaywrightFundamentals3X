# Playwright CLI Commands

This project has no npm scripts defined, so all commands are run with `npx playwright ...`.

## Running Tests

| Command | What it does |
| --- | --- |
| `npx playwright test` | Runs all tests in the project. |
| `npx playwright test tests/example.spec.ts` | Runs a single test file. |
| `npx playwright test -g "has title"` | Runs only tests whose title matches the given pattern (`-g` / `--grep`). |
| `npx playwright test --headed` | Runs tests with a visible browser window instead of headless. |
| `npx playwright test --ui` | Opens interactive UI mode with a watch panel, time-travel debugging, and locator picking. |
| `npx playwright test --debug` | Runs tests in debug mode using the Playwright Inspector to step through actions. |
| `npx playwright test --project=chromium` | Runs tests for a single configured project/browser (e.g. `chromium`, `firefox`, `webkit`). |
| `npx playwright test --workers=4` | Sets the number of parallel worker processes. |
| `npx playwright test --retries=2` | Retries failed tests up to the given number of times. |
| `npx playwright test --repeat-each=3` | Repeats every test the given number of times (useful for detecting flakiness). |
| `npx playwright test --last-failed` | Re-runs only the tests that failed in the previous run. |
| `npx playwright test --list` | Lists all tests that would run without actually executing them. |
| `npx playwright test --trace on` | Records a trace for every test, viewable in the trace viewer. |

## Generating & Debugging

| Command | What it does |
| --- | --- |
| `npx playwright codegen https://playwright.dev/` | Opens a browser and records your actions, generating test code automatically. |
| `npx playwright codegen --device="iPhone 13"` | Same as above but emulates a specific device profile. |
| `npx playwright show-report` | Opens the generated HTML test report in a browser. |
| `npx playwright show-trace trace.zip` | Opens a captured trace file in the trace viewer for step-by-step inspection. |

## Install / Setup

| Command | What it does |
| --- | --- |
| `npx playwright install` | Downloads and installs the Playwright browser binaries. |
| `npx playwright install --with-deps` | Installs browsers plus required OS-level dependencies (typically used in Linux CI). |
| `npx playwright install chromium` | Installs a single browser only (e.g. `chromium`, `firefox`, `webkit`). |
| `npx playwright uninstall` | Removes the installed Playwright browser binaries. |

## Utilities

| Command | What it does |
| --- | --- |
| `npx playwright open https://site.com` | Opens the given URL in a browser for manual inspection. |
| `npx playwright screenshot <url> out.png` | Captures a screenshot of the given URL and saves it to a file. |
| `npx playwright pdf <url> out.pdf` | Generates a PDF of the given URL (Chromium only). |
| `npx playwright cr <url>` | Quick-opens a URL in Chromium. |
| `npx playwright ff <url>` | Quick-opens a URL in Firefox. |
| `npx playwright wk <url>` | Quick-opens a URL in WebKit. |
| `npx playwright --version` | Prints the installed Playwright version. |

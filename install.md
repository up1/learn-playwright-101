# Add Playwright to your project


## 1. Playwright as a test runner
```
$npm init playwright@latest 
```

Generate folder `./cypress`
* tests/
* playwright.config.js/ts

Run test
```
$npx playwright test

// Run with UI mode
$npx playwright test --ui
```

## 2. Playwright as a library
```
$npm init -y
$npm i -d @playwright/test
```

Config file `package.json`
```
"scripts" : {
    "test": "playwright test"
}
```

Run test
```
$npm run test

> project-lib@1.0.0 test
> playwright test

Error: No tests found
```

Create test case in folder `tests`
```
import { test } from "@playwright/test";

test('Your test name goes here', async ({ page }) => {
  // Your test steps go here
})
```

Run test again
```
$npm run test             

> project-lib@1.0.0 test
> playwright test


Running 1 test using 1 worker

  ✓  1 tests/demo.spec.js:3:5 › Your test name goes here (155ms)

  1 passed (646ms)
```
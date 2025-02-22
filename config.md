# Basic configurations
* File `playwright.config.ts`

## Reporting
* jUnit format report (xml)
* Not open report

```
reporter: [ ['junit', { outputFile: './report/results.xml', open: 'never' }] ],
```

## Test-id attribute and enable recording VDO
```
use: {
    video: 'on',
    testIdAttribute: 'data-testid',
  },
```
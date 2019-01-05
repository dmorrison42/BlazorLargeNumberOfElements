# Blazor test with a large number of elements

## Getting Started

1. Launch with vs code.
2. TADA

If launching with something else navigate to /FetchData

## Problem

After the number of elements in the table reaches around 500,
the following error occurs in the browser (many times per second):

```
blazor.server.js:23 Uncaught TypeError: Cannot read property 'Symbol()' of undefined
    at a (blazor.server.js:23)
    at Object.t.getLogicalChild (blazor.server.js:23)
    at e.applyEdits (blazor.server.js:23)
    at e.updateComponent (blazor.server.js:23)
    at Object.t.renderBatch (blazor.server.js:16)
    at e.<anonymous> (blazor.server.js:38)
    at blazor.server.js:16
    at Array.forEach (<anonymous>)
    at e.invokeClientMethod (blazor.server.js:16)
    at e.processIncomingData (blazor.server.js:16)
```

Reducing the cap on the number of elements to around 300 masks the problem.

# Collection of fonts

This is mostly a collection of fonts that PathScale has a license to. If you don't have a license to a particular font then well, don't use it :P

Some fonts are being released to the public and in those directories you can find a license.

## Getting Started

Each font it's deployed as a different npm package

### Installing a font

    npm i @pathscale/fonts-metroclean

### Import font

Import the front from within js, it can be the entrypoint for your project main.js

```JS
import '@pathscale/fonts-metroclean'
```

### Style something


```CSS
textarea.fancy {
    font-family: 'metroclean';
    font-weight: bold;
}
```

### Caveats

Not every font support all possible weights and styles, you can refer to their specific documentation on their npm website to see what it supports.

## Project structure

Inside `packages/` you will find several subdirectories, one for each font.

This is how each font directory looks like

    .
    ├── files
    │   ├── metroclean-extrabold.ttf
    │   ├── metroclean-extrabold.vfc
    │   ├── metroclean-extrabold.woff2
    │   ├── metroclean-medium.ttf
    │   ├── metroclean-medium.vfc
    │   └── metroclean-medium.woff2
    ├── index.css
    ├── package.json
    └── README.md


`files` holds the raw font files, `package.json` handles npm versioning, `index.css` exports the raw files exposing them to the global css scope, effectively making fonts usable user projects.

Repro showing that Vites default rollup options make code splitting ineffective.

Build output with current options:

```
❯ yarn build
yarn run v1.22.5
warning package.json: No license field
$ vite build
vite v2.3.7 building for production...
✓ 242 modules transformed.
dist/assets/favicon.17e50649.svg          1.49kb
dist/assets/logo.ecc203fb.svg             2.61kb
dist/index.html                           0.45kb
dist/assets/index.0673ce28.css            0.76kb / brotli: 0.40kb
dist/assets/motion-features.553f16b7.js   71.78kb / brotli: 21.78kb
dist/assets/index.369957a6.js             132.48kb / brotli: 37.77kb
Done in 2.95s.
```

Build output with default options (comment out build config in vite.config.js to repro)

```
❯ yarn build
yarn run v1.22.5
warning package.json: No license field
$ vite build
vite v2.3.7 building for production...
✓ 242 modules transformed.
dist/assets/favicon.17e50649.svg          1.49kb
dist/assets/logo.ecc203fb.svg             2.61kb
dist/index.html                           0.51kb
dist/assets/motion-features.08e74a78.js   0.05kb / brotli: 0.05kb
dist/assets/index.0673ce28.css            0.76kb / brotli: 0.40kb
dist/assets/index.ab93243f.js             1.72kb / brotli: 0.69kb
dist/assets/vendor.720da851.js            202.88kb / brotli: 58.27kb
Done in 4.00s.
```

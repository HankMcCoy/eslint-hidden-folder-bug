# ESLint .bin bug

To reproduce the issue, install ESLint globall (`npm install -g eslint`) and then from within this repo run:

`eslint ./`

The `.eslintignore` file is set up to ignore everything inside the `ignoreme` folder but ESLint nevertheless lints the contents of the `ignoreme/.a` subdirectory. As far as I can tell so far this issue arises anytime an ignored folder has a hidden (i.e. prefixed with `.`) subdirectory.

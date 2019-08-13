# orders-manager-frontend
Frontend of app for managing orders in online store

# Launching project for contributing

You'll need to have [NodeJS](https://nodejs.org/en/) installed.
Verify it by running `node --version` in the console.
It should show at least 8th version.
If it reports error, please install node with [this link](https://nodejs.org/en/)

I use [yarn (facebook package manager)](https://yarnpkg.com/en/docs/install)
on this and other projects, please install it for comfortable work.
It's nice alternate to npm, really :)

Verify installation by running `yarn --version` in the console.
It should show 1.13 or higher.

Please read yarn's small [usage guide](https://yarnpkg.com/en/docs/usage).
And [here are complete docs to its CLI](https://yarnpkg.com/en/docs/cli).
The best feature of yarn (to me) is that it allows to run package scripts short way:
`yarn lint` instead of `npm run lint` and so on.

Fork this repository with `fork` button in the bottom top corner

Next clone **your new forked** repository.
**Change your-username to your actual github username in the command:**

`git clone https://github.com/your-username/orders-manager-frontend.git`

Go to project folder: `cd orders-manager-frontend`

Install packages: `yarn install`

Launch app: `yarn start`

Have a look at other available scripts in `package.json`

# Package scripts

- start - launches project at local dev server with hot reloading (it's hot as hell)
- build - makes production build of the project into `build` folder
- test - launches jest test runner
- eject - ejects project from create-react-app. Never run this script
- format - reformat all js,jsx,json,css files according to prettier config
- lint:js - runs eslint on js and jsx files
- lint:css - runs stylelint on css,sass,scss files
- lint - runs lint:js and then lint:css
- deploy - deploys project to github pages. This command runs `build` command before
- storybook - launches storybook
- build-storybook - builds storybook for deployment 

# Code style

I use prettier to format code. Have a look at prettier config file.
You always can run `yarn format` to reformat code according to our guide.
Most times, eslint or stylelint will report any code style violation.

# Commit style

I use [conventionallcommits specification](https://www.conventionalcommits.org/en/v1.0.0-beta.4/).
Except one rule: subject line should not exceed 50 characters.
It's required to make github render subject nicely.

# IDE setup

## WebStorm

EditorConfig is supported out of the box.

To reformat code according to prettier configuration right in WebStorm:
1. Type `Ctrl/cmd + ,` to open settings
2. Open `Languages & Frameworks/JavaScript/Prettier`
3. Make sure that `prettier package` fields points to
locally installed prettier package
4. After that you can run prettier on the current file with `Ctrl/cmd + alt/option + shift + P`

To view and fix eslint errors right in WebStorm
1. Type `Ctrl/cmd + ,` to open settings
2. Open `Languages & Frameworks/JavaScript/Code Quality Tools/ESLint`
3. Make sure that `automatic ESLint configuration` is checked
4. After that all js and jsx files will be automatically checked by eslint

To view and fix stylelint errors right in WebStorm:
1. Type `Ctrl/cmd + ,` to open settings
2. Open `Languages & Frameworks/Style Sheets/Stylelint`
3. Check `Enable` checkbox and make sure that `Stylelint package` field points
to locally installed stylelint package
4. After that all style sheets will be automatically checked by stylelint

Configure commit rules and inspections:
1. Type `Ctrl/cmd + ,` to open settings
2. Open `Version Congtrol/Commit Dialog`
3. Check `Force non-empty commit comments`
4. Under commit message inspections choose `error` severity for everything except `Spelling`.
`Spelling`'s severity should be `Typo`
5. Click on `limit body line` and choose **72** as right margin
6. For `limit subject lint` inspection right margin should be **50**,
according to our commit specification
7. Ensure that `Perform code analysis` checkbox in the `Before commit` section is checked.
It will run eslint or stylelint on changed files before commit

## Visual Studio Code

Install [editoconfig plugin](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
to ensure correct configuration related to editorconfig 

Install [eslint plugin](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
to view and fix eslint errors right in VS Code 

Install [stylelint plugin](https://marketplace.visualstudio.com/items?itemName=shinnn.stylelint)
to view and fix stylelint errors right in VS Code 

To prevent both the editor built-in linters (css,scss) and stylelint from reporting same errors,
disable the built-in ones in User or Workspace setting:
```
"css.validate": false,
"scss.validate": false
```

Install [prettier plugin](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
to reformat code according to prettier config right in VS code.

You may also install [spellchecker plugin](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
to ensure your code doesn't contain typos

Also, [GitLens plugin](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
can simplify work with git

Restart VS Code to ensure, that all extensions are correctly installed

To reformat code with prettier click `F1`->`Format document`.
If you're asked about formatter to use, choose prettier.

Configure commit message rules and inspections:

Type `Ctrl/cmd + ,` to open settings

Search for `git.inputValidationLength`
Ensure the value of this option is **72**

Search for `git.inputValidationSubjectLength`
The value of the first option should be **50**, according to our commit specification

If you have any questions, please don't hesitate to contact [me](https://t.me/DimaDK24)
or open an issue.

If you have any suggestions, how this doc can be improved, feel free to contact [me](https://t.me/DimaDK24)
or open PR or issue.

# Git workflow

We use [forking workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/forking-workflow)

Please read article above, if you're new to working with git in a team.

# solo-quote-UI
Angular app - quotation-plus.
For more information on Angular go to https://angular.io/docs.

## Development Setup

### Prerequisites

- Install any Node version > 18.

### Project Setup

Install the Angular CLI globally:

```
npm install -g @angular/cli@17
```

Clone the frontend project:

```
git clone https://github.com/rohitrana7/solo-quote-UI.git
```

Run the Application:

```
cd solo-quote-UI

npm ci

ng serve
or npx ng serve
or npm start
```

## Directory Structure

    .
    ├── src
    ├── .browserlistrc           # This file is used by the build system to adjust CSS and JS output to support the specified browsers below
    ├── .editorconfig            # Editor configuration, see https://editorconfig.org
    ├── .gitignore               # Contains files to ignore by VCS.
    ├── .prettierrc.json         # Files Containing Prettier rules.See https://prettier.io/
    ├── angular.json             # Provides config for Angular CLI.
    ├── tslint.json              # linting rules for typescript.
    ├── sonar-project.properties #Config for sonarscan(SonarQube)
    └── README.md

## Internal App Directory Structure

    ├── app
    |    ├── core               # Core Module
    |    |    ├── interceptor   # HTTP Interceptor inserting auth token
    |    |    ├── model         # files containing domain models
    |    |    └── services
    |    |
    |    ├── shared             # Shared Module
    |    |    ├── error         # Pages for common error like 404,500 etc.
    |    |    ├── layout        # Folder containing common layouts.
    |    |    └── services
    |    └── [Feature Modules for App]
    |
    ├── environments           # Files containing env specific constants
    └── assets                 # Folder containing assets.

## Before You Start Development

- Install Sonarlint on you text editor or IDE (https://www.sonarlint.org/).
- Prettier is configured in the app.Use [this] guide to install on you IDE.
  - If Possible use **FORMAT ON SAVE** settings on your IDE.

## Common commands

To run Development serve

```
ng serve or npm start
```

To run test cases

```
ng test
```

To run test code coverage

```
ng test --code-coverage
```

If you are getting `ng command not found` add `npx` before the commands

- How to generate karma config
```
ng generate config karma
```

## How to Deploy the app?

- Create branch from the development.

```bash
git checkout -b your_branch_name
```

- After doing changes,commit and push the changes to remote branch.

```bash
git add .
git commit -m "Your commit msg"
git push [Remote_Branch_Name]
```

- Create Pull Request to merge in master branch.
- If the PR checks are passing click the merge button.
- After that if you're using Jenkins, go to [Jenkins][jenkinsurl] -> ci-build-traktis -> master
- Run the Job.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Pre-commit Checks

- the repo uses pre-commit hook to format && fix lint issues for the staged files and run tests.
- To not run the pre-commit hooks use the `--no-verify` option in git commit.

```
git commit --no-verify
```

[this]: https://prettier.io/docs/en/editors.html
[jenkinsurl]: https://ci-jenkins.com

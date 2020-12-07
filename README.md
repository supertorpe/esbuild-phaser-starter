# esbuild Project Starter
This is a skeletal web/js project using esbuild. It includes the following features

1. Bundling the projects JS code into a single `app.js` file, using esbuild budler.
2. Run a server to serve the bundled code.
3. Run unit tests using web-test-runner and chai.
4. Run lint using eslint.

## Project Directory Structure

1. The root of the project conatins these files
    1. `.eslintrc`: ES Lint customized rules 
    2. `.gitignore`: List of files to be ignored by git
    3. `package.json`, `package-lock.json`: NPM package definition.
    4. `README.md`: This file.
    5. `web-test-runner.config.mjs`: web-test-runner configuration using Puppeteer headless.
2. `scripts/` directory: Contains build scripts
3. `src/` directory: Contains the application's source, including js, html, css, images, ...
4. `target/` directory: Will be generated after the first build. Contains build-generated files and directories:
    1. `coverage/` directory: Will be generated after the first test run. Contains test coverage report
    2. `dist/` directory: Contains the distribution files and source map


Note: The code included in `src` is for demo purposes. You can change it or remove it as you see fit.

## Running From The Command Line

Please look at `package.json` scripts section for a quick look at the supported commands.

### Setup
After you clone this repo to your local machine:

```bash
cd esbuild-project-starter
npm install
```

The above will download the `node_modules` dependencies of this project.

### Building

Remove build artifacts
```bash
npm run clean
```

Create bundle
```bash
npm run build
```

### Run a local dev web server
```bash
npm run server
```

### Run Tests
Test files names should follow the pattern `*.test.js`. Look at `src/utils/test` for examples.

Run all tests:
```bash
npm run test
```

Run a test watcher:
```bash
npm run test:watch
```

### Run Linter
```bash
npm run lint
```



## Dependencies
* esbuild: https://esbuild.github.io/
* Web Test Runner: https://modern-web.dev/docs/test-runner/overview/
* Chai: https://www.chaijs.com/api/bdd/
* ESLint: https://eslint.org/docs/rules/
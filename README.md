## Laravel ESlint Prettier Pint and Husky

This is an opinionated starter tha we use for internal projects.
I will write a blog post to go into detail on this setup but for now you can check this demo repo.

The stack is as follows:
- Laravel Breeze
- Inertia with React
- Eslint
- Prettier
- Husky
- Pest

## Included
- Eslint Config ( for React )
- Prettier Config
- Husky ( Git hooks )
- Lint Staged and Pretty Quick - Formats the code before commit.
- Laravel Pint
- Github Workflows for running the formatting again in case anything slipped.

### What about Vue.js
You can easily swap the rules on eslint to work with Vue

## How it works
- Eslint and Prettier are configured to work automatically with the files on `resources/js`
- When you make a commit it will run `npm run format` to make sure every file is formatted correctly and as specified in `.prettierrc` and `eslintrc.js`
- When you open a Pull Request that targets `main` it will automatically run two checks.
- First check is the `npm run format` to make sure nothing slipped locally and every file is formatted correctly.
- Second check is to run the tests with Pest.

## How to test
- Fork this repo and open a new branch
- Make a commit and PR

### Notes
For our internal projects we also have Cypress running on every PR but we might include that later.

This starter was brought to you by the team at [Lucky Media](https://www.luckymedia.dev/)

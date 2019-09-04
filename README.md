ESLint works when run from the command line (both in the root and in the package directory):

```sh
./lintroot.sh
```

```sh
./lintpkg.sh
```

Output:

```
$ eslint "src/**/*.{js,jsx,ts,tsx}"

PATH/vsc-eslint-monorepo-bug/packages/app/src/index.ts
  1:1   warning  Missing return type on function   @typescript-eslint/explicit-function-return-type
  1:10  warning  'test' is defined but never used  @typescript-eslint/no-unused-vars
  1:17  error    Unexpected empty function 'test'  @typescript-eslint/no-empty-function

✖ 3 problems (1 error, 2 warnings)
```

However, when you open the `packages/app/src/index.ts` file in VS Code you will see the following error:

```
Parsing error: File 'PATH/vsc-eslint-monorepo-bug/tsconfig.json' not found. eslint
```

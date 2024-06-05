This is an example to show that Vite isn't set by default for this issue: https://github.com/nrwl/nx/issues/22959

Run:

```shell
npx nx g @nx/react:lib library-name --directory=library-dir --importPath=@benzinga/lib-import-path --compiler=swc --bundler=none --dry-run
```

And see that `vite.config.ts` is not generated.


Now, if you has `--unitTestRunner=vitest` (perhaps it is set as the default in `nx.json`), then you will get a `vite.config.ts` file for the test target.

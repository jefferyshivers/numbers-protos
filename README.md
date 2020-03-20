# Numbers protos

This is an example of a small Protocol Buffer library. You'll just see the one proto file `money.proto` and a `protop.json` manifest.

You can import this project into another project using [`protop`](https://protop.io):

## Local link
If you pull this project locally and run `protop link`, then it will be available to import into another project:
```json
{
  ...
  "dependencies": {
    "awesomelabs/numbers": "0.1.0"
  }
}
```
Run `protop sync --use-links` in the other project to import this dependency.

## From Github
You can simply add the git URL to your manifest to import dependencies from Github, Gitlab, Bitbucket, etc:
```json
{
  ...
  "dependencies": {
    "awesomelabs/numbers": "git:https://github.com/jefferyshivers/numbers-protos"
  }
}
```

Run `protop sync` (or `protop sync --git-refresh` to pull the latest changes if any are made in the source). You can also create a `.protoprc` and add the `git.refresh` property:

```properties
git.refresh=true
```

If you don't use the Git refresh flag, you can continue your work offline since dependencies are cached in a system wide cache until they are cleared or refreshed.

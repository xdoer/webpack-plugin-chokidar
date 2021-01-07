# webpack-plugin-chokidar

## eg

```js
new WebPackPluginChokidar({
  chokidarConfigList: [
    {
      file: '../src/pages/**/index.tsx',
      opt: { persistent: true, ignoreInitial: true },
      actions: {
        on: {
          add: ({ compiler, compilation, watcher }, path) => {
            console.log(`File ${path} has been added`);
          },
        },
      },
    },
  ],
});
```

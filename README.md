# yarn-nm-volume

Demonstrates error installing dependencies into Docker volume using Yarn 3 with
node modules linker. https://github.com/yarnpkg/berry/issues/1184


To reproduce the error:

```
docker compose run script yarn install
```

Output when yarn fails:

```
➤ YN0065: Yarn will periodically gather anonymous telemetry: https://yarnpkg.com/advanced/telemetry
➤ YN0065: Run yarn config set --home enableTelemetry 0 to disable

➤ YN0000: ┌ Resolution step
➤ YN0000: └ Completed
➤ YN0000: ┌ Fetch step
➤ YN0000: └ Completed
➤ YN0000: ┌ Link step
➤ YN0001: │ Error: EBUSY: resource busy or locked, rmdir '/work/node_modules'
➤ YN0000: └ Completed
➤ YN0000: Failed with errors in 0s 98ms
```

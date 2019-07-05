# capture-logs-example
> How to capture console logs and debug module logs

## Show log messages normally

```shell
$ npm start
> node .

this is console log message ✅
this is console warn ⚠️
this is console error 🔥
```

## Capture log messages

```shell
$ npm run log
> node -r ./log .

this is console log message ✅
this is console warn ⚠️
this is console error 🔥
*** printing saved messages ***
log: this is console log message ✅
warn: this is console warn ⚠️
error: this is console error 🔥
```

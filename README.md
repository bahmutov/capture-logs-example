# capture-logs-example
> How to capture console logs and debug module logs

## Show log messages normally

```text
$ npm start
> node .

this is console log message ✅
this is console warn ⚠️
this is console error 🔥
```

## Capture log messages

```text
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

## Debug logs

```text
$ DEBUG=verbose node ./index-debug.js
this is console log message ✅
this is console warn ⚠️
this is console error 🔥
  verbose this is verbose debug = 42 +0ms
```

## Capture debug logs

No `DEBUG=...` yet we capture the debug calls

```text
$ node -r ./log ./index-debug.js
this is console log message ✅
this is console warn ⚠️
this is console error 🔥
*** printing saved messages ***
log: this is console log message ✅
warn: this is console warn ⚠️
error: this is console error 🔥
debug:   verbose this is verbose debug = 42 +0ms
```

With `DEBUG=verbose` we show and capture the debug calls

```text
$ DEBUG=verbose node -r ./log ./index-debug.js
this is console log message ✅
this is console warn ⚠️
this is console error 🔥
  verbose this is verbose debug = 42 +0ms
*** printing saved messages ***
log: this is console log message ✅
warn: this is console warn ⚠️
error: this is console error 🔥
debug:   verbose this is verbose debug = 42 +0ms
```

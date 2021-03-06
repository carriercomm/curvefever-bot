# curvefever-bot
[![npm status](http://img.shields.io/npm/v/curvefever-bot.svg)](https://www.npmjs.org/package/curvefever-bot)
[![build status](https://secure.travis-ci.org/clux/curvefever-bot.svg)](http://travis-ci.org/clux/curvefever-bot)
[![dependency status](https://david-dm.org/clux/curvefever-bot.svg)](https://david-dm.org/clux/curvefever-bot)
[![coverage status](http://img.shields.io/coveralls/clux/curvefever-bot.svg)](https://coveralls.io/r/clux/curvefever-bot)
[![unstable](http://img.shields.io/badge/stability-unstable-E5AE13.svg)](http://nodejs.org/api/documentation.html#documentation_stability_index)

Curvefever-bot is a bot interface for the [curvefever-stats](https://npmjs.org/package/curvefever-stats) package. You can hook this up to [irc-stream](http://npmjs.org/package/irc-stream) (say), and use it to sign up to games on IRC, as well as having it auto-generate fair teams for you, provided you have associated the player IRC nicknames with their curvefever nicknames.

## Usage
The library exposes a [gu](https://npmjs.org/package/gu) instance that you can create by just passing in the missing gu options. Then pipe your transports into it:

```javascript
var curveBot = require('curvefever-bot').gu();
var ircStream = require('irc-stream')(ircServer, ircName, ircOpts);

ircStream.pipe(curveBot).pipe(ircStream);
```

Alternatively, change the config file directly and run `npm start` for IRC mode.

## Commands
On IRC type `curve help` for help.

## TODO
When there are other transport streams available, implement bin files for them.

## License
MIT-Licensed. See LICENSE file for details.

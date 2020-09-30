# twitch-player

# About

*twitch-player* is a Typescript `npm` package that provides an easy interaction with the
Twitch embeddable, interactive VOD and Clips player.

Currently, the Twitch Development team offers only a JS script for embedding an interactive
media player ([see this link](https://dev.twitch.tv/docs/embed/video-and-clips#interactive-frames-for-live-streams-and-vods)).
When developing Web apps using Typescript (for example in Angular) it is pretty cumbersome to work with the provided script, without any types support.

Because of this I've released this package, which has the following features:

* easy setup using `npm install` :heavy_check_mark:
* types support for Typescript :heavy_check_mark:
* tested with Angular :heavy_check_mark:

# Getting started


# How to use

## Creating a new player instance

```
const player = new TwitchPlayer('twitch-player', new TwitchPlayerOptions(
        1280,
        720,
        undefined,
        <video ID here>
      ));
```

* In this example, the first argument of the constructor (`twitch-player`),
represents the identifier of the `div` element where the player will be displayed.

* The second argument holds all the initialization options for the player, 
including the width, height and video that will be played

* For more information please [visit the Twitch Developer Reference](https://dev.twitch.tv/docs/embed/video-and-clips#interactive-frames-for-live-streams-and-vods).


## Interacting with the player

* Skipping 10 seconds forward: `player.seek(player.getCurrentTime() + 10)`
* Pausing: `player.pause()`
* Changing volume: `player.setVolume(0.7)`

## Reacting to player events

```
player.addEventListener(TwitchPlayerEvent.PAUSE, () => {
        console.log('paused');
      });
player.addEventListener(TwitchPlayerEvent.PLAY, () => {
        console.log('started');
      });
```

# Documentation

The documentation for all public classes, members and functions [can be found here](https://frozencure.github.io/twitch-player/).

# License

This project is available under the MIT license. See the LICENSE file for more information.



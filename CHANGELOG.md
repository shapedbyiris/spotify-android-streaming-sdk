Version 1.0.0-beta5
===================

**What's New:**

* We introduced two new playback events: `TRACK_START` and `TRACK_END` which
  replace the `TRACK_CHANGED` event.
  The uri of the track that started or finished playing can be read from
  player state sent with those events. ([Issue #8](https://github.com/spotify/android-sdk/issues/8))
* SDK now handles playback errors with new `PlayerNotificationCallback#onPlaybackError` method 
  which can be used to handle the unavailable tracks errors. ([Issue #37](https://github.com/spotify/android-sdk/issues/37))
* As an experimental feature you can now use disk cache in your app. It will store streamed
  tracks locally on the device and read them from disk when played next time.
  To enable disk cache, initialize Spotify as follows:

  ```
  Spotify spotify = new Spotify("myauthtoken");
  spotify.useCache(true);
  ```

**Bugs fixed:**

* `InitializationObserver#onError` callback is now delivered correctly on the UI thread.

Version 1.0.0-beta4
===================

**What's New:**

* You will now get player state with every player event.
* The player state now contains information about currently playing track
  and its duration. ([Issue #22](https://github.com/spotify/android-sdk/issues/22))
* Instead of keeping a copy of player state from native player inside Player object
  `getPlayerState()` is now asynchronous and requires a callback.
* We removed these methods from the Player object:
  * `isPlaying()`
  * `getPlaybackPosition()`
  * `isShuffling()`
  * `isRepeating()`

  This data can now be retrieved asynchronously with `getPlayerState()` or from
  the player state passed with player events.
* New callback for errors while logging in.
* Player initialization callback is now triggered after user successfully logs in.

**Bugs fixed:**

* SDK does not mix playback with Spotify App. ([Issue #28](https://github.com/spotify/android-sdk/issues/28))

Version 1.0.0-beta3
===================

**What's New:**

* We added the possibility to play a list of tracks (for example, an album's tracks).
Playing the list of tracks also supports playing from a specified index ([Issue #11](https://github.com/spotify/android-sdk/issues/11)).
* Improved API reference manual.

**Bugs Fixed:**

* We fixed clearing the buffer after pausing the playback and context switching now works correctly
 ([Issue #21](https://github.com/spotify/android-sdk/issues/21)).
* No more error when context ends ([Issue #20](https://github.com/spotify/android-sdk/issues/20))


Version 1.0.0-beta2
===================

**What's New:**

* SDK now comes as a single aar library.
* Added method to clear queued tracks.

**Bugs Fixed:**

* getPlaybackPosition returns correct values after seeking position
 ([Issue #7](https://github.com/spotify/android-sdk/issues/7)).

**Known Issues:**

* You can't play albums yet.
* Switching between playback contexts is buggy.


Version 1.0.0-beta1
===================

**What's New:**

* Initial release

**Known Issues:**

* SDK limited to authentication and playback. All other functionality is
  currently provided by the Web API.

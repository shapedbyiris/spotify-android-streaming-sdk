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

# MetaHumanUnreal

At the moment to properly use the NVIDIA Omniverse "audio2face" StreamLivelink feature within the project,
other then setting audio2face, you'll have to:
  1. Run the OMNIVERSE launcher > find the "audio2face" app > proceed to the destination folder > (if on Win) run "audio2face_headless.bat" to launch the app in the headless mode,
  2. Browse to "localhost:8011/docs". For reference: the https://docs.omniverse.nvidia.com/audio2face/latest/user-manual/rest-api.html
  3. Use the "/A2F/USD/Load" API, providing the prepared .usd
  4. Use the "/A2F/Exporter/ActivateStreamLivelink" API, providing the "/World/audio2face/StreamLivelink" argument,
  5. Use the "/A2F/Player/GetInstances" API to get the Player Instances,
  6. Use the "/A2F/Player/GetTracks" API to get the available tracks,
  7. Use the "/A2F/Player/SetTrack" API, providing the Player path and Track name, to set the track,
  8. Launch the UProject,
  9. Launch the "Minimal Default" map,

  IF THE "Minimal Default" MAP IS NOT OPENED, FOLLOW THE GUIDE: https://forums.unrealengine.com/t/failed-to-load-map-umap-appears-to-be-an-asset-file/383833

  TO GET ACQUAINTED WITH THE a2f set up, checkout the https://www.youtube.com/watch?v=6QV3U5PENPM&t=2s video. 
  YOU'LL HAVE TO ADJUST THE FOLLOWING MetaHuman BP using the mentioned steps in the video.
  TO GET TO THE MetaHuman BP:

  10. Use the "/A2F/Player/Play" API,
  11. Eject from the playing scene(F8) > in the Outliner find BP_JohnTP0 > set Live Link according to the https://www.youtube.com/watch?v=6QV3U5PENPM&t=2s video,
  12. Press F8 again to gain back the scene control 

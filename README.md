# Expo ImagePicker Incorrect File Extension Bug

This repository demonstrates a bug in Expo's ImagePicker where the returned URI for videos may have an incorrect file extension. This can lead to errors when attempting to play the video.

## Bug Description
The `ImagePicker` returns a URI suggesting a specific file extension (e.g., '.mp4'). However, the actual file on the device might have a different extension (e.g., '.MOV'), causing video players to fail.

## Reproduction
1.  Use `ImagePicker.launchImageLibraryAsync` to select a video.
2.  Note the file extension in the returned URI.
3.  Attempt to play the video using the URI.
4.  Observe potential errors due to the mismatch.

## Solution
The solution involves inspecting the actual file extension on the device before attempting playback. This ensures compatibility.
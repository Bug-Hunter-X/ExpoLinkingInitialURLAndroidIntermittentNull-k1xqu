# Expo Linking.getInitialURL() returns null on Android intermittently

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` function on Android. The function sometimes returns `null`, even when a deep link was used to open the app. This behavior is inconsistent and makes reliable deep link handling difficult.

## Bug Description

The `Linking.getInitialURL()` function, when called in the `useEffect` hook after the app starts, sporadically returns `null` on Android devices.  This occurs even when the app was explicitly launched from a deep link.  iOS shows no such behavior.

## Reproduction

1. Run the app on an Android device.
2. Launch the app using a deep link (e.g., `myapp://somepath`).
3. Observe the console output.  `getInitialURL()` may return `null`, even though the app was launched via the deep link.

## Solution

A reliable solution is unavailable currently.  Workarounds involve using alternative approaches for handling deep links or using additional techniques to mitigate the issue.

## Additional Notes

This bug's inconsistency makes debugging and fixing it challenging.  Further investigation is needed to fully understand the root cause and find a permanent fix.
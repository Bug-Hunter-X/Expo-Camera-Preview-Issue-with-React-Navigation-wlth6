# Expo Camera Preview Bug with React Navigation

This repository demonstrates a bug where the Expo Camera preview fails to render correctly after navigating away and back to the screen containing the camera using React Navigation. The camera preview might display a blank, frozen, or black screen.  This issue seems to stem from the interaction between React Navigation's component lifecycle management and how Expo's Camera component interacts with native modules.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app using `expo start`.
4. Navigate to the screen with the camera.
5. Navigate to a different screen.
6. Navigate back to the screen with the camera.
7. Observe that the camera preview may not render correctly.

## Potential Solution (see bugSolution.js)

The solution explores several approaches, including using `onCameraReady` to explicitly trigger the Camera, useEffect hooks for cleanup, and component ref to manage the Camera instance more effectively.
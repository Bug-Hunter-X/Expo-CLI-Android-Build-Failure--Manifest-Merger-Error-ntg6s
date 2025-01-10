# Expo CLI Android Build Failure: Manifest Merger Error

This repository demonstrates a bug in the Expo CLI where building an Android APK fails with a generic manifest merger error. The error message lacks detail, making debugging difficult.

The `bug.js` file shows a simplified Expo project structure that reproduces the issue.  `bugSolution.js` offers a potential solution, focusing on merging manifests properly.  Note that the exact fix may vary depending on the specific conflicting entries in your `AndroidManifest.xml`.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `expo prebuild`.
4. Attempt to build an Android APK using `expo build:android`.

The build should fail with a manifest merger error.

## Solution

The solution provided in `bugSolution.js` involves careful examination of your `AndroidManifest.xml` file to identify and resolve conflicting entries. The solution may include:

* Resolving conflicts in the declaration of activities, services, permissions, or other elements.
* Using merge tags (e.g., `<merge/>`) appropriately. 
* Ensuring that the merged manifest is valid and consistent.

This requires careful attention to how different components and libraries interact. Please refer to the Android documentation and the relevant library documentation for guidance.
# Firebase Authentication Unsubscribe Issue
This repository demonstrates a common issue encountered when using Firebase Authentication's `onAuthStateChanged` listener.  Failure to properly unsubscribe from the listener can lead to memory leaks and performance degradation.

## Bug Description
The original code lacked an explicit call to the `unsubscribe()` function to detach the listener. This resulted in the listener remaining active even when it was no longer required, consuming resources.

## Solution
The solution involves adding a call to `unsubscribe()` after the listener is no longer needed. This ensures that the listener is properly detached from the Firebase Authentication service, freeing up resources and preventing memory leaks.
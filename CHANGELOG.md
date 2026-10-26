## 0.0.7

* Migrates to built-in Kotlin (AGP 9); no longer applies the Kotlin Gradle Plugin.
* Updates minimum supported SDK version to Flutter 3.44/Dart 3.12.

## 0.0.6

* Fix: Resolved blank labels on first print by sending complete dummy print job at connection
* Fix: Dummy print job (1x1 white pixel) fully initializes entire print pipeline including image data transfer
* Fix: Added heartbeat command after startPrint() in main print sequence (Niimbot protocol workaround)
* Fix: Added allowPrintClear() call in proper sequence before startPagePrint()
* Fix: Store OutputStream and InputStream as member variables after connection
* Fix: Pass stored streams to NiimbotPrinter instead of letting it access socket getters repeatedly
* Fix: Prevents uninitialized stream instances from being used
* Improvement: Complete print pipeline (commands + image data) initialized before first real print
* Improvement: Corrected print command sequence to match Niimbot protocol specification
* Improvement: Added stream verification and error handling in connect method
* Improvement: Enhanced disconnect method to properly close and clear stored streams
* Breaking: NiimbotPrinter constructor now accepts (Context, OutputStream, InputStream) instead of (Context, BluetoothSocket)

## 0.0.2
* Add labelType to PrintData
* Add image to example desing image of canvas

## 0.0.1

* Upload all files

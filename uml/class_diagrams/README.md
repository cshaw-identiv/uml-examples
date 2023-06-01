This file provides an interface definition for a Fingerprint Reader driver.

```mermaid
classDiagram
direction LR
class FingerprintReader
<<interface>> FingerprintReader
FingerprintReader : registerListener(FingerprintListener&)
FingerprintReader : configure()
FingerprintReader : setPower(bool)
FingerprintReader : readFingerprintImage()

class FingerprintListener
<<interface>> FingerprintListener
FingerprintListener : notifyOfEvent()
FingerprintListener : receiveFingerprint()

FingerprintReader "1" --> "0..*" FingerprintListener
```
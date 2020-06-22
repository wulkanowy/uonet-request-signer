# PKCS12 data signing and key management in Swift 5.

## Setup
1. Add bridging header.
2. Add `#import <CommonCrypto/CommonCrypto.h>` in the bridging header.

## Usage
```swift
function sign(data: NSData) -> String? {
	let password = "<CertPassword>"
	let certificate: String = "<CertB64>"
	let decodedCert: Data = Data(base64Encoded: certificate)

	do {
		let cert = try PKCS12(certificate: decodedCert, password: password)
		return cert.signData(data: data)
	} catch {
		// Error
		return nil
	}
}
```

## License
[GPL v3.0](https://www.gnu.org/licenses/gpl-3.0.txt)

# https://theswiftdev.com/how-to-create-a-swift-package-collection/

package-collection-generate package.json collection.json

openssl pkcs12 -nocerts -in Certificates.p12 -out key.pem && openssl rsa -in key.pem -out rsa_key.pem

package-collection-sign output.json collection.json rsa_key.pem swift_package.cer

swift package-collection list
swift package-collection add --trust-unsigned https://raw.githubusercontent.com/erickyim/spm-collection/refs/heads/main/collection.json
swift package-collection refresh
swift package-collection search --keywords html

swift package-collection remove https://raw.githubusercontent.com/erickyim/spm-collection/refs/heads/main/collection.json
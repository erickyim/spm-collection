package-collection-generate package.json collection.json


openssl pkcs12 -nocerts -in Certificates.p12 -out key.pem && openssl rsa -in key.pem -out rsa_key.pem
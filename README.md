### Mock APNs Server

Mock APNs / testing server supporting ssl connections.

## Setup
Before you run the mock server you need to create a ssl certificate
```bash
openssl req -new -x509 -keyout private -out private -nodes
```

Converse it to DER format
```bash
openssl x509 -in private -out cert.crt -outform DER
```

Make apnsmock runnable by doing:
```bash
chmod a+x apnsmock
```

## Usage
Be sure you have the required dependencies:
```
pip install gevent
```
Then start up the server passing a valid ssl certificate's absolute path:
```
./apnsmock --cert "/absolute/path/to/private"
```


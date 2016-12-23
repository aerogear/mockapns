### Mock APNs Server

Mock APNs / testing server supporting ssl connections.

## Setup
Before you run the mock server you need to create a ssl certificate
```bash
openssl req -new -x509 -keyout key -out cert -nodes
```

Make apnsmock runnable by doing:
```bash
chmod a+x apnsmock
```

## Usage
Be sure you have the required dependencies:
```bash
pip install gevent
```
Then start up the server passing a valid ssl certificate's absolute path:
```bash
./apnsmock --cert "/absolute/path/to/certificate" --key "/absolute/path/to/private_key"
```
> Warning: please mind that mock-apns will start up even if the paths are wrong.

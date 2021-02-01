- Making signed apk - https://medium.com/@hasangi/making-a-signed-apk-for-your-react-native-application-98e8529678db

# Generate Keystore

```
keytool -genkey -v -keystore velotio.keystore -alias velotio-key-alias -keyalg RSA -keysize 2048 -validity 10000
```

Keep your generated file secret and password secret. Do not push them to version control

Generate base64 string from the generated file:

```
openssl base64 -in velotio.keystore -out velotio.keystore.base64
```
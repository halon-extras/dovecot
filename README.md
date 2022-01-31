# Dovecot user authentication

## dovecot_auth(options, username, password)
Try to authenticate the username against a dovecot server.

**Params**

- options `array` - options array
- username `string` - username
- password `string` - password

**Returns**: 1 if the authentication succeeded, 0 if the authentication failed and -1 if an error occurred.

The following options are available in the **options** array.

- address `string` - Address of the dovecot server. The default is `127.0.0.1`.
- port `number` - TCP port of the dovecot server. The default is `12345`.
- path `string` - Path to a the dovecot unix socket. Mutually exclusive with `address`.
- timeout `number` - Timeout in seconds. The default is 5 seconds.

There are also some protocol specific flags that may be configured.

- service `string` - Service name to identify this request. The default is smtp.
- rip `string` - The IP-address of the client (remote IP).
- lip `string` - The IP-address of the Halon (local IP).
- secured `boolean` - Set to true if the client has tlsstarted. The default is false

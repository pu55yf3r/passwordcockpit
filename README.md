# password-cockpit

## Environment variables for configuring your passwordcockpit instance
- PASSWORDCOCKPIT_DATABASE_USERNAME: Username for the database
- PASSWORDCOCKPIT_DATABASE_PASSWORD: Password for the database
- PASSWORDCOCKPIT_DATABASE_HOSTNAME: Hostname of the database server
- PASSWORDCOCKPIT_DATABASE_DATABASE: Name of the database
- PASSWORDCOCKPIT_BLOCK_CIPHER_KEY: Key for passwords and files encrypting, e.g. `Q7EeZaHdMV7PMBGrNRre27MFXLEKqMAS`
- PASSWORDCOCKPIT_AUTHENTICATION_SECRET_KEY: Key for JWT, e.g. `zfYKN7Z8XW8McgKaSD2uSNmQQ9dPmgTz`
- PASSWORDCOCKPIT_BASEHOST: Base host of the passwordcockpit service, e.g. `https://passwordcockpit.domain.com`
- PASSWORDCOCKPIT_SWAGGER: Enable swagger documentation, possible value: `enable` or `disable`. URL: PASSWORDCOCKPIT_BASEHOST/swagger
- PASSWORDCOCKPIT_SSL: Enable SSL, possible value: `enable` or `disable`. If enabled use port 443 if not, the port 80, the two ports cannot be opened at the same time. If enabled, the system generate a self-signed certificate
- PASSWORDCOCKPIT_SSL_CERTIFICATE_FILE: Path of the SSL certificate file for HTTPS, this will overwrite the self-signed auto generated file
- PASSWORDCOCKPIT_SSL_CERTIFICATE_KEY_FILE: Path of the SSL certificate key file for HTTPS, this will overwrite the self-signed auto generated file
- PASSWORDCOCKPIT_AUTHENTICATION_TYPE: Type of the authentication, possible value: `ldap` or `password`
	- Only for LDAP type:
		- PASSWORDCOCKPIT_LDAP_HOST: Hostname of the LDAP server
		- PASSWORDCOCKPIT_LDAP_PORT: Port of the LDAP server
		- PASSWORDCOCKPIT_LDAP_USERNAME: Username for LDAP, e.g. `uid=name,cn=users,dc=domain,dc=com`
		- PASSWORDCOCKPIT_LDAP_PASSWORD: Password for LDAP
		- PASSWORDCOCKPIT_LDAP_BASEDN: Base DN, e.g. `cn=users,dc=domain,dc=com`
		- PASSWORDCOCKPIT_LDAP_ACCOUNTFILTERFORMAT: Filter for retrieving accounts, e.g. `(&(memberOf=cn=group_name,cn=groups,dc=domain,dc=com)(uid=%s))`
		- PASSWORDCOCKPIT_LDAP_BINDREQUIRESDN: Bind requires DN, possible value: `true` or `false`
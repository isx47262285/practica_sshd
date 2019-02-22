# practica_sshd

## roberto@edt asix m06 curs 2018-2019

# SERVIDOR SSHD

escucha por el  puerto  **1022**

### descripcion:

un servidor que nos permite hacer conexiones remotas de usuarios locales unix o usuarios de ldap y nos crea nuestro home de manera segura mediante el sshd

## red de las partes implicadas

```
docker network create ldapnet
```

## ejecucion 

```
docker run --rm --name ldap -h ldap --network ldapnet -d robert72004/ldapserver_18roberto

docker run --rm --name sshd -h sshd --network ldapnet -it robert72004/sshd:server
```

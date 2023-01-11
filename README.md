# sampleldap
sample ldap server 

## some queries

Use them inside the ldap POD directly

ldap://ldap-service.ldap.svc.cluster.local:1389

ldapsearch -x -H ldap://ldap-service.ldap.svc.cluster.local:1389 -D "cn=admin,dc=example,dc=org" -W "objectclass=account"

ldapmodify -a -x -D "cn=admin,dc=example,dc=org" -w password -H ldap://ldap-service.ldap.svc.cluster.local:1389 -f newgroups.ldif

ldapsearch -x -H ldap://ldap-service.ldap.svc.cluster.local:1389 -b "dc=example,dc=org" 

ldapsearch -x -H ldap://ldap-service.ldap.svc.cluster.local:1389 -b "cn=user01,ou=users,dc=example,dc=org" -D "cn=admin,dc=example,dc=org" -w password

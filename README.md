# sampleldap
sample ldap server 

## some queries

ldap://ldap-service.ldap.svc.cluster.local:1389

ldapsearch -x -H ldap://ldap-service.ldap.svc.cluster.local:1389 -D "cn=admin,dc=example,dc=org" -W "objectclass=account"

ldapmodify -a -x -D "cn=admin,dc=example,dc=org" -w password -H ldap://ldap-service.ldap.svc.cluster.local:1389 -f newgroups.ldif

ldapsearch -x -H ldap://ldap-service.ldap.svc.cluster.local:1389 -b "dc=example,dc=org" 

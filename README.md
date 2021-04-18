# django-auth-ldap-ad-primarygroup

Overhaul of django-auth-ldap in https://github.com/django-auth-ldap

Django authentication backend that authenticates against an LDAP service from an Active Directory server. Including the primary group of users. 

** Replace the file https://github.com/django-auth-ldap/django-auth-ldap/blob/master/django_auth_ldap/config.py

** Modifications flagged with "####!!!!"


**It is necessary to add these parameters in the following configuration in settings.py

AUTH_LDAP_GROUP_TYPE = NestedActiveDirectoryGroupType()

AUTH_LDAP_GROUP_SEARCH = LDAPSearch(
    "OU=group1,DC=host,DC=com",
    ldap.SCOPE_SUBTREE,
   "(objectClass=group)", )

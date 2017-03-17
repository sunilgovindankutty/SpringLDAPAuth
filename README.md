# SpringLDAPAuth

This class helps with AD authentication issues after the UPN updates to support the Office 365 project.
It uses the sAMAccountName instead of UPN to do the user search.

Save the class to a security.ldap package in your project and update the Spring security config file to use the new class.
Change
```
<beans:bean id="adAuthenticationProvider" class="org.springframework.security.ldap.authentication.ad.ActiveDirectoryLdapAuthenticationProvider">
```
To
```
<beans:bean id="adAuthenticationProvider" class="security.ldap.MyLdapAuthenticationProvider">
```
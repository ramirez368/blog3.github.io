---
layout: default
---


[Ldap and Active Directory how they interact](https://www.youtube.com/watch?v=QyhNaY5O468&t=1s).

[//]: #  There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# What is LDAP?
LDAP (Lightweight Directory Access Protocol) is an open and cross platform protocol used for directory services authentication.

LDAP provides the communication language that applications use to communicate with other directory services servers. Directory services store the users, passwords, and computer accounts, and share that information with other entities on the network.



## LDAP Authentication:
![Ldap Authentication](https://api.softwarekeep.com/media/nimbus/helpcenter/LDAP_Authentification.png)

* _Anonymous authentication_: Grants client anonymous status to LDAP.
* _Unauthenticated authentication_: For logging purposes only, should not grant access to a client.
* _Name/Password authentication_: Grants access to the server based on the credentials supplied – simple user/pass authentication is not secure and is not suitable for authentication without confidentiality protection.

SASL authentication binds the LDAP server to another authentication mechanism, like Kerberos. The LDAP server uses the LDAP protocol to send an LDAP message to the other authorization service. That initiates a series of challenge response messages that result in either a successful authentication or a failure to authenticate.

It’s important to note that LDAP passes all of those messages in clear text by default, so anyone with a network sniffer can read the packets. You need to add TLS encryption or similar to keep your usernames and passwords safe.

### What is Active Directory?
Active Directory is a directory services implementation that provides all sorts of functionality like authentication, group and user management, policy administration and more.

Active Directory (AD) supports both Kerberos and LDAP – Microsoft AD is by far the most common directory services system in use today. AD provides Single-SignOn (SSO) and works well in the office and over VPN. AD and Kerberos are not cross platform, which is one of the reasons companies are implementing access management software to manage logins from many different devices and platforms in a single place. AD does support LDAP, which means it can still be part of your overall access management scheme.

Active Directory is just one example of a directory service that supports LDAP. There are other flavors, too: Red Hat Directory Service, OpenLDAP, Apache Directory Server, and more.



### LDAP vs. Active Directory
LDAP is a way of speaking to Active Directory.

LDAP is a protocol that many different directory services and access management solutions can understand.

The relationship between AD and LDAP is much like the relationship between Apache and HTTP:

* HTTP is a web protocol.
* Apache is a web server that uses the HTTP protocol.
* LDAP is a directory services protocol.
* Active Directory is a directory server that uses the LDAP protocol.
Occasionally you’ll hear someone say, “We don’t have Active Directory, but we have LDAP.” What they probably mean is that they have another product, such as OpenLDAP, which is an LDAP server.
It’s kind of like someone saying “We have HTTP” when they really meant “We have an Apache web server.”



![Table with Differences between LDAP and Active Directory ](https://ipwithease.com/wp-content/uploads/2020/06/LDAP-VS-AD-TABLE.jpg)

### What is an LDAP Query?
An LDAP query is a command that asks a directory service for some information. For instance, if you’d like to see which groups a particular user is a part of, you’d submit a query that looks like this:

(&(objectClass=user)(sAMAccountName=yourUserName)
(memberof=CN=YourGroup,OU=Users,DC=YourDomain,DC=com))

Beautiful syntax, huh? Not quite as simple as typing a web address into your browser. Feels like LISP.

Luckily, in most cases, you won’t need to write LDAP queries. To maintain your sanity, you’ll perform all your directory services tasks through a point-and-click management interface like Varonis DatAdvantage or perhaps using a command line shell like PowerShell that abstracts away the details of the raw LDAP protocol.

TL;DR: LDAP is a protocol, and Active Directory is a server. LDAP authenticates Active Directory – it’s a set of guidelines to send and receive information (like usernames and passwords) to Active Directory. Want to learn more? Get a 1:1 AD demo and learn how Varonis helps protect your Active Directory environment.


### I hope this was useful to how to setup Apache Server and being expose to more Linux


```
Thank you readers, and wait for next week blog
For Contact e-mail me at ramirez368@hotmail.com

```

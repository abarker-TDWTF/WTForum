Users and Authentication
===
v0.0

This document specifies the design for user authentication and carrying user objects within the software.

*This document is subject to change as features are added.*

===

###Basic Requirements

#####Authentication
- User accounts require unique, valid email addresses. No third part authentication is available.
- Passwords must not be stored in plaintext. Passwords should be stored in a salted, hashed format which does not allow recovery of the original password.
  - Current plan to cover this point: [BCrypt](http://bcrypt.codeplex.com/).
- Usernames must be unique.
- Authentication can be accompliched using the username or email.

####User Object
When transported within the software, the user object shall contain the following properties:

- User name - for easy display purposes
- Database user ID - for ease in calling database functions

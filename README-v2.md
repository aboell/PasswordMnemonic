# Password Mnemonic Generator

## Prologue

Name: Andy Boell

Date - 10/2/16

Module 6 - password.html & passwordconfig.html

## Purpose

Expanding on last module's work, Password Mnemonic Generator is now a fully customizable and  simple tool that tech trainers can use with end users to assist the end user in developing a strong password.

## Usage

For testing and reference, the first version is available [https://rawgit.com/aboell/PasswordMnemonic/master/password-original.html](https://rawgit.com/aboell/PasswordMnemonic/master/password-original.html)
The new versions are located at [https://rawgit.com/aboell/PasswordMnemonic/master/passwordconfig.html](https://rawgit.com/aboell/PasswordMnemonic/master/passwordconfig.html) and [https://rawgit.com/aboell/PasswordMnemonic/master/password.html](https://rawgit.com/aboell/PasswordMnemonic/master/password.html)
Provide a phrase that will be used to generate a password.  The password is then modified to add symbolic and number substitutions then a password strength is reported.

## Algorithm

The algorithm is still very simple; extract the first letter from the phrase to create a password.  Then modify the password with character substitutions to show the user variations and how it impacts the strength of the password.

## Strength Scale
With the first version, the user was stuck with the default password strength scale.  In version 2, a trainer or sysadmin can customize the password requirements using the passwordconfig.html file, then provide the genereated URL to the end user for application.
In the event a user visits password.html without first configuring all the parameters, the page loads the defaults.
**Default Password Strength Scale**

Length
* Weak < 8
* OK 8 or 9
* Strong 10 or 11
* Very Strong > 11

Character Classifications
* List of Character Classifications
	* Lower Case - a, b, c, etc.
	* Upper Case - A, B, C, etc.
	* Numbers - 1, 2, 3, etc.
	* Special Characters - ~ ` ! # $ % \ ^ & * + = - [ ] ' ; , / { } | " : < > ?
* Weak - 1 character classification
* OK - 2 character classifications
* Strong - 3 character classifications
* Very Strong - 4 character classifications

![Password Strength Matrix](/PasswordStrengthMatrix.JPG)


## Usage Example

### Input phrase
`This password is better than your last password by a long shot`

### Output generated
Suggested Password|Password Strength|Length|
---|---|---
`Tpibtylpbals`|**OK**|12
`Tpibty1pba1s`|**Strong**|12
`Tp!btylpb@l$`|**Strong**|12
`Tp!bty1pb@1$`|**Very Strong**|12

## Other

The default password strength scale is not based upon any recommended scale.  Rather it is currently designed as a proof of concept.

The character substitutions are arbitrarily selected on substitutions I have previously used in passwords. 

This page was created as an all-inclusive page with no calls outside itself.  This is keep the code review simple and provide a "piece of mind" that the passwords entered are not extracted and collected.

## Future Work

Try to roll this into a browser plugin in some way, as previously suggested by some classmates.

Add functionality that uses a resource like OSWAP PassFault [https://www.owasp.org/index.php/OWASP_Passfault](https://www.owasp.org/index.php/OWASP_Passfault) to provide additional feedback on how long it would take to brute-force the provided passwords.
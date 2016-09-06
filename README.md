# Password Mnemonic Generator

## Prologue

Name: Andy Boell
Date - 9/10/16
Module 3 - Password.html

## Purpose

Password Mnemonic Generator is a simple tool that tech trainers can use with end users to assist the end user in developing a strong password.

## Usage

For testing, you may use [https://rawgit.com/aboell/PasswordMnemonic/master/Password.html](https://rawgit.com/aboell/PasswordMnemonic/master/Password.html)
Provide a phrase that will be used to generate a password.  The password is then modified to add symbolic and number substitutions then a password strength is reported.

## Algorithm

The algorithm is very simple; extract the first letter from the phrase to create a password.  Then modify the password with character substitutions to show the user variations and how it impacts the strength of the password.

## Usage Example

### Input phrase
	"`This password is better than your last password by a long shot`"

### Output generated
	|Suggested Password|Password Strength|Length|
	|---|---|---|
	|Tpibtylpbals|**OK**|12|
	|Tpibty1pba1s|**Strong**|12|
	|Tp!btylpb@l$|**Strong**|12|
	|Tp!bty1pb@1$|**Very Strong**|12|

## Other

The default password strength scale is not based upon any recommended scale.  Rather it is currently designed as a proof of concept.

The character substitutions are arbitrarily selected on substitutions I have previously used in passwords. 

This page was created as an all-inclusive page with no calls outside itself.  This is keep the code review simple and provide a "piece of mind" that the passwords entered are not extracted and collected.

## Future Work

Add a second html page that organizational admins can use to customize the complexity requirements and generate a custom URL to send to end users that not only brands the page for their organizational use but to use their complexity requirements and strength classifications.

Add functionality that uses a resource like OSWAP PassFault [https://www.owasp.org/index.php/OWASP_Passfault](https://www.owasp.org/index.php/OWASP_Passfault) to provide additional feedback on how long it would take to brute-force the provided passwords.
# Email regex check

## Sample emails
simple@example.com,


very.common@example.com,


disposable.style.email.with+symbol@example.com,


other.email-with-hyphen@example.com,


fully-qualified-domain@example.com,


user.name+tag+sorting@example.com,


x@example.com,


example-indeed@strange-example.com,


test/test@test.com,


admin@mailserver1,


example@s.example,


" "@example.org,


"john..doe"@example.org,


mailhost!username@example.org,


"very.(),:;<>[]\".VERY.\"very@\\ \"very\".unusual"@strange.example.com,


user%example.com@example.org,


user-@example.org,


postmaster@[123.123.123.123],


postmaster@[IPv6:2001:0db8:85a3:0000:0000:8a2e:0370:7334],


--------NOTHING BELOW THIS LINE SHOULD BE FULLY GREEN-----------------------,


Abc.example.com,


A@b@c@example.com,


a"b(c)d,e:f;g<h>i[j\k]l@example.com,


just"not"right@example.com,


this is"not\allowed@example.com,


this\ still\"not\\allowed@example.com,


1234567890123456789012345678901234567890123456789012345678901234+x@example.com,


i_like_underscore@but_its_not_allowed_in_this_part.example.com,


QA[icon]CHOCOLATE[icon]@test.com

## Regex implementations

^[\w\d\.-]+@\[?[\w\d\.\-\]:?+\.[\w]+


^([\w\./+-]{1,64})@\[?([\w\d\./+-:]+)\]?


^([\w\.+-/]{1,64})@\[?([a-zA-Z\d/+-:]+)\]?


^([a-zA-Z0-9\.+-/!%]{1,64})@\[?([a-zA-Z\d/+-:]+)\]?


^([a-zA-Z0-9\.+-/!%_]){1,64}@\[?([a-zA-Z\d/+-:]+)\]?


^([a-zA-Z0-9\.+-/!%_" ](?!"\w)){1,64}@\[?([a-zA-Z\d/+-:]+)\]?


^([\w\d\.+-/!%_" (),:;<>](?!"\w)){1,64}@\[?([a-zA-Z\d/+-:]+)\]?.$


^([\w\d\.+\-/!%_" æøåÆØÅ](?!"\w)(?!\[)){1,64}@\[?([a-zA-Z\d/+-:]+)\]?.$

## Final regex checks

Strict and safe: ^([\w\d\.+\-/!%_" æøåÆØÅ](?!"\w)(?!\[)){1,64}@\[?([a-zA-Z\d/+-:]+)\]?.$


Not strict: ([\w\d\.+\-/!%_" æøåÆØÅ](?!"\w)(?!\[)){1,64}@\[?([a-zA-Z\d/+-:]+)\]?.

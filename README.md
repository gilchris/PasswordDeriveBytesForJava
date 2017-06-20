# PasswordDeriveBytesForJava
a Java port of C# PasswordDeriveBytes class

MS original PasswordDeriveBytes class contains a nonstandard extension of the PBKDF1 algorithm. So MS PasswordDeriveBytes is different of normal BKDF1.

This class has made imitating MS original PasswordDeriveBytes.

Still, it works for SHA-1, which is default for PasswordDeriveBytes.

## Behavior of C# PasswordDeriveBytes GetBytes with SHA1

Below result is I tested C# PasswordDeriveBytes GetBytes function with SHA1 byte by byte.
'A' is return value length of first call of GetBytes function.

| Argument of first call of GetBytes function | Return value of second call of GetBytes function |
| --- | --- |
| 1 ~  9 | Runtime Error |
| 10 ~ 19 | Skip (20 - A) bytes and read (20 - A) bytes in key stream + normal second result |
| 21 ~ 39 | Skip (40 - A) bytes and read (40 - A) bytes in key stream + normal second result |
| 40 ~ | normal second result |

# PasswordDeriveBytes For PHP by Gabriel Castillo

http://www.tyrodeveloper.com/2017/05/passwordderivebytes-en-php.html

Thank you for porting!
# PasswordDeriveBytesForJava
a Java port of C# PasswordDeriveBytes class

MS original PasswordDeriveBytes class contains a nonstandard extension of the PBKDF1 algorithm. So MS PasswordDeriveBytes is different of normal BKDF1.

This class has made imitating MS original PasswordDeriveBytes.

Still, it works for SHA-1, which is default for PasswordDeriveBytes.
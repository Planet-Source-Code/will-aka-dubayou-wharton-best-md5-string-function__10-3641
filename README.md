<div align="center">

## Best MD5 String Function


</div>

### Description

This is a pretty nice and clean MD5 sum for strings. Just Copy and Paste it in. Sorry if it gets bucherd by PSC
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Will \(aka DUBAYOU \) Wharton](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/will-aka-dubayou-wharton.md)
**Level**          |Intermediate
**User Rating**    |3.4 (17 globes from 5 users)
**Compatibility**  |C\#
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__10-14.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/will-aka-dubayou-wharton-best-md5-string-function__10-3641/archive/master.zip)





### Source Code

```
using System.Security.Cryptography;
    static string MD5Str(string raw)
    {
      MD5 md5serv = MD5CryptoServiceProvider.Create();
      byte[] hash;
      StringBuilder stringbuff = new StringBuilder();
      ASCIIEncoding asciienc = new ASCIIEncoding();
      byte[] buffer = asciienc.GetBytes(raw);
      hash = md5serv.ComputeHash(buffer);
      foreach (byte b in hash)
      {
        stringbuff.Append(b.ToString("x2"));
      }
      return stringbuff.ToString();
    }
```


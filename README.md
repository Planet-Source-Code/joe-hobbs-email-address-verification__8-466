<div align="center">

## Email Address Verification


</div>

### Description

This function verifies that an email address is indeed valid.

This function goes a step further than most other functions I have found online. It allows multi-level domains like subdomain.domain.com.

This function does NOT check for .com .org etc, because you never know what domains will be out there. And even checking for 3 or so characters will die on .tv and .info domains.
 
### More Info
 
$sEmailAddress = String containing the email address to check

Returns TRUE if the email address is valid


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Joe Hobbs](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/joe-hobbs.md)
**Level**          |Intermediate
**User Rating**    |4.6 (23 globes from 5 users)
**Compatibility**  |PHP 3\.0, PHP 4\.0
**Category**       |[Validation/ Processing](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/validation-processing__8-16.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/joe-hobbs-email-address-verification__8-466/archive/master.zip)





### Source Code

```
// Check to make sure email address is valid
function funcCheckEmail($sEmailAddress)
{
 // Regex of valid characters
 $sChars = "^[A-Za-z0-9\._-]+@([A-Za-z][A-Za-z0-9-]{1,62})(\.[A-Za-z][A-Za-z0-9-]{1,62})+$";
 // Check to make sure it is valid
 $bIsValid = true;
 if(!ereg("$sChars",$sEmailAddress))
 {
  $bIsValid = false;
 }
 return $bIsValid;
}
```


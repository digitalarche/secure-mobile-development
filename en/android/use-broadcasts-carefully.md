# Use Broadcasts Carefully

## Details

If no permission is set when sending a broadcast Intent, then any unprivileged app can receive the Intent unless it has an explicit destination.

An attacker could take advantage of an Intent that doesn't have any set permissions in the following way:
- Create a malicious app that includes a component with the same name as a legitimate component
- As long as that name (or namespace) is not already in use, the malicious app will install on the target device
- Extract sensitive data from the broadcast Intent sent to that component name"?

## Remediation

Use permissions to protect Intents in your application. Keep in mind that when sending information via a broadcast Intent to a third party component, that component could have been replaced by a malicious install.

## References

 * [https://developer.android.com/training/articles/security-tips.html#Permissions](https://developer.android.com/training/articles/security-tips.html#Permissions)
 * [http://shop.oreilly.com/product/0636920022596.do](http://shop.oreilly.com/product/0636920022596.do)

## CWE/OWASP

 * [M1 - Improper Platform Usage](https://www.owasp.org/index.php/Mobile_Top_10_2016-M1-Improper_Platform_Usage), [M7 - Client Code Quality](https://www.owasp.org/index.php/Mobile_Top_10_2016-M7-Poor_Code_Quality)
 * [CWE-925: Improper Verification of Intent by Broadcast Receiver](http://cwe.mitre.org/data/definitions/925.html)

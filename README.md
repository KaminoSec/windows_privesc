# Windows Privilege Escalation Exploits

[Service Escalation Registry (regsvc)](https://github.com/KaminoSec/windows_privesc/tree/main/service_escalation_registry) : Using Get-Acl we determine that the NT AUTHORITY\INTERACTIVE has full control over the regsvc registry. We can then add a malicious executable to the registry service and leverage this exploit to either get a reverse shell or add a user.

[SeImpersonate Potato Attack](https://github.com/KaminoSec/windows_privesc/tree/main/impersonation_potato_attack): Legitimate programs may utilize another process's token to escalate from Administrator to Local System, which has additional privileges. Processes generally do this by making a call to the `WinLogon` process to get a `SYSTEM` token, then executing itself with that token placing it within the SYSTEM space. Attackers often abuse this privilege in the "Potato style" privesc, where a service account can `SeImpersonate`, but not obtain full SYSTEM level privileges.

[Autorun Logon Registry](https://github.com/KaminoSec/windows_privesc/tree/main/impersonation_potato_attack): Running Autoruns.exe from [Sysinternals](https://learn.microsoft.com/en-us/sysinternals/downloads/autorun) we can view which programs that run from the autorun registry keys or folders. This tool also provides insight into Scheduled Tasks, Services, WinLogon, DLLS, and more.

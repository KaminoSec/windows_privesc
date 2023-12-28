# Windows Privilege Escalation Exploits

[Service Escalation Registry](https://github.com/KaminoSec/windows_privesc/tree/main/service_escalation_registry)

[SeImpersonate Potato Attack](https://github.com/KaminoSec/windows_privesc/tree/main/impoersonation_potato_attack): Legitimate programs may utilize another process's token to escalate from Administrator to Local System, which has additional privileges. Processes generally do this by making a call to the `WinLogon` process to get a `SYSTEM` token, then executing itself with that token placing it within the SYSTEM space. Attackers often abuse this privilege in the "Potato style" privesc, where a service account can `SeImpersonate`, but not obtain full SYSTEM level privileges.

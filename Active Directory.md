# Active Directory

# 53/DNS
- [ ] DNS Zone Transfer

# 139,445/SMB,Samba
- [ ] Null Session

# 389/LDAP
- [ ] LDAP Anonymous Bind


# Privilege Escallation

## `whoami /priv` permissions
- [ ] SeImpersonateToken
- [ ] SeManageVolumePrivilege ([Reference](https://github.com/CsEnox/SeManageVolumeExploit/releases/tag/public?source=post_page-----b95d3146cfe9--------------------------------)): The general idea is that the attacker can leverage this particular privilege with the exploitation to get full control over "`C:\`", and then it can craft a "`.dll`" file and place it in somewhere "`C:\Windows\System32\`" to trigger the payload as root. We will use `systeminfo`’s `tzres.dll` but you should be able to use any `.dll`. Create another reverse shell outputting the file as `tzres.dll` and transfer it to the victim; placing it in the `c:\windows\system32\wbem` directory. Execute `systeminfo`.
- [ ] SeMachineAccountPrivilege
- [ ] 

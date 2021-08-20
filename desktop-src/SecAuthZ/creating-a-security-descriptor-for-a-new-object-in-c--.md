---
description: Im folgenden Beispiel wird mithilfe des folgenden Prozesses eine Sicherheitsbeschreibung für einen neuen Registrierungsschlüssel erstellt. Ähnlicher Code kann verwendet werden, um einen Sicherheitsdeskriptor für andere Objekttypen zu erstellen.
ms.assetid: 866992a7-95c4-4094-87bb-e6d8eeb24317
title: Erstellen eines Sicherheitsdeskriptors für ein neues Objekt in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb97acf8a2c7c35d42c54a10baeabaa193f880d11a505ac459e6c705be28dd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782634"
---
# <a name="creating-a-security-descriptor-for-a-new-object-in-c"></a>Erstellen eines Sicherheitsdeskriptors für ein neues Objekt in C++

Im folgenden Beispiel wird [*mithilfe des folgenden*](/windows/desktop/SecGloss/s-gly) Prozesses eine Sicherheitsbeschreibung für einen neuen Registrierungsschlüssel erstellt. Ähnlicher Code kann verwendet werden, um einen Sicherheitsdeskriptor für andere Objekttypen zu erstellen.

-   Im Beispiel wird ein Array von [**EXPLICIT \_ ACCESS-Strukturen**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) mit den Informationen für zwei ACEs auffüllt. Ein ACE ermöglicht allen Benutzern Lesezugriff. der andere ACE ermöglicht den Vollzugriff für Administratoren.
-   Das [**EXPLICIT \_ ACCESS-Array**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) wird an die [**SetEntriesInAcl-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) übergeben, um eine DACL für den Sicherheitsdeskriptor zu erstellen.
-   Nach dem Zuweisen von Arbeitsspeicher für den Sicherheitsdeskriptor ruft das Beispiel die [**Funktionen InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) und [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) auf, um den Sicherheitsdeskriptor zu initialisieren und die DACL anfügen.
-   Der Sicherheitsdeskriptor wird dann in einer SECURITY ATTRIBUTES-Struktur gespeichert und an die \_ [**RegCreateKeyEx-Funktion**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa) übergeben, die den Sicherheitsdeskriptor an den neu erstellten Schlüssel anfügen kann.


```C++
#pragma comment(lib, "advapi32.lib")

#include <windows.h>
#include <stdio.h>
#include <aclapi.h>
#include <tchar.h>

void main()
{

    DWORD dwRes, dwDisposition;
    PSID pEveryoneSID = NULL, pAdminSID = NULL;
    PACL pACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea[2];
    SID_IDENTIFIER_AUTHORITY SIDAuthWorld =
            SECURITY_WORLD_SID_AUTHORITY;
    SID_IDENTIFIER_AUTHORITY SIDAuthNT = SECURITY_NT_AUTHORITY;
    SECURITY_ATTRIBUTES sa;
    LONG lRes;
    HKEY hkSub = NULL;

    // Create a well-known SID for the Everyone group.
    if(!AllocateAndInitializeSid(&SIDAuthWorld, 1,
                     SECURITY_WORLD_RID,
                     0, 0, 0, 0, 0, 0, 0,
                     &pEveryoneSID))
    {
        _tprintf(_T("AllocateAndInitializeSid Error %u\n"), GetLastError());
        goto Cleanup;
    }

    // Initialize an EXPLICIT_ACCESS structure for an ACE.
    // The ACE will allow Everyone read access to the key.
    ZeroMemory(&ea, 2 * sizeof(EXPLICIT_ACCESS));
    ea[0].grfAccessPermissions = KEY_READ;
    ea[0].grfAccessMode = SET_ACCESS;
    ea[0].grfInheritance= NO_INHERITANCE;
    ea[0].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[0].Trustee.TrusteeType = TRUSTEE_IS_WELL_KNOWN_GROUP;
    ea[0].Trustee.ptstrName  = (LPTSTR) pEveryoneSID;

    // Create a SID for the BUILTIN\Administrators group.
    if(! AllocateAndInitializeSid(&SIDAuthNT, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pAdminSID)) 
    {
        _tprintf(_T("AllocateAndInitializeSid Error %u\n"), GetLastError());
        goto Cleanup; 
    }

    // Initialize an EXPLICIT_ACCESS structure for an ACE.
    // The ACE will allow the Administrators group full access to
    // the key.
    ea[1].grfAccessPermissions = KEY_ALL_ACCESS;
    ea[1].grfAccessMode = SET_ACCESS;
    ea[1].grfInheritance= NO_INHERITANCE;
    ea[1].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[1].Trustee.TrusteeType = TRUSTEE_IS_GROUP;
    ea[1].Trustee.ptstrName  = (LPTSTR) pAdminSID;

    // Create a new ACL that contains the new ACEs.
    dwRes = SetEntriesInAcl(2, ea, NULL, &pACL);
    if (ERROR_SUCCESS != dwRes) 
    {
        _tprintf(_T("SetEntriesInAcl Error %u\n"), GetLastError());
        goto Cleanup;
    }

    // Initialize a security descriptor.  
    pSD = (PSECURITY_DESCRIPTOR) LocalAlloc(LPTR, 
                             SECURITY_DESCRIPTOR_MIN_LENGTH); 
    if (NULL == pSD) 
    { 
        _tprintf(_T("LocalAlloc Error %u\n"), GetLastError());
        goto Cleanup; 
    } 
 
    if (!InitializeSecurityDescriptor(pSD,
            SECURITY_DESCRIPTOR_REVISION)) 
    {  
        _tprintf(_T("InitializeSecurityDescriptor Error %u\n"),
                                GetLastError());
        goto Cleanup; 
    } 
 
    // Add the ACL to the security descriptor. 
    if (!SetSecurityDescriptorDacl(pSD, 
            TRUE,     // bDaclPresent flag   
            pACL, 
            FALSE))   // not a default DACL 
    {  
        _tprintf(_T("SetSecurityDescriptorDacl Error %u\n"),
                GetLastError());
        goto Cleanup; 
    } 

    // Initialize a security attributes structure.
    sa.nLength = sizeof (SECURITY_ATTRIBUTES);
    sa.lpSecurityDescriptor = pSD;
    sa.bInheritHandle = FALSE;

    // Use the security attributes to set the security descriptor 
    // when you create a key.
    lRes = RegCreateKeyEx(HKEY_CURRENT_USER, _T("mykey"), 0, _T(""), 0, 
            KEY_READ | KEY_WRITE, &sa, &hkSub, &dwDisposition); 
    _tprintf(_T("RegCreateKeyEx result %u\n"), lRes );

Cleanup:

    if (pEveryoneSID) 
        FreeSid(pEveryoneSID);
    if (pAdminSID) 
        FreeSid(pAdminSID);
    if (pACL) 
        LocalFree(pACL);
    if (pSD) 
        LocalFree(pSD);
    if (hkSub) 
        RegCloseKey(hkSub);

    return;

}
```



 

 

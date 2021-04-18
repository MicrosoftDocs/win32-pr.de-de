---
description: Im folgenden Beispiel wird versucht, die DACL eines File-Objekts zu ändern, indem der Besitz dieses Objekts übernommen wird.
ms.assetid: 0b309ac9-177d-425f-8b78-71fe73e41979
title: Übernehmen des Objekt Besitzes in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae43c28cb55193d43a15ed08f5905defded3dc2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347227"
---
# <a name="taking-object-ownership-in-c"></a>Übernehmen des Objekt Besitzes in C++

Im folgenden Beispiel wird versucht, die DACL eines File-Objekts zu ändern, indem der Besitz dieses Objekts übernommen wird. Dies ist nur erfolgreich, wenn der Aufrufer über Schreib \_ Zugriff auf das Objekt verfügt oder der Besitzer des Objekts ist. Wenn der anfängliche Versuch, die DACL zu ändern, fehlschlägt, kann ein Administrator den Besitz des Objekts übernehmen. Um dem Administrator den Besitz zu geben, aktiviert das Beispiel die \_ Berechtigung zum übernehmen \_ \_ von Besitz Namen in das [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)des Aufrufers und macht die Administratoren des lokalen Systems zum Besitzer des Objekts. Wenn der Aufrufer Mitglied der Gruppe "Administratoren" ist, kann der Code die DACL des Objekts ändern.

Zum Aktivieren und Deaktivieren von Berechtigungen wird in diesem Beispiel die unter [aktivieren und Deaktivieren von Berechtigungen in C++](enabling-and-disabling-privileges-in-c--.md)beschriebene setprivilege-Beispiel Funktion verwendet.


```C++
#include <windows.h>
#include <stdio.h>
#include <accctrl.h>
#include <aclapi.h>

//Forward declaration of SetPrivilege
BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) ;


BOOL TakeOwnership(LPTSTR lpszOwnFile) 
{

    BOOL bRetval = FALSE;

    HANDLE hToken = NULL; 
    PSID pSIDAdmin = NULL;
    PSID pSIDEveryone = NULL;
    PACL pACL = NULL;
    SID_IDENTIFIER_AUTHORITY SIDAuthWorld =
            SECURITY_WORLD_SID_AUTHORITY;
    SID_IDENTIFIER_AUTHORITY SIDAuthNT = SECURITY_NT_AUTHORITY;
    const int NUM_ACES  = 2;
    EXPLICIT_ACCESS ea[NUM_ACES];
    DWORD dwRes;

    // Specify the DACL to use.
    // Create a SID for the Everyone group.
    if (!AllocateAndInitializeSid(&SIDAuthWorld, 1,
                     SECURITY_WORLD_RID,
                     0,
                     0, 0, 0, 0, 0, 0,
                     &pSIDEveryone)) 
    {
        printf("AllocateAndInitializeSid (Everyone) error %u\n",
                GetLastError());
        goto Cleanup;
    }

    // Create a SID for the BUILTIN\Administrators group.
    if (!AllocateAndInitializeSid(&SIDAuthNT, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pSIDAdmin)) 
    {
        printf("AllocateAndInitializeSid (Admin) error %u\n",
                GetLastError());
        goto Cleanup;
    }

    ZeroMemory(&ea, NUM_ACES * sizeof(EXPLICIT_ACCESS));

    // Set read access for Everyone.
    ea[0].grfAccessPermissions = GENERIC_READ;
    ea[0].grfAccessMode = SET_ACCESS;
    ea[0].grfInheritance = NO_INHERITANCE;
    ea[0].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[0].Trustee.TrusteeType = TRUSTEE_IS_WELL_KNOWN_GROUP;
    ea[0].Trustee.ptstrName = (LPTSTR) pSIDEveryone;

    // Set full control for Administrators.
    ea[1].grfAccessPermissions = GENERIC_ALL;
    ea[1].grfAccessMode = SET_ACCESS;
    ea[1].grfInheritance = NO_INHERITANCE;
    ea[1].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[1].Trustee.TrusteeType = TRUSTEE_IS_GROUP;
    ea[1].Trustee.ptstrName = (LPTSTR) pSIDAdmin;

    if (ERROR_SUCCESS != SetEntriesInAcl(NUM_ACES,
                                         ea,
                                         NULL,
                                         &pACL))
    {
        printf("Failed SetEntriesInAcl\n");
        goto Cleanup;
    }

    // Try to modify the object's DACL.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        DACL_SECURITY_INFORMATION,   // change only the object's DACL
        NULL, NULL,                  // do not change owner or group
        pACL,                        // DACL specified
        NULL);                       // do not change SACL

    if (ERROR_SUCCESS == dwRes) 
    {
        printf("Successfully changed DACL\n");
        bRetval = TRUE;
        // No more processing needed.
        goto Cleanup;
    }
    if (dwRes != ERROR_ACCESS_DENIED)
    {
        printf("First SetNamedSecurityInfo call failed: %u\n",
                dwRes); 
        goto Cleanup;
    }

    // If the preceding call failed because access was denied, 
    // enable the SE_TAKE_OWNERSHIP_NAME privilege, create a SID for 
    // the Administrators group, take ownership of the object, and 
    // disable the privilege. Then try again to set the object's DACL.

    // Open a handle to the access token for the calling process.
    if (!OpenProcessToken(GetCurrentProcess(), 
                          TOKEN_ADJUST_PRIVILEGES, 
                          &hToken)) 
       {
          printf("OpenProcessToken failed: %u\n", GetLastError()); 
          goto Cleanup; 
       } 

    // Enable the SE_TAKE_OWNERSHIP_NAME privilege.
    if (!SetPrivilege(hToken, SE_TAKE_OWNERSHIP_NAME, TRUE)) 
    {
        printf("You must be logged on as Administrator.\n");
        goto Cleanup; 
    }

    // Set the owner in the object's security descriptor.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        OWNER_SECURITY_INFORMATION,  // change only the object's owner
        pSIDAdmin,                   // SID of Administrator group
        NULL,
        NULL,
        NULL); 

    if (dwRes != ERROR_SUCCESS) 
    {
        printf("Could not set owner. Error: %u\n", dwRes); 
        goto Cleanup;
    }
        
    // Disable the SE_TAKE_OWNERSHIP_NAME privilege.
    if (!SetPrivilege(hToken, SE_TAKE_OWNERSHIP_NAME, FALSE)) 
    {
        printf("Failed SetPrivilege call unexpectedly.\n");
        goto Cleanup;
    }

    // Try again to modify the object's DACL,
    // now that we are the owner.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        DACL_SECURITY_INFORMATION,   // change only the object's DACL
        NULL, NULL,                  // do not change owner or group
        pACL,                        // DACL specified
        NULL);                       // do not change SACL

    if (dwRes == ERROR_SUCCESS)
    {
        printf("Successfully changed DACL\n");
        bRetval = TRUE; 
    }
    else
    {
        printf("Second SetNamedSecurityInfo call failed: %u\n",
                dwRes); 
    }

Cleanup:

    if (pSIDAdmin)
        FreeSid(pSIDAdmin); 

    if (pSIDEveryone)
        FreeSid(pSIDEveryone); 

    if (pACL)
       LocalFree(pACL);

    if (hToken)
       CloseHandle(hToken);

    return bRetval;

}
```



 

 

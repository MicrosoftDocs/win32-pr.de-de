---
description: Im folgenden Beispiel werden die Funktionen OpenProcessToken und GetTokenInformation verwendet, um die Gruppenmitgliedschaften in einem Zugriffs Token zu erhalten.
ms.assetid: f895dfef-75ad-419c-95d0-6480bdf9c769
title: Suchen nach einer SID in einem Zugriffs Token in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713f69511f780898641e65f22503e595706307ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347229"
---
# <a name="searching-for-a-sid-in-an-access-token-in-c"></a>Suchen nach einer SID in einem Zugriffs Token in C++

Im folgenden Beispiel werden die Funktionen [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) und [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) verwendet, um die Gruppenmitgliedschaften in einem [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)zu erhalten. Anschließend wird mithilfe der " [**conneccateandinitializesid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) "-Funktion eine SID erstellt, die die bekannte SID der Administrator Gruppe für den lokalen Computer identifiziert. Im nächsten Schritt wird die [**equalsid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) -Funktion verwendet, um die bekannte SID mit den Gruppen-SIDs aus dem Zugriffs Token zu vergleichen. Wenn die SID im Token vorhanden ist, überprüft die Funktion die Attribute der SID, um zu bestimmen, ob Sie aktiviert ist.

Die [**checktokenmembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) -Funktion sollte verwendet werden, um zu bestimmen, ob eine angegebene SID in einem Zugriffs Token vorhanden und aktiviert ist. Diese Funktion beseitigt mögliche Fehlinterpretationen der aktiven Gruppenmitgliedschaft.


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "advapi32.lib")

#define MAX_NAME 256

BOOL SearchTokenGroupsForSID (VOID) 
{
    DWORD i, dwSize = 0, dwResult = 0;
    HANDLE hToken;
    PTOKEN_GROUPS pGroupInfo;
    SID_NAME_USE SidType;
    char lpName[MAX_NAME];
    char lpDomain[MAX_NAME];
    PSID pSID = NULL;
    SID_IDENTIFIER_AUTHORITY SIDAuth = SECURITY_NT_AUTHORITY;
       
    // Open a handle to the access token for the calling process.

    if (!OpenProcessToken( GetCurrentProcess(), TOKEN_QUERY, &hToken )) 
    {
        printf( "OpenProcessToken Error %u\n", GetLastError() );
        return FALSE;
    }

    // Call GetTokenInformation to get the buffer size.

    if(!GetTokenInformation(hToken, TokenGroups, NULL, dwSize, &dwSize)) 
    {
        dwResult = GetLastError();
        if( dwResult != ERROR_INSUFFICIENT_BUFFER ) {
            printf( "GetTokenInformation Error %u\n", dwResult );
            return FALSE;
        }
    }

    // Allocate the buffer.

    pGroupInfo = (PTOKEN_GROUPS) GlobalAlloc( GPTR, dwSize );

    // Call GetTokenInformation again to get the group information.

    if(! GetTokenInformation(hToken, TokenGroups, pGroupInfo, 
                            dwSize, &dwSize ) ) 
    {
        printf( "GetTokenInformation Error %u\n", GetLastError() );
        return FALSE;
    }

    // Create a SID for the BUILTIN\Administrators group.

    if(! AllocateAndInitializeSid( &SIDAuth, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pSID) ) 
    {
        printf( "AllocateAndInitializeSid Error %u\n", GetLastError() );
        return FALSE;
    }

    // Loop through the group SIDs looking for the administrator SID.

    for(i=0; i<pGroupInfo->GroupCount; i++) 
    {
        if ( EqualSid(pSID, pGroupInfo->Groups[i].Sid) ) 
        {

            // Lookup the account name and print it.

            dwSize = MAX_NAME;
            if( !LookupAccountSid( NULL, pGroupInfo->Groups[i].Sid,
                                  lpName, &dwSize, lpDomain, 
                                  &dwSize, &SidType ) ) 
            {
                dwResult = GetLastError();
                if( dwResult == ERROR_NONE_MAPPED )
                   strcpy_s (lpName, dwSize, "NONE_MAPPED" );
                else 
                {
                    printf("LookupAccountSid Error %u\n", GetLastError());
                    return FALSE;
                }
            }
            printf( "Current user is a member of the %s\\%s group\n", 
                    lpDomain, lpName );

            // Find out whether the SID is enabled in the token.
            if (pGroupInfo->Groups[i].Attributes & SE_GROUP_ENABLED)
                printf("The group SID is enabled.\n");
            else if (pGroupInfo->Groups[i].Attributes & 
                              SE_GROUP_USE_FOR_DENY_ONLY)
                printf("The group SID is a deny-only SID.\n");
            else 
                printf("The group SID is not enabled.\n");
        }
    }

    if (pSID)
        FreeSid(pSID);
    if ( pGroupInfo )
        GlobalFree( pGroupInfo );
    return TRUE;
}
```



 

 

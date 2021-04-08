---
description: Überprüfen Sie die Zugriffsrechte, die eine Sicherheits Beschreibung für einen Client zulässt.
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: Überprüfen des Client Zugriffs mit ACLs in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda629338d731d6e93f316fc15a6338c99bc1609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866256"
---
# <a name="verifying-client-access-with-acls-in-c"></a>Überprüfen des Client Zugriffs mit ACLs in C++

Das folgende Beispiel zeigt, wie ein Server die Zugriffsrechte überprüfen könnte, die eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) für einen Client zulässt. Im Beispiel wird die Funktion "Identitäts- [**amedpipeclient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) " verwendet. Allerdings würde dies mit den anderen Identitätswechsel Funktionen identisch funktionieren. Nach dem annehmen der Identität des Clients wird im Beispiel die [**openthumtotokenfunktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) aufgerufen, um das Identitätswechsel [*Token*](/windows/desktop/SecGloss/i-gly)zu erhalten. Anschließend wird die [**mapgenericmask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) -Funktion aufgerufen, um alle generischen Zugriffsrechte entsprechend der in der [**generischen \_**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) Zuordnungs Struktur angegebenen Zuordnung in die entsprechenden spezifischen und Standardrechte umzuwandeln.

Die [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) -Funktion überprüft die angeforderten Zugriffsrechte auf die Rechte, die für den Client in der DACL der Sicherheits Beschreibung zulässig sind. Um den Zugriff zu überprüfen und einen Eintrag im Sicherheits Ereignisprotokoll zu generieren, verwenden Sie die Funktion [**accesscheckandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) .


```C++
#include <windows.h>
#pragma comment(lib, "advapi32.lib")

BOOL ImpersonateAndCheckAccess(
  HANDLE hNamedPipe,               // handle of pipe to impersonate
  PSECURITY_DESCRIPTOR pSD,        // security descriptor to check
  DWORD dwAccessDesired,           // access rights to check
  PGENERIC_MAPPING pGeneric,       // generic mapping for object
  PDWORD pdwAccessAllowed          // returns allowed access rights
) 
{
   HANDLE hToken;
   PRIVILEGE_SET PrivilegeSet;
   DWORD dwPrivSetSize = sizeof( PRIVILEGE_SET );
   BOOL fAccessGranted=FALSE;

// Impersonate the client.

   if (! ImpersonateNamedPipeClient(hNamedPipe) ) 
      return FALSE;

// Get an impersonation token with the client's security context.

   if (! OpenThreadToken( GetCurrentThread(), TOKEN_ALL_ACCESS,
         TRUE, &hToken ))
   {
      goto Cleanup;
   }

// Use the GENERIC_MAPPING structure to convert any 
// generic access rights to object-specific access rights.

   MapGenericMask( &dwAccessDesired, pGeneric );

// Check the client's access rights.

   if( !AccessCheck( 
      pSD,                 // security descriptor to check
      hToken,              // impersonation token
      dwAccessDesired,     // requested access rights
      pGeneric,            // pointer to GENERIC_MAPPING
      &PrivilegeSet,       // receives privileges used in check
      &dwPrivSetSize,      // size of PrivilegeSet buffer
      pdwAccessAllowed,    // receives mask of allowed access rights
      &fAccessGranted ))   // receives results of access check
   {
      goto Cleanup;
   }

Cleanup:

   RevertToSelf();

   if (hToken != INVALID_HANDLE_VALUE)
      CloseHandle(hToken);  

   return fAccessGranted;
}
```



 

 

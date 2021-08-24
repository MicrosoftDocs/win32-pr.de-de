---
description: Überprüfen Sie die Zugriffsrechte, die ein Sicherheitsdeskriptor für einen Client zulässt.
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: Überprüfen des Clientzugriffs mit ACLs in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2160b48a3b88a617eaaea1e8fae63168db5a85e82cad62be5aef248ff51581
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906690"
---
# <a name="verifying-client-access-with-acls-in-c"></a>Überprüfen des Clientzugriffs mit ACLs in C++

Das folgende Beispiel zeigt, wie ein Server die Zugriffsrechte überprüfen kann, die ein [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) für einen Client zulässt. Im Beispiel wird die [**ImpersonateNamedPipeClient-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) verwendet. Dies funktioniert jedoch mithilfe einer der anderen Identitätswechselfunktionen gleich. Nach dem Identitätswechsel des Clients ruft das Beispiel die [**OpenThreadToken-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) auf, um das [*Identitätswechseltoken abzurufen.*](/windows/desktop/SecGloss/i-gly) Anschließend ruft sie die [**MapGenericMask-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) auf, um alle generischen Zugriffsrechte gemäß der in der GENERIC MAPPING-Struktur angegebenen Zuordnung in die entsprechenden spezifischen und [**\_ Standardrechte zu**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) konvertieren.

Die [**AccessCheck-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) überprüft die angeforderten Zugriffsrechte auf die Rechte, die für den Client in der DACL des Sicherheitsdeskriptors zulässig sind. Verwenden Sie die [**AccessCheckAndAuditAlarm-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) um den Zugriff zu überprüfen und einen Eintrag im Sicherheitsereignisprotokoll zu generieren.


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



 

 

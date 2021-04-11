---
description: Die LSA-Richtlinie bietet verschiedene Funktionen, mit denen Sie vertrauenswürdige Domänen erstellen, auflisten und löschen sowie Informationen zu vertrauenswürdigen Domänen festlegen und abrufen können.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Verwalten von Informationen zur vertrauenswürdigen Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7df297b8c83ebe9054ca6f04b657905c21fae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217616"
---
# <a name="managing-trusted-domain-information"></a>Verwalten von Informationen zur vertrauenswürdigen Domäne

Die LSA-Richtlinie bietet verschiedene Funktionen, mit denen Sie vertrauenswürdige Domänen erstellen, auflisten und löschen sowie Informationen zu vertrauenswürdigen Domänen festlegen und abrufen können.

Bevor Sie Informationen zu vertrauenswürdigen Domänen verwalten können, muss die Anwendung ein Handle für ein [**Richtlinien**](policy-object.md) Objekt erhalten, wie in [Öffnen eines Richtlinien Objekt Handles](opening-a-policy-object-handle.md)erläutert.

Sie können die vertrauenswürdigen Domänen durch Aufrufen von [**lsaenumeratetrusteddomainsex**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)auflisten.

Rufen Sie zum Abrufen von Informationen zu einer vertrauenswürdigen Domäne entweder " [**lsaquerytrust ddomaininfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) " oder " [**lsaquerytreuhänder ddomaininfobyname**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)" auf. Beide Funktionen geben dieselben Informationen zurück. Allerdings identifiziert **lsaquerytrust ddomaininfo** die vertrauenswürdige Domäne nach SID, und **lsaquerytreuhänder ddomaininfobyname** identifiziert die vertrauenswürdige Domäne anhand des Namens.

Um Informationen für eine vertrauenswürdige Domäne festzulegen, wenden Sie entweder [**lsasettrusteddomaininformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) oder [**lsasettrusteddomaininfobyname**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)an. Wie bei den Abfragefunktionen identifiziert **lsasettrusteddomaininformation** die vertrauenswürdige Domäne nach SID, während **lsasettrusteddomaininfobyname** die vertrauenswürdige Domäne anhand des Namens identifiziert.

Die Anwendung kann eine Vertrauensstellung für eine vertrauenswürdige Domäne widerrufen, indem [**lsadeletetrustddomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)aufgerufen wird.

Im folgenden Beispiel werden die vertrauenswürdigen Domänen für das lokale System aufgelistet.


```C++
#include <windows.h>

void EnumerateTrusts(LSA_HANDLE PolicyHandle)
{
  LSA_ENUMERATION_HANDLE hEnum=0; 
  PLSA_TRUST_INFORMATION TrustInfo = NULL;
  ULONG ulReturned = 0;               
  NTSTATUS Status = 0;
  ULONG i;
  WCHAR StringBuffer[256];

  // Enumerate the trusted domains until there are no more to return.
  do 
  {
    Status = LsaEnumerateTrustedDomains(
       PolicyHandle,         // an open policy handle
       &hEnum,               // enumeration tracker
       (PVOID*)&TrustInfo,   // buffer to receive data
       32000,                // recommended buffer size
       &ulReturned           // number of items returned in TrustInfo
    );

    // Check the return status for errors.
    if((Status != STATUS_SUCCESS) &&
       (Status != STATUS_MORE_ENTRIES) &&
     (Status != STATUS_NO_MORE_ENTRIES))
      {
        // Handle the error.
        wprintf(L"Error occurred enumerating domains %lu\n",
        LsaNtStatusToWinError(Status));
        return;
      } 

      wprintf(L"Status %lu\n", LsaNtStatusToWinError(Status));
      // Process the trusted domain information.
      for (i=0;i<ulReturned; i++) 
      {
        // LSA_Unicode strings might not be null-terminated.
        if(TrustInfo[i].Name.Length < 256)
        {
            wcsncpy_s(StringBuffer,
                256,
                TrustInfo[i].Name.Buffer,
                TrustInfo[i].Name.Length
            );
            // Guarantee that StringBuffer is null-terminated.
            StringBuffer[TrustInfo[i].Name.Length] = NULL; 
        }
        else
        {
            fprintf(stderr, "Name too long for string buffer.\n");
            exit(1);
        }
        
        wprintf(L"Enum Trusted Domain - %ws ", StringBuffer);
      }
      // Free the buffer.
      if (TrustInfo != NULL) 
      {
        LsaFreeMemory(TrustInfo);
        TrustInfo = NULL;
      }
    } while (Status != STATUS_NO_MORE_ENTRIES);
    return;
}
```



 

 




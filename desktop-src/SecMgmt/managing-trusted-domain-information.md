---
description: Die LSA-Richtlinie bietet mehrere Funktionen, mit denen Sie vertrauenswürdige Domänen erstellen, aufzählen und löschen sowie Informationen zu vertrauenswürdigen Domänen festlegen und abrufen können.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Verwalten von Informationen zu vertrauenswürdigen Domänen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a945705efaedf56920ee2170deeab9da0d01802259a57aca5cda2fac9d531aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894090"
---
# <a name="managing-trusted-domain-information"></a>Verwalten von Informationen zu vertrauenswürdigen Domänen

Die LSA-Richtlinie bietet mehrere Funktionen, mit denen Sie vertrauenswürdige Domänen erstellen, aufzählen und löschen sowie Informationen zu vertrauenswürdigen Domänen festlegen und abrufen können.

Bevor Sie vertrauenswürdige Domäneninformationen verwalten können, muss Ihre Anwendung ein Handle für ein [**Richtlinienobjekt**](policy-object.md) abrufen, wie unter [Öffnen eines Richtlinienobjekthandle](opening-a-policy-object-handle.md)erläutert.

Sie können die vertrauenswürdigen Domänen aufzählen, indem Sie [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)aufrufen.

Um Informationen zu einer vertrauenswürdigen Domäne abzurufen, rufen Sie entweder [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) oder [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)auf. Beide Funktionen geben die gleichen Informationen zurück. **LsaQueryTrustedDomainInfo** identifiziert die vertrauenswürdige Domäne jedoch anhand der SID, und **LsaQueryTrustedDomainInfoByName** identifiziert die vertrauenswürdige Domäne anhand des Namens.

Um Informationen für eine vertrauenswürdige Domäne festzulegen, rufen Sie entweder [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) oder [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)auf. Wie bei den Abfragefunktionen identifiziert **LsaSetTrustedDomainInformation** die vertrauenswürdige Domäne anhand der SID, während **LsaSetTrustedDomainInfoByName** die vertrauenswürdige Domäne anhand des Namens identifiziert.

Ihre Anwendung kann eine Vertrauensstellung für eine vertrauenswürdige Domäne widerrufen, indem [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)aufgerufen wird.

Im folgenden Beispiel werden die vertrauenswürdigen Domänen für das lokale System aufzählt.


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



 

 




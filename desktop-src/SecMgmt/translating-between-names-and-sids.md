---
description: Die lokale Sicherheitsstelle (Local Security Authority, LSA) stellt Funktionen für die Übersetzung zwischen Benutzer-, Gruppen- und lokalen Gruppennamen und den entsprechenden SID-Werten (Security Identifier) zur Verfügung.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Übersetzen zwischen Namen und SIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f67bd95e41a9813522d635e737f4fc528a61aebceeab205a2d40e1f44d7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004808"
---
# <a name="translating-between-names-and-sids"></a>Übersetzen zwischen Namen und SIDs

Die [*lokale Sicherheitsstelle*](/windows/desktop/SecGloss/l-gly) (Local Security Authority, LSA) stellt Funktionen für die Übersetzung zwischen Benutzer-, Gruppen- und lokalen Gruppennamen und den entsprechenden SID-Werten [*(Security Identifier)*](/windows/desktop/SecGloss/s-gly) zur Verfügung. Um Kontonamen zu suchen, rufen Sie die [**LsaLookupNames-Funktion**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) auf. Diese Funktion gibt die SID als RID-/Domänenindexpaar zurück. Um die SID als einzelnes Element zu erhalten, rufen Sie die [**LsaLookupNames2-Funktion**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) auf. Rufen Sie zum Suchen von SIDs [**LsaLookupSids auf.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)

Diese Funktionen können Namens- und SID-Informationen aus jeder Domäne übersetzen, die vom lokalen System als vertrauenswürdig eingestuft wird.

Bevor Sie zwischen Kontonamen und SIDs übersetzen können, muss Ihre Anwendung ein Handle für das lokale [**Policy-Objekt**](policy-object.md) erhalten, wie unter Öffnen eines [Richtlinienobjekthandpunkts gezeigt.](opening-a-policy-object-handle.md)

Im folgenden Beispiel wird die SID für ein Konto unter Berücksichtigung des Kontonamens nach der SID durch sucht.


```C++
void GetSIDInformation (LPWSTR AccountName,LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucName;
  PLSA_TRANSLATED_SID ltsTranslatedSID;
  PLSA_REFERENCED_DOMAIN_LIST lrdlDomainList;
  LSA_TRUST_INFORMATION myDomain;
  NTSTATUS ntsResult;
  PWCHAR DomainString = NULL;

  // Initialize an LSA_UNICODE_STRING with the name.
  if (!InitLsaString(&lucName, AccountName))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaLookupNames(
     PolicyHandle,     // handle to a Policy object
     1,                // number of names to look up
     &lucName,         // pointer to an array of names
     &lrdlDomainList,  // receives domain information
     &ltsTranslatedSID // receives relative SIDs
  );
  if (STATUS_SUCCESS != ntsResult) 
  {
    wprintf(L"Failed LsaLookupNames - %lu \n",
      LsaNtStatusToWinError(ntsResult));
    return;
  }

  // Get the domain the account resides in.
  myDomain = lrdlDomainList->Domains[ltsTranslatedSID->DomainIndex];
  DomainString = (PWCHAR) LocalAlloc(LPTR, myDomain.Name.Length + 1);
  wcsncpy_s(DomainString,
     myDomain.Name.Length + 1, 
     myDomain.Name.Buffer, 
     myDomain.Name.Length);

  // Display the relative Id. 
  wprintf(L"Relative Id is %lu in domain %ws.\n",
    ltsTranslatedSID->RelativeId,
    DomainString);

  LocalFree(DomainString);
  LsaFreeMemory(ltsTranslatedSID);
  LsaFreeMemory(lrdlDomainList);
}
```



Im vorherigen Beispiel konvertiert die **Funktion InitLsaString** eine Unicode-Zeichenfolge in eine [**LSA \_ UNICODE \_ STRING-Struktur.**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) Der Code für diese Funktion wird unter Verwenden von [LSA Unicode-Zeichenfolgen gezeigt.](using-lsa-unicode-strings.md)

> [!Note]  
> Diese Übersetzungsfunktionen werden hauptsächlich von Berechtigungs-Editoren bereitgestellt, um Informationen zur Zugriffssteuerungsliste (Access [*Control List,*](/windows/desktop/SecGloss/a-gly) ACL) anzuzeigen. Ein Berechtigungs-Editor sollte diese Funktionen immer mithilfe des [**Richtlinienobjekts**](policy-object.md) für das System aufrufen, in dem sich der Name oder die [*Sicherheits-ID-SID*](/windows/desktop/SecGloss/s-gly) befindet. Dadurch wird sichergestellt, dass während der Übersetzung auf die richtigen vertrauenswürdigen Domänen verwiesen wird.

 

Windows Access Control stellt auch Funktionen zur Verfügung, die Übersetzungen zwischen SIDs und Kontonamen ausführen: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) und [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Wenn Ihre Anwendung einen Kontonamen oder eine SID suchen muss und keine zusätzlicheN LSA-Richtlinienfunktionen verwendet, verwenden Sie die Windows Access Control-Funktionen anstelle der LSA-Richtlinienfunktionen. Weitere Informationen zu diesen Funktionen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

 

 

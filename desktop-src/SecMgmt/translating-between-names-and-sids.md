---
description: Die lokale Sicherheits Autorität (Local Security Authority, LSA) stellt Funktionen bereit, um zwischen Benutzer-, Gruppen-und lokalen Gruppennamen und den entsprechenden sid-Werten (Security Identifier) zu übersetzen.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Übersetzen von Namen und SIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417034a99331c09f20546f2f352bc762a86f02e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348759"
---
# <a name="translating-between-names-and-sids"></a>Übersetzen von Namen und SIDs

Die [*Lokale Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) stellt Funktionen bereit, um zwischen Benutzer-, Gruppen-und lokalen Gruppennamen und den entsprechenden sid-Werten ( [*Security Identifier*](/windows/desktop/SecGloss/s-gly) ) zu übersetzen. Um nach Kontonamen zu suchen, nennen Sie die [**lsalookupnames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) -Funktion. Diese Funktion gibt die SID als RID/Domänen-Index paar zurück. Um die SID als einzelnes Element abzurufen, nennen Sie die [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) -Funktion. Um SIDs zu suchen, nennen Sie [**lsalookupsids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).

Diese Funktionen können Name-und SID-Informationen von allen Domänen übersetzen, denen das lokale System vertraut.

Bevor Sie die Kontonamen und SIDs übersetzen können, muss die Anwendung ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt erhalten, wie in [Öffnen eines Richtlinien Objekt Handles](opening-a-policy-object-handle.md)gezeigt.

Im folgenden Beispiel wird die SID anhand des Konto namens nach einem Konto gesucht.


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



Im vorherigen Beispiel konvertiert die Funktion **initlsastring** eine Unicode-Zeichenfolge in eine [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Struktur. Der Code für diese Funktion wird in [Verwenden von LSA-Unicode](using-lsa-unicode-strings.md)-Zeichen folgen angezeigt.

> [!Note]  
> Diese Übersetzungsfunktionen werden hauptsächlich für die Verwendung durch Berechtigungs-Editoren zur Anzeige von [*Zugriffs Steuerungs Listen*](/windows/desktop/SecGloss/a-gly) -Informationen bereitgestellt. Ein Berechtigungs-Editor sollte diese Funktionen immer mit dem [**Richtlinien**](policy-object.md) Objekt für das System, in dem sich der Name oder die [*sicherheitsbezeichnersid*](/windows/desktop/SecGloss/s-gly) befindet, aufruft. Dadurch wird sichergestellt, dass während der Übersetzung auf den richtigen Satz vertrauenswürdiger Domänen verwiesen wird.

 

Windows Access Control bietet auch Funktionen, die Übersetzungen zwischen SIDs und Kontonamen ausführen: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) und [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Wenn Ihre Anwendung einen Kontonamen oder eine SID suchen muss und keine zusätzliche LSA-Richtlinien Funktionalität verwendet, verwenden Sie die Windows Access Control-Funktionen anstelle der LSA-Richtlinien Funktionen. Weitere Informationen zu diesen Funktionen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

 

 

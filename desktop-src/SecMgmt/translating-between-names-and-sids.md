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
# <a name="translating-between-names-and-sids"></a><span data-ttu-id="80c8a-103">Übersetzen von Namen und SIDs</span><span class="sxs-lookup"><span data-stu-id="80c8a-103">Translating Between Names and SIDs</span></span>

<span data-ttu-id="80c8a-104">Die [*Lokale Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) stellt Funktionen bereit, um zwischen Benutzer-, Gruppen-und lokalen Gruppennamen und den entsprechenden sid-Werten ( [*Security Identifier*](/windows/desktop/SecGloss/s-gly) ) zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="80c8a-104">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) provides functions to translate between user, group, and local group names and their corresponding [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) values.</span></span> <span data-ttu-id="80c8a-105">Um nach Kontonamen zu suchen, nennen Sie die [**lsalookupnames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="80c8a-105">To locate account names, call the [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) function.</span></span> <span data-ttu-id="80c8a-106">Diese Funktion gibt die SID als RID/Domänen-Index paar zurück.</span><span class="sxs-lookup"><span data-stu-id="80c8a-106">This function returns the SID as a RID/Domain index pair.</span></span> <span data-ttu-id="80c8a-107">Um die SID als einzelnes Element abzurufen, nennen Sie die [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="80c8a-107">To get the SID as a single element, call the [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) function.</span></span> <span data-ttu-id="80c8a-108">Um SIDs zu suchen, nennen Sie [**lsalookupsids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span><span class="sxs-lookup"><span data-stu-id="80c8a-108">To locate SIDs, call [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span></span>

<span data-ttu-id="80c8a-109">Diese Funktionen können Name-und SID-Informationen von allen Domänen übersetzen, denen das lokale System vertraut.</span><span class="sxs-lookup"><span data-stu-id="80c8a-109">These functions can translate name and SID information from any domain trusted by the local system.</span></span>

<span data-ttu-id="80c8a-110">Bevor Sie die Kontonamen und SIDs übersetzen können, muss die Anwendung ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt erhalten, wie in [Öffnen eines Richtlinien Objekt Handles](opening-a-policy-object-handle.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="80c8a-110">Before you can translate between account names and SIDs, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="80c8a-111">Im folgenden Beispiel wird die SID anhand des Konto namens nach einem Konto gesucht.</span><span class="sxs-lookup"><span data-stu-id="80c8a-111">The following example looks up the SID for an account, given the account name.</span></span>


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



<span data-ttu-id="80c8a-112">Im vorherigen Beispiel konvertiert die Funktion **initlsastring** eine Unicode-Zeichenfolge in eine [**LSA- \_ Unicode- \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Struktur.</span><span class="sxs-lookup"><span data-stu-id="80c8a-112">In the preceding example, the function **InitLsaString** converts a Unicode string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="80c8a-113">Der Code für diese Funktion wird in [Verwenden von LSA-Unicode](using-lsa-unicode-strings.md)-Zeichen folgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="80c8a-113">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

> [!Note]  
> <span data-ttu-id="80c8a-114">Diese Übersetzungsfunktionen werden hauptsächlich für die Verwendung durch Berechtigungs-Editoren zur Anzeige von [*Zugriffs Steuerungs Listen*](/windows/desktop/SecGloss/a-gly) -Informationen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="80c8a-114">These translation functions are primarily provided for use by permissions editors to display [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) information.</span></span> <span data-ttu-id="80c8a-115">Ein Berechtigungs-Editor sollte diese Funktionen immer mit dem [**Richtlinien**](policy-object.md) Objekt für das System, in dem sich der Name oder die [*sicherheitsbezeichnersid*](/windows/desktop/SecGloss/s-gly) befindet, aufruft.</span><span class="sxs-lookup"><span data-stu-id="80c8a-115">A permission editor should always call these functions using the [**Policy**](policy-object.md) object for the system where the name or [*security identifier*](/windows/desktop/SecGloss/s-gly) SID is located.</span></span> <span data-ttu-id="80c8a-116">Dadurch wird sichergestellt, dass während der Übersetzung auf den richtigen Satz vertrauenswürdiger Domänen verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="80c8a-116">This ensures that the proper set of trusted domains is referenced during the translation.</span></span>

 

<span data-ttu-id="80c8a-117">Windows Access Control bietet auch Funktionen, die Übersetzungen zwischen SIDs und Kontonamen ausführen: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) und [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span><span class="sxs-lookup"><span data-stu-id="80c8a-117">Windows Access Control also provides functions that perform translations between SIDs and account names: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) and [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span></span> <span data-ttu-id="80c8a-118">Wenn Ihre Anwendung einen Kontonamen oder eine SID suchen muss und keine zusätzliche LSA-Richtlinien Funktionalität verwendet, verwenden Sie die Windows Access Control-Funktionen anstelle der LSA-Richtlinien Funktionen.</span><span class="sxs-lookup"><span data-stu-id="80c8a-118">If your application needs to look up an account name or SID and does not use additional LSA Policy functionality, use the Windows Access Control functions instead of the LSA Policy functions.</span></span> <span data-ttu-id="80c8a-119">Weitere Informationen zu diesen Funktionen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="80c8a-119">For more information about these functions, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

 

 

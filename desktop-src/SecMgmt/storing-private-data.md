---
description: Die LSA-Richtlinie stellt zwei Funktionen bereit, mit denen Sie private Daten festlegen und abrufen können.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Speichern privater Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393498"
---
# <a name="storing-private-data"></a><span data-ttu-id="4cbb2-103">Speichern privater Daten</span><span class="sxs-lookup"><span data-stu-id="4cbb2-103">Storing Private Data</span></span>

<span data-ttu-id="4cbb2-104">Die LSA-Richtlinie stellt zwei Funktionen bereit, mit denen Sie private Daten festlegen und abrufen können.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-104">LSA Policy provides two functions that you can use to set and retrieve private data.</span></span> <span data-ttu-id="4cbb2-105">Diese Daten werden als verschlüsselte Zeichenfolge in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-105">This data is stored as an encrypted string in the registry.</span></span> <span data-ttu-id="4cbb2-106">Beispielsweise können Sie diese Funktionen zum Speichern von Server Konto Kennwörtern und anderen vertraulichen Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-106">For example, you can use these functions to store server account passwords and other sensitive information.</span></span>

<span data-ttu-id="4cbb2-107">Ruft die [**lsastoreprivatedata**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion auf, um private Daten zu speichern und zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-107">Call the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function to store and encrypt private data.</span></span> <span data-ttu-id="4cbb2-108">Wie im [privaten Datenobjekt](private-data-object.md)beschrieben, beinhalten private Datenobjekte drei spezialisierte Typen: "local", "Global" und "Machine".</span><span class="sxs-lookup"><span data-stu-id="4cbb2-108">As described in [Private Data Object](private-data-object.md), private data objects include three specialized types: local, global, and machine.</span></span> <span data-ttu-id="4cbb2-109">Fügen Sie zum Erstellen eines spezialisierten Objekts dem an **lsastoreprivatedata** weiter gegebenen Schlüsselnamen ein Präfix hinzu: "L $" für lokale Objekte, "G $" für globale Objekte und "M $" für Computer Objekte.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-109">To create a specialized object, add a prefix to the key name passed to **LsaStorePrivateData**: "L$" for local objects, "G$" for global objects, and "M$" for machine objects.</span></span> <span data-ttu-id="4cbb2-110">Wenn Sie keinen dieser speziellen Typen erstellen, müssen Sie kein Schlüsselnamen Präfix angeben.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-110">If you are not creating one of these specialized types, you do not need to specify a key name prefix.</span></span>

<span data-ttu-id="4cbb2-111">Um zuvor gespeicherte Private Daten abzurufen und zu decodieren, rufen Sie [**lsarelteveprivatedata**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)auf.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-111">To retrieve and decode previously stored private data, call [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span></span> <span data-ttu-id="4cbb2-112">Beachten Sie, dass Sie keine privaten Computer Datenobjekte abrufen können. Computer Objekte können nur vom Betriebssystem abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-112">Note that you cannot retrieve machine private data objects; machine objects can be retrieved only by the operating system.</span></span>

<span data-ttu-id="4cbb2-113">Bevor Sie private Daten speichern oder abrufen können, muss die Anwendung ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt erhalten, wie in [Öffnen eines Richtlinien Objekt Handles](opening-a-policy-object-handle.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-113">Before you can store or retrieve private data, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="4cbb2-114">Im folgenden Beispiel wird ein lokales privates Datenobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-114">The following example creates a local private data object.</span></span> <span data-ttu-id="4cbb2-115">Beachten Sie, dass die Funktion initlsastring eine [*Unicode*](/windows/desktop/SecGloss/u-gly) -Zeichenfolge in eine [**LSA-Unicode- \_ \_ Zeichen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) folgen Struktur konvertiert.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-115">Note that the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="4cbb2-116">Der Code für diese Funktion wird in [Verwenden von LSA-Unicode](using-lsa-unicode-strings.md)-Zeichen folgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-116">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="4cbb2-117">Die von der [**lsastoreprivatedata**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion gespeicherten Daten sind nicht absolut geschützt.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-117">The data stored by the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function is not absolutely protected.</span></span> <span data-ttu-id="4cbb2-118">Der Schlüssel verfügt jedoch über eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL), mit der nur die Ersteller und Administratoren die Daten lesen können.</span><span class="sxs-lookup"><span data-stu-id="4cbb2-118">The key, however, has a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that allows only the creator and administrators to read the data.</span></span>

 

 

 

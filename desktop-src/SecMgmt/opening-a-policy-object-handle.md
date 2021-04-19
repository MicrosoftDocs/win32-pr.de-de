---
description: Die meisten LSA-Richtlinien Funktionen erfordern ein Handle für das Richtlinien Objekt, das vom System abgefragt oder geändert werden soll. Rufen Sie zum Abrufen eines Handles für ein Richtlinien Objekt LsaOpenPolicy auf, und geben Sie den Namen des Systems an, auf das Sie zugreifen möchten, sowie den Satz der erforderlichen Zugriffsberechtigungen.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Öffnen eines Policy-Objekt Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c187720692db4937b6e1299dd2bb63fac647852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362956"
---
# <a name="opening-a-policy-object-handle"></a><span data-ttu-id="a1deb-104">Öffnen eines Policy-Objekt Handles</span><span class="sxs-lookup"><span data-stu-id="a1deb-104">Opening a Policy Object Handle</span></span>

<span data-ttu-id="a1deb-105">Die meisten LSA-Richtlinien Funktionen erfordern ein Handle für das [**Richtlinien**](policy-object.md) Objekt, das vom System abgefragt oder geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1deb-105">Most LSA Policy functions require a handle to the [**Policy**](policy-object.md) object for the system to query or modify.</span></span> <span data-ttu-id="a1deb-106">Rufen Sie zum Abrufen eines Handles für ein **Richtlinien** Objekt [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) auf, und geben Sie den Namen des Systems an, auf das Sie zugreifen möchten, sowie den Satz der erforderlichen Zugriffsberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="a1deb-106">To obtain a handle to a **Policy** object, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) and specify the name of the system you want to access and the set of access permissions required.</span></span>

<span data-ttu-id="a1deb-107">Welche Zugriffsberechtigungen für die Anwendung erforderlich sind, hängt von den Aktionen ab, die Sie ausführt.</span><span class="sxs-lookup"><span data-stu-id="a1deb-107">The access permissions required for your application depend on the actions it performs.</span></span> <span data-ttu-id="a1deb-108">Ausführliche Informationen zu den Berechtigungen, die für die einzelnen Funktionen erforderlich sind, finden Sie in der Beschreibung dieser Funktion in [LSA-Richtlinien Funktionen](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a1deb-108">For details about the permissions required for each function, see the description of that function in [LSA Policy Functions](management-functions.md).</span></span>

<span data-ttu-id="a1deb-109">Wenn der [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) -Aufrufvorgang erfolgreich ist, wird ein Handle für das [**Richtlinien**](policy-object.md) Objekt für das angegebene System zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1deb-109">If the call to [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) is successful, it returns a handle to the [**Policy**](policy-object.md) object for the specified system.</span></span> <span data-ttu-id="a1deb-110">Die Anwendung übergibt dann dieses Handle in nachfolgenden LSA-Richtlinien Funktionsaufrufen.</span><span class="sxs-lookup"><span data-stu-id="a1deb-110">Your application then passes this handle in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="a1deb-111">Wenn die Anwendung das Handle nicht mehr benötigt, sollte Sie [**lsaclose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) zum Freigeben von anrufen.</span><span class="sxs-lookup"><span data-stu-id="a1deb-111">When your application no longer needs the handle, it should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) to free it.</span></span>

<span data-ttu-id="a1deb-112">Im folgenden Beispiel wird gezeigt, wie ein [**Richtlinien**](policy-object.md) Objekt Handle geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a1deb-112">The following example shows how to open a [**Policy**](policy-object.md) object handle.</span></span>


```C++
#include <windows.h>

#define TARGET_SYSTEM_NAME L"mysystem"

LSA_HANDLE GetPolicyHandle()
{
  LSA_OBJECT_ATTRIBUTES ObjectAttributes;
  WCHAR SystemName[] = TARGET_SYSTEM_NAME;
  USHORT SystemNameLength;
  LSA_UNICODE_STRING lusSystemName;
  NTSTATUS ntsResult;
  LSA_HANDLE lsahPolicyHandle;

  // Object attributes are reserved, so initialize to zeros.
  ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

  //Initialize an LSA_UNICODE_STRING to the server name.
  SystemNameLength = wcslen(SystemName);
  lusSystemName.Buffer = SystemName;
  lusSystemName.Length = SystemNameLength * sizeof(WCHAR);
  lusSystemName.MaximumLength = (SystemNameLength+1) * sizeof(WCHAR);

  // Get a handle to the Policy object.
  ntsResult = LsaOpenPolicy(
        &lusSystemName,    //Name of the target system.
        &ObjectAttributes, //Object attributes.
        POLICY_ALL_ACCESS, //Desired access permissions.
        &lsahPolicyHandle  //Receives the policy handle.
    );

  if (ntsResult != STATUS_SUCCESS)
  {
    // An error occurred. Display it as a win32 error code.
    wprintf(L"OpenPolicy returned %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return NULL;
  } 
  return lsahPolicyHandle;
}
```



<span data-ttu-id="a1deb-113">Im vorherigen Beispiel hat die Anwendung Richtlinien für \_ alle \_ Zugriffs [*Berechtigungen*](/windows/desktop/SecGloss/p-gly)angefordert.</span><span class="sxs-lookup"><span data-stu-id="a1deb-113">In the preceding example, the application requested POLICY\_ALL\_ACCESS [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="a1deb-114">Ausführliche Informationen zu den Berechtigungen, die Ihre Anwendung beim Aufrufen von [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)anfordern soll, finden Sie in den Beschreibungen der Funktionen, an die die Anwendung das [**Richtlinien**](policy-object.md) Objekt Handle übergibt.</span><span class="sxs-lookup"><span data-stu-id="a1deb-114">For details about which permissions your application should request when calling [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), see the descriptions of the functions that your application will pass the [**Policy**](policy-object.md) object handle to.</span></span>

<span data-ttu-id="a1deb-115">Rufen Sie zum Öffnen eines Handles für das [**Richtlinien**](policy-object.md) Objekt einer vertrauenswürdigen Domäne [**lsacreatetrusteddomainex**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) auf (um eine neue Vertrauensstellung mit einer Domäne zu erstellen), oder rufen Sie [**lsaopentrusteddomainbyname**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) auf (um auf eine vorhandene Vertrauenswürdige Domäne zuzugreifen).</span><span class="sxs-lookup"><span data-stu-id="a1deb-115">To open a handle to the [**Policy**](policy-object.md) object of a trusted domain, call [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (to create a new trust relationship with a domain) or call [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (to access an existing trusted domain).</span></span> <span data-ttu-id="a1deb-116">Beide Funktionen legen einen Zeiger auf ein [**LSA- \_ handle**](lsa-handle.md)fest, das Sie dann in nachfolgenden LSA-Richtlinien Funktionsaufrufen angeben können.</span><span class="sxs-lookup"><span data-stu-id="a1deb-116">Both of these functions set a pointer to an [**LSA\_HANDLE**](lsa-handle.md), which you can then specify in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="a1deb-117">Wie bei [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)sollte Ihre Anwendung auch [**lsaclose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) aufgerufen werden, wenn das Handle für das **Richtlinien** Objekt der vertrauenswürdigen Domäne nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a1deb-117">As with [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), your application should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) when it no longer needs the handle to the trusted domain's **Policy** object.</span></span>

 

 

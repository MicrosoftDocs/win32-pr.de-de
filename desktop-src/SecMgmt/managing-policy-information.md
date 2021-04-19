---
description: Die LSA stellt Funktionen bereit, die Administratoren verwenden können, um globale Richtlinien Informationen für den lokalen Computer und die Domäne abzufragen und festzulegen.
ms.assetid: bbe27d16-0a6b-435a-ae80-5e983047b511
title: Verwalten von Richtlinien Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc76137f41c592370dbeecafd243f11012cb1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363670"
---
# <a name="managing-policy-information"></a><span data-ttu-id="49094-103">Verwalten von Richtlinien Informationen</span><span class="sxs-lookup"><span data-stu-id="49094-103">Managing Policy Information</span></span>

<span data-ttu-id="49094-104">Die LSA stellt Funktionen bereit, die Administratoren verwenden können, um globale Richtlinien Informationen für den lokalen Computer und die Domäne abzufragen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="49094-104">The LSA provides functions that administrators can use to query and set global policy information for the local computer and the domain.</span></span>

<span data-ttu-id="49094-105">Bevor Sie die Richtlinien Informationen verwalten können, muss die Anwendung ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt erhalten, wie in [Öffnen eines Richtlinien Objekt Handles](opening-a-policy-object-handle.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="49094-105">Before you can manage policy information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="49094-106">Dieses Handle ist für die Funktionen erforderlich, die Richtlinien Informationen verwalten.</span><span class="sxs-lookup"><span data-stu-id="49094-106">This handle is required by the functions that manage policy information.</span></span>

<span data-ttu-id="49094-107">Rufen Sie zum Abrufen von Informationen über die lokale Sicherheitsrichtlinie [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy)auf.</span><span class="sxs-lookup"><span data-stu-id="49094-107">To retrieve information about the local security policy, call [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy).</span></span> <span data-ttu-id="49094-108">Um die lokale Sicherheitsrichtlinie festzulegen, wenden Sie [**lsasetinformationpolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy)an.</span><span class="sxs-lookup"><span data-stu-id="49094-108">To set local security policy, call [**LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy).</span></span> <span data-ttu-id="49094-109">Die Beschreibung der Enumeration der [**\_ richtlinieninformationsklasse \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) enthält Informationen zu den Typen von Richtlinien Informationen, die abgefragt oder festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="49094-109">The description of the [**POLICY\_INFORMATION\_CLASS**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) enumeration details the types of policy information that can be queried or set.</span></span>

<span data-ttu-id="49094-110">Im folgenden Beispiel wird veranschaulicht, wie die Konto Domänen Informationen eines Systems abgerufen werden, wenn ein Handle für das [**Richtlinien**](policy-object.md) Objekt des Systems angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="49094-110">The following example demonstrates how to obtain a system's account domain information, given a handle to the system's [**Policy**](policy-object.md) object.</span></span>


```C++
#include <windows.h>

BOOL GetAccountDomainInfo(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult = STATUS_SUCCESS;
  PPOLICY_ACCOUNT_DOMAIN_INFO pPADInfo = NULL;
  PWCHAR name = NULL;
  UINT nameSize;
  
  ntsResult = LsaQueryInformationPolicy(
    PolicyHandle,                   // Open handle to a Policy object.
    PolicyAccountDomainInformation, // The information to get.
    (PVOID *)&pPADInfo              // Storage for the information.
  );

  if (ntsResult == STATUS_SUCCESS)
  {  
    // There is no guarantee that the LSA_UNICODE_STRING buffer
    // is null-terminated, so copy the name to a buffer that is.
    nameSize =  pPADInfo->DomainName.Length + 1 * sizeof(WCHAR);
    name = (WCHAR *) LocalAlloc(LPTR, nameSize);
    if (!name)
    {
        wprintf(L"Failed LocalAlloc\n");
        exit(1);
    }
    wcsncpy_s(name, nameSize, pPADInfo->DomainName.Buffer,
        pPADInfo->DomainName.Length);
    wprintf(L"The account domain name is %ws\n", name);
    LocalFree(name);
    if (STATUS_SUCCESS != LsaFreeMemory(pPADInfo))
        wprintf(L"LsaFreeMemory error\n");
  }
  else
  {
    // Show the corresponding win32 error code.
    wprintf(
        L"Error obtaining account domain information - (win32) %lu\n",
        LsaNtStatusToWinError(ntsResult));
  }

  return !ntsResult;
}

```



 

 

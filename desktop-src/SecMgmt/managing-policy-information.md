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
# <a name="managing-policy-information"></a>Verwalten von Richtlinien Informationen

Die LSA stellt Funktionen bereit, die Administratoren verwenden können, um globale Richtlinien Informationen für den lokalen Computer und die Domäne abzufragen und festzulegen.

Bevor Sie die Richtlinien Informationen verwalten können, muss die Anwendung ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt erhalten, wie in [Öffnen eines Richtlinien Objekt Handles](opening-a-policy-object-handle.md)gezeigt. Dieses Handle ist für die Funktionen erforderlich, die Richtlinien Informationen verwalten.

Rufen Sie zum Abrufen von Informationen über die lokale Sicherheitsrichtlinie [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy)auf. Um die lokale Sicherheitsrichtlinie festzulegen, wenden Sie [**lsasetinformationpolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy)an. Die Beschreibung der Enumeration der [**\_ richtlinieninformationsklasse \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) enthält Informationen zu den Typen von Richtlinien Informationen, die abgefragt oder festgelegt werden können.

Im folgenden Beispiel wird veranschaulicht, wie die Konto Domänen Informationen eines Systems abgerufen werden, wenn ein Handle für das [**Richtlinien**](policy-object.md) Objekt des Systems angegeben wird.


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



 

 

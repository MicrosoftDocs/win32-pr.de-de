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
# <a name="opening-a-policy-object-handle"></a>Öffnen eines Policy-Objekt Handles

Die meisten LSA-Richtlinien Funktionen erfordern ein Handle für das [**Richtlinien**](policy-object.md) Objekt, das vom System abgefragt oder geändert werden soll. Rufen Sie zum Abrufen eines Handles für ein **Richtlinien** Objekt [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) auf, und geben Sie den Namen des Systems an, auf das Sie zugreifen möchten, sowie den Satz der erforderlichen Zugriffsberechtigungen.

Welche Zugriffsberechtigungen für die Anwendung erforderlich sind, hängt von den Aktionen ab, die Sie ausführt. Ausführliche Informationen zu den Berechtigungen, die für die einzelnen Funktionen erforderlich sind, finden Sie in der Beschreibung dieser Funktion in [LSA-Richtlinien Funktionen](management-functions.md).

Wenn der [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) -Aufrufvorgang erfolgreich ist, wird ein Handle für das [**Richtlinien**](policy-object.md) Objekt für das angegebene System zurückgegeben. Die Anwendung übergibt dann dieses Handle in nachfolgenden LSA-Richtlinien Funktionsaufrufen. Wenn die Anwendung das Handle nicht mehr benötigt, sollte Sie [**lsaclose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) zum Freigeben von anrufen.

Im folgenden Beispiel wird gezeigt, wie ein [**Richtlinien**](policy-object.md) Objekt Handle geöffnet wird.


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



Im vorherigen Beispiel hat die Anwendung Richtlinien für \_ alle \_ Zugriffs [*Berechtigungen*](/windows/desktop/SecGloss/p-gly)angefordert. Ausführliche Informationen zu den Berechtigungen, die Ihre Anwendung beim Aufrufen von [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)anfordern soll, finden Sie in den Beschreibungen der Funktionen, an die die Anwendung das [**Richtlinien**](policy-object.md) Objekt Handle übergibt.

Rufen Sie zum Öffnen eines Handles für das [**Richtlinien**](policy-object.md) Objekt einer vertrauenswürdigen Domäne [**lsacreatetrusteddomainex**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) auf (um eine neue Vertrauensstellung mit einer Domäne zu erstellen), oder rufen Sie [**lsaopentrusteddomainbyname**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) auf (um auf eine vorhandene Vertrauenswürdige Domäne zuzugreifen). Beide Funktionen legen einen Zeiger auf ein [**LSA- \_ handle**](lsa-handle.md)fest, das Sie dann in nachfolgenden LSA-Richtlinien Funktionsaufrufen angeben können. Wie bei [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)sollte Ihre Anwendung auch [**lsaclose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) aufgerufen werden, wenn das Handle für das **Richtlinien** Objekt der vertrauenswürdigen Domäne nicht mehr benötigt wird.

 

 

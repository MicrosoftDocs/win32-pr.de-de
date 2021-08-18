---
description: Die meisten LSA-Richtlinienfunktionen erfordern ein Handle für das Policy-Objekt, damit das System abfragen oder ändern kann. Um ein Handle für ein Policy-Objekt zu erhalten, rufen Sie LsaOpenPolicy auf, und geben Sie den Namen des Systems, auf das Sie zugreifen möchten, und den Satz der erforderlichen Zugriffsberechtigungen an.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Öffnen eines Richtlinienobjekthandpunkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16baf2cf7e722faca1f0441505ec325b8e64c8aad95522e697b4905f566985af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894051"
---
# <a name="opening-a-policy-object-handle"></a>Öffnen eines Richtlinienobjekthandpunkts

Die meisten LSA-Richtlinienfunktionen erfordern ein Handle für das [**Policy-Objekt,**](policy-object.md) damit das System abfragen oder ändern kann. Um ein Handle für ein **Policy-Objekt** zu erhalten, rufen Sie [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) auf, und geben Sie den Namen des Systems, auf das Sie zugreifen möchten, und den Satz der erforderlichen Zugriffsberechtigungen an.

Welche Zugriffsberechtigungen für Ihre Anwendung erforderlich sind, hängt von den aktionen ab, die sie ausführt. Ausführliche Informationen zu den berechtigungen, die für jede Funktion erforderlich sind, finden Sie in der Beschreibung dieser Funktion in [LSA Policy Functions](management-functions.md).

Wenn der Aufruf von [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) erfolgreich ist, wird ein Handle an das [**Policy-Objekt**](policy-object.md) für das angegebene System zurückgegeben. Die Anwendung übergibt dieses Handle dann in nachfolgenden LSA Policy-Funktionsaufrufen. Wenn Ihre Anwendung das Handle nicht mehr benötigt, sollte sie [**LsaClose aufrufen,**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) um es frei zu geben.

Das folgende Beispiel zeigt, wie sie ein [**Policy-Objekthand**](policy-object.md) handle öffnen.


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



Im vorherigen Beispiel hat die Anwendung die BERECHTIGUNGEN POLICY \_ ALL \_ ACCESS [*angefordert.*](/windows/desktop/SecGloss/p-gly) Ausführliche Informationen dazu, welche Berechtigungen Ihre Anwendung beim Aufrufen von [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)anfordern soll, finden Sie in den Beschreibungen der Funktionen, an die Ihre Anwendung das Handle des [**Policy-Objekts**](policy-object.md) übergehen wird.

Um ein Handle für das [**Policy-Objekt**](policy-object.md) einer vertrauenswürdigen Domäne zu öffnen, rufen Sie [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) auf (um eine neue Vertrauensstellung mit einer Domäne zu erstellen), oder rufen [**Sie LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) auf (um auf eine vorhandene vertrauenswürdige Domäne zu zugreifen). Beide Funktionen legen einen Zeiger auf ein [**LSA \_ HANDLE**](lsa-handle.md)fest, das Sie dann in nachfolgenden LSA Policy-Funktionsaufrufen angeben können. Wie bei [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)sollte Ihre Anwendung [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) aufrufen, wenn sie das Handle für das Policy-Objekt der vertrauenswürdigen **Domäne nicht mehr** benötigt.

 

 

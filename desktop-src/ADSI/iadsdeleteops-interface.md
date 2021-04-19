---
title: Iadsdeleteops-Schnittstelle
description: Die iadsdeleteops-Schnittstelle wird in Aufsichts-und Wartungsroutinen für den zugrunde liegenden Verzeichnis Speicher verwendet. Es können Blattobjekte und gesamte Teil Strukturen in einem einzelnen Vorgang gelöscht werden.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- Iadsdeleteops-Schnittstelle ADSI
- Iadsdeleteops ADSI, using
- ADSI ADSI, Beispielcode C/C++, verwenden von iadsdeleteops zum Löschen ganzer Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd28e903996e8688d6c6fc672df080822595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339179"
---
# <a name="iadsdeleteops-interface"></a>Iadsdeleteops-Schnittstelle

Die [**iadsdeleteops**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) -Schnittstelle wird in Aufsichts-und Wartungsroutinen für den zugrunde liegenden Verzeichnis Speicher verwendet. Es können Blattobjekte und gesamte Teil Strukturen in einem einzelnen Vorgang gelöscht werden.

Wenn diese Schnittstelle nicht unterstützt wird, würde das Löschen eines Objekts aus Active Directory erfordern, dass jedes enthaltene Objekt rekursiv aufgezählt und gelöscht wird. Mit dieser Schnittstelle können alle Containerobjekte mit allen darin enthaltenen Objekten und untergeordneten Elementen mit einem einzelnen Vorgang gelöscht werden.

Im folgenden Codebeispiel werden der Container "eng" und alle untergeordneten Objekte gelöscht.


```C++
HRESULT hr;
IADsDeleteOps *pDeleteOps;
LPWSTR pwszUsername = NULL;
LPWSTR pwszPassword = NULL;

// Insert code to securely retrieve the pwszUsername and pwszPassword
// or leave as NULL to use the default security context of the 
// calling application.
 
// Bind to the LDAP provider.
hr = ADsOpenObject(L"LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com", 
    pwszUsername,
    pwszPassword,
    0,
    ADS_SECURE_AUTHENTICATION,
    IID_IADsDeleteOps, 
    (void**)&pDeleteOps);
if(S_OK == hr)
{
    // Delete the container and all child objects.
    pDeleteOps->DeleteObject(0);

    // Release the interface.
    pDeleteOps->Release();
}

if(pwszUsername)
{
    SecureZeroMemory(pwszUsername, lstrlen(pwszUsername) * sizeof(TCHAR));
}
if(pwszPassword)
{
    SecureZeroMemory(pwszPassword, lstrlen(pwszPassword) * sizeof(TCHAR));
}
```



Im folgenden Codebeispiel werden der Container "eng" und alle untergeordneten Objekte gelöscht.


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 





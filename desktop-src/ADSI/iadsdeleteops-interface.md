---
title: IADsDeleteOps-Schnittstelle
description: Die IADsDeleteOps-Schnittstelle wird in Überwachungs- und Wartungsroutinen für den zugrunde liegenden Verzeichnisspeicher verwendet. Sie kann Blattobjekte und ganze Teilstrukturen in einem einzigen Vorgang löschen.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- IADsDeleteOps Interface ADSI
- IADsDeleteOps ADSI mit
- ADSI ADSI , Beispielcode C/C++, mit IADsDeleteOps zum Löschen ganzer Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192411e53f54de2a5f73cc043f35cea6787f4b879972b6a69ada4760c175292a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839943"
---
# <a name="iadsdeleteops-interface"></a>IADsDeleteOps-Schnittstelle

Die [**IADsDeleteOps-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) wird in Überwachungs- und Wartungsroutinen für den zugrunde liegenden Verzeichnisspeicher verwendet. Sie kann Blattobjekte und ganze Teilstrukturen in einem einzigen Vorgang löschen.

Wenn diese Schnittstelle nicht unterstützt wird, erfordert das Löschen eines Objekts aus Active Directory, dass jedes enthaltene Objekt rekursiv aufzählt und gelöscht wird. Mit dieser Schnittstelle kann jedes Containerobjekt mit allen enthaltenen Objekten und Unterobjekten mit einem einzigen Vorgang gelöscht werden.

Im folgenden Codebeispiel werden der Container "Eng" und alle untergeordneten Objekte gelöscht.


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



Im folgenden Codebeispiel werden der Container "Eng" und alle untergeordneten Objekte gelöscht.


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 





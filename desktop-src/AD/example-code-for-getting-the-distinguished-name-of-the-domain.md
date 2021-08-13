---
title: Beispielcode zum Abrufen des Distinguished Name der Domäne
description: Dieses Thema enthält ein Codebeispiel, das den Distinguished Name der Domäne, zu der der lokale Computer gehört, mithilfe einer serverlosen Bindung ruft.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Beispiele: Active Directory, Abrufen des Distinguished Name der Domäne'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ebf027e6c95915e34b70f942fdbf342b3f49b9695d7885c442f015d2a74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693644"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Beispielcode zum Abrufen des Distinguished Name der Domäne

Dieses Thema enthält ein Codebeispiel, das den Distinguished Name der Domäne, zu der der lokale Computer gehört, mithilfe einer serverlosen Bindung ruft.

Im folgenden Visual Basic Codebeispiel wird der Distinguished Name der Domäne, zu der der lokale Computer gehört, mithilfe einer serverlosen Bindung ruft.


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



Im folgenden C#-Codebeispiel wird der Distinguished Name der Domäne, zu der der lokale Computer gehört, mithilfe einer serverlosen Bindung ruft.


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



Im folgenden C/C++-Codebeispiel wird der Distinguished Name der Domäne, zu der der lokale Computer gehört, mithilfe einer serverlosen Bindung ruft.


```C++
IADs *pads;
hr = ADsGetObject(  L"LDAP://rootDSE",
                    IID_IADs, 
                    (void**)&pads);

if(SUCCEEDED(hr))
{
    VARIANT var;

    VariantInit(&var);
    
    hr = pads->Get(CComBSTR("defaultNamingContext"), &var);
    if(SUCCEEDED(hr))
    {
        if(VT_BSTR == var.vt)
        {
            wprintf(var.bstrVal);
        }
        
        VariantClear(&var);
    }
    
    pads->Release();
}
```



 

 





---
title: Beispiel Code zum erhalten des Distinguished Name der Domäne
description: Dieses Thema enthält ein Codebeispiel, in dem der Distinguished Name der Domäne, in der der lokale Computer Mitglied ist, mithilfe der Server losen Bindung abgerufen wird.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, um den Distinguished Name der Domäne zu erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4badd8cd356ce5adfb20470a969e6f7444c010a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206269"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Beispiel Code zum erhalten des Distinguished Name der Domäne

Dieses Thema enthält ein Codebeispiel, in dem der Distinguished Name der Domäne, in der der lokale Computer Mitglied ist, mithilfe der Server losen Bindung abgerufen wird.

Im folgenden Visual Basic Codebeispiel wird der Distinguished Name der Domäne, in der der lokale Computer Mitglied ist, mithilfe der Server losen Bindung abgerufen.


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



Im folgenden c#-Codebeispiel wird der Distinguished Name der Domäne, in der der lokale Computer Mitglied ist, mithilfe der Server losen Bindung abgerufen.


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



Im folgenden C/C++-Codebeispiel wird der Distinguished Name der Domäne, in der der lokale Computer Mitglied ist, mithilfe der Server losen Bindung abgerufen.


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



 

 





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
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a><span data-ttu-id="9d5b1-104">Beispiel Code zum erhalten des Distinguished Name der Domäne</span><span class="sxs-lookup"><span data-stu-id="9d5b1-104">Example Code for Getting the Distinguished Name of the Domain</span></span>

<span data-ttu-id="9d5b1-105">Dieses Thema enthält ein Codebeispiel, in dem der Distinguished Name der Domäne, in der der lokale Computer Mitglied ist, mithilfe der Server losen Bindung abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9d5b1-105">This topic includes a code example that gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>

<span data-ttu-id="9d5b1-106">Im folgenden Visual Basic Codebeispiel wird der Distinguished Name der Domäne, in der der lokale Computer Mitglied ist, mithilfe der Server losen Bindung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d5b1-106">The following Visual Basic code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



<span data-ttu-id="9d5b1-107">Im folgenden c#-Codebeispiel wird der Distinguished Name der Domäne, in der der lokale Computer Mitglied ist, mithilfe der Server losen Bindung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d5b1-107">The following C# code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



<span data-ttu-id="9d5b1-108">Im folgenden C/C++-Codebeispiel wird der Distinguished Name der Domäne, in der der lokale Computer Mitglied ist, mithilfe der Server losen Bindung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d5b1-108">The following C/C++ code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


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



 

 





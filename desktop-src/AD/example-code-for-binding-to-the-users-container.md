---
title: Beispiel Code für die Bindung an den Container des Benutzers
description: Dieses Thema enthält ein Codebeispiel, das an den Benutzer Container in der aktuellen Domäne gebunden wird und die IADsContainer-Schnittstelle für den Container zurückgibt.
ms.assetid: 78524b05-f57a-4816-92eb-e37be74dd245
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, binden an den Container des Benutzers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db1ccb3d2331c4ccef5bbf28f58fa5c046337c7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038759"
---
# <a name="example-code-for-binding-to-the-users-container"></a>Beispiel Code für die Bindung an den Container des Benutzers

Im folgenden C++-Codebeispiel wird an den Benutzer Container in der aktuellen Domäne gebunden, und es wird die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle für den Container zurückgegeben. Weitere Informationen zum Binden an bekannte Objekte finden [Sie unterbinden an Well-Known Objekte mithilfe von wkguid](binding-to-well-known-objects-using-wkguid.md).


```C++
//**********************************************************
//
//  GetUsersContainer()
//
//  Binds to the well-known Users container in the current domain 
//  with the current user credentials. GUID_USERS_CONTAINER_W is 
//  defined in NTDSAPI.H.
//
//*******************************************************************

HRESULT GetUsersContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + 
                           wcslen(GUID_USERS_CONTAINER_W) + 
                           wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, 
                         pwszFormat, 
                         GUID_USERS_CONTAINER_W,
                         var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}
```



 

 
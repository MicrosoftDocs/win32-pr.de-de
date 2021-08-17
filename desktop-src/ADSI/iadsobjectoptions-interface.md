---
title: IADsObjectOptions-Schnittstelle
description: Die IADsObjectOptions-Schnittstelle ermöglicht den direkten Zugriff auf das Festlegen und Abrufen anbieterspezifischer Optionen.
ms.assetid: b4ac114f-1a23-4be6-af02-0c0d34a8f78f
ms.tgt_platform: multiple
keywords:
- IADsObjectOptions-Schnittstelle ADSI
- IADsObjectOptions ADSI mit
- ADSI ADSI , Beispielcode C/C++ mit IADsObjectOptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43701b4b846e4bf4e69dc8882397b5aba6b19ffc370ba418a34239782433073f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839923"
---
# <a name="iadsobjectoptions-interface"></a>IADsObjectOptions-Schnittstelle

Die [**IADsObjectOptions-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) ermöglicht den direkten Zugriff auf das Festlegen und Abrufen anbieterspezifischer Optionen.

Eine der Active Directory-Objektoptionen besteht in der Rückgabe des Hostnamens eines Servers. Im folgenden Codebeispiel wird die -Schnittstelle verwendet, um den Hostnamen des globalen Katalogservers abzurufen.


```C++
HRESULT GetGCServerName(VARIANT *vGCServer) 
{
    HRESULT hr = S_OK
    HRESULT hre = S_OK;
    IADsContainer *pContainer = NULL;
    IUnknown *pUnk = NULL;
    IEnumVARIANT *pEnum = NULL;
    IDispatch *pDisp = NULL;
    IADsObjectOptions *pOpt = NULL;
    VARIANT var;
    ULONG lFetch = 0;

    VariantInit(&var);
 
    // Bind to the global catalog using a serverless bind.
    hr = ADsOpenObject(L"GC:", NULL, NULL,
                       ADS_SECURE_AUTHENTICATION,
                       IID_IADsContainer, (void**) &pContainer );
    if (FAILED(hr))
        return (hr);
 
    hr = pContainer->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void**) &pEnum);
        if (SUCCEEDED(hr))
        {
            // Enumerate.
            hr = pEnum->Next(1, &var, &lFetch);
            if (SUCCEEDED(hr))
            {
                while (SUCCEEDED(hr))
                {
                    if (lFetch == 1)
                    {
                        pDisp = V_DISPATCH(&var);
                        hre = pDisp->QueryInterface(
                                          IID_IADsObjectOptions,
                                          (void**)&pOpt);
                        if (pDisp)
                            pDisp->Release();
                    }
                    VariantClear(&var);
                    hr = pEnum->Next(1, &var, &lFetch);
                }
                // S_FALSE indicates that the row was read properly.
                if (hr == S_FALSE)
                    hr = hre;
            }
 
            if (SUCCEEDED(hr))
            {
                // There is a valid pOpt, so request the server name.
                VariantInit(vGCServer);
                hr = pOpt->GetOption(ADS_OPTION_SERVERNAME,vGCServer);
            }
        }
    }
 
// Cleanup.
    VariantClear(&var);
    if (pOpt)
        pOpt->Release();
    if (pEnum)
        pEnum->Release();
    if (pUnk)
        pUnk->Release();
    if (pContainer)
        pContainer->Release();
    return (hr);
}
```



 

 





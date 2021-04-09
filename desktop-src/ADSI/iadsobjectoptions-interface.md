---
title: Iadsobjectoptions-Schnittstelle
description: Die iadsobjectoptions-Schnittstelle ermöglicht den direkten Zugriff auf das Festlegen und Abrufen von anbieterspezifischen Optionen.
ms.assetid: b4ac114f-1a23-4be6-af02-0c0d34a8f78f
ms.tgt_platform: multiple
keywords:
- Iadsobjectoptions-Schnittstelle ADSI
- Iadsobjectoptions ADSI, using
- ADSI ADSI, Beispielcode C/C++, using iadsobjectoptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049d4dee7f6bf2e7ebb61f01f42ef9fc39271c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947339"
---
# <a name="iadsobjectoptions-interface"></a><span data-ttu-id="80525-106">Iadsobjectoptions-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="80525-106">IADsObjectOptions Interface</span></span>

<span data-ttu-id="80525-107">Die [**iadsobjectoptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) -Schnittstelle ermöglicht den direkten Zugriff auf das Festlegen und Abrufen von anbieterspezifischen Optionen.</span><span class="sxs-lookup"><span data-stu-id="80525-107">The [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) interface enables direct access to setting and retrieving provider-specific options.</span></span>

<span data-ttu-id="80525-108">Eine der Active Directory Objekt Optionen besteht darin, den Hostnamen eines Servers zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="80525-108">One of the Active Directory object options is to return the host name of a server.</span></span> <span data-ttu-id="80525-109">Im folgenden Codebeispiel wird die-Schnittstelle verwendet, um den Hostnamen des globalen Katalog Servers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="80525-109">The following code example uses the interface to retrieve the host name of the global catalog server.</span></span>


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



 

 





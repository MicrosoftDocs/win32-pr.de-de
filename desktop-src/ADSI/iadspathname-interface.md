---
title: IADsPathname-Schnittstelle
description: Analysiert und ändert verschiedene Elemente eines ADsPath.
ms.assetid: 1f820488-2e75-4257-90c7-9ec67aac4fe4
ms.tgt_platform: multiple
keywords:
- IADsPathname-Schnittstelle ADSI
- IADsPathname ADSI mit
- ADSI ADSI , Beispielcode C/C++ mit IADsPathname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a87e64a5afabf0e7fc1fa760ec43c8ba4113fd9f39e90e42f77c307f6e6f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179523"
---
# <a name="iadspathname-interface"></a>IADsPathname-Schnittstelle

Die [**IADsPathname-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadspathname) analysiert und ändert verschiedene Elemente eines ADsPath. Außerdem werden ADsPaths zwischen verschiedenen Anzeigeformaten konvertiert.

Im folgenden Codebeispiel wird der Servername aus einem gültigen ADsPath extrahiert und zurückgegeben, damit er dem Benutzer in einem Wartungshilfsprogramm angezeigt wird.


```C++
HRESULT GetServerName(BSTR adsPath, BSTR *adsServer)
{
    HRESULT hr = S_OK;
    IADsPathname *pIADsPathname = NULL;
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
 
    // Set the path.
    hr = pIADsPathname->Set(adsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
        // Extract and return the server name.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_SERVER, adsServer);
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
}
```



Das folgende Codebeispiel hilft, ein neu erstelltes ADSI-Objekt zu initialisieren, indem die **Distinguished Name-Eigenschaft** des Objekts aus seinem eigenen ADsPath festgelegt wird. Beachten Sie, dass die aufrufende Routine alle Änderungen am zugrunde liegenden Verzeichnisspeicher committen muss, indem sie die **SetInfo-Methode** aufruft.


```C++
HRESULT SetDistinguishedName(IADs *pIADs)
{
    HRESULT hr = S_OK;
    CComBSTR sbstrADsPath;
    IADsPathname *pIADsPathname = NULL;
 
    // Get the ADsPath for this object.
    hr = pIADs->get_ADsPath(&sbstrADsPath);
    if (FAILED(hr))
        return (hr);
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
     // Set the path.
    hr = pIADsPathname->Set(sbstrADsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
    {
        CComBSTR sbstrDNPath;

        // Convert the path to Distinguished Name format.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,
                                     &sbstrDNPath);
 
        if (SUCCEEDED(hr))
        {
            // Set the distinguished name property.
            VARIANT var;
            VariantInit(&var);
            V_BSTR(&var) = sbstrDNPath;
            V_VT(&var) = VT_BSTR;
            hr = pIADs->Put(CComBSTR("distinguishedName"), var);
            VariantClear(&var);
        }
    }
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
 
}
```



 

 





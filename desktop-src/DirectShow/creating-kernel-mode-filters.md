---
description: Erstellen von Kernel-Mode Filtern
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Erstellen von Kernel-Mode Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473565046c462e8992350c3662360e4c22b3b5b75e10f0e79e1399885355056e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953939"
---
# <a name="creating-kernel-mode-filters"></a>Erstellen von Kernel-Mode Filtern

Bestimmte Kernelmodusfilter können nicht über **CoCreateInstance** erstellt werden und verfügen daher nicht über CLSIDs. Zu diesen Filtern gehören [tee/Sink-to-Sink Converter,](tee-sink-to-sink-converter.md)der [CC-Decoderfilter](cc-decoder-filter.md) und der [WST-Codecfilter.](wst-codec-filter.md) Um einen dieser Filter zu erstellen, verwenden Sie das [Systemgeräte-Enumeratorobjekt,](system-device-enumerator.md) und suchen Sie nach dem Namen des Filters.

1.  Erstellen Sie den Systemgeräte-Enumerator.
2.  Rufen Sie die [**ICreateDevEnum::CreateClassEnumerator-Methode**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit der CLSID der Filterkategorie für diesen Filter auf. Diese Methode erstellt einen Enumerator für die Filterkategorie. (Ein *Enumerator* ist einfach ein Objekt, das unter Verwendung einer definierten COM-Schnittstelle eine Liste anderer Objekte zurückgibt.) Der Enumerator gibt **IMoniker-Zeiger** zurück, die die Filter in dieser Kategorie darstellen.
3.  Rufen Sie für jeden Moniker **IMoniker::BindToStorage** auf, um eine **IPropertyBag-Schnittstelle** abzurufen.
4.  Rufen Sie **IPropertyBag::Read** auf, um den Namen des Filters abzurufen.
5.  Wenn der Name übereinstimmt, rufen **Sie IMoniker::BindToObject** auf, um den Filter zu erstellen.

Der folgende Code zeigt eine Funktion, die diese Schritte ausführt:


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



Im folgenden Codebeispiel wird diese Funktion verwendet, um den CC-Decoderfilter zu erstellen und dem Filterdiagramm hinzuzufügen:


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Themen zur erweiterten Erfassung](advanced-capture-topics.md)
</dt> <dt>

[Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




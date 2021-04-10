---
description: Erstellen von Kernel-Mode filtern
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Erstellen von Kernel-Mode filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c915a08312e33f0e35245325fd8bce7e55e486c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125414"
---
# <a name="creating-kernel-mode-filters"></a>Erstellen von Kernel-Mode filtern

Bestimmte kernelmodusfilter können nicht mithilfe von **cokreateinstance** erstellt werden und verfügen daher nicht über CLSIDs. Zu diesen Filtern gehören der " [Tee/Sink-to-Sink"-Konverter](tee-sink-to-sink-converter.md), der [CC-Decoderfilter](cc-decoder-filter.md) und der [WST-Codec](wst-codec-filter.md) -Filter. Verwenden Sie zum Erstellen eines dieser Filter das [System Geräte-Enumeratorobjekt](system-device-enumerator.md) , und suchen Sie nach dem Namen des Filters.

1.  Erstellen Sie den Enumerator für System Geräte.
2.  Aufrufen der [**ikreatedevenum:: feateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) -Methode mit der CLSID der Filterkategorie für diesen Filter. Diese Methode erstellt einen Enumerator für die Filterkategorie. (Ein *Enumerator* ist einfach ein Objekt, das mithilfe einer definierten COM-Schnittstelle eine Liste anderer Objekte zurückgibt.) Der Enumerator gibt **IMoniker** -Zeiger zurück, die die Filter in dieser Kategorie darstellen.
3.  Zum Abrufen einer **IPropertyBag** -Schnittstelle für jeden Moniker muss **IMoniker:: bindesstorage** aufgerufen werden.
4.  Aufrufen von **IPropertyBag:: Read** zum Abrufen des Namens des Filters.
5.  Wenn der Name übereinstimmt, rufen Sie **IMoniker:: bindjeobject** auf, um den Filter zu erstellen.

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



Im folgenden Codebeispiel wird diese Funktion verwendet, um den CC-Decoderfilter zu erstellen und dem Filter Diagramm hinzuzufügen:


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

[Erweiterte Erfassungs Themen](advanced-capture-topics.md)
</dt> <dt>

[Verwenden des Enumerators für System Geräte](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




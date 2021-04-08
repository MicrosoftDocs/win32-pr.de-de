---
description: Verwenden des Filter Mappers
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Verwenden des Filter Mappers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d7acf85a7b415fc161cd21e17d069b46c3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866452"
---
# <a name="using-the-filter-mapper"></a>Verwenden des Filter Mappers

Der [Filter Mapper](filter-mapper.md) ist ein COM-Objekt, das DirectShow-Filter auf der Grundlage verschiedener Suchkriterien auflistet. Der Filter Mapper kann weniger effizient sein als der Enumerator des System Geräts. Wenn Sie also Filter aus einer bestimmten Kategorie benötigen, sollten Sie den Enumerator des System Geräts verwenden. Wenn Sie jedoch einen Filter suchen müssen, der eine bestimmte Kombination von Medientypen unterstützt, aber nicht in eine Kategorie mit klarer Ausschneiden fällt, müssen Sie möglicherweise den Filter Mapper verwenden. (Ein Beispiel wäre ein rendererfilter oder ein Decoderfilter.)

Der Filter Mapper macht die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle verfügbar. Um nach einem Filter zu suchen, wird die [**IFilterMapper2:: enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode aufgerufen. Diese Methode nimmt mehrere Parameter an, die die Suchkriterien definieren, und gibt einen Enumerator für die übereinstimmenden Filter zurück. Der Enumerator unterstützt die [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) -Schnittstelle und stellt einen eindeutigen Moniker für jeden übereinstimmenden Filter bereit.

Im folgenden Beispiel werden Filter aufgelistet, die die Eingabe von digitalen Videos (DV) akzeptieren und mindestens eine Ausgabe-PIN eines beliebigen Medientyps aufweisen. (Der [DV-Video Decoder](dv-video-decoder-filter.md) -Filter entspricht diesen Kriterien.)


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



Die [**enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode verfügt über eine relativ große Anzahl von Parametern, die im Beispiel kommentiert werden. Die wichtigsten für dieses Beispiel sind:

-   Minimalwert: der Filter muss über einen Wert verfügen, der über einen Wert verfügt, der \_ \_ nicht \_ verwendet wird.
-   Eingabetypen: der Aufrufer übergibt ein Array mit Paaren von Haupttypen und Untertypen. Nur Filter, die mindestens eines dieser Paare unterstützen, stimmen zu.
-   Exakte Entsprechung: bei einem Filter können **null** -Werte für den Haupttyp, den Untertyp, die PIN-Kategorie oder das Medium registriert werden. Wenn Sie keine genaue Übereinstimmung angeben, fungiert ein **null** -Wert als Platzhalter, der mit jedem von Ihnen angegebenen Wert übereinstimmt. Mit der exakten Übereinstimmung muss der Filter genau mit Ihren Kriterien übereinstimmen. Wenn Sie jedoch einen **null** -Parameter in den Suchkriterien angeben, fungiert er immer als Platzhalter-oder "kein Pflege"-Wert, der mit einem beliebigen Filter übereinstimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auflisten von Geräten und Filtern](enumerating-devices-and-filters.md)
</dt> <dt>

[Intelligent Connect](intelligent-connect.md)
</dt> </dl>

 

 

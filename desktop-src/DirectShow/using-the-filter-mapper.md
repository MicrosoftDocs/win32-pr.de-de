---
description: Verwenden der Filterzuordnung
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Verwenden der Filterzuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48758c40b97477200b4fab1215eaccac53823771add86d6a8b915370776495a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049611"
---
# <a name="using-the-filter-mapper"></a>Verwenden der Filterzuordnung

Die [Filterzuordnung ist](filter-mapper.md) ein COM-Objekt, das DirectShow-Filter basierend auf verschiedenen Suchkriterien auflistet. Der Filterzuordnungs-Enumerator kann weniger effizient sein als der Systemgeräte-Enumerator. Wenn Sie also Filter aus einer bestimmten Kategorie benötigen, sollten Sie den Systemgeräte-Enumerator verwenden. Wenn Sie jedoch einen Filter suchen müssen, der eine bestimmte Kombination von Medientypen unterstützt, aber nicht in eine Kategorie mit eindeutigen Ausschnitten fällt, müssen Sie möglicherweise die Filterzuordnung verwenden. (Ein Beispiel wäre ein Rendererfilter oder ein Decoderfilter.)

Der Filter-Mapper macht die [**IFilterMapper2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) verfügbar. Um nach einem Filter zu suchen, rufen Sie die [**IFilterMapper2::EnumMatchingFilters-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) auf. Diese Methode verwendet mehrere Parameter, die die Suchkriterien definieren, und gibt einen Enumerator für die übereinstimmenden Filter zurück. Der Enumerator unterstützt die [**IEnumMoniker-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ienummoniker) und stellt für jeden übereinstimmenden Filter einen eindeutigen Moniker bereit.

Im folgenden Beispiel werden Filter aufzählt, die Digitale Videoeingaben (DV) akzeptieren und mindestens einen Ausgabepin eines beliebigen Medientyps haben. (Der [DV-Videodecoder-Filter](dv-video-decoder-filter.md) entspricht diesen Kriterien.)


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



Die [**EnumMatchingFilters-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) verfügt über eine relativ große Anzahl von Parametern, die im Beispiel kommentiert werden. Die wichtigsten für dieses Beispiel sind:

-   Mindestwert: Der Filter muss einen Wert haben, der höher ist als DER WERT FÜR NICHT \_ \_ ZU \_ VERWENDEN.
-   Eingabetypen: Der Aufrufer übergibt ein Array, das Paare von Haupttypen und Untertypen enthält. Nur Filter, die mindestens eines dieser Paare unterstützen, werden übereinstimmen.
-   Genaue Übereinstimmung: Ein Filter kann **NULL-Werte** für Haupttyp, Untertyp, Pinkategorie oder Mittel registrieren. Sofern Sie keinen genauen Abgleich angeben, fungiert ein **NULL-Wert** als Platzhalter, der mit jedem von Ihnen angegebenen Wert abgleicht. Bei genauem Abgleich muss der Filter genau Ihren Kriterien entsprechen. Wenn Sie jedoch einen **NULL-Parameter** in den Suchkriterien angeben, fungiert er immer als Platzhalter- oder "nicht so wichtig"-Wert, der mit jedem Filter abgleicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzählen von Geräten und Filtern](enumerating-devices-and-filters.md)
</dt> <dt>

[Intelligente Verbinden](intelligent-connect.md)
</dt> </dl>

 

 

---
description: Arbeiten mit PIN-Kategorien
ms.assetid: 1ee648b3-8370-4e4d-b513-d998131512ee
title: Arbeiten mit PIN-Kategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac58fff91821477cca51e0613772e3e5763d4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360122"
---
# <a name="working-with-pin-categories"></a>Arbeiten mit PIN-Kategorien

Wenn Sie die für eine PIN mit einer bestimmten Pin-Kategorie durchsuchen möchten, können Sie die [**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Methode verwenden. Im folgenden Beispiel wird nach einer Video Vorschau-Pin gesucht:


```C++
int i = 0;
hr = pBuild->FindPin(
    pFilter,               // Pointer to a filter to search.
    PINDIR_OUTPUT,         // Which pin direction?
    &PIN_CATEGORY_PREVIEW, // Which category? (NULL means "any category")
    &MEDIATYPE_Video,      // What media type? (NULL means "any type")
    FALSE,                 // Must be connected?
    i,                     // Get the i'th matching pin (0 = first match)
    &pPin                  // Receives a pointer to the pin.
);
```



Der erste Parameter ist ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters. Mit den nächsten drei Parametern werden die Richtung, die PIN-Kategorie und der Medientyp angegeben. Der Wert **false** im fünften Parameter gibt an, dass die PIN entweder verbunden oder nicht verbunden sein kann. (Genaue Definitionen dieser Parameter finden Sie in der Dokumentation für die-Methode.) Wenn die Methode eine passende PIN findet, wird ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle im *ppin* -Parameter zurückgegeben.

Obwohl die [**findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Methode praktisch ist, können Sie auch Ihre eigenen Hilfsfunktionen schreiben, wenn Sie dies bevorzugen. Um die Kategorie einer PIN zu ermitteln, wenden Sie die Methode " [**ikspropertyset:: Get**](ikspropertyset-get.md) " an, wie im Thema [PIN-Eigenschaften Satz](pin-property-set.md)beschrieben.

Der folgende Code zeigt eine Hilfsfunktion, die überprüft, ob eine PIN mit einer angegebenen Kategorie übereinstimmt:


```C++
// Returns TRUE if a pin matches the specified pin category.

BOOL PinMatchesCategory(IPin *pPin, REFGUID Category)
{
    BOOL bFound = FALSE;

    IKsPropertySet *pKs = NULL;
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (SUCCEEDED(hr))
    {
        GUID PinCategory;
        DWORD cbReturned;
        hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
            &PinCategory, sizeof(GUID), &cbReturned);
        if (SUCCEEDED(hr) && (cbReturned == sizeof(GUID)))
        {
            bFound = (PinCategory == Category);
        }
        pKs->Release();
    }
    return bFound;
}
```



Das nächste Beispiel ist eine Funktion, die eine PIN nach Kategorie sucht, ähnlich der [**findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Methode:


```C++
// Finds the first pin that matches a specified pin category and direction.

HRESULT FindPinByCategory(
    IBaseFilter *pFilter, // Pointer to the filter to search.
    PIN_DIRECTION PinDir, // Direction of the pin.
    REFGUID Category,     // Pin category.
    IPin **ppPin)         // Receives a pointer to the pin.
{
    *ppPin = 0;

    HRESULT hr = S_OK;
    BOOL bFound = FALSE;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (hr = pEnum->Next(1, &pPin, 0), hr == S_OK)
    {
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            goto done;
        }
        if ((ThisPinDir == PinDir) && 
            PinMatchesCategory(pPin, Category))
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();   // The caller must release the interface.
            bFound = TRUE;
            break;
        }
        SafeRelease(&pPin);
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    if (SUCCEEDED(hr) && !bFound)
    {
        hr = E_FAIL;
    }
    return hr;
}
```



Der folgende Code verwendet die Previous-Funktion, um nach einer Videoport-PIN für einen Filter zu suchen:


```C++
IPin *pVP; 
hr = FindPinByCategory(pFilter, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT, &pVP);
if (SUCCEEDED(hr))
{
    // Use pVP ... 
    // Release when you are done.
    pVP->Release();
}
```



Weitere Informationen zu Eigenschafts Sätzen finden Sie in der Dokumentation zum [Windows-Treiberkit (WDK)](/windows-hardware/drivers/gettingstarted/) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungs Themen](advanced-capture-topics.md)
</dt> <dt>

[PIN-Eigenschaften Satz](pin-property-set.md)
</dt> <dt>

[DirectShow-Video Erfassungs Filter](directshow-video-capture-filters.md)
</dt> </dl>

 

 

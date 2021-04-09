---
description: Auflisten von Pins
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Auflisten von Pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322f1764c46c146d1b899c869d1708eac1f0427d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860235"
---
# <a name="enumerating-pins"></a>Auflisten von Pins

Filter unterstützen die [**ibasefilter:: enumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) -Methode, die die für den Filter verfügbaren Pins auflistet. Er gibt einen Zeiger auf die [**ienumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle zurück. Die [**iumumpins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) -Methode ruft [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstellen Zeiger ab.

Das folgende Beispiel zeigt eine Funktion, die eine PIN mit einer angegebenen Richtung (Eingabe oder Ausgabe) für einen angegebenen Filter eingibt. Er verwendet die [**Pin- \_ Richtungs**](/windows/win32/api/strmif/ne-strmif-pin_direction) Enumeration, um die PIN-Richtung anzugeben, und die [**IPin:: querydirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) -Methode, um die Richtung der einzelnen aufgelisteten PIN zu ermitteln. Wenn diese Funktion eine passende PIN findet, wird ein **IPin** -Schnittstellen Zeiger mit einem ausstehenden Verweis Zähler zurückgegeben. Der Aufrufer ist für das Freigeben der-Schnittstelle verantwortlich.


```C++
HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins  *pEnum = NULL;
    IPin       *pPin = NULL;
    HRESULT    hr;

    if (ppPin == NULL)
    {
        return E_POINTER;
    }

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        hr = pPin->QueryDirection(&PinDirThis);
        if (FAILED(hr))
        {
            pPin->Release();
            pEnum->Release();
            return hr;
        }
        if (PinDir == PinDirThis)
        {
            // Found a match. Return the IPin pointer to the caller.
            *ppPin = pPin;
            pEnum->Release();
            return S_OK;
        }
        // Release the pin for the next time through the loop.
        pPin->Release();
    }
    // No more pins. We did not find a match.
    pEnum->Release();
    return E_FAIL;  
}
```



Diese Funktion kann problemlos geändert werden, um die n-te PIN mit der angegebenen Richtung oder die *n*-te nicht verbundene Pin zurückzugeben. (Um herauszufinden, ob eine PIN mit einer anderen Pin verbunden ist, müssen Sie die [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) -Methode abrufen.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auflisten von Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Suchen einer nicht verbundenen PIN für einen Filter](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> <dt>

[PIN-Eigenschaften Satz](pin-property-set.md)
</dt> </dl>

 

 




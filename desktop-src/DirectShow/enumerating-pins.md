---
description: Aufzählen von Pins
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Aufzählen von Pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d772903321c71ab2c6d66f7cc46b7ca61b11f96a4bc17b13b8b2f8931d8eac5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748710"
---
# <a name="enumerating-pins"></a>Aufzählen von Pins

Filter unterstützen die [**IBaseFilter::EnumPins-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) die die im Filter verfügbaren Pins auflistet. Sie gibt einen Zeiger auf die [**IEnumPins-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) zurück. Die [**IEnumPins::Next-Methode**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) ruft [**IPin-Schnittstellenzeer**](/windows/desktop/api/Strmif/nn-strmif-ipin) ab.

Das folgende Beispiel zeigt eine Funktion, die eine Stecknadel mit einer bestimmten Richtung (Eingabe oder Ausgabe) in einem bestimmten Filter sucht. Sie verwendet die [**PIN \_ DIRECTION-Enumeration,**](/windows/win32/api/strmif/ne-strmif-pin_direction) um die Pinrichtung anzugeben, und die [**IPin::QueryDirection-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) um die Richtung der einzelnen aufgelisteten Stecknadeln zu finden. Wenn diese Funktion einen übereinstimmenden  Pin findet, gibt sie einen IPin-Schnittstellenzeiger mit einer ausstehenden Verweisanzahl zurück. Der Aufrufer ist für die Freigabe der Schnittstelle verantwortlich.


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



Diese Funktion kann problemlos so geändert werden, dass der n-te Pin in der angegebenen Richtung oder der n-th unconnected pin *(n-th-Stift* ohne Verbindung) zurück gibt. (Um herauszufinden, ob eine Stecknadel mit einem anderen Pin verbunden ist, rufen Sie die [**IPin::ConnectedTo-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) auf.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzählen von Objekten in einem Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Suchen einer nicht verbundenen Stecknadel in einem Filter](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> <dt>

[Pin-Eigenschaftssatz](pin-property-set.md)
</dt> </dl>

 

 




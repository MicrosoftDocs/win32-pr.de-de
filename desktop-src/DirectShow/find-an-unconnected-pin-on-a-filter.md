---
description: In diesem Thema wird beschrieben, wie Sie eine nicht verbundene PIN für einen Filter finden. Das Auffinden einer nicht verbundenen PIN ist nützlich, wenn Sie Filter verbinden.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Suchen einer nicht verbundenen PIN für einen Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee47b811c027161b70769cb04063d0e8214934a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041117"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a>Suchen einer nicht verbundenen PIN für einen Filter

In diesem Thema wird beschrieben, wie Sie eine nicht verbundene PIN für einen Filter finden. Das Auffinden einer nicht verbundenen PIN ist nützlich, wenn Sie Filter verbinden.

In einem typischen Szenario für die DirectShow-Diagramm Entwicklung benötigen Sie eine nicht verbundene PIN, die einer bestimmten Pin-Richtung (Eingabe oder Ausgabe) entspricht. Wenn Sie z. b. zwei Filter verbinden, verbinden Sie eine Ausgabe-PIN von einem Filter mit einer Eingabe-PIN des anderen Filters. Beide Pins müssen nicht verbunden sein, bevor Sie eine Verbindung herstellen.

Zuerst wird eine Funktion benötigt, die testet, ob eine PIN mit einer anderen Pin verbunden ist. Diese Funktion Ruft die [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) -Methode auf, um zu überprüfen, ob die PIN mit einer anderen Pin verbunden ist.


```C++
// Query whether a pin is connected to another pin.
//
// Note: This function does not return a pointer to the connected pin.

HRESULT IsPinConnected(IPin *pPin, BOOL *pResult)
{
    IPin *pTmp = NULL;
    HRESULT hr = pPin->ConnectedTo(&pTmp);
    if (SUCCEEDED(hr))
    {
        *pResult = TRUE;
    }
    else if (hr == VFW_E_NOT_CONNECTED)
    {
        // The pin is not connected. This is not an error for our purposes.
        *pResult = FALSE;
        hr = S_OK;
    }

    SafeRelease(&pTmp);
    return hr;
}
```



> [!Note]  
> In diesem Beispiel wird die Funktion " [saferelease](/windows/desktop/medfound/saferelease) " verwendet, um Schnittstellen Zeiger freizugeben.

 

Als nächstes benötigen wir eine Funktion, die testet, ob eine PIN einer angegebenen Pin-Richtung entspricht. Diese Funktion Ruft die [**IPin:: querydirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) -Methode auf, um die PIN-Richtung zu erhalten.


```C++
// Query whether a pin has a specified direction (input / output)
HRESULT IsPinDirection(IPin *pPin, PIN_DIRECTION dir, BOOL *pResult)
{
    PIN_DIRECTION pinDir;
    HRESULT hr = pPin->QueryDirection(&pinDir);
    if (SUCCEEDED(hr))
    {
        *pResult = (pinDir == dir);
    }
    return hr;
}
```



Die Next-Funktion entspricht einer PIN nach Kriterien (PIN-Richtung und Verbindungsstatus).


```C++
// Match a pin by pin direction and connection state.
HRESULT MatchPin(IPin *pPin, PIN_DIRECTION direction, BOOL bShouldBeConnected, BOOL *pResult)
{
    assert(pResult != NULL);

    BOOL bMatch = FALSE;
    BOOL bIsConnected = FALSE;

    HRESULT hr = IsPinConnected(pPin, &bIsConnected);
    if (SUCCEEDED(hr))
    {
        if (bIsConnected == bShouldBeConnected)
        {
            hr = IsPinDirection(pPin, direction, &bMatch);
        }
    }

    if (SUCCEEDED(hr))
    {
        *pResult = bMatch;
    }
    return hr;
}
```



Die folgende Funktion verwendet die [**ienumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle zum Durchlaufen der Pins für den Filter. Der Aufrufer gibt die gewünschte Pin-Richtung an. Für jede Pin Ruft die Funktion `MatchPin` auf, um zu überprüfen, ob die PIN eine Entsprechung ist. Wenn die Richtung übereinstimmt und die PIN nicht verbunden ist, gibt die Funktion einen Zeiger auf die passende PIN im *pppin* -Parameter zurück.


```C++
// Return the first unconnected input pin or output pin.
HRESULT FindUnconnectedPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    BOOL bFound = FALSE;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = MatchPin(pPin, PinDir, FALSE, &bFound);
        if (FAILED(hr))
        {
            goto done;
        }
        if (bFound)
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();
            break;
        }
        SafeRelease(&pPin);
    }

    if (!bFound)
    {
        hr = VFW_E_NOT_FOUND;
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    return hr;
}
```



Ein Beispiel für die Verwendung dieser Funktion finden Sie unter Verbinden von [zwei Filtern](connect-two-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auflisten von Pins](enumerating-pins.md)
</dt> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 

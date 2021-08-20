---
description: In diesem Thema wird beschrieben, wie sie einen nicht verbundenen Pin in einem Filter finden. Das Suchen einer nicht verbundenen Stecknadel ist nützlich, wenn Sie Filter verbinden.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Suchen einer nicht verbundenen Stecknadel in einem Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a76100622f0398c58eb10f2dda041ba074f4610efbd1c649d48199ea2c676eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401754"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a>Suchen einer nicht verbundenen Stecknadel in einem Filter

In diesem Thema wird beschrieben, wie sie einen nicht verbundenen Pin in einem Filter finden. Das Suchen einer nicht verbundenen Stecknadel ist nützlich, wenn Sie Filter verbinden.

In einem typischen DirectShow-Diagramm-Erstellen-Szenario benötigen Sie einen nicht verbundenen Pin, der einer bestimmten Pinrichtung (Eingabe oder Ausgabe) entspricht. Wenn Sie beispielsweise zwei Filter verbinden, verbinden Sie einen Ausgabepin von einem Filter mit einem Eingabepin aus dem anderen Filter. Beide Stecknadeln müssen nicht verbunden sein, bevor Sie sie verbinden.

Zunächst benötigen wir eine Funktion, die testet, ob eine Stecknadel mit einem anderen Pin verbunden ist. Diese Funktion ruft die [**IPin::ConnectedTo-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) auf, um zu testen, ob die Stecknadel mit einem anderen Pin verbunden ist.


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
> In diesem Beispiel wird die [SafeRelease-Funktion verwendet,](/windows/desktop/medfound/saferelease) um Schnittstellenzeigener frei zu geben.

 

Als Nächstes benötigen wir eine Funktion, die testet, ob eine Stecknadel einer angegebenen Stecknadelrichtung entspricht. Diese Funktion ruft die [**IPin::QueryDirection-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) auf, um die Pinrichtung zu erhalten.


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



Die nächste Funktion entspricht einem Pin nach beiden Kriterien (Pinrichtung und Verbindungsstatus).


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



Schließlich verwendet die folgende Funktion die [**IEnumPins-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) um die Stecknadeln im Filter zu schleifen. Der Aufrufer gibt die gewünschte Pinrichtung an. Für jeden Pin ruft die Funktion auf, `MatchPin` um zu testen, ob der Pin eine Übereinstimmung ist. Wenn die Richtung stimmt und die Verbindung des Pins nicht hergestellt ist, gibt die Funktion einen Zeiger auf den entsprechenden Pin im *ppPin-Parameter* zurück.


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



Ein Beispiel für die Verwendung dieser Funktion finden Sie unter [Verbinden Zwei Filter.](connect-two-filters.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzählen von Pins](enumerating-pins.md)
</dt> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 

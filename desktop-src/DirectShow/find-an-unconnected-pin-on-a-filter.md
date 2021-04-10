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
# <a name="find-an-unconnected-pin-on-a-filter"></a><span data-ttu-id="cf375-104">Suchen einer nicht verbundenen PIN für einen Filter</span><span class="sxs-lookup"><span data-stu-id="cf375-104">Find an Unconnected Pin on a Filter</span></span>

<span data-ttu-id="cf375-105">In diesem Thema wird beschrieben, wie Sie eine nicht verbundene PIN für einen Filter finden.</span><span class="sxs-lookup"><span data-stu-id="cf375-105">This topic describes how to find an unconnected pin on a filter.</span></span> <span data-ttu-id="cf375-106">Das Auffinden einer nicht verbundenen PIN ist nützlich, wenn Sie Filter verbinden.</span><span class="sxs-lookup"><span data-stu-id="cf375-106">Finding an unconnected pin is useful when you are connecting filters.</span></span>

<span data-ttu-id="cf375-107">In einem typischen Szenario für die DirectShow-Diagramm Entwicklung benötigen Sie eine nicht verbundene PIN, die einer bestimmten Pin-Richtung (Eingabe oder Ausgabe) entspricht.</span><span class="sxs-lookup"><span data-stu-id="cf375-107">In a typical DirectShow graph-building scenario, you need an unconnected pin that matches a particular pin direction (input or output).</span></span> <span data-ttu-id="cf375-108">Wenn Sie z. b. zwei Filter verbinden, verbinden Sie eine Ausgabe-PIN von einem Filter mit einer Eingabe-PIN des anderen Filters.</span><span class="sxs-lookup"><span data-stu-id="cf375-108">For example, when you connect two filters, you connect an output pin from one filter to an input pin from the other filter.</span></span> <span data-ttu-id="cf375-109">Beide Pins müssen nicht verbunden sein, bevor Sie eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="cf375-109">Both pins must be unconnected before you connect them.</span></span>

<span data-ttu-id="cf375-110">Zuerst wird eine Funktion benötigt, die testet, ob eine PIN mit einer anderen Pin verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="cf375-110">First, we need a function that tests whether a pin is connected to another pin.</span></span> <span data-ttu-id="cf375-111">Diese Funktion Ruft die [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) -Methode auf, um zu überprüfen, ob die PIN mit einer anderen Pin verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="cf375-111">This function calls the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method to test whether the pin is connected to another pin.</span></span>


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
> <span data-ttu-id="cf375-112">In diesem Beispiel wird die Funktion " [saferelease](/windows/desktop/medfound/saferelease) " verwendet, um Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="cf375-112">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release interface pointers.</span></span>

 

<span data-ttu-id="cf375-113">Als nächstes benötigen wir eine Funktion, die testet, ob eine PIN einer angegebenen Pin-Richtung entspricht.</span><span class="sxs-lookup"><span data-stu-id="cf375-113">Next, we need a function that tests whether a pin matches a specified pin direction.</span></span> <span data-ttu-id="cf375-114">Diese Funktion Ruft die [**IPin:: querydirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) -Methode auf, um die PIN-Richtung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf375-114">This function calls the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to get the pin direction.</span></span>


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



<span data-ttu-id="cf375-115">Die Next-Funktion entspricht einer PIN nach Kriterien (PIN-Richtung und Verbindungsstatus).</span><span class="sxs-lookup"><span data-stu-id="cf375-115">The next function matches a pin by both criteria (pin direction and connection status).</span></span>


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



<span data-ttu-id="cf375-116">Die folgende Funktion verwendet die [**ienumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle zum Durchlaufen der Pins für den Filter.</span><span class="sxs-lookup"><span data-stu-id="cf375-116">Finally, the following function uses the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on the filter.</span></span> <span data-ttu-id="cf375-117">Der Aufrufer gibt die gewünschte Pin-Richtung an.</span><span class="sxs-lookup"><span data-stu-id="cf375-117">The caller specifies the desired pin direction.</span></span> <span data-ttu-id="cf375-118">Für jede Pin Ruft die Funktion `MatchPin` auf, um zu überprüfen, ob die PIN eine Entsprechung ist.</span><span class="sxs-lookup"><span data-stu-id="cf375-118">For each pin, the function calls `MatchPin` to test whether the pin is a match.</span></span> <span data-ttu-id="cf375-119">Wenn die Richtung übereinstimmt und die PIN nicht verbunden ist, gibt die Funktion einen Zeiger auf die passende PIN im *pppin* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="cf375-119">If the direction matches and the pin is unconnected, the function returns a pointer to the matching pin in the *ppPin* parameter.</span></span>


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



<span data-ttu-id="cf375-120">Ein Beispiel für die Verwendung dieser Funktion finden Sie unter Verbinden von [zwei Filtern](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="cf375-120">For an example of how this function can be used, see [Connect Two Filters](connect-two-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf375-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf375-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf375-122">Auflisten von Pins</span><span class="sxs-lookup"><span data-stu-id="cf375-122">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="cf375-123">Allgemeine Graph-Building Techniken</span><span class="sxs-lookup"><span data-stu-id="cf375-123">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="cf375-124">**ICaptureGraphBuilder2:: findpin**</span><span class="sxs-lookup"><span data-stu-id="cf375-124">**ICaptureGraphBuilder2::FindPin**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 

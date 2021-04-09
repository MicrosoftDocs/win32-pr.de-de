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
# <a name="enumerating-pins"></a><span data-ttu-id="40ae5-103">Auflisten von Pins</span><span class="sxs-lookup"><span data-stu-id="40ae5-103">Enumerating Pins</span></span>

<span data-ttu-id="40ae5-104">Filter unterstützen die [**ibasefilter:: enumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) -Methode, die die für den Filter verfügbaren Pins auflistet.</span><span class="sxs-lookup"><span data-stu-id="40ae5-104">Filters support the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method, which enumerates the pins available on the filter.</span></span> <span data-ttu-id="40ae5-105">Er gibt einen Zeiger auf die [**ienumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="40ae5-105">It returns a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="40ae5-106">Die [**iumumpins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) -Methode ruft [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstellen Zeiger ab.</span><span class="sxs-lookup"><span data-stu-id="40ae5-106">The [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method retrieves [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointers.</span></span>

<span data-ttu-id="40ae5-107">Das folgende Beispiel zeigt eine Funktion, die eine PIN mit einer angegebenen Richtung (Eingabe oder Ausgabe) für einen angegebenen Filter eingibt.</span><span class="sxs-lookup"><span data-stu-id="40ae5-107">The following example shows a function that locates a pin with a given direction (input or output) on a given filter.</span></span> <span data-ttu-id="40ae5-108">Er verwendet die [**Pin- \_ Richtungs**](/windows/win32/api/strmif/ne-strmif-pin_direction) Enumeration, um die PIN-Richtung anzugeben, und die [**IPin:: querydirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) -Methode, um die Richtung der einzelnen aufgelisteten PIN zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="40ae5-108">It uses the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration to specify the pin direction, and the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to find the direction of each enumerated pin.</span></span> <span data-ttu-id="40ae5-109">Wenn diese Funktion eine passende PIN findet, wird ein **IPin** -Schnittstellen Zeiger mit einem ausstehenden Verweis Zähler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40ae5-109">If this function finds a matching pin, it returns an **IPin** interface pointer with an outstanding reference count.</span></span> <span data-ttu-id="40ae5-110">Der Aufrufer ist für das Freigeben der-Schnittstelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="40ae5-110">The caller is responsible for releasing the interface.</span></span>


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



<span data-ttu-id="40ae5-111">Diese Funktion kann problemlos geändert werden, um die n-te PIN mit der angegebenen Richtung oder die *n*-te nicht verbundene Pin zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="40ae5-111">This function could easily be modified to return the nth pin with the specified direction, or the *n* th unconnected pin.</span></span> <span data-ttu-id="40ae5-112">(Um herauszufinden, ob eine PIN mit einer anderen Pin verbunden ist, müssen Sie die [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) -Methode abrufen.)</span><span class="sxs-lookup"><span data-stu-id="40ae5-112">(To find out if a pin is connected to another pin, call the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="40ae5-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40ae5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ae5-114">Auflisten von Objekten in einem Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="40ae5-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="40ae5-115">Suchen einer nicht verbundenen PIN für einen Filter</span><span class="sxs-lookup"><span data-stu-id="40ae5-115">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[<span data-ttu-id="40ae5-116">Allgemeine Graph-Building Techniken</span><span class="sxs-lookup"><span data-stu-id="40ae5-116">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="40ae5-117">PIN-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="40ae5-117">Pin Property Set</span></span>](pin-property-set.md)
</dt> </dl>

 

 




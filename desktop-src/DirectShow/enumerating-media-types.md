---
description: Auflisten von Medientypen
ms.assetid: 7878885f-c285-4744-8eab-445678dcfd49
title: Auflisten von Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3909c25e9ae5f90a3084eebb531431cc93ef46cd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351389"
---
# <a name="enumerating-media-types"></a><span data-ttu-id="c4e3f-103">Auflisten von Medientypen</span><span class="sxs-lookup"><span data-stu-id="c4e3f-103">Enumerating Media Types</span></span>

<span data-ttu-id="c4e3f-104">Pins unterstützen die [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode, die die bevorzugten Medientypen einer PIN auflistet.</span><span class="sxs-lookup"><span data-stu-id="c4e3f-104">Pins support the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method, which enumerates a pin's preferred media types.</span></span> <span data-ttu-id="c4e3f-105">Er gibt einen Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c4e3f-105">It returns a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="c4e3f-106">Die [**ienummediatypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) -Methode ruft Zeiger auf [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Strukturen ab, die Medientypen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c4e3f-106">The [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method retrieves pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures describing media types.</span></span>

<span data-ttu-id="c4e3f-107">Der Medientyp-Enumerator ist hauptsächlich vorhanden, um den Filter Graph-Manager beim Erstellen intelligenter Verbindungen zu unterstützen, und ihre Anwendungen verwenden ihn wahrscheinlich nicht.</span><span class="sxs-lookup"><span data-stu-id="c4e3f-107">The media type enumerator exists primarily to help the Filter Graph Manager make intelligent connections, and your applications will probably not use it.</span></span> <span data-ttu-id="c4e3f-108">Eine PIN gibt nicht notwendigerweise bevorzugte Medientypen zurück.</span><span class="sxs-lookup"><span data-stu-id="c4e3f-108">A pin does not necessarily return any preferred media types.</span></span> <span data-ttu-id="c4e3f-109">Darüber hinaus kann es sein, dass die zurückgegebenen Medientypen vom Verbindungsstatus des Filters abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c4e3f-109">Moreover, the media types it returns might depend on the filter's connection status.</span></span> <span data-ttu-id="c4e3f-110">Beispielsweise gibt die Ausgabepin eines Filters möglicherweise einen anderen Satz von Medientypen zurück, je nachdem, welcher Medientyp für die Eingabe-PIN des Filters festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c4e3f-110">For example, a filter's output pin might return a different set of media types depending on which media type was set for the filter's input pin.</span></span>

<span data-ttu-id="c4e3f-111">Im folgenden Beispiel wird ein bevorzugter Medientyp gefunden, der mit einem angegebenen Haupttyp, Untertyp oder Formattyp übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c4e3f-111">The following example finds a preferred media type that matches a specified major type, subtype, or format type.</span></span>


```C++
// Given a pin, find a preferred media type 
//
// pPin         Pointer to the pin.
// majorType    Preferred major type (GUID_NULL = don't care).
// subType      Preferred subtype (GUID_NULL = don't care).
// formatType   Preferred format type (GUID_NULL = don't care).
// ppmt         Receives a pointer to the media type. Can be NULL.
//
// Note: If you want to check whether a pin supports a desired media type,
//       but do not need the format details, set ppmt to NULL.
//
//       If ppmt is not NULL and the method succeeds, the caller must
//       delete the media type, including the format block. 

HRESULT GetPinMediaType(
    IPin *pPin,             // pointer to the pin
    REFGUID majorType,      // desired major type, or GUID_NULL = don't care
    REFGUID subType,        // desired subtype, or GUID_NULL = don't care
    REFGUID formatType,     // desired format type, of GUID_NULL = don't care
    AM_MEDIA_TYPE **ppmt    // Receives a pointer to the media type. (Can be NULL)
    )
{
    *ppmt = NULL;

    IEnumMediaTypes *pEnum = NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    BOOL bFound = FALSE;
    
    HRESULT hr = pPin->EnumMediaTypes(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    while (hr = pEnum->Next(1, &pmt, NULL), hr == S_OK)
    {
        if ((majorType == GUID_NULL) || (majorType == pmt->majortype))
        {
            if ((subType == GUID_NULL) || (subType == pmt->subtype))
            {
                if ((formatType == GUID_NULL) || 
                    (formatType == pmt->formattype))
                {
                    // Found a match. 
                    if (ppmt)
                    {
                        *ppmt = pmt;  // Return it to the caller
                    }
                    else
                    {
                        _DeleteMediaType(pmt);
                    }
                    bFound = TRUE;
                    break;
                }
            }
        }
        _DeleteMediaType(pmt);
    }

    SafeRelease(&pEnum);
    if (SUCCEEDED(hr))
    {
        if (!bFound)
        {
            hr = VFW_E_NOT_FOUND;
        }
    }
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="c4e3f-112">In diesem Beispiel wird die Funktion " [saferelease](/windows/desktop/medfound/saferelease) " verwendet, um Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c4e3f-112">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c4e3f-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4e3f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4e3f-114">Auflisten von Objekten in einem Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="c4e3f-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="c4e3f-115">**Ienummediatypes**</span><span class="sxs-lookup"><span data-stu-id="c4e3f-115">**IEnumMediaTypes**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)
</dt> </dl>

 

 

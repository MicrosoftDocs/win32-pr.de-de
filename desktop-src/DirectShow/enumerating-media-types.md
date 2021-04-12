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
# <a name="enumerating-media-types"></a>Auflisten von Medientypen

Pins unterstützen die [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode, die die bevorzugten Medientypen einer PIN auflistet. Er gibt einen Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle zurück. Die [**ienummediatypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) -Methode ruft Zeiger auf [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Strukturen ab, die Medientypen beschreiben.

Der Medientyp-Enumerator ist hauptsächlich vorhanden, um den Filter Graph-Manager beim Erstellen intelligenter Verbindungen zu unterstützen, und ihre Anwendungen verwenden ihn wahrscheinlich nicht. Eine PIN gibt nicht notwendigerweise bevorzugte Medientypen zurück. Darüber hinaus kann es sein, dass die zurückgegebenen Medientypen vom Verbindungsstatus des Filters abhängig sind. Beispielsweise gibt die Ausgabepin eines Filters möglicherweise einen anderen Satz von Medientypen zurück, je nachdem, welcher Medientyp für die Eingabe-PIN des Filters festgelegt wurde.

Im folgenden Beispiel wird ein bevorzugter Medientyp gefunden, der mit einem angegebenen Haupttyp, Untertyp oder Formattyp übereinstimmt.


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
> In diesem Beispiel wird die Funktion " [saferelease](/windows/desktop/medfound/saferelease) " verwendet, um Schnittstellen Zeiger freizugeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auflisten von Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[**Ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)
</dt> </dl>

 

 

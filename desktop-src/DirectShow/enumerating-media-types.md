---
description: Aufzählen von Medientypen
ms.assetid: 7878885f-c285-4744-8eab-445678dcfd49
title: Aufzählen von Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e2f063fc243d081b930a1bf47f85904dfbc2fc7eef00fb595d5f0fb3a451ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102800"
---
# <a name="enumerating-media-types"></a>Aufzählen von Medientypen

Pins unterstützen die [**IPin::EnumMediaTypes-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) die die bevorzugten Medientypen eines Pins aufzählt. Sie gibt einen Zeiger auf die [**IEnumMediaTypes-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) zurück. Die [**IEnumMediaTypes::Next-Methode**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) ruft Zeiger auf [**AM MEDIA \_ \_ TYPE-Strukturen**](/windows/win32/api/strmif/ns-strmif-am_media_type) ab, die Medientypen beschreiben.

Der Medientyp-Enumerator dient in erster Linie dazu, den Filter Graph Manager beim Herstellen intelligenter Verbindungen zu unterstützen, und Ihre Anwendungen verwenden ihn wahrscheinlich nicht. Ein Pin gibt nicht unbedingt bevorzugte Medientypen zurück. Darüber hinaus können die zurückgegebenen Medientypen vom Verbindungsstatus des Filters abhängen. Beispielsweise kann der Ausgabepin eines Filters einen anderen Satz von Medientypen zurückgeben, je nachdem, welcher Medientyp für den Eingabepin des Filters festgelegt wurde.

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
> In diesem Beispiel wird die [SafeRelease-Funktion](/windows/desktop/medfound/saferelease) verwendet, um Schnittstellenzeiger freizugeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzählen von Objekten in einem Filter Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)
</dt> </dl>

 

 

---
description: 'Schritt 3C:'
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: 'Schritt 3C: Implementieren der CheckTransform-Methode'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430ad933acfa7fc41a8b075183080e0b710a5d4780b55fa89cd4bf80984c1edc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075590"
---
# <a name="step-3c-implement-the-checktransform-method"></a>Schritt 3C: Implementieren der CheckTransform-Methode

Dies ist Schritt 3C des Tutorials [Schreiben von Transformationsfiltern.](writing-transform-filters.md)

> [!Note]  
> Dieser Schritt ist für Filter, die von **CTransInPlaceFilter** abgeleitet sind, nicht erforderlich.

 

Die [**CTransformFilter::CheckTransform-Methode**](ctransformfilter-checktransform.md) überprüft, ob ein vorgeschlagener Ausgabetyp mit dem aktuellen Eingabetyp kompatibel ist. Die -Methode wird auch aufgerufen, wenn der Eingabepin nach dem Herstellen der Verbindung mit dem Ausgabepin erneut eine Verbindung herstellt.

Im folgenden Beispiel wird überprüft, ob das Format RLE8-Video ist. Die Bilddimensionen entsprechen dem Eingabeformat. und die Paletteneinträge sind identisch. Außerdem werden Quell- und Zielrechtecke abgelehnt, die nicht mit der Bildgröße übereinstimmen.


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



**Stecknadelwiederherstellungen**

Anwendungen können Pins trennen und erneut verbinden. Angenommen, eine Anwendung verbindet beide Pins, trennt den Eingabepin und verbindet den Eingabepin dann mithilfe einer neuen Bildgröße erneut. In diesem Fall schlägt **CheckTransform** fehl, da die Abmessungen des Bilds nicht mehr übereinstimmen. Dieses Verhalten ist sinnvoll, obwohl der Filter auch versuchen könnte, den Ausgabepin mit einem neuen Medientyp erneut zu verbinden.

Weiter: [Schritt 4. Legen Sie Zuweisungseigenschaften](step-4--set-allocator-properties.md)fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erneutes Verbinden von Pins](reconnecting-pins.md)
</dt> <dt>

[Quell- und Zielrechtecke in Videorenderern](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 




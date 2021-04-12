---
description: 'Schritt 3C:'
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: 'Schritt 3C: Implementieren der checktransform-Methode'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78148701fc54e73a6970d45fde95d70f4cf0df3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218019"
---
# <a name="step-3c-implement-the-checktransform-method"></a>Schritt 3C: Implementieren der checktransform-Methode

Dies ist Schritt 3C des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).

> [!Note]  
> Dieser Schritt ist für Filter, die von **ctransinplacefilter** abgeleitet werden, nicht erforderlich.

 

Die [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode überprüft, ob ein vorgeschlagene Ausgabetyp mit dem aktuellen Eingabetyp kompatibel ist. Die-Methode wird auch aufgerufen, wenn die Eingabe-PIN erneut eine Verbindung herstellt, nachdem die PIN-Ausgabe Verbindung hergestellt

Im folgenden Beispiel wird überprüft, ob das Format RLE8 Video ist. die Bild Dimensionen entsprechen dem Eingabeformat. und die Paletteneinträge sind identisch. Sie lehnt auch Quell-und Ziel Rechtecke ab, die nicht mit der Bildgröße identisch sind.


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



**PIN-erneute Verbindungen**

Anwendungen können die PIN trennen und die Verbindung wiederherstellen. Angenommen, eine Anwendung verbindet beide Pins, trennt die eingabepin und verbindet die Eingabe-PIN dann erneut mit einer neuen Bildgröße. In diesem Fall schlägt **checktransform** fehl, da die Abmessungen des Bilds nicht mehr identisch sind. Dieses Verhalten ist sinnvoll, obwohl der Filter auch versuchen könnte, die Ausgabepin erneut mit einem neuen Medientyp zu verbinden.

Weiter: [Schritt 4. Legen Sie zuordnereigenschaften fest](step-4--set-allocator-properties.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PIN wird wieder hergestellt](reconnecting-pins.md)
</dt> <dt>

[Quell-und Ziel Rechtecke in Videorenderer](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 




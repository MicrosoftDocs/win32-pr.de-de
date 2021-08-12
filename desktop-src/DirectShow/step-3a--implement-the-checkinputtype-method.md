---
description: Schritt 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Schritt 3A. Implementieren der CheckInputType-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692175e0def453f86b618a355044e4a117a4343fed56f029704091134e8bc31f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652140"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Schritt 3A. Implementieren der CheckInputType-Methode

Dies ist Schritt 3A des Tutorials [Schreiben von Transformationsfiltern](writing-transform-filters.md).

Die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) wird aufgerufen, wenn der Upstreamfilter einen Medientyp für den Transformationsfilter vorschlägt. Diese Methode verwendet einen Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) bei dem es sich um einen schlanken Wrapper für die [**AM MEDIA \_ \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) handelt. Bei dieser Methode sollten Sie jedes relevante Feld der **AM \_ MEDIA \_ TYPE-Struktur** untersuchen, einschließlich der Felder im Formatblock. Sie können die in **CMediaType** definierten Accessormethoden verwenden oder direkt auf die Strukturmitglieder verweisen. Wenn ein Feld ungültig ist, geben Sie VFW \_ E TYPE NOT ACCEPTED \_ \_ \_ zurück. Wenn der gesamte Medientyp gültig ist, geben Sie S \_ OK zurück.

Im RLE-Encoderfilter muss der Eingabetyp beispielsweise ein 8-Bit- oder 4-Bit-unkomprimiertes RGB-Video sein. Es gibt keinen Grund, andere Eingabeformate wie 16- oder 24-Bit-RGB zu unterstützen, da der Filter sie in eine niedrigere Bittiefe konvertieren muss und DirectShow bereits einen [Color Space Converter-Filter](color-space-converter-filter.md) für diesen Zweck bietet. Im folgenden Beispiel wird davon ausgegangen, dass der Encoder 8-Bit-Videos unterstützt, aber kein 4-Bit-Video:


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



In diesem Beispiel überprüft die -Methode zuerst den Haupttyp und unteren Typ. Anschließend wird der Formattyp überprüft, um sicherzustellen, dass der Formatblock eine [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ist. Der Filter könnte auch [**VIDEOINFOHEADER2 unterstützen,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)aber in diesem Fall würde es keinen echten Vorteil geben. Die **VIDEOINFOHEADER2-Struktur** fügt Unterstützung für Interlacing und nicht quadratische Pixel hinzu, die in 8-Bit-Videos wahrscheinlich nicht relevant sind.

Wenn der Formattyp richtig ist, überprüft das Beispiel die **Member biBitCount** und **biCompression** der **VIDEOINFOHEADER-Struktur,** um sicherzustellen, dass das Format 8-Bit unkomprimiert RGB ist. Wie in diesem Beispiel gezeigt, müssen Sie die


```C++
pbFormat
```



Zeiger auf die richtige Struktur, basierend auf dem Formattyp. Überprüfen Sie immer den Formattyp GUID **(Formattyp**) und die Größe des Formatblocks (**cbFormat**), bevor Sie den Zeiger konvertieren.

Im Beispiel wird außerdem überprüft, ob die Anzahl der Paletteneinträge mit der Bittiefe kompatibel ist und der Formatblock groß genug ist, um die Paletteneinträge zu speichern. Wenn alle diese Informationen richtig sind, gibt die Methode S \_ OK zurück.

Weiter: [Schritt 3B. Implementieren sie die GetMediaType-Methode](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 




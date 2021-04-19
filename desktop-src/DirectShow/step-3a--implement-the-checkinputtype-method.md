---
description: Schritt 3a.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Schritt 3a. Implementieren der checkinputtype-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350035"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Schritt 3a. Implementieren der checkinputtype-Methode

Dies ist Schritt 3a des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).

Die [**ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md) -Methode wird aufgerufen, wenn der upstreamfilter einen Medientyp für den Transformations Filter vorschlägt. Diese Methode nimmt einen Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt an, bei dem es sich um einen dünnen Wrapper für die [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur von am handelt. In dieser Methode sollten Sie alle relevanten Felder der **am- \_ \_ Medientyp** Struktur untersuchen, einschließlich der Felder im Format Block. Sie können die in **cmediatype** definierten Accessor-Methoden verwenden oder direkt auf die Strukturmember verweisen. Wenn ein Feld ungültig ist, wird der Vfw \_ E- \_ Typ \_ nicht \_ akzeptiert. Wenn der gesamte Medientyp gültig ist, geben Sie S \_ OK zurück.

Beispielsweise muss im Filter des RLE-Encoders der Eingabetyp ein 8-Bit-oder ein 4-Bit-nicht komprimiertes RGB-Video sein. Es gibt keinen Grund, andere Eingabeformate (z. b. 16-oder 24-Bit-RGB) zu unterstützen, da der Filter Sie in eine niedrigere bidirektiontiefe konvertieren muss und DirectShow bereits einen [Farb Raum Konverter](color-space-converter-filter.md) -Filter für diesen Zweck bereitstellt. Im folgenden Beispiel wird davon ausgegangen, dass der Encoder ein 8-Bit-Video, aber kein 4-Bit-Video unterstützt:


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



In diesem Beispiel überprüft die-Methode zuerst den Haupttyp und den Untertyp. Anschließend wird der Formattyp überprüft, um sicherzustellen, dass der Format Block eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur ist. Der Filter kann auch [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)unterstützen, aber in diesem Fall würde es keinen echten Vorteil haben. Die **VIDEOINFOHEADER2** -Struktur fügt Unterstützung für das durchlaufen und nicht eckige Pixel hinzu, die in 8-Bit-Videos wahrscheinlich nicht relevant sind.

Wenn der Formattyp richtig ist, überprüft das Beispiel die Member **biBitCount** und **bicompression** der **videoinfoheader** -Struktur, um zu überprüfen, ob das Format 8-Bit-nicht komprimiertes RGB ist. Wie in diesem Beispiel gezeigt, müssen Sie das


```C++
pbFormat
```



Zeiger auf die richtige-Struktur, basierend auf dem Formattyp. Überprüfen Sie vor dem Umwandeln des Zeigers immer den Formattyp GUID (**Format Type**) und die Größe des Format Blocks (**cbformat**).

Im Beispiel wird außerdem überprüft, ob die Anzahl der Paletteneinträge mit der Bittiefe kompatibel ist und der Format Block groß genug ist, um die Paletteneinträge aufzunehmen. Wenn alle diese Informationen korrekt sind, gibt die Methode "S \_ OK" zurück.

Als nächstes: [Schritt 3B. implementieren Sie die getmediatype-Methode](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 




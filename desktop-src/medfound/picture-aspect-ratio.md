---
description: In diesem Thema werden zwei verwandte Konzepte, das Bildseiten Verhältnis und das Pixel Seitenverhältnis beschrieben.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Bildseiten Verhältnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215020"
---
# <a name="picture-aspect-ratio"></a>Bildseiten Verhältnis

In diesem Thema werden zwei verwandte Konzepte, das Bildseiten Verhältnis und das Pixel Seitenverhältnis beschrieben. Anschließend wird beschrieben, wie diese Konzepte in Microsoft Media Foundation mithilfe von Medientypen ausgedrückt werden.

-   [Bildseiten Verhältnis](#picture-aspect-ratio)
    -   [Letterbox](#letterboxing)
    -   [Schwenken und überprüfen](#pan-and-scan)
-   [Pixel Seitenverhältnis](#pixel-aspect-ratio)
-   [Arbeiten mit Seitenverhältnissen](#working-with-aspect-ratios)
-   [Code Beispiele](#code-examples)
    -   [Suchen des Anzeige Bereichs](#finding-the-display-area)
    -   [Zwischen Pixel-Seitenverhältnissen](#converting-between-pixel-aspect-ratios)
    -   [Berechnen des Bereichs "Briefkasten"](#calculating-the-letterbox-area)
-   [Zugehörige Themen](#related-topics)

## <a name="picture-aspect-ratio"></a>Bildseiten Verhältnis

*Bildseiten Verhältnis* definiert die Form des angezeigten Video Bilds. Das Seitenverhältnis des Bilds ist als "x:y" gekennzeichnet, wobei "x:y" das Verhältnis der Bildbreite zur Bildhöhe ist. Bei den meisten Videostandards wird das Seitenverhältnis von 4:3 oder 16:9 verwendet. Das 16:9-Seitenverhältnis wird häufig als " *Breitbild*" bezeichnet. Der Kino Film verwendet häufig ein Seitenverhältnis von 1:85:1 oder 1:66:1. Das Seitenverhältnis des Bilds wird auch als *Seitenverhältnis anzeigen* bezeichnet.

![Diagramm, das 4:3-und 16:9-Seitenverhältnisse anzeigt](images/aspect-ratio01.png)

Manchmal hat das Video Bild nicht dieselbe Form wie der Anzeigebereich. Beispielsweise kann ein 4:3-Video in einem Breitbild (16 × 9) angezeigt werden. In Computer Videos wird das Video möglicherweise in einem Fenster angezeigt, das eine beliebige Größe aufweist. In diesem Fall gibt es drei Möglichkeiten, wie das Bild im Anzeigebereich angepasst werden kann:

-   Strecken Sie das Bild entlang einer Achse, sodass es an den Anzeigebereich angepasst ist.
-   Skalieren Sie das Bild so, dass es in den Anzeigebereich passt, während Sie das ursprüngliche Bildseiten Verhältnis beibehalten.
-   Zuschneiden des Bilds.

Das Strecken des Bilds an den Anzeigebereich ist fast immer falsch, da es das richtige Bildseiten Verhältnis nicht beibehält.

### <a name="letterboxing"></a>Letterbox

Der Prozess der Skalierung eines Bildschirm Bilds an eine 4:3-Anzeige wird im nächsten Diagramm als *Letterbox* bezeichnet. Die resultierenden rechteckigen Bereiche am oberen und unteren Rand des Bilds sind in der Regel mit schwarz gefüllt, auch wenn andere Farben verwendet werden können.

![Diagramm mit der korrekten Methode zum Briefkasten](images/aspect-ratio02.png)

Der umgekehrte Fall, das Skalieren eines 4:3-Bilds an eine Bildschirm Abbildung zeigt, wird manchmal als *Pillarboxing* bezeichnet. Der Begriff " *Letterbox* " wird jedoch auch allgemein verwendet, um ein Video Bild so zu skalieren, dass es an einen beliebigen Anzeigebereich angepasst wird.

![Diagramm mit Pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>Schwenken und überprüfen

"Pan-and-Scan" ist ein Verfahren, bei dem ein Breitbild auf einen vier × 3-rechteckigen Bereich zugeschnitten wird, um auf einem 4:3-Display Gerät angezeigt zu werden. Das resultierende Bild füllt die gesamte Anzeige aus, ohne dass schwarze Letterbox-Bereiche erforderlich sind, aber Teile des ursprünglichen Bilds werden aus dem Bild herausgeschnitten. Der Bereich, der zugeschnitten wird, kann sich von Frame zu Frame bewegen, während sich der Bereich des Interesses verschiebt. Der Begriff "Pan" in "Pan *-and-Scan* " bezieht sich auf den Schwenk Effekt, der durch das Verschieben des Bereichs "schwenken" und "Scannen" verursacht wird.

![Diagramm mit Pan-and-Scan](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>Pixel Seitenverhältnis

*Pixel Seitenverhältnis* (par) misst die Form eines Pixels.

Wenn ein digitales Bild aufgezeichnet wird, wird das Bild sowohl vertikal als auch horizontal entnommen. Dies führt zu einem rechteckigen Array von quantifizierten Beispielen, die als *Pixel* oder *Pels* bezeichnet werden. Die Form des Stichproben Rasters bestimmt die Form der Pixel im digitalisierten Bild.

Im folgenden finden Sie ein Beispiel, in dem kleine Zahlen verwendet werden, um die mathematische Mathematik beizubehalten. Angenommen, das ursprüngliche Bild ist quadratisch (das Bildseiten Verhältnis ist 1:1); angenommen, das Stichproben Raster enthält 12 Elemente, die in einem 4 × 3-Raster angeordnet sind. Die Form jedes resultierenden Pixels ist größer als die Breite. Insbesondere ist die Form jedes Pixels 3 × 4. Pixel, die nicht quadratisch sind, werden als *nicht quadratische Pixel* bezeichnet.

![Diagramm mit einem nicht quadratischen Stichproben Raster](images/aspect-ratio05.png)

Das Pixel Seitenverhältnis gilt auch für das Anzeigegerät. Die physische Form des Anzeige Geräts und die Auflösung des physischen Pixels (über-und Abgleich) bestimmen das par des Anzeige Geräts. Computer Monitore verwenden im allgemeinen quadratische Pixel. Wenn das Bild par und das Anzeige-par nicht übereinstimmen, muss das Bild in einer Dimension, entweder vertikal oder horizontal, skaliert werden, damit es ordnungsgemäß angezeigt wird. Die folgende Formel bezieht sich auf par, das Anzeige Seitenverhältnis (dar) und die Bildgröße in Pixel:

*Dar* = (*Bildbreite in Pixel*  /  *Bildhöhe in Pixel*) × *par*

Beachten Sie, dass Bildbreite und Bildhöhe in dieser Formel auf das Bild im Speicher verweisen, nicht auf das angezeigte Bild.

Im folgenden finden Sie ein Beispiel für eine reale Darstellung: NTSC-M-Analog Video enthält 480-Scan Zeilen im aktiven Bildbereich. "ITU-R Rec. BT. 601" gibt eine horizontale Samplingrate von 704 sichtbaren Pixeln pro Zeile an und ergibt ein digitales Bild mit 704 x 480 Pixeln. Das gewünschte Bildseiten Verhältnis ist 4:3 und ergibt ein par von 10:11.

-   DAR: 4:3
-   Breite in Pixel: 704
-   Höhe in Pixel: 480
-   Par: 10/11

4/3 = (704/420) x (10/11)

Um dieses Bild ordnungsgemäß auf einem Anzeigegerät mit quadratischen Pixeln anzuzeigen, müssen Sie entweder die Breite um 10/11 oder die Höhe um 11/10 skalieren.

## <a name="working-with-aspect-ratios"></a>Arbeiten mit Seitenverhältnissen

Die korrekte Form eines Video Frames wird durch das *Pixel Seitenverhältnis* (par) und den *Anzeigebereich* definiert.

-   Der par-Typ definiert die Form der Pixel in einem Bild. Quadratische Pixel haben ein Seitenverhältnis von 1:1. Jedes andere Seitenverhältnis beschreibt ein nicht quadratisches Pixel. Beispielsweise verwendet NTSC TV eine 10:11-par-. Wenn Sie das Video auf einem Computermonitor präsentieren, hat die Anzeige quadratische Pixel (1:1 PAR). Der Inhalt des Quell Inhalts ist im MF-Attribut [**\_ Pixel- \_ \_ Seiten \_ Verhältnis**](mf-mt-pixel-aspect-ratio-attribute.md) für den Medientyp angegeben.
-   Der Anzeigebereich ist der Bereich des Video Bilds, das angezeigt werden soll. Es gibt zwei relevante Anzeige Bereiche, die im Medientyp angegeben werden können:
    -   Pan-and-Scan-blenden. Die Pan-and-Scan-Öffnung ist ein 4 × 3-Videobereich, der im Pan/Scan-Modus angezeigt werden soll. Es wird verwendet, um breit Bildinhalte in einer 4 × 3-Anzeige ohne Letterboxing anzuzeigen. Die "Pan-and-Scan"- **Öffnung ist im** MF-Attribut " [**MF \_ MT \_ Pan \_ Scan \_ Aperture**](mf-mt-pan-scan-aperture-attribute.md) " angegeben und sollte nur verwendet werden, wenn das MF MT-Attribut für die Überprüfung [**\_ \_ \_ \_ aktiviert**](mf-mt-pan-scan-enabled-attribute.md) ist.
    -   Anzeige Öffnung. Diese Öffnung ist in einigen Videostandards definiert. Alles außerhalb der Anzeige Öffnung ist der Overscan-Bereich und sollte nicht angezeigt werden. Beispielsweise beträgt das NTSC-Fernsehen 720 × 480 Pixel mit einer Anzeige Öffnung von 704 × 480. Die Anzeige Öffnung ist im MF-Master-Attribut für die [**\_ \_ minimale \_ Anzeige \_ Öffnung**](mf-mt-minimum-display-aperture-attribute.md) angegeben. Wenn Sie vorhanden ist, sollte Sie verwendet werden, wenn der Pan-and-Scan-Modus **false** ist.

Wenn der Pan-and-can-Modus **false** ist und keine Anzeige Öffnung definiert ist, sollte der gesamte Videoframe angezeigt werden. Dies gilt auch für die meisten Videoinhalte außer für Fernseh-und DVD-Videos. Das Seitenverhältnis des gesamten Bilds wird als (*Anzeige Bereichs Breite* Anzeige  /  *Bereichs Höhe*) × *par* berechnet.

## <a name="code-examples"></a>Codebeispiele

### <a name="finding-the-display-area"></a>Suchen des Anzeige Bereichs

Der folgende Code zeigt, wie Sie den Anzeigebereich vom Medientyp aus aufrufen.


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a>Zwischen Pixel-Seitenverhältnissen

Der folgende Code zeigt, wie ein Rechteck von einem Pixel Seitenverhältnis (par) in ein anderes konvertiert wird, während gleichzeitig das Bildseiten Verhältnis beibehalten wird.


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a>Berechnen des Bereichs "Briefkasten"

Der folgende Code berechnet den Briefkasten Bereich bei Angabe eines Quell-und Ziel Rechtecks. Es wird davon ausgegangen, dass beide Rechtecke denselben Wert aufweisen.


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> <dt>

[**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**MF- \_ MT- \_ Schwenken- \_ Scan \_ aktiviert**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 




---
description: 'In diesem Thema werden zwei verwandte Konzepte beschrieben: Bildseitenverhältnis und Pixel-Seitenverhältnis.'
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Bildseitenverhältnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae59cf213a9d44c9075f33be4bd422b81ced6dea270cf4fc9408990442529e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972981"
---
# <a name="picture-aspect-ratio"></a>Bildseitenverhältnis

In diesem Thema werden zwei verwandte Konzepte beschrieben: Bildseitenverhältnis und Pixel-Seitenverhältnis. Anschließend wird beschrieben, wie diese Konzepte in Microsoft Media Foundation mithilfe von Medientypen ausgedrückt werden.

-   [Bildseitenverhältnis](#picture-aspect-ratio)
    -   [Letterboxing](#letterboxing)
    -   [Schwenken und Scannen](#pan-and-scan)
-   [Pixel-Seitenverhältnis](#pixel-aspect-ratio)
-   [Arbeiten mit Seitenverhältnissen](#working-with-aspect-ratios)
-   [Codebeispiele](#code-examples)
    -   [Suchen des Anzeigebereichs](#finding-the-display-area)
    -   [Konvertieren zwischen Pixel-Seitenverhältnissen](#converting-between-pixel-aspect-ratios)
    -   [Berechnen des Letterbox-Bereichs](#calculating-the-letterbox-area)
-   [Zugehörige Themen](#related-topics)

## <a name="picture-aspect-ratio"></a>Bildseitenverhältnis

*Bildseitenverhältnis* definiert die Form des angezeigten Videobilds. Das Seitenverhältnis des Bilds wird mit X:Y notiert, wobei X:Y das Verhältnis von Bildbreite zu Bildhöhe ist. Die meisten Videostandards verwenden entweder das Bildseitenverhältnis 4:3 oder 16:9. Das Seitenverhältnis 16:9 wird häufig als *Widescreen* bezeichnet. Der Film verwendet häufig ein Seitenverhältnis von 1:85:1 oder 1:66:1. Bildseitenverhältnis wird auch als *Anzeigeseitenverhältnis (Display Aspect Ratio,* DAR) bezeichnet.

![Diagramm der Seitenverhältnisse 4:3 und 16:9](images/aspect-ratio01.png)

Manchmal hat das Videobild nicht die gleiche Form wie der Anzeigebereich. Beispielsweise kann ein 4:3-Video auf einem Widescreen (16×9)-Fernsehgerät angezeigt werden. Im Computervideo kann das Video in einem Fenster mit einer beliebigen Größe angezeigt werden. In diesem Fall gibt es drei Möglichkeiten, wie das Bild in den Anzeigebereich passen kann:

-   Strecken Sie das Bild entlang einer Achse, um es an den Anzeigebereich anzupassen.
-   Skalieren Sie das Bild so, dass es dem Anzeigebereich entspricht, und behalten Sie dabei das ursprüngliche Seitenverhältnis des Bilds bei.
-   Zuschneiden des Bilds.

Das Strecken des Bilds an den Anzeigebereich ist fast immer falsch, da das richtige Bildseitenverhältnis nicht beibehalten wird.

### <a name="letterboxing"></a>Letterboxing

Der Prozess der Skalierung eines Breitbilds für eine 4:3-Anzeige wird als *Letterboxing* bezeichnet, wie im nächsten Diagramm dargestellt. Die resultierenden retanglularen Bereiche am oberen und unteren Rand des Bilds werden in der Regel mit Schwarz gefüllt, obwohl andere Farben verwendet werden können.

![Diagramm, das die richtige Methode zum Letterbox-Schreiben zeigt](images/aspect-ratio02.png)

Der umgekehrte Fall, das Skalieren eines 4:3-Bilds für eine Breitbildanzeige, wird manchmal als *Pillarboxing* bezeichnet. Der Begriff *Letterbox* wird jedoch auch im allgemeinen Sinn verwendet, um die Skalierung eines Videobilds für einen beliebigen Anzeigebereich zu bedeuten.

![Diagramm mit Pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>Schwenken und Scannen

Schwenken und Scannen ist eine Technik, bei der ein Breitbild auf einen rechteckigen Bereich von 4×3 zugeschnitten wird, um es auf einem 4:3-Anzeigegerät anzuzeigen. Das resultierende Bild füllt die gesamte Anzeige aus, ohne dass schwarze Letterboxbereiche erforderlich sind, aber Teile des ursprünglichen Bilds werden aus dem Bild zugeschnitten. Der bereich, der zugeschnitten wird, kann von Frame zu Frame verschoben werden, wenn sich der bereichliche Bereich verschiebt. Der Begriff "Schwenken" in *Schwenken und Scannen* bezieht sich auf den Schwenkeffekt, der durch das Verschieben des Schwenk- und Scanbereichs verursacht wird.

![Diagramm mit Schwenken und Scannen](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>Pixel-Seitenverhältnis

*Das Pixel-Seitenverhältnis* (PAR) misst die Form eines Pixels.

Wenn ein digitales Bild erfasst wird, wird das Bild sowohl vertikal als auch horizontal entnommen, was zu einem rechteckigen Array von quantisierten Stichproben führt, die als *Pixel* oder *Kästchen* bezeichnet werden. Die Form des Stichprobenrasters bestimmt die Form der Pixel im digitalisierten Bild.

Im Folgenden finden Sie ein Beispiel, in dem kleine Zahlen verwendet werden, um die Mathematische Berechnung einfach zu halten. Angenommen, das ursprüngliche Bild ist quadratisch (d. b. das Seitenverhältnis des Bilds ist 1:1). und nehmen wir an, dass das Samplingraster 12 Elemente enthält, die in einem 4×3-Raster angeordnet sind. Die Form jedes resultierenden Pixels ist größer als die Breite. Die Form jedes Pixels ist 3×4. Pixel, die nicht quadratisch sind, werden als *nicht quadratische Pixel* bezeichnet.

![Diagramm mit einem Raster für nicht quadratische Stichprobenentnahme](images/aspect-ratio05.png)

Das Pixel-Seitenverhältnis gilt auch für das Anzeigegerät. Die physische Form des Anzeigegeräts und die physische Pixelauflösung (über- und herunter) bestimmen den PAR des Anzeigegeräts. Computermonitore verwenden im Allgemeinen quadratische Pixel. Wenn bildPAR und display PAR nicht übereinstimmen, muss das Bild vertikal oder horizontal in einer Dimension skaliert werden, um ordnungsgemäß angezeigt zu werden. Die folgende Formel bezieht sich auf PAR, das Seitenverhältnis (Display Aspect Ratio, DAR) und die Bildgröße in Pixel:

*DAR* = (*Bildbreite in Pixel*  /  *Bildhöhe in Pixel*) × *PAR*

Beachten Sie, dass Bildbreite und Bildhöhe in dieser Formel auf das Bild im Arbeitsspeicher und nicht auf das angezeigte Bild verweisen.

Hier sehen Sie ein beispiel aus der Praxis: Das analoge NTSC-M-Video enthält 480 Scanzeilen im aktiven Bildbereich. ITU-R Rec. BT.601 gibt eine horizontale Samplingrate von 704 sichtbaren Pixeln pro Zeile an, die ein digitales Bild mit 704 x 480 Pixel ergibt. Das beabsichtigte Bildseitenverhältnis ist 4:3 und ergibt einen PAR von 10:11.

-   DAR: 4:3
-   Breite in Pixel: 704
-   Höhe in Pixel: 480
-   PAR: 10/11

4/3 = (704/420) x (10/11)

Um dieses Bild ordnungsgemäß auf einem Anzeigegerät mit quadratischen Pixeln anzuzeigen, müssen Sie entweder die Breite um 10/11 oder die Höhe um 11/10 skalieren.

## <a name="working-with-aspect-ratios"></a>Arbeiten mit Seitenverhältnissen

Die richtige Form eines Videoframes wird durch das *Pixel-Seitenverhältnis (PAR)* und den *Anzeigebereich* definiert.

-   Der PAR definiert die Form der Pixel in einem Bild. Quadratpixel weisen ein Seitenverhältnis von 1:1 auf. Jedes andere Seitenverhältnis beschreibt ein nicht quadratisches Pixel. NtSC-Fernsehgerät verwendet z.B. einen 10:11 PAR. Angenommen, Sie stellen das Video auf einem Computermonitor vor, hat die Anzeige quadratische Pixel (1:1 PAR). Der PAR-Wert des Quellinhalts wird im [**MF MT PIXEL ASPECT \_ \_ \_ \_ RATIO-Attribut**](mf-mt-pixel-aspect-ratio-attribute.md) für den Medientyp angegeben.
-   Der Anzeigebereich ist der Bereich des Videobilds, das angezeigt werden soll. Es gibt zwei relevante Anzeigebereiche, die im Medientyp angegeben werden können:
    -   Pan-and-Scan-Öffnung. Die Pan-and-Scan-Öffnung ist eine 4×3-Videoregion, die im Schwenk-/Scanmodus angezeigt werden soll. Es wird verwendet, um Breitbildinhalte in einer 4×3-Anzeige ohne Letterboxing anzuzeigen. Die Pan-and-Scan-Öffnung wird im [**MF MT PAN SCAN \_ \_ \_ \_ APERTURE-Attribut**](mf-mt-pan-scan-aperture-attribute.md) angegeben und sollte nur verwendet werden, wenn das [**MF MT PAN SCAN \_ \_ \_ \_ ENABLED-Attribut**](mf-mt-pan-scan-enabled-attribute.md) **TRUE** ist.
    -   Anzeigeaufblendung. Diese Öffnung ist in einigen Videostandards definiert. Alles außerhalb der Anzeigegeblendung ist der überscannte Bereich und sollte nicht angezeigt werden. Ntsc-Fernsehgerät hat z. B. 720×480 Pixel mit einer Öffnung von 704×480. Die Anzeigeblende wird im [**MF MT MINIMUM DISPLAY \_ \_ \_ \_ APERTURE-Attribut**](mf-mt-minimum-display-aperture-attribute.md) angegeben. Falls vorhanden, sollte es verwendet werden, wenn der Schwenk- und Scanmodus **FALSE** ist.

Wenn schwenk- und kann-Modus **FALSE** ist und keine Anzeigeaufblendung definiert ist, sollte der gesamte Videoframe angezeigt werden. Tatsächlich ist dies bei den meisten Videoinhalten mit Ausnahme von Fernseh- und DVD-Videos der Fall. Das Seitenverhältnis des gesamten Bilds wird als *(Anzeigebereichsbreitenhöhe*  /  ) × *PAR* berechnet.

## <a name="code-examples"></a>Codebeispiele

### <a name="finding-the-display-area"></a>Suchen des Anzeigebereichs

Der folgende Code zeigt, wie sie den Anzeigebereich vom Medientyp abrufen.


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



### <a name="converting-between-pixel-aspect-ratios"></a>Konvertieren zwischen Pixel-Seitenverhältnissen

Der folgende Code zeigt, wie Ein Rechteck von einem Pixel-Seitenverhältnis (PAR) in ein anderes konvertiert wird, während das Seitenverhältnis des Bilds beibehalten wird.


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



### <a name="calculating-the-letterbox-area"></a>Berechnen des Letterbox-Bereichs

Der folgende Code berechnet den Letterboxbereich mit einem Quell- und Zielrechteck. Es wird davon ausgegangen, dass beide Rechtecke denselben PAR haben.


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

[Videomedientypen](video-media-types.md)
</dt> <dt>

[**MF \_ MT \_ MINIMUM \_ DISPLAY \_ APERTURE**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**MF \_ MT PIXEL \_ \_ \_ SEITENVERHÄLTNIS**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 




---
description: Bild-Stride
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Bild-Stride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360afb6fdeca4c543957326b041654d75ff17b66db8918e42d781d414e8b7586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958149"
---
# <a name="image-stride"></a>Bild-Stride

Wenn ein Videobild im Arbeitsspeicher gespeichert wird, enthält der Speicherpuffer möglicherweise zusätzliche Aufpaddungsbytes nach jeder Pixelzeile. Die Auf padding-Bytes wirken sich darauf aus, wie das Bild im Arbeitsspeicher gespeichert wird, aber nicht, wie das Bild angezeigt wird.

Der *Schritt ist* die Anzahl von Bytes von einer Zeile pixel im Arbeitsspeicher bis zur nächsten Pixelzeile im Arbeitsspeicher. Stride wird auch als *Tonhöhe bezeichnet.* Wenn Auf padding bytes vorhanden sind, ist der Schritt breiter als die Breite des Bilds, wie in der folgenden Abbildung dargestellt.

![Diagramm, das ein Bild plus Auf padding zeigt.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Zwei Puffer, die Videoframes mit gleichen Dimensionen enthalten, können zwei unterschiedliche Schritte haben. Wenn Sie ein Videobild verarbeiten, müssen Sie den Schritt berücksichtigen.

Darüber hinaus gibt es zwei Möglichkeiten, wie ein Bild im Arbeitsspeicher angeordnet werden kann. In einem *Bild von oben nach unten* wird die oberste Pixelzeile im Bild zuerst im Arbeitsspeicher angezeigt. In einem *Bild von unten nach oben* wird die letzte Pixelzeile zuerst im Arbeitsspeicher angezeigt. Die folgende Abbildung zeigt den Unterschied zwischen einem Bild von oben nach unten und einem Bild von unten nach oben.

![Diagramm, das Bilder von oben nach unten und von unten nach oben zeigt.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Ein Bild von unten nach oben hat einen negativen Schritt, da stride als die Anzahl von Bytes definiert ist, die in Bezug auf das angezeigte Bild eine Reihe von Pixeln nach unten verschieben müssen. YUV-Images sollten immer von oben nach unten angezeigt werden, und alle Images, die in einer Direct3D-Oberfläche enthalten sind, müssen von oben nach unten angezeigt werden. RGB-Bilder im Systemspeicher befinden sich in der Regel von unten nach oben.

Insbesondere Videotransformationen müssen Puffer mit nicht übereinstimmenden Schritten verarbeiten, da der Eingabepuffer möglicherweise nicht mit dem Ausgabepuffer übereinstimmen kann. Angenommen, Sie möchten ein Quellimage konvertieren und das Ergebnis in ein Zielimage schreiben. Angenommen, beide Bilder haben die gleiche Breite und Höhe, aber möglicherweise nicht das gleiche Pixelformat oder denselben Bildschritt.

Der folgende Beispielcode zeigt einen generalisierten Ansatz zum Schreiben dieser Art von Funktion. Dies ist kein vollständiges Funktionierendes Beispiel, da es viele der spezifischen Details abstrahiert.


```C++
void ProcessVideoImage(
    BYTE*       pDestScanLine0,     
    LONG        lDestStride,        
    const BYTE* pSrcScanLine0,      
    LONG        lSrcStride,         
    DWORD       dwWidthInPixels,     
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        SOURCE_PIXEL_TYPE *pSrcPixel = (SOURCE_PIXEL_TYPE*)pDestScanLine0;
        DEST_PIXEL_TYPE *pDestPixel = (DEST_PIXEL_TYPE*)pSrcScanLine0;

        for (DWORD x = 0; x < dwWidthInPixels; x +=2)
        {
            pDestPixel[x] = TransformPixelValue(pSrcPixel[x]);
        }
        pDestScanLine0 += lDestStride;
        pSrcScanLine0 += lSrcStride;
    }
}
```



Diese Funktion verwendet sechs Parameter:

-   Ein Zeiger auf den Anfang der Scanzeile 0 im Zielbild.
-   Der Schritt des Zielimages.
-   Ein Zeiger auf den Anfang der Scanzeile 0 im Quellbild.
-   Der Schritt des Quellbilds.
-   Die Breite des Bilds in Pixel.
-   Die Höhe des Bilds in Pixel.

Die allgemeine Idee ist, eine Zeile nach der anderen zu verarbeiten und dabei jedes Pixel in der Zeile zu iterieren. Angenommen, SOURCE PIXEL TYPE und DEST PIXEL TYPE sind Strukturen, die das Pixellayout für die Quell- bzw. \_ \_ \_ \_ Zielbilder darstellen. (Beispiel: 32-Bit-RGB verwendet die [**RGBQUAD-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) Nicht jedes Pixelformat verfügt über eine vordefinierte Struktur.) Wenn Sie den Arrayzeiger in den Strukturtyp konvertieren, können Sie auf die RGB- oder YUV-Komponenten der einzelnen Pixel zugreifen. Am Anfang jeder Zeile speichert die Funktion einen Zeiger auf die Zeile. Am Ende der Zeile wird der Zeiger um die Breite des Bildschritts erhöht, wodurch der Zeiger auf die nächste Zeile erhöht wird.

In diesem Beispiel wird für jedes Pixel eine hypothetische Funktion namens TransformPixelValue aufruft. Dies kann eine beliebige Funktion sein, die ein Zielpixel aus einem Quellpixel berechnet. Die genauen Details hängen natürlich von der jeweiligen Aufgabe ab. Wenn Sie z. B. über ein planares YUV-Format verfügen, müssen Sie unabhängig von der Lumaebene auf die Flugzeugebenen zugreifen. mit Interlaced-Video müssen Sie die Felder möglicherweise separat verarbeiten. usw.

Um ein konkretes Beispiel zu geben, konvertiert der folgende Code ein 32-Bit-RGB-Bild in ein AYUV-Bild. Auf die RGB-Pixel wird über eine [**RGBQUAD-Struktur**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) zugegriffen, und auf die AYUV-Pixel wird mithilfe einer [**DXVA2 \_ AYUVSample8-Struktur**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) zugegriffen.


```C++
//-------------------------------------------------------------------
// Name: RGB32_To_AYUV
// Description: Converts an image from RGB32 to AYUV
//-------------------------------------------------------------------
void RGB32_To_AYUV(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD             *pSrcPixel = (RGBQUAD*)pSrc;
        DXVA2_AYUVSample8   *pDestPixel = (DXVA2_AYUVSample8*)pDest;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestPixel[x].Alpha = 0x80;
            pDestPixel[x].Y = RGBtoY(pSrcPixel[x]);   
            pDestPixel[x].Cb = RGBtoU(pSrcPixel[x]);   
            pDestPixel[x].Cr = RGBtoV(pSrcPixel[x]);   
        }
        pDest += lDestStride;
        pSrc += lSrcStride;
    }
}
```



Im nächsten Beispiel wird ein 32-Bit-RGB-Bild in ein YV12-Bild konvertiert. Dieses Beispiel zeigt, wie ein planares YUV-Format behandelt wird. (YV12 ist ein planares 4:2:0-Format.) In diesem Beispiel verwaltet die Funktion drei separate Zeiger für die drei Ebenen im Zielbild. Der grundlegende Ansatz ist jedoch identisch mit dem vorherigen Beispiel.


```C++
void RGB32_To_YV12(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    assert(dwWidthInPixels % 2 == 0);
    assert(dwHeightInPixels % 2 == 0);

    const BYTE *pSrcRow = pSrc;
    
    BYTE *pDestY = pDest;

    // Calculate the offsets for the V and U planes.

    // In YV12, each chroma plane has half the stride and half the height  
    // as the Y plane.
    BYTE *pDestV = pDest + (lDestStride * dwHeightInPixels);
    BYTE *pDestU = pDest + 
                   (lDestStride * dwHeightInPixels) + 
                   ((lDestStride * dwHeightInPixels) / 4);

    // Convert the Y plane.
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestY[x] = RGBtoY(pSrcPixel[x]);    // Y0
        }
        pDestY += lDestStride;
        pSrcRow += lSrcStride;
    }

    // Convert the V and U planes.

    // YV12 is a 4:2:0 format, so each chroma sample is derived from four 
    // RGB pixels.
    pSrcRow = pSrc;
    for (DWORD y = 0; y < dwHeightInPixels; y += 2)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        RGBQUAD *pNextSrcRow = (RGBQUAD*)(pSrcRow + lSrcStride);

        BYTE *pbV = pDestV;
        BYTE *pbU = pDestU;

        for (DWORD x = 0; x < dwWidthInPixels; x += 2)
        {
            // Use a simple average to downsample the chroma.

            *pbV++ = ( RGBtoV(pSrcPixel[x]) +
                       RGBtoV(pSrcPixel[x + 1]) +       
                       RGBtoV(pNextSrcRow[x]) +         
                       RGBtoV(pNextSrcRow[x + 1]) ) / 4;        

            *pbU++ = ( RGBtoU(pSrcPixel[x]) +
                       RGBtoU(pSrcPixel[x + 1]) +       
                       RGBtoU(pNextSrcRow[x]) +         
                       RGBtoU(pNextSrcRow[x + 1]) ) / 4;    
        }
        pDestV += lDestStride / 2;
        pDestU += lDestStride / 2;
        
        // Skip two lines on the source image.
        pSrcRow += (lSrcStride * 2);
    }
}
```



In all diesen Beispielen wird davon ausgegangen, dass die Anwendung den Bildschritt bereits bestimmt hat. Sie können diese Informationen manchmal aus dem Medienpuffer erhalten. Andernfalls müssen Sie ihn basierend auf dem Videoformat berechnen. Weitere Informationen zum Berechnen von Bildschritten und zum Arbeiten mit Medienpuffern für Videos finden Sie unter [Unkomprimierte Videopuffer](uncompressed-video-buffers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videomedientypen](video-media-types.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 

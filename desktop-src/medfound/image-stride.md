---
description: Bild Schritt
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Bild Schritt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813c0f3d99297758761bdfb5973fc2b16e3339f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566555"
---
# <a name="image-stride"></a>Bild Schritt

Wenn ein Video Bild im Arbeitsspeicher gespeichert wird, kann der Speicherpuffer nach jeder Zeile von Pixeln zusätzliche Leerraum Bytes enthalten. Die Füll Zeichen in Bytes beeinflussen, wie das Bild im Arbeitsspeicher gespeichert wird, aber nicht, wie das Bild angezeigt wird.

Der *Stride* -Wert ist die Anzahl der Bytes aus einer Zeile mit Pixeln im Arbeitsspeicher bis zur nächsten Zeile im Arbeitsspeicher. Stride wird auch als " *Pitch*" bezeichnet. Wenn Auffüll-Bytes vorhanden sind, ist der Stride breiter als die Breite des Bilds, wie in der folgenden Abbildung dargestellt.

![Diagramm, das ein Bild Plus Padding anzeigt.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Zwei Puffer, die Video Frames mit identischen Dimensionen enthalten, können zwei unterschiedliche Schritte aufweisen. Wenn Sie ein Video Bild verarbeiten, müssen Sie das Konto berücksichtigen.

Außerdem gibt es zwei Möglichkeiten, wie ein Image im Arbeitsspeicher angeordnet werden kann. In einem *Top-Down-* Bild wird die obere Zeile der Pixel im Bild zuerst im Arbeitsspeicher angezeigt. In einem *Bottom-up-* Bild wird die letzte Zeile der Pixel zuerst im Arbeitsspeicher angezeigt. Die folgende Abbildung zeigt den Unterschied zwischen einem Bild von oben nach unten und einem unteren Bild.

![Diagramm mit Top-Down-und Bottom-up-Bildern.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Ein Bottom-up-Bild hat einen negativen Schritt, da Stride definiert ist, da die Anzahl der Bytes in Bezug auf das angezeigte Bild eine Zeile von Pixeln nach unten verschieben muss. YUV-Images sollten immer von oben nach unten sein, und jedes in einer Direct3D-Oberfläche enthaltene Bild muss von oben nach unten angezeigt werden. RGB-Images im Systemspeicher sind in der Regel im unteren Bereich.

Insbesondere Video Transformationen müssen Puffer mit nicht übereinstimmenden Schritten verarbeiten, da der Eingabepuffer möglicherweise nicht mit dem Ausgabepuffer übereinstimmt. Nehmen Sie beispielsweise an, dass Sie ein Quell Image konvertieren und das Ergebnis in ein Zielbild schreiben möchten. Angenommen, beide Bilder haben die gleiche Breite und Höhe, aber Sie verfügen möglicherweise nicht über das gleiche Pixel Format oder den gleichen Bild Schritt.

Der folgende Beispielcode zeigt einen generalisierten Ansatz zum Schreiben dieser Art von Funktion. Dies ist kein umfassendes Beispiel, da viele der spezifischen Details zusammengeführt werden.


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



Diese Funktion nimmt sechs Parameter an:

-   Ein Zeiger auf den Anfang der Scan Zeile 0 im Zielbild.
-   Der Schritt des zielbilds.
-   Ein Zeiger auf den Anfang der Scan Zeile 0 im Quell Image.
-   Der Schritt des Quell Bilds.
-   Die Breite des Bilds in Pixel.
-   Die Höhe des Bilds in Pixel.

Die allgemeine Idee besteht darin, eine Zeile gleichzeitig zu verarbeiten und die einzelnen Pixel in der Zeile zu durchlaufen. Angenommen, der Quell-und der \_ \_ dest- \_ \_ Pixeltyp sind Strukturen, die das Pixel Layout für das Quell-bzw. Ziel Abbild darstellen. (32-Bit RGB verwendet beispielsweise die [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Struktur. Nicht jedes Pixel Format weist eine vordefinierte Struktur auf.) Wenn Sie den Array Zeiger in den Strukturtyp umwandeln, können Sie auf die RGB-oder YUV-Komponenten der einzelnen Pixel zugreifen. Am Anfang der einzelnen Zeilen wird von der Funktion ein Zeiger auf die Zeile gespeichert. Am Ende der Zeile wird der Zeiger um die Breite des Bild Schritts erhöht, wodurch der Zeiger auf die nächste Zeile erhöht wird.

In diesem Beispiel wird für jedes Pixel eine hypothetische Funktion mit dem Namen transformpixelvalue aufgerufen. Dies kann eine beliebige Funktion sein, die ein Zielpixel aus einem Quell Pixel berechnet. Natürlich hängen die genauen Details von der jeweiligen Aufgabe ab. Wenn Sie z. b. ein planare-YUV-Format haben, müssen Sie auf die Chroma-Ebenen unabhängig von der Luma-Ebene zugreifen. mit einem Zeilen Sprung Video müssen Sie die Felder möglicherweise separat verarbeiten. und so weiter.

Um ein konkreteres Beispiel zu erhalten, konvertiert der folgende Code ein 32-Bit-RGB-Bild in ein ayuv-Image. Der Zugriff auf RGB-Pixel erfolgt über eine [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Struktur, und der Zugriff auf die ayuv-Pixel erfolgt mithilfe einer [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) -Struktur Struktur.


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



Im nächsten Beispiel wird ein 32-Bit-RGB-Bild in ein YV12-Image konvertiert. In diesem Beispiel wird gezeigt, wie ein planare-YUV-Format behandelt wird. (YV12 ist ein planare 4:2:0-Format.) In diesem Beispiel werden von der-Funktion drei separate Zeiger für die drei Ebenen im Zielbild verwaltet. Der grundlegende Ansatz ist jedoch mit dem vorherigen Beispiel identisch.


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



In allen diesen Beispielen wird davon ausgegangen, dass die Anwendung bereits den Bild Schritt ermittelt hat. Sie können diese Informationen manchmal aus dem Medien Puffer erhalten. Andernfalls müssen Sie ihn basierend auf dem Videoformat berechnen. Weitere Informationen zum Berechnen von Image Stride und zum Arbeiten mit Medien Puffern für Videos finden Sie unter [unkomprimierte Video Puffer](uncompressed-video-buffers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Medientypen](video-media-types.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 

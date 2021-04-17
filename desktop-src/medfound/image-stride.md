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
# <a name="image-stride"></a><span data-ttu-id="26df7-103">Bild Schritt</span><span class="sxs-lookup"><span data-stu-id="26df7-103">Image Stride</span></span>

<span data-ttu-id="26df7-104">Wenn ein Video Bild im Arbeitsspeicher gespeichert wird, kann der Speicherpuffer nach jeder Zeile von Pixeln zusätzliche Leerraum Bytes enthalten.</span><span class="sxs-lookup"><span data-stu-id="26df7-104">When a video image is stored in memory, the memory buffer might contain extra padding bytes after each row of pixels.</span></span> <span data-ttu-id="26df7-105">Die Füll Zeichen in Bytes beeinflussen, wie das Bild im Arbeitsspeicher gespeichert wird, aber nicht, wie das Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="26df7-105">The padding bytes affect how the image is stored in memory, but do not affect how the image is displayed.</span></span>

<span data-ttu-id="26df7-106">Der *Stride* -Wert ist die Anzahl der Bytes aus einer Zeile mit Pixeln im Arbeitsspeicher bis zur nächsten Zeile im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="26df7-106">The *stride* is the number of bytes from one row of pixels in memory to the next row of pixels in memory.</span></span> <span data-ttu-id="26df7-107">Stride wird auch als " *Pitch*" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="26df7-107">Stride is also called *pitch*.</span></span> <span data-ttu-id="26df7-108">Wenn Auffüll-Bytes vorhanden sind, ist der Stride breiter als die Breite des Bilds, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="26df7-108">If padding bytes are present, the stride is wider than the width of the image, as shown in the following illustration.</span></span>

![Diagramm, das ein Bild Plus Padding anzeigt.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

<span data-ttu-id="26df7-110">Zwei Puffer, die Video Frames mit identischen Dimensionen enthalten, können zwei unterschiedliche Schritte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="26df7-110">Two buffers that contain video frames with equal dimensions can have two different strides.</span></span> <span data-ttu-id="26df7-111">Wenn Sie ein Video Bild verarbeiten, müssen Sie das Konto berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="26df7-111">If you process a video image, you must take the stride into account.</span></span>

<span data-ttu-id="26df7-112">Außerdem gibt es zwei Möglichkeiten, wie ein Image im Arbeitsspeicher angeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="26df7-112">In addition, there are two ways that an image can be arranged in memory.</span></span> <span data-ttu-id="26df7-113">In einem *Top-Down-* Bild wird die obere Zeile der Pixel im Bild zuerst im Arbeitsspeicher angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26df7-113">In a *top-down* image, the top row of pixels in the image appears first in memory.</span></span> <span data-ttu-id="26df7-114">In einem *Bottom-up-* Bild wird die letzte Zeile der Pixel zuerst im Arbeitsspeicher angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26df7-114">In a *bottom-up* image, the last row of pixels appears first in memory.</span></span> <span data-ttu-id="26df7-115">Die folgende Abbildung zeigt den Unterschied zwischen einem Bild von oben nach unten und einem unteren Bild.</span><span class="sxs-lookup"><span data-stu-id="26df7-115">The following illustration shows the difference between a top-down image and a bottom-up image.</span></span>

![Diagramm mit Top-Down-und Bottom-up-Bildern.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

<span data-ttu-id="26df7-117">Ein Bottom-up-Bild hat einen negativen Schritt, da Stride definiert ist, da die Anzahl der Bytes in Bezug auf das angezeigte Bild eine Zeile von Pixeln nach unten verschieben muss.</span><span class="sxs-lookup"><span data-stu-id="26df7-117">A bottom-up image has a negative stride, because stride is defined as the number of bytes need to move down a row of pixels, relative to the displayed image.</span></span> <span data-ttu-id="26df7-118">YUV-Images sollten immer von oben nach unten sein, und jedes in einer Direct3D-Oberfläche enthaltene Bild muss von oben nach unten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="26df7-118">YUV images should always be top-down, and any image that is contained in a Direct3D surface must be top-down.</span></span> <span data-ttu-id="26df7-119">RGB-Images im Systemspeicher sind in der Regel im unteren Bereich.</span><span class="sxs-lookup"><span data-stu-id="26df7-119">RGB images in system memory are usually bottom-up.</span></span>

<span data-ttu-id="26df7-120">Insbesondere Video Transformationen müssen Puffer mit nicht übereinstimmenden Schritten verarbeiten, da der Eingabepuffer möglicherweise nicht mit dem Ausgabepuffer übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="26df7-120">Video transforms in particular need to handle buffers with mismatched strides, because the input buffer might not match the output buffer.</span></span> <span data-ttu-id="26df7-121">Nehmen Sie beispielsweise an, dass Sie ein Quell Image konvertieren und das Ergebnis in ein Zielbild schreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="26df7-121">For example, suppose that you want to convert a source image and write the result to a destination image.</span></span> <span data-ttu-id="26df7-122">Angenommen, beide Bilder haben die gleiche Breite und Höhe, aber Sie verfügen möglicherweise nicht über das gleiche Pixel Format oder den gleichen Bild Schritt.</span><span class="sxs-lookup"><span data-stu-id="26df7-122">Assume that both images have the same width and height, but might not have the same pixel format or the same image stride.</span></span>

<span data-ttu-id="26df7-123">Der folgende Beispielcode zeigt einen generalisierten Ansatz zum Schreiben dieser Art von Funktion.</span><span class="sxs-lookup"><span data-stu-id="26df7-123">The following example code shows a generalized approach for writing this kind of function.</span></span> <span data-ttu-id="26df7-124">Dies ist kein umfassendes Beispiel, da viele der spezifischen Details zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="26df7-124">This is not a complete working example, because it abstracts many of the specific details.</span></span>


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



<span data-ttu-id="26df7-125">Diese Funktion nimmt sechs Parameter an:</span><span class="sxs-lookup"><span data-stu-id="26df7-125">This function takes six parameters:</span></span>

-   <span data-ttu-id="26df7-126">Ein Zeiger auf den Anfang der Scan Zeile 0 im Zielbild.</span><span class="sxs-lookup"><span data-stu-id="26df7-126">A pointer to the start of scan line 0 in the destination image.</span></span>
-   <span data-ttu-id="26df7-127">Der Schritt des zielbilds.</span><span class="sxs-lookup"><span data-stu-id="26df7-127">The stride of the destination image.</span></span>
-   <span data-ttu-id="26df7-128">Ein Zeiger auf den Anfang der Scan Zeile 0 im Quell Image.</span><span class="sxs-lookup"><span data-stu-id="26df7-128">A pointer to the start of scan line 0 in the source image.</span></span>
-   <span data-ttu-id="26df7-129">Der Schritt des Quell Bilds.</span><span class="sxs-lookup"><span data-stu-id="26df7-129">The stride of the source image.</span></span>
-   <span data-ttu-id="26df7-130">Die Breite des Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="26df7-130">The width of the image in pixels.</span></span>
-   <span data-ttu-id="26df7-131">Die Höhe des Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="26df7-131">The height of the image in pixels.</span></span>

<span data-ttu-id="26df7-132">Die allgemeine Idee besteht darin, eine Zeile gleichzeitig zu verarbeiten und die einzelnen Pixel in der Zeile zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="26df7-132">The general idea is to process one row at a time, iterating over each pixel in the row.</span></span> <span data-ttu-id="26df7-133">Angenommen, der Quell-und der \_ \_ dest- \_ \_ Pixeltyp sind Strukturen, die das Pixel Layout für das Quell-bzw. Ziel Abbild darstellen.</span><span class="sxs-lookup"><span data-stu-id="26df7-133">Assume that SOURCE\_PIXEL\_TYPE and DEST\_PIXEL\_TYPE are structures representing the pixel layout for the source and destination images, respectively.</span></span> <span data-ttu-id="26df7-134">(32-Bit RGB verwendet beispielsweise die [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="26df7-134">(For example, 32-bit RGB uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure.</span></span> <span data-ttu-id="26df7-135">Nicht jedes Pixel Format weist eine vordefinierte Struktur auf.) Wenn Sie den Array Zeiger in den Strukturtyp umwandeln, können Sie auf die RGB-oder YUV-Komponenten der einzelnen Pixel zugreifen.</span><span class="sxs-lookup"><span data-stu-id="26df7-135">Not every pixel format has a predefined structure.) Casting the array pointer to the structure type enables you to access the RGB or YUV components of each pixel.</span></span> <span data-ttu-id="26df7-136">Am Anfang der einzelnen Zeilen wird von der Funktion ein Zeiger auf die Zeile gespeichert.</span><span class="sxs-lookup"><span data-stu-id="26df7-136">At the start of each row, the function stores a pointer to the row.</span></span> <span data-ttu-id="26df7-137">Am Ende der Zeile wird der Zeiger um die Breite des Bild Schritts erhöht, wodurch der Zeiger auf die nächste Zeile erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="26df7-137">At the end of the row, it increments the pointer by the width of the image stride, which advances the pointer to the next row.</span></span>

<span data-ttu-id="26df7-138">In diesem Beispiel wird für jedes Pixel eine hypothetische Funktion mit dem Namen transformpixelvalue aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="26df7-138">This example calls a hypothetical function named TransformPixelValue for each pixel.</span></span> <span data-ttu-id="26df7-139">Dies kann eine beliebige Funktion sein, die ein Zielpixel aus einem Quell Pixel berechnet.</span><span class="sxs-lookup"><span data-stu-id="26df7-139">This could be any function that calculates a target pixel from a source pixel.</span></span> <span data-ttu-id="26df7-140">Natürlich hängen die genauen Details von der jeweiligen Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="26df7-140">Of course, the exact details will depend on the particular task.</span></span> <span data-ttu-id="26df7-141">Wenn Sie z. b. ein planare-YUV-Format haben, müssen Sie auf die Chroma-Ebenen unabhängig von der Luma-Ebene zugreifen. mit einem Zeilen Sprung Video müssen Sie die Felder möglicherweise separat verarbeiten. und so weiter.</span><span class="sxs-lookup"><span data-stu-id="26df7-141">For example, if you have a planar YUV format, you must access the chroma planes independently from the luma plane; with interlaced video, you might need to process the fields separately; and so forth.</span></span>

<span data-ttu-id="26df7-142">Um ein konkreteres Beispiel zu erhalten, konvertiert der folgende Code ein 32-Bit-RGB-Bild in ein ayuv-Image.</span><span class="sxs-lookup"><span data-stu-id="26df7-142">To give a more concrete example, the following code converts a 32-bit RGB image into an AYUV image.</span></span> <span data-ttu-id="26df7-143">Der Zugriff auf RGB-Pixel erfolgt über eine [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Struktur, und der Zugriff auf die ayuv-Pixel erfolgt mithilfe einer [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) -Struktur Struktur.</span><span class="sxs-lookup"><span data-stu-id="26df7-143">The RGB pixels are accessed using an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, and the AYUV pixels are accessed using a [**DXVA2\_AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) structure structure.</span></span>


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



<span data-ttu-id="26df7-144">Im nächsten Beispiel wird ein 32-Bit-RGB-Bild in ein YV12-Image konvertiert.</span><span class="sxs-lookup"><span data-stu-id="26df7-144">The next example converts a 32-bit RGB image to a YV12 image.</span></span> <span data-ttu-id="26df7-145">In diesem Beispiel wird gezeigt, wie ein planare-YUV-Format behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="26df7-145">This example shows how to handle a planar YUV format.</span></span> <span data-ttu-id="26df7-146">(YV12 ist ein planare 4:2:0-Format.) In diesem Beispiel werden von der-Funktion drei separate Zeiger für die drei Ebenen im Zielbild verwaltet.</span><span class="sxs-lookup"><span data-stu-id="26df7-146">(YV12 is a planar 4:2:0 format.) In this example, the function maintains three separate pointers for the three planes in the target image.</span></span> <span data-ttu-id="26df7-147">Der grundlegende Ansatz ist jedoch mit dem vorherigen Beispiel identisch.</span><span class="sxs-lookup"><span data-stu-id="26df7-147">However, the basic approach is the same as the previous example.</span></span>


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



<span data-ttu-id="26df7-148">In allen diesen Beispielen wird davon ausgegangen, dass die Anwendung bereits den Bild Schritt ermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="26df7-148">In all of these examples, it is assumed that the application has already determined the image stride.</span></span> <span data-ttu-id="26df7-149">Sie können diese Informationen manchmal aus dem Medien Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="26df7-149">You can sometimes get this information from the media buffer.</span></span> <span data-ttu-id="26df7-150">Andernfalls müssen Sie ihn basierend auf dem Videoformat berechnen.</span><span class="sxs-lookup"><span data-stu-id="26df7-150">Otherwise, you must calculate it based on the video format.</span></span> <span data-ttu-id="26df7-151">Weitere Informationen zum Berechnen von Image Stride und zum Arbeiten mit Medien Puffern für Videos finden Sie unter [unkomprimierte Video Puffer](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="26df7-151">For more information about calculating image stride and working with media buffers for video, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26df7-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26df7-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26df7-153">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="26df7-153">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="26df7-154">Medientypen</span><span class="sxs-lookup"><span data-stu-id="26df7-154">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 

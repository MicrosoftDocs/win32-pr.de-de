---
title: Verarbeiten des Videos
description: Verarbeiten des Videos
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Windows Media Player-Plug-ins, videodsp
- Plug-ins, videodsp
- Plug-Ins für die digitale Signalverarbeitung, Videoverarbeitung
- DSP-Plug-ins, Videoverarbeitung
- videodsp-Plug-ins, verarbeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8d21aaa3999d05ea3628ff341c74379b07a6dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039172"
---
# <a name="processing-the-video"></a><span data-ttu-id="c9a50-108">Verarbeiten des Videos</span><span class="sxs-lookup"><span data-stu-id="c9a50-108">Processing the Video</span></span>

<span data-ttu-id="c9a50-109">Die Details des Verarbeitungs Videos variieren je nach Format. Diese Details werden über den Rahmen dieser Dokumentation hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="c9a50-109">The details of processing video vary for each format; it is beyond the scope of this documentation to provide these details.</span></span> <span data-ttu-id="c9a50-110">Im Allgemeinen ist das Ziel des Plug-ins, die Farbdaten im Eingabepuffer zu ändern und die Daten dann in den Ausgabepuffer zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="c9a50-110">In a general sense, the goal of the plug-in is to change the color data in the input buffer and then copy the data to the output buffer.</span></span>

<span data-ttu-id="c9a50-111">Das Beispiel-Plug-in verarbeitet zwei Arten von Videoformaten: YUV und RGB.</span><span class="sxs-lookup"><span data-stu-id="c9a50-111">The sample plug-in processes two types of video formats: YUV and RGB.</span></span>

<span data-ttu-id="c9a50-112">Bei einem YUV-Video werden die roten und blauen Farbinformationen in den Werten "You" und "V" codiert, und die Leuchtkraft Ebene wird durch den Y-Wert dargestellt. der grüne Wert ist codiert und kann mithilfe eines Algorithmus wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c9a50-112">For YUV video, the red and blue color information is encoded in the U and V values and the luminance level is represented by the Y value; the green value is encoded and can be recovered by using an algorithm.</span></span> <span data-ttu-id="c9a50-113">Das Beispiel-Plug-in ändert einfach die Werte von "You" und "V", um die Farbstufe zu beeinflussen</span><span class="sxs-lookup"><span data-stu-id="c9a50-113">The sample plug-in simply changes the U and V values to affect the color level.</span></span> <span data-ttu-id="c9a50-114">Jedes U-oder V-Byte hat einen Wert zwischen 0 (null) und 255.</span><span class="sxs-lookup"><span data-stu-id="c9a50-114">Each U or V byte has a value between zero and 255.</span></span> <span data-ttu-id="c9a50-115">Das Plug-in passt die einzelnen Werte zuerst so an, dass Sie durch einen Bereich von-128 bis 127 dargestellt werden, und skaliert den Wert dann mit dem angegebenen Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="c9a50-115">The plug-in first adjusts each value to be represented by a range from -128 to 127, and then scales the value by the supplied scale factor.</span></span> <span data-ttu-id="c9a50-116">Schließlich passt der Code den Wert für den ursprünglichen Bereich von 0 bis 255 erneut an und kopiert die Daten in den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="c9a50-116">Finally, the code adjusts the value again for the original zero-to-255 range and copies the data to the output buffer.</span></span> <span data-ttu-id="c9a50-117">Im folgenden Beispielcode wird das-Video verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c9a50-117">The following example code processes UYVY video.</span></span> <span data-ttu-id="c9a50-118">In diesem Format ist jedes andere Byte ein U-oder Y-Wert.</span><span class="sxs-lookup"><span data-stu-id="c9a50-118">In this format, every other byte is a U or Y value.</span></span>


```C++
while( dwHeight-- )
{
    DWORD x = dwWidth; 

        while( x-- )
        {
        // Scale the U and V bytes to 128.
        // Just copy the Y bytes.
        if( x%2 )
        {
            pbTarget[x] = pbSource[x];
        }
        else
        {
            long temp = (long)((pbSource[x] - 128) * m_fScaleFactor);

            // Truncate if exceeded full scale.
            if (temp > 127)
            temp = 127;
            if (temp < -128)
            temp = -128;

            pbTarget[x] = temp + 128;
        }
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="c9a50-119">Bei RGB-Videos werden die Farb-und Beleuchtungs Informationen als separate rote, grüne und blaue Werte codiert.</span><span class="sxs-lookup"><span data-stu-id="c9a50-119">For RGB video, the color and luminance information is encoded as separate red, green, and blue values.</span></span> <span data-ttu-id="c9a50-120">Das Beispiel-Plug-in berechnet den Mittelwert der drei Werte, um den Wert für grau zu bestimmen, und passt dann die einzelnen Farbwerte mithilfe des bereitgestellten Skalierungsfaktors an.</span><span class="sxs-lookup"><span data-stu-id="c9a50-120">The sample plug-in computes the average of the three values to determine the value for gray, and then adjusts each color value by using the supplied scale factor.</span></span> <span data-ttu-id="c9a50-121">Auch hier müssen die Werte für den Bereich von-128 bis 127 vor der Skalierung normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c9a50-121">Once again, the values must be normalized for the -128 to 127 range before scaling.</span></span> <span data-ttu-id="c9a50-122">Der folgende Code aus Process32Bit zeigt den Prozess für RGB32:</span><span class="sxs-lookup"><span data-stu-id="c9a50-122">The following code from Process32Bit shows the process for RGB32:</span></span>


```C++
while( dwHeight-- )
{
    RGBQUAD* pPixelIn = (RGBQUAD*)pbSource;
    RGBQUAD* pPixelOut = (RGBQUAD*)pbTarget;

    for( DWORD x = 0; x < dwWidth; x++ )
    {
    // Get the color bytes.
    long lBlue = (long) pPixelIn[x].rgbBlue;
    long lGreen = (long) pPixelIn[x].rgbGreen;
    long lRed = (long) pPixelIn[x].rgbRed;

    // Compute the average for gray.
    long lAverage = ( lBlue + lGreen + lRed ) / 3;

    // Scale the colors to the average.
    pPixelOut[x].rgbBlue = (BYTE)( ( lBlue - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbGreen = (BYTE)( ( lGreen - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbRed = (BYTE)( ( lRed - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbReserved = pPixelIn[x].rgbReserved;
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="c9a50-123">Weitere Informationen zu Videoformaten finden Sie auf der [FourCC-Website](../directshow/fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c9a50-123">For more information about video formats, see the [FourCC website](../directshow/fourcc-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9a50-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9a50-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9a50-125">**Implementieren eines Video DSP-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="c9a50-125">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 
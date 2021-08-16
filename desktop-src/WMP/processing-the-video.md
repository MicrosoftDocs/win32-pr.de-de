---
title: Verarbeiten des Videos
description: Verarbeiten des Videos
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Windows Media Player-Plug-Ins, Video-DSP
- Plug-Ins, Video-DSP
- Digitale Signalverarbeitungs-Plug-Ins, Videoverarbeitung
- DSP-Plug-Ins, Videoverarbeitung
- Video-DSP-Plug-Ins, Verarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea168199270cfe8029b7b9303a7745db2c255f4268252a5bd80472a73c6f2f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334023"
---
# <a name="processing-the-video"></a>Verarbeiten des Videos

Die Details der Videoverarbeitung variieren je nach Format. es geht über den Rahmen dieser Dokumentation hinaus, diese Details anzugeben. Im Allgemeinen besteht das Ziel des Plug-Ins darin, die Farbdaten im Eingabepuffer zu ändern und dann die Daten in den Ausgabepuffer zu kopieren.

Das Beispiel-Plug-In verarbeitet zwei Arten von Videoformaten: YUV und RGB.

Für YUV-Videos werden die Rot- und Blaufarbeninformationen in den You- und V-Werten codiert, und die Leuchtdichteebene wird durch den Y-Wert dargestellt. der grüne Wert ist codiert und kann mithilfe eines Algorithmus wiederhergestellt werden. Das Beispiel-Plug-In ändert einfach die You- und V-Werte, um die Farbebene zu beeinflussen. Jedes U- oder V-Byte hat einen Wert zwischen 0 und 255. Das Plug-In passt zunächst jeden Wert so an, dass er durch einen Bereich von -128 bis 127 dargestellt wird, und skaliert den Wert dann nach dem angegebenen Skalierungsfaktor. Schließlich passt der Code den Wert erneut für den ursprünglichen Bereich von 0 bis 255 an und kopiert die Daten in den Ausgabepuffer. Im folgenden Beispielcode wird das UYVY-Video verarbeitet. In diesem Format ist jedes andere Byte ein U- oder Y-Wert.


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



Für RGB-Videos werden die Informationen zu Farbe und Leuchtdichte als separate Werte für Rot, Grün und Blau codiert. Das Beispiel-Plug-In berechnet den Durchschnitt der drei Werte, um den Wert für Grau zu bestimmen, und passt dann jeden Farbwert mithilfe des angegebenen Skalierungsfaktors an. Auch hier müssen die Werte vor der Skalierung für den Bereich -128 bis 127 normalisiert werden. Der folgende Code aus Process32Bit zeigt den Prozess für RGB32:


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



Weitere Informationen zu Videoformaten finden Sie auf der [FourCC-Website.](../directshow/fourcc-codes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Video-DSP-Plug-Ins**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 
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
# <a name="processing-the-video"></a>Verarbeiten des Videos

Die Details des Verarbeitungs Videos variieren je nach Format. Diese Details werden über den Rahmen dieser Dokumentation hinausgehen. Im Allgemeinen ist das Ziel des Plug-ins, die Farbdaten im Eingabepuffer zu ändern und die Daten dann in den Ausgabepuffer zu kopieren.

Das Beispiel-Plug-in verarbeitet zwei Arten von Videoformaten: YUV und RGB.

Bei einem YUV-Video werden die roten und blauen Farbinformationen in den Werten "You" und "V" codiert, und die Leuchtkraft Ebene wird durch den Y-Wert dargestellt. der grüne Wert ist codiert und kann mithilfe eines Algorithmus wieder hergestellt werden. Das Beispiel-Plug-in ändert einfach die Werte von "You" und "V", um die Farbstufe zu beeinflussen Jedes U-oder V-Byte hat einen Wert zwischen 0 (null) und 255. Das Plug-in passt die einzelnen Werte zuerst so an, dass Sie durch einen Bereich von-128 bis 127 dargestellt werden, und skaliert den Wert dann mit dem angegebenen Skalierungsfaktor. Schließlich passt der Code den Wert für den ursprünglichen Bereich von 0 bis 255 erneut an und kopiert die Daten in den Ausgabepuffer. Im folgenden Beispielcode wird das-Video verarbeitet. In diesem Format ist jedes andere Byte ein U-oder Y-Wert.


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



Bei RGB-Videos werden die Farb-und Beleuchtungs Informationen als separate rote, grüne und blaue Werte codiert. Das Beispiel-Plug-in berechnet den Mittelwert der drei Werte, um den Wert für grau zu bestimmen, und passt dann die einzelnen Farbwerte mithilfe des bereitgestellten Skalierungsfaktors an. Auch hier müssen die Werte für den Bereich von-128 bis 127 vor der Skalierung normalisiert werden. Der folgende Code aus Process32Bit zeigt den Prozess für RGB32:


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



Weitere Informationen zu Videoformaten finden Sie auf der [FourCC-Website](../directshow/fourcc-codes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Video DSP-Plug-ins**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 
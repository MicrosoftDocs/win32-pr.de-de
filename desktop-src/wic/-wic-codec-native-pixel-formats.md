---
description: In diesem Thema werden die Pixelformate vorgestellt, die von der Windows Imaging Component (WIC) bereitgestellt werden.
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: Übersicht über native Pixelformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379e67d422ccbd05ef178e67eb25c973e6b5943ef85d22873097f245f8914a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206338"
---
# <a name="native-pixel-formats-overview"></a>Übersicht über native Pixelformate

In diesem Thema werden die Pixelformate vorgestellt, die von der Windows Imaging Component (WIC) bereitgestellt werden.

Ein Pixelformat beschreibt das Speicherlayout jedes Pixels in einer Bitmap. Dieses Speicherlayout beschreibt, wie die Bilddaten einer Bitmap codiert werden, indem das numerische Format und die Farbkanalorganisation angegeben werden. WIC unterstützt mehrere numerische Formate für mehrere Farbkanalorganisationsschemas und bietet eine Vielzahl von Pixelformaten.

-   [Bittiefe](#bit-depth)
-   [Numerische Codierung](#numerical-encoding)
-   [Farbkanäle](#color-channels)
    -   [RGB-/BGR-Farbmodell](#rgbbgr-color-model)
    -   [CMYK-Farbmodell](#cmyk-color-model)
    -   [n-Kanal-Farbmodell](#n-channel-color-model)
    -   [Indizierte und Graustufenfarbmodelle](#indexed-and-grayscale-color-models)
    -   [Y'CbCr-Farbmodell](#ycbcr-color-model)
-   [WIC-Pixelformat](#wic-pixel-format)
    -   [Nicht definierte Pixelformate](#undefined-pixel-formats)
    -   [Indizierte Pixelformate](#indexed-pixel-formats)
    -   [Gepackte Bitpixelformate](#packed-bit-pixel-formats)
    -   [Graustufenpixelformate](#grayscale-pixel-formats)
    -   [RGB-/BGR-Pixelformate](#rgbbgr-pixel-formats)
    -   [CMYK-Pixelformate](#cmyk-pixel-formats)
    -   [n-Kanal-Pixelformate](#n-channel-pixel-formats)
    -   [Nur Alphapixelformate](#alpha-only-pixel-formats)
    -   [Y'CbCr-Pixelformate](#ycbcr-pixel-formats)
-   [Farbraum](#color-space)
-   [Native Imageformate](#native-image-formats)
    -   [Nativer BMP-Codec](#bmp-native-codec)
    -   [Nativer GIF-Codec](#gif-native-codec)
    -   [Nativer ICO-Codec](#ico-native-codec)
    -   [Nativer JPEG-Codec](#jpeg-native-codec)
    -   [Nativer PNG-Codec](#png-native-codec)
    -   [Nativer TIFF-Codec](#tiff-native-codec)
    -   [Nativer JPEG-XR-Codec](#jpeg-xr-native-codec)
-   [Nativer DDS-Codec](#dds-native-codec)
-   [Erweiterbarkeit des Pixelformats](#pixel-format-extensibility)
-   [Zugehörige Themen](#related-topics)

## <a name="bit-depth"></a>Bittiefe

Die *Bittiefe* ist die Anzahl der Bits, die zum Codieren der einzelnen Farbkanäle verwendet werden. Heutzutage verwenden die meisten digitalen Bilder eine Bittiefe von 8. Dies bedeutet, dass jeder Farbkanal in einem Pixel durch 8 Bits dargestellt wird und 2⁸ (256) eindeutige Werte pro Kanal bereitstellt. Ein Bild mit einer Bittiefe von 8 und drei Farbkanälen (z. B. Rot, Grün und Blau) verwendet 24 Bits pro Pixel (bpp), wodurch 2issen⁴ (16.777.216) verschiedene Farben pro Pixel zur Verfügung steht.

Für eine bessere Farbauflösung kann eine Bittiefe von 16 oder 32 verwendet werden. Dadurch wird jeder Farbkanal mit eindeutigen Werten von 2⁶ (65.536) oder 2.000 eindeutigen Werten auf Kosten von mehr Arbeitsspeicher pro Pixel zur Verfügung stellen.

In einigen Formaten ist die Bittiefe kein Vielfaches von 8. Diese Formate werden als *gepackte* Formate bezeichnet, da die Farbkanäle in einem Pixel nicht an Bytegrenzen ausgerichtet sind. Wenn die Bittiefe beispielsweise 5 beträgt, können drei Farbkanäle in 16 Bits gespeichert werden (einschließlich 1 Bit Auffüllung, um Pixel bytebündig auszurichten). Gepackte Formate sind nützlich, wenn arbeitsspeicher- oder verarbeitungsleistungsbeschränkt sind.

## <a name="numerical-encoding"></a>Numerische Codierung

Für den Großteil der heutigen digitalen Bilder werden Unsigned Bytes und unsigned short integers verwendet, um den numerischen Bereich jedes Farbkanals zu beschreiben. Der Mindestwert (0) stellt die Intensität 0 (null) in einem einzelnen Farbkanal dar, und Schwarz wird erreicht, wenn alle Farbkanäle null sind. Auf ähnliche Weise stellt der maximale Wert die vollständige Intensität dar, und Weiß wird erreicht, wenn alle Farbkanäle eine volle Intensität aufweisen. Bei einer Bittiefe von 8 stellt ein UINT 256 eindeutige Werte pro Farbkanal (0 bis 255) bereit. Ein 16-Bit-UINT bietet 65.536 eindeutige Werte pro Farbkanal (0 bis 65.535).

Darüber hinaus unterstützt WIC Festkomma- und Gleitkommaformate. Diese Formate unterstützen größere dynamische Bereiche, da der gesamte numerische Bereich jedes Farbkanals größer als der sichtbare Bereich ist. Daher können Farben während der Zwischenschritte der Bildverarbeitung oberhalb oder unterhalb des sichtbaren Bereichs angepasst werden, ohne dass Bildinformationen verloren geht.

### <a name="fixed-point-numerical-encoding"></a>Fixed-Point numerische Codierung

16-Bit-Festkommawerte werden als s2.13 interpretiert: Vorzeichenbit, zwei ganzzahlige Bits und 13 Sekundenbruchteile. Bei verwendung dieser Interpretation ein numerischer Bereich von –4,0 bis +3,999... kann dargestellt werden, wobei der Wert 1,0 durch den ganzzahligen Wert 8192 (0x2000) dargestellt wird.

32-Bit-Festkommawerte werden als s7.24 interpretiert: Vorzeichenbit, sieben ganzzahlige Bits und 24 Bruchbits. Bei verwendung dieser Interpretation ein numerischer Bereich von –128,0 bis +127,999... kann dargestellt werden, wobei der Wert 1,0 durch den ganzzahligen Wert mit Vorzeichen 16777216 (0x01000000) dargestellt wird.

## <a name="color-channels"></a>Farbkanäle

Die Farbkanäle eines Pixelformats definieren das Speicherlayout jeder Farbe innerhalb der Bilddaten einer Bitmap. In den heutigen digitalen Bildern gibt es eine Vielzahl verschiedener Farbkanalstrukturen, und WIC bietet Unterstützung für viele dieser Strukturen.

### <a name="rgbbgr-color-model"></a>RGB-/BGR-Farbmodell

RGB- und BGR-Formate beschreiben Farben in einem additiven Farbmodell. Die gängigste Methode zur Beschreibung eines Bilds besteht darin, drei separate Farbkanäle zu verwenden, die die Farben Rot (R), Grün (G) und Blau (B) darstellen. WIC bietet Unterstützung für diese drei Kanäle in der Reihenfolge rot-grün-blau (RGB) oder blau-grün-rot (BGR). Dies ist die Reihenfolge, in der jeder Farbkanal innerhalb des sequenziellen Bitstreams angezeigt wird. Im \_ GUID-Format WICPixelFormat32bppRGB ist jedes Pixel beispielsweise 32 Bit breit. Der rote Kanal ist das erste (am wenigsten signifikante) Byte im Arbeitsspeicher, gefolgt von grün und dann blau. Umgekehrt sind die Farbkanäle im \_ GUID WICPixelFormat32bppBGR-Format in umgekehrter Reihenfolge. WIC unterstützt eine Reihe von RGB-/BGR-Formaten, einschließlich spezieller gepackter Bitformate wie GUID \_ WICPixelFormat16bppBGR555.

> [!Note]  
> Die Farbkanäle der speziellen BGR-gepackten Bitformate sind nicht in Vielfachen von 8 enthalten, wie die Farbkanäle in typischen Pixelformaten. Dies bedeutet, dass die Kanalwerte nicht bytebündig ausgerichtet sind. Beim Lesen von gepackten Bitfarbkanälen muss Vorsicht walten lassen.

 

Zusätzlich zum RGB- und BGR-Format bietet WIC auch RGB- und BGR-Pixelformate, die einen Alphakanal (A) unterstützen. Der Alphakanal stellt Deckkraftdaten für das Pixel bereit. Bei Formaten mit einem hinzugefügten Alphakanal ist der Alphakanal in der Regel der letzte in der Reihenfolge des Farbkanals. Im Pixelformat GUID \_ WICPixelFormat32bppBGRA ist die Bytereihenfolge beispielsweise blau, grün und rot, gefolgt vom Alphakanal.

WIC unterstützt auch vormultiplikierte Alpha-RGB-Pixelformate (P). In einem typischen RGBA-Pixelformat sind die Farbwerte rot, grün und blau die tatsächlichen Farbwerte für das Bild. Um ein zusammengesetztes Bild im RGBA-Standardformat zu erstellen, muss der Alphawert des Vordergrundbilds mit jedem der roten, grünen und blauen Kanäle multipliziert werden, bevor er der Farbe des Hintergrundbilds hinzugefügt wird. In einem vormultiplizierten Alpha-RGB-Pixelformat wurde jeder Farbkanal bereits mit dem Alphawert multipliziert. Dies bietet eine effizientere Methode der Bildkomposition mit Alphakanaldaten. Um die echten Farbwerte jedes Kanals in einem PRGBA-/PBGRA-Pixelformat abzurufen, muss die Alphakanalmultiplikation durch Division von Farbwerten durch den Alphawert umgekehrt werden.

### <a name="cmyk-color-model"></a>CMYK-Farbmodell

CMYK ist ein subtrahtives Farbmodell, das beim Drucken verwendet wird. Die von einem CMYK-Modell erzeugten Farben werden durch das Licht generiert, das nicht aufgenommen, sondern reflektiert wird. CMYK ist ein Vierkanalmodell von Cyan (C), Magenta (M), Gelb (Y) und Schwarz (K). Wenn alle vier Farbkanäle den Maximalwert aufweisen, ist das Ergebnis schwarz. Wie die RGB-/BGR-Farbmodelle wird die Bytereihenfolge innerhalb des sequenziellen Bitstreams durch den Namen des Pixelformats angegeben. Beispielsweise besteht jedes Pixel im Pixelformat GUID \_ WICPixelFormat32bppCMYK aus 32 Bits. Das erste Byte enthält den Cyan-Wert, gefolgt von Magenta, Gelb und Schwarz. WIC bietet Pixelformate für CMYK mit 32 und 64 Bits pro Pixel (bpp).

Zusätzlich zum CMYK-Standardfarbmodell stellt WIC auch CMYK mit Alpha zur Verfügung. Dadurch können CMYK-Bilder alphanumerische Daten aufweisen, die dem RGB-/BGR-Farbmodell ähneln. Der Alphakanal befindet sich unmittelbar nach Schwarz im sequenziellen Bitstream einer Bitmap.

### <a name="n-channel-color-model"></a>n-Kanal-Farbmodell

Aus Gründen der Flexibilität bietet WIC auch Pixelformate, die keine vordefinierte Kanalreihenfolge aufweisen. WIC bietet Pixelformate, die zwischen drei und acht Kanäle kontinuierlicher Bilddaten in Bittiefe von 8 und 16 unterstützen. Im Gegensatz zu den RGB-/BGR- und CMYK-Pixelformaten geben n-Kanalformate nicht die Kanalreihenfolge an, sondern die Anzahl der verfügbaren Farbkanäle. Beispielsweise besteht jedes Pixel im Pixelformat GUID \_ WICPixelFormat32bpp4Channels aus 32 Bits, wobei jeder der vier Kanäle ein einzelnes Byte belegt.

WIC stellt auch Pixelformate für n-Kanal mit Alpha bereit. Dadurch können n-Kanalbilder alphanumerische Daten aufweisen, die den RGB-/BGR- und CMYK-Farbmodellen ähneln. Der Alphakanal befindet sich unmittelbar nach dem letzten Farbkanal im sequenziellen Bitstream einer Bitmap.

### <a name="indexed-and-grayscale-color-models"></a>Indizierte und Graustufenfarbmodelle

*Indizierte* Formate verwenden eine Tabelle mit Farben, die als *Palette* bezeichnet wird. Die Palette wird extern für die Pixeldaten gespeichert oder implizit definiert. Der Wert jedes Pixels im Bild ist ein Index in der Palette. Bei einem indizierten Format hängt die Anzahl der Bits pro Pixel direkt mit der Anzahl der Einträge in der Palette zusammen. Dadurch wird die Datenmenge, die zum Darstellen des Bilds erforderlich ist, erheblich reduziert, aber auch die Anzahl der für das Bild verfügbaren Farben eingeschränkt. WIC unterstützt indizierte Formate mit 1, 2, 4 oder 8 BPP.

Für Monocolore-Formate (Graustufen) unterstützt WIC 1, 2, 4, 8, 16 und 32 Bits pro Pixel. Bei Bittiefe von 1, 8, 16 und 32 werden die Farbdaten in einem einzigen Kanal gespeichert. Bei Bittiefe von 2 oder 4 sind Pixel Indizes in einer Graustufenpalette.

### <a name="ycbcr-color-model"></a>Y'CbCr-Farbmodell

WIC fügt Unterstützung für das JPEG JFIF Y'CbCr-Farbmodell hinzu. Y'CbCr trennt Farben in eine Lumakomponente (Y') und zwei Komponenten (Cb und Cr). Viele JPEG-Dateien speichern Bilddaten nativ mithilfe des Y'CbCr-Farbmodells.

Das menschliche visuelle System reagiert weniger empfindlich auf Änderungen in der Färbung als auf Luma, und Y'CbCr-Formate können von dieser geringeren Empfindlichkeit profitieren, indem sie die Menge der Imkdaten reduzieren, die relativ zu luma gespeichert werden. Sie erreichen dies, indem sie "luma" und "luma" in separaten Ebenen speichern und jede Komponentenebene auf eine andere Auflösung skalieren. Diese Vorgehensweise wird als Subsampling für Diensampling bezeichnet.

Da Luma- und Lumadaten separat gespeichert werden und unterschiedliche Auflösungen aufweisen können, definiert WIC separate Luma- und Pixelformate für Pixel. WIC unterstützt Daten mit 8 Bits pro Kanal.

## <a name="wic-pixel-format"></a>WIC-Pixelformat

Die Pixelformate in WIC werden mithilfe von GUIDs definiert, um Konflikte mit IHVs zu vermeiden. WIC stellt einen Anzeigenamen bereit, um auf die GUID eines nativen Pixelformats zu verweisen. Die Benennungskonvention für die WIC-Pixelformate lautet wie folgt:

**\[GUID \_ WICPixelFormat \] \[ Bits Per Pixel \] \[ Channel Order Storage \] \[ Type\]**

| Formatkomponente         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ WICPixelFormat** | Die beschreibende Identifikation für alle WIC-Pixelformate. Der Anzeigename für alle WIC-Pixel beginnt mit dieser Zeichenfolge.                                                                                                                                                                                       |
| **Bits pro Pixel**       | Die Anzahl der Bits pro Pixel (bpp), die für das Pixelformat verwendet werden.                                                                                                                                                                                                                                                |
| **Kanalreihenfolge**        | Das Farbkanalmodell und die Reihenfolge der einzelnen Kanäle für das Format.                                                                                                                                                                                                                                            |
| **Speichertyp**         | Die numerische Codierung, die für das Pixelformat verwendet wird. Die Standardcodierung ist eine ganze Zahl ohne Vorzeichen. Wenn den Farbmodellinformationen nichts folgt, wird eine ganze Zahl ohne Vorzeichen (UINT) impliziert. FixedPoint und Float werden verwendet, um Pixelformate zu identifizieren, die Festkomma- bzw. Gleitkommacodierung verwenden. |



 

> [!Note]  
> Bei n-Kanal-Formaten \[ gibt die Kanalreihenfolge \] nicht die Farbreihenfolge an, sondern die Anzahl der verfügbaren Kanäle. Beispielsweise stellt GUID \_ WICPixelFormat24bpp3Channels drei Farbkanäle bereit, wobei "3Channels" der \[ Eintrag \] Kanalreihenfolge ist, aber nur die Anzahl der Kanäle und nicht die Reihenfolge angibt.

 

Der Anzeigename GUID \_ WICPixelFormat24bppRGB bedeutet beispielsweise, dass das Pixelformat 24 Bit pro Pixel und das RGB-Farbmodell verwendet. Da der Name einen Speichertyp nicht explizit identifiziert, wird eine ganze Zahl ohne Vorzeichen impliziert.

WIC unterstützt mehrere Pixelformate. In den folgenden Tabellen werden ähnliche Pixelformate nach Farbstruktur gruppiert, während zusätzliche Informationen wie Bittiefe, Bits pro Pixel und numerische Codierung angegeben werden. Jede Tabelle enthält die folgenden Informationen:

-   **Anzeigename**. Der Anzeigename des Pixelformats.
-   **Kanalanzahl**. Die Anzahl der Farbkanäle.
-   **Bits pro Kanal.** Die Anzahl der Bits pro Kanal (Bittiefe).
-   **Bits pro Pixel.** Die Anzahl der Bits pro Pixel, einschließlich aller Auffüllungsbits.
-   **Storage Geben Sie ein.** Die numerische Codierung der Bilddaten. Dieser Wert kann eine ganze Zahl ohne Vorzeichen (UINT), eine Festkommazahl (FixedPoint) oder eine Gleitkommazahl (Float) sein.

> [!Note]  
> Aus Gründen der Übersichtlichkeit bezieht sich dieses Dokument nur anhand ihrer Anzeigenamen auf Pixelformate. Den tatsächlichen Hexadezimalwert für die Pixelformate finden Sie in den wincodec.h/idl-Dateien.

 

### <a name="undefined-pixel-formats"></a>Nicht definierte Pixelformate

Die folgende Liste zeigt generische Pixelformate, die verwendet werden, wenn das Pixelformat nicht definiert ist oder für einen Bildvorgang unwichtig ist.

-   GUID \_ WICPixelFormatUndefined
-   GUID \_ WICPixelFormatDontCare

### <a name="indexed-pixel-formats"></a>Indizierte Pixelformate

In der folgenden Tabelle sind die von WIC bereitgestellten indizierten Pixelformate aufgeführt. In diesen Formaten ist der Wert für jedes Pixel ein Index in einer Farbpalette.



| Anzeigename                   | Kanalanzahl | Bits pro Pixel | Speichertyp |
|---------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat1bppIndexed | 1             | 1              | UINT         |
| GUID \_ WICPixelFormat2bppIndexed | 1             | 2              | UINT         |
| GUID \_ WICPixelFormat4bppIndexed | 1             | 4              | UINT         |
| GUID \_ WICPixelFormat8bppIndexed | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>Gepackte Bitpixelformate

In der folgenden Tabelle sind die von WIC bereitgestellten gepackten Bitformate aufgeführt. In diesen Formaten werden Farbkanaldaten nicht bytebündig ausgerichtet.



| Anzeigename                          | Kanalanzahl | Bits pro Kanal       | Bits pro Pixel | Speichertyp |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| GUID \_ WICPixelFormat16bppBGR555           | 3             | 5                      | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGR565           | 3             | 5(B)/6(G)/5(R)         | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGRA555          | 4             | 5(B)/5(G)/5(R)/1(A)    | 16             | UINT         |
| GUID \_ WICPixelFormat32bppBGR101010        | 3             | 10                     | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102      | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102XR    | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2      | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |

Für die Formate GUID \_ WICPixelFormat32bppBGR101010 und GUID \_ WICPixelFormat32bppRGBA1010102 wird der rote Kanal in den am wenigsten wichtigen Bits gespeichert. Für die FORMATE GUID \_ WICPixelFormat32bppR10G10B10A2 und GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 wird der rote Kanal in den wichtigsten Bits definiert, das gleiche Layout wie [DXGI_FORMAT_R10G10B10A2_UNORM](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

Das \_ GUID-Format WICPixelFormat32bppR10G10B10A2HDR10 ist das 10-Bit-Pixelformat für HDR10 (BT.2020-Farbraum und SMPTE ST.2084 EOTF).

### <a name="grayscale-pixel-formats"></a>Graustufenpixelformate

In der folgenden Tabelle sind die von WIC bereitgestellten Graustufenformate aufgeführt. In diesen Formaten stellen Farbdaten Graustufen dar.



| Anzeigename                           | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|-----------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormatBlackWhite          | 1             | 1                | 1              | UINT         |
| GUID \_ WICPixelFormat2bppGray            | 1             | 2                | 2              | UINT         |
| GUID \_ WICPixelFormat4bppGray            | 1             | 4                | 4              | UINT         |
| GUID \_ WICPixelFormat8bppGray            | 1             | 8                | 8              | UINT         |
| GUID \_ WICPixelFormat16bppGray           | 1             | 16               | 16             | UINT         |
| GUID \_ WICPixelFormat16bppGrayFixedPoint | 1             | 16               | 16             | FixedPoint   |
| GUID \_ WICPixelFormat16bppGrayHalf       | 1             | 16               | 16             | Float        |
| GUID \_ WICPixelFormat32bppGrayFloat      | 1             | 32               | 32             | Float        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint | 1             | 32               | 32             | FixedPoint   |



 

### <a name="rgbbgr-pixel-formats"></a>RGB/BGR-Pixelformate

In der folgenden Tabelle sind die RGB/BGR-Formate aufgeführt, die von WIC bereitgestellt werden. Diese Formate trennen die Primärfarbdaten in die Kanäle Rot (R), Grün (G) und Blau (B). Für Deckkraftinformationen in einigen Formaten wird ein zusätzlicher Alphakanal (A) bereitgestellt.



| Anzeigename                            | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bppRGB             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat24bppBGR             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat32bppBGR             | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppBGRA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBE\*          | 4             | 8                | 32             | Float        |
| GUID \_ WICPixelFormat32bppPRGBA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppPBGRA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat48bppRGB             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppBGR             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | 3             | 16               | 48             | Fest        |
| GUID \_ WICPixelFormat48bppBGRFixedPoint   | 3             | 16               | 48             | Fest        |
| GUID \_ WICPixelFormat48bppRGBHalf         | 3             | 16               | 48             | Float        |
| GUID \_ WICPixelFormat64bppRGBA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppBGRA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPRGBA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPBGRA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | 3             | 16               | 64             | Fest        |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | 4             | 16               | 64             | Fest        |
| GUID \_ WICPixelFormat64bppBGRAFixedPoint  | 4             | 16               | 64             | Fest        |
| GUID \_ WICPixelFormat64bppRGBHalf         | 3             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat64bppRGBAHalf        | 4             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | 3             | 32               | 96             | Fest        |
| GUID \_ WICPixelFormat128bppRGBFloat       | 3             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBAFloat      | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppPRGBAFloat     | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | 3             | 32               | 128            | Fest        |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | 4             | 32               | 128            | Fest        |



 

> [!Note]  
> \*Das GUID \_ WICPixelFormat32bppRGBE-Format codiert drei 16-Bit-Gleitkommawerte in 4 Bytes wie folgt: Drei 8-Bit-Mantisse ohne Vorzeichen für die R-, G- und B-Kanäle sowie einen freigegebenen 8-Bit-Exponenten. Dieses Format bietet 16-Bit-Gleitkommagenauigkeit in einer kleineren Pixeldarstellung.

 

Ab Windows 8 und dem [Plattformupdate für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)bietet WIC zusätzliche Formate, wie in der tabelle hier gezeigt.



| Anzeigename                      | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppRGB       | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppRGB       | 3             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat96bppRGBFloat  | 3             | 32               | 96             | GLEITKOMMAZAHL        |
| GUID \_ WICPixelFormat64bppPRGBAHalf | 4             | 16               | 64             | GLEITKOMMAZAHL        |



 

### <a name="cmyk-pixel-formats"></a>CMYK-Pixelformate

In der folgenden Tabelle sind die von WIC bereitgestellten CMYK-Formate aufgeführt. Diese Formate trennen die Primären Farbdaten in Cyan-Kanäle (C), Magenta-Kanäle (M), gelben (Y) und schwarzen Kanälen (K).



| Anzeigename                      | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppCMYK      | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppCMYK      | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bppCMYKAlpha | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bppCMYKAlpha | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>n-Kanal-Pixelformate

In der folgenden Tabelle sind die von WIC bereitgestellten n-kanal-Formate aufgeführt. Diese Formate stellen eine Reihe von nicht definierten Farbkanälen zum Speichern von Bilddaten zur Verfügung.



| Anzeigename                            | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bpp3Channels       | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat48bpp3Channels       | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat32bpp4Channels       | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp4Channels       | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bpp4ChannelsAlpha  | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat40bpp5Channels       | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp5Channels       | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat48bpp5ChannelsAlpha  | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat48bpp6Channels       | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp6Channels       | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat56bpp6ChannelsAlpha  | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat56bpp7Channels       | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp7Channels      | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat64bpp8Channels       | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp8Channels      | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | 9             | 8                | 72             | UINT         |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | 9             | 16               | 144            | UINT         |



 

### <a name="alpha-only-pixel-formats"></a>Nur Alpha-Pixelformate

In der folgenden Tabelle sind die von WIC bereitgestellten Alpha-Only-Formate aufgeführt. Dieses Format enthält nur Alphainformationen.



| Anzeigename                 | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|-------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppAlpha | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Y'CbCr Pixel-Formate

In der folgenden Tabelle sind die von WIC bereitgestellten Y'CbCr-Formate aufgeführt. In diesen Formaten werden die primären Farbdaten in Luma (Y), blauer Farbunterschied (Cb) und Roter Chomaunterschied (Cr) getrennt. Beachten Sie, dass diese Formate zum Speichern von JPEG JFIF Y'CbCr-Pixeldaten entworfen wurden.



| Anzeigename                 | Kanalanzahl | Bits pro Pixel | Speichertyp |
|-------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppY     | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCb    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCr    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat16bppCbCr | 2             | 16             | UINT         |



 

## <a name="color-space"></a>Farbraum

Pixelformate selbst haben keinen Farbraum. Im Allgemeinen ist der Farbraum eine semantische Interpretation der Pixelwerte, die vom Kontext der Bitmap abhängt. Einige Bilder identifizieren einen Farbkontext, der den Farbraum des Bilds definiert. Nur bei Fehlen eines Farbkontexts sollte der Farbraum abgeleitet werden.

Farbkontextinformationen werden von der [**IWICColorContext-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) für WIC definiert. Verwenden Sie die **GetColorContext-Methode,** um die Farbkontextinformationen für einen Bildrahmen abzurufen.

Wenn keine Farbrauminformationen für ein Bild vorliegen, ist die allgemeine Regel für den Farbraumrückschluss, dass UINT RGB- und Graustufenformate den RGB-Standardfarbraum (sRGB) verwenden, während die RGB- und Graustufenformate mit Festkomma- und Gleitkomma den erweiterten RGB-Farbraum (scRGB) verwenden. Das CPPE-Farbmodell verwendet einen RWOP-Farbraum.

## <a name="native-image-formats"></a>Native Bildformate

Jeder der Windows WIC-Codecs unterstützt eine Teilmenge der WIC-Pixelformate. Für jeden Codec können sich die unterstützten Decodierungsformate von den unterstützten Codierungsformaten unterscheiden.

Wenn beim Decodieren eines Bilds Daten nativ in einem Pixelformat gespeichert werden, das vom Decoder nicht unterstützt wird, werden sie in ein unterstütztes Format konvertiert. Um das Ausgabepixelformat zu bestimmen, rufen [**Sie IWICBitmapFrameDecode::GetPixelFormat auf.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

Verwenden Sie beim Codieren eines Bilds [**IWICBitmapFrameEncode::SetPixelFormat,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) um an fordern, dass der Encoder ein bestimmtes Pixelformat verwendet. Der Encoder gibt das nächstgelegene unterstützte Pixelformat zurück, das sich von dem angeforderten Format unterscheiden kann.

Die folgenden Tabellen zeigen die Pixelformate, die von den einzelnen bereitgestellten WIC Windows codecs unterstützt werden.

### <a name="bmp-native-codec"></a>Nativer BMP-Codec



| Decoderpixelformate                   | Encoder-Pixelformate                   |
|-----------------------------------------|-----------------------------------------|
| GUID \_ WICPixelFormat1bppIndexed         | GUID \_ WICPixelFormat1bppIndexed         |
| GUID \_ WICPixelFormat4bppIndexed         | GUID \_ WICPixelFormat4bppIndexed         |
| GUID \_ WICPixelFormat8bppIndexed         | GUID \_ WICPixelFormat8bppIndexed         |
| GUID \_ WICPixelFormat16bppBGR555         | GUID \_ WICPixelFormat16bppBGR555         |
| GUID \_ WICPixelFormat16bppBGR565         | GUID \_ WICPixelFormat16bppBGR565         |
| GUID \_ WICPixelFormat24bppBGR            | GUID \_ WICPixelFormat24bppBGR            |
| GUID \_ WICPixelFormat32bppBGR            | GUID \_ WICPixelFormat32bppBGR            |
| GUID \_ WICPixelFormat32bppBGRA\*         | GUID \_ WICPixelFormat32bppBGRA\*         |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint | GUID \_ WICPixelFormat32bppPBGRA          |
|                                         | GUID \_ WICPixelFormat64bppRGBAFixedPoint |
|                                         | GUID \_ WICPixelFormat64bppBGRAFixedPoint |



 

> [!Note]  
> GUID \_ WICPixelFormat32bppBGRA wird nur in Windows 8, dem [Plattformupdate für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)und höher unterstützt.
>
> -   Verwenden Sie zum Codieren in diesem Format die Encoderoption **EnableV5Header32bppBGRA.** Der BMP wird mit einem BITMAPV5HEADER-Header geschrieben.
> -   Wenn eine Datei über einen BITMAPV5HEADER verfügt, wird sie als GUID \_ WICPixelFormat32bppBGRA decodiert.

 

### <a name="gif-native-codec"></a>Nativer GIF-Codec



| Decoderpixelformate           | Encoderpixelformate           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |



 

### <a name="ico-native-codec"></a>Nativer ICO-Codec



| Decoderpixelformate         | Encoderpixelformate |
|-------------------------------|-----------------------|
| GUID \_ WICPixelFormat32bppBGRA |                       |



 

### <a name="jpeg-native-codec"></a>Nativer JPEG-Codec



| Decoderpixelformate         | Encoderpixelformate         |
|-------------------------------|-------------------------------|
| GUID \_ WICPixelFormat8bppGray  | GUID \_ WICPixelFormat8bppGray  |
| GUID \_ WICPixelFormat24bppBGR  | GUID \_ WICPixelFormat24bppBGR  |
| GUID \_ WICPixelFormat32bppCMYK | GUID \_ WICPixelFormat32bppCMYK |



 

### <a name="png-native-codec"></a>Nativer PNG-Codec



| Decoderpixelformate           | Encoderpixelformate           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat2bppIndexed | GUID \_ WICPixelFormat2bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite  | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat2bppGray    | GUID \_ WICPixelFormat2bppGray    |
| GUID \_ WICPixelFormat4bppGray    | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray    | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray   | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat24bppBGR    | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat32bppBGRA   | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat48bppRGB    | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat64bppRGBA   | GUID \_ WICPixelFormat48bppBGR    |
|                                 | GUID \_ WICPixelFormat64bppRGBA   |
|                                 | GUID \_ WICPixelFormat64bppBGRA   |



 

### <a name="tiff-native-codec"></a>Nativer TIFF-Codec



| Decoderpixelformate                | Encoderpixelformate           |
|--------------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed      | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed      | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed      | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite       | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat4bppGray         | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray         | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray        | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat32bppGrayFloat   | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat24bppBGR         | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat32bppBGRA        | GUID \_ WICPixelFormat32bppCMYK   |
| GUID \_ WICPixelFormat32bppPBGRA       | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat48bppRGB         | GUID \_ WICPixelFormat64bppRGBA   |
| GUID \_ WICPixelFormat32bppCMYK        |                                 |
| GUID \_ WICPixelFormat40bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat64bppRGBA        |                                 |
| GUID \_ WICPixelFormat64bppPRGBA       |                                 |
| GUID \_ WICPixelFormat64bppCMYK        |                                 |
| GUID \_ WICPixelFormat80bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat96bppRGBFloat\*  |                                 |
| GUID \_ WICPixelFormat128bppRGBAFloat  |                                 |
| GUID \_ WICPixelFormat128bppPRGBAFloat |                                 |



 

> [!Note]  
> GUID \_ WICPixelFormat96bppRGBFloat wird nur in Windows 8, dem [Plattformupdate für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)und höher unterstützt.

 

### <a name="jpeg-xr-native-codec"></a>Nativer JPEG-XR-Codec



| Decoderpixelformate                    | Encoderpixelformate                    |
|------------------------------------------|------------------------------------------|
| GUID \_ WICPixelFormatBlackWhite           | GUID \_ WICPixelFormatBlackWhite           |
| GUID \_ WICPixelFormat8bppGray             | GUID \_ WICPixelFormat8bppGray             |
| GUID \_ WICPixelFormat16bppBGR555          | GUID \_ WICPixelFormat16bppBGR555          |
| GUID \_ WICPixelFormat16bppGray            | GUID \_ WICPixelFormat16bppGray            |
| GUID \_ WICPixelFormat24bppBGR             | GUID \_ WICPixelFormat24bppBGR             |
| GUID \_ WICPixelFormat24bppRGB             | GUID \_ WICPixelFormat24bppRGB             |
| GUID \_ WICPixelFormat32bppBGR             | GUID \_ WICPixelFormat32bppBGR             |
| GUID \_ WICPixelFormat32bppBGRA            | GUID \_ WICPixelFormat32bppBGRA            |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | GUID \_ WICPixelFormat48bppRGBFixedPoint   |
| GUID \_ WICPixelFormat16bppGrayFixedPoint  | GUID \_ WICPixelFormat16bppGrayFixedPoint  |
| GUID \_ WICPixelFormat32bppBGR101010       | GUID \_ WICPixelFormat32bppBGR101010       |
| GUID \_ WICPixelFormat48bppRGB             | GUID \_ WICPixelFormat48bppRGB             |
| GUID \_ WICPixelFormat64bppRGBA            | GUID \_ WICPixelFormat64bppRGBA            |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat96bppRGBFixedPoint   |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat128bppRGBAFloat      |
| GUID \_ WICPixelFormat128bppRGBFloat       | GUID \_ WICPixelFormat128bppRGBFloat       |
| GUID \_ WICPixelFormat32bppC JPG            | GUID \_ WICPixelFormat32bppC JPG            |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | GUID \_ WICPixelFormat64bppRGBAFixedPoint  |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | GUID \_ WICPixelFormat128bppRGBAFixedPoint |
| GUID \_ WICPixelFormat64bppC JPG            | GUID \_ WICPixelFormat64bppC JPG            |
| GUID \_ WICPixelFormat24bpp3Channels       | GUID \_ WICPixelFormat24bpp3Channels       |
| GUID \_ WICPixelFormat32bpp4Channels       | GUID \_ WICPixelFormat32bpp4Channels       |
| GUID \_ WICPixelFormat40bpp5Channels       | GUID \_ WICPixelFormat40bpp5Channels       |
| GUID \_ WICPixelFormat48bpp6Channels       | GUID \_ WICPixelFormat48bpp6Channels       |
| GUID \_ WICPixelFormat56bpp7Channels       | GUID \_ WICPixelFormat56bpp7Channels       |
| GUID \_ WICPixelFormat64bpp8Channels       | GUID \_ WICPixelFormat64bpp8Channels       |
| GUID \_ WICPixelFormat48bpp3Channels       | GUID \_ WICPixelFormat48bpp3Channels       |
| GUID \_ WICPixelFormat64bpp4Channels       | GUID \_ WICPixelFormat64bpp4Channels       |
| GUID \_ WICPixelFormat80bpp5Channels       | GUID \_ WICPixelFormat80bpp5Channels       |
| GUID \_ WICPixelFormat96bpp6Channels       | GUID \_ WICPixelFormat96bpp6Channels       |
| GUID \_ WICPixelFormat112bpp7Channels      | GUID \_ WICPixelFormat112bpp7Channels      |
| GUID \_ WICPixelFormat128bpp8Channels      | GUID \_ WICPixelFormat128bpp8Channels      |
| GUID \_ WICPixelFormat40bppCLANGAlpha       | GUID \_ WICPixelFormat40bppCLANGAlpha       |
| GUID \_ WICPixelFormat80bppC ACHSEAlpha       | GUID \_ WICPixelFormat80bppC ACHSEAlpha       |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | GUID \_ WICPixelFormat32bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | GUID \_ WICPixelFormat40bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | GUID \_ WICPixelFormat48bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | GUID \_ WICPixelFormat56bpp6ChannelsAlpha  |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | GUID \_ WICPixelFormat64bpp7ChannelsAlpha  |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | GUID \_ WICPixelFormat72bpp8ChannelsAlpha  |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | GUID \_ WICPixelFormat64bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | GUID \_ WICPixelFormat80bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | GUID \_ WICPixelFormat96bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bppRGBAHalf        | GUID \_ WICPixelFormat112bpp6ChannelsAlpha |
| GUID \_ WICPixelFormat48bppRGBHalf         | GUID \_ WICPixelFormat128bpp7ChannelsAlpha |
| GUID \_ WICPixelFormat32bppRGBE            | GUID \_ WICPixelFormat144bpp8ChannelsAlpha |
| GUID \_ WICPixelFormat16bppGrayHalf        | GUID \_ WICPixelFormat64bppRGBAHalf        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint  | GUID \_ WICPixelFormat48bppRGBHalf         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | GUID \_ WICPixelFormat32bppRGBE            |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | GUID \_ WICPixelFormat16bppGrayHalf        |
| GUID \_ WICPixelFormat64bppRGBHalf         | GUID \_ WICPixelFormatBlackWhite           |



 

## <a name="dds-native-codec"></a>Nativer DDS-Codec



| Decoderpixelformate          | Encoder-Pixelformate          |
|--------------------------------|--------------------------------|
| GUID \_ WICPixelFormat32bppBGRA  | GUID \_ WICPixelFormat32bppBGRA  |
| GUID \_ WICPixelFormat32bppPBGRA | GUID \_ WICPixelFormat32bppPBGRA |



 

> [!Note]  
> Der bereitgestellte DDS Windows codec unterstützt DDS-Dateien, die mit den folgenden DXGI \_ FORMAT-Werten codiert werden:

 

-   DXGI \_ FORMAT \_ BC1 \_ UNORM
-   DXGI \_ FORMAT \_ BC2 \_ UNORM
-   DXGI \_ FORMAT \_ BC3 \_ UNORM

Diese werden als GUID \_ WICPixelFormat32bppBGRA oder GUID \_ WICPixelFormat32bppPBGRA decodiert und codiert. Weitere Informationen finden Sie unter Übersicht über [das DDS-Format.](dds-format-overview.md)

## <a name="pixel-format-extensibility"></a>Erweiterbarkeit des Pixelformats

Benutzerdefinierte Bildformate können Pixelformate verwenden, die nicht nativ von WIC bereitgestellt werden, z. B. YCbCr (YUV) und YCCK (Y/Cb/Cr/K). WIC bietet ein Erweiterbarkeitsmodell, mit dem sowohl integrierte als auch Add-In-Pixelformate innerhalb derselben Bildverarbeitungspipeline funktionieren können. Um diese Pixelformate in die WIC-Bildverarbeitungspipeline zu integrieren, müssen Sie Pixelformatkonverter erstellen, um Add-In-Pixelformate in ein oder mehrere native Pixelformate zu konvertieren. Die Hauptschnittstelle zum Erstellen von Formatkonvertern ist [**IWICFormatConverter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-GUIDs und CLSIDs](-wic-guids-clsids.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 

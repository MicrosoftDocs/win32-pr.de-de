---
description: In diesem Thema werden die Pixel Formate von Windows Imaging Component (WIC) vorgestellt.
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: Übersicht über Native Pixel Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df37481399ac8193effc5d8f93aa49050460ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362333"
---
# <a name="native-pixel-formats-overview"></a>Übersicht über Native Pixel Formate

In diesem Thema werden die Pixel Formate von Windows Imaging Component (WIC) vorgestellt.

Ein Pixel Format beschreibt das Speicher Layout der einzelnen Pixel in einer Bitmap. In diesem Speicher Layout wird beschrieben, wie die Bilddaten einer Bitmap codiert werden, indem das numerische Format und die Farb Kanal Organisation angegeben werden. WIC unterstützt mehrere numerische Formate für mehrere Farb Kanal-Organisations Schemas, die eine Vielzahl von Pixel Formaten bereitstellen.

-   [Bittiefe](#bit-depth)
-   [Numerische Codierung](#numerical-encoding)
-   [Farbkanäle](#color-channels)
    -   [RGB/BGR-Farbmodell](#rgbbgr-color-model)
    -   [CMYK-Farbmodell](#cmyk-color-model)
    -   [n-Kanal-Farbmodell](#n-channel-color-model)
    -   [Indizierte und Graustufen Farbmodelle](#indexed-and-grayscale-color-models)
    -   [Y' CbCr Color Model](#ycbcr-color-model)
-   [WIC-Pixel Format](#wic-pixel-format)
    -   [Nicht definierte Pixel Formate](#undefined-pixel-formats)
    -   [Indizierte Pixel Formate](#indexed-pixel-formats)
    -   [Gepackte bitpixel Formate](#packed-bit-pixel-formats)
    -   [Graustufen Pixel Formate](#grayscale-pixel-formats)
    -   [RGB/BGR-Pixel Formate](#rgbbgr-pixel-formats)
    -   [CMYK-Pixel Formate](#cmyk-pixel-formats)
    -   [n-Kanal-Pixel Formate](#n-channel-pixel-formats)
    -   [Nur Alpha-Pixel Formate](#alpha-only-pixel-formats)
    -   [Y' CbCr-Pixel Formate](#ycbcr-pixel-formats)
-   [Farbraum](#color-space)
-   [Native Image Formate](#native-image-formats)
    -   [BMP nativer Codec](#bmp-native-codec)
    -   [GIF Native Codec](#gif-native-codec)
    -   [Nativer ICO-Codec](#ico-native-codec)
    -   [JPEG-System eigener Codec](#jpeg-native-codec)
    -   [Nativer PNG-Codec](#png-native-codec)
    -   [TIFF-Native Codec](#tiff-native-codec)
    -   [JPEG-XR Native Codec](#jpeg-xr-native-codec)
-   [Nativer DDS-Codec](#dds-native-codec)
-   [Erweiterbarkeit des Pixel Formats](#pixel-format-extensibility)
-   [Zugehörige Themen](#related-topics)

## <a name="bit-depth"></a>Bittiefe

Die *Bittiefe* ist die Anzahl der Bits, die zum Codieren der einzelnen Farbkanäle verwendet werden. Heutzutage verwenden die meisten digitalen Images eine Bits-Tiefe von 8, was bedeutet, dass jeder Farbkanal in einem Pixel durch 8 Bits dargestellt wird, wobei 2 ⁸ (256) eindeutige Werte pro Kanal bereitgestellt werden. Ein Bild mit einer Bit Tiefe von 8 und drei Farbkanälen (z. b. rot, grün und blau) verwendet 24 Bits pro Pixel (BPP), das 2 ² ⁴ (16.777.216) verschiedene Farben pro Pixel bereitstellt.

Zur besseren Farbauflösung kann eine Bittiefe von 16 oder 32 verwendet werden. Dadurch wird jeder Farbkanal mit 2 ¹ ⁶ (65.536) oder 2 ³ ² eindeutigen Werten bereitstellt, wobei der Arbeitsspeicher pro Pixel kostengünstiger ist.

In manchen Formaten ist die Bittiefe kein Vielfaches von 8. Diese Formate werden als *gepackte* Formate bezeichnet, da die Farbkanäle in einem Pixel nicht an Byte Grenzen ausgerichtet sind. Wenn z. b. die Bit-Tiefe von 5 beträgt, können drei Farbkanäle in 16 Bits (einschließlich 1-Bit-Auffüll Zeichen) gespeichert werden, um Pixel Byte bündig zu machen. Gepackte Formate sind nützlich, wenn die Arbeitsspeicher-oder Verarbeitungsleistung begrenzt ist.

## <a name="numerical-encoding"></a>Numerische Codierung

Für die Mehrzahl der heutigen digitalen Images werden unsignierte Bytes und ganze Zahlen ohne Vorzeichen verwendet, um den numerischen Bereich der einzelnen Farbkanäle zu beschreiben. Der minimale Wert (0) stellt eine Intensität von 0 (null) in einem einzelnen Farbkanal dar und schwarz, wenn alle Farbkanäle NULL sind. Entsprechend stellt der Höchstwert volle Intensität dar, und weiß wird erreicht, wenn alle Farbkanäle vollständig sind. Bei einer Bits-Tiefe von 8 stellt ein uint 256 eindeutige Werte pro Farbkanal (0-255) bereit. Ein 16-Bit-uint bietet 65.536 eindeutige Werte pro Farbkanal (0-65.535).

Außerdem unterstützt WIC ein-und Gleit Komma Format. Diese Formate unterstützen größere dynamische Bereiche, da der gesamte numerische Bereich jedes Farbkanals größer als der sichtbare Bereich ist. Folglich können Farben während der Zwischenschritte der Bildverarbeitung über oder unter dem sichtbaren Bereich angepasst werden, ohne dass Bild Informationen verloren gehen.

### <a name="fixed-point-numerical-encoding"></a>Fixed-Point numerische Codierung

16-Bit-feste Punktwerte werden als s 2,13: Signier Bit, zwei ganzzahlige Bits und dreizehn Bruchteile interpretiert. Mit dieser Interpretation wird ein numerischer Bereich von-4,0 bis + 3,999... kann dargestellt werden, wobei der Wert 1,0 durch den ganz8192 zahligen Wert (0x2000) mit Vorzeichen dargestellt wird.

32-Bit-feste Punktwerte werden als s 7,24: Signier Bit, sieben ganzzahlige Bits und zwanzig Sekundenbruchteile interpretiert. Mit dieser Interpretation wird ein numerischer Bereich von-128,0 bis + 127,999... kann dargestellt werden, wobei der Wert 1,0 durch den ganzzahligen Wert 16777216 (0x01000000) dargestellt wird.

## <a name="color-channels"></a>Farbkanäle

Die Farbkanäle eines Pixel Formats definieren das Speicher Layout der einzelnen Farben innerhalb der Bilddaten einer Bitmap. Es gibt eine Vielzahl verschiedener Farb Kanal Strukturen, die in den heutigen digitalen Images üblich sind, und WIC bietet Unterstützung für viele dieser Strukturen.

### <a name="rgbbgr-color-model"></a>RGB/BGR-Farbmodell

Die Formate RGB und BGR beschreiben Farben in einem Modell mit Additiven Farben. Die gängigste Methode zum Beschreiben eines Bilds besteht aus drei separaten Farbkanälen, die die Farben rot (R), grün (G) und blau (B) darstellen. WIC bietet Unterstützung für diese drei Kanäle in der Reihenfolge rot-grün-blau (RGB) oder blau-grün-rot (BGR). Dies ist die Reihenfolge, in der die einzelnen Farbkanäle im sequenziellen Bitstream angezeigt werden. Im GUID \_ WICPixelFormat32bppRGB-Format ist jedes Pixel beispielsweise 32 Bits breit. Der rote Kanal ist das erste (am wenigsten bedeutende) Byte im Speicher, gefolgt von Grün und blau. Im Gegensatz \_ dazu sind die Farbkanäle im GUID WICPixelFormat32bppBGR-Format in umgekehrter Reihenfolge. WIC unterstützt eine Reihe von RGB/BGR-Formaten, einschließlich spezieller gepackter Bitformate wie GUID \_ WICPixelFormat16bppBGR555.

> [!Note]  
> Die Farbkanäle der speziellen BGR-gepackten Bitformate sind nicht in Vielfachen von 8 wie die farbchannels in typischen Pixel Formaten. Dies bedeutet, dass die channelwerte nicht Byte bündig sind. Beim Lesen von gepackten bitfarbkanälen muss Vorsicht geboten werden.

 

Zusätzlich zu den RGB-und BGR-Formaten stellt WIC auch RGB-und BGR-Pixel Formate bereit, die einen Alpha-Kanal (A) unterstützen. Der Alphakanal stellt Deckkraft Daten für das Pixel bereit. Bei Formaten mit einem hinzugefügten Alphakanal kommt der Alphakanal normalerweise in der Reihenfolge des Farbkanals vor. Beispielsweise ist im Pixel Format GUID \_ WICPixelFormat32bppBGRA die Byte Reihenfolge blau, grün und rot, gefolgt vom Alphakanal.

WIC unterstützt auch vorab multiplizierte Alpha RGB-Pixel Formate (P). In einem typischen RGBA-Pixel Format sind die roten, grünen und blauen Farbwerte die eigentlichen Farbwerte für das Bild. Um ein zusammengesetztes Bild im standardmäßigen RGBA-Format zu erstellen, muss der Alpha Wert des Vordergrund Bilds mit jedem der roten, grünen und blauen Kanäle multipliziert werden, bevor es der Farbe des Hintergrund Bilds hinzugefügt wird. In einem vorab multiplizierten Alpha RGB-Pixel Format wurde jeder Farbkanal bereits mit dem Alpha-Wert multipliziert. Dies bietet eine effizientere Methode der Bildkomposition mit Alphakanal Daten. Um die tatsächlichen Farbwerte jedes Kanals in einem prgba/pbgra-Pixel Format abzurufen, muss die Alphakanal Multiplikation durch den Alpha-Wert umkehrbar werden.

### <a name="cmyk-color-model"></a>CMYK-Farbmodell

CMYK ist ein subtraktives Farbmodell, das beim Drucken verwendet wird. Die von einem CMYK-Modell erzeugten Farben werden durch das Licht generiert, das nicht übernommen, aber reflektiert wird. CMYK ist ein vier Kanal Modell von Zyan (C), Magenta (M), Yellow (Y) und Black (K). Wenn alle vier Farbkanäle den maximalen Wert haben, ist das Ergebnis schwarz. Wie bei den RGB/BGR-Farb Modellen wird die Byte Reihenfolge im sequenziellen Bitstream durch den Namen des Pixel Formats angegeben. Beispielsweise besteht im Pixel Format GUID \_ WICPixelFormat32bppCMYK jedes Pixel aus 32 Bits. Das erste Byte enthält den Zyan-Wert, gefolgt von Magenta, gelb und schwarz. WIC bietet Pixel Formate für CMYK bei 32 und 64 Bits pro Pixel (BPP).

Zusätzlich zum standardmäßigen CMYK-Farbmodell stellt WIC auch CMYK mit Alpha bereit. Dadurch können CMYK-Bilder Alpha Mischungs Daten aufweisen, die dem RGB/BGR-Farbmodell ähneln. Der Alphakanal befindet sich direkt nach schwarz im sequenziellen Bitdaten Strom einer Bitmap.

### <a name="n-channel-color-model"></a>n-Kanal-Farbmodell

Aus Gründen der Flexibilität stellt WIC auch Pixel Formate bereit, die nicht über eine vordefinierte Kanal Reihenfolge verfügen. WIC stellt Pixel Formate bereit, die von drei bis acht Kanälen fortlaufender Bilddaten in der Bittiefe von 8 und 16 unterstützen. Im Gegensatz zu RGB/BGR-und CMYK-Pixel Formaten geben n-Channel-Formate nicht die Kanal Reihenfolge an, sondern die Anzahl der verfügbaren Farbkanäle. Beispielsweise besteht im Pixel Format GUID \_ WICPixelFormat32bpp4Channels jedes Pixel aus 32 Bits, wobei jeder der vier Kanäle ein einzelnes Byte belegen.

WIC stellt auch Pixel Formate für n-Channel mit Alpha bereit. Dadurch können n-Channel-Bilder Alpha Mischungs Daten aufweisen, die den RGB/BGR-und CMYK-Farb Modellen ähneln. Der Alphakanal befindet sich unmittelbar nach dem letzten Farbkanal im sequenziellen Bitdaten Strom einer Bitmap.

### <a name="indexed-and-grayscale-color-models"></a>Indizierte und Graustufen Farbmodelle

*Indizierte* Formate verwenden eine Tabelle mit Farben, die als *Palette* bezeichnet werden. Die Palette wird extern in den Pixeldaten gespeichert oder nicht implizit definiert. Der Wert jedes Pixels im Bild ist ein Index in der Palette. Bei einem indizierten Format steht die Anzahl der Bits pro Pixel direkt im Zusammenhang mit der Anzahl der Einträge in der Palette. Dadurch wird die Datenmenge, die für die Darstellung des Bilds erforderlich ist, erheblich reduziert, aber auch die Anzahl der für das Bild verfügbaren Farben beschränkt. WIC unterstützt indizierte Formate mit einem bpp von 1, 2, 4 oder 8.

Für monochrome Formate (Graustufen Formate) unterstützt WIC 1, 2, 4, 8, 16 und 32 Bits pro Pixel. Bei Bittiefen von 1, 8, 16 und 32 werden die Farbdaten in einem einzelnen Kanal gespeichert. Bei Bittiefen von 2 oder 4 sind Pixel Indizes in eine Graustufen Palette.

### <a name="ycbcr-color-model"></a>Y' CbCr Color Model

WIC bietet Unterstützung für das JPEG-jff y' CbCr-Farbmodell. ' CbCr ' separate Farben in eine ' Luma '-Komponente (Y ') und zwei Chroma-Komponenten (CB und CR). Viele JPEG-Dateien speichern die Bilddaten im systemeigenen Modus mit dem CbCr-Farbmodell.

Das menschliche visuelle System ist weniger sensibel für Änderungen in Chroma als bei Luma, und y' CbCr-Formate können diese geringere Empfindlichkeit durch Verringern der Menge an Chroma-Daten, die relativ zu Luma gespeichert werden, nutzen. Dies erreichen Sie, indem Sie Chroma und luma in separaten Ebenen speichern und jede Komponentenebene auf eine andere Auflösung skalieren. Diese Vorgehensweise wird als Chroma-Unterstichprobe bezeichnet.

Da Chroma-und Luma-Daten separat gespeichert werden und unter Umständen unterschiedliche Auflösungen aufweisen, werden von WIC separate Luma-und Chroma-Pixel Formate definiert. WIC unterstützt Daten mit 8 Bits pro Kanal.

## <a name="wic-pixel-format"></a>WIC-Pixel Format

Die Pixel Formate in WIC werden mithilfe von GUIDs definiert, um Konflikte mit IHVs zu vermeiden. WIC stellt einen anzeigen Amen für den Verweis auf die GUID eines systemeigenen Pixel Formats bereit. Die Benennungs Konvention für die WIC-Pixel Formate lautet wie folgt:

**\[GUID \_ wicpixelformat \] \[ Bits pro Pixel- \] \[ channelorder- \] \[ Speichertyp\]**

| Format Komponente         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ wicpixelformat** | Die beschreibende Identifikation für alle WIC-Pixel Formate. Der Anzeige Name für alle WIC-Pixel beginnt mit dieser Zeichenfolge.                                                                                                                                                                                       |
| **Bits pro Pixel**       | Die Anzahl der Bits pro Pixel (BPP), die für das Pixel Format verwendet werden.                                                                                                                                                                                                                                                |
| **Kanal Reihenfolge**        | Das Farb Kanal Modell und die Reihenfolge der einzelnen Kanäle für das Format.                                                                                                                                                                                                                                            |
| **Speichertyp**         | Die numerische Codierung, die für das Pixel Format verwendet wird. Die Standard Codierung ist eine Ganzzahl ohne Vorzeichen. Wenn nichts auf die Farbmodell Informationen folgt, wird eine Ganzzahl ohne Vorzeichen (uint) impliziert. Mit FixedPoint und float werden Pixel Formate identifiziert, für die die fest Komma-und Gleit Komma Codierung verwendet wird. |



 

> [!Note]  
> Bei n-Channel-Formaten \[ gibt die Channelreihenfolge \] keine Farb Reihenfolge an, sondern die Anzahl der verfügbaren Kanäle. GUID \_ WICPixelFormat24bpp3Channels stellt z. b. drei Farbkanäle bereit, bei denen "3channels" der Eintrag in der \[ Kanal Reihenfolge ist \] , aber nur die Anzahl der Kanäle und nicht die Reihenfolge angibt.

 

Der Anzeige Name GUID \_ WICPixelFormat24bppRGB bedeutet beispielsweise, dass das Pixel Format 24 Bits pro Pixel und das RGB-Farbmodell verwendet. Da der Name keinen Speichertyp explizit identifiziert, wird eine ganze Zahl ohne Vorzeichen impliziert.

WIC unterstützt mehrere Pixel Formate. Die folgenden Tabellen gruppieren ähnliche Pixel Formate nach Farbstruktur und bieten gleichzeitig zusätzliche Informationen, wie z. b. Bittiefe, Bits pro Pixel und numerische Codierung. Jede Tabelle enthält die folgenden Informationen:

-   Anzeige **Name**. Der Anzeige Name des Pixel Formats.
-   **Kanalanzahl**. Die Anzahl der farbchannels.
-   **Bits pro Kanal**. Die Anzahl der Bits pro Kanal (Bittiefe).
-   **Bits pro Pixel**. Die Anzahl der Bits pro Pixel, einschließlich aller Füll Teile.
-   Der **Speichertyp**. Die numerische Codierung der Bilddaten. Bei diesem Wert kann es sich um eine Ganzzahl ohne Vorzeichen (uint), eine festpunktzahl (FixedPoint) oder eine Gleit Komma Zahl (float) handeln.

> [!Note]  
> Aus Gründen der Übersichtlichkeit bezieht sich dieses Dokument auf Pixel Formate nur anhand ihrer anzeigen Amen. Der tatsächliche Hexadezimalwert für die Pixel Formate finden Sie in den wincodec. h/IDL-Dateien.

 

### <a name="undefined-pixel-formats"></a>Nicht definierte Pixel Formate

Die folgende Liste zeigt generische Pixel Formate, die verwendet werden, wenn das Pixel Format nicht definiert ist oder für einen Bild Vorgang unwichtig ist.

-   GUID \_ wicpixelformatundefiniert
-   GUID \_ wicpixelformatdontcare

### <a name="indexed-pixel-formats"></a>Indizierte Pixel Formate

In der folgenden Tabelle sind die von WIC bereitgestellten indizierten Pixel Formate aufgeführt. In diesen Formaten ist der Wert für jedes Pixel ein Index in eine Farbpalette.



| Anzeigename                   | Kanalanzahl | Bits pro Pixel | Speichertyp |
|---------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat1bppIndexed | 1             | 1              | UINT         |
| GUID \_ WICPixelFormat2bppIndexed | 1             | 2              | UINT         |
| GUID \_ WICPixelFormat4bppIndexed | 1             | 4              | UINT         |
| GUID \_ WICPixelFormat8bppIndexed | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>Gepackte bitpixel Formate

In der folgenden Tabelle sind die von WIC bereitgestellten gepackten Bitformate aufgeführt. In diesen Formaten werden Farb Kanal Daten nicht in Byte ausgerichtet.



| Anzeigename                          | Kanalanzahl | Bits pro Kanal       | Bits pro Pixel | Speichertyp |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| GUID \_ WICPixelFormat16bppBGR555           | 3             | 5                      | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGR565           | 3             | 5 (B)/6 (G)/5 (R)         | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGRA555          | 4             | 5 (B)/5 (G)/5 (R)/1 (A)    | 16             | UINT         |
| GUID \_ WICPixelFormat32bppBGR101010        | 3             | 10                     | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102      | 4             | 10 (R)/10 (G)/10 (B)/2 (a) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102XR    | 4             | 10 (R)/10 (G)/10 (B)/2 (a) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2      | 4             | 10 (R)/10 (G)/10 (B)/2 (a) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 | 4             | 10 (R)/10 (G)/10 (B)/2 (a) | 32             | UINT         |

Bei den Formaten GUID \_ WICPixelFormat32bppBGR101010 und GUID \_ WICPixelFormat32bppRGBA1010102 wird der rote Kanal in den geringsten Bits gespeichert. Bei den Formaten GUID \_ WICPixelFormat32bppR10G10B10A2 und GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 wird der rote Kanal in den signifikantesten Bits definiert, das gleiche Layout wie [DXGI_FORMAT_R10G10B10A2_UNORM](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

Das Format GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 ist das 10-Bit-Pixel Format für HDR10 (BT. 2020-Farbraum und SMPTE St. 2084 EotF).

### <a name="grayscale-pixel-formats"></a>Graustufen Pixel Formate

In der folgenden Tabelle sind die von WIC bereitgestellten Graustufen Formate aufgeführt. In diesen Formaten steht Farbdaten für graue Schattierungen.



| Anzeigename                           | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|-----------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ wicpixelformatblackwhite          | 1             | 1                | 1              | UINT         |
| GUID \_ WICPixelFormat2bppGray            | 1             | 2                | 2              | UINT         |
| GUID \_ WICPixelFormat4bppGray            | 1             | 4                | 4              | UINT         |
| GUID \_ WICPixelFormat8bppGray            | 1             | 8                | 8              | UINT         |
| GUID \_ WICPixelFormat16bppGray           | 1             | 16               | 16             | UINT         |
| GUID \_ WICPixelFormat16bppGrayFixedPoint | 1             | 16               | 16             | FixedPoint   |
| GUID \_ WICPixelFormat16bppGrayHalf       | 1             | 16               | 16             | Float        |
| GUID \_ WICPixelFormat32bppGrayFloat      | 1             | 32               | 32             | Float        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint | 1             | 32               | 32             | FixedPoint   |



 

### <a name="rgbbgr-pixel-formats"></a>RGB/BGR-Pixel Formate

In der folgenden Tabelle sind die RGB/BGR-Formate aufgeführt, die von WIC bereitgestellt werden. Diese Formate trennen die primären Farbdaten in rote (R), grüne (G) und blaue (B) Channels. Ein zusätzlicher Alpha (A)-Kanal wird in einigen Formaten für Deckkraft Informationen bereitgestellt.



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
> \*Das GUID \_ WICPixelFormat32bppRGBE-Format codiert 3 16-Bit-Gleit Komma Werte in 4 Bytes wie folgt: drei nicht signierte 8-Bit-Mantissen für die R-, G-und B-Kanäle sowie einen freigegebenen 8-Bit-Exponenten. Dieses Format bietet eine 16-Bit-Gleit Komma Genauigkeit in einer kleineren Pixel Darstellung.

 

Ab Windows 8 und dem [Platt Form Update für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)bietet WIC zusätzliche Formate, die in der Tabelle aufgeführt sind.



| Anzeigename                      | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppRGB       | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppRGB       | 3             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat96bppRGBFloat  | 3             | 32               | 96             | GLEITKOMMAZAHL        |
| GUID \_ WICPixelFormat64bppPRGBAHalf | 4             | 16               | 64             | GLEITKOMMAZAHL        |



 

### <a name="cmyk-pixel-formats"></a>CMYK-Pixel Formate

In der folgenden Tabelle sind die von WIC bereitgestellten CMYK-Formate aufgeführt. Diese Formate trennen die primären Farbdaten in Zyan-(C), Magenta (M), gelbe (Y) und schwarze (K)-Kanäle.



| Anzeigename                      | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppCMYK      | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppCMYK      | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bppCMYKAlpha | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bppCMYKAlpha | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>n-Kanal-Pixel Formate

In der folgenden Tabelle werden die von WIC bereitgestellten n-Kanal Formate aufgelistet. Diese Formate stellen eine Reihe von nicht definierten Farbkanälen zum Speichern von Bilddaten bereit.



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



 

### <a name="alpha-only-pixel-formats"></a>Nur Alpha-Pixel Formate

In der folgenden Tabelle sind die von WIC bereitgestellten Alpha reinen Formate aufgeführt. Dieses Format enthält nur Alpha Informationen.



| Anzeigename                 | Kanalanzahl | Bits pro Kanal | Bits pro Pixel | Speichertyp |
|-------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppAlpha | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Y' CbCr-Pixel Formate

In der folgenden Tabelle werden die von WIC bereitgestellten CbCr-Formate aufgelistet. Diese Formate trennen die primären Farbdaten in "Luma (Y)", "Blue Chroma Difference (CB)" und "Red Choma Difference (CR)". Beachten Sie, dass diese Formate so konzipiert sind, dass JPEG jff y' CbCr Pixeldaten gespeichert werden.



| Anzeigename                 | Kanalanzahl | Bits pro Pixel | Speichertyp |
|-------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppY     | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCb    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCr    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat16bppCbCr | 2             | 16             | UINT         |



 

## <a name="color-space"></a>Farbraum

Die Pixel Formate in sich haben keinen Farbraum. Im Allgemeinen ist der Farbraum eine semantische Interpretation der Pixelwerte, die vom Kontext der Bitmap abhängen. Einige Bilder identifizieren einen Farb Kontext, der den Farbraum des Bilds definiert. Nur wenn ein Farb Kontext vorhanden ist, sollte der farbliche Leerraum abgeleitet werden.

Farb Kontextinformationen werden von der [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) -Schnittstelle für WIC definiert. Um die Farb Kontextinformationen für einen Bildframe abzurufen, verwenden Sie die **GetColorContext** -Methode.

Wenn keine Farb Rauminformationen für ein Abbild vorhanden sind, besteht die allgemeine Regel für den leerschluss, dass uint RGB-und Graustufen Formate den standardmäßigen RGB-Farbraum (sRGB) verwenden, während für ein fest Komma-und Gleit Komma-RGB-und Graustufen Formate der erweiterte RGB-Farbraum (ScRGB) verwendet wird. Das CMYK-Farbmodell verwendet einen rwop-Farbraum.

## <a name="native-image-formats"></a>Native Image Formate

Jedes von Windows bereitgestellte WIC-Codecs unterstützt eine Teilmenge der WIC-Pixel Formate. Bei jedem Codec können sich die unterstützten decodierungsformate von den unterstützten Codierungsformaten unterscheiden.

Wenn Daten beim Decodieren eines Bilds in einem vom Decoder nicht unterstützten Pixel Format System intern gespeichert werden, wird es in ein unterstütztes Format konvertiert. Um das Ausgabe Pixel Format zu ermitteln, nennen Sie [**IWICBitmapFrameDecode:: GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat).

Verwenden Sie beim Codieren eines Bilds [**IWICBitmapFrameEncode:: SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) , um anzufordern, dass der Encoder ein bestimmtes Pixel Format verwendet. Der Encoder gibt das nächstgelegene unterstützte Pixel Format zurück, das sich von dem angeforderten unterscheiden kann.

In den folgenden Tabellen sind die Pixel Formate aufgeführt, die von den einzelnen von Windows bereitgestellten WIC-Codecs unterstützt werden

### <a name="bmp-native-codec"></a>BMP nativer Codec



| Decoder-Pixel Formate                   | Encoder-Pixel Formate                   |
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
> GUID \_ WICPixelFormat32bppBGRA wird nur in Windows 8, dem [Platt Form Update für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)und höher unterstützt.
>
> -   Um dieses Format zu codieren, verwenden Sie die Option **EnableV5Header32bppBGRA** Encoder. Der BMP wird mit einem BITMAPV5HEADER-Header geschrieben.
> -   Wenn eine Datei über eine BITMAPV5HEADER verfügt, decodiert Sie als GUID \_ WICPixelFormat32bppBGRA.

 

### <a name="gif-native-codec"></a>GIF Native Codec



| Decoder-Pixel Formate           | Encoder-Pixel Formate           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |



 

### <a name="ico-native-codec"></a>Nativer ICO-Codec



| Decoder-Pixel Formate         | Encoder-Pixel Formate |
|-------------------------------|-----------------------|
| GUID \_ WICPixelFormat32bppBGRA |                       |



 

### <a name="jpeg-native-codec"></a>JPEG-System eigener Codec



| Decoder-Pixel Formate         | Encoder-Pixel Formate         |
|-------------------------------|-------------------------------|
| GUID \_ WICPixelFormat8bppGray  | GUID \_ WICPixelFormat8bppGray  |
| GUID \_ WICPixelFormat24bppBGR  | GUID \_ WICPixelFormat24bppBGR  |
| GUID \_ WICPixelFormat32bppCMYK | GUID \_ WICPixelFormat32bppCMYK |



 

### <a name="png-native-codec"></a>Nativer PNG-Codec



| Decoder-Pixel Formate           | Encoder-Pixel Formate           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat2bppIndexed | GUID \_ WICPixelFormat2bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ wicpixelformatblackwhite  | GUID \_ wicpixelformatblackwhite  |
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



 

### <a name="tiff-native-codec"></a>TIFF-Native Codec



| Decoder-Pixel Formate                | Encoder-Pixel Formate           |
|--------------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed      | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed      | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed      | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ wicpixelformatblackwhite       | GUID \_ wicpixelformatblackwhite  |
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
> GUID \_ WICPixelFormat96bppRGBFloat wird nur in Windows 8, dem [Platt Form Update für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)und höher unterstützt.

 

### <a name="jpeg-xr-native-codec"></a>JPEG-XR Native Codec



| Decoder-Pixel Formate                    | Encoder-Pixel Formate                    |
|------------------------------------------|------------------------------------------|
| GUID \_ wicpixelformatblackwhite           | GUID \_ wicpixelformatblackwhite           |
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
| GUID \_ WICPixelFormat32bppCMYK            | GUID \_ WICPixelFormat32bppCMYK            |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | GUID \_ WICPixelFormat64bppRGBAFixedPoint  |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | GUID \_ WICPixelFormat128bppRGBAFixedPoint |
| GUID \_ WICPixelFormat64bppCMYK            | GUID \_ WICPixelFormat64bppCMYK            |
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
| GUID \_ WICPixelFormat40bppCMYKAlpha       | GUID \_ WICPixelFormat40bppCMYKAlpha       |
| GUID \_ WICPixelFormat80bppCMYKAlpha       | GUID \_ WICPixelFormat80bppCMYKAlpha       |
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
| GUID \_ WICPixelFormat64bppRGBHalf         | GUID \_ wicpixelformatblackwhite           |



 

## <a name="dds-native-codec"></a>Nativer DDS-Codec



| Decoder-Pixel Formate          | Encoder-Pixel Formate          |
|--------------------------------|--------------------------------|
| GUID \_ WICPixelFormat32bppBGRA  | GUID \_ WICPixelFormat32bppBGRA  |
| GUID \_ WICPixelFormat32bppPBGRA | GUID \_ WICPixelFormat32bppPBGRA |



 

> [!Note]  
> Der von Windows bereitgestellte Codec unterstützt DDS-Dateien, die mithilfe der folgenden DXGI-Format Werte codiert werden \_ :

 

-   DXGI- \_ Format \_ BC1 \_ unorm
-   DXGI- \_ Format \_ BC2 \_ unorm
-   DXGI- \_ Format \_ BC3 \_ unorm

Diese werden decodiert und als GUID- \_ WICPixelFormat32bppBGRA oder GUID \_ WICPixelFormat32bppPBGRA codiert. Weitere Informationen finden Sie in der [Übersicht über das DDS-Format](dds-format-overview.md).

## <a name="pixel-format-extensibility"></a>Erweiterbarkeit des Pixel Formats

Benutzerdefinierte Bildformate können Pixel Formate verwenden, die nicht nativ von WIC bereitgestellt werden, z. b. YCbCr (YUV) und YCCK (Y/CB/CR/K). WIC bietet ein Erweiterbarkeits Modell, mit dem sowohl integrierte als auch Add-in-Pixel Formate in derselben Abbild Pipeline funktionieren. Um diese Pixel Formate in die WIC-Imaging-Pipeline zu integrieren, müssen Sie Pixel Format Konverter erstellen, um Add-in-Pixel Formate in ein oder mehrere der systemeigenen Pixel Formate zu konvertieren. Die Hauptschnittstelle zum Entwickeln von Format Konvertern ist [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-GUIDs und CLSIDs](-wic-guids-clsids.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[HD-Foto Spezifikation 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 

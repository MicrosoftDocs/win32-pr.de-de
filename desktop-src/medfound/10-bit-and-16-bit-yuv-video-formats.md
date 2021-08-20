---
description: In diesem Thema werden die 10- und 16-Bit-YUV-Formate beschrieben, die für die Erfassung, Verarbeitung und Anzeige von Videos im Microsoft Windows-Betriebssystem empfohlen werden.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: 10-Bit- und 16-Bit-YUV-Videoformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652929257c071bd735e1d6c7ec36e1767d904da7d2364ac3e30c61c81f342f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065730"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a>10-Bit- und 16-Bit-YUV-Videoformate

In diesem Thema werden die 10- und 16-Bit-YUV-Formate beschrieben, die für die Erfassung, Verarbeitung und Anzeige von Videos im Microsoft Windows-Betriebssystem empfohlen werden.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht](#overview)
-   [FOURCC-Codes für 10-Bit- und 16-Bit-YUV](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [Oberflächendefinitionen](#surface-definitions)
    -   [4:2:0-Formate](#420-formats)
    -   [4:2:2-Formate](#422-formats)
    -   [4:4:4-Formate](#444-formats)
-   [Bevorzugte YUV-Formate](#preferred-yuv-formats)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Diese Formate verwenden eine Feste-Punkt-Darstellung sowohl für den Lumakanal als auch für die Luntekanäle (C'b und C'r). Beispielwerte sind skalierte 8-Bit-Werte mit einem Skalierungsfaktor von 2^(n − 8), wobei n entweder 10 oder 16 gemäß den Abschnitten 7.7-7.8 und 7.11-7.12 von SMPTE 274M ist. Genauigkeitskonvertierungen können mit einfachen Bitverschiebungen ausgeführt werden. Wenn der weißer Punkt eines 8-Bit-Formats beispielsweise 235 ist, hat das entsprechende 10-Bit-Format einen Weißen Punkt bei 940 (235 × 4).

Die hier beschriebenen 16-Bit-Darstellungen verwenden Little-Endian-WORD-Werte für jeden Kanal.  Die 10-Bit-Formate verwenden auch 16 Bits für jeden Kanal, wobei die niedrigsten 6 Bits auf 0 festgelegt sind, wie im folgenden Diagramm dargestellt.

![Diagramm mit 10-Bit-Darstellung](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

Da die 10-Bit- und 16-Bit-Darstellungen des gleichen YUV-Formats das gleiche Speicherlayout aufweisen, ist es möglich, eine 10-Bit-Darstellung ohne Genauigkeitsverlust in eine 16-Darstellung zu konvertieren. Es ist auch möglich, eine 16-Bit-Darstellung in eine 10-Bit-Darstellung zu casten. (Die Formate Y416 und Y410 sind jedoch eine Ausnahme von dieser allgemeinen Regel, da sie nicht das gleiche Speicherlayout verwenden.)

Wenn die Grafikhardware eine Oberfläche liest, die eine 10-Bit-Darstellung enthält, sollte sie die niedrigen 6 Bits jedes Kanals ignorieren. Wenn eine Oberfläche gültige 16-Bit-Daten enthält, sollte sie jedoch als 16-Bit-Oberfläche identifiziert werden.

In den Formaten, die Alpha enthalten, weist ein vollständig transparentes Pixel den Alphawert 0 auf, und ein vollständig nicht transparentes Pixel hat den Alphawert (2^n) – 1, wobei n die Anzahl der Alphabits ist. Alpha wird als linearer Wert angenommen, der auf jede Komponente angewendet wird, nachdem die Komponente in ihre normalisierte lineare Form konvertiert wurde.

Bei Bildern im Videospeicher wählt der Grafiktreiber die Speicherausrichtung der Oberfläche aus. Die Oberfläche muss **DWORD** ausgerichtet sein. Das heißt, dass einzelne Linien innerhalb einer Oberfläche garantiert an einer 32-Bit-Grenze beginnen, obwohl die Ausrichtung größer als 32 Bits sein kann. Der Ursprung (0,0) ist immer die obere linke Ecke der Oberfläche.

Für die Zwecke dieser Dokumentation entspricht der Begriff *U* *cb*, und der Begriff *V* entspricht *Cr*.

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a>FOURCC-Codes für 10-Bit- und 16-Bit-YUV

Die FOURCC-Codes für die hier beschriebenen Formate verwenden die folgende Konvention:

-   Wenn das Format planar ist, ist das erste Zeichen im FOURCC-Code "P". Wenn das Format gepackt ist, ist das erste Zeichen "Y".
-   Das zweite Zeichen im FOURCC-Code wird durch die Stichprobenentnahme bestimmt, wie in der folgenden Tabelle dargestellt.

    

    | Sampling von Stichproben | FOURCC-Codebuchstabe |
    |-----------------|--------------------|
    | 4:4:4           | '4'                |
    | 4:2:2           | '2'                |
    | 4:2:1           | '1'                |
    | 4:2:0           | '0'                |

    

     

-   Die letzten beiden Zeichen in FOURCC geben die Anzahl der Bits pro Kanal an, entweder "16" für 16 Bits oder "10" für 10 Bits.

Mit diesem Schema wurden die folgenden FOURCC-Codes definiert. Derzeit wurden keine 4:2:1-Formate für 10-Bit- oder 16-Bit-YUV definiert.



| FOURCC | Beschreibung            |
|--------|------------------------|
| P016   | Planar, 4:2:0, 16-Bit. |
| P010   | Planar, 4:2:0, 10-Bit. |
| P216   | Planar, 4:2:2, 16-Bit. |
| P210   | Planar, 4:2:2, 10-Bit. |
| Y216   | Gepackt, 4:2:2, 16-Bit. |
| Y210   | Gepackt, 4:2:2, 10-Bit. |
| Y416   | Gepackt, 4:4:4, 16-Bit  |
| Y410   | Gepackt, 4:4:4, 10-Bit. |



 

Untertyp-GUIDs wurden auch von diesen FOURCCs definiert. weitere Informationen finden Sie unter [Video-Untertyp-GUIDs.](video-subtype-guids.md)

## <a name="surface-definitions"></a>Oberflächendefinitionen

In diesem Abschnitt wird das Speicherlayout der einzelnen Formate beschrieben. In den folgenden Beschreibungen bezieht sich der Begriff **WORD** auf einen Little-Endian-16-Bit-Wert und der Begriff **DWORD** auf einen Little-Endian-32-Bit-Wert.

### <a name="420-formats"></a>4:2:0-Formate

Es werden zwei 4:2:0-Formate mit den FOURCC-Codes P016 und P010 definiert. Sie verwenden das gleiche Speicherlayout, aber P016 verwendet 16 Bits pro Kanal und P010 10 Bits pro Kanal.

### <a name="p016-and-p010"></a>P016 und P010

In diesen beiden Formaten werden alle Y-Beispiele zuerst im Arbeitsspeicher als Array von **WORD** s mit einer geraden Anzahl von Zeilen angezeigt. Der Oberflächenschritt kann größer als die Breite der Y-Ebene sein. Auf dieses Array folgt unmittelbar ein Array von **WORD** s, das sie und V-Beispiele enthält, wie im folgenden Diagramm dargestellt.

![Diagramm: Layout von p016 und p010 Pixel](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

Wenn das kombinierte U-V-Array als Array von **DWORD-s** adressiert wird, enthält das am wenigsten signifikante Wort (LSW) den U-Wert und das wichtigste Wort (MSW) den V-Wert. Der Schritt der kombinierten U-V-Ebene entspricht dem Schritt der Y-Ebene. Die U-V-Ebene verfügt über halb so viele Linien wie die Y-Ebene.

Diese beiden Formate sind die bevorzugten 4:2:0-Planpixelformate für YUV-Darstellungen mit höherer Genauigkeit. Es wird erwartet, dass es sich um eine Zwischenbedingung für DXVA-Accelerators (DirectX Video Acceleration) handelt, die 10-Bit- oder 16-Bit-4:2:0-Videos unterstützen.

### <a name="422-formats"></a>4:2:2-Formate

Es werden vier 4:2:2-Formate definiert, zwei planar und zwei gepackt. Sie verfügen über die folgenden FOURCC-Codes:

-   P216
-   P210
-   Y216
-   Y210

### <a name="p216-and-p210"></a>P216 und P210

In diesen beiden planaren Formaten werden alle Y-Beispiele zuerst im Arbeitsspeicher als Array von **WORD** s mit einer geraden Anzahl von Zeilen angezeigt. Der Oberflächenschritt kann größer als die Breite der Y-Ebene sein. Auf dieses Array folgt unmittelbar ein Array von **WORD** s, das sie und V-Beispiele enthält, wie im folgenden Diagramm dargestellt.

![Diagramm mit p216- und p210-Pixellayout](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

Wenn das kombinierte U-V-Array als Array von **DWORD-s** adressiert wird, enthält die LSW den U-Wert und das MSW den V-Wert. Der Schritt der kombinierten U-V-Ebene entspricht dem Schritt der Y-Ebene. Die U-V-Ebene hat die gleiche Anzahl von Linien wie die Y-Ebene.

Diese beiden Formate sind die bevorzugten 4:2:2 planaren Pixelformate für YUV-Darstellungen mit höherer Genauigkeit. Es wird erwartet, dass sie eine kurzfristige Anforderung für Die DirectX-Videobeschleunigung (DXVA) sind, die 10-Bit- oder 16-Bit-4:2:2-Videos unterstützen.

### <a name="y216-and-y210"></a>Y216 und Y210

In diesen beiden gepackten Formaten wird jedes Pixelpaar als Array von vier WORD-Formaten gespeichert, wie in der folgenden Abbildung dargestellt.

![Diagramm, das das y216- und y210-Pixellayout zeigt.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

Das erste **WORD** im Array enthält das erste Y-Beispiel im Paar, das zweite **WORD** enthält das U-Beispiel, das dritte **WORD** enthält das zweite Y-Beispiel und das vierte **WORD** enthält das V-Beispiel.

Y210 ist mit Y216 identisch, außer dass jede Stichprobe nur 10 Bits mit signifikanten Daten enthält. Die am wenigsten signifikanten 6 Bits werden auf 0 (null) festgelegt, wie zuvor beschrieben.

### <a name="444-formats"></a>4:4:4 Formate

Es werden zwei 4:4:4-Formate mit den FOURCC-Codes Y410 und Y416 definiert. Beide sind gepackte Formate.

### <a name="y410"></a>Y410

Dieses Format ist eine gepackte 10-Bit-Darstellung, die 2 Bits Alpha enthält. Jedes Pixel wird als einzelnes **DWORD** mit dem Speicherlayout codiert, das im folgenden Diagramm dargestellt ist.

![Diagramm, das das y410-Pixel-Layout zeigt.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

Bits 0-9 enthalten das U-Beispiel, Bits 10-19 enthalten das Y-Beispiel, Bits 20-29 enthalten das V-Beispiel und Bits 30-31 den Alphawert. Um anzugeben, dass ein Pixel vollständig deckend ist, muss eine Anwendung die beiden Alphabits auf 0x03.

### <a name="y416"></a>Y416

Dieses Format ist eine gepackte 16-Bit-Darstellung, die 16 Bits Alpha enthält. Jedes Pixel wird wie in der folgenden Abbildung dargestellt als **DWORD-Paar** codiert.

![Diagramm, das das Layout mit y416 Pixeln zeigt.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

Bits 0-15 enthalten das U-Beispiel, Bits 16-31 enthalten das Y-Beispiel, Bits 32-47 enthalten das V-Beispiel und Bits 48-63 den Alphawert.

Um anzugeben, dass ein Pixel vollständig deckend ist, muss eine Anwendung die beiden Alphabits auf 0xFFFF. Dieses Format ist in erster Linie als Zwischenformat während der Bildverarbeitung vorgesehen, um die Ansammlung von Fehlern zu vermeiden.

## <a name="preferred-yuv-formats"></a>Bevorzugte YUV-Formate

In der folgenden Tabelle sind die bevorzugten YUV-Formate aufgeführt, einschließlich 8-Bit-Formate.



| Format | Sampling von Luftproben | Gepackt oder planar | Bits pro Kanal |
|--------|-----------------|------------------|------------------|
| AYUV   | 4:4:4           | Verpackt           | 8                |
| Y410   | 4:4:4           | Verpackt           | 10               |
| Y416   | 4:4:4           | Verpackt           | 16               |
| AI44   | 4:4:4           | Verpackt           | Palettiert       |
| YUY2   | 4:2:2           | Verpackt           | 8                |
| Y210   | 4:2:2           | Verpackt           | 10               |
| Y216   | 4:2:2           | Verpackt           | 16               |
| P210   | 4:2:2           | Planar           | 10               |
| P216   | 4:2:2           | Planar           | 16               |
| NV12   | 4:2:0           | Planar           | 8                |
| P010   | 4:2:0           | Planar           | 10               |
| P016   | 4:2:0           | Planar           | 16               |
| NV11   | 4:1:1           | Planar           | 8                |



 

Wenn ein Objekt eine bestimmte Bittiefe und ein bestimmtes Samplingschema unterstützt, wird empfohlen, die entsprechenden YUV-Formate zu unterstützen, die in dieser Tabelle aufgeführt sind. (Objekte unterstützen möglicherweise zusätzliche Formate, die hier nicht aufgeführt sind.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfohlene 8-Bit-YUV-Formate für video rendering](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Video-Untertyp-GUIDs](video-subtype-guids.md)
</dt> <dt>

[Videomedientypen](video-media-types.md)
</dt> </dl>

 

 




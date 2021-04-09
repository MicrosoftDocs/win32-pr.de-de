---
description: In diesem Thema werden die 10-und 16-Bit-YUV-Formate beschrieben, die zum erfassen, verarbeiten und Anzeigen von Videos im Microsoft Windows-Betriebssystem empfohlen werden.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: 10-Bit-und 16-Bit-YUV-Video Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129560"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a>10-Bit-und 16-Bit-YUV-Video Formate

In diesem Thema werden die 10-und 16-Bit-YUV-Formate beschrieben, die zum erfassen, verarbeiten und Anzeigen von Videos im Microsoft Windows-Betriebssystem empfohlen werden.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht](#overview)
-   [FourCC Codes für 10-Bit-und 16-Bit-YUV](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [Oberflächen Definitionen](#surface-definitions)
    -   [4:2:0 Formate](#420-formats)
    -   [4:2:2 Formate](#422-formats)
    -   [4:4:4 Formate](#444-formats)
-   [Bevorzugte YUV-Formate](#preferred-yuv-formats)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Diese Formate verwenden eine Fixed-Point-Darstellung für die Kanäle "Luma" und "Chroma" ("c" und "c"). Beispiel Werte sind skalierte 8-Bit-Werte unter Verwendung eines Skalierungsfaktors von 2 ^ (n − 8), wobei n entweder 10 oder 16 ist, gemäß den Abschnitten 7.7-7.8 und 7.11-7.12 von SMPTE 274m. Genauigkeits Konvertierungen können mithilfe von einfachen Bitverschiebungen durchgeführt werden. Wenn der weiße Punkt eines 8-Bit-Formats z. b. 235 ist, hat das entsprechende 10-Bit-Format einen weißen Punkt bei 940 (235 × 4).

In den hier beschriebenen 16-Bit-Darstellungen werden für jeden Kanal Little-Endian- **Wort** Werte verwendet. Die 10-Bit-Formate verwenden auch 16 Bits für jeden Kanal, wobei die niedrigsten 6 Bits auf 0 (null) festgelegt sind, wie im folgenden Diagramm dargestellt.

![Diagramm mit 10-Bit-Darstellung](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

Da die 10-Bit-und die 16-Bit-Darstellung desselben YUV-Formats das gleiche Speicher Layout aufweisen, ist es möglich, eine 10-Bit-Darstellung ohne Genauigkeits Verlust in eine 16-Darstellung umzuwandeln. Es ist auch möglich, eine 16-Bit-Darstellung in eine 10-Bit-Darstellung umzuwandeln. (Bei den Formaten Y416 und Y410 handelt es sich jedoch um eine Ausnahme von dieser allgemeinen Regel, da Sie nicht das gleiche Speicher Layout haben.)

Wenn die Grafikhardware eine Oberfläche liest, die eine 10-Bit-Darstellung enthält, sollten die nieder wertigen 6 Bits der einzelnen Kanäle ignoriert werden. Wenn eine Oberfläche gültige 16-Bit-Daten enthält, sollte Sie jedoch als 16-Bit-Oberfläche identifiziert werden.

In den Formaten, die Alpha enthalten, weist ein vollständig transparentes Pixel einen Alpha-Wert von 0 (null) auf, und ein vollständig undurchsichtiges Pixel weist den Alpha-Wert (2 ^ n) – 1 auf, wobei n die Anzahl der Alpha Bits ist. Bei Alpha wird angenommen, dass es sich um einen linearen Wert handelt, der auf jede Komponente angewendet wird, nachdem die Komponente in die normalisierte lineare Form konvertiert wurde.

Bei Bildern im Videospeicher wählt der Grafiktreiber die Arbeitsspeicher Ausrichtung der Oberfläche aus. Die Oberfläche muss in **DWORD** ausgerichtet sein. Das heißt, einzelne Zeilen innerhalb einer Oberfläche werden garantiert an einer 32-Bit-Grenze gestartet, obwohl die Ausrichtung größer als 32 Bits sein kann. Der Ursprung (0,0) ist immer die obere linke Ecke der Oberfläche.

Im Rahmen dieser Dokumentation entspricht der Begriff " *U* " dem Wert von " *CB*", und der Begriff " *V* " entspricht *CR*.

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a>FourCC Codes für 10-Bit-und 16-Bit-YUV

In den FourCC-Codes für die hier beschriebenen Formate wird die folgende Konvention verwendet:

-   Wenn das Format Planar ist, lautet das erste Zeichen im FourCC-Code "P". Wenn das Format gepackt ist, ist das erste Zeichen "Y".
-   Das zweite Zeichen im FourCC-Code wird durch die Chroma-Stichprobenentnahme bestimmt, wie in der folgenden Tabelle dargestellt.

    

    | Chroma-Sampling | FourCC-Code Buchstabe |
    |-----------------|--------------------|
    | 4:4:4           | 0:                |
    | 4:2:2           | 2,2                |
    | 4:2:1           | '1'                |
    | 4:2:0           | '0'                |

    

     

-   Die letzten zwei Zeichen im FourCC geben die Anzahl der Bits pro Kanal an, entweder "16" für 16 Bits oder "10" für 10 Bits.

Mithilfe dieses Schemas wurden die folgenden FOURCC-Codes definiert. Zurzeit wurden keine 4:2:1-Formate für 10-Bit-oder 16-Bit-YUV definiert.



| FOURCC | BESCHREIBUNG            |
|--------|------------------------|
| P016   | Planar, 4:2:0, 16-Bit. |
| P010   | Planar, 4:2:0, 10-Bit. |
| P216   | Planar, 4:2:2, 16-Bit. |
| P210   | Planar, 4:2:2, 10-Bit. |
| Y216   | Gepackt, 4:2:2, 16 Bit. |
| Y210   | Gepackt, 4:2:2, 10-Bit. |
| Y416   | Gepackt, 4:4:4, 16 Bit  |
| Y410   | Gepackt, 4:4:4, 10-Bit. |



 

Untertyp-GUIDs wurden auch aus diesen fourccs definiert. siehe [Video Untertyp-GUIDs](video-subtype-guids.md).

## <a name="surface-definitions"></a>Oberflächen Definitionen

In diesem Abschnitt wird das Speicher Layout der einzelnen Formate beschrieben. In den folgenden Beschreibungen verweist der Begriff **Word** auf einen Little-Endian-16-Bit-Wert, und der Begriff **DWORD** verweist auf einen Little-Endian-32-Bit-Wert.

### <a name="420-formats"></a>4:2:0 Formate

Es werden zwei 4:2:0-Formate mit den FourCC-Codes P016 und P010 definiert. Sie verwenden dasselbe Speicher Layout, aber P016 verwendet 16 Bits pro Kanal und P010 verwendet 10 Bits pro Kanal.

### <a name="p016-and-p010"></a>P016 und P010

In diesen beiden Formaten werden alle Y-Beispiele als erstes im Arbeitsspeicher als Array von **Word** s mit einer geraden Anzahl von Zeilen angezeigt. Der Oberflächen Schritt kann größer als die Breite der Y-Ebene sein. Auf dieses Array folgt unmittelbar ein Array von **Word** s, das verschachtelte Sie-und V-Beispiele enthält, wie im folgenden Diagramm dargestellt.

![Diagramm mit P016 und P010 Pixel Layout](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

Wenn das kombinierte U-V-Array als Array von **DWORD** adressiert wird, enthält das unwichtigste Wort (LSW) den U-Wert und das signifikanteste Wort (MSW) den V-Wert. Der Schritt der kombinierten U-V-Ebene entspricht dem STRIDE der Y-Ebene. Die U-V-Ebene hat die Hälfte der Zeilen in der Y-Ebene.

Diese beiden Formate sind die bevorzugten 4:2:0-planaren Pixel Formate für YUV-Darstellungen mit höherer Genauigkeit. Es wird erwartet, dass es sich um eine zwischen Bedingung für DXVA-Accelerators (DirectX Video Acceleration) handelt, die 10-Bit-oder 16-Bit-4:2:0-Videos unterstützen.

### <a name="422-formats"></a>4:2:2 Formate

Vier 4:2:2 Formate sind definiert, zwei planare und zwei gepackte. Sie verfügen über die folgenden FOURCC-Codes:

-   P216
-   P210
-   Y216
-   Y210

### <a name="p216-and-p210"></a>P216 und P210

In diesen beiden planaren Formaten werden alle Y-Beispiele als erstes im Arbeitsspeicher als Array von **Word** s mit einer geraden Anzahl von Zeilen angezeigt. Der Oberflächen Schritt kann größer als die Breite der Y-Ebene sein. Auf dieses Array folgt unmittelbar ein Array von **Word** s, das verschachtelte Sie-und V-Beispiele enthält, wie im folgenden Diagramm dargestellt.

![Diagramm mit P216 und P210 Pixel Layout](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

Wenn das kombinierte U-V-Array als ein Array von **DWORD** s adressiert wird, enthält der LSW den U-Wert, und der MSW enthält den V-Wert. Der Schritt der kombinierten U-V-Ebene entspricht dem STRIDE der Y-Ebene. Die U-V-Ebene verfügt über die gleiche Anzahl von Zeilen wie die Y-Ebene.

Diese beiden Formate sind die bevorzugten 4:2:2-planaren Pixel Formate für YUV-Darstellungen mit höherer Genauigkeit. Es wird erwartet, dass es sich um eine zwischen Bedingung für DXVA-Accelerators (DirectX Video Acceleration) handelt, die 10-Bit-oder 16-Bit-4:2:2-Videos unterstützen.

### <a name="y216-and-y210"></a>Y216 und Y210

In diesen zwei verpackten Formaten wird jedes Pixel Paar als Array von vier **Wörtern** gespeichert, wie in der folgenden Abbildung dargestellt.

![Diagramm, das das Pixel Layout y216 und y210 anzeigt.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

Das erste **Wort** im Array enthält das erste y-Beispiel im Paar, das zweite **Wort** enthält das U-Beispiel, das dritte **Wort** enthält das zweite y-Beispiel, und das vierte **Wort** enthält das V-Beispiel.

Y210 ist mit Y216 identisch, mit dem Unterschied, dass jedes Beispiel nur 10 Bits signifikanter Daten enthält. Die am wenigsten wichtigen 6 Bits werden auf 0 (null) festgelegt, wie zuvor beschrieben.

### <a name="444-formats"></a>4:4:4 Formate

Es werden zwei 4:4:4-Formate mit den FourCC-Codes Y410 und Y416 definiert. Beide sind gepackte Formate.

### <a name="y410"></a>Y410

Dieses Format ist eine gepackte 10-Bit-Darstellung, die 2 Bits von Alpha enthält. Jedes Pixel wird als einzelnes **DWORD** mit dem im folgenden Diagramm dargestellten Arbeitsspeicher Layout codiert.

![Diagramm, das das y410 Pixel Layout anzeigt.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

Bits 0-9 enthalten das U-Beispiel, Bits 10-19 enthalten das Y-Beispiel, Bits 20-29 das V-Beispiel und Bits 30-31 den Alpha-Wert. Um anzugeben, dass ein Pixel vollständig undurchsichtig ist, muss eine Anwendung die beiden Alpha Bits gleich 0x03 festlegen.

### <a name="y416"></a>Y416

Dieses Format ist eine gepackte 16-Bit-Darstellung, die 16 Bits von Alpha enthält. Jedes Pixel wird als Paar von **DWORD** s codiert, wie in der folgenden Abbildung dargestellt.

![Diagramm, das das y416 Pixel Layout anzeigt.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

Bits 0-15 enthalten das U-Beispiel, Bits 16-31 enthalten das Y-Beispiel, Bits 32-47 das V-Beispiel und Bits 48-63 den Alpha-Wert.

Um anzugeben, dass ein Pixel vollständig undurchsichtig ist, muss eine Anwendung die beiden Alpha Bits gleich 0xFFFF festlegen. Dieses Format dient primär als zwischen Format bei der Bildverarbeitung, um die Ansammlung von Fehlern zu vermeiden.

## <a name="preferred-yuv-formats"></a>Bevorzugte YUV-Formate

In der folgenden Tabelle werden die bevorzugten YUV-Formate einschließlich 8-Bit-Formaten aufgelistet.



| Format | Chroma-Sampling | Gepackt oder planare | Bits pro Kanal |
|--------|-----------------|------------------|------------------|
| Ayuv   | 4:4:4           | Stop           | 8                |
| Y410   | 4:4:4           | Stop           | 10               |
| Y416   | 4:4:4           | Stop           | 16               |
| AI44   | 4:4:4           | Stop           | Das Paletten       |
| Im YUY2   | 4:2:2           | Stop           | 8                |
| Y210   | 4:2:2           | Stop           | 10               |
| Y216   | 4:2:2           | Stop           | 16               |
| P210   | 4:2:2           | Planare           | 10               |
| P216   | 4:2:2           | Planare           | 16               |
| NV12   | 4:2:0           | Planare           | 8                |
| P010   | 4:2:0           | Planare           | 10               |
| P016   | 4:2:0           | Planare           | 16               |
| NV11   | 4:1:1           | Planare           | 8                |



 

Es wird empfohlen, dass ein Objekt, das eine bestimmte Bittiefe und ein Chroma-Samplings unterstützt, die entsprechenden YUV-Formate unterstützt, die in dieser Tabelle aufgeführt sind. (Objekte unterstützen möglicherweise zusätzliche Formate, die hier nicht aufgeführt sind.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfohlene 8-Bit-YUV-Formate für Video Rendering](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Video Untertyp-GUIDs](video-subtype-guids.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> </dl>

 

 




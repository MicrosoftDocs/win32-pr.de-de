---
title: Nicht komprimierte Medienuntertypen
description: Nicht komprimierte Medienuntertypen
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- Windows Medienformat-SDK, Medientypen
- Advanced Systems Format (ASF), Medientypen
- ASF (Advanced Systems Format), Medientypen
- Windows Medienformat-SDK, nicht komprimierte Medienuntertypen
- Advanced Systems Format (ASF), nicht komprimierte Medienuntertypen
- ASF (Advanced Systems Format), nicht komprimierte Medienuntertypen
- Medientypen, nicht komprimierte Medienuntertypen
- Unkomprimierte Medienuntertypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdbd691a3b43a83656feffa1be114b5180d24cc5e29359b4168a4656d99fd03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807340"
---
# <a name="uncompressed-media-subtypes"></a>Nicht komprimierte Medienuntertypen

In der folgenden Tabelle sind die Untertypen für nicht komprimierte Medien aufgeführt. Dies sind Typen, die als Eingabe- und Ausgabeformate verwendet werden, sowie Formate für unkomprimierte Streams. Nicht alle Typen in den folgenden Tabellen werden in jeder Hinsicht unterstützt. Unterstützte Eingabe- und Ausgabeformattypen können nach Codec im Writer bzw. Reader/synchronen Reader aufzählen. Informationen zu den typen, die für unkomprimierte Streams unterstützt werden, finden Sie unter [Verwenden von unkomprimiertem Audio und Video Streams](using-uncompressed-audio-and-video-streams.md).

Die verschiedenen hier aufgeführten RGB- und palettisierten RGB-Videotypen definieren Farben im RGB-Format, in dem jede Farbe durch die Intensitätswerte der roten, grünen und blauen Komponenten des Pixels dargestellt wird. Jeder Intensitätswert kann zwischen 0 und 255 liegen, für etwa 16,78 Millionen eindeutige Farben. RGB lässt sich problemlos in Farbwerte übersetzen, die für Computermonitore verwendet werden, die rote, grüne und blaue Farbflächen verwenden, um Farben anzuzeigen. Palettierte Videotypen müssen Paletteninformationen enthalten, die direkt der [**WMVIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) folgen. Ebenso erfordert ein 16-Bit-Video Bitfeldinformationen, die nach der WMVIDEOINFOHEADER-Struktur enthalten sein sollten.

Einige der Medienuntertypen in der folgenden Tabelle bieten weniger Farben als das RGB-System kann, wie in der Spalte Beschreibung beschrieben. In palettisierten RGB-Typen stellen Farben in der Palette RGB-Werte dar, werden jedoch durch einen Wert angegeben, der die Position der Farbe in der Palette angibt.



| Nicht komprimierter Medienuntertyp | BESCHREIBUNG                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ RGB1       | Palettiertes RGB-Video mit 1 Farbbit, das 2 Farben darstellt. Wird normalerweise für monocolore Bilder verwendet.                                                                                                                         |
| WMMEDIASUBTYPE \_ RGB4       | Palettiertes RGB-Video mit 4 Farbbits, die 16 Farben darstellen.                                                                                                                                                           |
| WMMEDIASUBTYPE \_ RGB8       | Palettiertes RGB-Video mit 8 Farbbits, die 256 Farben darstellen.                                                                                                                                                          |
| WMMEDIASUBTYPE \_ RGB565     | RGB-Video mit 16 Farbbits, die 65.536 Farben darstellen. Dieses Format verwendet 5 Bits für Rot, 6 Bits für Grün und 5 Bits für Blau.                                                                                         |
| WMMEDIASUBTYPE \_ RGB555     | RGB-Video mit 16 Farbbits, die 32.768 Farben darstellen. Dieses Format verwendet 5 Bits für jede Farbe und ignoriert das 16. Bit.                                                                                           |
| WMMEDIASUBTYPE \_ RGB24      | RGB-Video mit 24 Farbbits, die alle 16.777.216 Farben darstellen, die für das RGB-Farbdarstellungsschema verfügbar sind. Dieses Format verwendet 8 Bits für jeden Farbintensiven Wert.                                                |
| WMMEDIASUBTYPE \_ RGB32      | RGB-Video mit 32 Farbbits, die alle 16.777.216 Farben darstellen, die für das RGB-Farbdarstellungsschema verfügbar sind. Dieses Format verwendet 8 Bits für jede Farbe und reserviert die verbleibenden 8 Bits für Transparenzinformationen. |
| WMMEDIASUBTYPE \_ I420       | YUV-Video im planaren Format 4:2:0 gespeichert, wobei zuerst die U-Ebene und dann die V-Ebene angezeigt wird.                                                                                                                      |
| WMMEDIASUBTYPE \_ IYUV       | Identisch mit I420.                                                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ YV12       | YUV-Video im planaren Format 4:2:0 gespeichert, wobei zuerst die V-Ebene und dann die U-Ebene angezeigt wird. YV12 ist mit I420 identisch, mit der Ausnahme, dass die Sie- und die V-Ebene umgeschaltet werden.                                               |
| WMMEDIASUBTYPE \_ YUY2       | YUV-Video im gepackten 4:2:2-Format gespeichert.                                                                                                                                                                                 |
| WMMEDIASUBTYPE \_ UYVY       | YUV-Video im gepackten 4:2:2-Format gespeichert. Ähnlich wie YUY2, aber mit unterschiedlicher Datenreihenfolge.                                                                                                                            |
| WMMEDIASUBTYPE \_ YVYO       | YUV-Video im gepackten 4:2:2-Format gespeichert. Ähnlich wie YUY2, aber mit unterschiedlicher Datenreihenfolge.                                                                                                                            |
| WMMEDIASUBTYPE \_ P422       | YUV-Video, das mit einem planaren 4:2:2-Format gespeichert wird.                                                                                                                                                                            |
| WMMEDIASUBTYPE \_ YVU9       | YUV-Video im planaren Format 16:1:1 gespeichert.                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ PCM        | Unkomprimierte Audiodaten, die mitHilfe von PulseCode-Pulse-Code gespeichert werden.                                                                                                                                                              |
| WMMEDIASUBTYPE \_ DRM        | Unkomprimierte, aber verschlüsselte Audiodaten, die mit einem sicheren Audiopfad verwendet werden.                                                                                                                                                       |
| WMSCRIPTTYPE \_ TwoStrings   | Skriptbefehle, die aus einer Zeichenfolge mit dem Befehlstyp und einer Zeichenfolge mit den Befehlsdaten bestehen. Dies ist der einzige unterstützte Skripttyp im Windows Media Format SDK.                                     |
| WMMEDIASUBTYPE \_ WebStream  | Dateiübertragungsdaten, die HTML-Dateien und -Komponenten für Webstreaming enthalten.                                                                                                                                               |
| WMMEDIASUBTYPE \_ VIDEOIMAGE | Eingabetyp für den Windows Media Video 9-Bildcodec. Beispiele sind eine Kombination aus Bitmapbildern und Transformationsdaten.                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Zuweisen von Ausgabeformaten**](assigning-output-formats.md)
</dt> <dt>

[**Komprimierte Medienuntertypen**](compressed-media-subtypes.md)
</dt> <dt>

[**Medientypbezeichner**](media-type-identifiers.md)
</dt> <dt>

[**Medientypen**](media-types.md)
</dt> <dt>

[**So geben Sie Eingabeformate an**](to-enumerate-input-formats.md)
</dt> </dl>

 

 





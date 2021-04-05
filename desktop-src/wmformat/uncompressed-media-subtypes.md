---
title: Nicht komprimierte Medien Untertypen
description: Nicht komprimierte Medien Untertypen
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- Windows Media-Format-SDK, Medientypen
- Advanced Systems Format (ASF), Medientypen
- ASF (Advanced Systems Format), Medientypen
- Windows Media-Format-SDK, unkomprimierte Medien Untertypen
- Advanced Systems Format (ASF), unkomprimierte Medien Untertypen
- ASF (Advanced Systems Format), unkomprimierte Medien Untertypen
- Medientypen, nicht komprimierte Medien Untertypen
- nicht komprimierte Medien Untertypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7ea730b480f738caa6e0eeccb8674f3cdc4c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709599"
---
# <a name="uncompressed-media-subtypes"></a>Nicht komprimierte Medien Untertypen

In der folgenden Tabelle sind die Untertypen der nicht komprimierten Medien aufgeführt. Dabei handelt es sich um Typen, die als Eingabe-und Ausgabeformate und Formate für nicht komprimierte Streams verwendet werden. Nicht alle Typen in den folgenden Tabellen werden auf alle Arten unterstützt. Unterstützte Eingabe-und Ausgabeformate können von Codec im Writer bzw. Reader/synchroner Reader aufgelistet werden. Informationen zu den Typen, die für nicht komprimierte Streams unterstützt werden, finden [Sie unter Verwenden von nicht komprimierten Audiodatenströmen](using-uncompressed-audio-and-video-streams.md).

Die verschiedenen hier aufgeführten RGB-und Paletten-RGB-Video Typen definieren Farben im RGB-Format, wobei jede Farbe durch die Intensitätswerte der roten, grünen und blauen Komponenten des Pixels dargestellt wird. Jeder Intensitätswert kann zwischen 0 und 255 liegen, bei ungefähr 16.780.000 eindeutigen Farben. RGB übersetzt problemlos in Farbwerte, die für Computer Monitore verwendet werden, die rote, grüne und blaue Phosphors zum Anzeigen von Farben verwenden. In den Video Typen mit Paletten müssen Paletteninformationen direkt nach der [**wmvideoinfoheader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) -Struktur enthalten sein. Ebenso benötigt das 16-Bit-Video bitfeldinformationen, die nach der wmvideoinfoheader-Struktur eingeschlossen werden müssen.

Einige der Medien Untertypen in der folgenden Tabelle bieten weniger Farben als das RGB-System, wie in der Beschreibungs Spalte beschrieben. In Paletten-RGB-Typen stellen Farben in der Palette RGB-Werte dar, werden jedoch durch einen Wert angegeben, der die Position der Farbe in der Palette angibt.



| Unkomprimierter Medien Untertyp | BESCHREIBUNG                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wmmediasubtype \_ RGB1       | Paletten-RGB-Video mit einem farbbit, das zwei Farben darstellt. Wird normalerweise für monochrome Bilder verwendet.                                                                                                                         |
| Wmmediasubtype \_ RGB4       | Paletten-RGB-Video mit 4 Farbbits, die 16 Farben darstellen.                                                                                                                                                           |
| Wmmediasubtype \_ RGB8       | Paletten-RGB-Video mit 8 Farbbits, die 256 Farben darstellen.                                                                                                                                                          |
| Wmmediasubtype \_ RGB565     | RGB-Video mit 16 Farbbits, die 65.536 Farben darstellen. Dieses Format verwendet 5 Bits für Rot, 6 Bits für Grün und 5 Bits für blau.                                                                                         |
| Wmmediasubtype \_ RGB555     | RGB-Video mit 16 Farbbits, die 32.768 Farben darstellen. Dieses Format verwendet für jede Farbe 5 Bits und ignoriert das sechzehnte Bit.                                                                                           |
| Wmmediasubtype \_ RGB24      | RGB-Video mit 24 Farbbits, die alle für das RGB-Farb Darstellungs Schema verfügbaren 16.777.216-Farben darstellen. Dieses Format verwendet 8 Bits für jeden Farb Intensitätswert.                                                |
| Wmmediasubtype \_ RGB32      | RGB-Video mit 32 Farbbits, die alle für das RGB-Farb Darstellungs Schema verfügbaren 16.777.216-Farben darstellen. In diesem Format werden für jede Farbe 8 Bits verwendet, und die restlichen 8 Bits werden für Transparenz Informationen reserviert. |
| Wmmediasubtype \_ I420       | YUV-Video, das im planare 4:2:0-Format gespeichert ist, wobei die U-Ebene zuerst angezeigt wird, gefolgt von der V-Ebene.                                                                                                                      |
| wmmediasubtype \_ IYUV       | Identisch mit I420.                                                                                                                                                                                                       |
| Wmmediasubtype \_ YV12       | YUV-Video, das im planare 4:2:0-Format gespeichert ist, wobei die V-Ebene zuerst angezeigt wird, gefolgt von der U-Ebene. YV12 ist mit I420 identisch, mit der Ausnahme, dass die-und-V-Ebenen gewechselt werden.                                               |
| Wmmediasubtype \_ im YUY2       | YUV-Video im gepackten 4:2:2-Format gespeichert.                                                                                                                                                                                 |
| wmmediasubtype \_ UYVY       | YUV-Video im gepackten 4:2:2-Format gespeichert. Vergleichbar mit im YUY2, aber mit einer unterschiedlichen Datenreihen Folge.                                                                                                                            |
| wmmediasubtype \_ yvyu       | YUV-Video im gepackten 4:2:2-Format gespeichert. Vergleichbar mit im YUY2, aber mit einer unterschiedlichen Datenreihen Folge.                                                                                                                            |
| Wmmediasubtype \_ P422       | YUV-Video, das mit einem planare 4:2:2-Format gespeichert wird.                                                                                                                                                                            |
| Wmmediasubtype \_ YVU9       | YUV-Video, das im planare 16:1:1-Format gespeichert ist.                                                                                                                                                                                |
| wmmediasubtype \_ PCM        | Nicht komprimierte Audiodaten, die mithilfe von Pulse Code-Modulation gespeichert werden                                                                                                                                                              |
| wmmediasubtype \_ DRM        | Nicht komprimierte, aber verschlüsselte Audiodaten, die mit einem sicheren Audiopfad verwendet werden.                                                                                                                                                       |
| Wmscripttype \_ twostrings   | Skript Befehle, die aus einer Zeichenfolge bestehen, die den Befehlstyp und eine Zeichenfolge mit den Befehlsdaten enthält. Dies ist der einzige unterstützte Skripttyp im Windows Media-Format-SDK.                                     |
| Wmmediasubtype- \_ Webstream  | Datei Übertragungsdaten, die HTML-Dateien und-Komponenten für das Webstreaming enthalten.                                                                                                                                               |
| wmmediasubtype- \_ Videoimage | Eingabetyp für den Windows Media Video 9-Bildcodec. Beispiele sind eine Kombination aus Bitmap-Bildern und Transformations Daten.                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Zuweisen von Ausgabeformaten**](assigning-output-formats.md)
</dt> <dt>

[**Komprimierte Medien Untertypen**](compressed-media-subtypes.md)
</dt> <dt>

[**Medientyp-IDs**](media-type-identifiers.md)
</dt> <dt>

[**Medientypen**](media-types.md)
</dt> <dt>

[**So zählen Sie Eingabeformate auf**](to-enumerate-input-formats.md)
</dt> </dl>

 

 





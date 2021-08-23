---
description: Texturzuordnungen sind digitalisierte Bilder, die auf dreidimensionalen Formen gezeichnet werden, um visuelle Details hinzuzufügen.
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: Komprimierte Texturressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd4e21dfd0e042f8d8d97fd8415529a2b4a5a952334df3e7f39ef8ae20a890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989280"
---
# <a name="compressed-texture-resources-direct3d-9"></a>Komprimierte Texturressourcen (Direct3D 9)

Texturzuordnungen sind digitalisierte Bilder, die auf dreidimensionalen Formen gezeichnet werden, um visuelle Details hinzuzufügen. Sie werden diesen Formen während der Rasterung zugeordnet, und der Prozess kann große Mengen an Systembus und Arbeitsspeicher verbrauchen. Um den von Texturen verbrauchten Arbeitsspeicher zu reduzieren, unterstützt Direct3D die Komprimierung von Texturoberflächen. Einige Direct3D-Geräte unterstützen komprimierte Texturoberflächen nativ. Wenn Sie auf solchen Geräten eine komprimierte Oberfläche erstellt und die Daten in diese geladen haben, kann die Oberfläche in Direct3D wie jede andere Texturoberfläche verwendet werden. Direct3D verarbeitet die Dekomprimierung, wenn die Textur einem 3D-Objekt zugeordnet wird.

## <a name="storage-efficiency-and-texture-compression"></a>Storage Effizienz und Texturkomprimierung

Bei allen Texturkomprimierungsformaten handelt es sich um zwei Komprimierungsformate. Obwohl dies nicht bedeutet, dass eine Textur notwendigerweise quadratisch ist, bedeutet dies, dass sowohl x als auch y die Zweier-Kraft sind. Wenn eine Textur beispielsweise ursprünglich 512 mal 128 Bytes beträgt, wäre die nächste mipmapping 256 mal 64 und so weiter, bei der jede Ebene um eine Zweierleistung abnimmt. Bei niedrigeren Ebenen, bei denen die Textur nach 16 durch 2 und 8 durch 1 gefiltert wird, werden Bits verschwendet, da der Komprimierungsblock immer ein 4-by-4-Block von Texel ist. Nicht verwendete Teile des Blocks werden aufpaddiert. Obwohl es verschwendete Bits auf den niedrigsten Ebenen gibt, ist der Gesamtgewinn immer noch signifikant. Der schlechteste Fall ist theoretisch eine 2K um 1 Textur (2⁰ Leistung). Hier wird nur eine einzelne Pixelzeile pro Block codiert, während der Rest des Blocks nicht verwendet wird.

## <a name="mixing-formats-within-a-single-texture"></a>Mischen von Formaten innerhalb einer einzelnen Textur

Es ist wichtig zu beachten, dass jede einzelne Textur angeben muss, dass ihre Daten als 64 oder 128 Bits pro Gruppe von 16 Texeln gespeichert werden. Wenn für die Textur 64-Bit-Blöcke verwendet werden , also dxt1 formatieren, ist es möglich, das opake alpha-Format und das 1-Bit-Alphaformat pro Block innerhalb derselben Textur zu mischen. Anders ausgedrückt: Der Vergleich der Ganzzahlgröße ohne Vorzeichen von Farbe 0 und Farbe 1 wird für jeden Block mit \_ \_ 16 Texeln eindeutig durchgeführt.

Sobald die 128-Bit-Blöcke verwendet werden, muss der Alphakanal entweder explizit (format DXT2 und DXT3) oder interpolierter Modus (Format DXT4 und DXT5) für die gesamte Textur angegeben werden. Wenn der interpolierte Modus (FORMAT DXT4 und DXT5) ausgewählt ist, können wie bei der Farbe entweder acht interpolierte Alphas oder sechs interpolierte Alphas blockweise verwendet werden. Auch hier wird der Größenvergleich von Alpha 0 und Alpha 1 auf \_ Block-für-Block-Basis \_ eindeutig durchgeführt.

Direct3D bietet Dienste zum Komprimieren von Oberflächen, die zum Texturieren von 3D-Modellen verwendet werden. Dieser Abschnitt enthält Informationen zum Erstellen und Bearbeiten der Daten auf einer komprimierten Texturoberfläche.

Informationen finden Sie in den folgenden Themen.

-   [Nicht transparente und 1-Bit-Alphatextur (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Texturen mit Alphakanälen (Direct3D 9)](textures-with-alpha-channels.md)
-   [Komprimierte Texturformate (Direct3D 9)](compressed-texture-formats.md)
-   [Verwenden von komprimierten Texturen (Direct3D 9)](using-compressed-textures.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 




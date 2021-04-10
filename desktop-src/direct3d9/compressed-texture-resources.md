---
description: Textur Karten sind digitalisierte Bilder, die auf dreidimensionalen Formen gezeichnet werden, um visuelle Details hinzuzufügen.
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: Komprimierte Textur Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b7ef048c0e1780f92246a407863a4fa48a94a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214256"
---
# <a name="compressed-texture-resources-direct3d-9"></a>Komprimierte Textur Ressourcen (Direct3D 9)

Textur Karten sind digitalisierte Bilder, die auf dreidimensionalen Formen gezeichnet werden, um visuelle Details hinzuzufügen. Diese Formen werden während der rasterisierung in diese Formen zugeordnet, und der Prozess kann eine große Menge an System Bus und Arbeitsspeicher beanspruchen. Direct3D unterstützt die Komprimierung von Textur Oberflächen, um den von Texturen genutzten Arbeitsspeicher zu reduzieren. Einige Direct3D-Geräte unterstützen komprimierte Textur Oberflächen nativ. Wenn Sie auf solchen Geräten eine komprimierte Oberfläche erstellt und die Daten darin geladen haben, kann die Oberfläche in Direct3D wie jede andere Textur Oberfläche verwendet werden. Direct3D behandelt die Komprimierung, wenn die Textur einem 3D-Objekt zugeordnet wird.

## <a name="storage-efficiency-and-texture-compression"></a>Speichereffizienz und Textur Komprimierung

Alle Textur Komprimierungs Formate sind zwei. Obwohl dies nicht bedeutet, dass eine Textur zwangsläufig quadratisch ist, bedeutet dies, dass sowohl x als auch y die beiden Kräfte sind. Wenn eine Textur z. b. ursprünglich 512 x 128 Bytes ist, wäre die nächste Mipmapping 256 von 64 usw., wobei jede Ebene durch eine Potenz von zwei verringert wird. Bei niedrigeren Ebenen, bei denen die Textur nach 16 und 8 um 1 gefiltert wird, gibt es vergeudete Bits, da der Komprimierungs Block immer ein 4 x 4-Block von texeln ist. Nicht verwendete Teile des Blocks werden aufgefüllt. Obwohl es auf den niedrigsten Ebenen verwaist Bits gibt, ist der Gesamtgewinn weiterhin signifikant. Der schlimmste Fall ist theoretisch eine 2-k-bis 1-Textur (2 ⁰ Potenz). Hier wird nur eine einzelne Zeile mit Pixeln pro Block codiert, während der restliche Block nicht verwendet wird.

## <a name="mixing-formats-within-a-single-texture"></a>Mischen von Formaten innerhalb einer einzelnen Textur

Beachten Sie, dass jede einzelne Textur angeben muss, dass Ihre Daten als 64-oder 128 Bits pro Gruppe von 16 texeln gespeichert werden. Wenn 64-Bit-Blöcke, d. h. Format DXT1, für die Textur verwendet werden, ist es möglich, die nicht transparenten und 1-Bit-Alpha Formate auf Block Basis innerhalb derselben Textur zu mischen. Anders ausgedrückt: der Vergleich der Größenordnung ohne Vorzeichen von Farbe \_ 0 und Farbe \_ 1 wird für jeden Block von 16 texeln eindeutig ausgeführt.

Sobald die 128-Bit-Blöcke verwendet werden, muss der Alphakanal entweder im expliziten Format (Format DXT2 und DXT3) oder im interformatierten Modus (Format DXT4 und DXT5) für die gesamte Textur angegeben werden. Wenn interaktivierter Modus (Format DXT4 und DXT5) ausgewählt ist, können die beiden beiden interformatierten Premultiplied-Modi oder sechs interpoliert Premultiplied-Modi auf blockweise verwendet werden. Auch hier wird der Größenvergleich von Alpha \_ 0 und Alpha \_ 1 eindeutig auf Block-für-Block-Basis durchgeführt.

Direct3D bietet Dienste zum Komprimieren von Oberflächen, die für die Texturierung von 3D-Modellen verwendet werden. Dieser Abschnitt enthält Informationen zum Erstellen und Bearbeiten der Daten in einer komprimierten Textur Oberfläche.

Die Informationen sind in den folgenden Themen enthalten.

-   [Undurchsichtige und 1-Bit-Alpha Texturen (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Texturen mit Alpha Kanälen (Direct3D 9)](textures-with-alpha-channels.md)
-   [Komprimierte Textur Formate (Direct3D 9)](compressed-texture-formats.md)
-   [Verwenden von komprimierten Texturen (Direct3D 9)](using-compressed-textures.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 




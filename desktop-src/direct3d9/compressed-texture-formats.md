---
description: Dieser Abschnitt enthält Informationen über die interne Organisation von komprimierten Textur Formaten.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Komprimierte Textur Formate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748800"
---
# <a name="compressed-texture-formats-direct3d-9"></a>Komprimierte Textur Formate (Direct3D 9)

Dieser Abschnitt enthält Informationen über die interne Organisation von komprimierten Textur Formaten. Sie benötigen diese Details nicht zur Verwendung komprimierter Texturen, da Sie D3DX-Funktionen für die Konvertierung in und aus komprimierten Formaten verwenden können. Diese Informationen sind jedoch nützlich, wenn Sie direkt mit komprimierten Oberflächendaten arbeiten möchten.

Direct3D verwendet ein Komprimierungs Format, das Textur Zuordnungen in 4 x 4 textrotze unterteilt. Wenn die Textur keine Transparenz enthält (nicht transparent) oder wenn die Transparenz durch ein 1-Bit-Alpha angegeben wird, stellt ein 8-Byte-Block den Textur Zuordnungs Block dar. Wenn die Textur Zuordnung transparente Texels mit einem Alphakanal enthält, stellt Sie einen 16-Byte-Block dar.

-   [Undurchsichtige und 1-Bit-Alpha Texturen (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Texturen mit Alpha Kanälen (Direct3D 9)](textures-with-alpha-channels.md)

Jede einzelne Textur muss angeben, dass Ihre Daten als 64-oder 128 Bits pro Gruppe von 16 texeln gespeichert werden. Wenn 64-Bit-Blöcke, d. h. Format DXT1, für die Textur verwendet werden, ist es möglich, die nicht transparenten und 1-Bit-Alpha Formate auf Block Basis innerhalb derselben Textur zu mischen. Anders ausgedrückt: der Vergleich der Größenordnung ohne Vorzeichen von Farbe \_ 0 und Farbe \_ 1 wird für jeden Block von 16 texeln eindeutig ausgeführt.

Wenn 128-Bit-Blöcke verwendet werden, muss der Alphakanal entweder im expliziten Format (Format DXT2 oder DXT3) oder im interinterinterformatierten Modus (Format DXT4 oder DXT5) für die gesamte Textur angegeben werden. Wenn der interaktivierte Modus ausgewählt ist, können die beiden acht interaktivierten Premultiplied-und sechs interpoliert Premultiplied-Modi in Form von Farben für blockweise verwendet werden. Auch hier wird der Größenvergleich von Alpha \_ 0 und Alpha \_ 1 eindeutig auf Block-für-Block-Basis durchgeführt.

Die Tonhöhe für DXTn-Formate unterscheidet sich von dem, was in DirectX 7,0 zurückgegeben wurde. Die Tonhöhe wird jetzt in Bytes (nicht in Blöcken) gemessen. Wenn Sie z. b. eine Breite von 16 haben, verfügen Sie über eine Höhe von vier Blöcken (4 \* 8 für DXT1, 4 \* 16 für DXT2-5).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komprimierte Textur Ressourcen](compressed-texture-resources.md)
</dt> </dl>

 

 




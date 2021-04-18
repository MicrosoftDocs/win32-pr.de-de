---
description: Frühe, computergenerierte 3D-Images, obwohl Sie in der Regel für Ihre Zeit erweitert sind, haben tendenziell ein glänzendes Kunststoff Erscheinungsbild.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Grundlegende texturierungskonzepte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338923"
---
# <a name="basic-texturing-concepts-direct3d-9"></a>Grundlegende texturierungskonzepte (Direct3D 9)

Frühe, computergenerierte 3D-Images, obwohl Sie in der Regel für Ihre Zeit erweitert sind, haben tendenziell ein glänzendes Kunststoff Erscheinungsbild. Sie fehlten nicht die Typen von Markierungen, wie z. b. scuffs, Risse, Fingerabdrücke und smudges, die 3D-Objekten eine realistische visuelle Komplexität einräumen. In den letzten Jahren haben sich die Texturen in den Entwicklern als Tool zur Verbesserung des Realismus von computergenerierten 3D-Images erfreut.

In der täglichen Verwendung bezieht sich die Wort Textur auf die glätttheit oder die rautheit eines Objekts. In Computergrafiken ist eine Textur jedoch eine Bitmap von Pixel Farben, die einem Objekt die Darstellung der Textur verleiht.

Da Direct3D-Texturen Bitmaps sind, kann jede Bitmap auf ein Direct3D-primitiv angewendet werden. Beispielsweise können Anwendungen Objekte erstellen und bearbeiten, für die offenbar ein Holz kornmuster vorhanden ist. Grass, Dirt und Rocks können auf einen Satz von 3D-primitiven angewendet werden, die einen Hügel bilden. Das Ergebnis ist ein realistisch aussehende Hügel. Sie können Texturing auch zum Erstellen von Effekten verwenden, z. b. bei Vorzeichen an einem Straßenrand, bei Rock Schichten in einer Klippe oder in der Darstellung von Marmor auf einem Boden.

Außerdem unterstützt Direct3D erweiterte texturierungstechniken, wie z. b. Textur Mischung, mit oder ohne Transparenz und einfache Zuordnung. Weitere Informationen finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md) und [Light Mapping with Texturen (Direct3D 9)](light-mapping-with-textures.md).

Wenn Ihre Anwendung ein HAL-Gerät (Hardware Abstraktion Layer) oder ein Software Gerät erstellt, kann Sie die Texturen 8, 16, 24, 32, 64 oder 128-Bit verwenden.

Weitere Informationen finden Sie in den folgenden Themen.

-   [Textur Adressierungs Modi (Direct3D 9)](texture-addressing-modes.md)
-   [Struktur Änderungs Bereiche (Direct3D 9)](texture-dirty-regions.md)
-   [Textur Paletten (Direct3D 9)](texture-palettes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 




---
title: Beispiel für DDS-volumetextur
description: Verwenden Sie für eine volumetextur die DDSCAPS \_ Complex, DDSCAPS2 \_ Volume, ddsd \_ -Tiefe, Flags und Set und dwtiefe. Eine volumetextur ist eine Erweiterung einer Standard Textur für Direct3D 9; eine volumetextur kann mit oder ohne Mipmaps definiert werden.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338194"
---
# <a name="dds-volume-texture-example"></a>Beispiel für DDS-volumetextur

Verwenden Sie für eine volumetextur die DDSCAPS \_ Complex, DDSCAPS2 \_ Volume, ddsd \_ -Tiefe, Flags und Set und dwtiefe. Eine volumetextur ist eine Erweiterung einer Standard Textur für Direct3D 9; eine volumetextur kann mit oder ohne Mipmaps definiert werden.

Für Volumes ohne Mipmaps wird jedes tiefen Slice in der richtigen Reihenfolge in die Datei geschrieben. Wenn Mipmaps eingeschlossen werden, werden alle tiefen Slices für eine bestimmte MipMap-Ebene miteinander geschrieben, wobei jede Ebene die Hälfte so viele Slices wie die vorherige Ebene mit einem Mindestwert von 1 enthält.

Beispielsweise würde eine 64-by-64 von-4-volumekarte, die das Pixel Format R8G8B8 (3 Bytes pro Pixel) mit allen MipMap-Ebenen verwendet, Folgendes enthalten:



| DDS-Komponenten                      | \# Satz    |
|-------------------------------------|-------------|
| header                              | 128 Bytes   |
| 64-bis-64 Slice 1 von 4 Hauptbild.   | 12288 bytes |
| 64-bis-64 Slice 2 von 4 Hauptbild.   | 12288 bytes |
| 64-bis-64 Slice 3 von 4 Hauptbild.   | 12288 bytes |
| 64-bis-64 Slice 4 von 4 Hauptbild.   | 12288 bytes |
| 32-bis-32 Slice 1 von 2 MipMap-Bild. | 3072 bytes  |
| 32-bis-32 Slice 2 von 2 MipMap-Bild. | 3072 bytes  |
| 16-bis-16-Slice 1 von 1 MipMap-Bild. | 768 Bytes   |
| 8 x 8 Slice 1 von 1 MipMap-Bild.   | 192 Bytes   |
| 4 x 4 Slice 1 von 1 MipMap-Bild.   | 48 Bytes    |
| 2:2 Slice 1 von 1 MipMap-Bild.   | 12 Bytes    |
| 1 bis 1 Slice 1 von 1 MipMap-Bild.   | 3 Byte     |



 

Beachten Sie, dass die kleinste MipMap-Ebene nur 3 Bytes beträgt, da die Bitzahl 24 beträgt und auf dieser Ebene keine Komprimierung hinzugefügt wird.

Unterstützung für Volumentexturen wurde in DirectX 8 hinzugefügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 





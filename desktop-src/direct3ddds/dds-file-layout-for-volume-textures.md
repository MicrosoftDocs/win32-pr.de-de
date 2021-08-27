---
title: Beispiel für DDS-Volumetextur
description: Verwenden Sie für eine Volumetextur DDSCAPS \_ COMPLEX, DDSCAPS2 \_ VOLUME, DDSD \_ DEPTH, flags and set und dwDepth. Eine Volumentextur ist eine Erweiterung einer Standardtextur für Direct3D 9. Eine Volumetextur kann mit oder ohne Mipmaps definiert werden.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79501ea3ffa6f4a660f4ab3b248fedbdc7df17bf8af94520cad5808c3c611fd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025740"
---
# <a name="dds-volume-texture-example"></a>Beispiel für DDS-Volumetextur

Verwenden Sie für eine Volumetextur DDSCAPS \_ COMPLEX, DDSCAPS2 \_ VOLUME, DDSD \_ DEPTH, flags and set und dwDepth. Eine Volumentextur ist eine Erweiterung einer Standardtextur für Direct3D 9. Eine Volumetextur kann mit oder ohne Mipmaps definiert werden.

Bei Volumes ohne Mipmaps wird jeder Tiefenslice in der Reihenfolge in die Datei geschrieben. Wenn Mipmaps eingeschlossen werden, werden alle Tiefenslices für eine bestimmte Mipmapebene zusammen geschrieben, und jede Ebene enthält halb so viele Slices wie die vorherige Ebene mit mindestens 1.

Eine 64-by-64-by-4-Volumezuordnung mit dem Pixelformat R8G8B8 (3 Bytes pro Pixel) mit allen Mipmap-Ebenen würde beispielsweise Folgendes enthalten:



| DDS-Komponenten                      | \# Bytes    |
|-------------------------------------|-------------|
| header                              | 128 Bytes   |
| 64 by-64 Slice 1 von 4 Hauptimages.   | 12288 Bytes |
| 64 by-64 Slice 2 von 4 Hauptimages.   | 12288 Bytes |
| 64 by-64 Slice 3 von 4 Hauptimages.   | 12288 Bytes |
| 64 by-64 Slice 4 von 4 Hauptimages.   | 12288 Bytes |
| 32 by-32 Slice 1 von 2 Mipmap-Bildern. | 3072 Bytes  |
| 32 by-32 Slice 2 von 2 Mipmap-Bildern. | 3072 Bytes  |
| 16 by-16 Slice 1 von 1 Mipmap-Bild. | 768 Bytes   |
| 8-by-8 Slice 1 von 1 Mipmap-Bild.   | 192 Bytes   |
| 4-by-4 Slice 1 von 1 Mipmap-Bild.   | 48 Bytes    |
| 2-by-2 Slice 1 von 1 Mipmap-Bild.   | 12 Bytes    |
| 1-by-1 Slice 1 von 1 Mipmap-Bild.   | 3 Byte     |



 

Beachten Sie, dass die kleinste Mipmapebene nur 3 Bytes beträgt, da die Bitanzahl 24 beträgt und auf dieser Ebene keine zusätzliche Komprimierung hinzugefügt wird.

Unterstützung für Volumetexturen wurde in DirectX 8 hinzugefügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 





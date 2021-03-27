---
title: Unterteilung von Texture2D- und Texture2DArray-Unterressourcen
description: Diese Tabellen zeigen, wie Texture2D und Texture2DArray-unter Ressourcen nebeneinander angeordnet werden.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390644"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Unterteilung von Texture2D- und Texture2DArray-Unterressourcen

Diese Tabellen zeigen, wie [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) -unter Ressourcen nebeneinander angeordnet werden. Die Werte in diesen Tabellen zählen nicht zum Ende der MIP-Verpackung.

Diese Tabelle zeigt, wie die unter Ressourcen [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) mit der Multisampling-Anzahl 1 nebeneinander dargestellt werden.



| Bits/Pixel (1 Stichprobe/Pixel) | Kachel Dimensionen (Pixel, WxH) |
|-----------------------------|-------------------------------|
| 8                           | 256x256                       |
| 16                          | Größe 256x128                       |
| 32                          | 128x128                       |
| 64                          | 128 x 64                        |
| 128                         | 64 x 64                         |
| BC1, 4                       | 512 x 256                       |
| BC2, 3, 5, 6, 7                 | 256x256                       |



 

Die von den Kachel Ressourcen nicht unterstützten Formatbit-Zahlen sind 96 bpp-Formate, Videoformate, DXGI- \_ Format \_ R1 \_ unorm, DXGI- \_ Format \_ R8G8 \_ B8G8 \_ unorm und DXGI- \_ Format \_ R8R8 \_ G8B8 \_ unorm.

Diese Tabelle zeigt, wie [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) -unter Ressourcen mit verschiedenen Multisampling-Zählungen nebeneinander angeordnet werden.



| Anzahl von mehreren Stichproben           | Aufteilen von Kachel Dimensionen oberhalb durch (WxH) |
|-----------------------------|-------------------------------|
| 1                           | 1x1                           |
| 2                           | 2x1                           |
| 4                           | 2 x 2                           |
| 8                           | 4x2                           |
| 16                          | 4x4                           |



 

Nur die Stichproben Anzahl 1 und 4 sind erforderlich (und zulässig), damit Sie mit gekachelten Ressourcen unterstützt werden. Gekachelte Ressourcen unterstützen derzeit nicht 2, 8 und 16, obwohl Sie angezeigt werden.

Implementierungen können für nicht gekachelte Ressourcen zwei, 8 und/oder 16 Sample Multisampling Antialiasing (MSAA)-Modus unterstützen, auch wenn Sie von einer gekachelten Ressource nicht unterstützt werden.

Gekachelte Ressourcen mit Stichproben Anzahl größer als 1 können 128 bpp-Formate nicht verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kacheln eines gekachelten Ressourcenbereichs](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 
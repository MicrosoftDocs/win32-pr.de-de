---
title: Unterteilung von Texture2D- und Texture2DArray-Unterressourcen
description: Diese Tabellen zeigen, wie Texture2D- und Texture2DArray-Unterressourcen gekachelt werden.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7cc181845785ab978dc5d58b1e131a7f32c34a6d04006af1ac8034f089ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530435"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Unterteilung von Texture2D- und Texture2DArray-Unterressourcen

Diese Tabellen zeigen, wie [**Texture2D-**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray-Unterressourcen**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) gekachelt werden. Die Werte in diesen Tabellen zählen nicht tail mip packing.

Diese Tabelle zeigt, wie [**Texture2D-**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray-Unterressourcen**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) mit multisample-Anzahl von 1 gekachelt werden.



| Bits/Pixel (1 Stichprobe/Pixel) | Kacheldimensionen (Pixel, WxH) |
|-----------------------------|-------------------------------|
| 8                           | 256x256                       |
| 16                          | 256 x 128                       |
| 32                          | 128 x 128                       |
| 64                          | 128 x 64                        |
| 128                         | 64 x 64                         |
| BC1,4                       | 512 x 256                       |
| BC2,3,5,6,7                 | 256x256                       |



 

Formatbitanzahlen, die für gekachelte Ressourcen nicht unterstützt werden, sind 96 BPP-Formate, Videoformate, DXGI \_ FORMAT \_ R1 \_ UNORM, DXGI \_ FORMAT \_ R8G8 \_ B8G8 \_ UNORM und DXGI \_ FORMAT \_ R8R8 \_ G8B8 \_ UNORM.

Diese Tabelle zeigt, wie [**Texture2D-**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) und [**Texture2DArray-Unterressourcen**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) mit verschiedenen Multisampelanzahlen gekachelt werden.



| Multisampleanzahl           | Kacheldimensionen über dividieren durch (WxH) |
|-----------------------------|-------------------------------|
| 1                           | 1x1                           |
| 2                           | 2x1                           |
| 4                           | 2x2                           |
| 8                           | 4x2                           |
| 16                          | 4x4                           |



 

Es sind nur die Stichprobenanzahlen 1 und 4 erforderlich (und zulässig), um mit gekachelten Ressourcen unterstützt zu werden. Gekachelte Ressourcen unterstützen derzeit 2, 8 und 16 nicht, obwohl sie angezeigt werden.

Implementierungen können auswählen, dass der MSAA-Modus (Sample MultiSample Antialiasing) für nicht gekachelte Ressourcen 2, 8 und/oder 16 unterstützt, obwohl diese nicht unterstützt werden.

Gekachelte Ressourcen mit Stichprobenanzahlen, die größer als 1 sind, können keine 128 BPP-Formate verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kacheln des Bereichs einer gekachelten Ressource](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 
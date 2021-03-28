---
title: Unterteilung von Texture3D-Unterressourcen
description: Diese Tabelle zeigt, wie Texture3D-unter Ressourcen nebeneinander angeordnet werden.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993606"
---
# <a name="texture3d-subresource-tiling"></a>Unterteilung von Texture3D-Unterressourcen

Diese Tabelle zeigt, wie [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) -unter Ressourcen nebeneinander angeordnet werden. Die Werte in dieser Tabelle zählen nicht zum Ende der MIP-Verpackung.

In dieser Tabelle wird das [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) -tichen berücksichtigt, und die x/y-Dimensionen werden um 4 dividiert, und es werden 16 Ebenen hinzugefügt. Alle Kacheln für die erste Ebene (2D-Ebene der Kacheln, die die ersten 16 Ebenen der Tiefe definieren) werden vor den nachfolgenden Ebenen angezeigt.

> [!Note]  
> Die [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) -Unterstützung in gekachelten Ressourcen wird in der ersten Implementierung von gekachelten Ressourcen nicht verfügbar gemacht, die gewünschten Kachel Formen werden hier jedoch aufgeführt, da die Unterstützung in einer zukünftigen Version möglicherweise berücksichtigt

 



| Bits/Pixel (1 Stichprobe/Pixel) | Kachel Dimensionen (Pixel, WxHxD) |
|-----------------------------|---------------------------------|
| 8                           | 64x32x32                        |
| 16                          | 32x32x32                        |
| 32                          | 32x32x16                        |
| 64                          | 32x16x16                        |
| 128                         | 16x16x16                        |
| BC1, 4                       | 128 x 64x16                       |
| BC2, 3, 5, 6, 7                 | 64x64x16                        |



 

Die von den Kachel Ressourcen nicht unterstützten Formatbit-Zahlen sind 96 bpp-Formate, Videoformate, DXGI- \_ Format \_ R1 \_ unorm, DXGI- \_ Format \_ R8G8 \_ B8G8 \_ unorm und DXGI- \_ Format \_ R8R8 \_ G8B8 \_ unorm.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kacheln eines gekachelten Ressourcenbereichs](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 
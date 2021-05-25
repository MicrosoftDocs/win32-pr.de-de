---
description: Vertex-Shader kapselt Konstanten. Diese Konstanten werden vom VS20Caps-Member von D3DCAPS9 verwendet.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342945"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

Vertex-Shader kapselt Konstanten. Diese Konstanten werden vom VS20Caps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.



| \#Definieren                              | Wert          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVS20CAPS-PRÄDIKATION \_              | (1 << 0) | Anweisungsprädikation wird unterstützt. Siehe [setp \_ comp - vs](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH | 24             | Der maximale Grad an Schachtelung dynamischer Ablaufsteuerungsanweisungen ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), wenn comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), wenn \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH | 0              | Die Mindestebene der Schachtelung dynamischer Ablaufsteuerungsanweisungen ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), wenn \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ MAX \_ NUMTEMPS                | 32             | Die maximale Anzahl von unterstützten temporären Registern.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ MIN \_ NUMTEMPS                | 12             | Die Mindestanzahl von unterstützten temporären Registern.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH  | 4              | Die maximale Tiefe der Schachtelung der Schleife [– vs](../direct3dhlsl/loop---vs.md)rep / [– vs](../direct3dhlsl/rep---vs.md) und call – [vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions.                                                                                           |
| D3DVS20 \_ MIN \_ STATICFLOWCONTROLDEPTH  | 1              | Die minimale Tiefe der Schachtelung der Schleife [– vs](../direct3dhlsl/loop---vs.md)rep / [– vs](../direct3dhlsl/rep---vs.md) und call – [vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions.                                                                                           |



 

## <a name="constant-information"></a>Konstante Informationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 

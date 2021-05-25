---
description: Shaderfunktionsflags für Pixel.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4eed8fb6c7a5c4c4da31185dc4cc8c1661f7109
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343115"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Shaderfunktionsflags für Pixel.



| \#Definieren                                     | Wert          | BESCHREIBUNG                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE      | (1 << 0) | Beliebiges Swizzling wird unterstützt.                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS  | (1 << 1) | Anweisungen zum Farbverlauf werden unterstützt.                                                                                                                                                                              |
| D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION           | (1 << 2) | Anweisungsvordication wird unterstützt. Weitere Informationen [finden Sie unter setp comp - \_ ps](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT  | (1 << 3) | Es gibt keine Beschränkung für die Anzahl der abhängigen Lesezeichen pro Anweisung.                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT | (1 << 4) | Die Anzahl der Texanweisungen ist nicht begrenzt.                                                                                                                                                              |
| D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH        | 24             | Die maximale Schachtelungsebene dynamischer Ablaufsteuerungsanweisungen (break, breakc, ifc).                                                                                                                           |
| D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH        | 0              | Die Mindestebene der Schachtelung dynamischer Ablaufsteuerungsanweisungen (break, breakc, ifc).                                                                                                                           |
| D3DPS20 \_ MAX \_ NUMTEMPS                       | 32             | Der Treiber unterstützt höchstens diese vielen temporären Register.                                                                                                                                                     |
| D3DPS20 \_ MIN \_ NUMTEMPS                       | 12             | Der Treiber unterstützt mindestens so viele temporäre Register.                                                                                                                                                    |
| D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH         | 4              | Die maximale Schachtelungstiefe der [Schleife – vs](../direct3dhlsl/loop---vs.md) / [rep – vs](../direct3dhlsl/rep---vs.md) und call – [vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions. |
| D3DPS20 \_ MIN \_ STATICFLOWCONTROLDEPTH         | 1              | Die minimale Tiefe der Schachtelung der [Schleife – vs](../direct3dhlsl/loop---vs.md) / [rep – vs.](../direct3dhlsl/rep---vs.md) [und call – vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions. |
| D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS            | 512            | Der Treiber unterstützt höchstens diese vielen Anweisungen.                                                                                                                                                           |
| D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS            | 96             | Der Treiber unterstützt mindestens diese vielen Anweisungen.                                                                                                                                                          |



 

Diese Konstanten werden vom D3DPSHADERCAPS2 \_ 0-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstanteninformationen



|  Anforderung                        | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 

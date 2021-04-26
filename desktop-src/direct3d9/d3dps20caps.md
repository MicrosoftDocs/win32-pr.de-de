---
description: Pixelshaderfunktionsflags.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2326b8f5066d34087fb543c7771a0cd547b98f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995267"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Pixelshaderfunktionsflags.



| \#Definieren                                     | Wert          | BESCHREIBUNG                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE      | (1 << 0) | Beliebiges Swizzling wird unterstützt.                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS  | (1 << 1) | Farbverlaufsanweisungen werden unterstützt.                                                                                                                                                                              |
| D3DD3DPSHADERCAPS2 \_ \_ 0-PRÄDIKATION           | (1 << 2) | Anweisungsprädikation wird unterstützt. Siehe [setp \_ comp - ps](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT  | (1 << 3) | Es gibt keine Beschränkung für die Anzahl abhängiger Lesefunktionen pro Anweisung.                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT | (1 << 4) | Es gibt keine Beschränkung für die Anzahl von Texanweisungen.                                                                                                                                                              |
| D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH        | 24             | Die maximale Schachtelungsebene von Anweisungen für die dynamische Flusssteuerung (Break, Breakc, ifc).                                                                                                                           |
| D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH        | 0              | Die minimale Schachtelungsebene der Anweisungen für die dynamische Flusssteuerung (Break, Breakc, ifc).                                                                                                                           |
| D3DPS20 \_ MAX \_ NUMTEMPS                       | 32             | Der Treiber unterstützt nur diese vielen temporären Registrierungen.                                                                                                                                                     |
| D3DPS20 \_ \_ MIN. NUMTEMPS                       | 12             | Der Treiber unterstützt mindestens diese vielen temporären Registrierungen.                                                                                                                                                    |
| D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH         | 4              | Die maximale Tiefe der Schachtelung der Schleife [– vs](../direct3dhlsl/loop---vs.md)rep / [– vs](../direct3dhlsl/rep---vs.md) und call – [vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions. |
| D3DPS20 \_ \_ MIN. STATICFLOWCONTROLDEPTH         | 1              | Die minimale Tiefe der Schachtelung der Schleife [– vs](../direct3dhlsl/loop---vs.md)rep / [– vs](../direct3dhlsl/rep---vs.md) und call – [vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions. |
| D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS            | 512            | Der Treiber unterstützt alle diese vielen Anweisungen.                                                                                                                                                           |
| D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS            | 96             | Der Treiber unterstützt mindestens diese vielen Anweisungen.                                                                                                                                                          |



 

Diese Konstanten werden vom D3DPSHADERCAPS2 \_ 0-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 

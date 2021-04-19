---
description: Vertex-Shader-Konstanten Konstanten. Diese Konstanten werden vom VS20Caps-Member von D3DCAPS9 verwendet.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344616"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

Vertex-Shader-Konstanten Konstanten. Diese Konstanten werden vom VS20Caps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.



| \#definieren                              | Wert          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVS20CAPS- \_ Prädikat              | (1 << 0) | Das Anweisungs Prädikat wird unterstützt. Weitere Informationen finden Sie unter [SETP \_ Comp-vs](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ Max \_ dynamicflowcontroltiefe | 24             | Die maximale Schachtelungs Ebene der dynamischen Fluss Steuerungs Anweisungen ([break-vs](../direct3dhlsl/break---vs.md), [break- \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), [if \_ Comp-vs](../direct3dhlsl/if-comp---vs.md), if \_ Comp-vs, if [pred-vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ Min \_ dynamicflowcontroltiefe | 0              | Die minimale Schachtelungs Ebene der dynamischen Fluss Steuerungs Anweisungen ([break-vs](../direct3dhlsl/break---vs.md), [break- \_ vs](../direct3dhlsl/break-comp---vs.md), [break p-vs](../direct3dhlsl/breakp---vs.md), [if \_ Comp-vs](../direct3dhlsl/if-comp---vs.md), if \_ Comp-vs, if [pred-vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ Max. \_ numTemps                | 32             | Die maximal unterstützte Anzahl von temporären Registern.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ Min. \_ numTemps                | 12             | Die Mindestanzahl der unterstützten temporären Register.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ Max \_ staticflowcontroltiefe  | 4              | Die maximale [Schachtelungs Schachtelung der Schleifen-vs](../direct3dhlsl/loop---vs.md) / [-](../direct3dhlsl/rep---vs.md) und [](../direct3dhlsl/call---vs.md) / [callnz-bool-vs-](../direct3dhlsl/callnz-bool---vs.md) Anweisungen.                                                                                           |
| D3DVS20 \_ Min \_ staticflowcontroltiefe  | 1              | Die minimale Tiefe der [Schachtelung der Schleifen-vs](../direct3dhlsl/loop---vs.md) / [-](../direct3dhlsl/rep---vs.md) und [](../direct3dhlsl/call---vs.md) / [callnz-bool-vs-](../direct3dhlsl/callnz-bool---vs.md) Anweisungen.                                                                                           |



 

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 

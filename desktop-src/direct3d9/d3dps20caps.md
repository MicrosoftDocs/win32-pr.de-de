---
description: Funktionsflags für Pixelshader.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a6da0dfc3fd09ce54e52b633066c6da09660c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127533"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Funktionsflags für Pixelshader.



|                                              |                |                                                                                                                                                                                                                   |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                                     | Wert          | BESCHREIBUNG                                                                                                                                                                                                       |
| D3DD3DPSHADERCAPS2 \_ 0, \_ willkürliche aryswizzle      | (1 << 0) | Willkürliche swizzelnder werden unterstützt.                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions  | (1 << 1) | Farbverlaufs Anweisungen werden unterstützt.                                                                                                                                                                              |
| D3DD3DPSHADERCAPS2 \_ 0- \_ Prädikat           | (1 << 2) | Das Anweisungs Prädikat wird unterstützt. Weitere Informationen finden Sie unter [SETP \_ Comp-PS](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ nodependentleslimit  | (1 << 3) | Es gibt keine Beschränkung für die Anzahl der abhängigen Lesevorgänge pro Anweisung.                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit | (1 << 4) | Es gibt keine Beschränkung für die Anzahl der TeX-Anweisungen.                                                                                                                                                              |
| D3DPS20 \_ Max \_ dynamicflowcontroltiefe        | 24             | Die maximale Schachtelungs Ebene der dynamischen Fluss Steuerungs Anweisungen (Break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ Min \_ dynamicflowcontroltiefe        | 0              | Die minimale Schachtelungs Ebene der dynamischen Fluss Steuerungs Anweisungen (Break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ Max. \_ numTemps                       | 32             | Der Treiber unterstützt höchstens dieses viele temporäre Register.                                                                                                                                                     |
| D3DPS20 \_ Min. \_ numTemps                       | 12             | Der Treiber unterstützt mindestens dieses viele temporäre Register.                                                                                                                                                    |
| D3DPS20 \_ Max \_ staticflowcontroltiefe         | 4              | Die maximale [Schachtelungs Schachtelung der Schleifen-vs](../direct3dhlsl/loop---vs.md) / [-](../direct3dhlsl/rep---vs.md) und [](../direct3dhlsl/call---vs.md) / [callnz-bool-vs-](../direct3dhlsl/callnz-bool---vs.md) Anweisungen. |
| D3DPS20 \_ Min \_ staticflowcontroltiefe         | 1              | Die minimale Tiefe der [Schachtelung der Schleifen-vs](../direct3dhlsl/loop---vs.md) / [-](../direct3dhlsl/rep---vs.md) und [](../direct3dhlsl/call---vs.md) / [callnz-bool-vs-](../direct3dhlsl/callnz-bool---vs.md) Anweisungen. |
| D3DPS20 \_ Max. \_ numinstructionslots            | 512            | Der Treiber unterstützt höchstens diese zahlreichen Anweisungen.                                                                                                                                                           |
| D3DPS20 \_ Min. \_ numinstructionslots            | 96             | Der Treiber unterstützt mindestens diese Anzahl von Anweisungen.                                                                                                                                                          |



 

Diese Konstanten werden vom D3DPSHADERCAPS2 0- \_ Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 

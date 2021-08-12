---
title: bufinfo (sm5 – asm)
description: Fragen Sie die Elementanzahl für einen Puffer ab (jedoch nicht den konstanten Puffer).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a107896973e7457b4bf596843ec77934d95675d50a146190a7f9f40e1c2ce3c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287583"
---
# <a name="bufinfo-sm5---asm"></a>bufinfo (sm5 – asm)

Fragen Sie die Elementanzahl für einen Puffer ab (jedoch nicht den konstanten Puffer).



| bufinfo dest \[ .mask \] , srcResource |
|------------------------------------|



 



| Element                                                                                                               | Beschreibung                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Die Adresse der Ergebnisse.<br/>                                         |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Buffer, mit Ausnahme eines konstanten Puffers, in einem SRV (t \# ) oder UAV (u \# ).<br/> |



 

## <a name="remarks"></a>Hinweise

Alle Komponenten in *dest* erhalten die ganzzahlige Anzahl von Elementen in der Shaderressourcenansicht des Puffers. Die Anzahl der Elemente hängt von den Ansichtsparametern ab, z. B. vom Speicherformat.

Bei einem typisierten Puffer-SRV oder UAV ist der Rückgabewert die Anzahl der Elemente in der Ansicht (wobei ein Element eine Einheit des typisierten Formats ist).

Für einen SRV- oder UAV-Rohpuffer ist der Rückgabewert die Anzahl der Bytes in der Ansicht.

Bei einem strukturierten Puffer-SRV oder UAV ist der Rückgabewert die Anzahl der Strukturen in der Ansicht.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






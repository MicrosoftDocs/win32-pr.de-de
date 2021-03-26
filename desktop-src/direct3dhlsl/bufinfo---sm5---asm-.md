---
title: bufinfo (SM5-ASM)
description: Abfragen der Element Anzahl in einem Puffer (aber nicht im Konstanten Puffer).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993078"
---
# <a name="bufinfo-sm5---asm"></a>bufinfo (SM5-ASM)

Abfragen der Element Anzahl in einem Puffer (aber nicht im Konstanten Puffer).



| bufinfo dest \[ . mask \] , srkresource |
|------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse der Ergebnisse.<br/>                                         |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Puffer, bei dem es sich nicht um einen konstanten Puffer handelt, in einem SRV (t \# ) oder UAV (u \# ).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle-Komponenten in *dest* empfangen die ganzzahlige Anzahl von Elementen in der Shader-Ressourcen Ansicht des Puffers. Die Anzahl der Elemente hängt von den Sicht Parametern (z. b. dem Speicherformat) ab.

Bei einem typisierten Puffer SRV oder UAV ist der Rückgabewert die Anzahl der Elemente in der Sicht (wobei ein Element eine Einheit des typisierten Formats ist).

Bei einem rohpuffer-SRV oder UAV ist der Rückgabewert die Anzahl der Bytes in der Sicht.

Bei einem strukturierten Puffer SRV oder UAV ist der Rückgabewert die Anzahl der Strukturen in der Sicht.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






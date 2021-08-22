---
title: imm_atomic_consume (sm5 – asm)
description: Dekrementieren Sie den ausgeblendeten 32-Bit-Indikator atomisch, der mit einer Unordered Access View (UAV) count oder Append gespeichert ist, und geben Sie den neuen Wert zurück.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0244b885d9d2c46b734994d5e101f79147839d0cf76e2bab5669e52700cf59e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119314"
---
# <a name="imm_atomic_consume-sm5---asm"></a>imm \_ atomic \_ consume (sm5 – asm)

Dekrementieren Sie den ausgeblendeten 32-Bit-Indikator atomisch, der mit einer Unordered Access View (UAV) count oder Append gespeichert ist, und geben Sie den neuen Wert zurück.



| imm \_ atomic \_ consume dst0 \[ .single component mask , \_ \_ \] dstUAV |
|---------------------------------------------------------------|



 



| Element                                                                                           | Beschreibung                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[in \] Enthält den zurückgegebenen ursprünglichen Indikatorwert.<br/>           |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[in \] Einem strukturierten Puffer-UAV mit dem Count- oder Append-Flag. <br/> |



 

## <a name="remarks"></a>Hinweise

Unter [imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) finden Sie eine Erläuterung der Gültigkeit des zurückgegebenen Count-Werts, je nachdem, ob der UAV Count oder Append ist. Dasselbe gilt für **imm \_ atomic \_ consume**.

**imm \_ atomic \_ consume** führt eine atomische Dekrementierung des Indikatorwerts aus und gibt den neuen Wert an *dst0* zurück.

Es gibt keine Klammer der Anzahl, sodass sie sich nach Unterlauf umschließt.

Der gleiche Shader kann nicht versuchen, sowohl **imm \_ atomic \_ alloc** als auch imm atomic consume auf demselben UAV zu **\_ \_ nutzen.** Darüber hinaus kann die GPU nicht zulassen, dass mehrere Shaderaufrufe **imm \_ atomic \_ alloc** und **imm \_ atomic \_ consume** auf demselben UAV kombinieren.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt diese Anweisung für alle Shaderstufen für die Direct3D 11.1-Runtime, die ab Windows 8 verfügbar ist.



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






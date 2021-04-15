---
title: imm_atomic_consume (SM5-ASM)
description: Verringert den ausgeblendeten 32-Bit-Leistungs Zähler atomisch, der mit einer Anzahl oder angefügenter Zugriffs Ansicht (UAV) gespeichert wird, und gibt den neuen Wert zurück.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993127"
---
# <a name="imm_atomic_consume-sm5---asm"></a>imm \_ Atomic \_ -Verbrauch (SM5-ASM)

Verringert den ausgeblendeten 32-Bit-Leistungs Zähler atomisch, der mit einer Anzahl oder angefügenter Zugriffs Ansicht (UAV) gespeichert wird, und gibt den neuen Wert zurück.



| "imm \_ Atomic" \_ dst0 \[ . \_ einzelkomponentenmaske \_ \] , dstuav |
|---------------------------------------------------------------|



 



| Element                                                                                           | BESCHREIBUNG                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[in \] enthält den zurückgegebenen ursprünglichen Leistungs Zählers.<br/>           |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*<br/> | \[in \] einem strukturierten Puffer-UAV mit dem count-oder Append-Flag. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Eine Erläuterung zur Gültigkeit des zurückgegebenen zählungs Werts finden Sie unter " [imm \_ Atomic \_ zuordnungszahl](imm-atomic-alloc--sm5---asm-.md) ", je nachdem, ob die UAV "count" oder "append" ist Das gleiche gilt für **den \_ atomischen Atomic- \_ Verbrauch**.

der unteilbare Wert für " **imm \_ Atomic \_** " führt einen atomaren Dekrement des Leistungs Zählers durch und gibt den neuen Wert an *dst0* zurück.

Es gibt keine Klammer für die Anzahl, daher wird Sie bei einem Unterlauf umschlossen.

Der gleiche Shader kann nicht gleichzeitig sowohl einen " **imm \_ Atomic- \_ Zuweisungen** " als auch einen " **imm Atomic"- \_ \_ Verbrauch** auf derselben UAV Darüber hinaus kann die GPU nicht mehrere shaderaufrufe zulassen, um die Verwendung von " **imm \_ Atomic \_ zugc** " und " **imm \_ Atomic \_** " in derselben UAV zu mischen.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.



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

 

 






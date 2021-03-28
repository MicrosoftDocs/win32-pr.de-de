---
title: dcl_function_body (SM5-ASM)
description: Deklarieren Sie einen Funktions Text.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101114"
---
# <a name="dcl_function_body-sm5---asm"></a>DCL \_ \_ -Funktions Text (SM5-ASM)

Deklarieren Sie einen Funktions Text.



| DCL- \_ Funktions \_ Text FB\# |
|--------------------------|



 



| Element                                                          | BESCHREIBUNG                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*ÖFB\#*<br/> | \[in \] der Bezeichnung des Speicher Orts, an dem die Funktion angezeigt wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung deklariert einen eindeutigen Funktions Text, dessen Code später im Programm bei der Bezeichnung FB angezeigt wird \# .

Funktions Texte werden in Funktionstabellen Deklarationen verwendet. Weitere Informationen finden Sie unter [DCL \_ Function \_ Table](dcl-function-table---sm5---asm-.md).

Im Rumpf-Shader und im Domänen-Shader, in dem mehrere Phasen vorhanden sind (Steuerungspunkt Phase, Verzweigungs Phase und joinphase), werden alle Funktions Texte (Bezeichnung FB \# ) nach allen Phasen angezeigt, anstatt nach Phasen gruppiert zu werden.

Es gibt keine Beschränkung, wie viele funktionskörper vorhanden sein können.

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

 

 






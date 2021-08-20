---
title: dmov (sm5 - asm)
description: Komponentenweises Verschieben. | dmov (sm5 - asm)
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21207ef46bde6a7ab34633bb40df69457a7282f1805fb604738300e8bd330cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118091537"
---
# <a name="dmov-sm5---asm"></a>dmov (sm5 - asm)

Komponentenweises Verschieben.



| dmov \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|-------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Move-Ziel. *dest*  =  *src0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die zu verschobenen Komponenten.<br/>            |



 

## <a name="remarks"></a>Hinweise

Bei den Modifizierern, die nicht swizzle sind, wird davon ausgegangen, dass es sich bei den Daten um Gleitkommadaten handelt. Das Fehlen von Modifizierern verschiebt Daten, ohne Bits zu ändern.

Die gültigen Swizzles für die Quellparameter sind .xyzw, .xyxy, .zwxy, .zwzw. Die folgenden *src-Zuordnungen* sind post swizzle:

-   *src0* ist ein double vec2 über (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).
-   *src1* ist ein double-vec2 zwischen (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

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

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






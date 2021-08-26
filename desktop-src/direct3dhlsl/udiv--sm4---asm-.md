---
title: udiv (sm4 - asm)
description: Division einer ganzen Zahl ohne Vorzeichen.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b1320d0518034129efe2222a42aa2694df0422db524da0714377cb43a2b9a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948980"
---
# <a name="udiv-sm4---asm"></a>udiv (sm4 - asm)

Division einer ganzen Zahl ohne Vorzeichen.



| udiv destQUOT \[ .mask \] , destREM \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|------------------------------------------------------------------------------|



 



| Element                                                                                                   | BESCHREIBUNG                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*<br/> | \[in \] Die Adresse des resultierenden Quotienten.<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*<br/>     | \[in \] Die Adresse des resultierenden Rests.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[in \] Die Komponenten, die durch *src1 geteilt werden sollen.*<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                        | \[in \] The components by whch to divide *src0*.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine komponentenweise Unterteilung des 32-Bit-Operanden *src0* durch den 32-Bit-Operanden *src1 aus.* Die Ergebnisse der Divisionen sind die 32-Bit-Quotienten, die in *destQUOT* platziert werden, und die 32-Bit-Reste, die in *destREM platziert werden.*

Division durch 0 gibt 0xffffffff für Quotient und Rest zurück.

Sie können entweder *destQUOT* oder *destREM* als NULL angeben, anstatt ein Register anzugeben, wenn der Quotient oder Rest nicht benötigt wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






---
title: xor (sm4 - asm)
description: Bitweises xor.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a4dae86a4c6ade427b749c2bb72974564b8a4b7a6baae6821edb3c0d63b2164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892410"
---
# <a name="xor-sm4---asm"></a>xor (sm4 - asm)

Bitweises xor.



| xor dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|-------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Ergebnis des Vorgangs.<br/>       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in The components to XOR with src1 ( Die Komponenten \] zu XOR mit *src1*).<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] The components to XOR with *src0*.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt ein komponentenweises logisches XOR jedes Paars von 32-Bit-Werten aus *src0* und *src1 aus.* 32-Bit-Ergebnisse werden in *dest platziert.*

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

 

 






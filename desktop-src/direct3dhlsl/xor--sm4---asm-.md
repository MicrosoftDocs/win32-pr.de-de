---
title: XOR (SM4-ASM)
description: Bitweises XOR.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389494"
---
# <a name="xor-sm4---asm"></a>XOR (SM4-ASM)

Bitweises XOR.



| XOR dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\] |
|-------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[im \] Ergebnis des Vorgangs.<br/>       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten zu XOR mit *Quelle1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den Komponenten zu XOR mit *src0*.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt ein Komponenten weises logisches XOR für jedes Paar von 32-Bit-Werten aus *src0* und *Quelle1* aus. 32-Bit-Ergebnisse werden in *dest* platziert.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






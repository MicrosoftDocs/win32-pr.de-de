---
title: oder (sm4 – asm)
description: Bitweises oder .
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a65d6ee2c5e5559d7d5e877a2bdef83b13a45a06ca0f00c980baa4811579f03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088743"
---
# <a name="or-sm4---asm"></a>oder (sm4 – asm)

Bitweises oder .



| oder dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|------------------------------------------------------|



 



| Element                                                            | Beschreibung                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Ergebnis des Vorgangs.<br/>      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten in OR mit *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Komponenten in OR mit *src0*.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt ein komponentenweises logisches OR jedes Paars von 32-Bit-Werten aus *src0* und *src1 aus.* Die 32-Bit-Ergebnisse werden in *dest platziert.*

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

 

 






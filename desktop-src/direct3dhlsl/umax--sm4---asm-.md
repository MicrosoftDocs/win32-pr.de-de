---
title: umax (sm4 - asm)
description: Komponentenweises Ganzzahl-Maximum ohne Vorzeichen.
ms.assetid: 86BCF7A7-99CA-481B-82B4-E0BA30963344
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac89ee5d9966e27b463b595c6d7ba105e22be6499fa69265989c39c2add50bd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484520"
---
# <a name="umax-sm4---asm"></a>umax (sm4 - asm)

Komponentenweises Ganzzahl-Maximum ohne Vorzeichen.



| umax dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle \] , |
|---------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> *dest*  =  *src0*  >  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der wert, der mit *src1 verglichen werden soll.*<br/>                                                                      |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der wert, der mit *src0 verglichen werden soll.*<br/>                                                                      |



 

## <a name="remarks"></a>Hinweise

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

 

 






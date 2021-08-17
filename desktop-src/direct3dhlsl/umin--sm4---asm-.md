---
title: umin (sm4 - asm)
description: Komponentenweise ganzzahlige Ganzzahl ohne Vorzeichen.
ms.assetid: 134B128F-7B47-4819-A576-80766EDB14C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dea32d1be6fd3d6fa63b04c52d004e16dc8c27250fb3a703fc46af64fac5d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722013"
---
# <a name="umin-sm4---asm"></a>umin (sm4 - asm)

Komponentenweise ganzzahlige Ganzzahl ohne Vorzeichen.



| umin dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle \] , |
|---------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> *dest*  =  *src0*  <  *src1* ? *src0* : *src1*<br/> |
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

 

 






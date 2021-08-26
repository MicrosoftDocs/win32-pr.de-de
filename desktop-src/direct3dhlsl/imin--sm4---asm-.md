---
title: imin (sm4 - asm)
description: Komponentenweise ganzzahliger Mindestwert.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0188b23700393034ad2187636d8d5bf846b8b8523b5336699443475c094fd26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982390"
---
# <a name="imin-sm4---asm"></a>imin (sm4 - asm)

Komponentenweise ganzzahliger Mindestwert.



| imin dest \[ .mask \] , \[  - \] src0 \[ .swizzle \] , \[ - \] src1 \[ .swizzle \] , |
|--------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Ergebnis des Vorgangs.<br/> *dest*  =  *src0*  <  *src1* ? *src0* : *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der wert, der mit *src1 verglichen werden soll.*<br/>                                                       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der wert, der mit *src0 verglichen werden soll.*<br/>                                                       |



 

## <a name="remarks"></a>Hinweise

Der optionale Negatmodifizierer für Quelloperatoren nimmt vor dem Ausführen des Vorgangs ein Komplement von 2 an.

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

 

 






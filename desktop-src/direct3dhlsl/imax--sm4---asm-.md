---
title: imax (sm4 - asm)
description: Komponentenweises Ganzzahl-Maximum.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da254802d32b936724e11cf947baf91c205a0d9f61754c2e142a1380166640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672860"
---
# <a name="imax-sm4---asm"></a>imax (sm4 - asm)

Komponentenweises Ganzzahl-Maximum.



| imax dest \[ .mask \] , \[  - \] src0 \[ .swizzle \] , \[ - \] src1 \[ .swizzle \] , |
|--------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Ergebnis des Vorgangs.<br/> *dest*  =  *src0*  >  *src1* ? *src0* : *src1*<br/> |
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

 

 






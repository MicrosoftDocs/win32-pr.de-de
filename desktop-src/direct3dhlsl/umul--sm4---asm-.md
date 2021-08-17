---
title: umul (sm4 - asm)
description: Ganze Zahl ohne Vorzeichen multipliziert.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec63b3a95ffbdf1f71142c9fc508e21e718b44d988b725dad5d73775746871c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721834"
---
# <a name="umul-sm4---asm"></a>umul (sm4 - asm)

Ganze Zahl ohne Vorzeichen multipliziert.



| umul destHI \[ .mask \] , destLO \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|---------------------------------------------------------------------------|



 



| Element                                                                                           | Beschreibung                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[in \] Die hohen 32 Bits des Ergebnisses pro Komponente.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[in \] Die unteren 32 Bits des Ergebnisses pro Komponente.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[in \] Die Komponenten, mit denen *src1 multipliziert werden soll.*<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[in \] Die Komponenten, mit denen *src0 multipliziert werden soll.*<br/>    |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine komponentenweise Multiplikation der 32-Bit-Operanden *src0* und *src1* ohne Vorzeichen aus und erzeugt das richtige vollständige 64-Bit-Ergebnis pro Komponente. Die niedrigen 32 Bits pro Komponente werden in *destLO platziert.* Die hohen 32 Bits pro Komponente werden in *destHI platziert.*

Sie können entweder *destHI* oder *destLO* als NULL angeben, anstatt ein Register anzugeben, wenn die hohen oder niedrigen 32 Bits des 64-Bit-Ergebnisses nicht benötigt werden.

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

 

 






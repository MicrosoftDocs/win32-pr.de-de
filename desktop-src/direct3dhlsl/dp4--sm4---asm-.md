---
title: dp4 (sm4 - asm)
description: 4-dimensionaler Vektor punktprodukt der Komponenten rgba, POS-Swizzle.
ms.assetid: A41EC054-0060-49CA-90FB-A096E63DD27D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 742bf3c736d6769a70bf9dd792e453cc5977e9eb494206b5c110d10b01b60350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726670"
---
# <a name="dp4-sm4---asm"></a>dp4 (sm4 - asm)

4-dimensionaler Vektor punktprodukt der Komponenten rgba, POS-Swizzle.



| dp4 \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Ergebnis des Vorgangs. <br/> *dest*  =  *src0.r* \* *src1.r*  +  *src0.g* \* *src1.g*  +  *src0.b* \* *src1.b* +  *src0.a* \* *src1.a*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten in der -Funktion.<br/>                                                                                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Komponenten in der -Funktion.<br/>                                                                                                          |



 

## <a name="remarks"></a>Hinweise

Skalares Ergebnis, das in der Schreibmaske in Komponenten repliziert wird.

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

 

 






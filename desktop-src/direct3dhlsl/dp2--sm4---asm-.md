---
title: DP2 (SM4-ASM)
description: 2-dimensionaler Vektor Punkt-Produkt der Komponenten RG, POS-Swizzle.
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389511"
---
# <a name="dp2-sm4---asm"></a>DP2 (SM4-ASM)

2-dimensionaler Vektor Punkt-Produkt der Komponenten RG, POS-Swizzle.



| DP2 \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses. <br/> *dest*  =  *src0. r* \* *Quelle1. r*  +  *src0. g* \* *Quelle1. g*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten des Vorgangs.<br/>                                                                             |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den Komponenten des Vorgangs.<br/>                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Das skalare Ergebnis wurde in den Komponenten in der Schreib Maske repliziert.

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

 

 






---
title: eq (sm4 - asm)
description: Komponentenweiser Vektor-Gleitkommagleichheitsvergleich.
ms.assetid: 925578E4-0161-45A9-840F-14AA65FF4F33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a90af3fd6f65a6a81c32592650c4be33996c96a1d99415ec1dfecb0b0f83ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789040"
---
# <a name="eq-sm4---asm"></a>eq (sm4 - asm)

Komponentenweiser Vektor-Gleitkommagleichheitsvergleich.



| eq dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle\] |
|----------------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponente, die für *src1 verwendet werden soll.*<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Komponente, die für *src0 verwendet werden soll.*<br/>         |



 

## <a name="remarks"></a>Hinweise

Führt den Float-Vergleich (*src0*  ==  *src1*) für jede Komponente aus und schreibt das Ergebnis in *dest.*

Wenn der Vergleich true ist, 0xFFFFFFFF für diese Komponente zurückgegeben. Andernfalls 0x0000000 zurückgegeben.

Denormale werden vor dem Vergleich geleert (ursprüngliche Quellregister unverändert). +0 ist gleich -0. Der Vergleich mit NaN gibt false zurück.

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

 

 






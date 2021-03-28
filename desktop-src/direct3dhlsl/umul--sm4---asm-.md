---
title: Umul (SM4-ASM)
description: Ganzzahl ohne Vorzeichen multiplizieren.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389534"
---
# <a name="umul-sm4---asm"></a>Umul (SM4-ASM)

Ganzzahl ohne Vorzeichen multiplizieren.



| Umul desthi \[ . mask \] , destlo \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\] |
|---------------------------------------------------------------------------|



 



| Element                                                                                           | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*desthi*<br/> | \[in \] den hohen 32 Bits des Ergebnisses pro Komponente.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destlo*<br/> | \[in \] den unteren 32 Bits des Ergebnisses pro Komponente.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[in \] den Komponenten, nach denen *Quelle1* multipliziert werden soll.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/>                                | \[in \] den Komponenten, nach denen *src0* multipliziert werden soll.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine Komponenten Weise Multiplikation von nicht signierten 32-Bit-Operanden *src0* und *Quelle1* aus und erzeugt das korrekte vollständige 64-Bit-Ergebnis pro Komponente. Die unteren 32 Bits pro Komponente werden in " *destlo*" platziert. Die hohen 32 Bits pro Komponente werden in *desthi* platziert.

Sie können entweder *desthi* oder *destlo* als NULL angeben, anstatt ein Register anzugeben, wenn die hohen oder unteren 32 Bits des 64-Bit-Ergebnisses nicht benötigt werden.

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

 

 






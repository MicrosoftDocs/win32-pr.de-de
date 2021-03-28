---
title: udiv (SM4-ASM)
description: Unterteilung ohne Vorzeichen.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389536"
---
# <a name="udiv-sm4---asm"></a>udiv (SM4-ASM)

Unterteilung ohne Vorzeichen.



| udiv destquot \[ . mask \] , de Strem \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\] |
|------------------------------------------------------------------------------|



 



| Element                                                                                                   | BESCHREIBUNG                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destquot*<br/> | \[in \] der Adresse des resultierenden Quotienten.<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*"Debug"*<br/>     | \[in \] der Adresse des resultierenden Restwerts.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[in \] den Komponenten, die durch *Quelle1* dividiert werden sollen.<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/>                                        | \[in \] den Komponenten by welche to Divide *src0*.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine Komponenten Weise unsignierte Teilung des 32-Bit-Operanden *src0* durch den 32-Bit-Operanden *Quelle1* aus. Die Ergebnisse der Teilungen sind die 32-Bit-Quotienten in " *destquot* " und 32-Bit-Rest-Werten, die in " *de Strem*" platziert werden.

Division durch Null gibt 0xFFFFFFFF für den Quotienten und den Rest zurück.

Sie können entweder *destquot* oder *Destrem* als NULL angeben, anstatt ein Register anzugeben, wenn der Quotienten oder Rest nicht benötigt wird.

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

 

 






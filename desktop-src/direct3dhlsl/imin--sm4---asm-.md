---
title: Imin (SM4-ASM)
description: Die minimale Komponenten Weise Ganzzahl.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942384e7a988e4919a483e09c75e476d5a6917ba
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389569"
---
# <a name="imin-sm4---asm"></a>Imin (SM4-ASM)

Die minimale Komponenten Weise Ganzzahl.



| Imin dest \[ . mask \] , \[  - \] src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ . Swizzle \] , |
|--------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[im \] Ergebnis des Vorgangs.<br/> *dest*  =  *src0*  <  *Quelle1* ? *src0* : *Quelle1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[im \] Wert, der mit *Quelle1* verglichen werden soll.<br/>                                                       |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[im \] Wert, der mit *src0* verglichen werden soll.<br/>                                                       |



 

## <a name="remarks"></a>Bemerkungen

Der optionale Negation-Modifizierer für Quell Operanden nimmt die Ergänzung von 2 vor dem Ausführen des Vorgangs an.

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

 

 






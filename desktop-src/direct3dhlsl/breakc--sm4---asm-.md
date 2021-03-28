---
title: breakc (SM4-ASM)
description: Verschiebt den Ausführungs Punkt bedingt an die Anweisung nach der nächsten endschleife oder Endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389550"
---
# <a name="breakc-sm4---asm"></a>breakc (SM4-ASM)

Verschiebt den Ausführungs Punkt bedingt an die Anweisung nach der nächsten [endschleife](endloop--sm4---asm-.md) oder [Endswitch](endswitch--sm4---asm-.md).



| breakc { \_ z \|\_NZ} src0. Select- \_ Komponente |
|------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Komponente, für die die Bedingung getestet werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das tokenformat enthält den Offset der entsprechenden **ENDLOOP** -Anweisung im Shader.

Im folgenden Beispiel wird die **breakc** -Anweisung gezeigt.


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



Diese Anweisung muss in einer **Schleifen** / **endschleife** oder **Switch**- / **Endswitch** vorkommen.

Das 32-Bit-Register, das von *src0* bereitgestellt wird, wird auf einer Bitebene getestet. Wenn ein Bit ungleich 0 (null) ist, führt **breakc \_ NZ** die Unterbrechung aus. Wenn alle Bits NULL sind, führt **breakc \_ z** die Unterbrechung aus.

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

 

 






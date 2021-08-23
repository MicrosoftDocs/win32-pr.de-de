---
title: breakc (sm4 - asm)
description: Verschiebt den Ausführungspunkt bedingt in die Anweisung nach dem nächsten Endloop oder endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eff9be2428db0d0df24879f50964ce14f6831e235c54655958d9401224d7225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626470"
---
# <a name="breakc-sm4---asm"></a>breakc (sm4 - asm)

Verschiebt den Ausführungspunkt bedingt in die -Anweisung nach dem nächsten [Endloop](endloop--sm4---asm-.md) oder [endswitch](endswitch--sm4---asm-.md).



| breakc{ \_ z\|\_nz} src0.select-Komponente \_ |
|------------------------------------------|



 



| Element                                                            | Beschreibung                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponente, für die die Bedingung zu testen ist.<br/> |



 

## <a name="remarks"></a>Hinweise

Das Tokenformat enthält der Einfachheit halber den Offset der entsprechenden **Endloopanweisung** im Shader.

Das folgende Beispiel zeigt die **Breakc-Anweisung.**


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



Diese Anweisung muss in einer **Schleifenendschleife** / **oder** einem **Switch** / **endswitch angezeigt werden.**

Das von *src0* bereitgestellte 32-Bit-Register wird auf Bitebene getestet. Wenn ein Bit ungleich 0 (null) ist, führt **breakc \_ nz** die Unterbrechung aus. Wenn alle Bits 0 (null) sind, führt **breakc \_ z** die Unterbrechung aus.

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

 

 






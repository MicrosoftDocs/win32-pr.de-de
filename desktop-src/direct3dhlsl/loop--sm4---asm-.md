---
title: Schleife (SM4-ASM)
description: Gibt eine Schleife an, die bis zu einer Break-Anweisung iteriert.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993103"
---
# <a name="loop-sm4---asm"></a>Schleife (SM4-ASM)

Gibt eine Schleife an, die bis zu einer Break-Anweisung iteriert.



| loop |
|------|



 

## <a name="remarks"></a>Bemerkungen

die **Schleife** kann unbegrenzt durchlaufen werden, obwohl die allgemeine Ausführung des Shaders erzwungen werden kann, nachdem eine Reihe von Anweisungen ausgeführt wurden.

Fluss Kontroll Blöcke können bis zu 64 tief pro Unterroutine und Main verschachteln. Der HLSL-Compiler generiert keine Unterroutinen, die diesen Grenzwert überschreiten. Das Verhalten von Ablauf Steuerungs Anweisungen, die eine Tiefe von 64 Ebenen überschreiten, ist nicht definiert.

Das tokenformat enthält den Offset der entsprechenden [ENDLOOP](endloop--sm4---asm-.md) -Anweisung im Shader.

Im folgenden Beispiel wird gezeigt, wie die-Schleifen Anweisung verwendet wird.

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

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

 

 





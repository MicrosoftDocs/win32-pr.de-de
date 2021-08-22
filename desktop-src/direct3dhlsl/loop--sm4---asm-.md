---
title: loop (sm4 - asm)
description: Gibt eine Schleife an, die iteriert, bis eine Breakanweisung gefunden wird.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dfc3090e71c1101e2c2748924de24f5443363ede76b86130cf63c3a319c76ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043768"
---
# <a name="loop-sm4---asm"></a>loop (sm4 - asm)

Gibt eine Schleife an, die iteriert, bis eine Breakanweisung gefunden wird.



| loop |
|------|



 

## <a name="remarks"></a>Hinweise

**-Schleife** kann unbegrenzt iterieren, obwohl die gesamte Ausführung des Shaders möglicherweise gezwungen wird, zu beenden, nachdem einige Anweisungen ausgeführt wurden.

Flow Steuerblöcke können bis zu 64 Tiefe pro Unterroutine und Main schachteln. Der HLSL-Compiler generiert keine Unterroutinen, die diesen Grenzwert überschreiten. Das Verhalten von Ablaufsteuerungsanweisungen über 64 Ebenen hinaus pro Unterroutine ist nicht definiert.

Das Tokenformat enthält der Einfachheit halber den Offset der entsprechenden [Endloopanweisung](endloop--sm4---asm-.md) im Shader.

Im folgenden Beispiel wird die Verwendung der Schleifenanweisung veranschaulicht.

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

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

 

 





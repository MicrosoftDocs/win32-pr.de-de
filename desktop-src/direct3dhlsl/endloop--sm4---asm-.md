---
title: endloop (sm4 - asm)
description: Beendet eine Schleifen-Anweisung.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c266ea3dc4a4b1feba1264c20f31eb85e910ad6d69e63a42832ee9bb88082c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119504"
---
# <a name="endloop-sm4---asm"></a>endloop (sm4 - asm)

Beendet eine Schleifen-Anweisung.



| endloop |
|---------|



 

## <a name="remarks"></a>Hinweise

Im folgenden Beispiel wird die Verwendung dieser Anweisung veranschaulicht.

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

Das Tokenformat enthält der Einfachheit halber den Offset der entsprechenden Schleifenanweisung im Shader.

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

 

 





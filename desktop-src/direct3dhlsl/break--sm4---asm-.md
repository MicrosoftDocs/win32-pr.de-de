---
title: break (sm4 - asm)
description: Verschiebt den Ausführungspunkt nach dem nächsten endloop- oder endswitch-Befehl in die Anweisung.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17ca99b0e16da016145f7f23fe6e4ce6bd410325ff98d4c6dd1387943fbc718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983340"
---
# <a name="break-sm4---asm"></a>break (sm4 - asm)

Verschiebt den Ausführungspunkt nach dem nächsten [endloop-](endloop--sm4---asm-.md) oder [endswitch-Befehl](endswitch--sm4---asm-.md)in die Anweisung.



| break |
|-------|



 

## <a name="remarks"></a>Hinweise

Das Tokenformat enthält zur Vereinfachung den Offset der entsprechenden **endloop-** oder **endswitch-Anweisung** im Shader.

Das folgende Beispiel zeigt die **Break-Anweisung.**


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



Diese Anweisung muss in einem **Schleifenendloop** /  oder in einem **Fall** in einem **Switch** / **endswitch** angezeigt werden.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

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

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





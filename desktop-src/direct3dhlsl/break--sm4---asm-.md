---
title: Break (SM4-ASM)
description: Verschiebt den Ausführungs Punkt in die Anweisung nach der nächsten endschleife oder Endswitch.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313662"
---
# <a name="break-sm4---asm"></a>Break (SM4-ASM)

Verschiebt den Ausführungs Punkt in die Anweisung nach der nächsten [endschleife](endloop--sm4---asm-.md) oder [Endswitch](endswitch--sm4---asm-.md).



| break |
|-------|



 

## <a name="remarks"></a>Bemerkungen

Das tokenformat enthält den Offset der entsprechenden **ENDLOOP** -oder **Endswitch** -Anweisung im Shader.

Im folgenden Beispiel wird die **break** -Anweisung gezeigt.


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



Diese Anweisung muss innerhalb einer **Schleifen** / **endschleife** oder in einem **Fall** in einem **Switch**- / **Endswitch** vorkommen.

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

 

 





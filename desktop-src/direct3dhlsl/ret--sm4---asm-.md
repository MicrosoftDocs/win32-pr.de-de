---
title: ret (sm4 - asm)
description: Return-Anweisung.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7482c2c7351944824e2590f5c87dac63bde8f639a5ad42dffdfc71e4134603b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853750"
---
# <a name="ret-sm4---asm"></a>ret (sm4 - asm)

Return-Anweisung.



| Ret |
|-----|



 

## <a name="remarks"></a>Hinweise

Wenn sie sich innerhalb einer Unterroutine befindet, kehren Sie nach dem Aufruf zur Anweisung zurück. Wenn sie sich nicht in einer Unterroutine befindet, beenden Sie die Programmausführung.

Im folgenden Beispiel wird die Verwendung dieser Anweisung veranschaulicht.

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a>Beschränkungen

-   **ret** kann beliebig oft an einer beliebigen Stelle in einem Programm angezeigt werden.
-   Wenn [](label--sm4---asm-.md) eine Bezeichnungsanweisung in einem Shader angezeigt wird, muss ihr ein **ret-Befehl** vorangestellt werden, der in keiner Flusssteuerungsanweisungen geschachtelt ist.
-   Wenn in einem Shader Unterroutinen vorhanden sind, muss die letzte Anweisung im Shader ein **ret** sein.

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

 

 





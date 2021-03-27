---
title: ret (SM4-ASM)
description: Return-Anweisung.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719380"
---
# <a name="ret-sm4---asm"></a>ret (SM4-ASM)

Return-Anweisung.



| TZI |
|-----|



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie in einer Unterroutine sind, kehren Sie nach dem-Befehl zur Anweisung zurück. Wenn nicht innerhalb einer Unterroutine, beenden Sie die Ausführung des Programms.

Das folgende Beispiel zeigt die Verwendung dieser Anweisung.

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

-   **ret** kann beliebig oft in einem Programm vorkommen.
-   Wenn eine [Bezeichnungs Anweisung in](label--sm4---asm-.md) einem Shader vorkommt, muss Ihr ein **ret** -Befehl vorangestellt sein, der in keiner der Fluss Steuerungs Anweisungen enthalten ist.
-   Wenn sich Unterroutinen in einem Shader befinden, muss die letzte Anweisung im Shader ein **ret** sein.

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

 

 





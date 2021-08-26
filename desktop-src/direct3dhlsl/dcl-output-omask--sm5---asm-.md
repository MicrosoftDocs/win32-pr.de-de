---
title: dcl_output oMask (sm5 - asm)
description: Deklarieren Sie ein Ausgaberegister, das vom Shader geschrieben werden soll.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a6860904b557bc21a5202bbfd60105852adc260580457afb02b4fe6d92352b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068510"
---
# <a name="dcl_output-omask-sm5---asm"></a>dcl \_ output oMask (sm5 - asm)

Deklarieren Sie ein Ausgaberegister, das vom Shader geschrieben werden soll.



| dcl \_ output o \# \[ .mask\] |
|--------------------------|



 



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="o"></span><span id="O"></span>*O*<br/> | \[in \] Das Ausgaberegister.<br/> |



 

## <a name="remarks"></a>Hinweise


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a>Beschränkungen

-   Die Komponentenmaske kann eine beliebige Teilmenge von \[ xyzw \] sein. Durch das Verlassen von Lücken zwischen Komponenten wird jedoch Platz verschwendet.
-   Es ist gesetzlich, eine Obermenge der Komponentenmaske zu deklarieren, die für die Eingabe in der nächsten Phase deklariert wird. Sich gegenseitig ausschließende Masken sind jedoch nicht zulässig. Der Vertex-Shader, der o3.xy ausausgabet, bedeutet, dass der Pixel-Shader, der v3.z einträgt, ungültig ist, die Eingabe von v3.x oder v3.y oder v3.xy jedoch gültig ist.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     |         |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






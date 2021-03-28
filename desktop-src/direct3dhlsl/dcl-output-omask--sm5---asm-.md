---
title: dcl_output omask (SM5-ASM)
description: Deklarieren Sie ein Ausgabe Register, das vom Shader geschrieben werden soll.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389597"
---
# <a name="dcl_output-omask-sm5---asm"></a>DCL- \_ Ausgabe-omask (SM5-ASM)

Deklarieren Sie ein Ausgabe Register, das vom Shader geschrieben werden soll.



| DCL- \_ Ausgabe o \# \[ . Mask\] |
|--------------------------|



 



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="o"></span><span id="O"></span>*'*<br/> | \[im \] Ausgabe Register.<br/> |



 

## <a name="remarks"></a>Bemerkungen


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a>Beschränkungen

-   Die Komponenten Maske kann eine beliebige Teilmenge von \[ xyzw sein \] . Lücken zwischen den Komponenten zu belassen, verschwendet jedoch Speicherplatz.
-   Es ist zulässig, eine in der nächsten Phase für die Eingabe deklarierte übergeordnete Komponente der Komponenten Maske zu deklarieren. Sich gegenseitig ausschließende Masken sind jedoch nicht zulässig. Der Vertex-Shader gibt "O3. XY" aus, d. h., der Pixelshader, der "v3. z" ist, ist ungültig, aber die Eingabe von "v3. x", "v3. y" oder "v3.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     |         |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






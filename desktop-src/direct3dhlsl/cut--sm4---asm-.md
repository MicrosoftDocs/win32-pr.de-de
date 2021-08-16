---
title: cut (sm4 - asm)
description: Geometry Shader-Anweisung, die die aktuelle primitive Topologie abvervollständigen (wenn Scheitelungen ausgegeben wurden) und eine neue Topologie des Typs startet, der vom Geometry Shader deklariert wird.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34357c05cdd9506ec480d5021db5b330971de9fce7fd70ce9909658be9bb8c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908824"
---
# <a name="cut-sm4---asm"></a>cut (sm4 - asm)

Geometry Shader-Anweisung, die die aktuelle primitive Topologie abvervollständigen (wenn Scheitelungen ausgegeben wurden) und eine neue Topologie des Typs startet, der vom Geometry Shader deklariert wird.



| Schneiden |
|-----|



 

## <a name="remarks"></a>Hinweise

Wenn **ausschneiden** ausgeführt wird, geschieht zunächst, dass alle zuvor vom Geometry Shader-Aufruf ausgegebenen Topologien abgeschlossen sind. Wenn nicht genügend Scheitelungen für die vorherige primitive Topologie ausgegeben wurden, werden sie verworfen. Da die einzigen verfügbaren Ausgabetopologien für den Geometry-Shader Pointlist, Linestrip und Trianglestrip sind, gibt es beim Ausschneiden nie linke **Vertices.**

Wenn die vorherige Topologie abgeschlossen ist,  wird beim Ausschneiden eine neue Topologie mit der Topologie begonnen, die als Ausgabe des Geometrie-Shaders deklariert ist.

## <a name="restrictions"></a>Beschränkungen

-   Die **Cut-Anweisung** gilt nur für den Geometry Shader.
-   **cut** kann im Geometrie-Shader eine beliebige Anzahl von Malen angezeigt werden, auch innerhalb der Flusssteuerung.
-   Wenn der Geometrie-Shader endet und Scheitelungen ausgegeben wurden, wird die Topologie, die sie erstellen, abgeschlossen, als ob ein Ausschneiden als letzte Anweisung ausgeführt wurde. 
-   Wenn Streams deklariert wurden, muss [der \_ Ausschneidedatenstrom](cut-stream---sm5---asm-.md) anstelle von **ausgeschnitten werden.**

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





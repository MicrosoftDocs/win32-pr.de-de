---
title: Ausschneiden (SM4-ASM)
description: Geometry-shaderanweisung, die die aktuelle primitive Topologie (wenn beliebige Scheitel Punkte ausgegeben wurden) vervollständigt und eine neue Topologie des vom Geometry-Shader deklarierten Typs startet.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976328"
---
# <a name="cut-sm4---asm"></a>Ausschneiden (SM4-ASM)

Geometry-shaderanweisung, die die aktuelle primitive Topologie (wenn beliebige Scheitel Punkte ausgegeben wurden) vervollständigt und eine neue Topologie des vom Geometry-Shader deklarierten Typs startet.



| cut |
|-----|



 

## <a name="remarks"></a>Bemerkungen

Wenn **Ausschneiden** ausgeführt wird, ist das erste, dass jede zuvor ausgegebene Topologie durch den Geometry-Shader-Aufruf abgeschlossen ist. Wenn nicht genügend Scheitel Punkte für die vorherige primitive Topologie ausgegeben wurden, werden Sie verworfen. Da die einzigen verfügbaren ausgabetopologien für den Geometry-Shader "PointList", "linestrip" und "Trianglestrip" sind, gibt es keine übrig gebliebenen Scheitel Punkte beim **Ausschneiden**.

Wenn die vorherige Topologie (sofern vorhanden) abgeschlossen ist, bewirkt die **Ausschneide** , dass eine neue Topologie beginnt, wobei die Topologie verwendet wird, die als Geometry-Shader-Ausgabe deklariert ist.

## <a name="restrictions"></a>Beschränkungen

-   Die **Ausschneide** Anweisung gilt nur für den Geometry-Shader.
-   **Ausschneiden** kann beliebig oft im Geometry-Shader vorkommen, einschließlich innerhalb der Fluss Steuerung.
-   Wenn der Geometrie-Shader endet und Scheitel Punkte ausgegeben wurden, wird die Topologie, die Sie aufbauen, abgeschlossen, als ob eine **Ausschneide** als letzte Anweisung ausgeführt wurde.
-   Wenn Streams deklariert wurden, muss [Ausschneide Daten \_ Strom](cut-stream---sm5---asm-.md) anstelle von **Ausschneiden** verwendet werden.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

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

 

 





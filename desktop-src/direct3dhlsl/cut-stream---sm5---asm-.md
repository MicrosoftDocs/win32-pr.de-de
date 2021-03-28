---
title: cut_stream (SM5-ASM)
description: Die Geometry-Shader-Anweisung, die die aktuelle primitive Topologie im angegebenen Stream abschließt, wenn eine beliebige Scheitel Punkte ausgegeben wurden, und startet eine neue Topologie des Typs, der vom Geometry-Shader in diesem Stream deklariert wird.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389508"
---
# <a name="cut_stream-sm5---asm"></a>Ausschneide Daten \_ Strom (SM5-ASM)

Die Geometry-Shader-Anweisung, die die aktuelle primitive Topologie im angegebenen Stream abschließt, wenn eine beliebige Scheitel Punkte ausgegeben wurden, und startet eine neue Topologie des Typs, der vom Geometry-Shader in diesem Stream deklariert wird.



| \_Stream streamindex Ausschneiden |
|-------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[im \] Stream-Index.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn diese Anweisung ausgeführt wird, wird jede zuvor ausgegebene Topologie durch den Geometry-Shader-Aufruf abgeschlossen. Wenn nicht genügend Scheitel Punkte für die vorherige primitive Topologie ausgegeben werden, werden Sie verworfen. Da die einzigen verfügbaren ausgabetopologien für den Geometry-Shader PointList, linestrip und Trianglestrip sind, gibt es nie übrig gebliebene Scheitel Punkte.

*streamindex* muss ein unmittelbarer Wert \[ von 0.. 3 \] für einen deklarierten Stream sein.

Nachdem die vorherige Topologie (sofern vorhanden) abgeschlossen ist, bewirkt diese Anweisung, dass eine neue Topologie beginnt, wobei die Topologie verwendet wird, die als Ausgabe für den Geometry-Shader deklariert ist.

### <a name="restrictions"></a>Beschränkungen

-   Diese Anweisung gilt nur für den Geometry-Shader.
-   **Ausschneide Daten \_ Ströme** können beliebig oft im Geometry-Shader vorkommen, einschließlich innerhalb der Fluss Steuerung.
-   Wenn der Geometrie-Shader endet und Scheitel Punkte ausgegeben wurden, wird die Topologie, die Sie aufbauen, abgeschlossen, als ob eine Anweisung zum **Ausschneiden eines \_ Streams** als letzte Anweisung ausgeführt wurde.
-   Wenn Streams nicht deklariert wurden, müssen Sie [Ausschneiden](cut--sm4---asm-.md) anstelle von **Ausschneide Daten \_ Strom** verwenden.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 






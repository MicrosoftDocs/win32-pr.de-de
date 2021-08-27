---
title: cut_stream (sm5 - asm)
description: Die Geometry-Shaderanweisung, mit der die aktuelle primitive Topologie am angegebenen Stream abgeschlossen wird, wenn Scheitelungen ausgegeben wurden, und startet eine neue Topologie des Typs, der vom Geometrie-Shader in diesem Stream deklariert wird.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c019785d121bfb504b447456ad2376deb9c9c63357621513f42dcdf09351f465
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025020"
---
# <a name="cut_stream-sm5---asm"></a>cut \_ stream (sm5 - asm)

Die Geometry-Shaderanweisung, mit der die aktuelle primitive Topologie am angegebenen Stream abgeschlossen wird, wenn Scheitelungen ausgegeben wurden, und startet eine neue Topologie des Typs, der vom Geometrie-Shader in diesem Stream deklariert wird.



| Stream \_ streamIndex ausschneiden |
|-------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[in \] Der Streamindex.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn diese Anweisung ausgeführt wird, wird jede zuvor vom Aufruf des Geometrie-Shaders ausgegebene Topologie abgeschlossen. Wenn nicht genügend Scheitelungen für die vorherige primitive Topologie ausgegeben werden, werden sie verworfen. Da die einzigen verfügbaren Ausgabetopologien für den Geometrie-Shader Pointlist, Linestrip und Trianglestrip sind, gibt es nie übrige Scheitelpunkt.

*streamIndex* muss für einen deklarierten Stream den unmittelbaren Wert \[ 0..3 \] haben.

Wenn die vorherige Topologie abgeschlossen ist, bewirkt diese Anweisung, dass eine neue Topologie beginnt und die Topologie verwendet wird, die als Ausgabe für den Geometrie-Shader deklariert ist.

### <a name="restrictions"></a>Beschränkungen

-   Diese Anweisung gilt nur für den Geometrie-Shader.
-   **der \_ Ausschneidedatenstrom** kann im Geometrie-Shader eine beliebige Anzahl von Malen angezeigt werden, auch innerhalb der Flusssteuerung.
-   Wenn der Geometrie-Shader endet und Scheitelungen ausgegeben wurden, wird die topologie, die er erstellt, abgeschlossen, als ob eine Ausschneidestreamanweisung als letzte Anweisung ausgeführt wurde. **\_**
-   Wenn Streams nicht deklariert wurden, müssen Sie [cut](cut--sm4---asm-.md) anstelle von **cut stream \_ verwenden.**

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 






---
title: emit_stream (SM5-ASM)
description: Gibt einen Scheitelpunkt für einen angegebenen Stream aus.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389525"
---
# <a name="emit_stream-sm5---asm"></a>\_Ausgabestream (SM5-ASM)

Gibt einen Scheitelpunkt für einen angegebenen Stream aus.



| \_Stream streamindex ausgeben |
|--------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[im \] Stream-Index.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung bewirkt, dass alle deklarierten o- \# Register für den angegebenen Stream aus dem Geometry-Shader gelesen werden, um einen Scheitelpunkt zu generieren. Die Ausgabe gibt an, dass alle Daten in allen Ausgabe Registern für alle Streams nicht initialisiert werden, nicht nur der Stream, der an ausgegeben wird.

*streamindex* muss ein unmittelbarer Wert \[ von 0.. 3 \] für einen deklarierten Stream sein.

Wenn mehrere **\_ ausgabestreamaufrufe** ausgegeben werden, werden primitive generiert.

### <a name="restrictions"></a>Beschränkungen

-   **der \_ Ausgabestream** kann beliebig oft in einem Geometry-Shader vorkommen, einschließlich innerhalb der Fluss Steuerung.
-   Wenn Streams nicht deklariert wurden, müssen Sie die [Ausgabe anstelle des](emit--sm4---asm-.md) Ausgabestreams verwenden. **\_**

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

 

 






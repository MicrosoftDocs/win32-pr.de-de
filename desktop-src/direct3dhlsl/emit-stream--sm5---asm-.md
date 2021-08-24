---
title: emit_stream (sm5 - asm)
description: Geben Sie einen Scheitelpunkt an einen bestimmten Stream aus.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e90bfb72862abeccc8a9411904a7b42f77c933cc4c87af189d6557596389c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562700"
---
# <a name="emit_stream-sm5---asm"></a>Emit \_ stream (sm5 - asm)

Geben Sie einen Scheitelpunkt an einen bestimmten Stream aus.



| Stream \_ streamIndex aus geben |
|--------------------------|



 



| Element                                                                                                               | Beschreibung                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[in \] Der Streamindex.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung bewirkt, dass alle deklarierten o-Register für den angegebenen Stream aus dem Geometrie-Shader gelesen werden, um \# einen Scheitelpunkt zu generieren. Aferieren Sie die Ausgabe. Alle Daten in allen Ausgaberegistern für alle Datenströme werden nicht initialisiert, sondern nicht nur der stream, der ausgegeben wird.

*streamIndex* muss für einen deklarierten Stream den unmittelbaren Wert \[ 0..3 \] haben.

Wenn mehrere **\_ Streamaufrufe** ausgegeben werden, werden Primitive generiert.

### <a name="restrictions"></a>Beschränkungen

-   **emit \_ stream** kann in einem Geometrie-Shader eine beliebige Anzahl von Malen angezeigt werden, auch innerhalb der Flusssteuerung.
-   Wenn Streams nicht deklariert wurden, müssen Sie [emit](emit--sm4---asm-.md) anstelle von **stream \_ verwenden.**

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
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

 

 






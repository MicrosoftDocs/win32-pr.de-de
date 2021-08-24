---
title: dcl_tgsm_structured (sm5 – asm)
description: Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Threadgruppe des Compute-Shaders verfügbar ist. Der Arbeitsspeicher wird als Array von -Strukturen angezeigt.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5bf6a6782c455a9bb51ad941a8b6cb42bd70806512a2eef2ed5bd301e57c77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673900"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>dcl \_ tgsm \_ structured (sm5 – asm)

Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Threadgruppe des Compute-Shaders verfügbar ist. Der Arbeitsspeicher wird als Array von -Strukturen angezeigt.



| dcl \_ tgsm \_ structured g , \# structByteStride, structCount |
|----------------------------------------------------------|



 



| Element                                                                                                                                   | Beschreibung                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                                             | \[in \] Ein Verweis auf einen Block des freigegebenen Arbeitsspeichers der Größe *structByteStride* \* *structCount* Bytes. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[in \] The structure stride. Dieser Wert ist ein uint-Wert in Bytes und muss ein Vielfaches von 4 sein. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[in \] Die Anzahl der Strukturen.<br/>                                                                   |



 

## <a name="remarks"></a>Hinweise

Der Gesamtspeicher für alle g \# muss <= die Menge des pro Threadgruppe verfügbaren freigegebenen Arbeitsspeichers (32 KB) oder 8192 32-Bit-Skalarmodule sein.

Im Extremfall können Sie 8192 g gesamt deklarieren, \# wenn jede *structByteStride* von 4 und eine *structCount* von 1 hat.

Im entgegengesetzten Extremfall können Sie ein einzelnes g \# mit einem Strukturschritt von 32 KB und einer Strukturanzahl von 1 deklarieren.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

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

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






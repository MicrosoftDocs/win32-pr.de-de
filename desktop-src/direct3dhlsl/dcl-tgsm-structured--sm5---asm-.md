---
title: dcl_tgsm_structured (SM5-ASM)
description: Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Compute-Shader s-Thread Gruppe verfügbar ist. Der Arbeitsspeicher wird als Array von-Strukturen angezeigt.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993039"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>DCL \_ TGSM \_ strukturiert (SM5-ASM)

Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Compute-Shader s-Thread Gruppe verfügbar ist. Der Arbeitsspeicher wird als Array von-Strukturen angezeigt.



| DCL \_ TGSM \_ strukturiert g \# , structbytestride, structcount |
|----------------------------------------------------------|



 



| Element                                                                                                                                   | BESCHREIBUNG                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*selbst\#*<br/>                                                                             | \[in \] einem Verweis auf einen Block mit gemeinsam genutzter Arbeitsspeicher Größe von *structbytestride* \* *structcount* bytes. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structbytestride*<br/> | \[in \] der Struktur Stride. Dieser Wert ist ein uint in Bytes und muss ein Vielfaches von 4 sein. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structcount*<br/>                     | \[in \] der Anzahl der Strukturen.<br/>                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Der gesamte Speicherplatz für "g" \# muss <= der Menge an gemeinsam genutzter verfügbarem Arbeitsspeicher pro Thread Gruppe, 32 KB oder 8192 32-Bit-Skaren.

In einem Extremfall können Sie 8192 Gesamt-g s deklarieren \# , wenn beide einen *structbytestride* von 4 und einen *structcount* -Wert von 1 haben.

Im umgekehrten Extremfall können Sie ein einzelnes g \# mit einem Struktur-Stride von 32 KB und einer Struktur Anzahl von 1 deklarieren.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 






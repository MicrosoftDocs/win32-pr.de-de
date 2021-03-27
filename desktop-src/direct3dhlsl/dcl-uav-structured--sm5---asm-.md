---
title: dcl_uav_structured (SM5-ASM)
description: Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219210"
---
# <a name="dcl_uav_structured-sm5---asm"></a>strukturierte DCL \_ -UAV \_ (SM5-ASM)

Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader.



| DCL \_ UAV \_ strukturiert \[ \_ GLC \] dstuav, structbytestride |
|--------------------------------------------------------|



 



| Element                                                                                                                                   | BESCHREIBUNG                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*<br/>                                         | \[in \] der UAV.<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structbytestride*<br/> | \[in \] der Größe der Struktur in Bytes.<br/> |



 

## <a name="remarks"></a>Bemerkungen

*dstuav* ist ein u- \# Register, das als Verweis auf eine unorderedaccessview eines strukturierten Puffers mit dem angegebenen Schritt deklariert wurde, der an die API an den UAV-Slot gebunden werden muss \# .

Der Inhalt der-Struktur hat keinen Typ. für den Arbeitsspeicher ausgeführte Vorgänge können die Daten implizit als Typ interpretieren.

*structbytestride* ist die Größe der Struktur in Bytes im Puffer, der deklariert wird. Dieser Wert muss größer als 0 sein. *structbytestride* ist vom Typ uint und muss ein Vielfaches von 4 sein.

Anweisungen, die auf eine strukturierte u verweisen \# , nehmen eine 2D-Adresse auf, bei der die erste Komponente struct auswählt \[ \] und die zweite Komponente \[ Offset innerhalb von Struktur in ausgerichteten Bytes auswählt \] .

Das \_ GLC-Flag bedeutet "Global kohärent". Das Fehlen von \_ GLC bedeutet, dass die UAV im COMPUTE-Shader nur als "zusammenhängender Gruppe" oder "lokal kohärent" in einem einzelnen Pixelshader-Aufruf deklariert wird.

Das \_ OPC-Flag ist der Wert für die Beibehaltung der Reihenfolge. Wenn eine UAV an Slot \# (u) gebunden ist \# , muss Sie mit dem Counter-Flag erstellt worden sein. Dies bedeutet, dass die Atomic- [ \_ \_ Zuordnungen von "imm Atomic](imm-atomic-alloc--sm5---asm-.md) " oder " [imm \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) " im Shader einen Counter bearbeiten, dessen Werte im Shader als dauerhafter Verweis auf einen Speicherort in der UAV verwendet werden können. Die Daten können nicht neu angeordnet werden, nachdem der Shader vorbei ist.

Wenn das OPC- \_ Flag nicht vorhanden ist, bedeutet dies Folgendes: Wenn der Shader "[imm \_ Atomic \_ Zuweisungs](imm-atomic-alloc--sm5---asm-.md) Anweisungen" oder " [imm \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) using Instructions" verwendet und eine UAV an Slot \# (u) gebunden ist, muss Sie mit dem Append-Flag erstellt worden sein, das einen gegen Wert bereitstellt, der nicht garantiert, dass die Reihenfolge nach dem Aufruf des Shaders

Wenn das \_ OPC-Flag fehlt und der Shader keine " [imm \_ Atomic \_ Zuweisungs](imm-atomic-alloc--sm5---asm-.md) "-oder " [imm \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) using"-Anweisungen enthält, ist es zulässig, dass ein an Slot (u) gebundenes UAV \# mit dem Counter-Flag erstellt wurde (der Counter wird von diesem Shader nicht verwendet), ohne Flag (kein Counter), aber nicht mit dem Append-Flag.

> [!Note]  
> CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen die **strukturierte DCL- \_ TGSM \_**, aber nicht die [DCL- \_ TGSM- \_ Rohdaten](dcl-tgsm-raw--sm5---asm-.md).

 

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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



 

> [!Note]  
> Diese Anweisung wird in CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






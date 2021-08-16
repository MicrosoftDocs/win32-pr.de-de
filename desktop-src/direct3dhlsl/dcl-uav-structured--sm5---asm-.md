---
title: dcl_uav_structured (sm5 - asm)
description: Deklarieren Sie eine ungeordnete Zugriffsansicht (UAV) für die Verwendung durch einen Shader. | dcl_uav_structured (sm5 - asm)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b398dc8b59db6d8fc3a64effdf3cd93b56664881c4c7024a185ad6a212b9fb4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726798"
---
# <a name="dcl_uav_structured-sm5---asm"></a>dcl \_ uav \_ structured (sm5 - asm)

Deklarieren Sie eine ungeordnete Zugriffsansicht (UAV) für die Verwendung durch einen Shader.



| dcl \_ uav \_ structured \[ \_ glc \] dstUAV, structByteStride |
|--------------------------------------------------------|



 



| Element                                                                                                                                   | BESCHREIBUNG                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                                         | \[im \] UAV.<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[in \] Die Größe der Struktur in Bytes.<br/> |



 

## <a name="remarks"></a>Hinweise

*dstUAV* ist ein U-Register, das als Verweis auf eine UnorderedAccessView eines strukturierten Puffers mit dem angegebenen Stride deklariert ist, der an den UAV-Slot in der API gebunden werden \# \# muss.

Der Inhalt der -Struktur hat keinen Typ. Vorgänge, die für den Arbeitsspeicher ausgeführt werden, interpretieren die Daten möglicherweise implizit so, als ob sie einen Typ haben.

*structByteStride ist* die Größe der Struktur in Bytes im puffer, der deklariert wird. Dieser Wert muss größer als 0 sein. *structByteStride* ist vom Typ uint und muss ein Vielfaches von 4 sein.

Anweisungen, die auf ein strukturiertes u verweisen, nehmen eine 2D-Adresse an, wobei die erste Komponente die Struktur auswählt und die zweite Komponente offset innerhalb der Struktur in ausgerichteten Bytes \# \[ \] \[ auswählt. \]

Das \_ glc-Flag bedeutet für "global zusammenhängende". Das Fehlen von glc bedeutet, dass die UAV im Compute-Shader nur als "gruppenreigent" oder bei einem Aufruf eines Einzelnen Pixel-Shaders \_ als "lokal zusammenhängend" deklariert wird.

Das \_ opc-Flag ist der Zähler für die Beibehaltung der Reihenfolge. Sie gibt an, dass ein UAV mit dem COUNTER-Flag erstellt worden sein muss, wenn er an den Slot \# (u) \# gebunden ist. Dies bedeutet, dass [imm \_ atomic \_ alloc-](imm-atomic-alloc--sm5---asm-.md) oder [imm \_ \_ atomic-Vorgänge](imm-atomic-consume--sm5---asm-.md) im Shader einen Zähler bearbeiten, dessen Werte im Shader als permanenter Verweis auf eine Position im UAV verwendet werden können. Daten können nicht neu angeordnet werden, nachdem der Shader beendet wurde.

Das Fehlen des opc-Flags bedeutet, dass, wenn der \_ Shader imm atomic[ \_ \_ alloc-](imm-atomic-alloc--sm5---asm-.md) oder [imm \_ atomic \_ consume-Anweisungen](imm-atomic-consume--sm5---asm-.md) verwendet und ein UAV an den Slot (u) gebunden ist, mit dem APPEND-Flag erstellt worden sein muss, das einen Zähler bietet, der nicht garantiert, dass die Reihenfolge nach dem \# Shaderaufruf beibehalten wird.

Wenn das opc-Flag nicht vorhanden ist und der Shader keine Anweisungen für \_ [imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) oder [imm \_ atomic \_ consume](imm-atomic-consume--sm5---asm-.md) enthält, darf ein UAV, das an Slot (u) gebunden ist, mit dem COUNTER-Flag erstellt worden sein (der Indikator wird von diesem Shader nicht verwendet), kein Flag (kein Indikator), aber nicht mit dem \# APPEND-Flag.

> [!Note]  
> cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützt **dcl \_ tgsm \_ structured**, aber [nicht dcl \_ tgsm \_ raw](dcl-tgsm-raw--sm5---asm-.md).

 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt diese Anweisung für alle Shaderstufen für die Direct3D 11.1-Runtime, die ab Windows 8.



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

> [!Note]  
> Diese Anweisung wird in cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






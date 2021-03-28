---
title: dcl_tessellator_output_primitive (SM5-ASM)
description: Deklarieren Sie den primitiven Typ der Mosaik Ausgabe in einem Hull-Shader-Deklarations Abschnitt.
ms.assetid: 95F074C5-6012-4160-B78E-440C33C1ECC3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 390f22cdafe3b0d078bf8a502623a1c741e34e34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038368"
---
# <a name="dcl_tessellator_output_primitive-sm5---asm"></a>DCL \_ \_ \_ -Mosaik-Ausgabe primitive (SM5-ASM)

Deklarieren Sie den primitiven Typ der Mosaik Ausgabe in einem Hull-Shader-Deklarations Abschnitt.



| DCL-Mosaik \_ \_ Ausgabe \_ primitive {Ausgabe \_ Punkt \| Ausgabe \_ Zeile \| ausgabeausgabe \_ e \_ CW \| Ausgabe \_ Dreieck \_ CCW} |
|----------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                                                                                                                                                                                                                            | BESCHREIBUNG                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*Ausgabe \_ Punkt \| Ausgabe \_ Zeile \| triangloutput \_ e \_ CW \| Ausgabe \_ Dreieck \_ CCW*<br/> | \[im \] Ausgabe primitiven Typ.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle                 | Domain | Geometrie | Pixel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Deklarations Abschnitt |        |          |       |         |



 

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

 

 






---
title: Bytecode-Änderungen in SM 5.1
description: Mit SM 5.1 wird die Deklaration von Ressourcen Registern und die referenzierte Verwendung in Anweisungen geändert.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d66db788b0012a1c3221e37d4c2dd4e41566c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311621"
---
# <a name="bytecode-changes-in-sm51"></a>Bytecode-Änderungen in SM 5.1

Mit SM 5.1 wird die Deklaration von Ressourcen Registern und die referenzierte Verwendung in Anweisungen geändert.

SM 5.1 wechselt zum Deklarieren einer Register-"Variablen", ähnlich wie bei Gruppen Shared-Speicher Registern, wie im folgenden Beispiel veranschaulicht:

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

Die Disassembly dieses Beispiels folgt:

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim Space Slot  Elements
// ------------------------------ ---------- ------- ----------- ----- ---- ---------
// samp0                             sampler      NA          NA     0    5         1
// tex0                              texture  float4          2d     0    5         1
// tex1[0][5][3]                     texture  float4          2d     0   10 unbounded
// tex2[8]                           texture  float4          2d     1    0         8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots used
```

Jeder Shader-Ressourcenbereich verfügt jetzt über eine ID (Name) im Shader-Bytecode. Beispielsweise wird tex1 Texture Array nicht zu "'t 1" im Shader-Bytecode. Das Erteilen von eindeutigen IDs für jeden Ressourcenbereich ermöglicht zwei Dinge:

-   Identifizieren Sie eindeutig den Ressourcenbereich (siehe DCL \_ Resource \_ Texture2D), der in einer Anweisung indiziert wird (siehe Beispiel Anweisung).
-   Fügen Sie eine Gruppe von Attributen an die Deklaration an, z. b. Elementtyp, Stride-Größe, Raster Betriebsmodus usw..

Beachten Sie, dass die ID des Bereichs nicht mit der HLSL-Deklaration in der unteren Grenze verknüpft ist.

Die Reihenfolge der reflektionsressourcenbindungen und der Shader-Deklarations Anweisungen sind identisch, um die Übereinstimmung zwischen HLSL-Variablen und Bytecode-IDs zu ermitteln.

Jede Deklarations Anweisung in SM 5.1 verwendet einen 3D-Operanden, um Folgendes zu definieren: Range ID, Lower und Upper Bounds. Ein zusätzliches Token wird ausgegeben, um den Register Bereich anzugeben. Andere Token können ebenfalls ausgegeben werden, um zusätzliche Eigenschaften des Bereichs zu übermitteln, z. b. die cBuffer-Anweisung oder die strukturierte Puffer Deklarations Anweisung, die die Größe des cBuffer oder der Struktur ausgibt. Die genauen Codierungs Details finden Sie in d3d12TokenizedProgramFormat. h und D3D10ShaderBinary:: cshadercodeparser.

In den Anweisungen von SM 5.1 werden im Rahmen der Anweisung (wie in SM 5.0) keine zusätzlichen Ressourcen Operanden Informationen ausgegeben. Diese Informationen werden jetzt in die Deklarations Anweisungen verschoben. In SM 5.0 erforderte das Indizieren von Ressourcen, dass Ressourcen Attribute in erweiterten Opcode-Token beschrieben werden müssen, da die Indizierung die Zuordnung zur Deklaration verdeckt hat. In SM 5.1 ist jede ID (z. b. 't 1 ') eindeutig einer einzelnen Deklaration zugeordnet, die die erforderlichen Ressourcen Informationen beschreibt. Daher werden die erweiterten Opcode-Token, die für Anweisungen zum Beschreiben von Ressourcen Informationen verwendet werden, nicht mehr ausgegeben.

In nicht Deklarations Anweisungen ist ein Ressourcen Operand für Samplers, Srvs und UAVs ein 2D-Operand. Der erste Index ist eine Literalkonstante, die die Bereichs-ID angibt. Der zweite Index stellt den linearisierten Wert des Indexes dar. Der Wert wird relativ zum Anfang des entsprechenden Register Bereichs (nicht relativ zum Anfang des logischen Bereichs) berechnet, um die Korrelation mit der Stamm Signatur zu verbessern und die Treiber-compilerlast für die Anpassung des Indexes zu verringern.

Ein Ressourcen Operand für cbvs ist ein 3D-Operand: die literalkennung des Bereichs, Index des cBuffer, Offset in die bestimmte Instanz von cBuffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HLSL-Shader-Modell 5,1 Features für Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 5,1](shader-model-5-1.md)
</dt> </dl>

 

 





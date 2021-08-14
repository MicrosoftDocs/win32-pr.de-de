---
title: Bytecodeänderungen in SM5.1
description: SM5.1 ändert, wie Ressourcenregister deklariert und in anweisungen referenziert werden.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93d7d8533bac3750e743166a9d64b687fc06f0fbf21931d44e7d83d462cf15a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794558"
---
# <a name="bytecode-changes-in-sm51"></a>Bytecodeänderungen in SM5.1

SM5.1 ändert, wie Ressourcenregister deklariert und in anweisungen referenziert werden.

SM5.1 geht auf die Deklaration einer Registervariablen zu, ähnlich wie bei Gruppen-Shared Memory-Registern, wie im folgenden Beispiel veranschaulicht:

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

Die Disassemblierung dieses Beispiels folgt:

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

Jeder Shaderressourcenbereich verfügt jetzt über eine ID (einen Namen) im Shader-Bytecode. Beispielsweise wird das Texturarray "tex1" im Shader-Bytecode zu "t1". Die Angabe eindeutiger IDs für jeden Ressourcenbereich ermöglicht zwei Dinge:

-   Identifizieren Sie eindeutig, welcher Ressourcenbereich (siehe dcl resource texture2d) in einer Anweisung indiziert wird \_ \_ (siehe Beispielanweisung).
-   Fügen Sie eine Reihe von Attributen an die Deklaration an, z. B. Elementtyp, Stridegröße, Rasterbetriebsmodus usw.

Beachten Sie, dass die ID des Bereichs nicht mit der HLSL-Untergrenze-Deklaration verknüpft ist.

Die Reihenfolge der Reflektionsressourcenbindungen und Shaderdeklarationsanweisungen ist identisch, um die Übereinstimmung zwischen HLSL-Variablen und Bytecode-IDs zu identifizieren.

Jede Deklarationsanweisung in SM5.1 verwendet einen 3D-Operanden, um die Bereichs-ID, die untere und die obere Grenze zu definieren. Ein zusätzliches Token wird ausgegeben, um den Registerbereich anzugeben. Andere Token können auch ausgegeben werden, um zusätzliche Eigenschaften des Bereichs zu vermitteln, z. B. gibt die Cbuffer- oder strukturierte Pufferdeklarationsanweisung die Größe des Cbuffers oder der Struktur aus. Die genauen Details der Codierung finden Sie in d3d12TokenizedProgramFormat.h und D3D10ShaderBinary::CShaderCodeParser.

SM5.1-Anweisungen geben keine zusätzlichen Ressourcenoperndeninformationen als Teil der Anweisung aus (wie in SM5.0). Diese Informationen werden nun in die Deklarationsanweisungen verschoben. In SM5.0 erforderten Anweisungen zum Indizieren von Ressourcen Ressourcenattribute, die in erweiterten Opcodetoken beschrieben werden mussten, da die Indizierung die Zuordnung zur Deklaration verschleierte. In SM5.1 wird jede ID (z. B. "t1") eindeutig einer einzelnen Deklaration zugeordnet, die die erforderlichen Ressourceninformationen beschreibt. Daher werden die erweiterten Opcodetoken, die in Anweisungen zum Beschreiben von Ressourceninformationen verwendet werden, nicht mehr ausgegeben.

In Anweisungen ohne Deklaration ist ein Ressourcenopernd für Sampler, SRVs und UAVs ein 2D-Operand. Der erste Index ist eine Literalkonst constant, die die Bereichs-ID angibt. Der zweite Index stellt den linearisierten Wert des Indexes dar. Der Wert wird relativ zum Anfang des entsprechenden Registerbereichs berechnet (nicht relativ zum Anfang des logischen Bereichs), um besser mit der Stammsignatur zu korrelieren und den Treibercompileraufwand für die Anpassung des Indexes zu reduzieren.

Ein Ressourcenopernd für CBVs ist ein 3D-Operand: Literal-ID des Bereichs, Index des Cbuffers, Offset in die bestimmte Instanz von cbuffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HLSL-Shadermodell 5.1-Features für Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[Shadermodell 5.1](shader-model-5-1.md)
</dt> </dl>

 

 





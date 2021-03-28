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
# <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="f50eb-103">Bytecode-Änderungen in SM 5.1</span><span class="sxs-lookup"><span data-stu-id="f50eb-103">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="f50eb-104">Mit SM 5.1 wird die Deklaration von Ressourcen Registern und die referenzierte Verwendung in Anweisungen geändert.</span><span class="sxs-lookup"><span data-stu-id="f50eb-104">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span>

<span data-ttu-id="f50eb-105">SM 5.1 wechselt zum Deklarieren einer Register-"Variablen", ähnlich wie bei Gruppen Shared-Speicher Registern, wie im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="f50eb-105">SM5.1 moves towards declaring a register “variable”, similar to how it is done for group shared memory registers, illustrated by the following example:</span></span>

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

<span data-ttu-id="f50eb-106">Die Disassembly dieses Beispiels folgt:</span><span class="sxs-lookup"><span data-stu-id="f50eb-106">The disassembly of this example follows:</span></span>

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

<span data-ttu-id="f50eb-107">Jeder Shader-Ressourcenbereich verfügt jetzt über eine ID (Name) im Shader-Bytecode.</span><span class="sxs-lookup"><span data-stu-id="f50eb-107">Each shader resource range now has an ID (a name) in the shader bytecode.</span></span> <span data-ttu-id="f50eb-108">Beispielsweise wird tex1 Texture Array nicht zu "'t 1" im Shader-Bytecode.</span><span class="sxs-lookup"><span data-stu-id="f50eb-108">For example, tex1 texture array becomes ‘t1’ in the shader byte code.</span></span> <span data-ttu-id="f50eb-109">Das Erteilen von eindeutigen IDs für jeden Ressourcenbereich ermöglicht zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="f50eb-109">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="f50eb-110">Identifizieren Sie eindeutig den Ressourcenbereich (siehe DCL \_ Resource \_ Texture2D), der in einer Anweisung indiziert wird (siehe Beispiel Anweisung).</span><span class="sxs-lookup"><span data-stu-id="f50eb-110">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="f50eb-111">Fügen Sie eine Gruppe von Attributen an die Deklaration an, z. b. Elementtyp, Stride-Größe, Raster Betriebsmodus usw..</span><span class="sxs-lookup"><span data-stu-id="f50eb-111">Attach set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc..</span></span>

<span data-ttu-id="f50eb-112">Beachten Sie, dass die ID des Bereichs nicht mit der HLSL-Deklaration in der unteren Grenze verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="f50eb-112">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="f50eb-113">Die Reihenfolge der reflektionsressourcenbindungen und der Shader-Deklarations Anweisungen sind identisch, um die Übereinstimmung zwischen HLSL-Variablen und Bytecode-IDs zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="f50eb-113">The order of reflection resource bindings and shader declaration instructions is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="f50eb-114">Jede Deklarations Anweisung in SM 5.1 verwendet einen 3D-Operanden, um Folgendes zu definieren: Range ID, Lower und Upper Bounds.</span><span class="sxs-lookup"><span data-stu-id="f50eb-114">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="f50eb-115">Ein zusätzliches Token wird ausgegeben, um den Register Bereich anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f50eb-115">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="f50eb-116">Andere Token können ebenfalls ausgegeben werden, um zusätzliche Eigenschaften des Bereichs zu übermitteln, z. b. die cBuffer-Anweisung oder die strukturierte Puffer Deklarations Anweisung, die die Größe des cBuffer oder der Struktur ausgibt.</span><span class="sxs-lookup"><span data-stu-id="f50eb-116">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="f50eb-117">Die genauen Codierungs Details finden Sie in d3d12TokenizedProgramFormat. h und D3D10ShaderBinary:: cshadercodeparser.</span><span class="sxs-lookup"><span data-stu-id="f50eb-117">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and D3D10ShaderBinary::CShaderCodeParser.</span></span>

<span data-ttu-id="f50eb-118">In den Anweisungen von SM 5.1 werden im Rahmen der Anweisung (wie in SM 5.0) keine zusätzlichen Ressourcen Operanden Informationen ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="f50eb-118">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="f50eb-119">Diese Informationen werden jetzt in die Deklarations Anweisungen verschoben.</span><span class="sxs-lookup"><span data-stu-id="f50eb-119">This information is now moved to the declaration instructions.</span></span> <span data-ttu-id="f50eb-120">In SM 5.0 erforderte das Indizieren von Ressourcen, dass Ressourcen Attribute in erweiterten Opcode-Token beschrieben werden müssen, da die Indizierung die Zuordnung zur Deklaration verdeckt hat.</span><span class="sxs-lookup"><span data-stu-id="f50eb-120">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="f50eb-121">In SM 5.1 ist jede ID (z. b. 't 1 ') eindeutig einer einzelnen Deklaration zugeordnet, die die erforderlichen Ressourcen Informationen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f50eb-121">In SM5.1 each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="f50eb-122">Daher werden die erweiterten Opcode-Token, die für Anweisungen zum Beschreiben von Ressourcen Informationen verwendet werden, nicht mehr ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="f50eb-122">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="f50eb-123">In nicht Deklarations Anweisungen ist ein Ressourcen Operand für Samplers, Srvs und UAVs ein 2D-Operand.</span><span class="sxs-lookup"><span data-stu-id="f50eb-123">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="f50eb-124">Der erste Index ist eine Literalkonstante, die die Bereichs-ID angibt.</span><span class="sxs-lookup"><span data-stu-id="f50eb-124">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="f50eb-125">Der zweite Index stellt den linearisierten Wert des Indexes dar.</span><span class="sxs-lookup"><span data-stu-id="f50eb-125">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="f50eb-126">Der Wert wird relativ zum Anfang des entsprechenden Register Bereichs (nicht relativ zum Anfang des logischen Bereichs) berechnet, um die Korrelation mit der Stamm Signatur zu verbessern und die Treiber-compilerlast für die Anpassung des Indexes zu verringern.</span><span class="sxs-lookup"><span data-stu-id="f50eb-126">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="f50eb-127">Ein Ressourcen Operand für cbvs ist ein 3D-Operand: die literalkennung des Bereichs, Index des cBuffer, Offset in die bestimmte Instanz von cBuffer.</span><span class="sxs-lookup"><span data-stu-id="f50eb-127">A resource operand for CBVs is a 3D operand: literal ID of the range, index of the cbuffer, offset into the particular instance of cbuffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f50eb-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f50eb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f50eb-129">HLSL-Shader-Modell 5,1 Features für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f50eb-129">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="f50eb-130">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="f50eb-130">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> </dl>

 

 





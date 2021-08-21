---
title: ShaderModell 4-Assembly
description: ShaderModell 4-Assembly
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 805ffe89b1f9d14ca70da0a8121353e6bf766b8b6e433441350d1b55c4531415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119954"
---
# <a name="shader-model-4-assembly"></a>ShaderModell 4-Assembly

Shadermodell 4 erfordert, dass Sie Shader in HLSL programmieren. Der Shadercompiler kompiliert den HLSL-Code jedoch in eine Assembly, die auf dem Gerät ausgeführt wird. Wenn Sie PIX für Windows zum Debuggen Ihrer Shader verwenden, können Sie shader-Code entweder in HLSL oder assembly anzeigen. In diesem Abschnitt werden die Assemblyanweisungen shader Model 4 und Shader Model 4.1 aufgeführt, die beim Debuggen eines Shaders auftreten können.

<dl>

[Anweisungsmodifizierer](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[breakc](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[callc](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[continue](continue--sm4---asm-.md)  
[continuec](continuec--sm4---asm-.md)  
[Schneiden](cut--sm4---asm-.md)  
[dcl \_ constantBuffer](dcl-constantbuffer.md)  
[dcl \_ globalFlags](dcl-globalflags.md)  
[dcl \_ immediateConstantBuffer](dcl-immediateconstantbuffer.md)  
[dcl \_ indexableTemp](dcl-indexabletemp.md)  
[dcl \_ indexRange](dcl-indexrange.md)  
[\_DCL-Eingabe](dcl-input.md)  
[dcl \_ input \_ sv](dcl-input-sv.md)  
[dcl \_ input vPrim](dcl-input-vprim.md)  
[dcl \_ maxOutputVertexCount](dcl-maxoutputvertexcount.md)  
[\_dcl-Ausgabe](dcl-output.md)  
[dcl \_ output \_ oDepth](dcl-output-odepth.md)  
[dcl \_ output \_ sgv](dcl-output-sgv.md)  
[dcl \_ output \_ siv](dcl-output-siv.md)  
[dcl \_ outputTopology](dcl-outputtopology.md)  
[\_dcl-Ressource](dcl-resource.md)  
[dcl \_ sampler](dcl-sampler.md)  
[dcl \_ temps](dcl-temps.md)  
[default](default--sm4---asm-.md)  
[deriv \_ rtx](deriv-rtx--sm4---asm-.md)  
[deriv \_ rty](deriv-rty--sm4---asm-.md)  
[Verwerfen](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[dp2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[dp4](dp4--sm4---asm-.md)  
[else](else--sm4---asm-.md)  
[Emittieren](emit--sm4---asm-.md)  
[emitThenCut](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[endloop](endloop--sm4---asm-.md)  
[endswitch](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[Frc](frc--sm4---asm-.md)  
[ftoi](ftoi--sm4---asm-.md)  
[ftou](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[iadd](iadd--sm4---asm-.md)  
[ibfe](dne--sm5---asm-.md)  
[ieq](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[Ige](ige--sm4---asm-.md)  
[Ilt](ilt--sm4---asm-.md)  
[Imad](imad--sm4---asm-.md)  
[imin](imin--sm4---asm-.md)  
[imul](imul--sm4---asm-.md)  
[Ine](ine--sm4---asm-.md)  
[ineg](ineg--sm4---asm-.md)  
[ishl](ishl--sm4---asm-.md)  
[ishr](ishr--sm4---asm-.md)  
[itof](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[ld](ld--sm4---asm-.md)  
[Protokoll](log--sm4---asm-.md)  
[Schleife](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[wütend](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[Mov](mov--sm4---asm-.md)  
[movc](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[Nop](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md)  
[or](or--sm4---asm-.md)  
[Resinfo](resinfo--sm4---asm-.md)  
[Ret](ret--sm4---asm-.md)  
[retc](retc--sm4---asm-.md)  
[round \_ ne](round-ne--sm4---asm-.md)  
[round \_ ni](round-ni--sm4---asm-.md)  
[runder \_ Pi](round-pi--sm4---asm-.md)  
[round \_ z](round-z--sm4---asm-.md)  
[rsq](rsq--sm4---asm-.md)  
[Beispiel](sample--sm4---asm-.md)  
[Beispiel \_ b](sample-b--sm4---asm-.md)  
[Beispiel \_ c](sample-c--sm4---asm-.md)  
[Beispiel \_ c \_ lz](sample-c-lz--sm4---asm-.md)  
[Beispiel \_ d](sample-d--sm4---asm-.md)  
[Beispiel \_ l](sample-l--sm4---asm-.md)  
[sincos](sincos--sm4---asm-.md)  
[Sqrt](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[udiv](udiv--sm4---asm-.md)  
[uge](uge--sm4---asm-.md)  
[Ult](ult--sm4---asm-.md)  
[umad](umad--sm4---asm-.md)  
[Umax](umax--sm4---asm-.md)  
[umin](umin--sm4---asm-.md)  
[umul](umul--sm4---asm-.md)  
[ushr](ushr--sm4---asm-.md)  
[utof](utof--sm4---asm-.md)  
[Xor](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>Shadermodell 4.1-Assembly

ShaderModell 4.1 unterstützt alle Shadermodell 4.0-Anweisungen und die folgenden zusätzlichen Anweisungen:

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[Lod](lod--sm4-1---asm-.md)  
[sampleinfo](sampleinfo--sm4-1---asm-.md)  
[samplepos](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asm-Shaderreferenz](dx9-graphics-reference-asm.md)
</dt> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





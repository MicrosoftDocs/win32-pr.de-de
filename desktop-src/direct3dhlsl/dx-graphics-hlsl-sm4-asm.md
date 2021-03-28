---
title: Shader Model 4-Assembly
description: Shader Model 4-Assembly
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036999"
---
# <a name="shader-model-4-assembly"></a>Shader Model 4-Assembly

Shadermodell 4 erfordert, dass Sie Shader in HLSL programmieren. Der Shader-Compiler kompiliert den HLSL-Code jedoch in eine Assembly, die auf dem Gerät ausgeführt wird. Wenn Sie pix für Windows verwenden, um die Shader zu debuggen, können Sie den Shader-Code entweder in HLSL oder in der Assembly anzeigen. In diesem Abschnitt werden die Assemblyanweisungen Shader Model 4 und Shader Model 4,1 aufgelistet, die beim Debuggen eines Shaders auftreten können.

<dl>

[Anweisungs Modifizierer](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[breakc](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[callc](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[continue](continue--sm4---asm-.md)  
[continuec](continuec--sm4---asm-.md)  
[Schnitts](cut--sm4---asm-.md)  
[DCL \_ constantbuffer](dcl-constantbuffer.md)  
[DCL \_ globalflags](dcl-globalflags.md)  
[DCL \_ unmittelateconstantbuffer](dcl-immediateconstantbuffer.md)  
[DCL- \_ indexabletemp](dcl-indexabletemp.md)  
[DCL- \_ Indexbereich](dcl-indexrange.md)  
[DCL- \_ Eingabe](dcl-input.md)  
[DCL- \_ Eingabe \_ SV](dcl-input-sv.md)  
[DCL- \_ Eingabe vprim](dcl-input-vprim.md)  
[DCL \_ maxoutputvertexcount](dcl-maxoutputvertexcount.md)  
[DCL- \_ Ausgabe](dcl-output.md)  
[DCL- \_ Ausgabe- \_ otiefe](dcl-output-odepth.md)  
[DCL- \_ Ausgabe ( \_ Scalable)](dcl-output-sgv.md)  
[DCL- \_ Ausgabe ( \_ SIV)](dcl-output-siv.md)  
[DCL- \_ outputtopology](dcl-outputtopology.md)  
[DCL- \_ Ressource](dcl-resource.md)  
[DCL- \_ Sampler](dcl-sampler.md)  
[DCL- \_ Temps](dcl-temps.md)  
[default](default--sm4---asm-.md)  
[DERIV \_ RTX](deriv-rtx--sm4---asm-.md)  
[DERIV- \_ Eigenschaft](deriv-rty--sm4---asm-.md)  
[Würfen](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[DP2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[dp4](dp4--sm4---asm-.md)  
[else](else--sm4---asm-.md)  
[ausgeben](emit--sm4---asm-.md)  
[emitthencut](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[ENDLOOP](endloop--sm4---asm-.md)  
[Endswitch](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[FRC](frc--sm4---asm-.md)  
[der Befehl](ftoi--sm4---asm-.md)  
[ftou](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[IAdd](iadd--sm4---asm-.md)  
[ibfe](dne--sm5---asm-.md)  
[IEQ](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[ige](ige--sm4---asm-.md)  
[ILT](ilt--sm4---asm-.md)  
[Imad](imad--sm4---asm-.md)  
[Imin](imin--sm4---asm-.md)  
[imul](imul--sm4---asm-.md)  
[Bina](ine--sm4---asm-.md)  
[InEG](ineg--sm4---asm-.md)  
[ishl](ishl--sm4---asm-.md)  
[ISHR](ishr--sm4---asm-.md)  
[itof](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[Teufels](ld--sm4---asm-.md)  
[angezeigt](log--sm4---asm-.md)  
[loop](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[geworden](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[MOV](mov--sm4---asm-.md)  
["muvc"](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[NOP](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md)  
[or](or--sm4---asm-.md)  
[ResInfo](resinfo--sm4---asm-.md)  
[TZI](ret--sm4---asm-.md)  
[RETC](retc--sm4---asm-.md)  
[\_roundne](round-ne--sm4---asm-.md)  
[Round- \_ NI](round-ni--sm4---asm-.md)  
[Round \_ Pi](round-pi--sm4---asm-.md)  
[Round \_ z](round-z--sm4---asm-.md)  
[RSQ](rsq--sm4---asm-.md)  
[Blutprobe](sample--sm4---asm-.md)  
[Beispiel \_ b](sample-b--sm4---asm-.md)  
[Beispiel \_ c](sample-c--sm4---asm-.md)  
[Beispiel- \_ c- \_ LZ](sample-c-lz--sm4---asm-.md)  
[Beispiel \_ d](sample-d--sm4---asm-.md)  
[Beispiel \_ l](sample-l--sm4---asm-.md)  
[SinCos](sincos--sm4---asm-.md)  
[SQRT](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[udiv](udiv--sm4---asm-.md)  
[UGE](uge--sm4---asm-.md)  
[ULT](ult--sm4---asm-.md)  
[Umad](umad--sm4---asm-.md)  
[Umax](umax--sm4---asm-.md)  
[-in](umin--sm4---asm-.md)  
[Umul](umul--sm4---asm-.md)  
["ushr"](ushr--sm4---asm-.md)  
[utof](utof--sm4---asm-.md)  
[xor](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>Shader-Modell 4,1-Assembly

Shader-Modell 4,1 unterstützt alle Shadermodell-4,0-Anweisungen und die folgenden zusätzlichen Anweisungen:

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[LOD](lod--sm4-1---asm-.md)  
[sampleingefo](sampleinfo--sm4-1---asm-.md)  
[samplepos](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASM-Shader-Referenz](dx9-graphics-reference-asm.md)
</dt> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





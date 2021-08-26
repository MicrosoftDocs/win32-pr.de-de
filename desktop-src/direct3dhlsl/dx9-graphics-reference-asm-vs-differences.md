---
title: Vertex-Shaderunterschiede
description: Vertex-Shaderunterschiede
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 411a3a742fca508839651d56912fa00b2a6d8b82908b159694a3b1eff88f2318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982820"
---
# <a name="vertex-shader-differences"></a>Vertex-Shaderunterschiede

## <a name="instruction-slots"></a>Anweisungsslots

Jede Version unterstützt eine unterschiedliche Anzahl von maximalen Anweisungsslots.



| Version  | Maximale Anzahl von Anweisungsslots                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| Vs. \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | Mindestens 512 und bis zur Anzahl von Slots in D3DCAPS9. MaxVertexShader30InstructionSlots. Siehe [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). |



 

Informationen zu den Einschränkungen von Software-Shadern finden Sie unter [Software-Shader](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Flow Steuern von Schachtelungsgrenzwerten

-   Siehe [Flow Control Nesting Limits (Schachtelungsgrenzwerte für Steuerelement).](dx9-graphics-reference-asm-vs-instructions-flow-control.md)

## <a name="vs_1_1-features"></a>vs \_ 1 \_ 1 Features

Neue Anweisungen:

Siehe [Anweisungen – im Vergleich \_ zu 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).

Neue Register:

Siehe [Register – im Vergleich zu \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).

## <a name="vs_2_0-features"></a>vs \_ 2 \_ 0 Features

Neue Funktionen:

-   Statische Flusssteuerung
-   Alle vier Komponenten des [Adressregisters](dx9-graphics-reference-asm-vs-registers-address.md) (a0) sind verfügbar.

Neue Anweisungen:

-   Setupanweisungen – [defb – vs](defb---vs.md), [defi – vs](defi---vs.md)
-   Arithmetische Anweisungen – [abs – vs](abs---vs.md), [crs – vs](crs---vs.md), [lrp – vs](lrp---vs.md), [mova – vs](mova---vs.md), [nrm – vs](nrm---vs.md), [pow – vs](pow---vs.md), [sgn – vs](sgn---vs.md), [sincos – vs](sincos---vs.md)
-   Anweisungen für die statische Flusssteuerung – Aufruf – [vs](call---vs.md), [callnz bool – vs](callnz-bool---vs.md), else [–](else---vs.md)vs , [endif –](endif---vs.md)vs , [endloop – vs](endloop---vs.md), [endrep – vs](endrep---vs.md), if [bool – vs](if-bool---vs.md), label – [vs](label---vs.md), loop [– vs](loop---vs.md), rep [– vs](rep---vs.md), [ret – vs](ret---vs.md)

Neue Register:

-   [Konstantes boolesches Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)

## <a name="vs_2_x-features"></a>vs \_ 2 \_ x Features

Neue Features (D3DCAPS9. VS20Caps):

-   Dynamische Flusssteuerung
-   Schachtelung für Anweisungen zur dynamischen und statischen Flusssteuerung
-   Anzahl der [temporären Register](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) erhöht
-   Prädikation

Neue Anweisungen:

-   Anweisungen zur dynamischen Flusssteuerung – break [– vs](break---vs.md), break comp [– \_ vs](break-comp---vs.md), [breakp – vs](breakp---vs.md), [callnz pred – vs](callnz-pred---vs.md), wenn comp – [ \_ vs](if-comp---vs.md), wenn [pred – vs](if-pred---vs.md), [setp comp – \_ vs](setp-comp---vs.md)

Neue Register:

-   [Prädikatregister](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)

## <a name="vs_3_0-features"></a>vs \_ 3 \_ 0 Features

Neue Features:

-   Textursuche
-   [Indizierbare Ausgaberegister](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# )
-   Anzahl der [temporären Register](dx9-graphics-reference-asm-vs-registers-temporary.md)(r) \# auf 32 erhöht

Neue Anweisungen:

-   Setupanweisung – [dcl \_ samplerType (sm3 – vs asm)](dcl-samplertype---vs.md)
-   Texturanweisung – [texldl – vs](texldl---vs.md)

Neue Register:

-   [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
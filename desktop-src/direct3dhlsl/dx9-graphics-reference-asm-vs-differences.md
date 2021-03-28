---
title: Vertexshader-Unterschiede
description: Vertexshader-Unterschiede
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039121"
---
# <a name="vertex-shader-differences"></a>Vertexshader-Unterschiede

## <a name="instruction-slots"></a>Anweisungs Slots

Jede Version unterstützt eine abweichende Anzahl an maximalen Anweisungs Slots.



| Version  | Maximale Anzahl von Anweisungs Slots                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| vs \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | 512 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. MaxVertexShader30InstructionSlots. Siehe [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). |



 

Informationen zu den Einschränkungen von Software-Shadern finden Sie unter [Software-Shader](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Schachtelungs Limits der Fluss Steuerung

-   Siehe Schachtelungs [Limits der Fluss Steuerung](dx9-graphics-reference-asm-vs-instructions-flow-control.md).

## <a name="vs_1_1-features"></a>vs \_ 1 \_ 1-Features

Neue Anweisungen:

Weitere Informationen finden Sie unter [Anweisungen-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).

Neue Register:

Weitere Informationen finden Sie unter [Registern-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).

## <a name="vs_2_0-features"></a>vs \_ 2 \_ 0-Features

Neue Funktionen:

-   Statische Fluss Steuerung
-   Alle vier Komponenten des [Adress Registers](dx9-graphics-reference-asm-vs-registers-address.md) (a0) sind verfügbar.

Neue Anweisungen:

-   Setup Anweisungen- [DEFB-vs](defb---vs.md), [defi-vs](defi---vs.md)
-   Arithmetische Anweisungen: [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [MUVA-vs](mova---vs.md), [NRM-vs](nrm---vs.md), [Pow-vs](pow---vs.md), [SGN-vs](sgn---vs.md), [SinCos-vs](sincos---vs.md)
-   Anweisungen zur statischen Fluss Steuerung: [aufrufen-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [else-vs](else---vs.md), [EndIf-vs](endif---vs.md), [ENDLOOP-vs](endloop---vs.md), [ENDREP-vs](endrep---vs.md), [if bool-vs](if-bool---vs.md), [Label-vs](label---vs.md), [Loop-vs](loop---vs.md), [Rep-vs](rep---vs.md), [ret-vs](ret---vs.md)

Neue Register:

-   [Konstantes boolesches Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Konstantes ganzzahliges Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Schleifen-Counter-Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al)

## <a name="vs_2_x-features"></a>vs \_ 2 \_ x-Features

Neue Features (D3DCAPS9). VS20Caps):

-   Dynamische Fluss Steuerung
-   Schachtelung für dynamische und statische Fluss Steuerungs Anweisungen
-   Anzahl der [temporären Registrierungs](dx9-graphics-reference-asm-vs-registers-temporary.md)-e (r \# )
-   Prädikation

Neue Anweisungen:

-   Dynamische Fluss Steuerungs Anweisungen: unter [brechen](break---vs.md)von [Comp- \_ vs](break-comp---vs.md), Break [p-vs](breakp---vs.md), [callnz pred-vs](callnz-pred---vs.md), [if \_ Comp-vs](if-comp---vs.md), [if pred-vs](if-pred---vs.md), [SETP \_ Comp-vs](setp-comp---vs.md)

Neue Register:

-   [Prädikat Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)

## <a name="vs_3_0-features"></a>vs \_ 3 \_ 0-Features

Neue Features:

-   Textur Suche
-   Indizierbare [Ausgabe Register](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# )
-   Anzahl der [temporären Registrierungs](dx9-graphics-reference-asm-vs-registers-temporary.md)-e (r \# ) wurde auf 32 erweitert.

Neue Anweisungen:

-   Setup Anweisung- [DCL \_ samplertype (SM3-vs ASM)](dcl-samplertype---vs.md)
-   Textur Anweisung- [texldl-vs](texldl---vs.md)

Neue Register:

-   [Sampler (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
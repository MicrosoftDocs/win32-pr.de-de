---
title: Pixel-Shader-Unterschiede
description: Pixel-Shader-Unterschiede
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390504"
---
# <a name="pixel-shader-differences"></a>Pixel-Shader-Unterschiede

## <a name="instruction-slots"></a>Anweisungs Slots

Jede Version unterstützt eine andere Anzahl an maximalen Anweisungs Slots.



| Version  | Maximale Anzahl von Anweisungs Slots                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| PS \_ 1 \_ 1 | 4 Textur + 8 Arithmetik                                                                                              |
| PS \_ 1 \_ 2 | 4 Textur + 8 Arithmetik                                                                                              |
| PS \_ 1 \_ 3 | 4 Textur + 8 Arithmetik                                                                                              |
| PS \_ 1 \_ 4 | 6 Textur + 8 Arithmetik pro Phase                                                                                    |
| PS \_ 2 \_ 0 | 32 Textur + 64 Arithmetik                                                                                            |
| PS \_ 2 \_ x | 96 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. D3DPSHADERCAPS2 \_ 0. numinstructionslots. Siehe D3DPSHADERCAPS2 \_ 0. |
| PS \_ 3 \_ 0 | 512 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. MaxPixelShader30InstructionSlots. Siehe D3DPSHADERCAPS2 \_ 0.      |



 

Informationen zu den Einschränkungen von Software-Shadern finden Sie unter [Software-Shader](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Schachtelungs Limits der Fluss Steuerung

-   Siehe [Fluss Steuerungs Einschränkungen](dx9-graphics-reference-asm-ps-instructions-flow-control.md).

## <a name="ps_1_x-features"></a>PS \_ 1 \_ x-Funktionen

Neue Anweisungen:

Weitere Informationen finden Sie unter [PS 1 \_ \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).

Neue Register:

Siehe [PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4-Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="ps_2_0-features"></a>PS \_ 2 \_ 0-Features

Neue Funktionen:

-   Drei neue "swi. yzxw", ". zxyw", ". wzyx"
-   Die Anzahl der [temporären Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) wurde auf 12 angehoben.
-   Anzahl [konstanter float-Register](dx9-graphics-reference-asm-ps-registers-constant-float.md) Register (c \# ) auf 32
-   Anzahl der [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t \# ) wurde auf 8 angehoben.

Neue Anweisungen:

-   Setup Anweisungen- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)
-   Arithmetische Anweisungen- [ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [Exp-PS](exp---ps.md), [FRC-PS](frc---ps.md), [Log-PS](log---ps.md), [m3x2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md), [M4x4-PS](m4x4---ps.md), [Max-PS](max---ps.md), [Min-PS](min---ps.md), [NRM-PS](nrm---ps.md), [Pow-PS](pow---ps.md), [RCP-PS](rcp---ps.md), [RSQ-PS](rsq---ps.md), [SinCos-PS](sincos---ps.md)
-   Textur Anweisungen- [texld-PS \_ 2 \_ 0 und aufwärts](texld---ps-2-0.md) (unterschiedliche Syntax), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)

Neue Register:

-   [Sampler (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \#

## <a name="ps_2_x-features"></a>PS \_ 2 \_ x-Features

Neue Features (siehe [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)):

-   Dynamische Fluss Steuerung
-   Statische Fluss Steuerung
-   Schachtelung für dynamische und statische Fluss Steuerungs Anweisungen
-   Anzahl der [temporären Registrierungs](dx9-graphics-reference-asm-ps-registers-temporary.md)-e (r \# )
-   Beliebiger Quellpfad
-   Farbverlaufs Anweisungen
-   Prädikation
-   Keine abhängige Textur Lese Beschränkung
-   Keine Textur Anweisungs Beschränkung

Neue Anweisungen:

-   Anweisungen zur statischen Fluss Steuerung: [if bool-PS](if-bool---ps.md), [callps](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [EndIf-PS](endif---ps.md), [Rep-PS](rep---ps.md), [ENDREP-PS](endrep---ps.md), [Label-PS](label---ps.md), [ret-PS](ret---ps.md)
-   Dynamische Fluss Steuerungs Anweisungen-unter [brechen](break---ps.md)von [ \_ Comp-PS](break-comp---ps.md), [breakp-PS](break-p---ps.md), [callnz pred-PS](callnz-pred---ps.md), [if \_ Comp-PS](if-comp---ps.md), [if pred-PS](if-pred---ps.md), [SETP \_ Comp-PS](setp-comp---ps.md)
-   Arithmetische Anweisungen- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)
-   Textur Anweisung- [texldd-PS](texldd---ps.md)

Neue Register:

-   [Prädikat Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)

## <a name="ps_3_0-features"></a>Features von PS \_ 3 \_ 0

Neue Funktionen:

-   Konsolidierte 10 [Eingabe Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)s (v \# )
-   Indizierbares [Eingabe Farb Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) mit dem [Schleifen-Counter-Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al)
-   Anzahl der [temporären Registrierungs](dx9-graphics-reference-asm-ps-registers-temporary.md)-e (r \# ) wurde auf 32 erweitert.
-   Anzahl [konstanter float-Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c \# ) auf 224

Neue Anweisungen:

-   Setup Anweisung- [DCL- \_ Semantik (SM3-PS ASM)](dcl-usage---ps.md)
-   Statische Fluss Anweisungen- [Loop-PS](loop---ps.md), [ENDLOOP-PS](endloop---ps.md)
-   Arithmetische Anweisung- [SinCos-PS](sincos---ps.md) (neue Syntax)
-   Textur Anweisung- [texldl-PS](texldl---ps.md)

Neue Register:

-   [Eingabe Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )
-   [Positions Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vpos)
-   [Gesichts Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vface)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 
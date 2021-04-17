---
title: vs_2_x
description: Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473756"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.

Die Vertex-Shader-Version vs \_ 2 \_ x erweitert den von vs \_ 2 0 unterstützten Funktions Satz \_ . Jede zusätzliche Funktion wird durch eine entsprechende Obergrenze in der [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) -Struktur innerhalb von [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps)dargestellt. Um eine der erweiterten Features zu verwenden, die durch diese Caps repräsentiert werden, muss die Vertex-Shader-Version als vs \_ 2 x angegeben werden \_ .

-   [Anweisungen-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) enthält eine Liste der verfügbaren Anweisungen.
-   [Register-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) listet die verschiedenen Register Typen auf, die von Vertex-Shader-Alu verwendet werden.
-   [Vertex-Shader-registermodifiziererer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   [Vertex-Shader-Quell Registrierungs Modifizierers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.
-   Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.
-   Die [Ziel Register Maskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.

## <a name="new-features"></a>Neue Funktionen

Die neuen Features lauten wie folgt:

### <a name="dynamic-flow-control"></a>Dynamische Fluss Steuerung

Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0 ist, werden die folgenden dynamischen Fluss Steuerungs Anweisungen unterstützt:

-   [Wenn \_ Comp-vs](if-comp---vs.md)
-   [Break-vs](break---vs.md)
-   [" \_ Comp-vs" Abbrechen](break-comp---vs.md)

Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) ebenfalls festgelegt ist, werden die folgenden zusätzlichen Anweisungen für die Fluss Steuerung unterstützt:

-   [SETP \_ -Comp-vs](setp-comp---vs.md)
-   [Wenn pred-vs](if-pred---vs.md)
-   [callnz pred-vs](callnz-pred---vs.md)
-   [Break p-vs](breakp---vs.md)

Der Wertebereich für die Tiefe der dynamischen Fluss Steuerung liegt zwischen 0 und 24 und entspricht der Schachtelungs Tiefe der dynamischen Fluss Steuerungs Anweisungen (Weitere Informationen finden Sie unter [Fluss Steuerungs](dx9-graphics-reference-asm-vs-instructions-flow-control.md) Schachtelungs Limits). Wenn diese Obergrenze NULL ist, unterstützt das Gerät keine Anweisungen zur dynamischen Fluss Steuerung.

### <a name="number-of-temporary-registers"></a>Anzahl temporärer Register

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) stellt die Anzahl der vom Gerät unterstützten [temporären Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s dar. Der Wertebereich für diese Obergrenze liegt zwischen 12 und 32.

### <a name="static-flow-control-nesting-depth"></a>Schachtelungs Tiefe der statischen Fluss Steuerung

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) stellt die Schachtelungs Tiefe von zwei Typen von statischen Fluss Steuerungs Anweisungen dar: [Loop-vs](loop---vs.md) / [Rep-vs](rep---vs.md) und [](call---vs.md) / [Call-vs callnz bool-vs](callnz-bool---vs.md) / ,[Wenn bool-vs](if-bool---vs.md). Loop-vs/Rep-vs-Anweisungen bis zu D3DVS20CAPS tief geschachtelt werden können. Unabhängig davon können die Anweisungen "Aufruf-vs/callnz bool-vs" bis zu D3DVS20CAPS tief verschachtelt werden. Wenn D3DVS20CAPS ebenfalls festgelegt ist, wird [callnz pred-vs](callnz-pred---vs.md) in Richtung der Schachtelungs Tiefe von Call-vs/callnz bool-vs/if bool-vs gezählt (Weitere Informationen finden Sie unter [Fluss Steuerungs](dx9-graphics-reference-asm-vs-instructions-flow-control.md) Schachtelungs Limits).

### <a name="predication"></a>Prädikation

Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) festgelegt ist, unterstützt das Gerät [SETP \_ Comp-vs](setp-comp---vs.md) und Anweisungs Prädikat. Wenn D3DVS20CAPS auch größer als 0 ist, werden die folgenden zusätzlichen dynamischen Fluss Steuerungs Anweisungen unterstützt:

-   [Wenn pred-vs](if-pred---vs.md)
-   [callnz pred-vs](callnz-pred---vs.md)
-   [Break p-vs](breakp---vs.md)

### <a name="instruction-count"></a>Anweisungs Anzahl

Jeder Vertex-Shader kann bis zu 256 Anweisungen enthalten. Die Anzahl der auszustellenden Anweisungen kann aufgrund der Unterstützung für Schleifen/Rep erheblich höher sein und wird von [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)begrenzt. Dies sollte mindestens 0xFFFF betragen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
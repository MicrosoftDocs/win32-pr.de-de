---
title: ps_2_x
description: Erfahren Sie ps_2_x, einen programmierbaren Pixel-Shader, der aus einer Reihe von Anweisungen besteht, die mit Pixeldaten arbeiten.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37bc9709effeb865651ca920a155094946b88753586174ecf6e1ab06eabd2fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489410"
---
# <a name="ps_2_x"></a>PS \_ 2 \_ x

Ein programmierbarer Pixel-Shader besteht aus einer Reihe von Anweisungen, die mit Pixeldaten arbeiten. Registriert Übertragungsdaten in und aus der ALU. Zusätzliche Steuerung kann angewendet werden, um die Anweisung, die Ergebnisse oder die ausgeschriebenen Daten zu ändern.

-   [ps \_ 2 \_ x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) enthält eine Liste der verfügbaren Anweisungen.
-   [Ps \_ 2 \_ x Register listet](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) die verschiedenen Typen von Registern auf, die vom Vertex-Shader ALU verwendet werden.
-   [Modifizierer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Werden verwendet, um die Art und Weise zu ändern, wie eine Anweisung funktioniert.
-   [Die Zielregister-Schreibmaske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.
-   [Registermodifizierer für Pixel-Shaderquellen](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Source Register Swizzling bietet](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.

## <a name="dynamic-flow-control"></a>Dynamisches Flow-Steuerelement

[**DynamicFlowControlDepth stellt**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) die Schachtelungstiefe dynamischer Flusssteuerungsanweisungen [dar:](if-bool---ps.md)wenn , wenn [ \_ comp](if-comp---ps.md), wenn vor , break [- ps](break---ps.md)und [break comp - \_ ps](break-comp---ps.md). [ \_](if-pred---ps.md) Der Wert entspricht der Schachtelungstiefe des if \_ comp-Blocks. Wenn diese Obergrenze 0 ist, unterstützt das Gerät keine Anweisungen zur dynamischen Flusssteuerung.

## <a name="number-of-temporary-registers"></a>Anzahl temporärer Register

Die Anzahl temporärer Register, die vom Gerät unterstützt werden. Der Bereich liegt zwischen 12 und 32.

## <a name="static-flow-control-nesting-depth"></a>Statische Flow Steuerelement-Schachtelungstiefe

[**StaticFlowControlDepth stellt**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) die Schachtelungstiefe von zwei Typen statischer Flusssteuerungsanweisungen dar: [loop](loop---ps.md)  / [rep](rep---ps.md) und [](call---ps.md)  / [callnz](callnz-bool---ps.md). loop /rep-Anweisungen können bis in die **Tiefe von StaticFlowControlDepth geschachtelt** werden. Unabhängig können Die /callnz-Anweisungen in eine Tiefe von **StaticFlowControlDepth geschachtelt** werden.

## <a name="number-of-instruction-slots"></a>Anzahl der Anweisungsslots

Die Anzahl der Anweisungsslots kann zwischen 96 und maximal 512 liegen und wird von [**MaxPixelShaderInstructionSlots angegeben.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) Die Gesamtanzahl der Anweisungen, die ausgeführt werden können, wird durch **MaxPixelShaderInstructionsExecuted definiert.** Dies kann aufgrund von Schleifen- und Unterroutinenaufrufen größer als die Anzahl der Anweisungsslots sein.

## <a name="arbitrary-swizzle"></a>Beliebiger Swizzle

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird beliebiges Swizzle unterstützt. Siehe [Quellregister Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Anweisungen zum Farbverlauf

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, werden Farbverlaufsanweisungen unterstützt. Siehe [dsx – ps](dsx---ps.md), [dsy – ps](dsy---ps.md)und [texldd – ps](texldd---ps.md).

## <a name="predication"></a>Prädikation

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird die Anweisungsvordication unterstützt. Weitere Informationen [finden Sie unter Prädikatregister.](dx9-graphics-reference-asm-ps-registers-predicate.md)

## <a name="dependent-read-limit"></a>Abhängiger Lesegrenzwert

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine abhängigen Lesegrenzwerte.

## <a name="texture-instruction-limit"></a>Texturanweisungslimit

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine Beschränkung für Texturanweisungen.

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Texturs sampler beträgt 16.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 
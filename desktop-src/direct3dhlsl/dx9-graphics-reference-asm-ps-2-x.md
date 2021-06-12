---
title: ps_2_x
description: Erfahren Sie mehr über ps_2_x, einen programmierbaren Pixelshader, der aus einer Reihe von Anweisungen besteht, die mit Pixeldaten arbeiten.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9efedc6011cb63b6465fd2d3ced4a7807c09f4da
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010873"
---
# <a name="ps_2_x"></a>ps \_ 2 \_ x

Ein programmierbarer Pixel-Shader besteht aus einer Reihe von Anweisungen, die mit Pixeldaten arbeiten. Registriert Datenübertragungen in und aus der ALU. Es kann ein zusätzliches Steuerelement angewendet werden, um die Anweisung, die Ergebnisse oder die geschriebenen Daten zu ändern.

-   [ps \_ 2 \_ x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) enthält eine Liste der verfügbaren Anweisungen.
-   [ps \_ 2 \_ x Registers listet](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) die verschiedenen Registertypen auf, die vom Vertex-Shader ALU verwendet werden.
-   [Modifizierer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Werden verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   [Zielregister-Schreibmaske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.
-   [Die Quellregistermodifizierer des Pixelshader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Das Quellenregister swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) bietet zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.

## <a name="dynamic-flow-control"></a>Dynamische Flusssteuerung

[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) stellt die Schachtelungstiefe dynamischer Ablaufsteuerungsanweisungen dar: [, wenn](if-bool---ps.md) [, wenn \_ comp](if-comp---ps.md), [wenn vor \_ ,](if-pred---ps.md) [break - ps](break---ps.md), und break comp - [ \_ ps](break-comp---ps.md). Der Wert entspricht der Schachtelungstiefe des if \_ comp-Blocks. Wenn diese Obergrenze 0 (null) ist, unterstützt das Gerät keine Anweisungen zur dynamischen Flusssteuerung.

## <a name="number-of-temporary-registers"></a>Anzahl temporärer Register

Die Anzahl der vom Gerät unterstützten temporären Register. Der Bereich liegt zwischen 12 und 32.

## <a name="static-flow-control-nesting-depth"></a>Schachtelungstiefe der statischen Flusssteuerung

[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) stellt die Schachtelungstiefe von zwei Typen statischer Ablaufsteuerungsanweisungen dar: [](loop---ps.md)  / [Schleifenreplik und](rep---ps.md) [Aufruf](call---ps.md)  / [von callnz](callnz-bool---ps.md). Schleifenanweisungen /rep können bis zu **StaticFlowControlDepth** deep geschachtelt werden. Unabhängig davon können Aufrufanweisungen von /callnz bis zu **StaticFlowControlDepth** deep geschachtelt werden.

## <a name="number-of-instruction-slots"></a>Anzahl der Anweisungsslots

Die Anzahl der Anweisungsslots kann zwischen 96 und maximal 512 liegen und wird von [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)angegeben. Die Gesamtzahl der Anweisungen, die ausgeführt werden können, wird von **MaxPixelShaderInstructionsExecuted** definiert. Dies kann aufgrund von Schleifen- und Unterroutinenaufrufen größer als die Anzahl der Anweisungsslots sein.

## <a name="arbitrary-swizzle"></a>Beliebiger Swizzle

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird beliebige Swizzle unterstützt. Weitere Informationen finden Sie [unter Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Farbverlaufsanweisungen

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, werden Farbverlaufsanweisungen unterstützt. Siehe [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)und [texldd - ps](texldd---ps.md).

## <a name="predication"></a>Prädikation

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, wird die Anweisungsprädikation unterstützt. Weitere Informationen finden Sie unter [Prädikatregister.](dx9-graphics-reference-asm-ps-registers-predicate.md)

## <a name="dependent-read-limit"></a>Abhängiger Lesegrenzwert

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine abhängigen Lesegrenzwerte.

## <a name="texture-instruction-limit"></a>Grenzwert für Texturanweisung

Wenn [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) festgelegt ist, gibt es keine Beschränkung für Texturanweisungen.

## <a name="sampler-count"></a>Sampleranzahl

Die Anzahl der verfügbaren Textur-Sampler beträgt 16.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 
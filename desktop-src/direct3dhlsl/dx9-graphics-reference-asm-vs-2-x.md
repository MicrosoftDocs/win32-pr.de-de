---
title: vs_2_x
description: Erfahren Sie vs_2_x, einen programmierbaren Vertex-Shader, der aus einer Reihe von Anweisungen besteht, die mit Scheitelpunktdaten arbeiten.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3449ae4c1e1eb3b977916f6fb1d19303e9d21a4e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010714"
---
# <a name="vs_2_x"></a>Vs. \_ 2 \_ x

Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die mit Scheitelpunktdaten arbeiten. Registriert Übertragungsdaten in und aus der ALU. Zusätzliche Steuerung kann angewendet werden, um die Anweisung, die Ergebnisse oder die ausgeschriebenen Daten zu ändern.

Vertex-Shaderversion im Vergleich zu 2 x erweitert den von unterstützten Funktionssatz im Vergleich \_ \_ zu \_ 2 \_ 0. Jedes zusätzliche Feature wird durch eine entsprechende Obergrenze in der [**D3DCAPS9-Struktur**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) in [D3DVS20CAPS dargestellt.](/windows/desktop/direct3d9/d3dvs20caps) Um eines der erweiterten Features zu verwenden, die durch diese Obergrenzen dargestellt werden, muss die Vertex-Shaderversion im Vergleich zu \_ 2 x angegeben \_ werden.

-   [Anweisungen im Vergleich \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) enthält eine Liste der verfügbaren Anweisungen.
-   [Register: Im Vergleich \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) werden die verschiedenen Registertypen aufgeführt, die von der Vertex-Shader-ALU verwendet werden.
-   [Vertex-Shader-Registermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Art und Weise zu ändern, wie eine Anweisung funktioniert.
-   [Vertex-Shader-Quellregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Source Register Swizzling bietet](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.
-   [Zielregistermaskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.

## <a name="new-features"></a>Neue Funktionen

Die neuen Features lauten wie folgt:

### <a name="dynamic-flow-control"></a>Dynamische Flusssteuerung

Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0 ist, werden die folgenden Anweisungen zur dynamischen Flusssteuerung unterstützt:

-   [if \_ comp – vs](if-comp---vs.md)
-   [break – vs](break---vs.md)
-   [break \_ comp – vs](break-comp---vs.md)

Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) ebenfalls festgelegt ist, werden die folgenden zusätzlichen Anweisungen zur Flusssteuerung unterstützt:

-   [setp \_ comp – vs](setp-comp---vs.md)
-   [if pred – vs](if-pred---vs.md)
-   [callnz pred – vs](callnz-pred---vs.md)
-   [Breakp im Vergleich zu](breakp---vs.md)

Der Wertebereich für die dynamische Flusssteuerungstiefe beträgt 0 bis 24 und entspricht der Schachtelungstiefe der Anweisungen für die dynamische Flusssteuerung (weitere Informationen finden Sie unter [Grenzwerte](dx9-graphics-reference-asm-vs-instructions-flow-control.md) für die Flusssteuerungsschachtelung). Wenn diese Obergrenze 0 ist, unterstützt das Gerät keine Anweisungen zur dynamischen Flusssteuerung.

### <a name="number-of-temporary-registers"></a>Anzahl temporärer Register

[D3DVS20CAPS stellt](/windows/desktop/direct3d9/d3dvs20caps) die Anzahl der temporären [Register](dx9-graphics-reference-asm-vs-registers-temporary.md)dar, die vom Gerät unterstützt werden. Der Wertebereich für diese Obergrenze beträgt 12 bis 32.

### <a name="static-flow-control-nesting-depth"></a>Schachtelungstiefe der statischen Flusssteuerung

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) stellt die Schachtelungstiefe von zwei Typen statischer Flusssteuerungsanweisungen dar: loop [– vs](loop---vs.md)rep – vs und call – vs callnz bool – vs if bool – vs . loop – vs/rep – vs instructions can be nested up to D3DVS20CAPS deep (Vs. bool – vs. loop – vs/rep – vs. Anweisungen können bis / [](rep---vs.md) zu [](call---vs.md) / [](callnz-bool---vs.md) / [](if-bool---vs.md)D3DVS20CAPS tief geschachtelt werden). Unabhängig können aufrufe – vs/callnz bool – vs instructions bis zu D3DVS20CAPS deep geschachtelt werden. Wenn D3DVS20CAPS ebenfalls festgelegt ist, wird [callnz pred - vs](callnz-pred---vs.md) zur Schachtelungstiefe des Aufrufs gezählt – vs/callnz bool – vs/if bool – vs (details finden Sie unter [Grenzwerte](dx9-graphics-reference-asm-vs-instructions-flow-control.md) für die Flusssteuerungsschachtelung).

### <a name="predication"></a>Prädikation

Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) festgelegt ist, unterstützt das Gerät [setp \_ comp - vs](setp-comp---vs.md) and instruction predication. Wenn D3DVS20CAPS ebenfalls größer als 0 ist, werden die folgenden zusätzlichen Anweisungen zur dynamischen Flusssteuerung unterstützt:

-   [if pred – vs](if-pred---vs.md)
-   [callnz pred – vs](callnz-pred---vs.md)
-   [Breakp im Vergleich zu](breakp---vs.md)

### <a name="instruction-count"></a>Anweisungsanzahl

Für jeden Vertex-Shader können bis zu 256 Anweisungen gespeichert sein. Die Anzahl der ausgeführten Anweisungen kann viel höher sein (aufgrund der Unterstützung von Schleifen/Wiederholungen) und ist durch [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)begrenzt, was mindestens 0xFFFF.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
---
title: vs_2_x
description: Erfahren Sie mehr über vs_2_x, einen programmierbaren Vertex-Shader, der aus einer Reihe von Anweisungen besteht, die mit Scheitelpunktdaten arbeiten.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a412c7980ef12bfd8814933cd9d3de07db27fac353a636406e96e1377cd57829
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023970"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die mit Scheitelpunktdaten arbeiten. Registriert Datenübertragungen in und aus der ALU. Es kann ein zusätzliches Steuerelement angewendet werden, um die Anweisung, die Ergebnisse oder die geschriebenen Daten zu ändern.

Die Vertex-Shaderversion im Vergleich zu \_ 2 \_ x erweitert den Von \_ vs. 2 0 unterstützten \_ Featuresatz. Jedes zusätzliche Feature wird durch eine entsprechende Obergrenze in der [**D3DCAPS9-Struktur**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) in [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps)dargestellt. Um eines der erweiterten Features zu verwenden, die durch diese Obergrenzen dargestellt werden, muss die Vertex-Shaderversion als vs 2 x angegeben \_ \_ werden.

-   [Anweisungen im Vergleich zu \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) enthält eine Liste der verfügbaren Anweisungen.
-   [Register : Im Vergleich zu \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) werden die verschiedenen Registertypen aufgelistet, die von der Vertex-Shader-ALU verwendet werden.
-   [Vertex-Shaderregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   [Vertex-Shader-Quellregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Das Quellenregister swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) bietet zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.
-   [Die Zielregistermaskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.

## <a name="new-features"></a>Neue Funktionen

Neue Features sind wie folgt:

### <a name="dynamic-flow-control"></a>Dynamisches Flow-Steuerelement

Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0 ist, werden die folgenden Anweisungen zur dynamischen Flusssteuerung unterstützt:

-   [if \_ comp - vs](if-comp---vs.md)
-   [break – im Vergleich zu](break---vs.md)
-   [break \_ comp – vs](break-comp---vs.md)

Wenn [auch D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) festgelegt ist, werden die folgenden zusätzlichen Anweisungen zur Flusssteuerung unterstützt:

-   [setp \_ comp – vs](setp-comp---vs.md)
-   [if pred – vs](if-pred---vs.md)
-   [callnz pred – vs](callnz-pred---vs.md)
-   [breakp – im Vergleich zu](breakp---vs.md)

Der Wertebereich für die dynamische Flusssteuerungstiefe beträgt 0 bis 24 und entspricht der Schachtelungstiefe der Anweisungen für die dynamische Flusssteuerung (weitere Informationen finden [Sie unter Flow Control Nesting Limits (Schachtelungsgrenzwerte](dx9-graphics-reference-asm-vs-instructions-flow-control.md) für Die Steuerung). Wenn diese Obergrenze 0 (null) ist, unterstützt das Gerät keine Anweisungen zur dynamischen Flusssteuerung.

### <a name="number-of-temporary-registers"></a>Anzahl temporärer Register

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) stellt die Anzahl der vom Gerät unterstützten [temporären Register](dx9-graphics-reference-asm-vs-registers-temporary.md)dar. Der Wertebereich für diese Obergrenze beträgt 12 bis 32.

### <a name="static-flow-control-nesting-depth"></a>Schachtelungstiefe des statischen Flow-Steuerelements

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) stellt die Schachtelungstiefe von zwei Typen statischer Flusssteuerungsanweisungen dar: [loop - vs](loop---vs.md)rep - / [vs](rep---vs.md) and call - [vs](call---vs.md) / [callnz bool - vs](callnz-bool---vs.md)if / [bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions kann bis zu D3DVS20CAPS deep geschachtelt werden. Unabhängig voneinander können Aufrufe – vs/callnz bool – vs Instructions bis zu D3DVS20CAPS deep geschachtelt werden. Wenn auch D3DVS20CAPS festgelegt ist, wird [callnz pred – vs](callnz-pred---vs.md) in die Schachtelungstiefe des Aufrufs gezählt – vs/callnz bool – vs/if bool – vs (weitere Informationen finden Sie unter Flow Steuern von [Schachtelungsgrenzwerten).](dx9-graphics-reference-asm-vs-instructions-flow-control.md)

### <a name="predication"></a>Prädikation

Wenn [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) festgelegt ist, unterstützt das Gerät [setp \_ comp - vs](setp-comp---vs.md) und instruction predication. Wenn D3DVS20CAPS ebenfalls größer als 0 ist, werden die folgenden zusätzlichen Anweisungen zur dynamischen Flusssteuerung unterstützt:

-   [if pred – vs](if-pred---vs.md)
-   [callnz pred – vs](callnz-pred---vs.md)
-   [breakp – im Vergleich zu](breakp---vs.md)

### <a name="instruction-count"></a>Anweisungsanzahl

Jeder Vertex-Shader kann bis zu 256 Anweisungen speichern. Die Anzahl der ausgeführten Anweisungen kann (aufgrund der Unterstützung von Schleifen/Wiederholungen) deutlich höher sein und ist durch [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)begrenzt, das mindestens 0xFFFF sein sollte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
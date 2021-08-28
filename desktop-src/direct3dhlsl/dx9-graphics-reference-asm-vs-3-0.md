---
title: vs_3_0
description: Erfahren Sie vs_3_0, einem programmierbaren Vertex-Shader, der aus einer Reihe von Anweisungen besteht, die mit Scheitelpunktdaten arbeiten.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd10f6d726118679f395f01714233c7096fd5189
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476416"
---
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die mit Scheitelpunktdaten arbeiten. Registriert Übertragungsdaten in und aus der ALU. Zusätzliche Steuerung kann angewendet werden, um die Anweisung, die Ergebnisse oder die ausgeschriebenen Daten zu ändern.

Vertex-Shaderversion im Vergleich zu 3 0 erweitert den von \_ \_ unterstützten Funktionssatz im Vergleich zu \_ 2 \_ x. Jedes der Features in im Vergleich zu 2 X, für das eine Obergrenze festgelegt werden muss, ist in im Vergleich \_ zu 3 0 verfügbar, \_ ohne dass die Obergrenze erforderlich \_ \_ ist.

-   [Anweisungen im Vergleich \_ zu \_ 3 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) enthält eine Liste der verfügbaren Anweisungen.
-   [Register: Im Vergleich \_ zu 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) werden die verschiedenen Typen von Registern aufgeführt, die vom Vertex-Shader ALU verwendet werden.
-   [Vertex-Shader-Registermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Art und Weise zu ändern, wie eine Anweisung funktioniert.
-   [Vertex-Shader-Quellregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Source Register Swizzling bietet](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.
-   [Zielregistermaskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.

## <a name="new-features"></a>Neue Funktionen

Neue Features der Vertex-Shaderversion im Vergleich \_ zu 3 \_ 0 sind in den folgenden Abschnitten aufgeführt.

### <a name="indexing-registers"></a>Indizieren von Registern

In den früheren Shadermodellen konnte nur die konstante Registerbank indiziert werden. In diesem Modell können die folgenden Registerbanken mithilfe des Schleifenzählerregisters (Loop Counter Register, aL) indiziert werden:

-   Eingaberegister (v \# )
-   Ausgaberegister (o \# )

### <a name="vertex-textures"></a>Scheitelpunkttexturen

Dieses Shadermodell unterstützt die Textursuche im Vertex-Shader mit texldl. Die Scheitelpunkt-Engine verfügt über vier Texturs sampler-Phasen (im Unterschied zum Verschiebungszuordnungs-Sampler und den Texturs samplern in der Pixel-Engine), die zum Abtasten von Texturen verwendet werden können, die in diesen Phasen festgelegt wurden. Weitere [Informationen finden Sie unter Vertextexturen in \_ vs. \_ 3 0 (DirectX HLSL).](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)

### <a name="vertex-stream-frequency"></a>Vertexstreamhäufigkeit

Mit diesem Feature kann eine Teilmenge der Eingaberegister mit einer anderen Rate als einmal pro Scheitelpunkt initialisiert werden. Weitere Informationen [finden Sie unter Zeichnen von nicht indizierter Geometrie.](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)

### <a name="shader-output"></a>Shaderausgabe

Ähnlich wie bei 2 0 kann die Ausgabe des Shaders bei der statischen \_ \_ Flusssteuerung variieren. Seien Sie vorsichtig bei dynamischen Verzweigungen, da dies dazu führen kann, dass shader-Ausgaben pro Scheitelpunkt variieren. Dies führt zu unvorhersehbaren Ergebnissen auf unterschiedlicher Hardware.

### <a name="dynamic-flow-control"></a>Dynamische Flusssteuerung

Alle Anweisungen zur dynamischen Flusssteuerung werden unterstützt. Der maximal zulässige Wert für die Schachtelungstiefe beträgt 24. (Weitere [Informationen finden Flow unter Steuern von Schachtelungsgrenzwerten.)](dx9-graphics-reference-asm-vs-instructions-flow-control.md)

### <a name="temporary-registers"></a>Temporäre Register

Insgesamt werden 32 temporäre Register (r \# ) unterstützt.

### <a name="static-flow-control"></a>Statisches Flow-Steuerelement

Die maximale Schachtelungstiefe für [die Schleife im Vergleich zu](loop---vs.md)rep / [beträgt](rep---vs.md) 4. Die maximale Schachtelungstiefe für [aufruf – vs](call---vs.md) / [callnz bool – vs](callnz-bool---vs.md) / [callnz pred – vs](callnz-pred---vs.md) is 4. Bei [bool im Vergleich zu ist](if-bool---vs.md)der maximal zulässige Wert für die Schachtelungstiefe 24. (Weitere [Informationen finden Flow unter Steuern von Schachtelungsgrenzwerten.)](dx9-graphics-reference-asm-vs-instructions-flow-control.md)

### <a name="predication"></a>Prädikation

Anweisungsvordication wird unterstützt. Verwenden [Sie setp \_ comp im Vergleich zum](setp-comp---vs.md) Festlegen des Prädikatregisters.

### <a name="instruction-count"></a>Anweisungsanzahl

Jeder Vertexshader ist zwischen 512 und der Anzahl von Slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9 zulässig.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) Die Anzahl der ausgeführten Anweisungen kann aufgrund der Unterstützung von Schleifen/Wiederholungen deutlich höher sein. Dies wird jedoch durch MaxVShaderInstructionsExecuted in D3DCAPS9 begrenzt, das mindestens 0xFFFF.

### <a name="device-caps"></a>Geräteobergrenze

Wenn Vertex-Shader 3 0 unterstützt wird, werden die folgenden Obergrenzen \_ in der Hardware unterstützt (mindestens):




| Cap | Funktion | 
|-----|------------|
| Shader-Obergrenzen | <ul><li>DynamicFlowControlDepth ist 24</li><li>NumTemps ist 32</li><li>StaticFlowControlDepth ist 4</li><li>Prädication wird unterstützt.</li></ul> | 
| GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom | 8 KB | 
| VertexShaderVersion | 3_0 | 
| MaxVertexShaderConst | 256 | 
| MaxVertexShader30InstructionSlots | 512 | 
| Support für 50000 | D3DPRASTERCAPS_FOGVERTEX | 
| VertexTextureFilterCaps | <ul><li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li><li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li></ul> | 
| <a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a> | Scheitelpunktelemente in einer Scheitelpunktdeklaration können denselben Streamoffset gemeinsam haben. | 
| Vertexformate | <ul><li>D3DDECLTYPE_UBYTE4</li><li>D3DDECLTYPE_UBYTE4N</li><li>D3DDECLTYPE_SHORT2N</li><li>D3DDECLTYPE_SHORT4N</li><li>D3DDECLTYPE_FLOAT16_2</li><li>D3DDECLTYPE_FLOAT16_4</li></ul> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 

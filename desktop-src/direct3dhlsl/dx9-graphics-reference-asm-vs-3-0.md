---
title: vs_3_0
description: Erfahren Sie mehr über vs_3_0, einen programmierbaren Vertex-Shader, der aus einer Reihe von Anweisungen besteht, die mit Scheitelpunktdaten arbeiten.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 310d64170280053c34766f214969f78d66560ea3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011073"
---
# <a name="vs_3_0"></a>Vs \_ 3 \_ 0

Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunktdaten ausgeführt werden. Registriert Datenübertragungen in und aus der ALU. Es kann ein zusätzliches Steuerelement angewendet werden, um die Anweisung, die Ergebnisse oder die geschriebenen Daten zu ändern.

Die Vertex-Shaderversion im Vergleich \_ zu 3 \_ 0 erweitert den Featuresatz, der von und 2 x unterstützt \_ \_ wird. Jedes der Features in vs \_ 2 \_ X, für die eine Obergrenze festgelegt werden muss, ist in \_ Vs. 3 \_ 0 verfügbar, ohne dass die Obergrenze erforderlich ist.

-   [Anweisungen im Vergleich zu \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) enthält eine Liste der verfügbaren Anweisungen.
-   [Register : Im Vergleich zu \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) werden die verschiedenen Registertypen aufgelistet, die von der Vertex-Shader-ALU verwendet werden.
-   [Vertex-Shaderregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   [Vertex-Shader-Quellregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.
-   [Das Quellenregister swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) bietet zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.
-   [Die Zielregistermaskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.

## <a name="new-features"></a>Neue Funktionen

Neue Features der Vertex-Shaderversion im Vergleich zu \_ Version \_ 3 0 sind in den folgenden Abschnitten aufgeführt.

### <a name="indexing-registers"></a>Indizierungsregister

In den früheren Shadermodellen konnte nur die konstante Registerbank indiziert werden. In diesem Modell können die folgenden Registerbanken mithilfe des Schleifenzählerregisters (Loop Counter Register, aL) indiziert werden:

-   Eingaberegister (v \# )
-   Ausgaberegister (o \# )

### <a name="vertex-textures"></a>Scheitelpunkttexturen

Dieses Shadermodell unterstützt die Textursuche im Vertex-Shader mithilfe von Texldl. Die Vertex-Engine verfügt über vier Textur-Samplerstufen (die sich von der Verschiebungszuordnungs-Sampler und den Textur-Samplern in der Pixel-Engine unterscheiden), die zum Abtasten von Texturen verwendet werden können, die in diesen Phasen festgelegt sind. Siehe [Vertextexturen in vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).

### <a name="vertex-stream-frequency"></a>Vertexstreamfrequenz

Mit diesem Feature kann eine Teilmenge der Eingaberegister mit einer anderen Rate als einmal pro Scheitelpunkt initialisiert werden. Weitere Informationen finden Sie unter [Zeichnen einer nicht indizierten Geometrie.](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)

### <a name="shader-output"></a>Shaderausgabe

Ähnlich wie bei \_ 2 \_ 0 kann die Ausgabe des Shaders mit der statischen Flusssteuerung variieren. Seien Sie vorsichtig bei der dynamischen Verzweigung, da dies dazu führen kann, dass shader-Ausgaben pro Scheitelpunkt variieren. Dies führt zu unvorhersehbaren Ergebnissen auf unterschiedlichen Hardwarekomponenten.

### <a name="dynamic-flow-control"></a>Dynamische Flusssteuerung

Alle Anweisungen zur dynamischen Flusssteuerung werden unterstützt. Der maximal zulässige Schachtelungstiefewert ist 24. (Weitere Informationen finden Sie unter [Schachtelungsgrenzwerte](dx9-graphics-reference-asm-vs-instructions-flow-control.md) für die Flusssteuerung.)

### <a name="temporary-registers"></a>Temporäre Register

Insgesamt werden 32 temporäre Register \# (r) unterstützt.

### <a name="static-flow-control"></a>Statische Flusssteuerung

Die maximale Schachtelungstiefe für [die Schleife – im Vergleich zu](loop---vs.md)rep – im Vergleich / [zu](rep---vs.md) 4. Die maximale Schachtelungstiefe für [call - vs](call---vs.md) / [callnz bool - vs](callnz-bool---vs.md) / [callnz pred - vs](callnz-pred---vs.md) ist 4. Bei [bool – im Vergleich](if-bool---vs.md)zu – ist der maximal zulässige Schachtelungstiefewert 24. (Weitere Informationen finden Sie unter [Schachtelungsgrenzwerte](dx9-graphics-reference-asm-vs-instructions-flow-control.md) für die Flusssteuerung.)

### <a name="predication"></a>Prädikation

Anweisungsprädikation wird unterstützt. Verwenden Sie [setp \_ comp - vs](setp-comp---vs.md) , um das Prädikatregister festzulegen.

### <a name="instruction-count"></a>Anweisungsanzahl

Jeder Vertexshader ist überall von 512 bis zur Anzahl der Slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)zulässig. Die Anzahl der ausgeführten Anweisungen kann aufgrund der Schleifen-/Rep-Unterstützung deutlich höher sein. Dies ist jedoch durch MaxVShaderInstructionsExecuted in D3DCAPS9 begrenzt, das mindestens 0xFFFF sein sollte.

### <a name="device-caps"></a>Geräteobergrenzen

Wenn Vertex-Shader 3 \_ 0 unterstützt wird, werden die folgenden Obergrenzen (mindestens) in der Hardware unterstützt:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Cap</th>
<th>Funktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Shader-Kapselungen</td>
<td><ul>
<li>DynamicFlowControlDepth ist 24</li>
<li>NumTemps ist 32</li>
<li>StaticFlowControlDepth ist 4</li>
<li>Prädikation wird unterstützt.</li>
</ul></td>
</tr>
<tr class="even">
<td>GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</td>
<td>8 KB</td>
</tr>
<tr class="odd">
<td>VertexShaderVersion</td>
<td>3_0</td>
</tr>
<tr class="even">
<td>MaxVertexShaderConst</td>
<td>256</td>
</tr>
<tr class="odd">
<td>MaxVertexShader30InstructionSlots</td>
<td>512</td>
</tr>
<tr class="even">
<td>Unterstützung für Diess</td>
<td>D3DPRASTERCAPS_FOGVERTEX</td>
</tr>
<tr class="odd">
<td>VertexTextureFilterCaps</td>
<td><ul>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></td>
<td>Vertexelemente in einer Scheitelpunktdeklaration können denselben Datenstromoffset gemeinsam nutzen.</td>
</tr>
<tr class="odd">
<td>Vertexformate</td>
<td><ul>
<li>D3DDECLTYPE_UBYTE4</li>
<li>D3DDECLTYPE_UBYTE4N</li>
<li>D3DDECLTYPE_SHORT2N</li>
<li>D3DDECLTYPE_SHORT4N</li>
<li>D3DDECLTYPE_FLOAT16_2</li>
<li>D3DDECLTYPE_FLOAT16_4</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
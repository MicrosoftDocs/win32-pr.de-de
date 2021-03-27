---
title: vs_3_0
description: Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22a0e6e84aff34dcec44713dc4382e391ad05c2b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103858528"
---
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.

Die Vertex-Shader-Version vs \_ 3 \_ 0 erweitert den von vs \_ 2 x unterstützten Funktions Satz \_ . Alle Features in vs \_ 2 X, \_ für die eine Obergrenze festgelegt werden muss, sind in vs \_ 3 \_ 0 verfügbar, ohne dass die Obergrenze erforderlich ist.

-   [Anweisungen: vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) enthält eine Liste der verfügbaren Anweisungen.
-   [Register-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) listet die verschiedenen Register Typen auf, die von Vertex Shader Alu verwendet werden.
-   [Vertex-Shader-registermodifiziererer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Funktionsweise einer Anweisung zu ändern.
-   [Vertex-Shader-Quell Registrierungs Modifizierers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.
-   Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.
-   Die [Ziel Register Maskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.

## <a name="new-features"></a>Neue Funktionen

\_In den folgenden Abschnitten werden die neuen Features der Vertex-Shader-Version vs 3 \_ 0 aufgeführt.

### <a name="indexing-registers"></a>Indizieren von Registern

In den früheren shadermodellen konnte nur die Konstante Register Bank indiziert werden. In diesem Modell können die folgenden Register Banken indiziert werden, indem das Schleifen-Counter-Register (Al) verwendet wird:

-   Eingabe Register (v \# )
-   Ausgabe Register (o \# )

### <a name="vertex-textures"></a>Scheitelpunkt Texturen

Dieses Shader-Modell unterstützt die Textur Suche im Vertex-Shader mithilfe von texldl. Die Vertex-Engine verfügt über vier Textur Sampler-Phasen (die sich vom Verschiebungs Übersichts Sampler und den Textur Beispielen in der Pixel-Engine unterscheiden), die zum Beispiel für Texturen verwendet werden können, die in diesen Phasen festgelegt sind. Weitere Informationen finden Sie [unter Scheitelpunkt Texturen in vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).

### <a name="vertex-stream-frequency"></a>Vertexstreamhäufigkeit

Diese Funktion ermöglicht es, dass eine Teilmenge der Eingabe Register mit einer anderen Rate als einmal pro Scheitelpunkt initialisiert wird. Siehe [Zeichnen nicht indizierter Geometrie](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).

### <a name="shader-output"></a>Shader-Ausgabe

Ähnlich wie bei vs \_ 2 \_ 0 kann die Ausgabe des Shaders von der statischen Fluss Steuerung abweichen. Gehen Sie bei dynamischer Verzweigungen vorsichtig vor, da dies dazu führen kann, dass Shader-Ausgaben pro Scheitelpunkt variieren. Dies führt zu unvorhersehbaren Ergebnissen auf einer anderen Hardware.

### <a name="dynamic-flow-control"></a>Dynamische Fluss Steuerung

Alle Anweisungen zur dynamischen Fluss Steuerung werden unterstützt. Der maximal zulässige Wert für die Schachtelungs Tiefe ist 24. (Ausführliche Informationen finden Sie unter [Fluss Steuerungs](dx9-graphics-reference-asm-vs-instructions-flow-control.md) Schachtelungs Limits.)

### <a name="temporary-registers"></a>Temporäre Register

Insgesamt werden 32 temporäre Register (r \# ) unterstützt.

### <a name="static-flow-control"></a>Statische Fluss Steuerung

Die maximale Schachtelungs Tiefe für [Loop-vs](loop---vs.md) / [Rep-vs](rep---vs.md) ist 4. Die maximale Schachtelungs Tiefe für [Aufruf-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz pred-vs](callnz-pred---vs.md) ist 4. Bei [booleschen](if-bool---vs.md)Werten beträgt der Wert für die maximale Schachtelungs Tiefe 24. (Ausführliche Informationen finden Sie unter [Fluss Steuerungs](dx9-graphics-reference-asm-vs-instructions-flow-control.md) Schachtelungs Limits.)

### <a name="predication"></a>Prädikation

Das Anweisungs Prädikat wird unterstützt. Verwenden Sie [SETP \_ Comp-vs](setp-comp---vs.md) , um das Prädikat Register festzulegen.

### <a name="instruction-count"></a>Anweisungs Anzahl

Jeder Vertex-Shader ist von 512 bis zur Anzahl der Slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)zulässig. Die Anzahl der auszuwerenden Anweisungen kann aufgrund der Unterstützung für Schleifen/Rep sehr viel höher sein. Dies wird jedoch durch maxvshaderinstructionsexecuted in D3DCAPS9 begrenzt, das mindestens 0xFFFF betragen sollte.

### <a name="device-caps"></a>Geräte Obergrenzen

Wenn Vertex Shader 3 \_ 0 unterstützt wird, werden die folgenden Obergrenzen auf Hardware (minimal) unterstützt:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Decke</th>
<th>Funktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Shader-Caps</td>
<td><ul>
<li>Dynamicflowcontroltiefe ist 24</li>
<li>NumTemps ist 32</li>
<li>Staticflowcontroltiefe ist 4</li>
<li>Ein Prädikat wird unterstützt.</li>
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
<td>Maxvertexshaderkonstanten</td>
<td>256</td>
</tr>
<tr class="odd">
<td>MaxVertexShader30InstructionSlots</td>
<td>512</td>
</tr>
<tr class="even">
<td>Unterstützung für Nebel</td>
<td>D3DPRASTERCAPS_FOGVERTEX</td>
</tr>
<tr class="odd">
<td>Vertextexturefiltercaps</td>
<td><ul>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></td>
<td>Vertex-Elemente in einer Scheitelpunkt Deklaration können denselben Streamoffset gemeinsam verwenden.</td>
</tr>
<tr class="odd">
<td>Scheitelpunkt Formate</td>
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

 

 
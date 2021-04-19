---
title: Semantik
description: Eine Semantik ist eine Zeichenfolge, die an eine Shadereingabe oder -ausgabe angefügt ist und Informationen über die beabsichtigte Verwendung eines Parameters übermittelt.
ms.assetid: 6f5c504c-1940-4d1c-b594-a2132599376b
keywords:
- BINORMAL, Semantik (DirectX HLSL)
- BLENDINDICES, Semantik (DirectX HLSL)
- BLENDWEIGHT, Semantik (DirectX HLSL)
- COLOR, Semantik (DirectX HLSL)
- SEMANTIC, Semantics (DirectX HLSL)
- POSITIONT, Semantik (DirectX HLSL)
- PSIZE, Semantik (DirectX HLSL)
- TANGENT, Semantik (DirectX HLSL)
- TESSFACTOR, Semantik (DirectX HLSL)
- TEXCOORD, Semantik (DirectX HLSL)
- VFACE, Semantik (DirectX HLSL)
- VPOS, Semantik (DirectX HLSL)
- System-Value Semantik
- Systemwertsemantik
- ClipDistance, Semantik (DirectX HLSL)
- Abdeckung, Semantik (DirectX HLSL)
- CullDistance, Semantik (DirectX HLSL)
- Tiefe, Semantik (DirectX HLSL)
- InstanceID, Semantik (DirectX HLSL)
- IsFrontFace, Semantik (DirectX HLSL)
- Position, Semantik (DirectX HLSL)
- PrimitiveID, Semantik (DirectX HLSL)
- RenderTargetArrayIndex, Semantik (DirectX HLSL)
- Ziel, Semantik (DirectX HLSL)
- SampleIndex, semantics (DirectX HLSL)
- VertexID, Semantik (DirectX HLSL)
- ViewportArrayIndex, Semantik (DirectX HLSL)
- SV_ClipDistance, Semantik (DirectX HLSL)
- SV_CullDistance, Semantik (DirectX HLSL)
- SV_Depth, Semantik (DirectX HLSL)
- SV_DepthGreaterEqual, Semantik (DirectX HLSL)
- SV_DepthLessEqual, Semantik (DirectX HLSL)
- SV_IsFrontFace, Semantik (DirectX HLSL)
- SV_Position, Semantik (DirectX HLSL)
- SV_RenderTargetArrayIndex, Semantik (DirectX HLSL)
- SV_Target, Semantik (DirectX HLSL)
- SV_ViewportArrayIndex, Semantik (DirectX HLSL)
- SV_InstanceID, Semantik (DirectX HLSL)
- SV_PrimitiveID, Semantik (DirectX HLSL)
- SV_VertexID, Semantik (DirectX HLSL)
- SV_Coverage, Semantik (DirectX HLSL)
- SV_SampleIndex, Semantik (DirectX HLSL)
- SV_InnerCoverage, semanitcs (DirectX HLSL)
- SV_StencilRef, Semantik (DirectX HLSL)
- SV_GroupID, Semantik (DirectX HLSL)
- SV_GroupThreadID, Semantik (DirectX HLSL)
- SV_DispatchThreadID Semantik (DirectX HLSL)
- SV_GroupIndex, Semantik (DirectX HLSL)
- SV_OutputControlPointID, Semantik (DirectX HLSL)
- SV_TessFactor, Semantik (DirectX HLSL)
- SV_InsideTessFactor, Semantik (DirectX HLSL)
- SV_DomainLocation, Semantik (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8979b4e4842a4c84317b456802ed8f1beefea35
ms.sourcegitcommit: 1d3c59a7066a75facc0565027251cad1ca1dd9c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/18/2021
ms.locfileid: "107594165"
---
# <a name="semantics"></a>Semantik

Eine Semantik ist eine Zeichenfolge, die an eine Shadereingabe oder -ausgabe angefügt ist und Informationen über die beabsichtigte Verwendung eines Parameters übermittelt. Semantik ist für alle Variablen erforderlich, die zwischen Shaderstufen übergeben werden. Die Syntax zum Hinzufügen einer Semantik zu einer Shadervariablen ist hier dargestellt ([Variablensyntax (DirectX HLSL)](dx-graphics-hlsl-variable-syntax.md)).

Im Allgemeinen sind Daten, die zwischen Pipelinestufen übergeben werden, vollständig generisch und werden vom System nicht eindeutig interpretiert. Beliebige Semantik ist zulässig, die keine besondere Bedeutung haben. Parameter (in Direct3D 10 und höher), die diese spezielle Semantik enthalten, werden als [Systemwertsemantik](#system-value-semantics)bezeichnet.

## <a name="semantics-supported-in-direct3d-9-and-direct3d-10-and-later"></a>In Direct3D 9 und Direct3D 10 und höher unterstützte Semantik

Die folgenden Semantiktypen werden sowohl in Direct3D 9 als auch in Direct3D 10 und höher unterstützt.

- [Vertex-Shadersemantik](#vertex-shader-semantics)
- [Pixelschattensemantik](#pixel-shader-semantics)

### <a name="vertex-shader-semantics"></a>Vertex-Shadersemantik

Diese Semantik hat eine Bedeutung, wenn sie an einen Vertex-Shader-Parameter angefügt wird. Diese Semantik wird sowohl in Direct3D 9 als auch in Direct3D 10 und höher unterstützt.

| Eingabe | BESCHREIBUNG | Typ |
|-|-|-|
| BINORMAL \[ n\] | Binormal | float4 |
| BLENDINDICES \[ n\] | Indizes mischen | uint |
| BLENDWEIGHT \[ n\] | Mischungsgewichtungen | float |
| COLOR \[ n\] | Diffuse und speculare Farbe | float4 |
| NORMAL \[ n\] | Normaler Vektor | float4 |
| POSITION \[ n\] | Scheitelpunktposition im Objektbereich. | float4 |
| POSITIONT | Transformierte Scheitelpunktposition. | float4 |
| PSIZE \[ n\] | Punktgröße | float |
| TANGENT \[ n\] | Tangens | float4 |
| TEXCOORD \[ n\] | Texturkoordinaten | float4 |

| Output | BESCHREIBUNG | Typ |
|-|-|-|
| COLOR \[ n\] | Diffuse oder Glanzfarbe | float4 |
| Nebel | Scheitelpunkt-Scheitelpunkt | float |
| POSITION \[ n\] | Position eines Scheitelpunkts im homogenen Raum. Berechnen Sie die Position im Bildschirmbereich, indem Sie (x,y,z) durch w dividieren. Jeder Vertex-Shader muss einen Parameter mit dieser Semantik schreiben. | float4 |
| PSIZE | Punktgröße | float |
| TESSFACTOR \[ n\] | Mosaikfaktor | float |

`n` ist eine optionale ganze Zahl zwischen 0 und der Anzahl der unterstützten Ressourcen. Beispiel: POSITION0, TEXCOORD1 usw.

### <a name="pixel-shader-semantics"></a>Pixelshadersemantik

Diese Semantik hat eine Bedeutung, wenn sie an einen Pixel-Shader-Eingabeparameter angefügt wird. Diese Semantik wird sowohl in Direct3D 9 als auch in Direct3D 10 und höher unterstützt.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Eingabe</th>
<th>BESCHREIBUNG</th>
<th>Typ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COLOR[n]</td>
<td>Diffuse oder Glanzfarbe.</td>
<td>float4</td>
</tr>
<tr class="even">
<td>TEXCOORD[n]</td>
<td>Texturkoordinaten</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>VFACE</td>
<td>Gleitkommaskalar, der ein nach hinten gerichtetes Primitiv angibt. Ein negativer Wert wird rückwärts, während ein positiver Wert der Kamera gegenüber steht.
<blockquote>
[!Note]<br />
Diese Semantik ist in <a href="dx-graphics-hlsl-sm3.md">Direct3D 9 Shader Model 3.0 verfügbar.</a> Verwenden Sie für Direct3D 10 und höher stattdessen <a href="#semantics-supported-only-for-direct3d-10-and-newer">SV_IsFrontFace.</a>
</blockquote>
<br/></td>
<td>float</td>
</tr>
<tr class="even">
<td>VPOS</td>
<td>Die Pixelposition (x,y) im Bildschirmbereich. Informationen zum Konvertieren eines Direct3D 9-Shaders (der diese Semantik verwendet) in einen Direct3D 10- und höher-Shader finden Sie unter <a href="#direct3d-9-vpos-and-direct3d-10-sv_position">Direct3D 9 VPOS und Direct3D 10 SV_Position</a>)</td>
<td>float2</td>
</tr>
</tbody>
</table>

<table>
<th>Output</th>
<th>BESCHREIBUNG</th>
<th>Typ</th>
</tr>
<td>COLOR[n]</td>
<td>Ausgabefarbe</td>
<td>float4</td>
</tr>
<td>DEPTH[n]</td>
<td>Ausgabetiefe</td>
<td>float</td>
</tr>
</table>

`n` ist eine optionale ganze Zahl zwischen 0 und der Anzahl der unterstützten Ressourcen. Beispiel: PSIZE0, COLOR1 usw.

Die COLOR-Semantik ist nur im Shader-Kompatibilitätsmodus gültig (d. h., wenn der Shader mit D3D10 \_ SHADER \_ ENABLE \_ BACKWARDS COMPATIBILITY erstellt \_ wird).

## <a name="semantics-supported-only-for-direct3d-10-and-newer"></a>Semantik wird nur für Direct3D 10 und neuer unterstützt.

Die folgenden Semantiktypen wurden für Direct3D 10 neu eingeführt und sind für Direct3D 9 nicht verfügbar.

- [Systemwertsemantik](#system-value-semantics)

### <a name="system-value-semantics"></a>System-Value Semantik

Die Systemwertsemantik ist neu in Direct3D 10. Alle Systemwerte beginnen mit einem \_ SV-Präfix. Ein gängiges Beispiel ist SV \_ POSITION, das von der Rasterizerphase interpretiert wird. Die Systemwerte sind in anderen Teilen der Pipeline gültig. Die SV-Position kann z. B. \_ als Eingabe für einen Vertex-Shader sowie als Ausgabe angegeben werden. Pixel-Shader können nur in Parameter mit der \_ Systemwertsemantik SV Depth und SV \_ Target schreiben.

Andere Systemwerte (SV \_ VertexID, SV \_ InstanceID, SV \_ IsFrontFace) können nur in den ersten aktiven Shader in der Pipeline eingegeben werden, der den bestimmten Wert interpretieren kann. Danach muss die Shaderfunktion die Werte an nachfolgende Phasen übergeben.

SV PrimitiveID ist eine Ausnahme von dieser Regel, die nur in \_ den ersten aktiven Shader in der Pipeline eingegeben wird, der den bestimmten Wert interpretieren kann. Die Hardware kann den gleichen ID-Wert wie die Eingabe für die Phase des Hüllen-Shaders, den Domänen-Shader und nach der ersten aktivierten Stufe bereitstellen: geometry-shader stage oder pixel-shader stage.

Wenn das Mosaik aktiviert ist, sind die Stufen "hull-shader" und "domain-shader" vorhanden. Für einen bestimmten Patch gilt die gleiche PrimitiveID für den Hüllen-Shader-Aufruf des Patches und für alle Aufrufe des Domänen-Shaders mit Mosaik. Dieselbe PrimitiveID wird auch an die nächste aktive Phase weitergegeben. geometry-shader stage oder pixel-shader stage ,wenn aktiviert.

Wenn der geometry-Shader SV \_ PrimitiveID eingibt und weil er null oder mindestens einen Primitiven pro Aufruf ausgeben kann, muss der Shader eine eigene Auswahl des SV \_ PrimitiveID-Werts für jedes Primitive ausgeben, wenn ein nachfolgender Pixel-Shader SV \_ PrimtiveID eingibt.

Als weiteres Beispiel kann SV \_ PrimitiveID nicht von der Vertex-Shader-Stufe interpretiert werden, da ein Scheitelpunkt ein Member mehrerer Primitive sein kann.

Diese Semantik wurde Direct3D 10 hinzugefügt. Sie sind in Direct3D 9 nicht verfügbar.

Systemwertsemantik für die Rasterizerphase.

| System-Value Semantik | Beschreibung | Typ |
|-|-|-|
| SV \_ ClipDistance \[ n\] | Clipabstandsdaten. Bei SV ClipDistance-Werten wird jeweils davon ausgegangen, dass es sich um einen \_ Float32-Abstand zu einer Ebene handelt. Das primitive Setup ruft nur die Rasterung in Pixeln auf, für die die interpolierten Ebenenentfernungen >= 0 sind. Mehrere Clipebenen können gleichzeitig implementiert werden, indem mehrere Komponenten eines oder mehrerer Scheitelpunktelemente als SV \_ ClipDistance deklariert werden. Bei den kombinierten Clip- und CULL-Entfernungswerten handelt es sich bei den meisten D3D CLIP- ODER CULL DISTANCE COUNT-Komponenten in den meisten \# \_ \_ \_ \_ \_ D3D CLIP- ODER \# \_ \_ \_ CULL \_ DISTANCE ELEMENT \_ \_ COUNT-Registern. Verfügbar für alle Shader, in die gelesen oder geschrieben werden soll, mit Ausnahme des Vertex-Shaders, der den Wert schreiben, aber nicht als Eingabe verwenden kann.<br/> Das **Clipplanes-Attribut** funktioniert wie SV ClipDistance, funktioniert jedoch auf allen Hardwarefeatures der Ebene \_ 9 x und [](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) \_ höher. Weitere Informationen finden Sie unter User clip planes on feature level 9 hardware (Benutzeroberflächenebenen auf Hardware [auf Featureebene 9).](./user-clip-planes-on-10level9.md)<br/> | float |
| SV \_ CullDistance \[ n\] | Cull-Entfernungsdaten. Wenn Komponenten von Scheitelpunktelement(en) diese Bezeichnung erhalten, werden diese Werte jeweils als float32-Signierter Abstand zu einer Ebene angenommen. Primitive werden vollständig verworfen, wenn die Ebenenentfernung(en) für alle Scheitelungen im Primitiv 0 < ist. Mehrere CULL-Ebenen können gleichzeitig verwendet werden, indem mehrere Komponenten eines oder mehrerer Scheitelpunktelemente als SV \_ CullDistance deklariert werden. Bei den kombinierten Clip- und CULL-Entfernungswerten handelt es sich bei den meisten D3D CLIP- ODER CULL DISTANCE COUNT-Komponenten in den meisten \# \_ \_ \_ \_ \_ D3D CLIP- ODER \# \_ \_ \_ CULL \_ DISTANCE ELEMENT \_ \_ COUNT-Registern. Verfügbar für alle Shader, in die gelesen oder geschrieben werden soll, mit Ausnahme des Vertex-Shaders, der den Wert schreiben, aber nicht als Eingabe verwenden kann.<br/> | float |
| \_SV-Abdeckung | Eine Maske, die für Eingabe, Ausgabe oder beides eines Pixel-Shaders angegeben werden kann. <br/> Für SV \_ Coverage auf einem Pixel-Shader wird OUTPUT auf PS \_ 4 \_ 1 oder höher unterstützt. <br/> Für SV \_ Coverage auf einem Pixel-Shader erfordert INPUT ps \_ 5 \_ 0 oder höher. <br/> | uint |
| \_SV-Tiefe | Tiefenpufferdaten. Kann vom Pixel-Shader geschrieben werden. | float |
| SV \_ DepthGreaterEqual | In einem Pixel-Shader lässt die Ausgabetiefe zu, solange sie größer oder gleich dem vom Rasterizer festgelegten Wert ist. Ermöglicht das Anpassen der Tiefe, ohne das frühe Z zu deaktivieren. | float |
| SV \_ DepthLessEqual | In einem Pixel-Shader lässt die Ausgabetiefe zu, solange sie kleiner oder gleich dem vom Rasterizer festgelegten Wert ist. Ermöglicht das Anpassen der Tiefe, ohne das frühe Z zu deaktivieren. | float |
| [SV \_ DispatchThreadID](sv-dispatchthreadid.md) | Definiert den globalen Threadoffset innerhalb des Dispatch-Aufrufs pro Dimension der Gruppe. Verfügbar als Eingabe für den Compute-Shader. (schreibgeschützte) | uint3 |
| [SV \_ DomainLocation](sv-domainlocation.md) | Definiert den Speicherort auf der Hülle des aktuellen Domänenpunkts, der ausgewertet wird. Verfügbar als Eingabe für den Domänen-Shader. (schreibgeschützte) | float2 \| 3 |
| [SV \_ GroupID](sv-groupid.md) | Definiert den Gruppenoffset innerhalb eines Dispatchaufrufs pro Dimension des Dispatchaufrufs. Verfügbar als Eingabe für den Compute-Shader. (schreibgeschützt) | uint3 |
| [SV \_ GroupIndex](sv-groupindex.md) | Stellt einen flachen Index für einen angegebenen Thread innerhalb einer angegebenen Gruppe zur Verfügbar als Eingabe für den Compute-Shader. (schreibgeschützt) | uint |
| [SV \_ GroupThreadID](sv-groupthreadid.md) | Definiert den Threadoffset innerhalb der Gruppe pro Dimension der Gruppe. Verfügbar als Eingabe für den Compute-Shader. (schreibgeschützt) | uint3 |
| [SV \_ GSInstanceID](sv-gsinstanceid.md) | Definiert die Instanz des Geometrie-Shaders. Verfügbar als Eingabe für den Geometrie-Shader. Die -Instanz wird benötigt, da ein Geometrie-Shader bis zu 32-mal auf demselben Geometrieprimitiven aufgerufen werden kann. | uint |
| SV \_ InnerCoverage | Stellt verdeckte konservative Rasterungsinformationen dar (d. h., ob ein Pixel garantiert vollständig abgedeckt ist). Kann vom Pixel-Shader gelesen oder geschrieben werden. | |
| [SV \_ InsideTessFactor](sv-insidetessfactor.md) | Definiert die Mosaikmenge innerhalb einer Patchoberfläche. Verfügbar im Hüllen-Shader zum Schreiben und im Domänen-Shader zum Lesen. | float \| float \[ 2\] |
| SV \_ InstanceID | Bezeichner pro Instanz, der automatisch von der Laufzeit generiert wird (siehe [Using System-Generated Values (Direct3D 10) (Verwenden von System-Generated-Werten (Direct3D 10)).](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md) Verfügbar für alle Shader. | |
| SV \_ IsFrontFace | Gibt an, ob ein Dreieck nach vorne gerichtet ist. Für Linien und Punkte hat IsFrontFace den Wert true. Die Ausnahme sind Linien, die aus Dreiecken gezeichnet werden (Wireframe-Modus), wodurch IsFrontFace auf die gleiche Weise wie das Rastern des Dreiecks im Vollbildmodus festgelegt wird. Kann vom Geometry-Shader in geschrieben und vom Pixelshader gelesen werden. | bool |
| [SV \_ OutputControlPointID](sv-outputcontrolpointid.md) | Definiert den Index der Kontrollpunkt-ID, die durch einen Aufruf des Haupteinstiegspunkts des Hüllen-Shaders betrieben wird. Kann nur vom Hüllen-Shader gelesen werden. | uint |
| \_SV-Position | Wenn SV \_ Position für die Eingabe für einen Shader deklariert wird, kann einer von zwei Interpolationsmodi angegeben werden: linearNoPerspective oder linearNoPerspectiveCentroid, wobei letzteres bewirkt, dass beim Multisample-Antialiasing mithilfe von "centroid-snapped xyzw" Werte bereitgestellt werden. Bei Verwendung in einem Shader beschreibt SV \_ Position die Pixelposition. Verfügbar in allen Shadern, um die Pixelmitte mit einem Offset von 0,5 abzurufen. | float4 |
| SV \_ PrimitiveID | Bezeichner pro Primitiver, der automatisch von der Laufzeit generiert wird (siehe [Verwenden von System-Generated Values (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Kann von den Geometrie- oder Pixel-Shadern in geschrieben und von den Geometrie-, Pixel-, Hüllen- oder Domänen-Shadern gelesen werden. | uint |
| SV \_ RenderTargetArrayIndex | Renderzielarrayindex. Wird auf die Ausgabe des Geometrie-Shaders angewendet und gibt den Renderzielarrayslice an, auf den der Pixel-Shader den Primitiven ziehen wird. SV \_ RenderTargetArrayIndex ist nur gültig, wenn das Renderziel eine Arrayressource ist. Diese Semantik gilt nur für Primitive. Wenn ein Primitiver mehr als einen Scheitelpunkt hat, wird der Wert des führenden Scheitelpunkts verwendet. Dieser Wert gibt auch an, welcher Arrayslice einer Tiefen-/Schablonenansicht für Lese-/Schreibzwecke verwendet wird.<br/> Kann aus dem Geometrie-Shader geschrieben und vom Pixel-Shader gelesen werden.<br/> Wenn [D3D11_FEATURE_DATA_D3D11_OPTIONS3::VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) ist, wird `true` SV RenderTargetArrayIndex auf jeden Shader angewendet, der den Rasterizer \_ einfing. | uint |
| SV \_ SampleIndex | Beispielhäufigkeitsindexdaten. Verfügbar, um nur vom Pixel-Shader gelesen oder darauf geschrieben werden zu können. | uint |
| SV \_ StencilRef | Stellt den aktuellen Pixel-Shader-Schablonenverweiswert dar. Kann nur vom Pixel-Shader geschrieben werden. | uint |
| \_ \[ SV-Ziel n , wobei \] 0 <= n <= 7 | Der Ausgabewert, der in einem Renderziel gespeichert wird. Der Index gibt an, in welche der acht möglicherweise gebundenen Renderziele geschrieben werden soll. Der Wert ist für alle Shader verfügbar. | float \[ 2 \| 3 \| 4\] |
| [SV \_ TessFactor](sv-tessfactor.md) | Definiert die Mosaikmenge an jedem Rand eines Patches. Verfügbar zum Schreiben im Hüllen-Shader und zum Lesen im Domänen-Shader. | float \[ 2 \| 3 \| 4\] |
| SV \_ VertexID | Bezeichner pro Scheitelpunkt, der automatisch von der Laufzeit generiert wird (siehe [Using System-Generated Values (Direct3D 10) (Verwenden von System-Generated-Werten (Direct3D 10))](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Nur als Eingabe für den Vertex-Shader verfügbar. | uint |
| SV \_ ViewportArrayIndex | Viewportarrayindex. Wird auf die Geometry-Shaderausgabe angewendet und gibt an, welcher Viewport für den primitiven , der gerade geschrieben wird, verwendet werden soll. Kann vom Pixelshader gelesen werden. Das Primitiv wird transformiert und mit dem Viewport abgeschnitten, der vom Index angegeben wird, bevor er an den Rasterizer übergeben wird. Diese Semantik gilt nur für Primitive. Wenn ein Primitiver über mehr als einen Scheitelpunkt verfügt, wird der Wert des führenden Scheitelpunkts verwendet. <br/> Wenn [D3D11_FEATURE_DATA_D3D11_OPTIONS3::VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) `true` ist, wird SV \_ ViewportArrayIndex auf jeden Shader angewendet, der den Rasterizer einspeist. | uint |
| SV \_ ShadingRate | Definiert durch Schattierungsratenwerte die Anzahl der Pixel, die von einem Pixel-Shaderaufruf für Geräte mit [variabler Schattierungsrate (Ebene 2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) oder höher) geschrieben wurden. [](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate) Kann aus dem Pixelshader gelesen werden. Kann aus einem Scheitelpunkt- oder Geometrie-Shader geschrieben werden. | uint |

### <a name="limitations-when-writing-sv_depth"></a>Einschränkungen beim Schreiben von \_ SV-Tiefe:

- Wenn Multisampling (MultisampleEnable ist in [**D3D10 \_ RASTERIZER \_ DESC**](/windows/win32/api/d3d10/ns-d3d10-d3d10_rasterizer_desc) **true)** und ein Tiefenwert (mit einem Pixel-Shader) geschrieben wird, wird der einzelne wert auch im [Tiefentest](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md)verwendet. Daher geht die Möglichkeit zum Rendern primitiver Kanten mit höherer Auflösung verloren, wenn Multisampling durchgeführt wird.
- Wenn Sie die dynamische Flusssteuerung verwenden, ist es unmöglich, zur Kompilierzeit zu bestimmen, ob ein Shader, der SV Depth in einigen Pfaden schreibt, \_ bei jeder Ausführung garantiert \_ SV-Tiefe schreibt. Fehler beim Schreiben der \_ SV-Tiefe, wenn deklariert wird, führt zu einem nicht definierten Verhalten (das die Verwerfung des Pixels enthalten kann oder nicht).
- Jeder float32-Wert, einschließlich +/-INF und NaN, kann in SV Depth geschrieben \_ werden.
- Das Schreiben von \_ SV-Tiefe ist weiterhin gültig, wenn Dual Source Color Blending (Dual Source Color Blending) verwendet wird.

## <a name="migration-from-direct3d-9-to-direct3d-10-and-later"></a>Migration von Direct3D 9 zu Direct3D 10 und höher

Die folgenden Probleme sollten bei der Migration von Code von Direct3D 9 zu Direct3D 10 und höher berücksichtigt werden:

### <a name="mapping-to-direct3d-9-semantics"></a>Zuordnung zur Direct3D 9-Semantik

Einige der Semantik von Direct3D 10 und höher sind direkt der Direct3D 9-Semantik zuordnen.

| Direct3D 10-Semantik | Direct3D 9 Equivalent Semantic |
|-|-|
| \_SV-Tiefe | DEPTH |
| \_SV-Position | POSITION |
| \_SV-Ziel | COLOR |

> [!] Hinweis für Direct3D 9-Entwickler: Für Direct3D 9-Ziele muss die Shadersemantik einer gültigen Direct3D 9-Semantik zuordnen. Für die Abwärtskompatibilität wird POSITION0 (und seine Variantennamen) als \_ SV-Position behandelt, COLOR wird als SV \_ TARGET behandelt.

- [Zuordnung zur Direct3D 9-Semantik](#mapping-to-direct3d-9-semantics)
- [Direct3D 9 VPOS und Direct3D 10 SV \_ Position](#direct3d-9-vpos-and-direct3d-10-sv_position)
- [Benutzeroberflächen in HLSL](#user-clip-planes-in-hlsl)

### <a name="direct3d-9-vpos-and-direct3d-10-sv_position"></a>Direct3D 9 VPOS und Direct3D 10 SV \_ Position

Die semantische SV-Position D3D10 bietet ähnliche Funktionen wie die \_ Direct3D 9-Shadermodell 3-VPOS-Semantik. In Direct3D 9 wird beispielsweise die folgende Syntax für einen Pixel-Shader verwendet, der Bildschirmraumkoordinaten verwendet:

```HLSL
float4 psMainD3D9( float4 screenSpace : VPOS ) : COLOR
{
    // code here 
}
```

VPOS wurde für shader model 3-Unterstützung hinzugefügt, um Bildschirmraumkoordinaten anzugeben, da die POSITION-Semantik für Objektraumkoordinaten vorgesehen war.

In Direct3D 10 und höher gibt die SV-Positionssemantik (bei Verwendung im Kontext eines Pixel-Shaders) Bildschirmraumkoordinaten \_ an (Offset um 0,5). Daher wäre der Direct3D 9-Shader ungefähr gleichwertig (ohne 0,5 Offset) wie folgt:

```HLSL
float4 psMainD3D10( float4 screenSpace : SV_Position ) : COLOR
{
    // code here
}
```

Bei der Migration von Direct3D 9 zu Direct3D 10 und höher müssen Sie dies beachten, wenn Sie Ihre Shader übersetzen.

### <a name="user-clip-planes-in-hlsl"></a>Benutzerclipebenen in HLSL

Ab Windows 8 können Sie das **Clipplanes-Funktionsattribut** in einer HLSL-Funktionsdeklaration anstelle von SV ClipDistance verwenden, damit Ihr [](dx-graphics-hlsl-function-syntax.md) \_ Shader sowohl auf [Featureebene](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 x als auch auf \_ Featureebene 10 und höher funktioniert. Weitere Informationen finden Sie unter [User clip planes on feature level 9 hardware (Benutzer clip planes on feature level 9 hardware ( Benutzer clip planes on feature level 9 hardware](./user-clip-planes-on-10level9.md)).

## <a name="related-topics"></a>Verwandte Themen

* [Sprachsyntax](dx-graphics-hlsl-language-syntax.md)
* [Variablen (DirectX HLSL)](dx-graphics-hlsl-variables.md)

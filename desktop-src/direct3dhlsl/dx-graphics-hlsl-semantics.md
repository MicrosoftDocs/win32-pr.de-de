---
title: Semantik
description: Eine Semantik ist eine Zeichenfolge, die an eine Shadereingabe oder-Ausgabe angehängt ist, die Informationen über die beabsichtigte Verwendung eines Parameters überträgt.
ms.assetid: 6f5c504c-1940-4d1c-b594-a2132599376b
keywords:
- Binormal, Semantik (DirectX HLSL)
- Blendindices, Semantik (DirectX HLSL)
- Blendweight, Semantik (DirectX HLSL)
- Farbe, Semantik (DirectX HLSL)
- Nebel, Semantik (DirectX HLSL)
- Positiont, Semantik (DirectX HLSL)
- Psize, Semantik (DirectX HLSL)
- Tangens, Semantik (DirectX HLSL)
- Mosaik Faktor, Semantik (DirectX HLSL)
- Texcoord, Semantik (DirectX HLSL)
- Vface, Semantik (DirectX HLSL)
- Vpos, Semantik (DirectX HLSL)
- System-Value Semantik
- System Wert Semantik
- Clipdistance, Semantik (DirectX HLSL)
- Abdeckung, Semantik (DirectX HLSL)
- Culldistance, Semantik (DirectX HLSL)
- Tiefe, Semantik (DirectX HLSL)
- InstanceId, Semantik (DirectX HLSL)
- Isfrontface, Semantik (DirectX HLSL)
- Position, Semantik (DirectX HLSL)
- Primitiveid, Semantik (DirectX HLSL)
- Rendertargetarrayindex, Semantik (DirectX HLSL)
- Ziel, Semantik (DirectX HLSL)
- Sampleingedex, Semantik (DirectX HLSL)
- Vertexid, Semantik (DirectX HLSL)
- Viewportarrayindex, Semantik (DirectX HLSL)
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
ms.openlocfilehash: 510f718608363c547c8333279826cc8bac141358
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219055"
---
# <a name="semantics"></a>Semantik

Eine Semantik ist eine Zeichenfolge, die an eine Shadereingabe oder-Ausgabe angehängt ist, die Informationen über die beabsichtigte Verwendung eines Parameters überträgt. Die Semantik ist für alle Variablen erforderlich, die zwischen den shaderstufen weitergegeben werden. Die Syntax zum Hinzufügen einer Semantik zu einer shadervariablen wird hier dargestellt ([Variablen Syntax (DirectX HLSL)](dx-graphics-hlsl-variable-syntax.md)).

Im Allgemeinen sind die zwischen den Pipeline Stufen übergebenen Daten vollständig generisch und werden vom System nicht eindeutig interpretiert. eine beliebige Semantik ist zulässig, die keine besondere Bedeutung hat. Parameter (in Direct3D 10 und höher), die diese besondere Semantik enthalten, werden als [System-Wert-Semantik](#system-value-semantics)bezeichnet.

## <a name="semantics-supported-in-direct3d-9-and-direct3d-10-and-later"></a>In Direct3D 9 und Direct3D 10 und höher Unterstützte Semantik

Die folgenden Typen von Semantik werden in Direct3D 9 und Direct3D 10 und höher unterstützt.

- [Vertex-Shader-Semantik](#vertex-shader-semantics)
- [Pixel-Shader-Semantik](#pixel-shader-semantics)

### <a name="vertex-shader-semantics"></a>Vertex-Shader-Semantik

Diese Semantik hat eine Bedeutung, wenn Sie an einen Vertex-Shader-Parameter angefügt wird. Diese Semantik wird in Direct3D 9 und Direct3D 10 und höher unterstützt.

| Eingabe | BESCHREIBUNG | type |
|-|-|-|
| Binormal \[ n\] | Binormal | float4 |
| Blendindices \[ n\] | Blend-Indizes | uint |
| Blendweight \[ n\] | Blend-Gewichtungen | float |
| Farbe \[ n\] | Diffuses und Glanz Farbe | float4 |
| Normaler \[ n\] | Normaler Vektor | float4 |
| Position \[ n\] | Vertex-Position im Objektbereich. | float4 |
| Positiont | Transformierte Scheitelpunkt Position. | float4 |
| Psize \[ n\] | Punktgröße | float |
| Tangens \[ n\] | Tangens | float4 |
| Texkoord \[ n\] | Texturkoordinaten | float4 |
| Output | BESCHREIBUNG | type |
| Farbe \[ n\] | Diffuse oder Glanz Farbe | float4 |
| Neben | Scheitelpunkt Nebel | float |
| Position \[ n\] | Position eines Scheitel Punkts im homogenen Raum. Computeposition im Bildschirmbereich durch aufteilen (x, y, z) durch w. Jeder Vertex-Shader muss einen Parameter mit dieser Semantik schreiben. | float4 |
| PSIZE | Punktgröße | float |
| Mosaik Faktor \[ n\] | Mosaik Faktor | float |

`n` ist eine optionale ganze Zahl zwischen 0 und der Anzahl unterstützter Ressourcen. Beispielsweise POSITION0, TEXCOORD1 usw.

### <a name="pixel-shader-semantics"></a>Pixel-Shader-Semantik

Diese Semantik hat eine Bedeutung, wenn Sie an einen Pixel-Shader-Eingabeparameter angefügt wird. Diese Semantik wird in Direct3D 9 und Direct3D 10 und höher unterstützt.

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
<th>type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Farbe [n]</td>
<td>Diffuses oder Glanz Farben.</td>
<td>float4</td>
</tr>
<tr class="even">
<td>Texcoord [n]</td>
<td>Texturkoordinaten</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>Vface</td>
<td>Gleit Komma-Skalar, der einen mit der Rückseite ausgerichteten primitiven angibt. Ein negativer Wert steht rückwärts, während ein positiver Wert der Kamera angezeigt wird.
<blockquote>
[!Note]<br />
Diese Semantik ist in <a href="dx-graphics-hlsl-sm3.md">Direct3D 9-Shader-Modell 3,0</a>verfügbar. Verwenden Sie für Direct3D 10 und höher <a href="#semantics-supported-only-for-direct3d-10-and-newer">SV_IsFrontFace</a> .
</blockquote>
<br/></td>
<td>float</td>
</tr>
<tr class="even">
<td>Vpos</td>
<td>Die Pixelposition (x, y) im Bildschirmbereich. Informationen zum Konvertieren eines Direct3D 9-Shaders (der diese Semantik verwendet) in einen Shader für Direct3D 10 und höher finden Sie unter <a href="#direct3d-9-vpos-and-direct3d-10-sv_position">Direct3D 9 vpos und Direct3D 10 SV_Position</a>).</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Output</td>
<td>BESCHREIBUNG</td>
<td>type</td>
</tr>
<tr class="even">
<td>Farbe [n]</td>
<td>Ausgabe Farbe</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>Tiefe [n]</td>
<td>Ausgabe Tiefe</td>
<td>float</td>
</tr>
</tbody>
</table>

`n` ist eine optionale ganze Zahl zwischen 0 und der Anzahl unterstützter Ressourcen. Beispielsweise PSIZE0, COLOR1 usw.

Die Farb Semantik ist nur im Shader-Kompatibilitätsmodus gültig (d. h., wenn der Shader mit d3d10 Shader erstellt wird, um die abwärts \_ \_ Kompatibilität zu aktivieren \_ \_ ).

## <a name="semantics-supported-only-for-direct3d-10-and-newer"></a>Die Semantik wird nur für Direct3D 10 und höher unterstützt.

Die folgenden Typen von Semantik wurden für Direct3D 10 neu eingeführt und sind für Direct3D 9 nicht verfügbar.

- [System-Wert-Semantik](#system-value-semantics)

### <a name="system-value-semantics"></a>System-Value Semantik

Die System-Wert-Semantik ist neu in Direct3D 10. Alle System Werte beginnen mit einem SV- \_ Präfix, ein gängiges Beispiel ist die SV- \_ Position, die von der Raster-Stufe interpretiert wird. Die System Werte sind an anderen Teilen der Pipeline gültig. Beispielsweise kann die SV- \_ Position als Eingabe für einen Vertex-Shader und eine Ausgabe angegeben werden. Pixel-Shader können nur in Parameter mit der SV \_ -Tiefe und der \_ System-Wert-Semantik von SV Target schreiben.

Andere System Werte (SV \_ vertexid, SV \_ InstanceId, SV \_ isfrontface) können nur in den ersten aktiven Shader in der Pipeline eingegeben werden, der den jeweiligen Wert interpretieren kann. Anschließend muss die Shader-Funktion die Werte an nachfolgende Stufen übergeben.

SV \_ primitiveid ist eine Ausnahme von dieser Regel, die nur in den ersten aktiven Shader in der Pipeline eingegeben werden kann, der den jeweiligen Wert interpretieren kann. die Hardware kann denselben ID-Wert wie die Eingabe für die Hülle-Shader-Stufe, die Domäne-Shader-Stufe und danach die jeweils aktivierte Phase bereitstellen.

Wenn Mosaik aktiviert ist, sind die Stufen "Hull-Shader" und "Domain-Shader" vorhanden. Für einen bestimmten Patch gilt die gleiche primitiveid für den "Hull-Shader"-Aufruf des Patches und für alle im Mosaik Bereich aufzurufenden Domänen-Shader. Dieselbe primitiveid wird auch an die nächste aktive Phase weitergegeben. Geometry-Shader-Stufe oder Pixel-Shader-Stufe, wenn diese aktiviert ist.

Wenn der Geometrie-Shader die SV \_ primitiveid eingibt und NULL oder eine oder mehrere primitive pro Aufruf ausgeben kann, muss der Shader seine eigene Auswahl des SV \_ primitiveid-Werts für jede Ausgabe primitive programmieren, wenn ein weiterer Pixel-Shader den Wert SV \_ primtiveid eingibt.

Ein weiteres Beispiel: die "SV \_ primitiveid" kann nicht von der Vertex-Shader-Phase interpretiert werden, da ein Scheitelpunkt ein Member mehrerer primitiver sein kann.

Diese Semantik wurde Direct3D 10 hinzugefügt. Sie sind in Direct3D 9 nicht verfügbar.

System-Wert-Semantik für die Raster-Stufe.

| System-Value Semantik | BESCHREIBUNG | type |
|-|-|-|
| SV \_ clipdistance \[ n\] | Entfernungs Entfernungs Daten. Bei SV \_ clipdistance-Werten wird davon ausgegangen, dass es sich um einen float32 signed Distance to an eine Ebene handelt. Bei der primitiven Einrichtung werden nur die Rasterung in Pixel aufgerufen, für die die Entfernung der interpoliert Ebenen >= 0 ist. Mehrere Clip-Flächen können gleichzeitig implementiert werden, indem mehrere Komponenten eines oder mehrerer Scheitelpunkt Elemente als SV \_ clipdistance deklariert werden. Die kombinierten Werte für Clip-und Auslesen-Abstände sind höchstens D3D \# \_ Clip-oder auslesen-Entfernungs \_ \_ \_ \_ Komponenten in höchstens D3D Clip- \# \_ \_ oder \_ \_ \_ \_ Auslesen-Entfernungs Register. Verfügbar für alle Shader, die gelesen oder geschrieben werden sollen, mit Ausnahme des Vertex-Shader, der den Wert schreiben, aber nicht als Eingabe annehmen kann.<br/> Das **clipplane** -Attribut funktioniert wie SV \_ clipdistance, funktioniert jedoch auf allen Hardware [Funktionsebenen](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x und höher. Weitere Informationen finden Sie unter [User Clip Plane on Feature Level 9 Hardware](./user-clip-planes-on-10level9.md).<br/> | float |
| SV \_ culldistance \[ n\] | Entfernungs Entfernungs Daten. Wenn diese Bezeichnung von der Komponente (n) der Vertex-Elemente angenommen wird, wird davon ausgegangen, dass diese Werte als float32 signed Distance to an eine Ebene vorliegen. Primitive werden vollständig verworfen, wenn der Abstand der Ebene für alle Scheitel Punkte im primitiven < 0 ist. Mehrere umfügende Flächen können gleichzeitig verwendet werden, indem mehrere Komponenten eines oder mehrerer Vertex-Elemente als SV \_ culldistance deklariert werden. Die kombinierten Werte für Clip-und Auslesen-Abstände sind höchstens D3D \# \_ Clip-oder auslesen-Entfernungs \_ \_ \_ \_ Komponenten in höchstens D3D Clip- \# \_ \_ oder \_ \_ \_ \_ Auslesen-Entfernungs Register. Verfügbar für alle Shader, die gelesen oder geschrieben werden sollen, mit Ausnahme des Vertex-Shader, der den Wert schreiben, aber nicht als Eingabe annehmen kann.<br/> | float |
| SV- \_ Abdeckung | Eine Maske, die für Eingabe-, Ausgabe-oder beides eines Pixelshaders angegeben werden kann. <br/> Für die SV- \_ Abdeckung in einem Pixelshader wird die Ausgabe auf PS \_ 4 \_ 1 oder höher unterstützt. <br/> Für die SV- \_ Abdeckung eines Pixelshaders erfordert die Eingabe PS \_ 5 \_ 0 oder höher. <br/> | uint |
| SV- \_ Tiefe | Tiefen Puffer Daten. Kann von einem Pixelshader geschrieben werden. | float |
| SV \_ depthgreaterequal | In einem Pixelshader lässt die Auswertungs Tiefe zu, solange der Wert größer oder gleich dem vom Rasterizer festgelegten Wert ist. Ermöglicht das Anpassen der Tiefe, ohne die frühe Z zu deaktivieren. | float |
| SV \_ depthlessequal | In einem Pixelshader lässt die Auswertungs Tiefe zu, solange der Wert kleiner oder gleich dem Wert ist, der vom Rasterizer bestimmt wird. Ermöglicht das Anpassen der Tiefe, ohne die frühe Z zu deaktivieren. | float |
| [SV \_ dispatchthreadid](sv-dispatchthreadid.md) | Definiert den globalen Thread Offset innerhalb des dispatchaufrufes pro Dimension der Gruppe. Verfügbar als Eingabe für den Compute-Shader. (schreibgeschützt) | uint3 |
| [SV \_ domainlocation](sv-domainlocation.md) | Definiert den Speicherort auf der Hülle des aktuellen Domänen Punkts, der ausgewertet wird. Als Eingabe für den Domänen-Shader verfügbar. (schreibgeschützt) | float2 \| 3 |
| [SV \_ GroupID](sv-groupid.md) | Definiert den Gruppen Offset in einem Dispatch-Befehl pro Dimension des dispatchaufrufes. Verfügbar als Eingabe für den Compute-Shader. (schreibgeschützt) | uint3 |
| [SV \_ groupIndex](sv-groupindex.md) | Stellt einen vereinfachten Index für einen angegebenen Thread innerhalb einer angegebenen Gruppe bereit. Verfügbar als Eingabe für den Compute-Shader. (schreibgeschützt) | uint |
| [SV \_ groupthreadid](sv-groupthreadid.md) | Definiert den Thread Offset innerhalb der Gruppe pro Dimension der Gruppe. Verfügbar als Eingabe für den Compute-Shader. (schreibgeschützt) | uint3 |
| [SV \_ gsinstanceid](sv-gsinstanceid.md) | Definiert die Instanz des Geometry-Shaders. Verfügbar als Eingabe für den Geometry-Shader. Die-Instanz ist erforderlich, da ein Geometry-Shader bis zu 32-mal für denselben Geometry-primitiven aufgerufen werden kann. | uint |
| SV \_ innercoverage | Stellt unterschätzte konservative rasterisierungsinformationen dar (d. h., ob ein Pixel garantiert vollständig abgedeckt ist). Kann vom Pixelshader gelesen oder geschrieben werden. | |
| [SV \_ insidetess Factor](sv-insidetessfactor.md) | Definiert den Mosaik Betrag innerhalb einer patchoberfläche. Verfügbar im Hull-Shader zum Schreiben und im Domänen-Shader zum Lesen verfügbar. | float \| float \[ 2\] |
| SV \_ InstanceId | Pro-Instanz-Bezeichner, der automatisch von der Laufzeit generiert wird (siehe [verwenden System-Generated Werte (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Verfügbar für alle Shader. | |
| SV \_ isfrontface | Gibt an, ob ein Dreieck im Vordergrund steht. Für Linien und Punkte hat isfrontface den Wert true. Bei der Ausnahme handelt es sich um Zeilen, die aus Dreiecke (Wireframe-Modus) gezeichnet werden, wodurch isfrontface auf die gleiche Weise festgelegt wird, wie das Dreieck im Vollbildmodus geren Kann vom Geometry-Shader geschrieben und vom Pixelshader gelesen werden. | bool |
| [SV \_ outputcontrolpointid](sv-outputcontrolpointid.md) | Definiert den Index der Kontrollpunkt-ID, die durch einen Aufruf des Haupt Einstiegs Punkts des Hull-Shader betrieben wird. Kann nur vom Hull-Shader gelesen werden. | uint |
| SV- \_ Position | Wenn die SV- \_ Position für die Eingabe in einen Shader deklariert ist, kann Sie einen der beiden folgenden Interpolations Modi angeben: linearnoperspecor linearnoperspectivecentroid, wobei letztere bei der Multisampling-Antialiasing Bereitstellung von Centroid-angedockten xyzw-Werten bewirkt. Wenn die Position in einem Shader verwendet wird, \_ beschreibt die Position des SV den Pixel Speicherort. Verfügbar in allen Shadern, um das Pixel Center mit einem Offset von 0,5 zu erhalten. | float4 |
| SV \_ primitiveid | Pro primitiver Bezeichner, der automatisch von der Laufzeit generiert wird (siehe [verwenden System-Generated Werte (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Kann von den geometry-oder Pixel-Shadern geschrieben und durch die Geometrie-, Pixel-, Hull-oder Domänen-Shader gelesen werden. | uint |
| SV \_ rendertargetarrayindex | Renderziel-Array Index. Wird auf die Geometrie-Shader-Ausgabe angewendet und gibt den renderzielarray-Slice an, auf den der primitive-Shader verweist. \_Der SV rendertargetarrayindex ist nur gültig, wenn das Renderziel eine Array Ressource ist. Diese Semantik gilt nur für primitive; Wenn ein primitiv mehr als einen Scheitelpunkt hat, wird der Wert aus dem führenden Scheitelpunkt verwendet. Dieser Wert gibt auch an, welches Array Slice einer Tiefe/Schablonen Ansicht für Lese-/Schreibzwecke verwendet wird.<br/> Kann aus dem Geometry-Shader geschrieben und vom Pixelshader gelesen werden.<br/> Wenn [D3D11_FEATURE_DATA_D3D11_OPTIONS3:: vpandrtarrayindexfromanyshaderfeedingrasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) ist `true` , dann \_ wird SV rendertargetarrayindex auf jeden Shader angewendet, der das Rasterizer-Element speist. | uint |
| SV \_ sampleingedex | Beispiel Daten für den Häufigkeits Index. Verfügbar, das nur vom Pixel-Shader gelesen oder geschrieben werden soll. | uint |
| SV \_ stencilref | Stellt den aktuellen Pixelshader-Schablonen Verweis Wert dar. Kann nur vom Pixel-Shader geschrieben werden. | uint |
| SV \_ Target \[ n \] , wobei 0 <= n <= 7 | Der Ausgabewert, der in einem Renderziel gespeichert wird. Der Index gibt an, in welche der 8 möglicherweise gebundenen Renderziele geschrieben werden sollen. Der Wert ist für alle Shader verfügbar. | float \[ 2 \| 3 \| 4\] |
| [SV-Mosaik \_ Faktor](sv-tessfactor.md) | Definiert den Mosaik Betrag an jedem Rand eines Patches. Verfügbar zum Schreiben im Hull-Shader und lesen im Domänen-Shader. | float \[ 2 \| 3 \| 4\] |
| SV \_ vertexid | Pro-Vertex-Bezeichner, der automatisch von der Laufzeit generiert wird (siehe [verwenden System-Generated Werte (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Nur als Eingabe für den Vertex-Shader verfügbar. | uint |
| SV \_ viewportarrayindex | Viewport-Array Index. Wird auf die Geometrie-Shader-Ausgabe angewendet und gibt an, welcher Viewport für das primitive verwendet werden soll, das zurzeit geschrieben wird. Kann vom Pixelshader gelesen werden. Der primitive wird transformiert und für den Viewport abgeschnitten, der durch den Index angegeben wird, bevor er an den Rasterizer übergeben wird. Diese Semantik gilt nur für primitive; Wenn ein primitiv mehr als einen Scheitelpunkt hat, wird der Wert aus dem führenden Scheitelpunkt verwendet. <br/> Wenn [D3D11_FEATURE_DATA_D3D11_OPTIONS3:: vpandrtarrayindexfromanyshaderfeedingrasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) ist `true` , dann \_ wird SV viewportarrayindex auf jeden Shader angewendet, der den Rasterizer nährt. | uint |
| SV \_ shadingrate | Definiert durch Schattierungs Raten [Werte](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)die Anzahl der Pixel, die von einem Pixelshader-Aufruf für [Variablen Schattierungs Raten der Ebene 2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) oder höher geschrieben werden. Kann aus dem Pixelshader gelesen werden. Kann aus einem Scheitelpunkt oder einem Geometry-Shader geschrieben werden. | uint |

### <a name="limitations-when-writing-sv_depth"></a>Einschränkungen beim Schreiben von SV- \_ Tiefe:

- Wenn multisamplinggrad (multisampleenable in [**d3d10 \_ Rasterizer \_**](/windows/win32/api/d3d10/ns-d3d10-d3d10_rasterizer_desc)Debug) und das Schreiben eines tiefen Werts (mit einem Pixelshader) verwendet wird, wird auch der einzelne Wert, der **ausgegeben wird,** im [tiefen Test](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md)verwendet, sodass die Fähigkeit zum Rendern primitiver Kanten bei einer höheren Auflösung bei multisamplinggrad verloren geht.
- Wenn die dynamische Fluss Steuerung verwendet wird, ist es nicht möglich, zur Kompilierzeit zu bestimmen, ob ein Shader, der die SV-Tiefe in einigen Pfaden schreibt, sicherstellt, dass die \_ SV- \_ Tiefe bei jeder Ausführung geschrieben wird. Wenn beim Deklarieren keine SV-Tiefe geschrieben wird, führt dies zu einem \_ nicht definierten Verhalten (das ggf. das Verwerfen des Pixels einschließt).
- Alle float32-Werte einschließlich +/-inf und Nan können in die SV-Tiefe geschrieben werden \_ .
- Das Schreiben von SV- \_ Tiefe ist weiterhin gültig, wenn Sie eine Dual-Source-Farbmischung

## <a name="migration-from-direct3d-9-to-direct3d-10-and-later"></a>Migration von Direct3D 9 zu Direct3D 10 und höher

Beim Migrieren von Code von Direct3D 9 zu Direct3D 10 und höher sollten die folgenden Punkte berücksichtigt werden:

### <a name="mapping-to-direct3d-9-semantics"></a>Zuordnung zu Direct3D 9-Semantik

Einige der Semantik Direct3D 10 und höher werden direkt der Semantik Direct3D 9 zugeordnet.

| Direct3D 10-Semantik | Direct3D 9 äquivalente Semantik |
|-|-|
| SV- \_ Tiefe | DEPTH |
| SV- \_ Position | POSITION |
| SV- \_ Ziel | COLOR |

> [!] Hinweis für Direct3D 9-Entwickler: für Direct3D 9-Ziele muss die Shader-Semantik einer gültigen Direct3D 9-Semantik zugeordnet werden. Aus Gründen der Abwärtskompatibilität werden POSITION0 (und die zugehörigen Variant-Namen) als SV- \_ Ziel behandelt. Farbe wird als SV- \_ Ziel behandelt.

- [Zuordnung zu Direct3D 9-Semantik](#mapping-to-direct3d-9-semantics)
- [Direct3D 9 vpos und Direct3D 10 SV \_ Position](#direct3d-9-vpos-and-direct3d-10-sv_position)
- [Benutzer Clip Flächen in HLSL](#user-clip-planes-in-hlsl)

### <a name="direct3d-9-vpos-and-direct3d-10-sv_position"></a>Direct3D 9 vpos und Direct3D 10 SV \_ Position

Die d3d10 Semantic SV- \_ Position bietet ähnliche Funktionen wie die Semantik des Direct3D 9-Shader Model 3-vpos. Beispielsweise wird in Direct3D 9 die folgende Syntax für einen PixelShader verwendet, der Bildschirmraum Koordinaten verwendet:

```HLSL
float4 psMainD3D9( float4 screenSpace : VPOS ) : COLOR
{
    // code here 
}
```

Vpos wurde für die Unterstützung von Shader Model 3 hinzugefügt, um Bildschirmraum Koordinaten anzugeben, da die Positions Semantik für Objekt Raumkoordinaten vorgesehen war.

In Direct3D 10 und höher gibt die SV- \_ Positions Semantik (bei Verwendung im Kontext eines Pixelshaders) Bildschirmraum Koordinaten (Offset um 0,5) an. Daher wäre der Direct3D 9-Shader ungefähr Äquivalent (ohne Berücksichtigung des 0,5-Offsets) für Folgendes:

```HLSL
float4 psMainD3D10( float4 screenSpace : SV_Position ) : COLOR
{
    // code here
}
```

Wenn Sie von Direct3D 9 zu Direct3D 10 und höher migrieren, müssen Sie dies beim Übersetzen der Shader beachten.

### <a name="user-clip-planes-in-hlsl"></a>Benutzer Clip Flächen in HLSL

Ab Windows 8 können Sie das **clipplane** -Funktions Attribut in einer HLSL- [Funktionsdeklaration](dx-graphics-hlsl-function-syntax.md) anstelle von SV \_ clipdistance verwenden, damit Ihr Shader auf [Featureebene](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x und auf Featureebene 10 und höher funktioniert. Weitere Informationen finden Sie unter [User Clip Plane on Feature Level 9 Hardware](./user-clip-planes-on-10level9.md).

## <a name="related-topics"></a>Zugehörige Themen

* [Sprach Syntax](dx-graphics-hlsl-language-syntax.md)
* [Variablen (DirectX HLSL)](dx-graphics-hlsl-variables.md)
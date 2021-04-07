---
description: In dieser Tabelle sind FVF-Codes einer D3DVERTEXELEMENT9-Struktur zugeordnet.
ms.assetid: de865481-2a08-4d25-967c-8e68b7affe8d
title: Zuordnung von FVF-Codes zu einer Direct3D 9-Deklaration (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85442cf1c92c78aa1a37f4d4a4ec3de154f5b8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745368"
---
# <a name="mapping-fvf-codes-to-a-direct3d-9-declaration-direct3d-9"></a>Zuordnung von FVF-Codes zu einer Direct3D 9-Deklaration (Direct3D 9)

In dieser Tabelle sind FVF-Codes einer [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Struktur zugeordnet.



| F-VF                                                   | Datentyp                                                           | Verbrauch                                                                         | Verwendungs Index |
|-------------------------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|
| D3DFVF \_ XYZ                                           | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE- \_ Position                                                        | 0           |
| D3DFVF \_ xyzrhw                                        | D3DDECLTYPE \_ float4                                                 | D3DDECLUSAGE \_ positiont                                                       | 0           |
| D3DFVF \_ xyzw                                          | D3DDECLTYPE \_ float4                                                 | D3DDECLUSAGE- \_ Position                                                        | 0           |
| D3DFVF \_ XYZB5 und D3DFVF \_ lastbeta \_ UBYTE4            | D3DVSDT \_ FLOAT3, D3DVSDT \_ float4, D3DVSDT \_ UBYTE4                   | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ blendweight, D3DDECLUSAGE \_ blendindices | 0           |
| D3DFVF \_ XYZB5 und D3DFVF \_ lastbeta \_ D3DCOLOR          | D3DVSDT \_ FLOAT3, D3DVSDT \_ float4, D3DVSDT \_ D3DCOLOR                 | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ blendweight, D3DDECLUSAGE \_ blendindices | 0           |
| D3DFVF \_ XYZB5                                         | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float4, D3DDECLTYPE \_ FLOAT1       | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ blendweight, D3DDECLUSAGE \_ blendindices | 0           |
| D3DFVF \_ xyzbn (n = 1.. 4)                                | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ floatn                            | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ blendweight                             | 0           |
| D3DFVF \_ xyzbn (n = 1.. 4) und D3DFVF \_ lastbeta \_ UBYTE4   | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float (n-1), D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ blendweight, D3DDECLUSAGE \_ blendindices | 0           |
| D3DFVF \_ xyzbn (n = 1.. 4) und D3DFVF \_ lastbeta \_ D3DCOLOR | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ float (n-1), D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ Position, D3DDECLUSAGE \_ blendweight, D3DDECLUSAGE \_ blendindices | 0           |
| D3DFVF \_ Normal                                        | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ Normal                                                          | 0           |
| D3DFVF \_ Psize                                         | D3DDECLTYPE \_ FLOAT1                                                 | D3DDECLUSAGE \_ Psize                                                           | 0           |
| D3DFVF \_ diffuses                                       | D3DDECLTYPE \_ D3DCOLOR                                               | D3DDECLUSAGE- \_ Farbe                                                           | 0           |
| D3DFVF \_ Glanz                                      | D3DDECLTYPE \_ D3DCOLOR                                               | D3DDECLUSAGE- \_ Farbe                                                           | 1           |
| D3DFVF \_ texcoordsizem (n)                              | D3DDECLTYPE \_ floatm                                                 | D3DDECLUSAGE \_ texcoord                                                        | n           |



 

## <a name="vertex-declarations-with-d3ddeclusage_positiont"></a>Vertex-Deklarationen mit D3DDECLUSAGE \_ positiont

Das vorhanden sein eines Vertex-Elements mit (D3DUSAGE \_ positiont, 0) wird verwendet, um dem Gerät mitzuteilen, dass die Vertex-Daten bereits über die Scheitelpunkt Verarbeitung (z. b. eine FVF mit D3DFVF \_ xyzrhw Bit festgelegt) wurden. Wenn die aktuell festgelegte Deklaration zum Zeitpunkt der Erstellung über ein Element mit der \_ Semantik (D3DUSAGE positiont, 0) verfügt, wird die gesamte Vertexverarbeitung übersprungen (genau so, als ob eine "f VF with D3DFVF \_ xyzrhw"-Bit festgelegt wurde).

Es gibt einige Einschränkungen bei Scheitelpunkt Deklarationen mit (D3DDECLUSAGE \_ positiont, 0):

-   In solchen Deklarationen kann nur Stream NULL verwendet werden.
-   Vertex-Elemente müssen sortiert werden, indem der Streamoffset erhöht wird.
-   Der Streamoffset muss DWORD-bündig sein.
-   Dasselbe Paar (Verwendung, Verwendungs Index) sollte nur einmal aufgeführt werden.
-   Nur die D3DDECLMETHOD- \_ Standardmethode kann verwendet werden.
-   Andere Scheitelpunkt Elemente können nicht die \_ Semantik (D3DDECLUSAGE Position, 0) aufweisen.

Außerdem gibt es einige Einschränkungen für eine solche Deklaration, die sich auf die Gerätetreiber Version bezieht. Diese Einschränkungen sind wirksam, weil Direct3D solche Deklarationen direkt an den Treiber sendet, ohne eine Konvertierung durchzuführen.

## <a name="vertex-declarations-without-d3ddeclusage_positiont"></a>Vertex-Deklarationen ohne D3DDECLUSAGE \_ positiont

Die Laufzeit überprüft die Erstellung von Deklarationen. Im folgenden finden Sie die allgemeinen Regeln für die zulässige Deklarationen.

-   Alle Scheitelpunkt Elemente für einen Stream müssen aufeinander folgen und nach Offset sortiert werden.
-   Der Streamoffset muss DWORD-bündig sein.
-   Dasselbe Paar (Verwendung, Verwendungs Index) sollte nur einmal aufgeführt werden.
-   Wenn D3DDEVCAPS2 \_ vertexelementscansharestreamoffset festgelegt ist, dann
    -   Mehrere Scheitelpunkt Elemente können denselben Offset in einem Stream gemeinsam verwenden.
    -   Die Vertex-Elemente können alle verschiedene Typen aufweisen, die von unterschiedlichen Größen abweichen können.
    -   Die Vertex-Elemente können beliebig überlappend sein. Ein Element kann z. b. an einer Position eines Streams beginnen, die gleichzeitig in der Mitte eines anderen Elements ist.
    -   Vertex-Elemente dürfen den Streamoffset in beliebiger Reihenfolge aufweisen.
-   Die Anzahl der Scheitelpunkt Elemente darf nicht größer als 64 sein.
-   Der "US-ageingangs Index" sollte im Bereich von \[ 0-15 liegen \] .
-   Deklaration, die mit der drawprimitiven API verwendet wird, sollte keine anderen Scheitelpunkt Elemente als D3DDECLMETHOD \_ Default, D3DDECLMETHOD \_ lookuppresampling oder D3DDECLMETHOD \_ Lookup aufweisen.
-   Die Deklaration, die D3DDECLMETHOD \_ Lookup oder lookuppresampling enthält, sollte nur mit der programmierbaren Scheitelpunkt Pipeline verwendet werden.
-   Die mit der drawrectpatch/drawtapatch-API verwendete Deklaration darf keine Scheitelpunkt Elemente mit D3DDECLMETHOD \_ lookuppresampling oder D3DDECLMETHOD \_ Lookup aufweisen.
-   Die Deklaration darf nur über ein Element mit der D3DDECLMETHOD \_ Lookup-oder der D3DDECLMETHOD \_ lookuppresampling-Methode verfügen.
-   Bei der Deklaration mit D3DDECLMETHOD \_ Lookup oder D3DDECLMETHOD \_ lookuppresampling sollten keine anderen Elemente als D3DDECLMETHOD default vorhanden sein \_ , da die Verschiebungs Zuordnung nur für N-Patches erfolgt.
-   Vertex-Elemente mit D3DDECLMETHOD \_ Lookup oder D3DDECLMETHOD \_ lookuppresampling können nur mit der \_ Semantik (D3DDECLUSAGE Sample, n) und umgekehrt verwendet werden.
-   Wenn ein Vertex-Element mit \_ der D3DDECLMETHOD Lookup-Methode über einen streamindex und einen Offset eines bereits vorhandenen Vertex-Elements verfügt, sollte dieses Scheitelpunkt Element denselben Datentyp aufweisen.
-   Ein Vertex-Element mit der D3DDECLMETHOD \_ Lookup-Methode muss den D3DDECLTYPE \_ FLOAT2/3/4-Datentyp aufweisen.
-   Vertex-Elemente mit den Typen D3DDECLMETHOD \_ crossuv, D3DDECLMETHOD \_ partialu und D3DDECLMETHOD \_ partialv sollten einen Offset eines Vertex-Elements mit einem kompatiblen Datentyp aufweisen.
-   Ein Vertex-Element mit der-Methode D3DDECLMETHOD \_ UV oder D3DDECLMETHOD \_ lookuppresampling muss den Typ D3DDECLTYPE nicht \_ verwendet, den Stream Index NULL und den Streamoffset 0 (null) aufweisen.
-   Deklarationen mit den Methoden D3DDECLMETHOD \_ UV, D3DDECLMETHOD \_ partialu und D3DDECLMETHOD \_ partialv können nur mit drawrectpatch verwendet werden.
-   Usage D3DDECLUSAGE \_ Tess Factor sollte nur mit dem Datentyp D3DDECLTYPE \_ FLOAT1 und dem Verwendungs Index 0 verwendet werden.
-   Wenn eine Deklaration für Mosaik Vorgänge (drawrectpatch, drawzpatch, N-Patches) verwendet wird, muss der Datentyp kleiner oder gleich D3DDECLTYPE \_ SHORT4 sein.
-   Deklarationen, die Methoden enthalten, die bestimmte Gerätefunktionen erfordern (z. b. Verschiebungs Zuordnung, RT-Patches), können nur erstellt werden, wenn Sie vom Gerät unterstützt werden.
-   Eine Scheitelpunkt Deklaration, die zum Zeichnen von Punkten und Zeilen verwendet wird, darf nicht über D3DDECLMETHOD \_ default verfügen.
-   Die Deklarationen, die erstellt werden können, sind auch von den Treiberfunktionen abhängig.

## <a name="driver-considerations"></a>Überlegungen zu Treibern

### <a name="pre-direct3d-9-drivers"></a>Pre-Direct3D 9-Treiber

-   Die Eingabe Deklaration muss in eine gültige FVF übersetzt werden können (in derselben Reihenfolge wie Vertex-Elemente und deren Datentypen).
-   Lücken in Texturkoordinaten sind nicht zulässig. Dies bedeutet Folgendes: Wenn ein Scheitelpunkt Element mit (D3DDECLUSAGE \_ texcoord, n) vorhanden ist, sollte auch ein Vertex-Element mit (D3DDECLUSAGE \_ texcoord, n-1) vorhanden sein.

### <a name="direct3d-9-drivers-without-pixel-shader-version-3-support"></a>Direct3D 9-Treiber ohne Unterstützung für Pixel-Shader, Version 3

-   Die Eingabe Deklaration muss in eine gültige FVF übersetzt werden können (in derselben Reihenfolge wie Vertex-Elemente und deren Datentypen).
-   Lücken in Texturkoordinaten sind zulässig.

### <a name="direct3d-9-drivers-with-pixel-shader-version-3-support"></a>Direct3D 9-Treiber mit Unterstützung für Pixel-Shader, Version 3

Allgemeinere Deklarationen sind zulässig.

-   Vertex-Elemente können in beliebiger Reihenfolge vorliegen und beliebige Datentypen aufweisen.
-   Mehrere Scheitelpunkt Elemente können denselben Streamoffset gemeinsam verwenden und einen anderen Typ aufweisen, wenn D3DDEVCAPS2 \_ vertexelementscansharestreamoffset vom Gerät festgelegt wird.

## <a name="vertex-declaration-usage-with-the-programmable-vertex-pipeline"></a>Verwendung der Vertexdeklaration mit der programmierbaren Scheitelpunkt Pipeline

-   Zur zeichnungszeit sucht Direct3D nach der gleichen Kombination aus "Verwendungs Verwendungs Index" in der aktuellen Vertexdeklaration und der aktuellen Vertex-Shader-Funktion. Wenn die Kombination gefunden wird, wird die Register from Shader-Funktion DCL als Ziel für das Vertex-Element verwendet.
-   Wenn ein Vertex-Element in der aktuellen Vertexdeklaration über eine Verwendung verfügt, die im aktuellen Vertexshader nicht gefunden wird, wird dieses Vertex-Element ignoriert.
-   Bei Verwendung einer Vertex-Shader-Version, die kleiner als 2,0 ist, muss die gesamte im Shader-Code erwähnte Semantik in der Deklaration vorhanden sein, die zur zeichnungszeit gebunden ist. Wenn Sie Vertex-Shader 2,0 und höher verwenden, ist diese Einschränkung, die es Anwendungen ermöglicht, unterschiedliche Scheitelpunkt Deklarationen mit demselben Vertex-Shader zu verwenden, nicht vorhanden. Dies ist hilfreich, wenn ein Vertex-Shader Eingabedaten auf der Grundlage statischer Bedingungen liest. Die Vertex-Shader-Register sind nicht initialisiert, da diese keine undefinierten Werte aufweisen.

Bei der Verwendung von mit der Hardware Vertex-Verarbeitung auf einem DirectX 8-Treiber gibt es zusätzliche Einschränkungen:

-   Vertex-Elemente dürfen sich nicht überlappen oder den gleichen Offset gemeinsam verwenden.
-   Die Datentypen sind darauf beschränkt, was der DirectX 8-Treiber verstehen kann.

Der Fehler bei der Deklaration von "" schlägt möglicherweise fehl, wenn die angegebene Deklaration nicht in eine DirectX 8-Deklaration konvertiert werden kann. Bei einem Gerät im gemischten Modus tritt dieser Fehler zur zeichnungszeit auf, \* da dies der einzige Zeitpunkt ist, zu dem bekannt ist, ob dieser Shader bei der Verarbeitung von Hardware-oder Software Scheitel Punkten verwendet wird.

## <a name="vertex-declaration-usage-with-the-fixed-function-pipeline"></a>Verwendung der Vertex-Deklaration mit der Fixed-Funktions Pipeline

Es können nur Deklarationen verwendet werden, die den folgenden Regeln entsprechen:

-   Es sollten keine Lücken zwischen Scheitelpunkt Elementen vorhanden sein (Skip ist in einer DirectX 8-Deklaration, die für die Fixed-Funktions Pipeline verwendet wird, nicht zulässig).
-   Semantic (D3DDECLUSAGE \_ Position, 0) muss angegeben werden und muss den D3DDECLTYPE \_ FLOAT3-Datentyp aufweisen.
-   Ein Vertex-Element mit der D3DDECLMETHOD \_ --Methode muss use D3DDECLUSAGE \_ texcoord oder D3DDECLUSAGE \_ blendweight angeben.
-   Ein Vertex-Element mit der D3DDECLMETHOD \_ partialu \_ -, partialv-oder \_ crossuv-Methode kann nur mit D3DDECLUSAGE \_ Position, \_ Normal, \_ blendweight oder \_ texcoord verwendet werden und muss den Eingabetyp D3DDECLTYPE \_ FLOAT3 verwenden.

Wenn eine Deklaration für die Verarbeitung von Hardware Scheitel Punkten in einem DirectX 8-Treiber verwendet wird, konvertiert die Direct3D-Laufzeit diese Deklaration in eine DirectX 8-Deklaration mit den folgenden Regeln:

-   Vertex-Elemente können nicht denselben Offset in einem Datenstrom gemeinsam verwenden, und Sie können sich nicht überlappen.
-   Der Datentyp muss kleiner oder gleich D3DDECLTYPE \_ SHORT4 sein.
-   Nur die folgenden Methoden sind zulässig: D3DDECLMETHOD \_ Default, D3DDECLMETHOD \_ crossuv und D3DDECLMETHOD \_ UV
-   Die [Zuordnung zwischen einer Direct3D 9-Deklaration und einer Direct3D 8-Deklaration (Direct3D 9)](mapping-between-a-directx-9-declaration-and-directx-8.md) zeigt, welche Direct3D 9-Semantik in eine DirectX 8-Style-Deklaration konvertiert werden konnte. "Usage" und "Start Index" werden in einen Registerwert konvertiert.
-   Wenn in einer Deklaration n Scheitelpunkt Elemente vorhanden sind und 0-m (m < n) einem FVF zugeordnet ist (Elemente, die in der [Zuordnung zwischen einer Direct3D-Deklaration und FVF-Codes (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md)beschrieben werden), aber m + 1 nicht, dann gilt Folgendes:
    -   Wenn eine von m + 2 bis n-1 Scheitelpunkt Elemente FVF/dx8decl zugeordnet ist, ist die Deklaration ungültig.
    -   Die Elemente 0 bis m werden konvertiert (von der Laufzeit für DirectX 8 und ältere Treiber). und durch die Direct3D 9-Treiber) mithilfe der [Zuordnung zwischen einer Direct3D-Deklaration und FVF-Codes (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md), m + 1, m + 2, bis n-1 dem zusammenhängenden texkoord (k), texcoord (k + 1), beginnend mit einem beliebigen texkoord in den Elementen 0-m zugeordnet wird.
    -   Es wird davon ausgegangen, dass der Datentyp in einem zugeordneten texcoord den Wert float \[ 1234 ersetzt, der \] den Datentyp ersetzt, den das aktuelle Element enthält (aber die gleiche Größe). Daher kann der vorhandene Datentyp etwas sein, das sich nicht in der [Zuordnung zwischen einer Direct3D-Deklaration und einem f-Code (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md)befindet.
    -   Wenn k 8 erreicht, ist die Deklaration für "f"/"dx8decl" ungültig.
    -   Wenn Zuordnungen zu texcoords aufgetreten sind, ist es erforderlich, dass für die gesamte Deklaration keine Elemente mit der Generierungs Methode außer default vorhanden sind oder die Deklaration für FVF/dx8decl ungültig ist.

## <a name="using-vertex-declarations-with-processvertices"></a>Verwenden von Scheitelpunkt Deklarationen mit ProcessVertices

Eine Scheitelpunkt Deklaration könnte verwendet werden, um die Ausgabe von ProcessVertices zu beschreiben. Diese Deklaration sollte den folgenden Regeln entsprechen:

-   Es muss nur Stream 0 verwendet werden.
-   Nur D3DDECLMETHOD- \_ Standardmethoden sind zulässig.
-   Es können nur D3DDECLTYPE \_ floatn-oder D3DDECLTYPE \_ D3DCOLOR-Datentypen verwendet werden.
-   Vertex-Elemente können nicht denselben Offset verwenden und einander überlappen.
-   Vertex-Elemente mit (D3DDECLUSAGE \_ Position, 0) oder (D3DDECLUSAGE \_ positiont, 0) sind nicht erforderlich.
-   Vertex-Elemente mit (D3DDECLUSAGE \_ Position, 0) und (D3DDECLUSAGE \_ positiont, 0) dürfen nicht in derselben Deklaration vorhanden sein.
-   Der aktuelle Vertexshader muss, Version 3,0, oder höher sein, wenn eine solche Deklaration verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Deklaration](vertex-declaration.md)
</dt> </dl>

 

 




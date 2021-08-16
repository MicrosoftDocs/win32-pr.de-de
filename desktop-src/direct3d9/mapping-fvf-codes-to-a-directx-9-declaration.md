---
description: Diese Tabelle ordnet FVF-Codes einer D3DVERTEXELEMENT9-Struktur zu.
ms.assetid: de865481-2a08-4d25-967c-8e68b7affe8d
title: Zuordnen von FVF-Codes zu einer Direct3D 9-Deklaration (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8ef4d5e8e29c4c7f6af8d82b650b4898c57d900b92b8dd45ca2368bb9eacce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799076"
---
# <a name="mapping-fvf-codes-to-a-direct3d-9-declaration-direct3d-9"></a>Zuordnen von FVF-Codes zu einer Direct3D 9-Deklaration (Direct3D 9)

Diese Tabelle ordnet FVF-Codes einer [**D3DVERTEXELEMENT9-Struktur**](d3dvertexelement9.md) zu.



| FVF                                                   | Datentyp                                                           | Verbrauch                                                                         | Nutzungsindex |
|-------------------------------------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------|-------------|
| D3DFVF \_ XYZ                                           | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ POSITION                                                        | 0           |
| D3DFVF \_ XYZRHW                                        | D3DDECLTYPE \_ FLOAT4                                                 | D3DDECLUSAGE \_ POSITIONT                                                       | 0           |
| D3DFVF \_ XYZW                                          | D3DDECLTYPE \_ FLOAT4                                                 | D3DDECLUSAGE \_ POSITION                                                        | 0           |
| D3DFVF \_ XYZB5 und D3DFVF \_ LASTBETA \_ UBYTE4            | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ UBYTE4                   | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5 und D3DFVF \_ LASTBETA \_ D3DCOLOR          | D3DVSDT \_ FLOAT3, D3DVSDT \_ FLOAT4, D3DVSDT \_ D3DCOLOR                 | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZB5                                         | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT4, D3DDECLTYPE \_ FLOAT1       | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n=1..4)                                | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOATn                            | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT                             | 0           |
| D3DFVF \_ XYZBn (n=1..4) und D3DFVF \_ LASTBETA \_ UBYTE4   | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT(n-1), D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ XYZBn (n=1..4) und D3DFVF \_ LASTBETA \_ D3DCOLOR | D3DDECLTYPE \_ FLOAT3, D3DDECLTYPE \_ FLOAT(n-1), D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ BLENDWEIGHT, D3DDECLUSAGE \_ BLENDINDICES | 0           |
| D3DFVF \_ NORMAL                                        | D3DDECLTYPE \_ FLOAT3                                                 | D3DDECLUSAGE \_ NORMAL                                                          | 0           |
| D3DFVF \_ PSIZE                                         | D3DDECLTYPE \_ FLOAT1                                                 | D3DDECLUSAGE \_ PSIZE                                                           | 0           |
| D3DFVF \_ DIFFUSE                                       | D3DDECLTYPE \_ D3DCOLOR                                               | D3DDECLUSAGE \_ COLOR                                                           | 0           |
| D3DFVF \_ SPECULAR                                      | D3DDECLTYPE \_ D3DCOLOR                                               | D3DDECLUSAGE \_ COLOR                                                           | 1           |
| D3DFVF \_ TEXCOORDSIZEm(n)                              | D3DDECLTYPE \_ FLOATm                                                 | D3DDECLUSAGE \_ TEXCOORD                                                        | n           |



 

## <a name="vertex-declarations-with-d3ddeclusage_positiont"></a>Scheitelpunktdeklarationen mit D3DDECLUSAGE \_ POSITIONT

Das Vorhandensein eines Scheitelpunktelements mit (D3DUSAGE POSITIONT, 0) wird verwendet, um dem Gerät anzugeben, dass die einkommenden Scheitelpunktdaten bereits eine Scheitelpunktverarbeitung (z. B. eine \_ FVF mit D3DFVF XYZRHW-Bitsatz) verarbeitet \_ haben. Wenn die derzeit festgelegte Deklaration zur Zeichnen-Zeit ein Element mit der Semantik (D3DUSAGE POSITIONT, 0) auf hat, wird die gesamte Vertexverarbeitung übersprungen (so, als ob eine \_ FVF mit D3DFVF \_ XYZRHW-Bit festgelegt wurde).

Es gibt einige Einschränkungen für Scheitelpunktdeklarationen mit (D3DDECLUSAGE \_ POSITIONT, 0):

-   In solchen Deklarationen kann nur der Stream 0 (null) verwendet werden.
-   Scheitelpunktelemente müssen durch Erhöhen des Streamoffsets sortiert werden.
-   Der Streamoffset muss DWORD-ausgerichtet sein.
-   Das gleiche Paar (Nutzung, Nutzungsindex) sollte nur einmal aufgeführt werden.
-   Nur die D3DDECLMETHOD \_ DEFAULT-Methode kann verwendet werden.
-   Andere Vertexelemente können nicht die Semantik (D3DDECLUSAGE \_ POSITION, 0) haben.

Darüber hinaus gelten einige Einschränkungen für eine solche Deklaration im Zusammenhang mit der Gerätetreiberversion. Diese Einschränkungen sind wirksam, da Direct3D solche Deklarationen direkt an den Treiber sendet, ohne dass eine Konvertierung erfolgt.

## <a name="vertex-declarations-without-d3ddeclusage_positiont"></a>Scheitelpunktdeklarationen ohne D3DDECLUSAGE \_ POSITIONT

Runtime überprüft die Erstellung von Deklarationen. Im Folgenden finden Sie die allgemeinen Regeln dafür, welche Deklarationen legal sind.

-   Alle Scheitelpunktelemente für einen Stream müssen aufeinanderfolgende und nach Offset sortiert sein.
-   Der Streamoffset muss DWORD-ausgerichtet sein.
-   Das gleiche Paar (Nutzung, Nutzungsindex) sollte nur einmal aufgeführt werden.
-   Wenn D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET festgelegt ist, dann
    -   Mehrere Scheitelpunktelemente können den gleichen Offset in einem Stream gemeinsam haben.
    -   Die Scheitelpunktelemente können alle verschiedene Typen haben, die unterschiedliche Größen haben können.
    -   Die Scheitelpunktelemente können sich willkürlich überlappen. Beispielsweise kann ein Element an einer Position eines Streams beginnen, der sich gleichzeitig in der Mitte eines anderen Elements befindet.
    -   Vertexelemente dürfen einen Streamoffset in beliebiger Reihenfolge haben.
-   Die Anzahl der Scheitelpunktelemente darf nicht größer als 64 sein.
-   UsageIndex sollte im Bereich \[ von 0 bis 15 \] liegen.
-   Die Deklaration, die mit der DrawPrimitive-API verwendet wird, darf keine anderen Scheitelpunktelemente als D3DDECLMETHOD \_ DEFAULT, D3DDECLMETHOD \_ LOOKUPPRESAMPLED oder D3DDECLMETHOD \_ LOOKUP enthalten.
-   Die Deklaration, die D3DDECLMETHOD LOOKUP oder LOOKUPPRESAMPLED enthält, sollte nur mit der \_ programmierbaren Vertexpipeline verwendet werden.
-   Die Deklaration, die mit der DrawRectPatch/DrawTriPatch-API verwendet wird, darf keine Scheitelpunktelemente mit D3DDECLMETHOD \_ LOOKUPPRESAMPLED oder D3DDECLMETHOD \_ LOOKUP enthalten.
-   Die Deklaration sollte nur ein Element mit der D3DDECLMETHOD \_ LOOKUP- oder D3DDECLMETHOD \_ LOOKUPPRESAMPLED-Methode enthalten.
-   Deklarationen mit D3DDECLMETHOD LOOKUP oder \_ D3DDECLMETHOD LOOKUPPRESAMPLED dürfen keine anderen Elemente als \_ D3DDECLMETHOD DEFAULT enthalten, da die Verschiebungszuordnung nur für \_ N-Patches erfolgt.
-   Vertexelemente mit D3DDECLMETHOD LOOKUP oder \_ D3DDECLMETHOD LOOKUPPRESAMPLED können nur mit der \_ Semantik (D3DDECLUSAGE SAMPLE, n) und umgekehrt verwendet \_ werden.
-   Wenn ein Vertexelement mit der D3DDECLMETHOD LOOKUP-Methode über einen Streamindex und einen Offset eines bereits vorhandenen Vertexelements verfügt, sollte dieses \_ Vertexelement denselben Datentyp haben.
-   Ein Vertexelement mit der D3DDECLMETHOD \_ LOOKUP-Methode muss den Datentyp D3DDECLTYPE \_ FLOAT2/3/4 haben.
-   Vertexelemente mit den Typen D3DDECLMETHOD \_ CROSSUV, D3DDECLMETHOD PARTIALU und \_ D3DDECLMETHOD PARTIALV sollten einen Offset eines Scheitelpunktelements mit einem kompatiblen Datentyp \_ haben.
-   Ein Vertexelement mit der Methode D3DDECLMETHOD UV oder \_ D3DDECLMETHOD LOOKUPPRESAMPLED muss den Typ \_ D3DDECLTYPE UNUSED, den Streamindex 0 (null) und den Streamoffset 0 \_ (null) haben.
-   Deklarationen mit den Methoden D3DDECLMETHOD \_ UV, D3DDECLMETHOD PARTIALU und \_ D3DDECLMETHOD PARTIALV können nur \_ mit DrawRectPatch verwendet werden.
-   Die Verwendung von D3DDECLUSAGE TESSFACTOR sollte nur mit dem \_ Datentyp D3DDECLTYPE FLOAT1 und dem \_ Verwendungsindex 0 verwendet werden.
-   Wenn eine Deklaration für Mosaik (DrawRectPatch, DrawTriPatch, N-Patches) verwendet wird, muss der Datentyp kleiner oder gleich D3DDECLTYPE \_ SHORT4 sein.
-   Deklarationen, die Methoden enthalten, die bestimmte Gerätefunktionen erfordern (z. B. Verschiebungszuordnung, RT-Patches), können nur erstellt werden, wenn das Gerät sie unterstützt.
-   Eine Scheitelpunktdeklaration, die zum Zeichnen von Punkten und Linien verwendet wird, darf keine anderen Methoden als D3DDECLMETHOD \_ DEFAULT haben.
-   Die Deklarationen, die erstellt werden können, hängen auch von den Treiberfunktionen ab.

## <a name="driver-considerations"></a>Überlegungen zum Treiber

### <a name="pre-direct3d-9-drivers"></a>Pre-Direct3D 9-Treiber

-   Die Eingabedeklaration muss in eine gültige FVF übersetzbar sein (sie muss die gleiche Reihenfolge von Scheitelpunktelementen und deren Datentypen haben).
-   Lücken in Texturkoordinaten sind nicht zulässig. Dies bedeutet, dass bei einem Scheitelpunktelement mit (D3DDECLUSAGE TEXCOORD, n) auch ein Scheitelpunktelement mit \_ (D3DDECLUSAGE \_ TEXCOORD, n-1) enthalten sein sollte.

### <a name="direct3d-9-drivers-without-pixel-shader-version-3-support"></a>Direct3D 9-Treiber ohne Unterstützung für Pixels shader Version 3

-   Die Eingabedeklaration muss in eine gültige FVF übersetzbar sein (sie muss die gleiche Reihenfolge von Scheitelpunktelementen und deren Datentypen haben).
-   Lücken in Texturkoordinaten sind zulässig.

### <a name="direct3d-9-drivers-with-pixel-shader-version-3-support"></a>Direct3D 9-Treiber mit Unterstützung für Pixel-Shader Version 3

Allgemeinere Deklarationen sind zulässig.

-   Scheitelpunktelemente können in beliebiger Reihenfolge sein und über beliebige Datentypen verfügen.
-   Mehrere Scheitelpunktelemente können denselben Streamoffset gemeinsam verwenden und gleichzeitig einen anderen Typ haben, wenn D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET vom Gerät festgelegt wird.

## <a name="vertex-declaration-usage-with-the-programmable-vertex-pipeline"></a>Verwendung der Scheitelpunktdeklaration mit der programmierbaren Vertexpipeline

-   Zur Zeichnen-Zeit sucht Direct3D in der aktuellen Vertexdeklaration und der aktuellen Vertex-Shaderfunktion nach der gleichen Kombination aus Nutzungs- und Nutzungsindex. Wenn die Kombination gefunden wird, wird das Register aus der Shaderfunktions-DCL als Ziel für das Scheitelpunktelement verwendet.
-   Wenn ein Scheitelpunktelement in der aktuellen Scheitelpunktdeklaration über eine Verwendung verfügt, die im aktuellen Vertex-Shader nicht gefunden wird, wird dieses Vertexelement ignoriert.
-   Bei Verwendung einer Vertex-Shaderversion unter 2.0 muss die im Shadercode erwähnte Semantik in der Deklaration vorhanden sein, die zur Zeichnen-Zeit gebunden ist. Wenn Vertex-Shader 2.0 und höher verwendet werden, ist diese Einschränkung, die anwendungen die Verwendung verschiedener Vertexdeklarationen mit demselben Vertex-Shader ermöglicht, nicht vorhanden. Dies ist nützlich, wenn ein Vertex-Shader Eingabedaten basierend auf statischen Bedingungen liest. Vertex-Shaderregister, die nicht initialisiert wurden, verfügen daher über nicht definierte Werte.

Es gibt zusätzliche Einschränkungen bei der Verwendung mit Hardwarevertexverarbeitung auf einem DirectX 8-Treiber:

-   Scheitelpunktelemente können sich nicht überlappen oder denselben Offset gemeinsam haben.
-   Datentypen sind auf das beschränkt, was der DirectX 8-Treiber verstehen kann.

CreateVertexDeclaration kann fehlschlagen, wenn die bereitgestellte Deklaration nicht in eine DirectX 8-Deklaration konvertiert werden kann. Bei einem Gerät im gemischten Modus kommt es zu diesem Fehler zur Draw-Zeit, da dies der einzige Zeitpunkt ist, an dem bekannt ist, ob dieser Shader mit Hardware- oder \* Softwarevertexverarbeitung verwendet wird.

## <a name="vertex-declaration-usage-with-the-fixed-function-pipeline"></a>Verwendung der Scheitelpunktdeklaration mit der Festen Funktionspipeline

Es können nur Deklarationen verwendet werden, die den folgenden Regeln entsprechen:

-   Es sollten keine Lücken zwischen Scheitelpunktelementen bestehen (SKIP war in einer DirectX 8-Deklaration, die für die feste Funktionspipeline verwendet wird, nicht zulässig).
-   Semantic (D3DDECLUSAGE POSITION, 0) muss angegeben werden und muss \_ den Datentyp D3DDECLTYPE \_ FLOAT3 haben.
-   Ein Vertexelement mit der D3DDECLMETHOD UV-Methode muss die Verwendung \_ von D3DDECLUSAGE \_ TEXCOORD oder D3DDECLUSAGE \_ BLENDWEIGHT angeben.
-   Ein Vertexelement mit der Methode D3DDECLMETHOD PARTIALU, PARTIALV oder CROSSUV kann nur mit \_ \_ \_ D3DDECLUSAGE POSITION, NORMAL, BLENDWEIGHT oder TEXCOORD verwendet werden und muss den Eingabetyp \_ \_ \_ \_ D3DDECLTYPE \_ FLOAT3 verwenden.

Wenn eine Deklaration mit Hardwarevertexverarbeitung auf einem DirectX 8-Treiber verwendet wird, konvertiert die Direct3D-Runtime sie mit den folgenden Regeln in eine DirectX 8-deklaration:

-   Scheitelpunktelemente können nicht den gleichen Offset in einem Stream gemeinsam haben und dürfen sich nicht überlappen.
-   Der Datentyp muss kleiner oder gleich D3DDECLTYPE \_ SHORT4 sein.
-   Es sind nur die folgenden Methoden zulässig: D3DDECLMETHOD \_ DEFAULT, D3DDECLMETHOD \_ CROSSUV und D3DDECLMETHOD \_ UV
-   Die Zuordnung zwischen [einer Direct3D 9-Deklaration und einer Direct3D 8-Deklaration (Direct3D 9)](mapping-between-a-directx-9-declaration-and-directx-8.md) zeigt, welche Direct3D 9-Semantik in eine DirectX 8-Deklaration konvertiert werden könnte. Usage und UsageIndex werden in einen Registerwert konvertiert.
-   Wenn eine Deklaration n Scheitelpunktelemente enthält und 0 –m (m < n) einer FVF (Elemente, die in Zuordnung zwischen einer Direct3D-Deklaration und [FVF-Codes (Direct3D 9)](mapping-between-a-directx-9-declaration-and-fvf-codes.md)beschrieben sind), m + 1 jedoch nicht, dann:
    -   Wenn eines von m + 2 bis n - 1 Scheitelpunktelementen FVF/dx8decl zuordnen, ist die Deklaration ungültig.
    -   Die Elemente 0 in m werden konvertiert (von der Runtime für DirectX 8 und ältere Treiber und von den Direct3D 9-Treibern) mithilfe der Zuordnung zwischen einer Direct3D-Deklaration und [FVF-Codes (Direct3D 9),](mapping-between-a-directx-9-declaration-and-fvf-codes.md)m + 1, m + 2 bis n - 1 werden zusammenhängenden Texcoord(k), texcoord(k+1) zugeordnet, beginnend mit jedem Texcoord in Elementen 0 - m.
    -   Es wird davon ausgegangen, dass der Datentyp bei einem zugeordneten Texcoord float 1234 ist und dabei den Datentyp ersetzt, den das aktuelle Element enthält (jedoch die \[ \] gleiche Größe). Daher kann der vorhandene Datentyp etwas sein, das nicht unter Zuordnung zwischen einer Direct3D-Deklaration und [FVF-Codes (Direct3D 9) enthalten ist.](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
    -   Wenn k 8 erreicht, ist die Deklaration für FVF/dx8decl ungültig.
    -   Wenn Zuordnungen zu Texcoords aufgetreten sind, muss die gesamte Deklaration keine Elemente mit einer anderen Generierungsmethode als DEFAULT enthalten, oder die Deklaration ist für FVF/dx8decl ungültig.

## <a name="using-vertex-declarations-with-processvertices"></a>Verwenden von Scheitelpunktdeklarationen mit ProcessVertices

Eine Scheitelpunktdeklaration kann verwendet werden, um die Ausgabe von ProcessVertices zu beschreiben. Diese Deklaration sollte den folgenden Regeln entsprechen:

-   Nur Stream 0 muss verwendet werden.
-   Nur D3DDECLMETHOD \_ DEFAULT-Methoden sind zulässig.
-   Es können nur die D3DDECLTYPE \_ FLOATn- oder D3DDECLTYPE \_ D3DCOLOR-Datentypen verwendet werden.
-   Scheitelpunktelemente können nicht den gleichen Offset gemeinsam haben oder sich überlappen.
-   Vertexelemente mit (D3DDECLUSAGE \_ POSITION, 0) oder (D3DDECLUSAGE \_ POSITIONT,0) sind nicht erforderlich.
-   Vertexelemente mit (D3DDECLUSAGE \_ POSITION, 0) und (D3DDECLUSAGE \_ POSITIONT,0) können nicht in derselben Deklaration vorhanden sein.
-   Der aktuelle Vertex-Shader muss Version 3.0 oder höher sein, wenn eine solche Deklaration verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunktdeklaration](vertex-declaration.md)
</dt> </dl>

 

 




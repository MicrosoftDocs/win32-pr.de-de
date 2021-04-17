---
title: Mosaik Phasen
description: Die Direct3D 11-Laufzeit unterstützt drei neue Phasen, die das Mosaik implementieren, das untergeordnete Oberflächen auf niedriger Detailebene in die GPU konvertiert.
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aacb48ccc2c95ab93ba4f34212e654880d9a369
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "104316664"
---
# <a name="tessellation-stages"></a>Mosaik Phasen

Die Direct3D 11-Laufzeit unterstützt drei neue Phasen, die das Mosaik implementieren, das untergeordnete Oberflächen auf niedriger Detailebene in die GPU konvertiert. Mosaik Kacheln (oder unterbrechen) hoch geordnete Oberflächen in geeignete Strukturen zum Rendern.

Durch die Implementierung von Mosaik in Hardware kann eine Grafik Pipeline niedrigere Detailmodelle auswerten (niedrigere Polygon Anzahl) und die Darstellung ausführlicher darstellen. Obwohl das Software Mosaik durchgeführt werden kann, kann durch Hardware implementiertes Mosaik eine unglaubliche Menge an visuellen Details generieren (einschließlich der Unterstützung für die Verschiebungs Zuordnung), ohne die visuellen Details zu den Modellgrößen hinzuzufügen und die Aktualisierungs Raten zu erhöhen.

-   [Vorteile der Mosaik Funktionen](#tessellation-benefits)
-   [Neue Pipeline Stufen](#new-pipeline-stages)
    -   [Hülle-Shader-Phase](#hull-shader-stage)
    -   [Mosaik Phase](#tessellator-stage)
    -   [Domäne-Shader-Phase](#domain-shader-stage)
-   [APIs für die Initialisierung von Mosaik Phasen](#apis-for-initializing-tessellation-stages)
-   [Vorgehensweise:](#how-tos)
-   [Zugehörige Themen](#related-topics)

## <a name="tessellation-benefits"></a>Vorteile der Mosaik Funktionen

Mosaik

-   Spart Menge Arbeitsspeicher und Bandbreite, sodass eine Anwendung detailliertere Oberflächen aus Modellen mit niedriger Auflösung Rendering kann. Das Mosaik Verfahren, das in der Pipeline Direct3D 11 implementiert ist, unterstützt auch die Verschiebungs Zuordnung, die beeindruckende Mengen von Oberflächendetails liefern kann.
-   Unterstützt skalierbare Renderingverfahren, z. b. fortlaufende oder Ansichts abhängige Detailebenen, die im Handumdrehen berechnet werden können.
-   Verbessert die Leistung, indem teure Berechnungen mit niedrigerer Häufigkeit ausgeführt werden (Berechnungen in einem Modell mit niedrigerer Detail Ausführung). Dies kann das Kombinieren von Berechnungen mithilfe von Blend-Formen oder Morph-Zielen für realistische Animationen oder Physik Berechnungen für die Konflikterkennung oder die Dynamik des Soft Texts einschließen.

Die Pipeline Direct3D 11 implementiert das Mosaik in Hardware, das die Arbeit von der CPU auf die GPU auslädt. Dies kann zu sehr großen Leistungsverbesserungen führen, wenn eine Anwendung eine große Anzahl von Morph-Zielen und/oder komplexeren Modelle für das Skinning/-debuggingmodell implementiert. Um auf die neuen Mosaik Features zuzugreifen, müssen Sie sich über einige neue Pipeline Phasen informieren.

## <a name="new-pipeline-stages"></a>Neue Pipeline Stufen

Das Mosaik verwendet die GPU, um eine ausführlichere Oberfläche aus einer Oberfläche zu berechnen, die aus Quad-Patches, Dreiecks Patches oder Isolationen erstellt wird. Um der hoch geordneten Oberfläche zu nähern, wird jeder Patch mithilfe von Mosaik Faktoren in Dreiecke, Punkte oder Zeilen unterteilt. Die Pipeline Direct3D 11 implementiert Mosaik mithilfe von drei neuen Pipeline Stufen:

-   [Hull-Shader-Phase](#hull-shader-stage) : eine programmierbare Shader-Stufe, die einen Geometry-Patch (und Patch-Konstanten) erzeugt, die den einzelnen Eingabe Patches (Quad, Dreieck oder Line) entsprechen.
-   Mosaik [Phase](#tessellator-stage) : eine Funktion für eine Fixed-Funktions Pipeline, mit der ein Samplings-Muster der Domäne erstellt wird, das den Geometry-Patch darstellt und einen Satz kleinerer Objekte (Dreiecke, Punkte oder Linien) generiert, die diese Beispiele verbinden.
-   [Domäne-Shader-Phase](#domain-shader-stage) : eine programmierbare Shader-Stufe, die die Vertex-Position berechnet, die den einzelnen Domänen Beispielen entspricht.

Im folgenden Diagramm werden die neuen Phasen der Pipeline Direct3D 11 hervorgehoben.

![Diagramm der Direct3D 11-Pipeline, mit der die Stufen "Hull-Shader", "Mosaik Bereich" und "Domänen-Shader" hervorgehoben werden](images/d3d11-pipeline-stages-tessellation.png)

Das folgende Diagramm zeigt den Fortschritt durch die Mosaik Phasen. Der Fortschritt beginnt mit der Oberfläche für die Unterteilung mit niedriger Detailgenauigkeit. Im nächsten Schritt wird der Eingabe Patch mit dem entsprechenden Geometry-Patch, den Domänen Beispielen und den Dreiecken hervorgehoben, mit denen diese Beispiele verbunden werden. Der Fortschritt verdeutlicht schließlich die Scheitel Punkte, die diesen Beispielen entsprechen.

![Diagramm der Mosaik Entwicklung](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Hull-Shader Phase

Ein Hull-Shader, der einmal pro Patch aufgerufen wird, wandelt Eingabe Steuerungs Punkte um, die eine niedrige Reihenfolge in Steuerungs Punkte definieren, aus denen ein Patch besteht. Außerdem werden einige pro-Patch-Berechnungen durchführt, um Daten für die Mosaik Phase und die Domänen Phase bereitzustellen. Auf der einfachsten Blackbox-Ebene würde die Hülle-Shader-Stufe in etwa wie das folgende Diagramm aussehen.

![Diagramm der Hülle-Shader-Phase](images/d3d11-hull-shader.png)

Ein Hull-Shader wird mit einer HLSL-Funktion implementiert und verfügt über die folgenden Eigenschaften:

-   Die Shader-Eingabe liegt zwischen 1 und 32 Kontrollpunkten.
-   Die Shader-Ausgabe liegt zwischen 1 und 32 Kontrollpunkten, unabhängig von der Anzahl der Mosaik Faktoren. Die Kontrollpunkte, die von einem Hull-Shader ausgegeben werden, können von der Domänen-Shader-Stufe verwendet werden. Patch-konstantendaten können von einem Domänen-Shader verwendet werden. Mosaik Faktoren können vom Domänen-Shader und der Mosaik Phase genutzt werden.
-   Die Mosaik Faktoren legen fest, wie viel zwischen den einzelnen Patches unterteilt werden soll.
-   Der Shader deklariert den Zustand, der für die Mosaik Phase erforderlich ist. Hierzu gehören Informationen wie z. b. die Anzahl der Kontrollpunkte, der Typ der Patchfläche und der Partitionierungstyp, der beim Mosaik Vorgang verwendet werden soll. Diese Informationen werden in der Regel am Anfang des Shader-Codes als Deklarationen angezeigt.
-   Wenn in der Hull-Shader-Stufe ein beliebiger Edge-Mosaik Faktor auf = 0 oder NaN festgelegt wird, wird der Patch als "culled" festgelegt. Folglich kann die Mosaik Phase nicht ausgeführt werden, und der Domänen-Shader wird nicht ausgeführt, und für diesen Patch wird keine sichtbare Ausgabe erzeugt.

Auf einer tieferen Ebene arbeitet ein Hull-Shader tatsächlich in zwei Phasen: eine Steuerungspunkt Phase und eine patchkonstantenphase, die parallel von der Hardware ausgeführt werden. Der HLSL-Compiler extrahiert die Parallelität in einem Hull-Shader und codiert Sie in Bytecode, der die Hardware steuert.

-   Die Steuerungspunkt Phase wird für jeden Steuerungspunkt einmal betrieben, die Kontrollpunkte für einen Patch gelesen und ein Ausgabe Steuerungspunkt (durch eine controlpointid identifiziert) erzeugt.
-   Die Patch-Konstante-Phase arbeitet einmal pro Patch, um Edge-Mosaik Faktoren und andere pro-Patch-Konstanten zu generieren. Intern können viele patchkonstantenphasen gleichzeitig ausgeführt werden. Die patchkonstantenphase hat schreibgeschützten Zugriff auf alle Eingabe-und Ausgabe Steuerungs Punkte.

Hier ist ein Beispiel für einen Hull-Shader:


```
[patchsize(12)]
[patchconstantfunc(MyPatchConstantFunc)]
MyOutPoint main(uint Id : SV_ControlPointID,
     InputPatch<MyInPoint, 12> InPts)
{
     MyOutPoint result;
     
     ...
     
     result = TransformControlPoint( InPts[Id] );

     return result;
}
```



Ein Beispiel, das einen Hull-Shader erstellt, finden Sie unter Gewusst [wie: Erstellen eines Hull-Shaders](direct3d-11-advanced-stages-hull-shader-create.md).

### <a name="tessellator-stage"></a>Mosaik Phase

Der Mosaik Prozess ist eine Stufe mit fester Funktionsweise, die durch das Binden eines Hull-Shaders an die Pipeline initialisiert wird (siehe Gewusst [wie: Initialisieren der Mosaik Stufe](direct3d-11-advanced-stages-tessellator-initialize.md)). Der Zweck der Mosaik Stufe besteht darin, eine Domäne (Quad, Tri oder Line) in viele kleinere Objekte (Dreiecke, Punkte oder Linien) zu unterteilen. Der Mosaik-Mosaik Kachel eine kanonische Domäne in einem normalisierten (null-zu-eins-) Koordinatensystem. Beispielsweise wird eine Quad-Domäne zu einem Einheits Quadrat.

Der Mosaik Prozess arbeitet einmal pro Patch mit den Mosaik Faktoren (die angeben, wie fein die Domäne verarbeitet werden soll) und dem Partitionierungstyp (der den Algorithmus angibt, der zum Aufteilen eines Patches verwendet wird), der aus der Hülle-Shader-Stufe übergangen wird. Der Mosaik Prozess gibt UV-Koordinaten (und optional w) und die Oberflächen Topologie für die Domäne-Shader-Phase aus.

Intern arbeitet der Mosaik Prozess in zwei Phasen:

-   In der ersten Phase werden die Mosaik Faktoren verarbeitet, Rundungs Probleme behoben, die Verarbeitung sehr kleiner Faktoren, das reduzieren und Kombinieren von Faktoren mithilfe der 32-Bit-Gleit Komma Arithmetik durchgesetzt.
-   In der zweiten Phase werden Punkt-oder topologielisten basierend auf dem ausgewählten Partitionierungstyp generiert. Dabei handelt es sich um die Hauptaufgabe der Mosaik Phase, die 16-Bit-Bruchzahlen mit fest Komma-Arithmetik verwendet. Mit fester Punkt Arithmetik wird die Hardwarebeschleunigung unter Beibehaltung zulässiger Genauigkeit ermöglicht. Bei einem 64-Meter weiten Patch kann diese Genauigkeit z. b. Punkte bei einer Auflösung von 2 mm platzieren.



| Partitionierungstyp | Range                       |
|----------------------|-----------------------------|
| \_ungerade Bruchzahlen      | \[1... 63\]                  |
| sogar Bruchteile \_     | Mosaik Faktor Bereich: \[ 2.. 64\] |
| integer              | Mosaik Faktor Bereich: \[ 1.. 64\] |
| pow2                 | Mosaik Faktor Bereich: \[ 1.. 64\] |



 

### <a name="domain-shader-stage"></a>Domain-Shader Phase

Ein Domänen-Shader berechnet die Scheitelpunkt Position eines unterteilten Punkts im Ausgabe Patch. Ein Domänen-Shader wird einmal pro Tess-Phasen-Ausgabepunkt ausgeführt und hat schreibgeschützten Zugriff auf die in der Mosaik Phase ausgegebene UV-Koordinaten, den Hull-Shader-Ausgabe Patch und die Hull-Shader-Ausgabe Patch-Konstanten, wie im folgenden Diagramm gezeigt.

![Diagramm der Domäne-Shader-Phase](images/d3d11-domain-shader.png)

Zu den Eigenschaften des Domänen-Shader gehören:

-   Ein Domänen-Shader wird einmal pro Ausgabe Koordinate aus der Mosaik Phase aufgerufen.
-   Ein Domänen-Shader nutzt Ausgabe Steuerungs Punkte aus der Hull-Shader-Stufe.
-   Ein Domänen-Shader gibt die Position eines Scheitel Punkts aus.
-   Eingaben sind die Hull-shaderausgaben, einschließlich der Steuerungs Punkte, der patchkonstanten Daten und der Mosaik Faktoren. Die Mosaik Faktoren können die Werte enthalten, die vom Mosaik der fixierten Funktion und die unformatierten Werte verwendet werden (z. b. vor dem Runden des ganzzahligen Mosaik Beispiels), was beispielsweise die geomsche Verbrechung vereinfacht.

Nachdem der Domänen-Shader abgeschlossen ist, ist das Mosaik abgeschlossen, und die Pipeline Daten werden mit der nächsten Pipeline Phase (Geometry-Shader, Pixelshader usw.) fortgesetzt. Ein Geometry-Shader, der primitive mit der Verwendung erwartet (z. b. 6 Scheitel Punkte pro Dreieck), ist nicht gültig, wenn das Mosaik aktiv ist (Dies führt zu einem nicht definierten Verhalten, das von der debugschicht beklagt wird).

Im folgenden finden Sie ein Beispiel für einen Domänen-Shader:


```
void main( out    MyDSOutput result, 
           float2 myInputUV : SV_DomainPoint, 
           MyDSInput DSInputs,
           OutputPatch<MyOutPoint, 12> ControlPts, 
           MyTessFactors tessFactors)
{
     ...

     result.Position = EvaluateSurfaceUV(ControlPoints, myInputUV);
}
```



## <a name="apis-for-initializing-tessellation-stages"></a>APIs für die Initialisierung von Mosaik Phasen

Das Mosaik ist mit zwei neuen programmierbaren shaderphasen implementiert: einem Hull-Shader und einem Domänen-Shader. Diese neuen shaderphasen werden mit HLSL-Code programmiert, der in Shader Model 5 definiert ist. Die neuen shaderziele lauten: HS \_ 5 \_ 0 und DS \_ 5 \_ 0. Wie alle programmierbaren shaderphasen wird Code für die Hardware aus kompilierten Shadern extrahiert, die an die Laufzeit geleitet werden, wenn Shader mithilfe von APIs wie [**dssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) und [**hssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)an die Pipeline gebunden werden. Zuerst muss der Shader jedoch mit APIs wie z. b. " [**kreatehullshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) " und " [**kreatedomainshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)" erstellt werden.

Aktivieren Sie das Mosaik, indem Sie einen Hull-Shader erstellen und ihn an die Hülle-Shader-Stufe binden (Dadurch wird die Mosaik Phase automatisch eingerichtet). Um die abschließenden Vertex-Positionen aus den Mosaik Patches zu generieren, müssen Sie auch einen Domänen-Shader erstellen und an die Domäne-Shader-Stufe binden. Sobald das Mosaik aktiviert ist, muss die Dateneingabe für die Eingabe Assembler-Stufe Patchdaten sein. Das heißt, die Topologie des Eingabe Assemblers muss eine patchkonstante-Topologie aus [**D3D11 \_ primitiver \_ topologiesatz**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) mit [**iasetprimitivetopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)sein.

Um das Mosaik zu deaktivieren, legen Sie den Hull-Shader und den Domänen-Shader auf **null** fest. Weder die Geometry-Shader-Phase noch die Stream-Output-Phase kann die Ausgabe von Hull-Shader-Ausgabe Steuer Punkten oder Patchdaten lesen.

-   Neue Topologien für die Eingabe-Assembler-Phase, bei denen es sich um Erweiterungen für diese Enumeration handelt.

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    Die Topologie wird mithilfe von [ **iasetprimitivetopology** auf die Eingabe-Assembler-Phase festgelegt.](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   Die neuen programmierbaren shaderphasen erfordern natürlich, dass ein anderer Zustand festgelegt wird, um konstante Puffer, Beispiele und Shaderressourcen an die entsprechenden Pipeline Stufen zu binden. Diese neuen ID3D11Device-Methoden werden zum Festlegen dieses Zustands implementiert.
    -   [**Dsgetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers)
    -   [**Dsgetsamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetsamplers)
    -   [**Dsgetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshader)
    -   [**Dsgetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshaderresources)
    -   [**Dssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers)
    -   [**Dssetsamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetsamplers)
    -   [**Dssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)
    -   [**Dssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshaderresources)
    -   [**Hsgetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers)
    -   [**Hsgetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshaderresources)
    -   [**Hsgetsamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetsamplers)
    -   [**Hsgetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshader)
    -   [**Hssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers)
    -   [**Hssetsamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetsamplers)
    -   [**Hssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)
    -   [**Hssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshaderresources)

## <a name="how-tos"></a>Vorgehensweise:

Die Dokumentation enthält auch Beispiele für die Initialisierung der Mosaik Stufen.



| Element                                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[Gewusst wie: Erstellen eines Hull-Shaders](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | Erstellen Sie einen Hull-Shader.<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[Gewusst wie: Entwerfen eines Hull-Shaders](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | Entwerfen Sie einen Hull-Shader.<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[Gewusst wie: Initialisieren der Mosaik Phase](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | Initialisieren Sie die Mosaik Phase.<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[Vorgehensweise: Erstellen eines Domänen-Shader](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | Erstellen Sie einen Domänen-Shader.<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[Vorgehensweise: Entwerfen eines Domänen-Shader](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | Erstellen Sie einen Domänen-Shader.<br/>            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafik Pipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 


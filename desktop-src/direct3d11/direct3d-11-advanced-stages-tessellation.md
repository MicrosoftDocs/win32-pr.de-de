---
title: Mosaikstufen
description: Die Direct3D 11-Runtime unterstützt drei neue Phasen, die das Mosaik implementieren, das Unterteilungsoberflächen mit geringem Detail in primitivere Detailtypen auf der GPU konvertiert.
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d272ad1db53c6e70a856255c1826f4867f069897b42da0219cd334d48226d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099232"
---
# <a name="tessellation-stages"></a>Mosaikstufen

Die Direct3D 11-Runtime unterstützt drei neue Phasen, die das Mosaik implementieren, das Unterteilungsoberflächen mit geringem Detail in primitivere Detailtypen auf der GPU konvertiert. Mosaikkacheln (oder unterbricht) hochwertige Oberflächen in geeignete Strukturen für das Rendering.

Durch die Implementierung des Mosaiks in der Hardware kann eine Grafikpipeline Modelle mit niedrigeren Details (niedrigere Polygonanzahl) auswerten und detaillierter rendern. Während das Mosaik von Software durchgeführt werden kann, kann das von der Hardware implementierte Mosaik eine enorme Menge visueller Details generieren (einschließlich unterstützung der Verschiebungszuordnung), ohne die visuellen Details zu den Modellgrößen und Lähmungsaktualisierungsraten hinzufügen zu müssen.

-   [Mosaikvorteile](#tessellation-benefits)
-   [Neue Pipelinestufen](#new-pipeline-stages)
    -   [Hüllen-Shader-Stufe](#hull-shader-stage)
    -   [Mosaikphase](#tessellator-stage)
    -   [Domänen-Shader-Phase](#domain-shader-stage)
-   [APIs zum Initialisieren von Mosaikstufen](#apis-for-initializing-tessellation-stages)
-   [So geht's:](#how-tos)
-   [Zugehörige Themen](#related-topics)

## <a name="tessellation-benefits"></a>Mosaikvorteile

Tessellation:

-   Spart viel Arbeitsspeicher und Bandbreite, wodurch eine Anwendung detailliertere Oberflächen aus Modellen mit niedriger Auflösung rendern kann. Die in der Direct3D 11-Pipeline implementierte Mosaiktechnik unterstützt auch die Verschiebungszuordnung, die beeindruckende Mengen an Oberflächendetails erzeugen kann.
-   Unterstützt skalierbare Renderingtechniken, z. B. fortlaufende oder Ansichtsabhängige Detailebenen, die direkt berechnet werden können.
-   Verbessert die Leistung, indem teure Berechnungen mit geringerer Häufigkeit durchgeführt werden (Berechnungen für ein Modell mit niedrigeren Details). Dies kann z. B. Überblendungsberechnungen mithilfe von Mischungsformen oder Morphzielen für realistische Animationen oder physikalische Berechnungen zur Kollisionserkennung oder soft body dynamics umfassen.

Die Direct3D 11-Pipeline implementiert Mosaik in Hardware, die die Arbeit von der CPU auf die GPU auslädt. Dies kann zu sehr großen Leistungsverbesserungen führen, wenn eine Anwendung eine große Anzahl von Morph-Zielen und/oder anspruchsvollere Skinning-/Modellmodelle implementiert. Um auf die neuen Mosaikfeatures zugreifen zu können, müssen Sie sich über einige neue Pipelinephasen informieren.

## <a name="new-pipeline-stages"></a>Neue Pipelinestufen

Das Mosaik verwendet die GPU, um eine detailliertere Oberfläche aus einer Oberfläche zu berechnen, die aus Quad-Patches, Dreieckspatches oder Isolinien erstellt wurde. Zur Ungefährung der hoch geordneten Oberfläche wird jeder Patch unter Verwendung von Mosaikfaktoren in Dreiecke, Punkte oder Linien unterteilt. Die Direct3D 11-Pipeline implementiert das Mosaik mithilfe von drei neuen Pipelinestufen:

-   [Hülle-Shader-Stufe:](#hull-shader-stage) Eine programmierbare Shaderstufe, die einen Geometriepatch (und Patchkonst constants) erzeugt, die jedem Eingabepatch (Quad, Dreieck oder Linie) entsprechen.
-   [Mosaikphase:](#tessellator-stage) Eine feste Funktionspipelinephase, die ein Samplingmuster der Domäne erstellt, das den Geometriepatch darstellt und eine Reihe kleinerer Objekte (Dreiecke, Punkte oder Linien) generiert, die diese Beispiele verbinden.
-   [Domänen-Shader-Stufe:](#domain-shader-stage) Eine programmierbare Shaderphase, die die Scheitelpunktposition berechnet, die den einzelnen Domänenbeispielen entspricht.

Das folgende Diagramm zeigt die neuen Phasen der Direct3D 11-Pipeline.

![Diagramm der Direct3d 11-Pipeline, die die Phasen "Hülle-Shader", "Tessellator" und "Domänen-Shader" hervor hebt](images/d3d11-pipeline-stages-tessellation.png)

Das folgende Diagramm zeigt den Fortschritt durch die Mosaikphasen. Der Fortschritt beginnt mit der Unterteilungsoberfläche mit niedrigen Details. Der Fortschritt hebt als Nächstes den Eingabepatch mit dem entsprechenden Geometriepatch, Domänenbeispielen und Dreiecken hervor, die diese Beispiele verbinden. Der Fortschritt hebt schließlich die Scheitelpunkte hervor, die diesen Beispielen entsprechen.

![Diagramm des Mosaikfortschritts](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Hull-Shader Stage

Ein Hüllen-Shader, der einmal pro Patch aufgerufen wird, transformiert Eingabekontrollpunkte, die eine oberfläche niedriger Ordnung definieren, in Kontrollpunkte, aus denen ein Patch besteht. Außerdem werden einige Berechnungen pro Patch zur Bereitstellung von Daten für die Mosaikphase und die Domänenphase erstellt. Auf der einfachsten Blackbox-Ebene würde die Phase des Hüllen-Shaders in etwa wie im folgenden Diagramm aussehen.

![Diagramm der Hüllen-Shader-Stufe](images/d3d11-hull-shader.png)

Ein Hüllen-Shader wird mit einer HLSL-Funktion implementiert und verfügt über die folgenden Eigenschaften:

-   Die Shadereingabe liegt zwischen 1 und 32 Kontrollpunkten.
-   Die Shaderausgabe liegt unabhängig von der Anzahl der Mosaikfaktoren zwischen 1 und 32 Kontrollpunkten. Die Steuerpunkteausgabe eines Hüllen-Shaders kann von der Domänen-Shader-Stufe verwendet werden. Patchkonst constant data can be consumed by a domain shader; (Patchkonst constant data can be consumed by a domain shader; Patchkonst constant data can be consumed by Mosaikfaktoren können vom Domänen-Shader und der Mosaikphase verwendet werden.
-   Mosaikfaktoren bestimmen, wie viel die einzelnen Patches subdiviert werden.
-   Der Shader deklariert den für die Mosaikphase erforderlichen Zustand. Dies schließt Informationen wie die Anzahl der Kontrollpunkte, den Typ der Patchgesicht und den Typ der Partitionierung ein, die beim Mosaik verwendet werden soll. Diese Informationen werden in der Regel als Deklarationen am Anfang des Shadercodes angezeigt.
-   Wenn die Phase des Hüllen-Shaders einen Edge-Mosaikfaktor auf = 0 oder NaN setzt, wird der Patch gecullt. Daher kann die Mosaikphase ausgeführt werden, der Domänen-Shader wird nicht ausgeführt, und für diesen Patch wird keine sichtbare Ausgabe erzeugt.

Auf einer tieferen Ebene arbeitet ein Hüllen-Shader tatsächlich in zwei Phasen: einer Kontrollpunktphase und einer Patchkonst konstanten Phase, die parallel von der Hardware ausgeführt werden. Der HLSL-Compiler extrahiert die Parallelität in einem Hüllen-Shader und codiert sie in Bytecode, der die Hardware steuert.

-   Die Kontrollpunktphase wird einmal für jeden Kontrollpunkt ausgeführt, liest die Kontrollpunkte für einen Patch und generiert einen Ausgabekontrollpunkt (identifiziert durch eine ControlPointID).
-   Die Patchkonst constant-Phase wird einmal pro Patch betrieben, um Edge-Mosaikfaktoren und andere Pro-Patch-Konstanten zu generieren. Intern können viele Patchkonst constant-Phasen gleichzeitig ausgeführt werden. Die Patchkonst constant-Phase verfügt über schreibgeschützten Zugriff auf alle Eingabe- und Ausgabekontrollpunkte.

Hier ist ein Beispiel für einen Hüllen-Shader:


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



Ein Beispiel zum Erstellen eines Hüllen-Shaders finden Sie unter [How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md).

### <a name="tessellator-stage"></a>Mosaikphase

Der Mosaikator ist eine Phase mit fester Funktion, die durch Binden eines Hüllen-Shaders an die Pipeline initialisiert wird (siehe [How To: Initialize the Tessellator Stage](direct3d-11-advanced-stages-tessellator-initialize.md)). Der Zweck der Mosaikphase besteht im Unterstufen einer Domäne (quad, tri oder line) in viele kleinere Objekte (Dreiecke, Punkte oder Linien). Der Mosaikator kachelt eine kanonische Domäne in einem normalisierten Koordinatensystem (0:1). Beispielsweise wird eine Quad-Domäne in ein Einheitenquadreck geesselt.

Der Mosaikator arbeitet einmal pro Patch unter Verwendung der Mosaikfaktoren (die angeben, wie fein die Domäne mosaikiert wird) und dem Partitionierungstyp (der den Algorithmus angibt, der zum Aufteilen eines Patches verwendet wird), die aus der Hülle-Shader-Phase übergeben werden. Der Mosaikator gibt uv-Koordinaten (und optional w) und die Oberflächentopologie an die Domänen-Shader-Stufe aus.

Intern arbeitet der Mosaikator in zwei Phasen:

-   In der ersten Phase werden die Mosaikfaktoren verarbeitet, Rundungsprobleme behoben, sehr kleine Faktoren werden verarbeitet, Faktoren werden reduziert und kombiniert, und es wird eine 32-Bit-Gleitkommaarithmetik verwendet.
-   In der zweiten Phase werden Punkt- oder Topologielisten basierend auf dem ausgewählten Partitionierungstyp generiert. Dies ist die Kernaufgabe der Mosaikphase und verwendet 16-Bit-Brüche mit Festpunktarithmetik. Die arithmetische Festpunktarithmetik ermöglicht die Hardwarebeschleunigung bei gleichzeitiger Aufrechterhaltung akzeptabler Genauigkeit. Bei einem 64 Meter breiten Patch kann diese Genauigkeit beispielsweise Punkte mit einer Auflösung von 2 mm platzieren.



| Partitionierungstyp | Range                       |
|----------------------|-----------------------------|
| Bruchteil \_ ungerade      | \[1...63\]                  |
| fractional \_ even     | TessFactor-Bereich: \[ 2..64\] |
| integer              | TessFactor-Bereich: \[ 1..64\] |
| pow2                 | TessFactor-Bereich: \[ 1..64\] |



 

### <a name="domain-shader-stage"></a>Domain-Shader Stage

Ein Domänen-Shader berechnet die Scheitelpunktposition eines unterteilten Punkts im Ausgabepatch. Ein Domänen-Shader wird einmal pro Mosaikstufenausgabepunkt ausgeführt und hat schreibgeschützten Zugriff auf die UV-Koordinaten der Mosaikphase, den Hüllen-Shader-Ausgabepatch und die Patchkonstatoren für die Hüllen-Shaderausgabe, wie im folgenden Diagramm dargestellt.

![Diagramm der Domänen-Shader-Phase](images/d3d11-domain-shader.png)

Zu den Eigenschaften des Domänen-Shaders gehören:

-   Ein Domänen-Shader wird einmal pro Ausgabekoordinate aus der Mosaikphase aufgerufen.
-   Ein Domänen-Shader verwendet Ausgabekontrollpunkte aus der Hülle-Shader-Phase.
-   Ein Domänen-Shader gibt die Position eines Scheitelpunkts aus.
-   Eingaben sind die Ausgaben des Hüllen-Shaders, einschließlich Kontrollpunkten, Patchkonsttendaten und Mosaikfaktoren. Zu den Mosaikfaktoren können die werte gehören, die vom Festfunktions-Mosaik verwendet werden, sowie die Rohwerte (z. B. vor dem Runden nach ganzzahligem Mosaik), die z. B. Geomorphing ermöglichen.

Nach Abschluss des Domänen-Shaders ist das Mosaik abgeschlossen, und die Pipelinedaten werden mit der nächsten Pipelinephase (Geometrie-Shader, Pixel-Shader usw.) fortgesetzt. Ein Geometrie-Shader, der Primitive mit Adjakenz erwartet (z. B. 6 Scheitelpunkt pro Dreieck), ist ungültig, wenn das Mosaik aktiv ist (dies führt zu einem nicht definierten Verhalten, über das sich die Debugebene beschwert).

Hier ist ein Beispiel für einen Domänen-Shader:


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



## <a name="apis-for-initializing-tessellation-stages"></a>APIs zum Initialisieren von Mosaikstufen

Das Mosaik wird mit zwei neuen programmierbaren Shaderstufen implementiert: einem Hüllen-Shader und einem Domänen-Shader. Diese neuen Shaderstufen werden mit HLSL-Code programmiert, der in Shadermodell 5 definiert ist. Die neuen Shaderziele sind: hs \_ 5 \_ 0 und ds \_ 5 \_ 0. Wie alle programmierbaren Shaderstufen wird Code für die Hardware aus kompilierten Shadern extrahiert, die an die Runtime übergeben werden, wenn Shader mithilfe von APIs wie [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) und [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)an die Pipeline gebunden werden. Zunächst muss der Shader jedoch mitHILFE von APIs wie [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) und [**CreateDomainShader erstellt werden.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)

Aktivieren Sie das Mosaik, indem Sie einen Hüllen-Shader erstellen und an die Hüllen-Shader-Stufe binden (dadurch wird automatisch die Mosaikstufe eingerichtet). Um die endgültigen Scheitelpunktpositionen aus den mosaikierten Patches zu generieren, müssen Sie auch einen Domänen-Shader erstellen und an die Domänen-Shader-Stufe binden. Sobald das Mosaik aktiviert ist, muss die Dateneingabe in die Eingabe-Assembler-Phase Patchdaten sein. Das heißt, die Eingabe-Assemblertopologie muss eine patchkonstierte Topologie von [**D3D11 \_ PRIMITIVE \_ TOPOLOGY**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) sein, die mit [**IASetPrimitiveTopology festgelegt wurde.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

Legen Sie zum Deaktivieren des Mosaiks den Hüllen-Shader und den Domänen-Shader auf **NULL fest.** Weder die Geometry-Shader-Stufe noch die Streamausgabephase können ausgabekontrollpunkte oder Patchdaten des Hülle-Shaders lesen.

-   Neue Topologien für die Eingabe-Assembler-Phase, die Erweiterungen dieser Enumeration sind.

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    Die Topologie wird mithilfe von [ **IASetPrimitiveTopology auf die Eingabe-Assembler-Phase festgelegt.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   Für die neuen programmierbaren Shaderstufen muss natürlich ein anderer Zustand festgelegt werden, um konstante Puffer, Beispiele und Shaderressourcen an die entsprechenden Pipelinestufen zu binden. Diese neuen ID3D11Device-Methoden werden zum Festlegen dieses Zustands implementiert.
    -   [**DSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers)
    -   [**DSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetsamplers)
    -   [**DSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshader)
    -   [**DSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshaderresources)
    -   [**DSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers)
    -   [**DSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetsamplers)
    -   [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)
    -   [**DSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshaderresources)
    -   [**HSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers)
    -   [**HSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshaderresources)
    -   [**HSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetsamplers)
    -   [**HSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshader)
    -   [**HSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers)
    -   [**HSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetsamplers)
    -   [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)
    -   [**HSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshaderresources)

## <a name="how-tos"></a>So geht's:

Die Dokumentation enthält auch Beispiele für die Initialisierung der Mosaikstufen.



| Element                                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[How To: Erstellen eines Hüllen-Shaders](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | Erstellen Sie einen Hüllen-Shader.<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[How To: Entwerfen eines Hüllen-Shaders](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | Entwerfen Sie einen Hüllen-Shader.<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[How To: Initialize the Tessellator Stage](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | Initialisieren Sie die Mosaikphase.<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[How To: Erstellen eines Domänen-Shaders](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | Erstellen Sie einen Domänen-Shader.<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[How To: Entwerfen eines Domänen-Shaders](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | Erstellen Sie einen Domänen-Shader.<br/>            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 


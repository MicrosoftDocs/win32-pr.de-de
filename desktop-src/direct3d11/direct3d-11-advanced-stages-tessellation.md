---
title: Mosaikstufen
description: Die Direct3D 11-Runtime unterstützt drei neue Phasen, die Mosaik implementieren, wodurch Unterteilungsoberflächen mit geringen Details in Primitive mit höheren Details auf der GPU konvertiert werden.
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

Die Direct3D 11-Runtime unterstützt drei neue Phasen, die Mosaik implementieren, wodurch Unterteilungsoberflächen mit geringen Details in Primitive mit höheren Details auf der GPU konvertiert werden. Mosaikkacheln (oder unterteilt) oberflächen hoher Ordnung in geeignete Strukturen für das Rendering.

Durch die Implementierung des Mosaiks in der Hardware kann eine Grafikpipeline Modelle mit niedrigeren Details (niedrigere Polygonanzahl) auswerten und ausführlicher rendern. Das Software-Mosaik kann zwar durchgeführt werden, aber das von der Hardware implementierte Mosaik kann eine enorme Menge visueller Details generieren (einschließlich Unterstützung für die Verschiebungszuordnung), ohne die visuellen Details den Modellgrößen hinzuzufügen und Aktualisierungsraten zu paralysieren.

-   [Mosaikvorteile](#tessellation-benefits)
-   [Neue Pipelinestufen](#new-pipeline-stages)
    -   [Hüllen-Shader-Stufe](#hull-shader-stage)
    -   [Tessellator-Phase](#tessellator-stage)
    -   [Domänen-Shader-Phase](#domain-shader-stage)
-   [APIs zum Initialisieren von Mosaikstufen](#apis-for-initializing-tessellation-stages)
-   [Vorgehensweise:](#how-tos)
-   [Zugehörige Themen](#related-topics)

## <a name="tessellation-benefits"></a>Mosaikvorteile

Tessellation:

-   Spart viel Arbeitsspeicher und Bandbreite, wodurch eine Anwendung detailliertere Oberflächen aus Modellen mit niedriger Auflösung rendern kann. Die in der Direct3D 11-Pipeline implementierte Mosaiktechnik unterstützt auch die Verschiebungszuordnung, die zu beeindruckenden Mengen von Oberflächendetails führen kann.
-   Unterstützt skalierbare Renderingtechniken, z. B. fortlaufende oder abhängige Detailebenen anzeigen, die im laufenden Betrieb berechnet werden können.
-   Verbessert die Leistung, indem teure Berechnungen mit geringerer Frequenz ausgeführt werden (Berechnungen für ein Modell mit niedrigeren Details). Dies kann das Kombinieren von Berechnungen mithilfe von Mischungsformen oder Morphzielen für realistische Animationen oder physikalische Berechnungen für die Kollisionserkennung oder die Softtext-Dynamics umfassen.

Die Direct3D 11-Pipeline implementiert das Mosaik in hardware, wodurch die Arbeit von der CPU auf die GPU ausgelastet wird. Dies kann zu sehr großen Leistungsverbesserungen führen, wenn eine Anwendung eine große Anzahl von Morphzielen und/oder komplexere Skinning-/Bereinigungsmodelle implementiert. Um auf die neuen Mosaikfeatures zugreifen zu können, müssen Sie sich über einige neue Pipelinephasen informieren.

## <a name="new-pipeline-stages"></a>Neue Pipelinestufen

Mosaik verwendet die GPU, um eine ausführlichere Oberfläche aus einer Oberfläche zu berechnen, die aus Quad-Patches, Dreieckspatches oder Isolinien erstellt wurde. Um die obere Oberfläche anzunähern, wird jeder Patch unter Verwendung von Mosaikfaktoren in Dreiecke, Punkte oder Linien unterteilt. Die Direct3D 11-Pipeline implementiert das Mosaik mithilfe von drei neuen Pipelinestufen:

-   [Hüllen-Shader-Stufe:](#hull-shader-stage) Eine programmierbare Shaderstufe, die einen Geometriepatch (und Patchkonstanten) erzeugt, die den einzelnen Eingabepatches (Quad, Dreieck oder Linie) entsprechen.
-   [Tessellator Stage](#tessellator-stage) : Eine Pipelinephase mit fester Funktion, die ein Samplingmuster der Domäne erstellt, das den Geometriepatch darstellt und eine Reihe kleinerer Objekte (Dreiecke, Punkte oder Linien) generiert, die diese Beispiele verbinden.
-   [Domänen-Shader-Stufe:](#domain-shader-stage) Eine programmierbare Shaderphase, die die Scheitelpunktposition berechnet, die den einzelnen Domänenstichproben entspricht.

Im folgenden Diagramm werden die neuen Phasen der Direct3D 11-Pipeline hervorgehoben.

![Diagramm der Direct3d 11-Pipeline, die die Phasen "hull-shader", "tessellator" und "domain-shader" hervorhebt](images/d3d11-pipeline-stages-tessellation.png)

Das folgende Diagramm zeigt den Fortschritt durch die Mosaikstufen. Der Fortschritt beginnt mit der Unterteilungsoberfläche mit geringen Details. Im nächsten Schritt wird der Eingabepatch mit den entsprechenden Geometriepatches, Domänenbeispielen und Dreiecken hervorgehoben, die diese Beispiele verbinden. Der Fortschritt hebt schließlich die Scheitelpunkte hervor, die diesen Beispielen entsprechen.

![Diagramm des Mosaikverlaufs](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Hull-Shader Phase

Ein Hüllen-Shader , der einmal pro Patch aufgerufen wird, transformiert Eingabekontrollpunkte, die eine Oberfläche mit niedriger Ordnung definieren, in Kontrollpunkte, aus denen ein Patch besteht. Außerdem werden einige Berechnungen pro Patch durchgeführt, um Daten für die Mosaikphase und die Domänenphase bereitzustellen. Auf der einfachsten Blackboxebene würde die Hüllen-Shader-Stufe in etwa wie im folgenden Diagramm aussehen.

![Diagramm der Hüllen-Shader-Stufe](images/d3d11-hull-shader.png)

Ein Hüllen-Shader wird mit einer HLSL-Funktion implementiert und verfügt über die folgenden Eigenschaften:

-   Die Shadereingabe liegt zwischen 1 und 32 Kontrollpunkten.
-   Die Shaderausgabe liegt unabhängig von der Anzahl der Mosaikfaktoren zwischen 1 und 32 Kontrollpunkten. Die Ausgabe der Kontrollpunkte eines Hüllen-Shaders kann von der Domänen-Shader-Stufe genutzt werden. Patchkonstante Daten können von einem Domänen-Shader genutzt werden. Mosaikfaktoren können vom Domänen-Shader und der Mosaikstufe genutzt werden.
-   Mosaikfaktoren bestimmen, wie viel die einzelnen Patches unterteilt werden sollen.
-   Der Shader deklariert den Zustand, der für die Mosaikphase erforderlich ist. Dies schließt Informationen wie die Anzahl der Kontrollpunkte, den Typ der Patchfläche und die Art der Partitionierung ein, die beim Mosaik verwendet werden soll. Diese Informationen werden in der Regel als Deklarationen am Anfang des Shadercodes angezeigt.
-   Wenn die Hüllen-Shader-Stufe einen Edge-Mosaikfaktor auf = 0 oder NaN festlegt, wird der Patch gelöscht. Daher kann die Mosaikphase ausgeführt werden, der Domänen-Shader wird nicht ausgeführt, und für diesen Patch wird keine sichtbare Ausgabe erzeugt.

Auf einer tieferen Ebene arbeitet ein Hüllen-Shader tatsächlich in zwei Phasen: einer Steuerungspunktphase und einer Patchkonstantenphase, die parallel von der Hardware ausgeführt werden. Der HLSL-Compiler extrahiert die Parallelität in einem Hüllen-Shader und codiert sie in Bytecode, der die Hardware steuert.

-   Die Steuerungspunktphase wird einmal für jeden Kontrollpunkt betrieben, liest die Kontrollpunkte für einen Patch und generiert einen Ausgabekontrollpunkt (identifiziert durch eine ControlPointID).
-   Die Patchkonstantenphase wird einmal pro Patch betrieben, um Edge-Mosaikfaktoren und andere Konstanten pro Patch zu generieren. Intern können viele patchkonstante Phasen gleichzeitig ausgeführt werden. Die Patchkonstantenphase hat schreibgeschützten Zugriff auf alle Eingabe- und Ausgabesteuerungspunkte.

Hier sehen Sie ein Beispiel für einen Hüllen-Shader:


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



Ein Beispiel zum Erstellen eines Hüllen-Shaders finden Sie unter [Vorgehensweise: Erstellen eines Hüllen-Shaders.](direct3d-11-advanced-stages-hull-shader-create.md)

### <a name="tessellator-stage"></a>Tessellator-Phase

Der Mosaikator ist eine Stufe mit fester Funktion, die initialisiert wird, indem ein Hüllen-Shader an die Pipeline gebunden wird (siehe [Vorgehensweise: Initialisieren der Tessellatorphase](direct3d-11-advanced-stages-tessellator-initialize.md)). Der Zweck der Mosaikphase besteht darin, eine Domäne (Quad, Tri oder Linie) in viele kleinere Objekte (Dreiecke, Punkte oder Linien) zu unterteilen. Der Mosaikator kachelt eine kanonische Domäne in einem normalisierten Koordinatensystem (0:1). Beispielsweise wird eine Quad-Domäne mit einem Einheitenquadrat verkettet.

Der Mosaikator arbeitet einmal pro Patch mithilfe der Mosaikfaktoren (die angeben, wie fein die Domäne mosaikiert wird) und des Partitionierungstyps (der den Algorithmus angibt, der zum Aufteilen eines Patches verwendet wird), die von der Hüllen-Shader-Stufe übergeben werden. Der Mosaikator gibt UV-Koordinaten (und optional w) und die Oberflächentopologie an die Domänen-Shader-Stufe aus.

Intern arbeitet der Mosaikator in zwei Phasen:

-   In der ersten Phase werden die Mosaikfaktoren verarbeitet, Rundungsprobleme behoben, sehr kleine Faktoren behandelt, Faktoren mit 32-Bit-Gleitkommaarithmetik reduziert und kombiniert.
-   In der zweiten Phase werden Punkt- oder Topologielisten basierend auf dem ausgewählten Partitionierungstyp generiert. Dies ist die Kernaufgabe der Mosaikstufe und verwendet 16-Bit-Bruchzahlen mit Arithmetik mit festem Punkt. Die Arithmetik mit festem Punkt ermöglicht die Hardwarebeschleunigung bei akzeptabler Genauigkeit. Bei einem Breitenpatch von 64 Metern kann diese Genauigkeit z. B. Punkte mit einer Auflösung von 2 mm platzieren.



| Partitionierungstyp | Range                       |
|----------------------|-----------------------------|
| fractional \_ odd      | \[1...63\]                  |
| fractional \_ even     | TessFactor-Bereich: \[ 2..64\] |
| integer              | TessFactor-Bereich: \[ 1..64\] |
| pow2                 | TessFactor-Bereich: \[ 1..64\] |



 

### <a name="domain-shader-stage"></a>Domain-Shader Phase

Ein Domänen-Shader berechnet die Scheitelpunktposition eines unterteilten Punkts im Ausgabepatch. Ein Domänen-Shader wird einmal pro Tessellator-Stage-Ausgabepunkt ausgeführt und hat schreibgeschützten Zugriff auf die UV-Koordinaten der Tessellator-Stufenausgabe, den Ausgabepatch des Hüllen-Shaders und die Ausgabepatchkonstanten des Hüllen-Shaders, wie im folgenden Diagramm dargestellt.

![Diagramm der Domänen-Shader-Phase](images/d3d11-domain-shader.png)

Zu den Eigenschaften des Domänen-Shaders gehören:

-   Ein Domänen-Shader wird einmal pro Ausgabekoordinate aus der Mosaikstufe aufgerufen.
-   Ein Domänen-Shader nutzt Ausgabekontrollpunkte aus der Hüllen-Shader-Phase.
-   Ein Domänen-Shader gibt die Position eines Scheitelpunkts aus.
-   Eingaben sind die Ausgaben des Hüllen-Shaders, einschließlich Steuerungspunkten, Patchkonstantendaten und Mosaikfaktoren. Die Mosaikfaktoren können die Vom festen Funktionstessellator verwendeten Werte sowie die rohen Werte (z. B. vor dem Runden durch ganzzahlige Mosaike) umfassen, was z. B. die Geomorphation ermöglicht.

Nach Abschluss des Domänen-Shaders ist das Mosaik abgeschlossen, und die Pipelinedaten werden mit der nächsten Pipelinephase (Geometrie-Shader, Pixel-Shader usw.) fortgesetzt. Ein Geometrie-Shader, der Primitive mit Adjazenz erwartet (z. B. 6 Scheitelpunkte pro Dreieck), ist ungültig, wenn die Mosaikierung aktiv ist (dies führt zu einem nicht definierten Verhalten, über das sich die Debugebene beschwert).

Hier sehen Sie ein Beispiel für einen Domänen-Shader:


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

Mosaik wird mit zwei neuen programmierbaren Shaderstufen implementiert: einem Hüllen-Shader und einem Domänen-Shader. Diese neuen Shaderstufen werden mit HLSL-Code programmiert, der im Shadermodell 5 definiert ist. Die neuen Shaderziele sind: hs \_ 5 \_ 0 und ds \_ 5 \_ 0. Wie alle programmierbaren Shaderstufen wird Code für die Hardware aus kompilierten Shadern extrahiert, die an die Laufzeit übergeben werden, wenn Shader mithilfe von APIs wie [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) und [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)an die Pipeline gebunden werden. Zunächst muss der Shader jedoch mithilfe von APIs wie [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) und [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)erstellt werden.

Aktivieren Sie das Mosaik, indem Sie einen Hüllen-Shader erstellen und an die Hüllen-Shader-Stufe binden (dadurch wird automatisch die Mosaikstufe eingerichtet). Um die endgültigen Scheitelpunktpositionen aus den Mosaikpatches zu generieren, müssen Sie auch einen Domänen-Shader erstellen und an die Domänen-Shader-Stufe binden. Sobald das Mosaik aktiviert ist, muss es sich bei der Dateneingabe in die Eingabeassemblierungsphase um Patchdaten handelt. Das heißt, die Eingabeassemblierungstopologie muss eine Patchkonstantentopologie aus [**D3D11 \_ PRIMITIVE \_ TOPOLOGY**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) sein, die mit [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)festgelegt ist.

Legen Sie zum Deaktivieren des Mosaiks den Hüllen-Shader und den Domänen-Shader auf **NULL** fest. Weder die geometry-shader-Stufe noch die Stream-Output-Stufe können Ausgabekontrollpunkte des Hüllen-Shaders lesen oder Daten patchen.

-   Neue Topologien für die Eingabeassembliererphase, die Erweiterungen dieser Enumeration sind.

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    Die Topologie wird mithilfe von [ **IASetPrimitiveTopology** auf die Eingabeassemblierungsphase festgelegt.](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   Natürlich müssen für die neuen programmierbaren Shaderstufen andere Zustände festgelegt werden, um konstante Puffer, Stichproben und Shaderressourcen an die entsprechenden Pipelinestufen zu binden. Diese neuen ID3D11Device-Methoden werden zum Festlegen dieses Zustands implementiert.
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

## <a name="how-tos"></a>Vorgehensweise:

Die Dokumentation enthält auch Beispiele für die Initialisierung der Mosaikstufen.



| Element                                                                                                                                                                                                                                                                                           | Beschreibung                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[Vorgehensweise: Erstellen eines Hüllen-Shaders](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | Erstellen Sie einen Hüllen-Shader.<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[Vorgehensweise: Entwerfen eines Hüllen-Shaders](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | Entwerfen sie einen Hüllen-Shader.<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[Vorgehensweise: Initialisieren der Tessellator-Stufe](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | Initialisieren Sie die Mosaikphase.<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[Vorgehensweise: Erstellen eines Domänen-Shaders](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | Erstellen Sie einen Domänen-Shader.<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[Vorgehensweise: Entwerfen eines Domänen-Shaders](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | Erstellen Sie einen Domänen-Shader.<br/>            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 


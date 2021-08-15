---
description: Vorausberechnungsübertragung der Radiance (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Vorausberechnungsübertragung der Radiance (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc18eff66dab9a696a3e441d894a327890c53888da008d72a5f143ca0d345a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798732"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a>Vorausberechnungsübertragung der Radiance (Direct3D 9)

## <a name="using-precomputed-radiance-transfer"></a>Verwenden der vorausbesetzten Radianceübertragung

Es gibt verschiedene Formen der Komplexität in interessanten Szenen, z. B. wie die Beleuchtungsumgebung modelliert wird (d. h. Bereichsbeleuchtungsmodelle im Vergleich zu punkt-/richtungsalen Modellen) und welche Art von globalen Effekten modelliert werden (z. B. Schatten, Interreflectionen, Unteroberflächen-Punktion). Herkömmliche interaktive Renderingtechniken modellieren einen begrenzten Teil dieser Komplexität. PRT ermöglicht diese Auswirkungen mit einigen erheblichen Einschränkungen:

-   Es wird davon ausgegangen, dass Objekte fest (d. h. keine Ns) sind.
-   Es handelt sich um einen objektzentrierten Ansatz (sofern Objekte nicht zusammen verschoben werden, werden diese globalen Effekte nicht zwischen ihnen beibehalten).
-   Es wird nur eine Beleuchtung mit niedriger Frequenz modelliert (was zu weichen Schatten führt). Für Hochfrequenzlichter (starke Schatten) müssten herkömmliche Techniken eingesetzt werden.

PRT erfordert eine der folgenden, aber nicht beide:

-   stark mosaikierte Modelle und im Vergleich \_ zu 1 \_ 1
-   ps \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>Diffuse Standard-Beleuchtung im Vergleich zu PRT

Die folgende Abbildung wird mit dem herkömmlichen Beleuchtungsmodell (n · l) gerendert. Sharp shadows could be enabled using another pass and some form of shadowing technique (shadow depth maps or shadow volumes) (Sharp shadows could be enabled using another pass and some form of shadowing technique (Schattentiefekarten oder Schattenvolumen)). Das Hinzufügen mehrerer Beleuchtungen erfordert entweder mehrere Durchläufe (wenn Schatten verwendet werden sollen) oder komplexere Shader mit herkömmlichen Techniken.

![Screenshot einer Mithilfe des herkömmlichen Beleuchtungsmodells gerenderten Abbildung](images/prt-diffuse-cropped.png)

Die nächste Abbildung wird mit PRT mit der besten Näherung eines einzelnen direktionalen Lichts gerendert, das es auflösen kann. Dies führt zu weichen Schatten, die mit herkömmlichen Techniken schwer zu erzeugen sind. Da DAS PRT immer beleuchtungsumgebungen vollständig modelliert, die mehrere Beleuchtungslichter hinzufügen oder eine Umgebungszuordnung verwenden, würden Sie nur die Werte (aber nicht die Anzahl) von Konstanten ändern, die vom Shader verwendet werden.

![Screenshot einer Mithilfe von PRT gerenderten Abbildung](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>PRT mit Interreflections

Die direkte Beleuchtung erreicht die Oberfläche direkt vom Licht. Interreflectionen erreichen die Oberfläche, nachdem sie einige Male von einer anderen Oberfläche abgeknüpft wurden. PRT kann dieses Verhalten modellieren, ohne die Leistung zur Laufzeit zu ändern, indem der Simulator einfach mit unterschiedlichen Parametern ausgeführt wird.

Die folgende Abbildung wird nur mit dem direkten PRT erstellt (0 Bounces ohne Interreflectionen).

![Screenshot einer Abbildung, die nur mithilfe des direkten PRT gerendert wird](images/prt-nointerreflections.png)

Die folgende Abbildung wird mithilfe von PRT mit Interreflectionen (2 Bounces mit Interreflectionen) erstellt.

![Screenshot einer Abbildung, die mithilfe von PRT mit Interreflectionen gerendert wurde](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>PRT mit Subsurface Scattering

Das Streuen von Unteroberflächen ist eine Technik, die modelliert, wie Licht bestimmte Materialien durchläuft. Drücken Sie z. B. eine leuchtende Taschenlampe gegen die Handfläche. Das Licht der Taschenlampe durchläuft Ihre Hand, springt umher (ändert die Farbe im Prozess) und verlässt die andere Seite Ihrer Hand. Dies kann auch mit einfachen Änderungen am Simulator und ohne Änderungen an der Laufzeit modelliert werden.

Die folgende Abbildung veranschaulicht PRT mit Unteroberflächen-Punktung.

![Screenshot einer Abbildung, die mithilfe von prt mit Unteroberflächen-Punktung gerendert wurde](images/prt-subsurface.png)

## <a name="how-prt-works"></a>Funktionsweise von PRT

Die folgenden Begriffe sind nützlich, um zu verstehen, wie PRT funktioniert, wie im folgenden Diagramm dargestellt.

Quellradanz: Die Quellenresonanz stellt die gesamte Beleuchtungsumgebung dar. In PRT wird eine beliebige Umgebung mithilfe der pherischen Tropenbasis als ungefähre Umgebung bezeichnet. Es wird davon ausgegangen, dass diese Beleuchtung relativ zum Objekt entfernt ist (die gleiche Annahme wie bei Umgebungszuordnungen).

Exit Radiance :Exit radiance (Exit-Radiance) ist das Licht, das von einem Punkt auf der Oberfläche aus einer beliebigen möglichen Quelle (reflektierte Bogenstärke, Streuung des Unteroberflächen, Lichtabbild) verlässt.

Übertragungsvektoren: Übertragungsvektoren ordnen quellauslösend dem Ausgangsbild zu und werden offline mithilfe einer komplexen Lichttransportsimulation vorausberechnunget.

![Diagramm zur Funktionsweise von prt](images/prt-lightingpicture.png)

PRT bestimmt den Renderingprozess in zwei Phasen, wie im folgenden Diagramm dargestellt:

1.  Eine teure Lichttransportsimulation berechnet Übertragungskoeffizienten, die zur Laufzeit verwendet werden können.
2.  Eine relativ einfache Laufzeitphase wird zuerst der Beleuchtungsumgebung mithilfe der pherischen Glühbirne angewend, dann werden diese Beleuchtungskoeffizienten und die vorausbesetzten Übertragungskoeffizienten (aus Phase 1) mit einem einfachen Shader verwendet, was zu Einer-Beendigungs-Lichtauslösung (dem Licht, das das Objekt verlässt) führt.

![Diagramm des PRT-Datenflusses](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>Verwenden der PRT-API

1.  Berechnen Sie die Übertragungsvektoren mit einer der Compute-... -Methoden von [**ID3DXPRTEngine**](id3dxprtengine.md).

    Der direkte Umgang mit diesen Übertragungsvektoren erfordert eine erhebliche Menge an Arbeitsspeicher und Shaderberechnung. Durch die Komprimierung wird die Erforderliche Menge an Arbeitsspeicher und Shaderberechnung erheblich reduziert.

    Die endgültigen Beleuchtungswerte werden in einem Vertex-Shader berechnet, der die folgende komprimierte Renderinggleichung implementiert.

    ![Gleichung des PRT-Renderings](images/prt-shaderequation.png)

    Hierbei gilt:

    

    | Parameter      | BESCHREIBUNG                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | Rp             | Ein einzelner Kanal mit Beendigungsausdance bei Scheitelpunkt p und wird an jedem Scheitelpunkt im Gitternetz ausgewertet.                     |
    | Mk             | Der Mittelwert für Cluster k. Dies ist ein Order 2-Vektor von Koeffizienten.                                               |
    | k              | Die Cluster-ID für Scheitelpunkt p.                                                                                    |
    | L<sup>'</sup>  | Die Näherung der Quellquelle in die SH-Basisfunktionen. Dies ist ein Order 2-Vektor von Koeffizienten. |
    | j              | Eine ganze Zahl, die die Anzahl der PCA-Vektoren summiert.                                                            |
    | w<sub>pj</sub> | Die jth PCA-Gewichtung für Punkt p. Dies ist ein einzelner Koeffizient.                                                   |
    | B<sub>kj</sub> | Der jth PCA-Basisvektor für Cluster k. Dies ist ein Order 2-Vektor von Koeffizienten.                               |

    

     

    Extrahieren... -Methoden von [**ID3DXPRTCompBuffer ermöglichen**](id3dxprtcompbuffer.md) den Zugriff auf komprimierte Daten aus der Simulation.

2.  Berechnen Sie die Quellleistung.

    Es gibt mehrere Hilfsfunktionen in der API, um eine Vielzahl gängiger Beleuchtungsszenarien zu verarbeiten.

    

    | Funktion                                                         | Zweck                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | Entspricht einem konventionellen direktionalen Licht.                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | Ungefähre lokale pherische Lichtquellen. (Beachten Sie, dass PRT nur mit Entfernungslichtumgebungen funktioniert.) |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | Entspricht einer entfernten Bereichslichtquelle. Ein Beispiel wäre die Sote (sehr kleiner Kegelwinkel).              |
    | [**D3DXSHEvalHemisphereLight**](d3dxshevalhemispherelight.md)   | Wertet ein Licht aus, bei dem es sich um eine lineare Interpolation zwischen zwei Farben handelt (eine auf jedem Pol einer Kugel).         |

    

     

3.  Berechnen Sie die Beendigungsausdance.

    Gleichung 1 muss jetzt an jedem Punkt mit einem Scheitelpunkt oder einem Pixel-Shader ausgewertet werden. Bevor der Shader ausgewertet werden kann, müssen Konstanten vorausbewertet und in die Konstantentabelle geladen werden (weitere Informationen finden Sie im [PRT-Demobeispiel).](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) Der Shader selbst ist eine einfache Implementierung dieser Gleichung.

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a>Literatur

Weitere Informationen zu PRT und pherischen Trophäen finden Sie in den folgenden Arbeiten:


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Weiterführende Themen](advanced-topics.md)
</dt> <dt>

[PRT-Gleichungen (Direct3D 9)](prt-equations.md)
</dt> <dt>

[Darstellen von PRT mit Texturen (Direct3D 9)](representing-prt-with-textures.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTEngine**](id3dxprtengine.md)
</dt> <dt>

[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)
</dt> <dt>

[Vorausberechnungsfunktionen für die Übertragung von Radiance](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




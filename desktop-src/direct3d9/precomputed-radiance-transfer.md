---
description: Voraus berechnete Strahlungs Übertragung (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Voraus berechnete Strahlungs Übertragung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569040"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a>Voraus berechnete Strahlungs Übertragung (Direct3D 9)

## <a name="using-precomputed-radiance-transfer"></a>Verwenden der Voraus berechneten Strahlungs Übertragung

Es gibt verschiedene Formen der Komplexität in interessanten Szenen, einschließlich der Modellierung der Beleuchtungs Umgebung (d. h. Flächen Beleuchtungs Modelle im Vergleich zu Punkt-/direktionalen) und der Art von globalen Effekten, die modelliert werden (z. b. Schatten, interreflektionen, unter Oberflächen Streuung). Herkömmliche interaktive Renderingverfahren modellieren einen begrenzten Anteil dieser Komplexität. PRT aktiviert diese Effekte mit einigen erheblichen Einschränkungen:

-   Es wird davon ausgegangen, dass Objekte starr sind (d. h. keine Deformationen).
-   Dabei handelt es sich um einen Objekt zentrierten Ansatz (es sei denn, Objekte werden gemeinsam verschoben, diese globalen Effekte werden nicht zwischen ihnen beibehalten).
-   Nur die Beleuchtung mit niedriger Frequenz wird modelliert (was zu weichen Schatten führt). Bei Hochfrequenz Lichtern (scharfe Schatten) müssten herkömmliche Techniken eingesetzt werden.

PRT erfordert eine der folgenden beiden Optionen:

-   hochgradig Mosaik Modelle und vs \_ 1 \_ 1
-   PS \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>Standard mäßige diffuse Beleuchtung im Vergleich zu PRT

Die folgende Abbildung wird mithilfe des herkömmlichen (n) Beleuchtungs Modells gerendert. Scharfe Schatten können mit einem anderen Durchlauf und einer Form der Shadowing-Technik (Schatten Tiefe Karten oder schattenvolumes) aktiviert werden. Das Hinzufügen mehrerer Lichter erfordert entweder mehrere Durchgänge (wenn Schatten verwendet werden sollen) oder komplexere Shader mit herkömmlichen Techniken.

![Screenshot einer Abbildung, die mithilfe des herkömmlichen Beleuchtungs Modells gerendert wird](images/prt-diffuse-cropped.png)

Die nächste Abbildung wird mit PRT mit der besten Näherung eines einzelnen direktionalen Lichts gerendert, das Sie auflösen kann. Dies führt dazu, dass weiche Schatten nicht mit herkömmlichen Techniken erzeugt werden. Da PRT immer alle Beleuchtungs Umgebungen mit mehreren Lichtern oder einer Umgebungs Zuordnung modelliert, würden Sie nur die Werte (aber nicht die Anzahl) der Konstanten ändern, die vom Shader verwendet werden.

![Screenshot einer mit PRT gerenderten Abbildung](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>PRT mit interreflektionen

Die direkte Beleuchtung erreicht die Oberfläche direkt vom Licht. Interreflektionen sind Lichtreich und erreichen die Oberfläche, nachdem eine andere Oberfläche so oft wie oft ausgeschaltet wurde. PRT kann dieses Verhalten modellieren, ohne die Leistung zur Laufzeit zu ändern, indem der Simulator einfach mit anderen Parametern ausgeführt wird.

Die folgende Abbildung wird nur mithilfe von Direct PRT erstellt (0 springt ohne interreflektionen).

![Screenshot einer Abbildung, die nur mit Direct PRT gerendert wird](images/prt-nointerreflections.png)

Die folgende Abbildung wird mithilfe von PRT mit interreflektionen erstellt (2 springt with interreflektionen).

![Screenshot einer Abbildung, die mithilfe von PRT mit interreflektionen gerendert wird](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>PRT with subsurface Scattering

Unter Surface im ist ein Verfahren, das die Art und Weise anzeigt, wie das Licht durch bestimmte Materialien verläuft. Drücken Sie als Beispiel eine Beleuchtung mit beleuchteter Taschenlampe. Das Licht aus der Taschenlampe durchläuft Ihre Hand, springt um (Ändern der Farbe im Prozess) und beendet von der anderen Seite. Dies kann auch mit einfachen Änderungen am Simulator und ohne Änderungen an der Laufzeit modelliert werden.

In der folgenden Abbildung wird PRT mit unter Oberflächen Streuung veranschaulicht.

![Screenshot einer Abbildung, die durch die Verwendung von PRT mit der unter Oberflächen Streuung gerendert wird](images/prt-subsurface.png)

## <a name="how-prt-works"></a>Funktionsweise von PRT

Die folgenden Begriffe sind hilfreich, um zu verstehen, wie PRT funktioniert, wie in der folgenden Abbildung dargestellt.

Quell Ausstrahlung: die Quell Ausstrahlung stellt die Beleuchtungs Umgebung als Ganzes dar. In PRT wird eine beliebige Umgebung mithilfe der kugelförmigen harmonischen Basis angezeigt. diese Beleuchtung wird vorausgesetzt, dass Sie relativ zum-Objekt ist (dieselbe Annahme wird in Umgebungs Zuordnungen vorgenommen).

Exit-Ausdruck: die Ausgangs-Glanz ist das Licht, das von einem Punkt auf der Oberfläche von einer beliebigen möglichen Quelle verlässt (reflektierte Strahlen, unter Oberflächen-Scattering, Ausgabe).

Übertragungs Vektoren: Übertragungs Vektoren ordnen Quell Strahlen in eine Ausgangs-und vorab berechnete Verwendung einer komplexen Light-Transport-Simulation.

![Diagramm zur Funktionsweise von PRT](images/prt-lightingpicture.png)

PRT Faktoren den Renderingprozess in zwei Phasen, wie im folgenden Diagramm dargestellt:

1.  Eine teure Light-Transport-Simulation führt eine Vorberechnung der Übertragungskoeffizienten aus, die zur Laufzeit verwendet werden können.
2.  In einer relativ einfachen Lauf Zeit Phase wird zunächst die Beleuchtungs Umgebung unter Verwendung der kugelförmigen harmonischen Basis und dann diese Beleuchtungs Koeffizienten und die Voraus berechneten Übertragungskoeffizienten (aus Phase 1) mit einem einfachen Shader verwendet, was zu einem exitglanz führt (das Licht, das das Objekt verlässt).

![Diagramm des PRT-Datenflusses](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>Verwenden der PRT-API

1.  Berechnen Sie die Übertragungs Vektoren mit einem der COMPUTE-... Methoden von [**ID3DXPRTEngine**](id3dxprtengine.md).

    Der direkte Umgang mit diesen Übertragungs Vektoren erfordert eine beträchtliche Menge an Arbeitsspeicher-und shaderberechnung. Durch die Komprimierung wird der erforderliche Arbeitsspeicher und die Shader-Berechnung erheblich reduziert.

    Die abschließenden Beleuchtungs Werte werden in einem Vertex-Shader berechnet, der die folgende komprimierte renderinggleichung implementiert.

    ![Gleichung des PRT-Rendering](images/prt-shaderequation.png)

    Hierbei gilt:

    

    | Parameter      | BESCHREIBUNG                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | Neutraler             | Ein einzelner Kanal mit exitstrahlung bei Scheitelpunkt p und wird bei jedem Scheitelpunkt im Mesh ausgewertet.                     |
    | Gegründete             | Der Mittelwert für Cluster k. Dies ist ein "Order ²"-Vektor von Koeffizienten.                                               |
    | k              | Die Cluster-ID für Vertex p.                                                                                    |
    | L<sup>'</sup>  | Die Näherung der Quell Ausstrahlung in die sh-Basisfunktionen. Dies ist ein "Order ²"-Vektor von Koeffizienten. |
    | j              | Eine ganze Zahl, die die Anzahl der PCA-Vektoren summiert.                                                            |
    | w-<sub>PJ</sub> | Die Jth-PCA-Gewichtung für Punkt p. Dies ist ein einzelner Koeffizient.                                                   |
    | B-<sub>kJ</sub> | Der Jth PCA-Basis Vektor für Cluster k. Dies ist ein "Order ²"-Vektor von Koeffizienten.                               |

    

     

    Der Extraktions-... [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Methoden ermöglichen den Zugriff auf komprimierte Daten aus der Simulation.

2.  Berechnen der Quell Ausstrahlung.

    Es gibt mehrere Hilfsfunktionen in der API, die eine Vielzahl von gängigen Beleuchtungs Szenarios verarbeiten können.

    

    | Funktion                                                         | Zweck                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | Gleicht ein herkömmliches Direktionales Licht.                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | Entspricht lokalen kugelförmigen Lichtquellen. (Beachten Sie, dass PRT nur bei Entfernungs Beleuchtungs Umgebungen funktioniert.) |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | Gleicht eine entfernte Bereichs-Lichtquelle. Ein Beispiel wäre die Sun (sehr kleiner Kegelwinkel).              |
    | [**D3DXSHEvalHemisphereLight**](d3dxshevalhemispherelight.md)   | Wertet ein Licht aus, bei dem es sich um eine lineare interpolung zwischen zwei Farben handelt (eine auf jedem Pol einer Kugel).         |

    

     

3.  Berechnen Sie die Exit-Strahlkraft.

    Gleichung 1 muss nun entweder mit einem Scheitelpunkt oder einem Pixelshader an jedem Punkt ausgewertet werden. Bevor der Shader ausgewertet werden kann, müssen Konstanten vorab berechnet und in die Konstante Tabelle geladen werden (Weitere Informationen finden Sie im [PRT-Demo Beispiel](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) ). Der Shader selbst ist eine einfache Implementierung dieser Gleichung.

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

    

## <a name="references"></a>References

Weitere Informationen zu PRT-und sphärischen Harmonisierungen finden Sie in den folgenden Artikeln:


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

[Erweiterte Themen](advanced-topics.md)
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

[Voraus berechnete Strahlungs Übertragungsfunktionen](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




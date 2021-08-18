---
description: Beim Rendern der 2D-Ausgabe mit vortransformationen Scheitelpunkten muss darauf geachtet werden, dass jeder Texelbereich ordnungsgemäß einem einzelnen Pixelbereich entspricht, da andernfalls Texturverzerrung auftreten kann.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Direktes Zuordnen von Texels zu Pixeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7294b88fb8b672aea980dbb23cb4e7c5bbd2bfdbf4d33a5078a09dbfa3084d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988260"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>Direktes Zuordnen von Texels zu Pixeln (Direct3D 9)

Beim Rendern der 2D-Ausgabe mit vortransformationen Scheitelpunkten muss darauf geachtet werden, dass jeder Texelbereich ordnungsgemäß einem einzelnen Pixelbereich entspricht, da andernfalls Texturverzerrung auftreten kann. Wenn Sie die Grundlagen des Prozesses verstehen, dem Direct3D beim Rastern und Texturieren von Dreiecken folgt, können Sie sicherstellen, dass Ihre Direct3D-Anwendung die 2D-Ausgabe ordnungsgemäß rendert.

![Abbildung einer 6x6-Auflösungsanzeige](images/maptex-fig1.png)

Das obige Diagramm zeigt Pixel, die als Quadrate modelliert werden. In Wirklichkeit sind Pixel jedoch Punkte, keine Quadrate. Jedes Quadrat im vorherigen Diagramm gibt den durch das Pixel beleuchteten Bereich an, aber ein Pixel ist immer nur ein Punkt in der Mitte eines Quadrats. Diese Unterscheidung ist wichtig, obwohl sie scheinbar klein ist. Eine bessere Abbildung der gleichen Anzeige ist im folgenden Diagramm dargestellt.

![Abbildung einer Anzeige, die aus Pixeln besteht](images/maptex-fig2.png)

Das obige Diagramm zeigt jedes physische Pixel ordnungsgemäß als Punkt in der Mitte jeder Zelle an. Die Bildschirmraumkoordinate (0, 0) befindet sich direkt am oberen linken Pixel und somit in der Mitte der linken oberen Zelle. Die obere linke Ecke der Anzeige befindet sich daher bei (-0,5, -0,5), da sie 0,5 Zellen links und 0,5 Zellen vom oberen linken Pixel entfernt ist. Direct3D rendert ein Quader mit Ecken bei (0, 0) und (4, 4), wie in der folgenden Abbildung dargestellt.

![Abbildung eines Umrisses eines unrasterisierten Quaders zwischen (0, 0) und (4, 4)](images/maptex-fig3.png)

Die obige Abbildung zeigt, wo sich das mathematische Quader im Verhältnis zur Anzeige befindet, zeigt jedoch nicht, wie das Quader aussehen wird, sobald Direct3D es rastert und an die Anzeige sendet. Tatsächlich ist es unmöglich, dass eine Rasteranzeige das Quad genau wie gezeigt auffüllt, da die Ränder des Quaders nicht mit den Grenzen zwischen Pixelzellen übereinstimmen. Anders ausgedrückt: Da jedes Pixel nur eine einzelne Farbe anzeigen kann, wird jede Pixelzelle nur mit einer einzigen Farbe gefüllt. Wenn die Anzeige das Quad genau wie gezeigt rendern würde, müssten die Pixelzellen entlang des Quaderrands zwei unterschiedliche Farben anzeigen: Blau, wo das Quader abgedeckt ist, und weiß, wo nur der Hintergrund sichtbar ist.

Stattdessen wird die Grafikhardware damit beauftragt, zu bestimmen, welche Pixel aufgefüllt werden sollen, um das Quader anzunähern. Dieser Prozess wird als Rasterung bezeichnet und unter [Rasterungsregeln (Direct3D 9)](rasterization-rules.md)ausführlich beschrieben. Für diesen speziellen Fall wird das rasterisierte Quader in der folgenden Abbildung dargestellt.

![Abbildung eines nicht textierten Quaders, gezeichnet von (0,0) bis (4,4)](images/maptex-fig4.png)

Beachten Sie, dass das an Direct3D übergebene Quader Ecken bei (0, 0) und (4, 4) hat, aber die gerasterte Ausgabe (die obige Abbildung) Ecken bei (-0,5,-0,5) und (3,5,3,5) hat. Vergleichen Sie die beiden obigen Abbildungen auf Renderingunterschiede. Sie können sehen, dass das, was die Anzeige tatsächlich rendert, die richtige Größe ist, aber um -0,5 Zellen in die x- und y-Richtung verschoben wurde. Mit Ausnahme von Multisamplingtechniken ist dies jedoch die bestmögliche Annäherung an den Quader. (Ausführliche Informationen zur Mehrfachsampling finden Sie im [Antialias-Beispiel.)](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) Beachten Sie, dass der resultierende Bereich der Dimension 5 x 5 anstelle der gewünschten 4 x 4 ist, wenn der Rasterizer jede Zelle auffüllt, die das Quader gekreuzt hat.

Wenn Sie davon ausgehen, dass Bildschirmkoordinaten aus der oberen linken Ecke des Anzeigerasters und nicht aus dem oberen linken Pixel stammen, wird das Quad genau wie erwartet angezeigt. Der Unterschied wird jedoch deutlich, wenn dem Quad eine Textur gegeben wird. Die folgende Abbildung zeigt die 4 x 4-Textur, die Sie direkt dem Quader zuordnen.

![Abbildung einer 4x4-Textur](images/maptex-fig5.png)

Da die Textur 4 x 4 Texel und das Quader 4 x 4 Pixel beträgt, können Sie davon ausgehen, dass das texturierte Quad genau wie die Textur angezeigt wird, unabhängig von der Position auf dem Bildschirm, auf dem das Quader gezeichnet wird. Dies ist jedoch nicht der Fall. sogar geringfügige Positionsänderungen beeinflussen, wie die Textur angezeigt wird. Die folgende Abbildung zeigt, wie ein Quader zwischen (0, 0) und (4, 4) nach der Rasterung und Textur angezeigt wird.

![Abbildung eines texturierten Quaders aus (0, 0) und (4, 4)](images/maptex-fig6.png)

Das in der obigen Abbildung gezeichnete Quader zeigt die texturierte Ausgabe (mit einem linearen Filtermodus und einem Klammeradressierungsmodus) mit der überlagerten rasterten Kontur. Im restlichen Teil dieses Artikels wird genau erläutert, warum die Ausgabe so aussieht, wie sie aussieht, anstatt wie die Textur aussieht. Für diejenigen, die die Lösung wünschen, ist dies hier: Die Ränder des Eingabequadards müssen sich auf den Begrenzungslinien zwischen Pixelzellen befinden. Indem die x- und y-Quad-Koordinaten einfach um -0,5 Einheiten verschoben werden, decken Texelzellen die Pixelzellen perfekt ab, und das Quader kann auf dem Bildschirm perfekt neu erstellt werden. (Die letzte Abbildung in diesem Thema zeigt das Quad an den korrigierten Koordinaten.)

Die Details, warum die gerasterte Ausgabe nur eine geringfügige Ähnlichkeit mit der Eingabetextur auf sich hat, hängen direkt mit der Art und Weise zusammen, in der Direct3D-Adressen und Stichprobentexturen vorliegen. Im Folgenden wird davon ausgegangen, dass Sie über ein gutes Verständnis des [Texturkoordinatenraums](texture-coordinates.md) und [der bilinearen Texturfilterung verfügen.](bilinear-texture-filtering.md)

Es ist sinnvoll, die Ausgabefarbe auf den Pixel-Shader zurückzuverfolgen, um zur Untersuchung der ungewöhnlichen Pixelausgabe zurückzukehren: Der Pixelshader wird für jedes ausgewählte Pixel aufgerufen, um Teil der gerasterten Form zu sein. Das in einer früheren Abbildung dargestellte blaue Quader könnte einen besonders einfachen Shader aufweisen:


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



Für den texturierten Quader muss der Pixelshader geringfügig geändert werden:


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



Dieser Code setzt voraus, dass die 4 x 4-Textur in MyTexture gespeichert ist. Wie gezeigt, ist der MySampler-Textur-Sampler so festgelegt, dass bilineare Filterung für MyTexture ausgeführt wird. Der Pixel-Shader wird einmal für jedes gerasterte Pixel aufgerufen, und jedes Mal, wenn die zurückgegebene Farbe die texturierte Texturfarbe in vTexCoord ist. Jedes Mal, wenn der Pixelshader aufgerufen wird, wird das vTexCoord-Argument auf die Texturkoordinaten an diesem Pixel festgelegt. Das bedeutet, dass der Shader den Textur-Sampler nach der gefilterten Texturfarbe an der genauen Position des Pixels fragt, wie in der folgenden Abbildung beschrieben.

![Abbildung der Samplingorte für Texturkoordinaten](images/maptex-fig7.png)

Die Textur (überlagert dargestellt) wird direkt an Pixelpositionen entnommen (als schwarze Punkte dargestellt). Texturkoordinaten sind von der Rasterung nicht betroffen (sie verbleiben im projizierten Bildschirmbereich des ursprünglichen Quaders). Die schwarzen Punkte zeigen an, wo sich die Rasterungspixel befinden. Die Texturkoordinaten an jedem Pixel lassen sich leicht ermitteln, indem die an jedem Scheitelpunkt gespeicherten Koordinaten interpoliert werden: Das Pixel bei (0,0) stimmt mit dem Scheitelpunkt bei (0, 0) überein. Daher sind die Texturkoordinaten an diesem Pixel einfach die Texturkoordinaten, die an diesem Scheitelpunkt gespeichert sind, UV (0,0, 0,0). Für das Pixel bei (3, 1) sind die interpolierten Koordinaten UV (0,75, 0,25), da sich dieses Pixel bei drei Vierteln der Breite der Textur und einem Viertel seiner Höhe befindet. Diese interpolierten Koordinaten werden an den Pixelshader übergeben.

Die Texel stehen in diesem Beispiel nicht mit den Pixeln an. jedes Pixel (und somit jeder Samplingpunkt) wird an der Ecke von vier Texeln positioniert. Da der Filtermodus auf Linear festgelegt ist, durchschnittlich der Sampler die Farben der vier Texel, die diese Ecke teilen. Dies erklärt, warum das Pixel, das rot sein sollte, tatsächlich drei Viertel grau plus ein Viertes Rot ist, das Pixel, das grün sein sollte, ein halbes Grau plus ein viertes Rot plus ein Viertes Grün usw.

Um dieses Problem zu beheben, müssen Sie lediglich das Quader ordnungsgemäß den Pixeln zuordnen, zu denen es gerastt wird, und damit die Texel korrekt Pixeln zuordnen. Die folgende Abbildung zeigt die Ergebnisse des Zeichnens des gleichen Quaders zwischen (-0,5, -0,5) und (3,5, 3,5), bei dem es sich um das von Anfang an vorgesehene Quader handelt.

![Abbildung eines texturierten Quaders, der mit dem gerasterten Quader übereinstimmt](images/maptex-fig8.png)

Die obige Abbildung zeigt, dass das Quader (dargestellt von (-0,5, -0,5) bis (3,5, 3,5)) genau mit dem gerasterten Bereich übereinstimmt.

## <a name="summary"></a>Zusammenfassung

Zusammengefasst sind Pixel und Texel tatsächlich Punkte, keine Vollkörperblöcke. Der Bildschirmbereich stammt aus dem oberen linken Pixel, Texturkoordinaten stammen jedoch in der linken oberen Ecke des Rasters der Textur. Denken Sie vor allem daran, 0,5 Einheiten von den x- und y-Komponenten Ihrer Scheitelpunktpositionen zu subtrahieren, wenn Sie im transformierten Bildschirmbereich arbeiten, um Texel ordnungsgemäß an Pixeln auszurichten.

Der folgende Code ist ein Beispiel für das Zurücksetzen der Scheitelpunkte eines 256 x 256-Quadrats, um eine 256 x 256-Textur im transformierten Bildschirmbereich ordnungsgemäß anzuzeigen.


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturkoordinaten](texture-coordinates.md)
</dt> </dl>

 

 




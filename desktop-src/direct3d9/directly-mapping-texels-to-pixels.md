---
description: Beim Rendern der 2D-Ausgabe mithilfe von vortransformierten Scheitel Punkten muss sorgfältig vorgegangen werden, um sicherzustellen, dass jeder texturbereich ordnungsgemäß einem einzelnen Pixel Bereich entspricht. andernfalls kann eine Textur Verzerrung auftreten.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Direkte Zuordnung von Texels zu Pixeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213928"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>Direkte Zuordnung von Texels zu Pixeln (Direct3D 9)

Beim Rendern der 2D-Ausgabe mithilfe von vortransformierten Scheitel Punkten muss sorgfältig vorgegangen werden, um sicherzustellen, dass jeder texturbereich ordnungsgemäß einem einzelnen Pixel Bereich entspricht. andernfalls kann eine Textur Verzerrung auftreten. Wenn Sie die Grundlagen des Prozesses verstehen, den Direct3D bei der rasterisierung und Texturierung von Dreiecken befolgt, können Sie sicherstellen, dass Ihre Direct3D-Anwendung die 2D-Ausgabe korrekt

![Abbildung einer 6x6-Auflösungs Anzeige](images/maptex-fig1.png)

Das vorangehende Diagramm zeigt Pixel, die als Quadraten modelliert werden. In der Realität sind Pixel jedoch Punkte und keine Quadrate. Jedes Quadrat im vorangehenden Diagramm gibt den Bereich an, der durch das Pixel beleuchtet ist, aber ein Pixel ist immer nur ein Punkt in der Mitte eines Quadrats. Dieser Unterschied ist, obwohl er scheinbar klein ist, wichtig. In der folgenden Abbildung ist eine bessere Darstellung der gleichen Anzeige dargestellt.

![Abbildung einer Anzeige, die aus Pixeln besteht](images/maptex-fig2.png)

Das vorangehende Diagramm zeigt jedes physische Pixel ordnungsgemäß als Punkt in der Mitte der einzelnen Zellen an. Die Bildschirmraum Koordinate (0,0) befindet sich direkt am oberen linken Pixel und somit in der Mitte der linken oberen Zelle. Die linke obere Ecke der Anzeige liegt daher bei (-0,5,-0,5), da es sich um 0,5 Zellen links und 0,5 Zellen aus dem oberen linken Pixel handelt. Direct3D führt ein vierfache mit Ecken bei (0,0) und (4, 4) aus, wie in der folgenden Abbildung dargestellt.

![Darstellung eines Gliederung eines unrasterisierten Quad zwischen (0,0) und (4, 4)](images/maptex-fig3.png)

In der obigen Abbildung wird gezeigt, wo sich das mathematische Vierfache in Bezug auf die Anzeige befindet, aber nicht, wie das Vierfache aussehen wird Direct3D es wird ein-und an die Anzeige gesendet. In der Tat ist es für eine Raster Anzeige nicht möglich, das Vierfache genau wie gezeigt auszufüllen, da die Ränder des Quad nicht mit den Begrenzungen zwischen Pixel Zellen übereinstimmen. Anders ausgedrückt: Da jedes Pixel nur eine einzelne Farbe anzeigen kann, wird jede Pixel Zelle nur mit einer einzelnen Farbe gefüllt. Wenn die Anzeige das Vierfache genau wie gezeigt Rendern würde, müssten die Pixel Zellen entlang des viergs des vierels zwei unterschiedliche Farben anzeigen: blau, wobei durch das vierfach und weiß abgedeckt ist, wo nur der Hintergrund sichtbar ist.

Stattdessen wird die Grafikhardware dafür zuständig, zu bestimmen, welche Pixel aufgefüllt werden sollten, um das Vierfache zu überstehen. Dieser Prozess wird als rasterization bezeichnet und wird in [rasterisierungsregeln (Direct3D 9)](rasterization-rules.md)ausführlich erläutert. In diesem speziellen Fall wird das unregelmäßige Vierfache in der folgenden Abbildung dargestellt.

![Abbildung eines unstrukturierten Quad von (0,0) bis (4, 4)](images/maptex-fig4.png)

Beachten Sie, dass das an Direct3D über gebene vierfache Ecken an (0,0) und (4, 4) aufweist, aber die gerastererte Ausgabe (die vorherige Abbildung) die Ecken (-0,5,-0,5) und (3,5, 3.5) enthält. Vergleichen Sie die vorangehenden beiden Abbildungen mit renderingunterschieden. Wie Sie sehen, ist die tatsächliche Größe der Anzeige die richtige Größe, Sie wurde jedoch um-0,5 Zellen in der x-und y-Richtung verschoben. Mit Ausnahme von Multisampling-Techniken ist dies jedoch die bestmögliche Näherung für das Vierfache. (Eine ausführliche Abdeckung von Multisampling finden Sie im [Beispiel für AntiAlias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) .) Beachten Sie, dass der resultierende Bereich der Dimension 5 x 5 statt der gewünschten 4 x 4 ist, wenn der Raster jede Zelle gefüllt hat.

Wenn Sie davon ausgehen, dass Bildschirm Koordinaten von der oberen linken Ecke des anzeigerasters anstatt vom oberen linken Pixel stammen, wird das Quad genau wie erwartet angezeigt. Der Unterschied wird jedoch deutlich, wenn dem Quad eine Textur zugewiesen wird. Die folgende Abbildung zeigt die 4 x 4-Textur, die Sie direkt dem Quad zuordnen.

![Abbildung einer 4 x 4-Textur](images/maptex-fig5.png)

Da es sich bei der Textur um 4 x 4 texeln handelt und das Vierfache 4 x 4 Pixel beträgt, können Sie davon ausgehen, dass das eingetextete Quad genau wie die Textur angezeigt wird, unabhängig von der Position auf dem Bildschirm, an der das Vierfache gezeichnet wird Dies ist jedoch nicht der Fall. sogar geringfügige Änderungen an der Position beeinflussen, wie die Textur angezeigt wird. In der folgenden Abbildung wird gezeigt, wie ein Quad zwischen (0,0) und (4, 4) angezeigt wird, nachdem es gerastert und strukturiert wurde.

![Abbildung eines strukturierten Quad, gezeichnet von (0,0) und (4, 4)](images/maptex-fig6.png)

Das in der obigen Abbildung gezeichnete vierfache zeigt die texturierte Ausgabe (mit einem linearen Filter Modus und einem Klammer Adressierungs Modus) mit der übergeordneten gerastten Gliederung. Im weiteren Verlauf dieses Artikels wird erläutert, warum die Ausgabe so aussieht, wie Sie aussieht, anstatt Sie wie die Textur zu betrachten. für diejenigen, die die Projekt Mappe wünschen, ist dies der Grund: die Ränder der Eingabe Quad müssen auf den Begrenzungs Linien zwischen Pixel Zellen liegen. Wenn Sie die x-und y-Quad-Koordinaten einfach um-0,5-Einheiten bewegen, decken textezellen Pixel Zellen perfekt ab, und das Vierfache kann auf dem Bildschirm vollständig neu erstellt werden. (Die letzte Abbildung in diesem Thema zeigt den Quad an den korrigierten Koordinaten.)

Die Details, warum die gerasterte Ausgabe nur geringfügige Ähnlichkeit mit der Eingabe Textur hat, sind direkt mit der Art und Weise verknüpft, in der sich die Texturen Direct3D-Adressen und-Beispiele Dabei wird davon ausgegangen, dass Sie über einen guten Einblick in den [Texturkoordinaten Bereich](texture-coordinates.md) und die [bilineare Textur Filterung](bilinear-texture-filtering.md)verfügen.

Wenn wir uns mit der Untersuchung der seltsamen Pixel Ausgabe auseinander bewegen, ist es sinnvoll, die Ausgabe Farbe zurück zum Pixelshader zu verfolgen: der Pixelshader wird für jedes Pixel aufgerufen, das Teil der rasterisierten Form ist. Das in einer früheren Abbildung gezeigte voll Bild blaue Quad könnte einen besonders einfachen Shader aufweisen:


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



Für das strukturierte vierfache muss der Pixelshader etwas geändert werden:


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



Dieser Code setzt voraus, dass die 4 x 4-Textur in MyTexture gespeichert wird. Wie gezeigt, wird der mysampler-Textur Sampler so festgelegt, dass er eine bilineare Filterung auf MyTexture ausführt. Der Pixelshader wird einmal für jedes gerastererte Pixel aufgerufen, und jedes Mal, wenn die zurückgegebene Farbe die Stichproben Textur Farbe bei vtexcoord ist. Jedes Mal, wenn der Pixelshader aufgerufen wird, wird das vtexcoord-Argument auf die Texturkoordinaten an diesem Pixel festgelegt. Dies bedeutet, dass der Shader den Textur Sampler an der genauen Position des Pixels an der genauen Position des Pixels anfordert, wie in der folgenden Abbildung dargestellt.

![Abbildung der Stichproben Positionen für Texturkoordinaten](images/maptex-fig7.png)

Die Textur (angezeigte übergeordnete Darstellung) wird direkt an Pixelpositionen (als schwarze Punkte angezeigt) entnommen. Texturkoordinaten sind von der rasterisierung nicht betroffen (Sie verbleiben im projizierten Bildschirmbereich des ursprünglichen Quad). Die schwarzen Punkte zeigen an, wo die rasterisierungspixel liegen. Die Texturkoordinaten an jedem Pixel können leicht durch Interpolation der in jedem Scheitelpunkt gespeicherten Koordinaten bestimmt werden: das Pixel bei (0,0) stimmt mit dem Scheitelpunkt bei (0,0) überein. Daher sind die Texturkoordinaten an diesem Pixel einfach die Texturkoordinaten, die an diesem Scheitelpunkt, UV (0,0, 0,0), gespeichert sind. Für das Pixel um (3, 1) sind die interpoliert-Koordinaten "UV (0,75, 0,25)", da sich dieses Pixel in drei Vierteln der Textur Breite und ein vierstel seiner Höhe befindet. Diese interpoliert-Koordinaten werden an den Pixelshader übermittelt.

Die texeln sind in diesem Beispiel nicht mit den Pixeln identisch. jedes Pixel (und somit jeder Stichproben Punkt) wird in der Ecke von vier texeln positioniert. Da der Filter Modus auf Linear festgelegt ist, durchläuft der Sampler die Farben der vier texeln, die diese Ecke teilen. Dadurch wird erläutert, warum das Pixel, das als rot erwartet wird, tatsächlich aus drei viertem Grau plus einem vierten rot besteht. das Pixel, das grün sein soll, ist ein Halbton Grau plus ein viertes rot plus ein viertes grün usw.

Um dieses Problem zu beheben, müssen Sie lediglich das Vierfache zu den Pixeln zuordnen, zu denen es gerengt wird, und die texeln ordnungsgemäß den Pixeln zuordnen. In der folgenden Abbildung sind die Ergebnisse der Zeichnung desselben viervieres zwischen (-0,5,-0,5) und (3,5, 3,5) dargestellt. Dies ist der von Anfang an vorgesehene Quad.

![Abbildung eines strukturierten Quad, das mit dem rasterisierten Quad übereinstimmt](images/maptex-fig8.png)

In der obigen Abbildung wird veranschaulicht, dass das Quad (dargestellt von (-0,5,-0,5) bis (3,5, 3,5)) exakt mit dem rasterisierten Bereich übereinstimmt.

## <a name="summary"></a>Zusammenfassung

Zusammenfassend sind Pixel und texeln tatsächlich Punkte, keine Solid-Blöcke. Der Bildschirmbereich stammt vom oberen linken Pixel, aber die Texturkoordinaten stammen von der oberen linken Ecke des Struktur Rasters. Am wichtigsten ist, dass Sie 0,5 Einheiten von den x-und y-Komponenten Ihrer Scheitelpunkt Positionen subtrahieren, wenn Sie in transformier ter Bildschirmfläche arbeiten, um texeln ordnungsgemäß mit Pixel auszurichten.

Der folgende Code ist ein Beispiel für das versetzen der Scheitel Punkte eines 256 256-Quadrat-Quadrats zum ordnungsgemäßen Anzeigen der Textur 256 by 256 im transformierten Bildschirmbereich.


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

 

 




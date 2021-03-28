---
title: Benutzer Clip Flächen auf Featureebene 9 Hardware
description: Ab Windows 8 unterstützt Microsoft High Level Shader Language (HLSL) eine Syntax, die Sie mit der Microsoft Direct3D 11-API zum Angeben von Benutzer Clip Flächen auf Featureebene 9 \_ x und höher verwenden können.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315572"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a>Benutzer Clip Flächen auf Featureebene 9 Hardware

Ab Windows 8 unterstützt Microsoft High Level Shader Language (HLSL) eine Syntax, die Sie mit der Microsoft Direct3D 11-API zum Angeben von Benutzer Clip Flächen auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher verwenden können. Sie können diese Clip-Plane-Syntax verwenden, um einen Shader zu schreiben, und dann dieses Shader-Objekt mit der Direct3D 11-API verwenden, um Sie auf allen Direct3D-Funktionsebenen auszuführen.

-   [Hintergrund](#background-reading)
-   [Syntax](#syntax)
-   [Erstellen von Clip-Flächen im Clip Bereich auf Featureebene 9 und höher](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [Hintergrund Lesevorgänge](#background-reading)
    -   [10 Level9-Funktionsebenen](#10level9-feature-levels)
    -   ["Clip Plane Math"](#clip-plane-math)
    -   [Clipping im Anzeigebereich](#clipping-in-view-space)
    -   [Projektions Matrix](#projection-matrix)
    -   [Clip Space Clip-Ebene](#clip-space-clip-plane)
-   [Zugehörige Themen](#related-topics)

## <a name="background"></a>Hintergrund

Sie können in der Microsoft Direct3D 9-API über [**IDirect3DDevice9:: setclipplane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) -und [**IDirect3DDevice9:: getclipplane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) -Methoden auf Benutzer Clip Flächen zugreifen. In Microsoft Direct3D 10 und höher können Sie auf Benutzer Clip Flächen über die Semantik " [SV \_ clipdistance](dx-graphics-hlsl-semantics.md) " zugreifen. Doch vor Windows 8 war "SV \_ clipdistance" in den [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ APIs Direct3D 10 oder Direct3D 11 nicht für die Funktionsebene 9 x-Hardware verfügbar. Vor Windows 8 war die einzige Möglichkeit für den Zugriff auf Benutzer Clip-und Featureebene mit 9 \_ x-Hardware die API Direct3D 9. Direct3D Windows Store-Apps können die Direct3D 9-API nicht verwenden. Hier wird die Syntax beschrieben, die Sie verwenden können, um über die Direct3D 11-API auf Featureebene 9 x und höher auf Benutzer Clip Flächen zuzugreifen \_ .

-Apps verwenden Clip Flächen, um eine Reihe von nicht sichtbaren Ebenen innerhalb der 3D-Welt zu definieren, die alle gezeichneten primitiven Ausschneiden (lösen). Windows zeichnet kein Pixel, das sich auf der negativen Seite von Clip Flächen befindet. Apps können dann mithilfe von Clip-Ebenen planare Reflektionen Rendering.

## <a name="syntax"></a>Syntax

Verwenden Sie diese Syntax, um Clip-Ebenen als Funktions Attribute in einer [Funktionsdeklaration](dx-graphics-hlsl-function-syntax.md)zu deklarieren. Hier verwenden wir beispielsweise die Syntax für ein Vertex-Shader-Fragment:

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

Dieses Beispiel für ein Scheitelpunkt-Shader-Fragment deutet auf zwei Clip-Flächen hin. Es zeigt, dass Sie das neue **clipplane** -Attribut in eckigen Klammern direkt vor dem Rückgabewert des Vertexshaders platzieren müssen. Innerhalb von Klammern nach dem **clipplane** -Attribut geben Sie eine Liste von bis zu 6 **float4** Konstanten an, die die ebenenkoeffizienten für die einzelnen aktiven Clip Ebenen definieren. Das Beispiel zeigt auch, dass Sie die Koeffizienten der einzelnen Ebenen in einem konstanten Puffer erstellen müssen.

> [!Note]  
> Es ist keine Syntax verfügbar, um eine Clip-Ebene dynamisch zu deaktivieren. Sie müssen entweder einen anderweitig identischen Shader ohne **clipplane** -Attribut neu kompilieren, oder die APP kann die Koeffizienten im Konstanten Puffer auf 0 (null) festlegen, sodass sich die Ebene nicht mehr auf Geometrie auswirkt.

 

Diese Syntax ist für jedes 4,0-oder spätere Scheitelpunkt-Shader-Ziel verfügbar, das vs \_ 4 \_ 0 \_ Level \_ 9 \_ 1 und vs \_ 4 \_ 0 \_ Level \_ 9 \_ 3 umfasst.

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a>Erstellen von Clip-Flächen im Clip Bereich auf Featureebene 9 und höher

Hier wird gezeigt, wie Sie Clip-und Ausschneide Flächen auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher erstellen.

### <a name="background-reading"></a>Hintergrund Lesevorgänge

"Einführung in 3D-Spieleprogrammierung mit DirectX 10" von Frank D. Luna erläutert den mathematischen Hintergrund der Grafik (Kapitel 1, 2 und 3), die Sie benötigen, und die verschiedenen Leerzeichen und Leerzeichen Transformationen, die im Vertex-Shader (Abschnitte 5,6 und 5,8) vorkommen.

### <a name="10level9-feature-levels"></a>10 Level9-Funktionsebenen

In Direct3D 10 und höher können Sie alle Bereiche, die sinnvoll sind, im Raum der Welt und im Bereich von Sicht Vorschauen. In Direct3D 9 wird jedoch Clip Space verwendet, bei dem es sich um einen vorperspektiven-Projektions Bereich handelt. Vektoren befinden sich im Ausschneide Bereich, wenn der Vertexshader Sie an Stufen übergibt, die in der [Grafik Pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline)befolgt werden.

Wenn Sie eine Windows Store-App schreiben, müssen Sie die featureebenen 10level9 ([Funktionsebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) verwenden, damit die APP auf Featureebene mit 9 \_ x und höherer Hardware ausgeführt werden kann. Da Ihre APP die Featureebene 9 \_ x und höher unterstützt, müssen Sie auch die gängige Funktion zum Anwenden von Clip-Flächen im Clip Bereich verwenden.

Wenn Sie einen Vertex-Shader mit vs \_ 4 \_ 0 \_ Level \_ 9 \_ 1 oder höher kompilieren, kann der Vertexshader das **clipplane** -Attribut verwenden. Ein Direct3D 10-Objekt oder ein späteres Objekt verfügt über ein Punktprodukt des ausgegebenen Vertex, das jede der im-Attribut angegebenen globalen **float4** -Konstanten enthält. Das Direct3D 9-Objekt verfügt über genügend Metadaten, damit die 10level9-Laufzeit die entsprechenden Aufrufe an [**IDirect3DDevice9:: setclipplane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane)ausgibt.

### <a name="clip-plane-math"></a>"Clip Plane Math"

Eine Clip Ebene wird durch einen Vektor mit vier Komponenten definiert. Die ersten drei Komponenten definieren einen x-, y-und z-Vektor, der vom Ursprung im Bereich ausgeht, den wir ausschneiden möchten. Dieser Vektor impliziert eine Ebene, die senkrecht zum Vektor und durch den Ursprung verläuft. Windows behält alle Pixel auf der Vektor Seite der Ebene bei und schneidet alle Pixel hinter der Ebene ab. Die Komponente "weiter w" überträgt die Ebene zurück und bewirkt, dass Windows einen kürzeren Clip bewirkt (ein negativer Wert bewirkt, dass Fenster mehr) entlang der Vektor Linie angezeigt werden. Wenn die x-, y-und z-Komponenten einen (normalisierten) Einheits Vektor bilden, überträgt w die Einheiten der Ebene w zurück.

Die von der GPU (Graphics Processing Unit) durchgeführte Mathematik ist ein einfaches Punktprodukt zwischen dem Scheitelpunkt Vektor (x, y, z, 1) und dem Vektor der Clippingebene. Dieser mathematische Vorgang erstellt eine Projektions Länge auf dem Clip Ebenen-Vektor. Ein negatives Punktprodukt zeigt den Scheitelpunkt auf der ausgeschnittenen Seite der Ebene an.

### <a name="clipping-in-view-space"></a>Clipping im Anzeigebereich

Hier ist unser Scheitelpunkt im Ansichts Bereich:

![Scheitelpunkt im Anzeigebereich](images/vertex-clip.png)

Hier sehen Sie unsere Ausschneide Ebene im Anzeigebereich:

![Ausschneide Ebene im Anzeigebereich](images/clip-plane-view.png)

Hier ist das Punktprodukt von Vertex und clisebene im Ansichts Raum:

Clipdistance = **v** = **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>

Diese mathematische Operation funktioniert für ein Direct3D 10-Objekt oder ein späteres Objekt, funktioniert aber nicht für ein Direct3D 9-Objekt. Für Direct3D 9 müssen wir zuerst unsere Projektions Transformation in Clip Space durchlaufen.

### <a name="projection-matrix"></a>Projektions Matrix

Eine Projektions Matrix wandelt einen Scheitelpunkt aus dem Ansichts Raum um (wobei der Ursprung das Auge des Viewers ist, + x nach rechts, + y ist hoch und + z direkt vorwärts) in den Clip Bereich. Die Projektions Matrix gibt den Scheitelpunkt für das Hardware Clipping und die [rasterisierungsphase](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage)wieder. Dies ist eine standardmäßige Perspektiven Matrix (andere Projektionen erfordern unterschiedliche mathematische):

<dl> *r*   -Verhältnis der Fensterbreite/-Höhe  
   Anzeige Winkel von i  
*f* -   Entfernung vom Viewer zur äußersten Ebene  
*n*   Entfernung vom Viewer zur near-Ebene
</dl>![Projektions Matrix](images/projection-matrix.png)

Die nächste Matrix ist eine vereinfachte Version der vorherigen Matrix. Die Matrix wird vereinfacht, sodass Sie später im Matrix Multiplikations Vorgang verwendet werden kann.

![vereinfachte Projektions Matrix](images/projection-matrix2.png)

Nun transformieren wir den Scheitelpunkt Scheitelpunkt in einen Clip Bereich mit einer Matrix Multiplikation:

![Matrix multiplizieren](images/matrix-multiply.png)

Bei der Matrix Multiplikation werden unsere x-und y-Komponenten nur geringfügig angepasst, aber unsere z-und w-Komponenten sind recht verändert. Unsere clisebene gibt uns nicht mehr, was wir wollen.

### <a name="clip-space-clip-plane"></a>Clip Space Clip-Ebene

Hier möchten wir eine Clip Space-Clip-Ebene erstellen, deren Punktprodukt mit dem Clip Space-Scheitelpunkt denselben Wert wie v = hat. **C** im Abschnitt [Clipping im Bereich Anzeige](#clipping-in-view-space) Bereich.

![clipbene](images/clip-space-clip-plane.png)

**v** **C**  =  **v P** **C**<sub>P</sub>

*v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *p* ₓ *C*<sub>p ₓ</sub>  + *v*<sub>y</sub>*p*<sub>y</sub>*C*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub>z</sub></sub>  +  *BC*<sub>p <sub>z</sub></sub>  +  *v*<sub>z</sub>*c*<sub>p <sub>w</sub></sub>

Nun können wir den vorangehenden mathematischen Vorgang von der Scheitelpunkt Komponente in vier separate Gleichungen aufteilen:

![x-Scheitelpunkt Komponente des Clip-Plane-Produkts](images/clip-space-clip-plane-equ1.png)

![y-Scheitelpunkt Komponente des Clip-Plane-Produkts](images/clip-space-clip-plane-equ2.png)

![w-Scheitelpunkt Komponente des Clip-Plane-Produkts](images/clip-space-clip-plane-equ3.png)

![z-Scheitelpunkt Komponente des Clip-Plane-Produkts](images/clip-space-clip-plane-equ4.png)

Unsere Ausschneide Ebene des Ansichts Raums und unsere Projektions Matrix werden abgeleitet

![Clip Space Clip-Ebene](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Syntax der Funktionsdeklaration](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 
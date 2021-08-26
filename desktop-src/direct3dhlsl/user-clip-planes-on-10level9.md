---
title: Benutzerclipebenen auf Hardware auf Featureebene 9
description: Ab Windows 8 unterstützt Microsoft High Level Shader Language (HLSL) eine Syntax, die Sie mit der Microsoft Direct3D 11-API verwenden können, um Benutzerclipebenen auf Featureebene 9 \_ x und höher anzugeben.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6ffd624e688dbe5e3591e10ee5c005a9d4564dc5a536e9c89cfcee50067c2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948970"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a>Benutzerclipebenen auf Hardware auf Featureebene 9

Ab Windows 8 unterstützt Microsoft High Level Shader Language (HLSL) eine Syntax, die Sie mit der Microsoft Direct3D 11-API verwenden können, um Benutzerclipebenen auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher anzugeben. Sie können diese Syntax für Clipebenen verwenden, um einen Shader zu schreiben, und dann dieses Shaderobjekt mit der Direct3D 11-API für die Ausführung auf allen Direct3D-Featureebenen verwenden.

-   [Hintergrund](#background-reading)
-   [Syntax](#syntax)
-   [Erstellen von Clipebenen im Clipspace auf Featureebene 9 und höher](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [Hintergrundlesezeit](#background-reading)
    -   [10Level9-Featureebenen](#10level9-feature-levels)
    -   [Clipebenenmathematik](#clip-plane-math)
    -   [Beschneiden im Ansichtsbereich](#clipping-in-view-space)
    -   [Projektionsmatrix](#projection-matrix)
    -   [Clip space clip plane (Clip space clip plane)](#clip-space-clip-plane)
-   [Zugehörige Themen](#related-topics)

## <a name="background"></a>Hintergrund

Sie können über die Methoden [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) und [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) auf Benutzerclipebenen in der Microsoft Direct3D 9-API zugreifen. In Microsoft Direct3D 10 und höher können Sie über die [SV \_ ClipDistance-Semantik](dx-graphics-hlsl-semantics.md) auf Benutzerclipebenen zugreifen. Vor Windows 8 war SV \_ ClipDistance jedoch nicht für [Hardware auf Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x in den Direct3D 10- oder Direct3D 11-APIs verfügbar. Vor Windows 8 war die einzige Möglichkeit, auf Benutzerclipebenen mit Hardware der Featureebene 9 x zuzugreifen, \_ die Direct3D 9-API. Direct3D Windows Store-Apps können die Direct3D 9-API nicht verwenden. Hier wird die Syntax beschrieben, mit der Sie über die Direct3D 11-API auf Featureebene 9 x und höher auf Benutzerclipebenen zugreifen \_ können.

Apps verwenden Clipebenen, um eine Reihe unsichtbarer Ebenen innerhalb der 3D-Welt zu definieren, die alle gezeichneten Primitive abschneiden (wegwerfen). Windows zeichnen kein Pixel, das sich auf der negativen Seite von Clipebenen befindet. Apps können dann Clipebenen verwenden, um planare Reflektionen zu rendern.

## <a name="syntax"></a>Syntax

Verwenden Sie diese Syntax, um Clipebenen als Funktionsattribute in einer [Funktionsdeklaration](dx-graphics-hlsl-function-syntax.md)zu deklarieren. Hier verwenden wir beispielsweise die Syntax für ein Vertex-Shaderfragment:

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

Dieses Beispiel für ein Vertex-Shaderfragment gibt zwei Clipebenen an. Es zeigt, dass Sie das neue **Clipplanes-Attribut** direkt vor dem Rückgabewert des Scheitelpunkt-Shaders in eckigen Klammern platzieren müssen. In Klammern nach dem **Clipplanes-Attribut** stellen Sie eine Liste mit bis zu 6 **float4-Konstanten** bereit, die die Ebenenkoeffizienten für jede aktive Clipebene definieren. Das Beispiel zeigt auch, dass Sie die Koeffizienten jeder Ebene in einem konstanten Puffer befinden müssen.

> [!Note]  
> Es ist keine Syntax verfügbar, um eine Clipebene dynamisch zu deaktivieren. Sie müssen entweder einen ansonsten identischen Shader ohne **Clipplanes-Attribut** neu kompilieren, oder Ihre App kann die Koeffizienten in Ihrem konstanten Puffer auf 0 (null) festlegen, damit die Ebene keine Geometrie mehr beeinflusst.

 

Diese Syntax ist für alle 4.0- oder höher-Vertex-Shaderziele verfügbar, einschließlich vs \_ 4 \_ 0 \_ Level \_ 9 \_ 1 und \_ vs 4 \_ 0 Level \_ \_ 9 \_ 3.

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a>Erstellen von Clipebenen im Clipspace auf Featureebene 9 und höher

Hier wird gezeigt, wie Clipebenen im Clipspace auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 x und höher erstellt \_ werden.

### <a name="background-reading"></a>Hintergrundlesezeit

"Introduction to 3D Game Programming with DirectX 10" (Einführung in die 3D-Spieleprogrammierung mit DirectX 10) von Frank D. Luna erläutert den mathematischen Grafikhintergrund (Kapitel 1, 2 und 3), den Sie benötigen, sowie die verschiedenen Leerzeichen und Raumtransformationen, die im Vertex-Shader auftreten (Abschnitte 5.6 und 5.8).

### <a name="10level9-feature-levels"></a>10Level9-Featureebenen

In Direct3D 10 und höher können Sie jeden sinnvollen Bereich beschneiden, häufig im Welt- oder Sichtbereich. Direct3D 9 verwendet jedoch einen Clipspace, bei dem es sich um einen Projektionsbereich mit Vorperspektivesteilung handelt. Vektoren befinden sich im Clipspace, wenn der Scheitelpunkt-Shader sie an Phasen übergibt, die in der [Grafikpipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline)folgen.

Wenn Sie eine Windows Store-App schreiben, müssen Sie 10Level9-Featureebenen[(Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 x) verwenden, \_ damit die App auf Hardware der Featureebene 9 x und höher ausgeführt werden \_ kann. Da Ihre App Die Featureebene 9 \_ x und höher unterstützt, müssen Sie auch die allgemeine Funktion zum Anwenden von Clipebenen im Clipspace verwenden.

Wenn Sie einen Vertex-Shader mit \_ 4 \_ 0 Ebene 9 1 oder höher kompilieren, \_ kann dieser \_ \_ Scheitelpunkt-Shader das **Clipplanes-Attribut** verwenden. Ein Direct3D 10-Objekt oder höher verfügt über ein Punktprodukt des ausgegebenen Scheitelpunkts, das jede der globalen **Float4-Konstanten** enthält, die im -Attribut angegeben sind. Das Direct3D 9-Objekt verfügt über genügend Metadaten, damit die 10Level9-Runtime die entsprechenden Aufrufe von [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane)ausstellen kann.

### <a name="clip-plane-math"></a>Clipebenenmathematik

Eine Clipebene wird durch einen Vektor mit vier Komponenten definiert. Die ersten drei Komponenten definieren einen x-, y-, z-Vektor, der aus dem Ursprung in dem Zuschneidenden Bereich stammt. Dieser Vektor impliziert eine Ebene, die dem Vektor entspricht und den Ursprung durchläuft. Windows behält alle Pixel auf der Vektorseite der Ebene bei und klammern alle Pixel hinter der Ebene ab. Die vierte w-Komponente pusht die Ebene zurück und bewirkt, dass Windows weniger abschneiden (ein negatives w bewirkt, dass Windows mehr clipen) entlang der Vektorlinie. Wenn die x-, y- und z-Komponenten einen (normalisierten) Einheitenvektor bilden, pusht w die Ebene w Einheiten zurück.

Die Berechnung, die die Grafikverarbeitungseinheit (GRAPHICS Processing Unit, GPU) ausführt, um clipping zu bestimmen, ist ein einfaches Punktprodukt zwischen dem Scheitelpunktvektor (x, y, z, 1) und dem Clippingebenenvektor. Dieser mathematische Vorgang erstellt eine Projektionslänge auf dem Clipebenenvektor. Ein negatives Punktprodukt zeigt den Scheitelpunkt an, der sich auf der abgeschnittenen Seite der Ebene befinden soll.

### <a name="clipping-in-view-space"></a>Beschneiden im Ansichtsbereich

Hier sehen Sie unseren Scheitelpunkt im Ansichtsbereich:

![Scheitelpunkt im Ansichtsbereich](images/vertex-clip.png)

Hier sehen Sie unsere Clipebene im Ansichtsbereich:

![Clipebene im Ansichtsbereich](images/clip-plane-view.png)

Hier ist das Punktprodukt aus Scheitelpunkt und Clipebene im Ansichtsbereich:

ClipDistance = **v** · **C**  =  *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub>  +  *v*<sub>z</sub>*C*<sub>z</sub>  +  *C*<sub>w</sub>

Dieser mathematische Vorgang funktioniert für ein Direct3D 10- oder höher-Objekt, aber nicht für ein Direct3D 9-Objekt. Für Direct3D 9 müssen wir zunächst unsere Projektionstransformation in clip space durchlaufen.

### <a name="projection-matrix"></a>Projektionsmatrix

Eine Projektionsmatrix transformiert einen Scheitelpunkt aus dem Ansichtsbereich (wobei der Ursprung das Auge des Betrachters ist, +x rechts, +y nach oben und +z geradeaus). Die Projektionsmatrix liest den Scheitelpunkt für die Hardwareausschneidung und die [Rasterungsphase.](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage) Hier ist eine Standardperspektivenmatrix (andere Projektionen erfordern andere mathematische Berechnungen):

<dl> *r-Verhältnis*   von Fensterbreite/Höhe  
*α*   Anzeigewinkel  
*f*   Entfernung vom Viewer zur fernen Ebene  
*n*   Entfernung zwischen dem Viewer und der näheren Ebene
</dl>![Projektionsmatrix](images/projection-matrix.png)

Die nächste Matrix ist eine vereinfachte Version der vorherigen Matrix. Wir zeigen die Matrix vereinfacht an, damit wir sie später im Matrixmultiplikationsvorgang verwenden können.

![Vereinfachte Projektionsmatrix](images/projection-matrix2.png)

Nun transformieren wir den Vertex des Ansichtsbereichs in einen Clipspace mit einer Matrixmultiplikation:

![Matrixmultiplikation](images/matrix-multiply.png)

In unserem Matrixmultiplikationsvorgang werden unsere x- und y-Komponenten nur geringfügig angepasst, aber unsere z- und w-Komponenten sind recht verrissen. Unsere Clipebene gibt uns nicht mehr die gewünschten Informationen.

### <a name="clip-space-clip-plane"></a>Clip space clip plane (Clip space clip plane)

Hier möchten wir eine Clipspace-Clipebene erstellen, deren Punktprodukt mit unserem Clip space Vertex den gleichen Wert wie **v · C** im Abschnitt [Clipping in view space (Beschneiden im Anzeigebereich).](#clipping-in-view-space)

![Clipebene](images/clip-space-clip-plane.png)

**v** · **C**  =  **v P** · **C**<sub>P</sub>

*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub>  +  *v* z C <sub>z</sub><sub></sub>  +  *C*<sub>w</sub>  =  *v* ₓ *P* ₓ *C*<sub>Pₓ</sub>  + *v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>P <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*C* P <sub><sub>z</sub></sub>  +  *BC* P <sub><sub>z</sub></sub>  +  *v* z <sub>C</sub><sub>P <sub>w</sub></sub>

Nun können wir den vorherigen mathematischen Vorgang nach Scheitelpunktkomponente in vier separate Gleichungen untergliedern:

![x Scheitelpunktkomponente des Clipebenenprodukts](images/clip-space-clip-plane-equ1.png)

![y Scheitelpunktkomponente des Clipebenenprodukts](images/clip-space-clip-plane-equ2.png)

![w Scheitelpunktkomponente des Clipebenenprodukts](images/clip-space-clip-plane-equ3.png)

![z Scheitelpunktkomponente des Clipebenenprodukts](images/clip-space-clip-plane-equ4.png)

Die Clipebene des Ansichtsraums und unsere Projektionsmatrix leiten sich ab und geben uns die Clipspace-Clipebene.

![Clip space clip plane (Clip space clip plane)](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Syntax der Funktionsdeklaration](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 
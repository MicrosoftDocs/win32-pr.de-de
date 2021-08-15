---
description: Die Unterstützung für Punkt-Sprites in Direct3D 9 ermöglicht das Hochleistungsrendering von Punkten (Partikelsystemen). Punkt-Sprites sind Generalisierungen generischer Punkte, die das Rendern beliebiger Formen gemäß der Definition durch Texturen ermöglichen.
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: Punkt-Sprites (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90abd21207d9b3866ff93bd6c73069b655056f1c28811689762b0ce669183793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520468"
---
# <a name="point-sprites-direct3d-9"></a>Punkt-Sprites (Direct3D 9)

Die Unterstützung für Punkt-Sprites in Direct3D 9 ermöglicht das Hochleistungsrendering von Punkten (Partikelsystemen). Punkt-Sprites sind Generalisierungen generischer Punkte, die das Rendern beliebiger Formen gemäß der Definition durch Texturen ermöglichen.

-   [Point Primitive Rendering-Steuerelemente](#point-primitive-rendering-controls)
-   [Berechnungen der Punktgröße](#point-size-computations)
-   [Point Rendering](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Point Primitive Rendering-Steuerelemente

Direct3D 9 unterstützt zusätzliche Parameter, um das Rendering von Punkt-Sprites (Punktprimitiven) zu steuern. Mit diesen Parametern können Punkte eine variable Größe aufweisen und eine vollständige Texturzuordnung angewendet werden. Die Größe der einzelnen Punkte wird durch eine von der Anwendung angegebene Größe in Kombination mit einer von Direct3D berechneten entfernungsbasierten Funktion bestimmt. Die Anwendung kann die Punktgröße entweder pro Scheitelpunkt oder durch Festlegen von D3DRS POINTSIZE angeben, was für Punkte ohne Scheitelpunktgröße \_ gilt. Die Punktgröße wird in Kameraraumeinheiten ausgedrückt, mit Ausnahme, wenn die Anwendung nach transformierte Vertex-Scheitelpunkte (FVF) über gibt. In diesem Fall wird die entfernungsbasierte Funktion nicht angewendet, und die Punktgröße wird auf dem Renderziel in Pixeleinheiten ausgedrückt.

Die Texturkoordinaten, die beim Rendern von Punkten berechnet und verwendet werden, hängen von der Einstellung von D3DRS \_ POINTSPRITEENABLE ab. Wenn dieser Wert auf **TRUE festgelegt ist,** werden die Texturkoordinaten so festgelegt, dass jeder Punkt die vollständige Textur anzeigt. Im Allgemeinen ist dies nur nützlich, wenn Punkte deutlich größer als ein Pixel sind. Wenn D3DRS POINTSPRITEENABLE auf FALSE festgelegt ist, wird die Scheitelpunkttexturkoordinate jedes Punkts \_ für den gesamten Punkt verwendet. 

## <a name="point-size-computations"></a>Berechnungen der Punktgröße

Die Punktgröße wird durch D3DRS \_ POINTSCALEENABLE bestimmt. Wenn dieser Wert auf **FALSE** festgelegt ist, wird die von der Anwendung angegebene Punktgröße als Bildschirmbereichsgröße (nach dem Transformierten) verwendet. Für Scheitelräume, die im Bildschirmbereich an Direct3D übergeben werden, werden keine Punktgrößen berechnet. die angegebene Punktgröße wird als Bildschirmbereichsgröße interpretiert.

Wenn D3DRS \_ POINTSCALEENABLE **true ist,** berechnet Direct3D die Größe des Bildschirmbereichspunkts gemäß der folgenden Formel. Die von der Anwendung angegebene Punktgröße wird in Kameraraumeinheiten ausgedrückt.

S s = Vh \* S <sub>i</sub> \* sqrt(1/(A + B D ₑ + C ( D \* \* ₑ 2 )))

In dieser Formel ist die Größe des Eingabepunkts S <sub>i</sub>entweder pro Scheitelpunkt oder der Wert des D3DRS \_ POINTSIZE-Renderzustands. Die Punktskalafaktoren D3DRS \_ POINTSCALE \_ A, D3DRS POINTSCALE B und \_ \_ D3DRS \_ POINTSCALE C werden \_ durch die Punkte A, B und C dargestellt. Die Höhe des Viewports V h ist der Height-Member der [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) der den Viewport darstellt. D ₑ der Abstand vom Auge zur Position (das Auge am Ursprung) wird berechnet, indem die Position des Augenraums des Punkts (Xₑ, Yₑ, Zₑ) und der folgende Vorgang durchgeführt wird.

D ₑ = sqrt (Xₑ): + Y ₑ): + Z ₑ 2)

Die maximale Punktgröße ( Pmₐₓ) wird bestimmt, indem der kleinere der MaxPointSize-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) oder der D3DRS \_ POINTSIZE \_ MAX-Renderzustand verwendet wird. Die minimale Punktgröße P<sub>min</sub>wird durch Abfragen des Werts von D3DRS \_ POINTSIZE \_ MIN bestimmt. Daher wird die endgültige Bildschirmbereichspunktgröße S wie folgt bestimmt.

-   Wenn Ss > Pmₐₓ, dann S = P mₐₓ
-   Wenn S < P<sub>min,</sub>dann S = P <sub>min</sub>
-   Andernfalls S = S s

## <a name="point-rendering"></a>Point Rendering

Ein Bildschirmbereichspunkt( P = ( X, Y, Z, W) der Bildschirmbereichsgröße S wird als Viereck der folgenden vier Scheitelungen rastert.

(( X + S/2, Y + S/2, Z, W), ( X + S/2, Y - S/2, Z, W), ( X - S/2, Y- S/2, Z, W), ( X - S/2, Y + S/2, Z, W))

Die Scheitelpunktfarbattribute werden an jedem Scheitelpunkt dupliziert. daher wird jeder Punkt immer mit konstanten Farben gerendert.

Die Zuweisung von Texturindizes wird durch die D3DRS \_ POINTSPRITEENABLE-Renderzustandseinstellung gesteuert. Wenn D3DRS POINTSPRITEENABLE auf FALSE festgelegt ist, werden die Scheitelpunkttexturkoordinaten an \_ jedem Scheitelpunkt dupliziert.  Wenn D3DRS POINTSPRITEENABLE auf TRUE festgelegt ist, werden die Texturkoordinaten an den vier Scheitelpunkten auf \_ die folgenden Werte festgelegt. 

(0.F, 0.F), (0.F, 1.F), (1.F, 0.F), (1.F, 1.F)

Dies wird im folgenden Diagramm veranschaulicht:

![Diagramm eines Quadrats mit bezeichneten Scheitelwerten für (u,v) und (x,y) Koordinatenwerte](images/spritepoint.png)

Wenn die Beschneidung aktiviert ist, werden Punkte wie folgt abgeschnitten. Wenn der Scheitelpunkt den Bereich der Tiefenwerte (MinZ und MaxZ der [**D3DVIEWPORT9-Struktur)**](d3dviewport9.md) überschreitet, in den eine Szene gerendert werden soll, befindet sich der Punkt außerhalb des Ansichtsfrustums und wird nicht gerendert. Wenn sich der Punkt unter Berücksichtigung der Punktgröße vollständig außerhalb des Viewports in X und Y befindet, wird der Punkt nicht gerendert. Die verbleibenden Punkte werden gerendert. Es ist möglich, dass sich die Punktposition außerhalb des Viewports in X oder Y befindet und immer noch teilweise sichtbar ist.

Punkte werden möglicherweise ordnungsgemäß auf benutzerdefinierte Clipebenen abgeschnitten. Wenn D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS nicht im PrimitiveMiscCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) festgelegt ist, werden Punkte nur basierend auf der Scheitelpunktposition auf benutzerdefinierte Clipebenen abgeschnitten, und die Punktgröße wird ignoriert. In diesem Fall werden skalierte Punkte vollständig gerendert, wenn sich die Scheitelpunktposition innerhalb der Clipebenen befindet, und verworfen, wenn sich die Scheitelpunktposition außerhalb einer Clipebene befindet. Anwendungen können potenzielle Artefakte verhindern, indem sie eine Rahmengeometrie zu Clipebenen hinzufügen, die so groß wie die maximale Punktgröße ist.

Wenn das D3DPMISCCAPS CLIPPLANESCALEDPOINTS-Bit festgelegt ist, werden die skalierten Punkte ordnungsgemäß auf benutzerdefinierte \_ Clipebenen abgeschnitten.

Die Hardwarevertexverarbeitung unterstützt möglicherweise die Punktgröße. Wenn beispielsweise ein Gerät mit D3DCREATE HARDWARE VERTEXPROCESSING auf einem Hardwareabstraktionsschichtgerät (Hardware Abstraction Layer, D3DDEVTYPE MPI) erstellt wird, für das das \_ \_ \_ MaxPointSize-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) auf 1,0 oder 0,0 festgelegt ist, sind alle Punkte ein einzelnes Pixel. Um Pixelpunkt-Sprites kleiner als 1,0 zu rendern, müssen Sie entweder FVF-TL-Scheitelpunkte (transformiert und beleuchtet) oder Softwarevertex processing (D3DCREATE SOFTWARE VERTEXPROCESSING) verwenden. In diesem Fall \_ emuliert die Direct3D-Laufzeit das Punkt-Sprite-Rendering. \_

Ein Hardwaregerät, das Scheitelpunktverarbeitung übernimmt und Punkt-Sprites unterstützt – MaxPointSize auf größer als 1,0f festgelegt – ist erforderlich, um die Größenberechnung für nicht übersetzte Sprites durchzuführen, und ist erforderlich, um den Pro-Scheitelpunkt oder D3DRS \_ POINTSIZED3DRS POINTSIZE für TL-Scheitelpunkte ordnungsgemäß festlegen zu \_ können.

Informationen zu Renderingregeln für Punkte, Linien und Dreiecke finden Sie unter [Rasterregeln (Direct3D 9).](rasterization-rules.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexpipeline](vertex-pipeline.md)
</dt> </dl>

 

 




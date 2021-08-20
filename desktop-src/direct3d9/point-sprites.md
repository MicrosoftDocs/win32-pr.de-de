---
description: Die Unterstützung für Punkt-Sprites in Direct3D 9 ermöglicht das leistungsstarke Rendern von Punkten (Partikelsystemen). Punkt-Sprites sind Verallgemeinerungen generischer Punkte, mit denen beliebige Formen wie durch Texturen definiert gerendert werden können.
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

Die Unterstützung für Punkt-Sprites in Direct3D 9 ermöglicht das leistungsstarke Rendern von Punkten (Partikelsystemen). Punkt-Sprites sind Verallgemeinerungen generischer Punkte, mit denen beliebige Formen wie durch Texturen definiert gerendert werden können.

-   [Point Primitive Rendering-Steuerelemente](#point-primitive-rendering-controls)
-   [Berechnungen der Punktgröße](#point-size-computations)
-   [Punktrendering](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Point Primitive Rendering-Steuerelemente

Direct3D 9 unterstützt zusätzliche Parameter, um das Rendering von Punkt-Sprites (Punktprimitiven) zu steuern. Mit diesen Parametern können Punkte variabler Größe aufweisen und eine vollständige Texturzuordnung angewendet werden. Die Größe jedes Punkts wird durch eine von der Anwendung angegebene Größe in Kombination mit einer entfernungsbasierten Funktion bestimmt, die von Direct3D berechnet wird. Die Anwendung kann die Punktgröße entweder pro Scheitelpunkt oder durch Festlegen von D3DRS \_ POINTSIZE angeben, was für Punkte ohne Scheitelpunktgröße gilt. Die Punktgröße wird in Kameraraumeinheiten ausgedrückt, mit Ausnahme von , wenn die Anwendung nachtransformationsbasierte FVF-Scheitelpunkte (Flexible Vertex Format) übergibt. In diesem Fall wird die entfernungsbasierte Funktion nicht angewendet, und die Punktgröße wird in Pixeleinheiten auf dem Renderziel ausgedrückt.

Die Texturkoordinaten, die beim Rendern von Punkten berechnet und verwendet werden, hängen von der Einstellung von D3DRS \_ POINTSPRITEENABLE ab. Wenn dieser Wert auf **TRUE** festgelegt ist, werden die Texturkoordinaten so festgelegt, dass jeder Punkt die vollständige Textur anzeigt. Im Allgemeinen ist dies nur nützlich, wenn Punkte deutlich größer als ein Pixel sind. Wenn D3DRS \_ POINTSPRITEENABLE auf **FALSE** festgelegt ist, wird die Scheitelpunkttexturkoordinate jedes Punkts für den gesamten Punkt verwendet.

## <a name="point-size-computations"></a>Berechnungen der Punktgröße

Die Punktgröße wird durch D3DRS \_ POINTSCALEENABLE bestimmt. Wenn dieser Wert auf **FALSE** festgelegt ist, wird die von der Anwendung angegebene Punktgröße als Bildschirmbereichsgröße (nachtransformation) verwendet. Für Scheitelpunkte, die im Bildschirmbereich an Direct3D übergeben werden, werden keine Punktgrößen berechnet. die angegebene Punktgröße wird als Bildschirmbereichsgröße interpretiert.

Wenn D3DRS \_ POINTSCALEENABLE **TRUE** ist, berechnet Direct3D die Größe des Bildschirmbereichspunkts gemäß der folgenden Formel. Die von der Anwendung angegebene Punktgröße wird in Kameraraumeinheiten ausgedrückt.

S s = Vh \* S <sub>i</sub> \* sqrt(1/(A + B D ₑ + C ( D \* \* ₑ sstelle )))

In dieser Formel ist die Eingabepunktgröße S <sub>i</sub>entweder pro Scheitelpunkt oder der Wert des D3DRS \_ POINTSIZE-Renderzustands. Die Punktskalierungsfaktoren D3DRS \_ POINTSCALE \_ A, D3DRS \_ POINTSCALE \_ B und D3DRS \_ POINTSCALE C werden durch die Punkte \_ A, B und C dargestellt. Die Höhe des Viewports , V h, ist das Height-Element der [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) das den Viewport darstellt. D ₑ, der Abstand zwischen dem Auge und der Position (dem Auge am Ursprung), wird berechnet, indem die Augenposition des Punkts (Xₑ, Yₑ, Zₑ) und die folgende Operation ausgeführt wird.

D ₑ = sqrt (Xₑ² + Y ₑ sstelle + Z ₑ sstelle)

Die maximale Punktgröße Pmₐₓ wird bestimmt, indem entweder der kleinere des MaxPointSize-Elements der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) oder der D3DRS \_ POINTSIZE \_ MAX-Renderzustand angenommen wird. Die Minimale Punktgröße P<sub>min</sub>wird durch Abfragen des Werts von D3DRS \_ POINTSIZE \_ MIN bestimmt. Daher wird die endgültige Größe des Bildschirmbereichspunkts , S, wie folgt bestimmt.

-   Wenn Ss > Pmₐₓ, dann S = P mₐₓ
-   , wenn S < P<sub>min,</sub>dann S = P <sub>min</sub>
-   Andernfalls S = S s

## <a name="point-rendering"></a>Punktrendering

Ein Bildschirmbereichspunkt P = ( X, Y, Z, W) der Bildschirmbereichsgröße S wird als Quaderatral der folgenden vier Scheitelpunkte gerastt.

(( X + S/2, Y + S/2, Z, W), ( X + S/2, Y - S/2, Z, W), ( X - S/2, Y- S/2, Z, W), ( X - S/2, Y + S/2, Z, W))

Die Vertexfarbattribute werden an jedem Scheitelpunkt dupliziert. daher wird jeder Punkt immer mit konstanten Farben gerendert.

Die Zuweisung von Texturindizes wird durch die D3DRS \_ POINTSPRITEENABLE-Renderzustandseinstellung gesteuert. Wenn D3DRS \_ POINTSPRITEENABLE auf **FALSE** festgelegt ist, werden die Scheitelpunkttexturkoordinaten an jedem Scheitelpunkt dupliziert. Wenn D3DRS \_ POINTSPRITEENABLE auf **TRUE** festgelegt ist, werden die Texturkoordinaten an den vier Scheitelpunkten auf die folgenden Werte festgelegt.

(0.F, 0.F), (0.F, 1.F), (1.F, 0.F), (1.F, 1.F)

Dies wird im folgenden Diagramm veranschaulicht:

![Diagramm eines Quadrats mit bezeichneten Scheitelpunkten für (u,v) und (x,y) Koordinatenwerte](images/spritepoint.png)

Wenn clipping aktiviert ist, werden Punkte wie folgt abgeschnitten. Wenn der Scheitelpunkt den Bereich der Tiefenwerte (MinZ und MaxZ der [**D3DVIEWPORT9-Struktur)**](d3dviewport9.md) überschreitet, in den eine Szene gerendert werden soll, befindet sich der Punkt außerhalb des Ansichts frustums und wird nicht gerendert. Wenn sich der Punkt unter Berücksichtigung der Punktgröße vollständig außerhalb des Viewports in X und Y befindet, wird der Punkt nicht gerendert. die verbleibenden Punkte werden gerendert. Es ist möglich, dass sich die Punktposition außerhalb des Viewports in X oder Y befindet und weiterhin teilweise sichtbar ist.

Punkte können auf benutzerdefinierten Clipebenen ordnungsgemäß abgeschnitten werden. Wenn D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS nicht im PrimitiveMiscCaps-Element der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) festgelegt ist, werden Punkte basierend auf der Scheitelpunktposition auf benutzerdefinierte Clipebenen abgeschnitten, wobei die Punktgröße ignoriert wird. In diesem Fall werden skalierte Punkte vollständig gerendert, wenn sich die Scheitelpunktposition innerhalb der Clipebenen befindet, und verworfen, wenn sich die Scheitelpunktposition außerhalb einer Clipebene befindet. Anwendungen können potenzielle Artefakte verhindern, indem sie Clipebenen eine Rahmengeometrie hinzufügen, die so groß wie die maximale Punktgröße ist.

Wenn das Bit D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS festgelegt ist, werden die skalierten Punkte ordnungsgemäß auf benutzerdefinierte Clipebenen abgeschnitten.

Die Hardwarevertexverarbeitung unterstützt möglicherweise die Punktgröße. Wenn beispielsweise ein Gerät mit D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING auf einem Hardwareabstraktionsschichtgerät (D3DDEVTYPE INVALID) erstellt wird, für \_ das der MaxPointSize-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) auf 1,0 oder 0,0 festgelegt ist, sind alle Punkte ein einzelnes Pixel. Um Pixelpunkt-Sprites kleiner als 1,0 zu rendern, müssen Sie entweder FVF-TL-Scheitelpunkte (transformiert und beleuchtet) oder Softwarevertexverarbeitung (D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING) verwenden. In diesem Fall emuliert die Direct3D-Laufzeit das Punkt-Sprite-Rendering.

Ein Hardwaregerät, das die Scheitelpunktverarbeitung durchführt und Punkt-Sprites unterstützt – MaxPointSize ist auf größer als 1,0f festgelegt – ist erforderlich, um die Größenberechnung für nicht transformierte Sprites durchzuführen, und ist erforderlich, um den pro Scheitelpunkt oder D3DRS \_ POINTSIZED3DRS \_ POINTSIZE für TL-Scheitelpunkte ordnungsgemäß festzulegen.

Informationen zu Renderingregeln für Punkte, Linien und Dreiecke finden Sie unter [Rasterungsregeln (Direct3D 9).](rasterization-rules.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexpipeline](vertex-pipeline.md)
</dt> </dl>

 

 




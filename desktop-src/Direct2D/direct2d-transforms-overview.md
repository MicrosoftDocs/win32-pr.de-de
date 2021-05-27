---
title: Übersicht über Transformationen
description: Stellt die Microsoft Direct2D-Transformations-API für Windows 7 vor. Direct2D ermöglicht Win32-Entwicklern das Ausführen von 2D-Grafiktransformationen.
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Direct2D, Übersicht über Transformationen
- Direct2D, Koordinatensysteme
- Direct2D, Renderziele
- Direct2D-, 2D-Transformationen
- 2D-Transformationen
- Transformationen, Informationen
- Transformationen, Renderziele
- Transformationen, Objekte
- Renderziele,Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b924c51d73e71f206fbb250f4a7dd50ca71db2a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549145"
---
# <a name="transforms-overview"></a>Übersicht über Transformationen

Dieses Thema erläutert die Grundlagen von Direct2D-Transformationen und enthält Beispiele für verschiedene Transformationen. Sie enthält die folgenden Teile:

-   [Was ist eine Direct2D-Transformation?](#what-is-a-direct2d-transform)
-   [Der Direct2D-Koordinatenraum](#the-direct2d-coordinate-space)
-   [Erstellen von Transformationsmatrizen](#creating-transformation-matrices)
-   [Renderingzieltransformationen](#rendering-target-transforms)
-   [Pinseltransformationen](#brush-transforms)
-   [Geometrietransformationen](#geometry-transforms)
-   [Auswirkungen einer Renderzieltransformation auf Clips](#how-a-render-target-transform-affects-clips)
-   [Zusammenfassung](#summary)
-   [Verwandte Themen](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>Was ist eine Direct2D-Transformation?

Eine Transformation gibt an, wie die Punkte eines Objekts von einem Koordinatenraum zu einem anderen oder von einer Position zu einer anderen innerhalb desselben Koordinatenraums zugeordnet werden. Diese Zuordnung wird durch eine Transformationsmatrix beschrieben, die als Auflistung von drei Zeilen mit drei Spalten mit FLOAT-Werten definiert ist, wie in der folgenden Tabelle dargestellt.



|    &nbsp;       |       &nbsp;    |  &nbsp; |
|-----------------|-----------------|-----|
| M11Standard: 1.0 | M12Standard: 0.0 | 0,0 |
| M21Standard: 0,0 | M22Standard: 1.0 | 0,0 |
| M31OffsetX: 0.0 | M32OffsetY: 0,0 | 1.0 |



 

In dieser Matrix definieren die Elemente M11, M12, M21 und M22 eine lineare Transformation, die ein Objekt skalieren, drehen oder verzerren kann. die OffsetX- und OffsetY-Elemente definieren die Übersetzung, die nach der linearen Transformation angewendet werden soll. Bei affinen Transformationen sind die Werte in der dritten Spalte immer 0,0, 0,0 und 1,0.

Da Direct2D nur affine (lineare) Transformationen unterstützt, wird seine Transformationsmatrix als 3:2-Matrix definiert, ohne dass die dritte Spalte aus der vorherigen Transformationsmatrix stammt. Die folgende Tabelle zeigt das Layout der Direct2D-Transformationsmatrix.



|    &nbsp;       |       &nbsp;    | 
|-----------------|-----------------|
| M11Standard: 1.0 | M12Standard: 0.0 |
| M21Standard: 0.0 | M22Standard: 1.0 |
| M31OffsetX: 0.0 | M32OffsetY: 0,0 |



 

In Direct2D wird diese 3:2-Matrix durch die [**D2D1 \_ MATRIX \_ 3X2-Struktur**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) dargestellt. Um allgemeine Matrixvorgänge zu vereinfachen, stellt Direct2D auch eine Klasse namens [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)zur Folge, die von der **D2D1 \_ MATRIX \_ 3X2-Struktur abgeleitet** wird.

Der Standardkonstruktor [**für Matrix3x2F lässt**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) das Objekt nicht initialisiert. Um eine Identitätsmatrix abzurufen, verwenden Sie [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix).

Wenn eine Identitätstransformation auf ein Objekt angewendet wird, ändert sie weder die Position noch die Form oder Größe des Objekts. Dies ähnelt der Art und Weise, wie die Multiplikation einer Zahl mit 1 die Zahl nicht ändert. Anders ausgedrückt: Die Identitätstransformation belässt die Koordinaten von Punkten allein und verschiebt die Punkte nicht an eine neue Position. Jede andere Transformation als die Identitätstransformation ändert die Position, Form und/oder Größe von Objekten.

Bei Transformationen geht es um Koordinaten, und das Verständnis des Direct2D-Koordinatenraums ist wichtig, um die Verwendung von Transformationen zu verstehen.

## <a name="the-direct2d-coordinate-space"></a>Der Direct2D-Koordinatenraum

Direct2D verwendet einen linkshändigen Koordinatenraum. Das bedeutet, dass positive Werte der X-Achse nach rechts und positive Werte der y-Achse nach unten zunehmen. Alles auf dem Bildschirm ist relativ zum Ursprung positioniert. Dies ist der Punkt, an dem sich die x-Achse und die y-Achse überschneiden (0, 0), wie in der folgenden Abbildung dargestellt. Direct2D-Renderziele verwenden diesen Koordinatenraum.

![Abbildung der X- und y-Achse eines linkshändigen Koordinatenraums](images/coordinatespace.png)

Indem Sie Werte in einer Transformationsmatrix bearbeiten, können Sie ein Objekt drehen, skalieren, verschiegen und verschieben (übersetzen). Wenn Sie beispielsweise OffsetX auf 100 und OffsetY auf 200 festlegen, verschieben Sie das Objekt um 100 Pixel nach rechts und 200 Pixel nach unten.

Um den Effekt der Objekt verschieben zu zeigen, müssen Sie die Übersetzungstransformation anwenden, um Ziele, Pinsel oder Geometrien zu rendern. Das Anwenden einer Transformation zum Rendern von Zielen wirkt sich auf den gesamten Bildschirm aus, während das Anwenden einer Transformation auf einen Pinsel oder eine Geometrie nur diesen bestimmten Pinsel oder diese Geometrie betrifft. Verwenden Sie zum Erstellen einer Transformationsmatrix die [**Matrix3x2F-Klasse.**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f)

## <a name="creating-transformation-matrices"></a>Erstellen von Transformationsmatrizen

Zum Erstellen von Transformationen für Drehung, Skalierung, Schiefe und Übersetzung stellt die [**Matrix3x2F-Klasse**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) die in der folgenden Tabelle gezeigten statischen Methoden bereit. Die Spalte Beispiel der Tabelle enthält Links zu den Themen zur Vorgehensweise, die veranschaulichen, wie die einzelnen Transformationsmethoden verwendet werden.



| Methode                                                                   | Beschreibung                                                                                                     | Beispiel                                            | Abbildung                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f::rotate**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | erstellt eine Drehungstransformation mit dem angegebenen Winkel und Mittelpunkt.                                | [Drehen eines Objekts](how-to-rotate.md)       | ![Abbildung eines Quadrats, das um 45 Grad im Uhrzeigersinn um die Mitte des ursprünglichen Quadrats gedreht wird](images/rotate-ovw.png)                 |
| [**matrix3x2f::scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | erstellt eine Skalierungstransformation, die über die angegebenen Skalierungsfaktoren und den Mittelpunkt verfügt.                           | [Skalieren eines Objekts](how-to-scale.md)         | ![Abbildung eines quadratisch skalierten 130 %](images/scale-ovw.png)                                                                           |
| [**matrix3x2f::skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | erstellt eine Schiefetransformation, die die angegebenen Werte für x-Achse und y-Achse sowie den Mittelpunkt enthält.                 | [Verzerren eines Objekts](how-to-skew.md)           | ![Abbildung einer quadratischen Schiefe um 30 Grad gegen den Uhrzeigersinn von der y-Achse](images/skew-ovw.png)                                     |
| [**matrix3x2f::translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | erstellt eine Übersetzungstransformation und gibt die Verschiebungen in Richtung der x-Achse und der y-Achse an. | [Übersetzen eines Objekts](how-to-translate.md) | ![Abbildung eines Quadrats, das 20 Einheiten entlang der positiven X-Achse und 10 Einheiten entlang der positiven Y-Achse verschoben wurde](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>Renderingzieltransformationen

Ein Renderziel ist eine Ressource, die von der [**ID2D1RenderTarget-Schnittstelle erbt.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Er erstellt Ressourcen zum Zeichnen und führt tatsächliche Zeichnungsvorgänge aus. Außerdem werden Methoden zum Transformieren des Koordinatenraums zur Verfügung stehen. Sie können die [**ID2D1RenderTarget::SetTransform-Methode**](id2d1rendertarget-settransform.md) aufrufen, um die angegebene Transformation auf das Renderziel anzuwenden. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.

Verwenden Sie zum Rendern von Inhalten die Zeichnungsmethoden des Renderziels. Bevor Sie mit dem Zeichnen beginnen, rufen Sie die [**BeginDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) auf. Um das Rendern von Inhalten fertig zu stellen, rufen Sie [**die EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) auf. Ein Beispiel finden Sie unter [Anwenden mehrerer Transformationen auf ein Objekt.](how-to-apply-multiple-transforms.md)

## <a name="brush-transforms"></a>Pinseltransformationen

Sie können die Transformation auf dem Pinsel anpassen, indem Sie [**SetTransform aufrufen.**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) Für diese Transformation können Sie sich den Pinsel als großes Papierstück und die verschiedenen Renderingprimitiven (Text, Geometrie, Rechteck und so weiter) als Schablonen überlegen. Wenn Sie die Pinseltransformation anpassen, ist dies so, als würden Sie das große Papier unter die Schablone gleiten, ohne die Position der Schablone selbst zu ändern. Sie können diese Technik verwenden, damit der Text von Gelb zu Schwarz im 3D-Raum verblasst.

Wenn die Pinseltransformation die Identitätstransformation ist, werden Pinsel im gleichen Koordinatenbereich wie das Renderziel angezeigt, in dem sie gezeichnet werden. Mit der Pinseltransformation kann ein Aufrufer ändern, wie Pinselkoordinaten diesem Raum zuordnen.

Der Pinselbereich wird in Direct2D anders angegeben als in Windows Presentation Foundation (WPF). In Direct2D ist der Pinselbereich nicht relativ zum gezeichneten Objekt, sondern das aktuelle Koordinatensystem des Renderziels, das von der Pinseltransformation transformiert wird, sofern es eines gibt. Damit der Pinsel ein Objekt wie in WPF ausfüllt, müssen Sie den Ursprung des Pinselbereichs in die obere linke Ecke des umgebenden Felds des Objekts übersetzen und dann den Pinselbereich skalieren, sodass die Basiskachel den Begrenzungsbereich des Objekts füllt.

Weitere Informationen zu Pinseltransformationen finden Sie unter [Übersicht über Direct2D-Pinsel.](direct2d-brushes-overview.md)

## <a name="geometry-transforms"></a>Geometrietransformationen

Wenn Sie Geometrien skalieren, verschieben, übersetzen oder verzerren, können Sie eine Transformation direkt auf eine bestimmte Geometrie anwenden, nicht auf eine Renderzieltransformation, die sich auf den gesamten Bildschirm auswirken würde. Eine Renderzieltransformation wirkt sich im Allgemeinen auf den Strich und die Füllung einer Geometrie aus. Im Gegensatz dazu wirkt sich eine Geometrietransformation nur auf die Füllung einer Geometrie aus, da die Transformation auf eine Geometrie angewendet wird, bevor sie strichen wird.

> [!Note]  
> Ab Windows 8 wirkt sich die Welttransformation nicht auf den Strich aus, wenn Sie den Strichtyp auf [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) oder [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)festlegen.

 

Sie können die Transformation für eine Geometrie anpassen, indem Sie [**ID2D1Factory::CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) aufrufen, um ein [**ID2D1TransformedGeometry-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) zu erstellen. Weitere Informationen zu Geometrietransformationen finden Sie unter [Übersicht über Direct2D-Geometrien.](direct2d-geometries-overview.md)

## <a name="how-a-render-target-transform-affects-clips"></a>Auswirkungen einer Renderzieltransformation auf Clips

Die Transformation auf einem Renderziel wirkt sich darauf aus, wie der Begrenzungsfeld eines an der Achse ausgerichteten Clips berechnet wird. Wenn [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) aufgerufen wird, wird der *clipRect-Parameter* durch die aktuelle Welttransformation transformiert, die auf dem Renderziel festgelegt ist. Nachdem die Transformation auf *clipRect* angewendet wurde, wird das an der Achse ausgerichtete Begrenzungsfeld für *clipRect* berechnet. Aus Effizienzgründen werden die Inhalte auf dieses an der Achse ausgerichtete Begrenzungsfeld und nicht auf den ursprünglichen *clipRect* abgeschnitten, der übergeben wird. Die folgenden Diagramme zeigen, wie eine Drehungstransformation auf das Renderziel, den resultierenden *clipRect* und ein berechnetes an der Achse ausgerichtetes umgebendes Feld angewendet wird.

1.  Angenommen, das Rechteck in der folgenden Abbildung ist ein Renderziel, das an den Bildschirmpixeln ausgerichtet ist.

    ![Abbildung eines Rechtecks (Renderziel)](images/pushaxisalignedclip-step1-rendertarget.png)

2.  Wenden Sie eine Drehungstransformation auf das Renderziel an. In der folgenden Abbildung stellt das schwarze Rechteck das ursprüngliche Renderziel und das rot gestrichelte Rechteck das transformierte Renderziel dar.

    ![Abbildung des ursprünglichen Rechtecks und eines gedrehten Rechtecks (transformiertes Renderziel)](images/pushaxisalignedclip-step2-transformed.png)

3.  Nachdem [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) aufgerufen wurde, wird die Drehungstransformation auf *clipRect angewendet.* In der folgenden Abbildung stellt das blaue Rechteck den transformierten *clipRect dar.*

    ![Abbildung eines kleineren blauen Rechtecks (Cliprect) innerhalb des gedrehten Rechtecks (transformiertes Renderziel)](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  Das an der Achse ausgerichtete Begrenzungsfeld wird berechnet. In der folgenden Abbildung stellt das grüne gestrichelte Rechteck den Begrenzungsfeld dar. Alle Inhalte werden an diesem an der Achse ausgerichteten Begrenzungsfeld abgeschnitten.

    ![Abbildung eines grünen Begrenzungsfelds auf dem kleinen blauen Rechteck (Cliprect)](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>Zusammenfassung

Direct2D erleichtert das Transformieren von zweidimensionalen Objekten mit vereinfachten Koordinatenräumen und verwandten Klassen. Mithilfe verschiedener Arten von Transformationen können Sie Ihre Objekte übersetzen, drehen, verskalieren und skalieren, um viele beeindruckende visuelle Effekte zu erzielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 
---
title: Übersicht über Transformationen
description: Führt die Microsoft Direct2D Transform API für Windows 7 ein. Direct2D ermöglicht Win32-Entwicklern das Ausführen von 2D-Grafik Transformationen.
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Direct2D, Übersicht über Transformationen
- Direct2D, Koordinatensysteme
- Direct2D, Renderziele
- Direct2D, 2D-Transformationen
- 2D-Transformationen
- Transformationen, Informationen zu
- Transformationen, Renderziele
- Transformationen, Objekte
- Renderziele, Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f3678f7b194f0f0188ed907a63737a97e9e58c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948788"
---
# <a name="transforms-overview"></a>Übersicht über Transformationen

In diesem Thema werden die Grundlagen von Direct2D-Transformationen erläutert, und es werden Beispiele für verschiedene Transformationen erläutert. Sie enthält die folgenden Teile:

-   [Was ist eine Direct2D-Transformation?](#what-is-a-direct2d-transform)
-   [Der Direct2D-Koordinaten Bereich](#the-direct2d-coordinate-space)
-   [Erstellen von Transformations Matrizen](#creating-transformation-matrices)
-   [Rendern von Ziel Transformationen](#rendering-target-transforms)
-   [Pinsel Transformationen](#brush-transforms)
-   [Geometrie Transformationen](#geometry-transforms)
-   [Auswirkungen einer renderzieltransformation auf Clips](#how-a-render-target-transform-affects-clips)
-   [Zusammenfassung](#summary)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-a-direct2d-transform"></a>Was ist eine Direct2D-Transformation?

Eine Transformation gibt an, wie die Punkte eines Objekts von einem Koordinaten Bereich zu einem anderen oder von einer Position zu einer anderen innerhalb desselben Koordinaten Raums zugeordnet werden. Diese Zuordnung wird durch eine Transformationsmatrix beschrieben, die als Auflistung von drei Zeilen mit drei Spalten von Gleit Komma Werten definiert ist, wie in der folgenden Tabelle dargestellt.



|                 |                 |     |
|-----------------|-----------------|-----|
| M11Default: 1,0 | M12Default: 0,0 | 0,0 |
| M21Default: 0,0 | M22Default: 1,0 | 0,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 | 1.0 |



 

In dieser Matrix definieren die Mitglieder von M11, M12, M21 und M22 eine lineare Transformation, mit der ein Objekt skaliert, gedreht oder verzerrt werden kann. Die OffsetX-und OffsetY-Member definieren die Übersetzung, die angewendet werden soll, nachdem die lineare Transformation durchgeführt wurde. Bei affinen Transformationen lauten die Werte in der dritten Spalte immer 0,0, 0,0 und 1,0.

Da Direct2D nur affine (lineare) Transformationen unterstützt, wird die Transformationsmatrix als 3-x-2-Matrix definiert, wobei die dritte Spalte aus der vorherigen Transformationsmatrix weggelassen wird. In der folgenden Tabelle wird das Layout der Direct2D-Transformationsmatrix gezeigt.



|                 |                 |
|-----------------|-----------------|
| M11Default: 1,0 | M12Default: 0,0 |
| M21Default: 0,0 | M22Default: 1,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 |



 

In Direct2D wird diese 3-by-2-Matrix durch die [**D2D1 \_ Matrix \_ 3x2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) -Struktur dargestellt. Zum vereinfachen allgemeiner Matrix Vorgänge bietet Direct2D auch eine Klasse mit dem Namen [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f), die von der **D2D1 \_ Matrix \_ 3x2-** Struktur abgeleitet ist.

Der Standardkonstruktor für [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) lässt das Objekt nicht initialisieren. Verwenden Sie [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix), um eine Identitätsmatrix abzurufen.

Wenn eine Identitäts Transformation auf ein Objekt angewendet wird, ändert Sie nicht die Position, Form oder Größe des Objekts. Es ähnelt der Art und Weise, wie die Multiplikation einer Zahl mit 1 die Zahl nicht ändert. Mit anderen Worten: die Identitäts Transformation verlässt die Koordinaten der Punkte allein und verschiebt die Punkte nicht an eine neue Position. Durch eine andere Transformation als die Identitäts Transformation werden die Position, die Form und/oder die Größe von Objekten geändert.

Bei Transformationen geht es um Koordinaten, und das Verständnis des Direct2D-Koordinaten Raums ist wichtig, um die Verwendung von Transformationen zu verstehen.

## <a name="the-direct2d-coordinate-space"></a>Der Direct2D-Koordinaten Bereich

Direct2D verwendet einen links gerichteten Koordinatenraum. Das heißt, die positiven Werte der x-Achse erhöhen die Rechte und die positiven Werte der y-Achse nach unten. Alles auf dem Bildschirm wird relativ zum Ursprung positioniert. Dies ist der Punkt, an dem sich die x-Achse und die y-Achse überschneiden (0,0), wie in der folgenden Abbildung dargestellt. Direct2D Renderziele verwenden diesen Koordinaten Bereich.

![Darstellung der x-Achse und der y-Achse eines Links gerichteten Koordinaten Raums](images/coordinatespace.png)

Durch die Bearbeitung von Werten in einer Transformationsmatrix können Sie ein Objekt drehen, skalieren, neigen und verschieben (übersetzen). Wenn Sie z. b. OffsetX auf 100 und OffsetY auf 200 festlegen, verschieben Sie das Objekt nach rechts um 100 Pixel und nach unten 200 Pixel.

Um die Auswirkung der Objekt Verschiebung anzuzeigen, müssen Sie die Konvertierungs Transformation anwenden, um Ziele, Pinsel oder Geometrien zu Renderen. Das Anwenden einer Transformation auf Renderziele wirkt sich auf den gesamten Bildschirm aus, während das Anwenden einer Transformation auf einen Pinsel oder eine Geometrie nur auf diesen speziellen Pinsel oder diese Geometrie wirkt. Um eine Transformationsmatrix zu erstellen, verwenden Sie die [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse.

## <a name="creating-transformation-matrices"></a>Erstellen von Transformations Matrizen

Zum Erstellen von Drehung, Skalierung, Schiefe und Konvertierungs Transformationen bietet die [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse die statischen Methoden, die in der folgenden Tabelle aufgeführt sind. Die Beispiel Spalte der Tabelle enthält Links zu den Gewusst-wie-Themen, die veranschaulichen, wie die einzelnen Transformationsmethoden verwendet werden.



| Methode                                                                   | BESCHREIBUNG                                                                                                     | Beispiel                                            | Abbildung                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**matrix3x2f:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | erstellt eine Dreh Transformation, die über den angegebenen Winkel und Mittelpunkt verfügt.                                | [Drehen eines Objekts](how-to-rotate.md)       | ![Abbildung eines Quadrats, das um 45 Grad im Uhrzeigersinn um den Mittelpunkt des ursprünglichen Quadrats gedreht wurde](images/rotate-ovw.png)                 |
| [**matrix3x2f:: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)) | erstellt eine Skalierungs Transformation, die über die angegebenen Skalierungsfaktoren und den angegebenen Mittelpunkt verfügt.                           | [Skalieren eines Objekts](how-to-scale.md)         | ![Abbildung eines quadratischen skalierten 130%](images/scale-ovw.png)                                                                           |
| [**matrix3x2f:: schiefe**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | erstellt eine schiefe Transformation, die die angegebenen Werte für die x-Achse und die y-Achse sowie den Mittelpunkt aufweist.                 | [Vorgehensweise beim Verzerren eines Objekts](how-to-skew.md)           | ![Abbildung einer quadratischen Verzerrung von 30 Grad gegen den Uhrzeigersinn von der y-Achse](images/skew-ovw.png)                                     |
| [**matrix3x2f:: Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))                | erstellt eine Übersetzungs Transformation und gibt die Verschiebungen in Richtung der x-und y-Achse an. | [Übersetzen eines Objekts](how-to-translate.md) | ![Abbildung eines quadratischen verschoder 20 Einheiten entlang der positiven x-Achse und 10 Einheiten entlang der positiven y-Achse](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a>Rendern von Ziel Transformationen

Ein Renderziel ist eine Ressource, die von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle erbt. Er erstellt Ressourcen zum Zeichnen und ausführen tatsächlicher Zeichnungsvorgänge. Außerdem werden Methoden zum Transformieren des Koordinaten Raums bereitstellt. Sie können die [**ID2D1RenderTarget:: setTransform**](id2d1rendertarget-settransform.md) -Methode aufrufen, um die angegebene Transformation auf das Renderziel anzuwenden. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.

Verwenden Sie zum Renderinginhalt die Zeichnungs Methoden des Renderziels. Bevor Sie mit dem Zeichnen beginnen, müssen Sie die [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufrufen. Um das Rendern von Inhalt abzuschließen, aufrufen Sie die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode. Ein Beispiel finden Sie unter [Anwenden mehrerer Transformationen auf ein Objekt](how-to-apply-multiple-transforms.md).

## <a name="brush-transforms"></a>Pinsel Transformationen

Sie können die Transformation für den Pinsel anpassen, indem Sie [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))aufrufen. Für diese Transformation können Sie sich den Pinsel als großes Papier und unterschiedlichen renderprimitiver (Text, Geometrie, Rechteck usw.) als Schablonen vorstellen. Wenn Sie die Pinsel Transformation anpassen, ist es so, als würden Sie den großen Teil des Papiers unterhalb der Schablone verschieben, ohne die Position der Schablone selbst zu ändern. Mit dieser Technik können Sie den Text von Gelb in schwarz in den 3D-Raum ausblenden.

Wenn die Pinsel Transformation die Identitäts Transformation ist, werden Pinsel im gleichen Koordinaten Bereich wie das Renderziel angezeigt, in dem Sie gezeichnet werden. Mithilfe der Pinsel Transformation kann ein Aufrufer ändern, wie Pinsel Koordinaten diesem Bereich zugeordnet werden.

Der Pinselbereich wird in Direct2D anders angegeben als in Windows Presentation Foundation (WPF). In Direct2D ist der Pinselbereich nicht relativ zu dem Objekt, das gezeichnet wird, sondern ist stattdessen das aktuelle Koordinatensystem des Renderziels, das von der Pinsel Transformation transformiert wird (sofern vorhanden). Damit der Pinsel ein Objekt wie in WPF erstellt, müssen Sie den Pinsel Raum Ursprung in die linke obere Ecke des umgebenden Felds des Objekts übersetzen und dann den Pinselbereich skalieren, sodass die Basis Kachel das umgebende Feld des Objekts füllt.

Weitere Informationen zu Pinsel Transformationen finden Sie unter [Übersicht über Direct2D-Pinsel](direct2d-brushes-overview.md).

## <a name="geometry-transforms"></a>Geometrie Transformationen

Beim Skalieren, verschieben, übersetzen oder neigen von Geometrien können Sie eine Transformation direkt auf eine bestimmte Geometrie anwenden, nicht auf eine renderzieltransformation, die sich auf den gesamten Bildschirm auswirken würde. Eine renderzieltransformation wirkt sich in der Regel auf den Strich und die Füllung einer Geometrie aus. Im Gegensatz dazu wirkt sich eine Geometrie Transformation nur auf das Ausfüllen einer Geometrie aus, da die Transformation auf eine Geometrie angewendet wird, bevor Sie gestreichelt wird.

> [!Note]  
> Ab Windows 8 wirkt sich die Welt Transformation nicht auf den Strich aus, wenn Sie den Stroke-Typ auf [**D2D1 \_ Stroke \_ Transform \_ Type \_ Fixed**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) oder [**D2D1 \_ Stroke \_ Transform \_ Type \_ Hairline**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)festgelegt haben.

 

Sie können die Transformation für eine Geometrie anpassen, indem Sie [**ID2D1Factory:: createtransformedgeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) aufrufen, um ein [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) -Objekt zu erstellen. Weitere Informationen zu Geometrie Transformationen finden Sie unter [Direct2D Geometries Overview](direct2d-geometries-overview.md).

## <a name="how-a-render-target-transform-affects-clips"></a>Auswirkungen einer renderzieltransformation auf Clips

Die Transformation für ein Renderziel wirkt sich darauf aus, wie das umgebende Feld eines Achsen ausgerichteten Clips berechnet wird. Wenn " [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) " aufgerufen wird, wird der *clipRect* -Parameter von der aktuellen Welt Transformation transformiert, die auf dem Renderziel festgelegt ist. Nachdem die Transformation auf *clipRect* angewendet wurde, wird das an der Achse ausgerichtete umgebende Feld für die *clipRect* berechnet. Aus Effizienzgründen wird der Inhalt auf dieses an der Achse ausgerichtete umgebende Feld und nicht auf die ursprüngliche *clipRect* zugeschnitten, die übergeben wird. Die folgenden Diagramme zeigen, wie eine Drehungs Transformation auf das Renderziel, das resultierende *clipRect* und ein berechnetes, auf Achsen ausgerichtete Begrenzungsfeld angewendet wird.

1.  Nehmen wir an, dass das Rechteck in der folgenden Abbildung ein Renderziel ist, das an den bildschirmpixeln ausgerichtet ist.

    ![Abbildung eines Rechtecks (Renderziel)](images/pushaxisalignedclip-step1-rendertarget.png)

2.  Anwenden einer Drehungs Transformation auf das Renderziel. In der folgenden Abbildung stellt das schwarze Rechteck das ursprüngliche Renderziel dar, und das rote gestrichelte Rechteck stellt das transformierte Renderziel dar.

    ![Abbildung des ursprünglichen Rechtecks und eines gedrehten Rechtecks (transformiertes Renderziel](images/pushaxisalignedclip-step2-transformed.png)

3.  Nachdem " [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) " aufgerufen wurde, wird die Drehungs Transformation auf *clipRect* angewendet. In der folgenden Abbildung stellt das blaue Rechteck den transformierten *clipRect* dar.

    ![Abbildung eines kleineren blauen Rechtecks (clipRect) innerhalb des gedrehten Rechtecks (transformiertes Renderziel)](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  Das an der Achse ausgerichtete umgebende Feld wird berechnet. In der folgenden Abbildung stellt das grüne gestrichelte Rechteck das umgebende Feld dar. Alle Inhalte werden auf dieses an der Achse ausgerichteten Begrenzungsfeld zugeschnitten.

    ![Abbildung eines grünen Begrenzungs Felds im kleinen blauen Rechteck (clipRect)](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a>Zusammenfassung

Direct2D vereinfacht das Transformieren zweidimensionaler Objekte mit vereinfachten Koordinaten Räumen und verknüpften Klassen. Durch die Verwendung verschiedener Arten von Transformationen können Sie Ihre Objekte übersetzen, drehen, neigen und skalieren, um viele beeindruckende visuelle Effekte zu erzielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 
---
title: Transformationen (DirectComposition)
description: In diesem Thema wird die Microsoft DirectComposition-Unterstützung für zweidimensionale (2D) affine (lineare) Transformationen und die Typen von Transformationen beschrieben, die DirectComposition unterstützt.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991e1205422864efdec82bbd4067b9c7662aaf29
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118655"
---
# <a name="transforms-directcomposition"></a>Transformationen (DirectComposition)

> [!NOTE]
> Für Apps auf Windows 10 empfehlen wir die Verwendung von Windows.UI.Composition-APIs anstelle von DirectComposition. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene.](/windows/uwp/composition/visual-layer-in-desktop-apps)

In diesem Thema wird die Microsoft DirectComposition-Unterstützung für zweidimensionale (2D) affine (lineare) Transformationen und die Typen von Transformationen beschrieben, die DirectComposition unterstützt.

DirectComposition unterstützt auch 3D-Perspektiventransformationen, aber da sie die Erstellung einer Zwischenbitmap erfordern, betrachtet DirectComposition sie als Effekte und nicht als Transformationen. Informationen zu 3D-Perspektivtransformationseffekten finden Sie unter [Effekte](effects.md).

Dieses Thema enthält die folgenden Abschnitte:

-   [Was ist eine DirectComposition 2D-Transformation?](#what-is-a-directcomposition-2d-transform)
-   [Der DirectComposition 2D-Koordinatenraum](#the-directcomposition-2d-coordinate-space)
-   [Unterstützung für affine 2D-Transformationen](#support-for-affine-2d-transforms)
-   [Matrix-2D-Transformationen](#matrix-2d-transforms)
-   [Transformieren von Gruppen](#transform-groups)
-   [Transformationsanimation](#transform-animation)
-   [Verwandte Themen](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>Was ist eine DirectComposition 2D-Transformation?

Mit einer 2D-Transformation können Sie die Position, Größe oder Art eines Visuals in zwei Dimensionen ändern, indem Sie das Visual an eine andere Position verschieben (Übersetzung), es vergrößern oder verkleinern (skalieren), es drehen (Drehung) oder seine Form verzerren (Verzerrung).

Eine 2D-Transformation wird erreicht, indem die Punkte eines Visuals von einer Position zu einer anderen innerhalb desselben Koordinatenraums oder von einem Koordinatenraum zu einem anderen zuordnen. Diese Zuordnung wird durch eine Tabelle mit Werten beschrieben, die als Transformationsmatrix bezeichnet wird und als Auflistung von drei Zeilen mit drei Spalten mit Gleitkommawerten definiert ist, wie in der folgenden Tabelle gezeigt.

:::row:::
    :::column:::
        M11Standard: 1.0<br/>
        M21Standard: 0.0<br/>
        M31OffsetX: 0.0
    :::column-end:::
    :::column:::
        M12Default: 0.0<br/>
        M22Default: 1.0<br/>
        M32OffsetY: 0.0
    :::column-end:::
    :::column:::
        0.0<br/>
        0.0<br/>
        1,0
    :::column-end:::
:::row-end:::

Die Transformationsmatrix für affine 2D-Transformationen ist eine 3:2-Matrix, die die dritte Spalte aus der vorherigen Transformationsmatrix ausgelassen. Die folgende Tabelle zeigt das Layout dieser Matrix.

:::row:::
    :::column:::
        M11Standard: 1.0<br/>
        M21Standard: 0.0<br/>
        M31OffsetX: 0.0
    :::column-end:::
    :::column:::
        M12Default: 0.0<br/>
        M22Default: 1.0<br/>
        M32OffsetY: 0.0
    :::column-end:::
:::row-end:::

> [!Note]  
> DirectComposition führt beim Anwenden von 2D-Transformationen auf Stereoinhalte keine spezielle Verarbeitung durch. Dies bedeutet, dass der 3D-Inhalt möglicherweise verzerrt erscheint, wenn eine 2D-Transformation darauf angewendet wird.

 

## <a name="the-directcomposition-2d-coordinate-space"></a>Der DirectComposition 2D-Koordinatenraum

DirectComposition verwendet einen linkshändigen 2D-Koordinatenraum. Das bedeutet, dass positive Werte der X-Achse nach rechts und positive Werte der y-Achse nach unten zunehmen. Visuals werden relativ zum Ursprung positioniert. Dies ist der Punkt, an dem sich die x-Achse und die y-Achse überschneiden (0, 0), wie in der folgenden Abbildung dargestellt.

![x-Achse und y-Achse eines linkshändigen Koordinatenraums](images/coordinatespace.png)

Indem Sie Werte in einer 3 by 2-Transformationsmatrix bearbeiten, können Sie ein Objekt in zwei Dimensionen drehen, skalieren, verschiegen und übersetzen. Wenn Sie beispielsweise OffsetX auf 100 und OffsetY auf 200 festlegen, verschieben Sie das Objekt um 100 Pixel nach rechts und 200 Pixel nach unten.

## <a name="support-for-affine-2d-transforms"></a>Unterstützung für affine 2D-Transformationen

Die folgende Tabelle beschreibt die Typen von affinen 2D-Transformationen, die von DirectComposition unterstützt werden, und listet die Schnittstellen auf, die Sie zum Ausführen der verschiedenen Arten von Transformationen verwenden können.



| Transformieren/Schnittstelle                                                                               | BESCHREIBUNG                                                                                              | Abbildung                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Rotieren der [**2D-Idcompositionrotatetransform-Neulinie**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[\]          | Drehen Sie ein Visual um den angegebenen Winkel um den angegebenen Mittelpunkt.                                 | ![Abbildung eines Quadrats, das um 45 Grad im Uhrzeigersinn um die Mitte des ursprünglichen Quadrats gedreht wurde](images/rotate.png)               |
| Skalieren einer [**2D-IDcompositionscaletransform-Neulinie**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[\]             | skalieren Sie ein Visual um den angegebenen Faktor um den angegebenen Mittelpunkt.                                 | ![Abbildung eines quadratisch skalierten 130 Prozent](images/scale.png)                                                                  |
| Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[ newline\]                | Verzerrt ein Visuelles um den angegebenen Winkel entlang der X- und y-Achse und um den angegebenen Mittelpunkt. | ![Abbildung einer quadratischen Schiefe von 30 Grad gegen den Uhrzeigersinn von der y-Achse](images/skew.png)                                   |
| Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ newline\] | Ändert die Position eines Visuals in Richtung der x-Achse und der y-Achse.                               | ![Abbildung eines Quadrats, das 20 Einheiten entlang der positiven X-Achse und 10 Einheiten entlang der positiven Y-Achse verschoben wurde](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>Matrix-2D-Transformationen

Mit [**der IDCompositionMatrixTransform-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) können Sie Eine eigene 3-by-2-affine 2D-Transformationsmatrix definieren und auf ein Visual anwenden. Diese Schnittstelle ist nützlich, wenn Sie einen Typ der affinen 2D-Transformation anwenden müssen, der nicht über die anderen DirectComposition-Transformationsschnittstellen verfügbar ist. Sie definieren die Matrix, indem Sie eine [**D2D \_ MATRIX \_ 3X2 \_ F-Struktur**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) ausfüllen und an die [**IDCompositionMatrixTransform::SetMatrix-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) übergeben.

## <a name="transform-groups"></a>Transformieren von Gruppen

Sie können Transformationsgruppen verwenden, um mehrere Transformationen zu einer Transformation zu kombinieren. Eine Transformationsgruppe definiert eine Auflistung von Transformationsobjekten, deren Matrizen in der Reihenfolge, in der sie in der Auflistung angegeben sind, multipliziert werden. Die resultierende Transformationsmatrix wird dann auf das Visual angewendet. Eine Transformationsgruppe erzeugt das gleiche Ergebnis wie das separat anwenden jeder Transformation.

Beachten Sie, dass die Reihenfolge der Transformationsobjekte in einer Transformationsgruppe wichtig ist. Wenn z. B. ein Visual zuerst gedreht, dann skaliert und dann übersetzt wird, ist das Ergebnis anders als wenn das Visual zuerst übersetzt, dann gedreht und dann skaliert wird. DirectComposition wendet die Transformationen immer in der Reihenfolge auf ein Visual an, in der sie in der Auflistung angegeben sind.

Um eine Transformationsgruppe zu erstellen, erstellen Sie zuerst die Transformationsobjekte, die Sie in die Gruppe enthalten möchten, und übergeben dann ein Array von Transformationsobjektzetern an die [**IDCompositionDevice::CreateTransformGroup-Methode.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) Nachdem Sie eine Transformationsgruppe erstellt haben, können Sie keine Transformationsobjekte hinzufügen oder entfernen. Sie können jedoch die Eigenschaften der einzelnen Transformationsobjekte in der Auflistung ändern, und die Änderungen werden in der resultierenden Transformationsmatrix widergespiegelt.

## <a name="transform-animation"></a>Transformationsanimation

Die Eigenschaften einer Transformation können animiert werden. Wenn eine Eigenschaft animiert wird, ändert DirectComposition den Wert der Eigenschaft im Laufe der Zeit und nicht alle auf einmal. Dies ist besonders nützlich, wenn Übergänge erstellt werden. Weitere Informationen finden Sie unter [Animation](animation.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectComposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 

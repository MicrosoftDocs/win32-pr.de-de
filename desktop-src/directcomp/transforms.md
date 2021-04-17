---
title: Transformationen (directcomposition)
description: In diesem Thema wird die Unterstützung von Microsoft directcomposition für zweidimensionale (2D) affine (lineare) Transformationen erläutert, und es werden die Typen von Transformationen beschrieben, die von directcomposition unterstützt werden.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27a1fec5774d208f240e6d2f1c8b7df09d25c486
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104571067"
---
# <a name="transforms-directcomposition"></a>Transformationen (directcomposition)

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema wird die Unterstützung von Microsoft directcomposition für zweidimensionale (2D) affine (lineare) Transformationen erläutert, und es werden die Typen von Transformationen beschrieben, die von directcomposition unterstützt werden.

Directcomposition unterstützt auch 3D-perspektivische Transformationen, aber da die Erstellung einer zwischenbitmap erforderlich ist, werden Sie von directcomposition als Effekte und nicht als Transformationen betrachtet. Weitere Informationen zu den Effekten von 3D-Perspektiven Transformationen finden Sie unter [Effekte](effects.md).

Dieses Thema enthält die folgenden Abschnitte:

-   [Was ist eine directcomposition 2D-Transformation?](#what-is-a-directcomposition-2d-transform)
-   [Der 2D-Koordinaten Bereich von directcomposition](#the-directcomposition-2d-coordinate-space)
-   [Unterstützung von affinen 2D-Transformationen](#support-for-affine-2d-transforms)
-   [Matrix 2D-Transformationen](#matrix-2d-transforms)
-   [Transformieren von Gruppen](#transform-groups)
-   [Animation transformieren](#transform-animation)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a>Was ist eine directcomposition 2D-Transformation?

Mit einer 2D-Transformation können Sie die Position, die Größe oder die Art eines visuellen Elements in zwei Dimensionen ändern, indem Sie das visuelle Element an eine andere Position (Übersetzung) verschieben, die Größe vergrößern oder verkleinern (Skalieren), Sie drehen oder die Form verzerren (Neigung).

Eine 2D-Transformation wird erzielt, indem die Punkte eines visuellen Elements von einer Position zu einer anderen innerhalb desselben Koordinaten Bereichs oder von einem Koordinaten Bereich zu einem anderen geordnet werden. Diese Zuordnung wird durch eine Tabelle mit Werten beschrieben, die als Transformationsmatrix bezeichnet werden und als eine Auflistung von drei Zeilen mit drei Spalten von Gleit Komma Werten definiert sind, wie in der folgenden Tabelle dargestellt.



|                 |                 |     |
|-----------------|-----------------|-----|
| M11Default: 1,0 | M12Default: 0,0 | 0,0 |
| M21Default: 0,0 | M22Default: 1,0 | 0,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 | 1.0 |



 

Die Transformationsmatrix für affine 2D-Transformationen ist eine 3 x 2-Matrix, in der die dritte Spalte aus der vorherigen Transformationsmatrix ausgelassen wird. In der folgenden Tabelle wird das Layout dieser Matrix gezeigt.



|                 |                 |
|-----------------|-----------------|
| M11Default: 1,0 | M12Default: 0,0 |
| M21Default: 0,0 | M22Default: 1,0 |
| M31OffsetX: 0,0 | M32OffsetY: 0,0 |



 

> [!Note]  
> Directcomposition führt keine besondere Verarbeitung durch, wenn 2D-Transformationen auf Stereo Inhalte angewendet werden. Dies bedeutet, dass der 3D-Inhalt möglicherweise verzerrt erscheint, wenn eine 2D-Transformation darauf angewendet wird.

 

## <a name="the-directcomposition-2d-coordinate-space"></a>Der 2D-Koordinaten Bereich von directcomposition

Directcomposition verwendet einen von Links übergebenen 2D-Koordinatenraum. Das heißt, die positiven Werte der x-Achse erhöhen die Rechte und die positiven Werte der y-Achse nach unten. Visuelle Elemente werden relativ zum Ursprung positioniert. Dies ist der Punkt, an dem sich die x-Achse und die y-Achse überschneiden (0,0), wie in der folgenden Abbildung dargestellt.

![die x-Achse und die y-Achse eines Links gerichteten Koordinaten Raums](images/coordinatespace.png)

Durch die Bearbeitung von Werten in einer 3-zu-2-Transformationsmatrix können Sie ein Objekt in zwei Dimensionen drehen, skalieren, neigen und übersetzen. Wenn Sie z. b. OffsetX auf 100 und OffsetY auf 200 festlegen, verschieben Sie das Objekt nach rechts um 100 Pixel und nach unten 200 Pixel.

## <a name="support-for-affine-2d-transforms"></a>Unterstützung von affinen 2D-Transformationen

In der folgenden Tabelle werden die von directcomposition unterstützten affinen 2D-Transformationen beschrieben, und es werden die Schnittstellen aufgelistet, die Sie verwenden können, um die verschiedenen Arten von Transformationen auszuführen.



| Transformation/Schnittstelle                                                                               | BESCHREIBUNG                                                                                              | Abbildung                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Drehen von 2D-[**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ -Zeilen Umstellungs Zeilen\]          | Drehen Sie ein visuelles Element um den angegebenen Winkel um den angegebenen Mittelpunkt.                                 | ![Abbildung eines Quadrats, das um 45 Grad im Uhrzeigersinn um den Mittelpunkt des ursprünglichen Quadrats gedreht wurde](images/rotate.png)               |
| Skalieren 2D-[**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)-Zeilen Umstellungs \[ Zeilen\]             | Skalieren Sie ein visuelles Element um den angegebenen Faktor zum angegebenen Mittelpunkt.                                 | ![Abbildung eines quadratischen skalierten 130-Prozentsatzes](images/scale.png)                                                                  |
| Neigung 2D [**idcompositionschiewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[ Zeilenumbruch\]                | verzerrt eine Visualisierung um den angegebenen Winkel entlang der x-und y-Achse und um den angegebenen Mittelpunkt. | ![Abbildung einer quadratischen Verzerrung von 30 Grad gegen den Uhrzeigersinn von der y-Achse](images/skew.png)                                   |
| Übersetzen von 2D-[**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ -Zeilen Umsätzen\] | Ändern Sie die Position eines visuellen Elements in Richtung der x-und y-Achse.                               | ![Abbildung eines quadratischen verschoder 20 Einheiten entlang der positiven x-Achse und 10 Einheiten entlang der positiven y-Achse](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a>Matrix 2D-Transformationen

Die [**idcompositionmatrixtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) -Schnittstelle ermöglicht es Ihnen, ihre eigene 3-bis-2-affine 2D-Transformationsmatrix zu definieren und Sie auf ein visuelles Element anzuwenden. Diese Schnittstelle ist nützlich, wenn Sie einen Typ von affine 2D-Transformation anwenden müssen, die über die anderen directcomposition-Transformations Schnittstellen nicht verfügbar ist. Sie definieren die Matrix, indem Sie eine [**D2D \_ Matrix \_ 3x2- \_ F-**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Struktur ausfüllen und an die [**idcompositionmatrixtransform:: setMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) -Methode übergeben.

## <a name="transform-groups"></a>Transformieren von Gruppen

Sie können Transformationsgruppen verwenden, um mehrere Transformationen zu einer zu kombinieren. Eine Transformations Gruppe definiert eine Auflistung von Transformations Objekten, deren Matrizen in der Reihenfolge multipliziert werden, in der Sie in der Auflistung angegeben werden. Die resultierende Transformationsmatrix wird dann auf das visuelle Element angewendet. Eine Transformations Gruppe erzeugt das gleiche Ergebnis wie das Anwenden der einzelnen Transformationen separat.

Beachten Sie, dass die Reihenfolge der Transformations Objekte in einer Transformations Gruppe wichtig ist. Wenn ein visuelles Element z. b. zuerst gedreht, dann skaliert und dann übersetzt wird, unterscheidet sich das Ergebnis von dem, wenn das visuelle Element zuerst übersetzt, dann gedreht und dann skaliert wird. Directcomposition wendet die Transformationen immer in der Reihenfolge an, in der Sie in der Auflistung angegeben werden.

Erstellen Sie zum Erstellen einer Transformations Gruppe zuerst die Transformations Objekte, die Sie in die Gruppe einschließen möchten, und übergeben Sie dann ein Array von Transformations Objekt Zeigern an die [**idcompositiondevice:: kreatetransformgroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) -Methode. Nachdem Sie eine Transformations Gruppe erstellt haben, können Sie keine Transformations Objekte hinzufügen oder entfernen. Sie können jedoch die Eigenschaften der einzelnen Transformations Objekte in der Auflistung ändern, und die Änderungen werden in der resultierenden Transformationsmatrix widergespiegelt.

## <a name="transform-animation"></a>Animation transformieren

Die Eigenschaften einer Transformation können animiert werden. Wenn eine Eigenschaft animiert wird, ändert directcomposition den Wert der Eigenschaft im Zeitverlauf und nicht alle auf einmal. Dies ist besonders nützlich, wenn Übergänge erstellt werden. Weitere Informationen finden Sie unter [Animation](animation.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directcomposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 

---
title: Effekte (directcomposition)
description: In diesem Thema werden die Grundlagen von Microsoft directcomposition-Effekten erläutert, und es werden die von directcomposition unterstützten Auswirkungen beschrieben.
ms.assetid: 805B17D2-2F6B-4C25-8C6D-41FFA5DFC774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cfd1ca154dcbc7e55ca65cc34d04cfa7d73ccee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390495"
---
# <a name="effects-directcomposition"></a>Effekte (directcomposition)

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden die Grundlagen von Microsoft directcomposition-Effekten erläutert, und es werden die von directcomposition unterstützten Auswirkungen beschrieben.

Dieses Thema enthält folgende Abschnitte:

-   [Was ist ein directcomposition-Effekt?](#what-is-a-directcomposition-effect)
-   [Deckkraft](#opacity)
-   [3D-Perspektiven-Transformationseffekte](#3d-perspective-transform-effects)
    -   [Der 3D-Koordinaten Bereich von directcomposition](#the-directcomposition-3d-coordinate-space)
    -   [3D-Drehungs Transformations Effekt](#3d-rotation-transform-effect)
    -   [Umwandlung von 3D-Skalierungs Effekten](#3d-scaling-transform-effect)
    -   [Transformations Effekt der 3D-Übersetzung](#3d-translation-transform-effect)
    -   [3D-Matrix Transformations Effekt](#3d-matrix-transform-effect)
    -   [3D-Transformations Effekt Gruppe](#3d-transform-effect-group)
-   [Effekt Objekte](#effect-objects)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-a-directcomposition-effect"></a>Was ist ein directcomposition-Effekt?

Ein directcomposition- *Effekt* ist ein Bitmap-Vorgang, der während der rasterisierung eines visuellen Elements angewendet wird, um die Darstellung des visuellen Elements auf irgendeine Weise zu ändern.

Directcomposition erstellt einen Effekt, indem eine visuelle Unterstruktur erstellt und in eine einzelne Bitmap gerendert wird, bevor der Effekt angewendet wird. Um z. b. einen 3D-perspektivischen Transformations Effekt zu erstellen, erzeugt directcomposition ein Bild einer visuellen Unterstruktur und Texturen das Bild dann auf eine 3D-Ebene, die entsprechend der resultierenden Matrix des 3D-Transformations Effekts transformiert wird.

Directcomposition unterstützt die folgenden Arten von Effekten.



| Effekttyp                                                   | BESCHREIBUNG                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------|
| [Deckkraft](#opacity)                                           | Legt die Deckkraft eines gesamten visuellen Elements fest.                                      |
| [3D-Perspektiven Transformation](#3d-perspective-transform-effects) | Wendet einen dreidimensionalen (3D) perspektivischen Transformations Effekt auf ein visuelles Element an. |



 

> [!Note]  
> Directcomposition führt keine besondere Verarbeitung durch, wenn Effekte auf 3D-Stereo Inhalte angewendet werden. Dies bedeutet, dass der 3D-Inhalt möglicherweise verzerrt erscheint, wenn ein Effekt darauf angewendet wird.

 

## <a name="opacity"></a>Opacity

Der Deck Kraft Effekt ermöglicht es Ihnen, den Deckkraft Faktor festzulegen, der beim Rendern des visuellen Elements auf ein gesamtes visuelles Element angewendet wird. Es unterscheidet sich von einer Alpha Maske darin, dass der gleiche Deckkraft Faktor auf alle Pixel im visuellen Element angewendet wird. Die Deckkraft wird als Wert zwischen 0 (vollständig transparent) und 1 (vollständig nicht transparent) angegeben.

Der Deck Kraft Faktor wird von der übergeordneten auf die untergeordneten visuellen Elemente angewendet, aber die sichtbaren Auswirkungen der schalten Einstellungen der Deckkraft werden im Eigenschafts Wert einzelner untergeordneter Visuals nicht angegeben. Wenn beispielsweise eine visuelle Stamm Visualisierung eine 50% (0,5)-Deckkraft aufweist und eines der untergeordneten Elemente eine 20%-Deckkraft (0,2) aufweist, wird die Deckkraft für dieses untergeordnete Element als 10% (0,1) gerendert, aber der Wert der Deck Kraft-Eigenschaft des untergeordneten Elements wäre weiterhin 0,2.

## <a name="3d-perspective-transform-effects"></a>3D-Perspektiven-Transformationseffekte

In diesem Abschnitt wird der Koordinaten Bereich beschrieben, der von directcomposition zum Ausführen von 3D-Perspektiven Transformations Effekten verwendet wird. Außerdem werden die Typen der von directcomposition unterstützten 3D-perspektivierungs Effekte beschrieben.

-   [Der 3D-Koordinaten Bereich von directcomposition](#the-directcomposition-3d-coordinate-space)
-   [3D-Drehungs Transformations Effekt](#3d-rotation-transform-effect)
-   [Umwandlung von 3D-Skalierungs Effekten](#3d-scaling-transform-effect)
-   [Transformations Effekt der 3D-Übersetzung](#3d-translation-transform-effect)
-   [3D-Matrix Transformations Effekt](#3d-matrix-transform-effect)
-   [3D-Transformations Effekt Gruppe](#3d-transform-effect-group)

> [!Note]  
> In directcomposition funktioniert das Anwenden von 3D-Effekten auf mehrere Ebenen in der visuellen Struktur nicht auf die gleiche Weise wie bei einer vollständigen 3D-Engine, wie z. b. Microsoft Direct3D. Angenommen, Sie verfügen über ein übergeordnetes visuelles Element, das über ein einzelnes untergeordnetes Visual verfügt. Wenn das untergeordnete visuelle Element in der z-Richtung (um die y-Achse) um 90 Grad vorwärts gedreht wird, würde der Rand des untergeordneten visuellen Edge den Viewer sehen, und es wird erwartet, dass das visuelle Element nicht sichtbar ist (da eine Bitmap keine echte Tiefe hat). Wenn das übergeordnete visuelle Element in der negativen z-Richtung (um die y-Achse) um 90 Grad rückwärts gedreht wird, wird möglicherweise erwartet, dass das untergeordnete visuelle Element vollständig sichtbar wird (da die Transformationen einander negieren). In directcomposition ist dies jedoch nicht der Fall. Das untergeordnete visuelle Element ist nicht sichtbar, da es in die übergeordnete Bitmap "vereinfacht" wird.

 

### <a name="the-directcomposition-3d-coordinate-space"></a>Der 3D-Koordinaten Bereich von directcomposition

Der directcomposition-Koordinatenraum für 3D-Transformationseffekte sucht den Ursprung (0, 0, 0) in der oberen linken Ecke der Bitmap-Oberfläche, wobei die positiven Werte der x-Achse nach rechts und die positiven Werte der y-Achse nach unten fortgesetzt werden und positive z-Achsen-Werte nach außen von dem Ursprung in den Viewer übergehen. Diese Abbildung zeigt den 3D-Koordinaten Bereich von directcomposition.

![3D--Koordinaten Bereich der directcompostion](images/3d-coordinate-space.png)

### <a name="3d-rotation-transform-effect"></a>3D-Drehungs Transformations Effekt

Ein 3D-Drehungs Transformations Effekt dreht eine Visualisierung in drei Dimensionen um den angegebenen Winkel um einen Drehungs Achsen Vektor \[ x, y und z, der \] sich am angegebenen Mittelpunkt (x, y, z) befindet. Der Winkel wird in Grad angegeben. Der standardmäßige Drehungs Achsen Vektor ist \[ 0, 0,-1 \] , und der Standard Mittelpunkt ist (0,0).

Verwenden Sie die [**idcompositiondevice:: CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) -Methode, um ein 3D-Drehungs Transformations Objekt zu erstellen. Die-Methode ruft eine [**IDCompositionRotateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d) -Schnittstelle ab, die Sie verwenden können, um die Eigenschaften des-Objekts festzulegen.

### <a name="3d-scaling-transform-effect"></a>Umwandlung von 3D-Skalierungs Effekten

Ein 3D-Effekt der Skalierungs Transformation sorgt für eine größere oder kleinere Visualisierung. Dabei wird ein visuelles Element in der \[ x-, y-und z- \] Richtung zum Mittelpunkt (x, y, z) skaliert. Der Standard Mittelpunkt ist (0,0).

Verwenden Sie die [**idcompositiondevice:: CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d) -Methode, um ein 3D-Skalierungs Transformations Objekt zu erstellen. Die-Methode ruft eine [**IDCompositionScaleTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform3d) -Schnittstelle ab, die Sie verwenden können, um die Eigenschaften des-Objekts festzulegen.

### <a name="3d-translation-transform-effect"></a>Transformations Effekt der 3D-Übersetzung

Ein 3D-Transformations Effekt ändert die Position eines visuellen Elements in der \[ x-, y-und z- \] Richtung.

Verwenden Sie die [**idcompositiondevice:: CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d) -Methode zum Erstellen eines 3D-Translation Transform-Objekts. Die-Methode ruft eine [**IDCompositionTranslateTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d) -Schnittstelle ab, die Sie verwenden können, um die Eigenschaften des-Objekts festzulegen.

### <a name="3d-matrix-transform-effect"></a>3D-Matrix Transformations Effekt

Die [**IDCompositionMatrixTransform3D**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) -Schnittstelle ermöglicht es Ihnen, eine eigene 4-x-4-Transformationsmatrix zu definieren und Sie auf ein visuelles Element anzuwenden. Diese Schnittstelle ist nützlich, wenn Sie einen 3D-perspektivischen Transformations Effekt anwenden müssen, der über die anderen Schnittstellen von directcomposition 3D-Transformations Effekten nicht verfügbar ist. Sie definieren die Matrix, indem Sie eine [**D3DMATRIX**](/windows/desktop/direct3d10/d3d10-d3dmatrix) -Struktur ausfüllen und Sie an die [**IDCompositionMatrixTransform3D:: setMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) -Methode übergeben. Alternativ können Sie jedes Element der Matrix mit der [**IDCompositionMatrixTransform3D:: setmatrixelement**](/previous-versions/windows/desktop/legacy/hh437429(v=vs.85)) -Methode festlegen.

### <a name="3d-transform-effect-group"></a>3D-Transformations Effekt Gruppe

[**Idcompositiondevice:: CreateTransform3DGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransform3dgroup) erstellt eine Auflistung von 3D-Transformations Effekten, die Sie auf ein visuelles Element als Gruppe anwenden können. Das Array kann eine beliebige Anzahl von Transformations Objekten enthalten und kann Matrix-, Drehung-, Skalierungs-und Übersetzungs Transformationen einschließen. Die Auflistung von 3D-Transformations Objekten führt zu einer Transformation, deren Wert der Matrix Multiplikation der einzelnen Transformations Matrizen in der Auflistung entspricht.

Die Reihenfolge der einzelnen Transformationen in der Gruppe ist wichtig. Wenn Sie z. b. zuerst drehen, dann skalieren und dann übersetzen, erhalten Sie ein anderes Ergebnis als bei der ersten Übersetzung, dann drehen und skalieren. Directcomposition respektiert die Reihenfolge, in der Sie 3D-Transformationen innerhalb einer Transform 3D-Gruppe auf die gleiche Weise wie für 2D-Transformationen angeben. Außerdem führen 3D-Perspektiven Transformationen zu einer Vereinfachung der visuellen Struktur, nachdem alle 3D-Transformationen in der aktuellen Visualisierung angewendet wurden. Dadurch wird sichergestellt, dass die Szene so nah wie möglich in 3D aussieht.

## <a name="effect-objects"></a>Effekt Objekte

Wenn Sie einen Effekt auf ein visuelles Element anwenden möchten, müssen Sie zunächst die Eigenschaften eines Effekt Objekts erstellen und festlegen, das den Typ des Effekts darstellt, den Sie im visuellen Element erzeugen möchten. Anschließend müssen Sie das Effect-Objekt auf die Effect-Eigenschaft des visuellen Elements anwenden.

Verwenden Sie zum Erstellen eines Effekt Objekts eine der folgenden [**idcompositiondevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) -Schnittstellen Methoden, um ein Effect-Objekt für den gewünschten Typ von Effekt zu erstellen. Mit den folgenden Methoden werden Effekt Objekte erstellt:

-   [**CreateMatrixTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-creatematrixtransform3d)
-   [**CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d)
-   [**CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d)
-   [**CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d)

Jede der vorangehenden Methoden Ruft eine Schnittstelle ab, mit der Sie die Eigenschaften des neu erstellten Effekt Objekts festlegen können. Verwenden Sie die Schnittstellen Methoden, um die Eigenschaften nach Bedarf festzulegen, um den gewünschten visuellen Effekt zu erzielen.

Die meisten Eigenschaften eines Effekt Objekts können animiert werden. Um eine bestimmte Eigenschaft zu animieren, erstellen Sie ein Animations Objekt und wenden es auf die Eigenschaft an, die Sie animieren möchten. Legen Sie andernfalls die-Eigenschaft auf einen statischen Wert fest, der den gewünschten Effekt erzeugt. Weitere Informationen zum Animieren von Eigenschaften finden Sie unter [Animation](animation.md).

Rufen Sie die [**idcompositionvisual:: SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) -Methode auf, um ein Effekt Objekt auf Visual anzuwenden. Wenn Sie einen Effekt auf ein visuelles Element anwenden, wird der Effekt auf die gesamte visuelle Teilstruktur angewendet, die auf das visuelle Element zeigt. Wenn Sie also beispielsweise die Deckkraft eines visuellen Elements auf 50 Prozent festlegen, wird die Deckkraft aller untergeordneten visuellen Elemente in der visuellen Teilstruktur um 50% reduziert. Sie können das gleiche Effekt Objekt auf ein oder mehrere visuelle Elemente anwenden. Wenn Sie die Eigenschaften eines Effekt Objekts nach dem Anwenden auf visuelle Elemente ändern, werden alle visuellen Elemente neu zusammengesetzt, um die Änderung widerzuspiegeln.

Mithilfe eines Effekts-Gruppen Objekts können Sie gleichzeitig mehrere Effekte auf ein visuelles Element anwenden. Rufen Sie zuerst " [**idcompositiondevice::**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) " auf, um das Objekt "Effect Group" zu erstellen, und fügen Sie dann mithilfe der [**idcompositioneffectgroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) -Schnittstelle des Objekts Effekte zur Gruppe hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directcomposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 
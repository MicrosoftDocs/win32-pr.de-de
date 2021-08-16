---
title: Effekte (DirectComposition)
description: In diesem Thema werden die Grundlagen von Microsoft DirectComposition-Effekten und die von DirectComposition unterstützten Arten von Effekten beschrieben.
ms.assetid: 805B17D2-2F6B-4C25-8C6D-41FFA5DFC774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c5119367a35725a85efe20b8ba4d0f9f9887ff91b4d9618e2215bedfbfef67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905050"
---
# <a name="effects-directcomposition"></a>Effekte (DirectComposition)

> [!NOTE]
> Für Apps in Windows 10 wird empfohlen, Windows.UI.Composition-APIs anstelle von DirectComposition zu verwenden. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden die Grundlagen von Microsoft DirectComposition-Effekten und die von DirectComposition unterstützten Arten von Effekten beschrieben.

Dieses Thema enthält folgende Abschnitte:

-   [Was ist ein DirectComposition-Effekt?](#what-is-a-directcomposition-effect)
-   [Deckkraft](#opacity)
-   [3D-Perspektiventransformationseffekte](#3d-perspective-transform-effects)
    -   [Der DirectComposition-3D-Koordinatenraum](#the-directcomposition-3d-coordinate-space)
    -   [3D-Drehungstransformationseffekt](#3d-rotation-transform-effect)
    -   [3D-Skalierungstransformationseffekt](#3d-scaling-transform-effect)
    -   [3D-Übersetzungstransformationseffekt](#3d-translation-transform-effect)
    -   [3D-Matrixtransformationseffekt](#3d-matrix-transform-effect)
    -   [3D-Transformationseffektgruppe](#3d-transform-effect-group)
-   [Effect-Objekte](#effect-objects)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-a-directcomposition-effect"></a>Was ist ein DirectComposition-Effekt?

Ein DirectComposition-Effekt ist ein Bitmapvorgang, der während der Rasterung eines Visuals angewendet wird, um die Darstellung des Visuals in irgendeiner Weise zu ändern. 

DirectComposition erstellt einen Effekt, indem eine visuelle Teilstruktur vor dem Anwenden des Effekts in eine einzelne Bitmap gerendert wird. Um beispielsweise einen 3D-Perspektiventransformationseffekt zu erstellen, erzeugt DirectComposition ein Bild einer visuellen Unterstruktur und texturiert das Bild dann auf eine 3D-Ebene, die entsprechend der resultierenden Matrix des 3D-Transformationseffekts transformiert wird.

DirectComposition unterstützt die folgenden Arten von Effekten.



| Effekttyp                                                   | BESCHREIBUNG                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------|
| [Deckkraft](#opacity)                                           | Legt die Deckkraft eines gesamten Visuals fest.                                      |
| [3D-Perspektiventransformation](#3d-perspective-transform-effects) | Wendet einen dreidimensionalen (3D)-Perspektiventransformationseffekt auf ein Visual an. |



 

> [!Note]  
> DirectComposition führt keine besondere Verarbeitung durch, wenn Effekte auf 3D-Stereoinhalte angewendet werden. Dies bedeutet, dass der 3D-Inhalt möglicherweise verzerrt erscheint, wenn ein Effekt darauf angewendet wird.

 

## <a name="opacity"></a>Opacity

Mit dem Deckkrafteffekt können Sie den Deckkraftfaktor festlegen, der beim Rendern des Visuals auf ein gesamtes Visual angewendet wird. Es unterscheidet sich von einer Alphamaske darin, dass der gleiche Deckkraftfaktor auf alle Pixel im Visual angewendet wird. Deckkraft wird als Wert im Bereich von 0 (vollständig transparent) bis 1 (vollständig deckend) angegeben.

Der Deckkraftfaktor wird von übergeordneten auf untergeordnete Visuals angewendet, aber die sichtbaren Auswirkungen der geschachtelten Deckkrafteinstellungen werden nicht im Eigenschaftswert einzelner untergeordneter Visuals angegeben. Wenn z. B. ein Stammvisual eine Deckkraft von 50 % (0,5) und eines seiner untergeordneten Elemente eine Deckkraft von 20 % (0,2) hat, wird die Deckkraft für das untergeordnete Element als 10 % (0,1) gerendert, aber der Wert der Deckkrafteigenschaft des untergeordneten Objekts wäre weiterhin 0,2.

## <a name="3d-perspective-transform-effects"></a>3D-Perspektiventransformationseffekte

In diesem Abschnitt wird der Koordinatenbereich beschrieben, den DirectComposition zum Ausführen von Transformationseffekten für die 3D-Perspektive verwendet. Außerdem werden die Typen von 3D-Perspektiventransformationseffekten beschrieben, die DirectComposition unterstützt.

-   [Der DirectComposition-3D-Koordinatenraum](#the-directcomposition-3d-coordinate-space)
-   [3D-Drehungstransformationseffekt](#3d-rotation-transform-effect)
-   [3D-Skalierungstransformationseffekt](#3d-scaling-transform-effect)
-   [3D-Übersetzungstransformationseffekt](#3d-translation-transform-effect)
-   [3D-Matrixtransformationseffekt](#3d-matrix-transform-effect)
-   [3D-Transformationseffektgruppe](#3d-transform-effect-group)

> [!Note]  
> In DirectComposition funktioniert das Anwenden von 3D-Effekten auf mehrere Ebenen in der visuellen Struktur nicht auf die gleiche Weise wie bei einer vollständigen 3D-Engine wie Microsoft Direct3D. Betrachten Sie beispielsweise ein übergeordnetes Visual, das über ein einzelnes untergeordnetes Visual verfügt. Wenn das untergeordnete Visual um 90 Grad in z-Richtung (um die y-Achse) gedreht wird, wird der Rand des untergeordneten visuellen Rands dem Viewer angezeigt. Daher erwarten wir, dass das Visual nicht sichtbar ist (da eine Bitmap keine echte Tiefe hat). Wenn das übergeordnete Visual dann um 90 Grad in negativer Z-Richtung (um die y-Achse) rückwärts gedreht wird, erwarten wir möglicherweise, dass das untergeordnete Visual vollständig sichtbar wird (da sich die Transformationen gegenseitig negieren). In DirectComposition ist dies jedoch nicht der Fall. Das untergeordnete Visual ist nicht sichtbar, da es in die übergeordnete Bitmap "flacher" wurde.

 

### <a name="the-directcomposition-3d-coordinate-space"></a>Der DirectComposition-3D-Koordinatenraum

Der DirectComposition-Koordinatenraum für 3D-Transformationseffekte sucht den Ursprung (0,0,0) in der oberen linken Ecke der Bitmapoberfläche, wobei positive x-Achsenwerte nach rechts fortgesetzt werden, positive y-Achsenwerte nach unten und positive Z-Achsenwerte, die vom Ursprung nach außen in Richtung des Betrachters fortgesetzt werden. Diese Abbildung zeigt den DirectComposition-3D-Koordinatenraum.

![directcompostion 3D-Koordinatenraum](images/3d-coordinate-space.png)

### <a name="3d-rotation-transform-effect"></a>3D-Drehungstransformationseffekt

Ein 3D-Drehungstransformationseffekt rotiert ein Visuelles in drei Dimensionen um den angegebenen Winkel um einen Drehachsenvektor \[ x,y,z, \] der sich am angegebenen Mittelpunkt (x,y,z) befindet. Der Winkel wird in Grad angegeben. Der Standardrotationsachsenvektor ist \[ 0,0,-1, \] und der Standardmittelpunkt ist (0,0,0).

Verwenden Sie die [**IDCompositionDevice::CreateRotateTransform3D-Methode,**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d) um ein 3D-Drehungstransformationsobjekt zu erstellen. Die -Methode ruft eine [**IDCompositionRotateTransform3D-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d) ab, mit der Sie die Eigenschaften des Objekts festlegen können.

### <a name="3d-scaling-transform-effect"></a>3D-Skalierungstransformationseffekt

Ein 3D-Skalierungstransformationseffekt macht ein Visuelles größer oder kleiner. Es skaliert ein Visual in der \[ Richtung x,y,z \] um den Mittelpunkt (x,y,z). Der Standardmittelpunkt ist (0,0,0).

Verwenden Sie die [**IDCompositionDevice::CreateScaleTransform3D-Methode,**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d) um ein 3D-Skalierungstransformationsobjekt zu erstellen. Die -Methode ruft eine [**IDCompositionScaleTransform3D-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform3d) ab, mit der Sie die Eigenschaften des Objekts festlegen können.

### <a name="3d-translation-transform-effect"></a>3D-Übersetzungstransformationseffekt

Ein 3D-Übersetzungstransformationseffekt ändert die Position eines Visuals in der \[ Richtung x,y,z. \]

Verwenden Sie die [**IDCompositionDevice::CreateTranslateTransform3D-Methode,**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d) um ein 3D-Übersetzungstransformationsobjekt zu erstellen. Die -Methode ruft eine [**IDCompositionTranslateTransform3D-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d) ab, mit der Sie die Eigenschaften des Objekts festlegen können.

### <a name="3d-matrix-transform-effect"></a>3D-Matrixtransformationseffekt

Mit der [**IDCompositionMatrixTransform3D-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) können Sie Eine eigene Transformationsmatrix von 4 x 4 definieren und auf ein Visual anwenden. Diese Schnittstelle ist nützlich, wenn Sie einen Typ von 3D-Perspektiventransformationseffekt anwenden müssen, der nicht über die anderen DirectComposition 3D-Transformationseffektschnittstellen verfügbar ist. Sie definieren die Matrix, indem Sie eine [**D3DMATRIX-Struktur**](/windows/desktop/direct3d10/d3d10-d3dmatrix) füllen und an die [**IDCompositionMatrixTransform3D::SetMatrix-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) übergeben. Alternativ können Sie jedes Element der Matrix mithilfe der [**IDCompositionMatrixTransform3D::SetMatrixElement-Methode**](/previous-versions/windows/desktop/legacy/hh437429(v=vs.85)) festlegen.

### <a name="3d-transform-effect-group"></a>3D-Transformationseffektgruppe

Die [**IDCompositionDevice::CreateTransform3DGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransform3dgroup) erstellt eine Sammlung von 3D-Transformationseffekten, die Sie als Gruppe auf ein Visual anwenden können. Das Array kann eine beliebige Anzahl von Transformationsobjekten sowie Matrix-, Dreh-, Skalierungs- und Übersetzungstransformationen enthalten. Die Auflistung von 3D-Transformationsobjekten führt zu einer Transformation, deren Wert die Matrixmultiplikation der einzelnen Transformationsmatrizen in der Auflistung ist.

Die Reihenfolge der einzelnen Transformationen in der Gruppe ist wichtig. Wenn Sie z. B. zuerst rotieren, dann skalieren und übersetzen, erhalten Sie ein anderes Ergebnis als beim ersten Übersetzen, drehen und dann skalieren. DirectComposition beachtet die Reihenfolge, in der Sie 3D-Transformationen innerhalb einer Transformations-3D-Gruppe angeben, genauso wie bei 2D-Transformationen. Darüber hinaus führen 3D-Perspektiventransformationen zu einer Vereinfachte der visuellen Struktur, nachdem alle 3D-Transformationen im aktuellen Visual angewendet wurden. Dadurch wird sichergestellt, dass die Szene so nah wie möglich an 3D ansieht.

## <a name="effect-objects"></a>Effect-Objekte

Um einen Effekt auf ein Visual anzuwenden, müssen Sie zunächst die Eigenschaften eines Effektobjekts erstellen und festlegen, das den Effekttyp darstellt, den Sie für das Visual erzeugen möchten. Anschließend müssen Sie das Effect-Objekt auf die Effect-Eigenschaft des Visuals anwenden.

Verwenden Sie zum Erstellen eines Effektobjekts eine der folgenden [**IDCompositionDevice-Schnittstellenmethoden,**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) um ein Effektobjekt für den gewünschten Effekttyp zu erstellen. Die folgenden Methoden erstellen Effect-Objekte:

-   [**CreateMatrixTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-creatematrixtransform3d)
-   [**CreateRotateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform3d)
-   [**CreateScaleTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform3d)
-   [**CreateTranslateTransform3D**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform3d)

Jede der vorangehenden Methoden ruft eine Schnittstelle ab, mit der Sie die Eigenschaften des neu erstellten Effektobjekts festlegen können. Verwenden Sie die Schnittstellenmethoden, um die Eigenschaften nach Bedarf festzulegen, um den gewünschten visuellen Effekt zu erzeugen.

Die meisten Eigenschaften eines Effektobjekts können animiert werden. Erstellen Sie zum Animieren einer bestimmten Eigenschaft ein Animationsobjekt, und wenden Sie es auf die Eigenschaft an, die Sie animieren möchten. Legen Sie andernfalls die -Eigenschaft auf einen statischen Wert fest, der den gewünschten Effekt erzeugt. Weitere Informationen zum Animieren von Eigenschaften finden Sie unter [Animation](animation.md).

Um ein Effektobjekt auf ein Visual anzuwenden, rufen Sie die [**IDCompositionVisual::SetEffect-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) auf. Wenn Sie einen Effekt auf ein Visual anwenden, wird der Effekt auf die gesamte visuelle Teilstruktur angewendet, die auf diesem Visual basiert. Wenn Sie also beispielsweise die Deckkraft eines Visuals auf 50 Prozent festlegen, wird die Deckkraft aller untergeordneten Visuals in der visuellen Unterstruktur um 50 Prozent reduziert. Sie können dasselbe Effektobjekt auf ein oder mehrere Visuals anwenden. Wenn Sie die Eigenschaften eines Effektobjekts ändern, nachdem Sie es auf Visuals anwenden, werden alle Visuals neu zusammengesetzt, um die Änderung widerzubilden.

Mithilfe eines Effektgruppenobjekts können Sie gleichzeitig mehrere Effekte auf ein Visual anwenden. Rufen Sie [**zuerst IDCompositionDevice::CreateEffectGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createeffectgroup) auf, um das Effektgruppenobjekt zu erstellen, und fügen Sie der Gruppe dann mithilfe der [**IDCompositionEffectGroup-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) des Objekts Effekte hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectComposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 
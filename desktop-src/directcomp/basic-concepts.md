---
title: Grundlegende Konzepte (DirectComposition)
description: Dieses Thema bietet eine Übersicht über die grundlegenden Konzepte von Microsoft DirectComposition.
ms.assetid: F442BDCA-C913-4438-BFFA-D3F28B68EE85
keywords:
- DirectComposition-Konzepte
- 'DirectComposition: Grundkonzepte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2dadcea55ec18089380d7dbe17d99e5dba92b06dd15774c43cd604f28f991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282030"
---
# <a name="basic-concepts"></a>Grundlegende Konzepte

> [!NOTE]
> Für Apps auf Windows 10 empfiehlt es sich, Windows.UI.Composition-APIs anstelle von DirectComposition zu verwenden. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene.](/windows/uwp/composition/visual-layer-in-desktop-apps)

Dieses Thema bietet eine Übersicht über die grundlegenden Konzepte von Microsoft DirectComposition. Sie enthält die folgenden Abschnitte:

-   [Aufbau](#composition-target-window)
-   [Visuals](#visuals)
    -   [Visuelle Struktur](#visual-tree)
    -   [Eigenschaften eines visuellen Objekts](#properties-of-a-visual-object)
-   [Geräteobjekt](#device-object)
-   [Kompositionszielfenster](#composition-target-window)
-   [Transaktionskomposition](#transactional-composition)
    -   [Batchverarbeitung](#batching)
    -   [Synchronisierung](#synchronization)
    -   [Geräteübergreifende visuelle Strukturen](#cross-device-visual-trees)
-   [Zugehörige Themen](#related-topics)

## <a name="composition"></a>Aufbau

DirectComposition definiert  eine Komposition als Sammlung von Bitmaps, die kombiniert und bearbeitet werden, indem verschiedene Transformationen, Effekte und Animationen verwendet werden, um ein visuelles Ergebnis in einer Anwendungsbenutzeroberfläche zu erzeugen. DirectComposition funktioniert nur mit Bitmapinhalten. Er unterstützt keine Vektoren oder Text. DirectComposition stellt keinen Bitmapinhalt zur Verfügung. Stattdessen werden Schnittstellen bereitgestellt, über die Benutzer mit D2D, DXGI zeichnen oder eigene Texturinhalte hochladen können.

Eine DirectComposition-Anwendung erstellt zwei Sätze von Objekten, um eine Szene zu erstellen: Bitmaps, die zusammen zusammengesetzt sind, und Visuals, die die räumlichen Beziehungen zwischen den Bitmaps definieren. Weitere Informationen zu den bitmap-Objekten, die von DirectComposition unterstützt werden, finden Sie unter [Bitmapobjekte.](bitmap-surfaces.md)

## <a name="visuals"></a>Visuals

*Visuals* (oder *visuelle Objekte)* sind die grundlegenden Elemente von DirectComposition. Sie sind die grundlegenden Bausteine, die Sie zum Erstellen von Kompositionen und Animationen in ihrer Anwendungsbenutzeroberfläche verwenden.

Programmierlich ist ein Visual ein Objekt, das über einen Satz von Eigenschaften verfügt und eine Schnittstelle verfügbar macht, die Sie zum Festlegen des Werts der Eigenschaften verwenden. Die Content-Eigenschaft eines Visuals ordnet dem Visual eine bestimmte Bitmap zu, während andere Eigenschaften steuern, wie DirectComposition das Visual positioniert und bearbeitet, während es auf dem Bildschirm gerendert wird.

Weitere Informationen finden Sie unter [Eigenschaften eines Visuals.](#properties-of-a-visual-object)

### <a name="visual-tree"></a>Visuelle Struktur

DirectComposition erstellt eine Komposition aus einer hierarchischen Auflistung visueller Objekte, die als visuelle *Struktur bezeichnet wird.* Das Visual im Stammverzeichnis einer  Struktur wird als Stammvisu visual bezeichnet und kann einem oder mehrere untergeordnete *Visuals* zugeordnet sein. Ein untergeordnetes Visual kann über ein oder mehrere eigene untergeordnete Visuals verfügen. Jedes Visual, dem untergeordnete Visuals zugeordnet sind, wird als übergeordnetes Visual bezeichnet, und alle untergeordneten Visuals, die dasselbe übergeordnete Element gemeinsam haben, werden als *gleichgeordnete Visuals bezeichnet.* Ein bestimmtes Visual zusammen mit allen untergeordneten und untergeordneten Visuals wird als visuelle *Unterstruktur bezeichnet.*

Die Position eines Visuals in der Struktur hilft dabei, seine Bildschirmposition und Z-Reihenfolge relativ zu den anderen Visuals in der Komposition zu bestimmen. Das Stammvisual wird relativ zur oberen linken Ecke des Clientbereichs des Zielfensters positioniert, in dem die Komposition gerendert wird. Alle untergeordneten Visuals werden relativ zur oberen linken Ecke des übergeordneten Visuals (oder des durch die TransformParent-Eigenschaft angegebenen Visuals) positioniert und immer in der Z-Reihenfolge vor dem übergeordneten Element angezeigt.

Die folgende Abbildung zeigt eine Komposition von Visuals und die Struktur der visuellen Struktur, die zum Erzeugen der Komposition verwendet wird. Visual 1 ist das Stammvisuell und auch das übergeordnete Element der untergeordneten Visuals 2 und 3, bei denen es sich um gleichgeordnete Visuals handelt. Visual 3 verfügt über zwei eigene untergeordnete Visuals: Visuals 4 und 5. Visuals 3 bis 5 bilden zusammen eine visuelle Teilstruktur.

![eine Komposition von Visuals und der entsprechenden visuellen Struktur](images/visuals-and-corresponding-tree.png)

Ein übergeordnetes Visual verwaltet eine geordnete Liste seiner untergeordneten Visuals. Wenn gleichgeordnete Visuals so positioniert sind, dass sie sich überlappen, legt DirectComposition die Z-Reihenfolge der gleichgeordneten Elemente basierend auf der Reihenfolge fest, in der sie in der Liste der übergeordneten Visuellen elemente angezeigt werden. Ein gleichgeordnetes , das später in der Liste angezeigt wird, wird vor allen gleichgeordneten Elemente platziert, die weiter oben in der Liste angezeigt werden. Die folgende Abbildung zeigt die Z-Reihenfolge überlappender untergeordneter Visuals.

![Die Z-Reihenfolge überlappender untergeordneter Visuals](images/overlapping-child-visuals.png)

### <a name="properties-of-a-visual-object"></a>Eigenschaften eines visuellen Objekts

Ein visuelles Objekt macht eine Reihe von Eigenschaften verfügbar, mit denen Sie den Bitmapinhalt für das Visual festlegen und steuern können, wie DirectComposition den visuellen Inhalt positioniert und bearbeitet. In den folgenden Abschnitten wird jede Eigenschaft ausführlich beschrieben.

-   [Inhaltseigenschaft](#content-property)
-   [Clip-Eigenschaft](#clip-property)
-   [BorderMode-Eigenschaft](#bordermode-property)
-   [BitmapInterpolationMode(Eigenschaft)](#bitmapinterpolationmode-property)
-   [CompositeMode-Eigenschaft](#compositemode-property)
-   [OffsetX- und OffsetY-Eigenschaften](#offsetx-and-offsety-properties)
-   [Effect-Eigenschaft](#effect-property)
-   [Transform-Eigenschaft](#transform-property)
-   [TransformParent-Eigenschaft](#transformparent-property)

### <a name="content-property"></a>Inhaltseigenschaft

Die Content-Eigenschaft eines Visuals gibt den Bitmapinhalt an, der dem Visual zugeordnet ist. Dies ist die Bitmap, die DirectComposition verwendet, wenn Sie das Visual in eine Komposition einordnen.

Sie legen die Content-Eigenschaft eines Visuals fest, indem Sie die [**IDCompositionVisual::SetContent-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) aufrufen.

Weitere Informationen zu den Typen von Bitmapinhalten, die von DirectComposition unterstützt werden, finden Sie unter [Bitmapobjekte](bitmap-surfaces.md).

### <a name="clip-property"></a>Clip-Eigenschaft

Die Clip-Eigenschaft eines Visuals gibt einen rechteckigen Bereich an, der als *Ausschneidebereich* (oder Cliprechteck) *bezeichnet wird.* Wenn ein Visual gerendert wird, wird nur der Teil des Visuals angezeigt, der in den Ausschneidebereich fällt, während alle Inhalte, die sich außerhalb des Ausschneidebereichs befinden, abgeschnitten werden (d. h. nicht angezeigt). DirectComposition unterstützt Clipping-Bereiche, die abgerundete oder quadratische Ecken haben.

Sie legen die Clip-Eigenschaft eines Visuals fest, indem Sie die [**IDCompositionVisual::SetClip-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) aufrufen.

Weitere Informationen finden Sie unter [Clipping](clipping.md).

### <a name="bordermode-property"></a>BorderMode-Eigenschaft

Die BorderMode-Eigenschaft gibt an, wie die Ränder von Bitmaps und Clips, die diesem Visual zugeordnet sind, oder mit Visuals in der Teilstruktur, die mit diesem Visual verknüpft sind, erstellt werden.

Der Rahmenmodus wirkt sich darauf aus, wie die Ränder einer Bitmap zusammengesetzt werden, wenn die Bitmap so transformiert wird, dass die Kanten nicht an ganzzahligen Koordinaten ausgerichtet sind. Sie wirkt sich auch darauf aus, wie Inhalte an den Ecken eines Clips mit abgerundeten Ecken abgeschnitten werden und wie am Rand eines Clips, der so transformiert wird, dass die Kanten nicht an ganzzahligen Koordinaten ausgerichtet sind.

Weitere Informationen finden Sie unter [**IDCompositionVisual::SetBorderMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode).

### <a name="bitmapinterpolationmode-property"></a>BitmapInterpolationMode(Eigenschaft)

Die BitmapInterpolationMode-Eigenschaft teilt DirectComposition mit, wie eine Bitmap erstellt wird, wenn sie transformiert wird, damit keine 1:1-Entsprechung zwischen Pixeln in der Bitmap und Pixeln auf dem Bildschirm besteht.

Sie legen die BitmapInterpolationMode-Eigenschaft eines Visuals fest, indem Sie die [**IDCompositionVisual::SetBitmapInterpolationMode-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode) aufrufen.

### <a name="compositemode-property"></a>CompositeMode-Eigenschaft

Die CompositeMode-Eigenschaft teilt DirectComposition mit, wie der Bitmapinhalt eines Visuals mit dem Renderziel kombiniert werden soll. Eine Beschreibung der unterstützten zusammengesetzten Modi finden Sie unter [**DCOMPOSITION \_ COMPOSITE \_ MODE**](/windows/desktop/api/DcompTypes/ne-dcomptypes-dcomposition_composite_mode).

Sie legen die CompositeMode-Eigenschaft eines Visuals fest, indem Sie die [**IDCompositionVisual::SetCompositeMode-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode) aufrufen.

### <a name="offsetx-and-offsety-properties"></a>OffsetX- und OffsetY-Eigenschaften

Die Eigenschaften OffsetX und OffsetY teilen DirectComposition mit, wo ein Visual horizontal und vertikal positioniert werden soll. Sie definieren die zweidimensionale feste Position, von der alle Transformationen und Effekte für das Visual berechnet werden.

Für ein Stammvisual definieren die OffsetX- und OffsetY-Eigenschaften die x-Koordinate und die y-Koordinate eines Punkts relativ zur oberen linken Ecke des Fensters, das das Visual hostet. Bei einem untergeordneten Visual sind die Koordinaten relativ zur oberen linken Ecke des übergeordneten Elements oder, wenn die [TransformParent-Eigenschaft](#transformparent-property) angegeben ist, die obere linke Ecke des angegebenen Visuals. Wenn ein Visual gerendert wird, wird es so positioniert, dass die obere linke Ecke des Visuals mit den angegebenen Koordinaten zusammenschneidet.

Sie legen die OffsetX- und OffsetY-Eigenschaften eines Visuals fest, indem Sie die [**Methoden IDCompositionVisual::SetOffsetX**](/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)) und [**SetOffsetY**](/previous-versions/windows/desktop/legacy/hh449131(v=vs.85)) aufrufen.

### <a name="effect-property"></a>Effect-Eigenschaft

Mit der Effect-Eigenschaft können Sie einen Effekt oder eine Gruppe von Effekten angeben, der die Zusammengestelltung eines Visuals und seiner Unterstruktur ändert. Beispielsweise können Sie Effekte angeben, die die Deckkraft eines Visuals steuern, das Visual auf verschiedene Weise mit einer anderen Bitmap mischen und Perspektiventransformationen auf das Visual anwenden.

Sie legen die Effect-Eigenschaft eines Visuals fest, indem Sie die [**IDCompositionVisual::SetEffect-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) aufrufen.

Weitere Informationen finden Sie unter [Effekte](effects.md).

### <a name="transform-property"></a>Transform-Eigenschaft

Die Transform-Eigenschaft gibt eine zweidimensionale Transformation (2D) oder eine Gruppe von 2D-Transformationen an, die DirectComposition für das Visual ausführen soll. Eine Transformation (oder Transformation) ist ein Vorgang, der das Koordinatensystem eines Visuals relativ zum übergeordneten Element oder relativ zu dem visual ändert, das von der [TransformParent-Eigenschaft angegeben wird.](#transformparent-property) Sie können Transformationen verwenden, um die Position, Größe oder Art eines Visuals zu ändern, indem Sie es an eine andere Position verschieben (Übersetzung), es vergrößern oder verkleinern (skalieren), es drehen (Drehung), seine Form verzerren (Skewing) und so weiter.

Sie legen die Transform-Eigenschaft eines Visuals fest, indem Sie die [**IDCompositionVisual::SetTransform-Methode**](/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)) aufrufen.

Weitere Informationen finden Sie unter [Transformationen](transforms.md).

### <a name="transformparent-property"></a>TransformParent-Eigenschaft

Das Koordinatensystem eines Visuals wird durch die Eigenschaften OffsetX, OffsetY und Transform geändert. Normalerweise definieren diese Eigenschaften das Koordinatensystem eines Visuals relativ zu seinem unmittelbar übergeordneten Element. Um ein anderes visuelles Element als das übergeordnete Element als Grundlage für das Koordinatensystem eines untergeordneten Visuals zu verwenden, verwenden Sie die TransformParent-Eigenschaft, um ein anderes Visual als "übergeordnetes Element" für Transformationszwecke anzugeben.

Sie legen die TransformParent-Eigenschaft eines Visuals fest, indem Sie die [**IDCompositionVisual::SetTransformParent-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent) aufrufen.

## <a name="device-object"></a>Geräteobjekt

Um DirectComposition verwenden zu können, müssen Sie eine Vielzahl von COMPONENT OBJECT MODEL (COM)-Objekten erstellen und bearbeiten. Das erste Objekt, das Sie erstellen  müssen, ist das DirectComposition-Geräteobjekt, da es als Factory zum Erstellen aller anderen Objekte dient, die in einer Komposition verwendet werden.

Sie erstellen ein Geräteobjekt, indem Sie die [**DCompositionCreateDevice-Funktion**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) aufrufen, die einen [**IDCompositionDevice-Schnittstellenzeiger**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) zurückgibt. Diese Schnittstelle macht eine Reihe von Methoden verfügbar, mit denen Sie visuelle Objekte, Clipobjekte, Animationsobjekte, Transformationsobjekte, Effektobjekte und so weiter erstellen.

Das Geräteobjekt dient einem anderen Zweck als einer Factory zum Erstellen anderer Objekte. Es macht eine Methode namens [**Commit verfügbar,**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) die eine visuelle Struktur zur Verarbeitung an DirectComposition übergibt. Weitere Informationen finden Sie unter [Transactional Composition](#transactional-composition).

Denken Sie daran, dass Sie zwar mehrere Instanzen des Geräteobjekts in Ihrer Anwendung erstellen können, aber alle Objekte, die Sie in einer bestimmten Komposition verwenden, von demselben Geräteobjekt erstellt werden müssen – mit einer Ausnahme: Sie können visuelle Objekte aus verschiedenen Geräteobjekten in derselben visuellen Struktur kombinieren. In diesem Fall behandelt DirectComposition die visuelle Struktur wie gewohnt, außer dass Änderungen an einem bestimmten visuellen Objekt in der Struktur nur wirksam werden, wenn die [**Commit-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) für das Geräteobjekt aufgerufen wird, das das visuelle Objekt erstellt hat.

Die Möglichkeit, Visuals von verschiedenen Geräten in derselben visuellen Struktur zu verwenden, ermöglicht es mehreren Threads, eine einzelne visuelle Struktur zu erstellen und zu bearbeiten, während zwei unabhängige Geräte beibehalten werden, die zum asynchronen Commit von Änderungen verwendet werden können. Weitere Informationen finden Sie unter [Geräteübergreifende visuelle Strukturen.](#cross-device-visual-trees)

## <a name="composition-target-window"></a>Kompositionszielfenster

Eine visuelle Struktur muss an ein Fenster gebunden werden, bevor eines der visuellen Elemente der Struktur auf dem Bildschirm angezeigt werden kann. Das Fenster, das als *Kompositionszielfenster* bezeichnet wird, kann ein Fenster der obersten Ebene oder ein untergeordnetes Fenster sein. Außerdem kann das Kompositionszielfenster ein mehrschichtiges Fenster sein. Das heißt, es kann den [**WS \_ EX \_ LAYERED-Fensterstil**](/windows/desktop/winmsg/extended-window-styles) haben.

DirectComposition ermöglicht es einer Anwendung, maximal zwei visuelle Strukturen an jedes Fenster zu binden. Die visuellen Strukturen enthalten eine , die über dem Fenster selbst, aber hinter allen untergeordneten Fenstern des Fensters zusammengesetzt ist, und eine andere, die über dem Fenster und über den untergeordneten Fenstern zusammengesetzt ist. Anders ausgedrückt: Jedes Fenster verfügt über vier konzeptionelle Ebenen, und alle Ebenen werden an den sichtbaren Bereich des Zielfensters abgeschnitten. Die folgende Abbildung zeigt die vier konzeptionellen Ebenen eines Fensters.

![die konzeptionellen Ebenen eines Fensters](images/directcomposition-layers.png)

## <a name="transactional-composition"></a>Transaktionskomposition

DirectComposition verwendet ein Transaktionsmodell, bei dem Sie einen Batchsatz von Änderungen an einem Visual erstellen und dann den Satz auf DirectComposition für die Verarbeitung auf einmal "commiten". Sie können dasselbe visuelle DirectComposition-Objekt ändern und die Änderungen mit einer beliebigen Anzahl von Commits vornehmen. Wenn der Desktopfenster-Manager (DWM) Batches auffängt, werden alle ausstehenden Batches in der Reihenfolge, in der sie ausgeführt wurden, auf den nächsten Frame angewendet.

Alle Änderungen innerhalb eines einzelnen Commits werden garantiert auf einen einzelnen Frame angewendet. Da DWM Batches einmal pro Frame sammelt, können Sie jedes bestimmte Objekt nur einmal pro Frame ändern. Nachfolgende Commits, die verschiedene Objekte ändern, können auch auf den aktuellen Frame angewendet werden. DirectComposition garantiert jedoch nicht, dass die Änderungen im gleichen Frame auftreten.

Mit [**den Methoden IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) und [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) können Sie Renderingupdates mit visuellen Updates synchronisieren. Sie können beispielsweise **IDCompositionSurface::BeginDraw** aufrufen, die OffsetX- und Clip-Eigenschaften eines Visuals aktualisieren, [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)aufrufen, Inhalt mit Microsoft DirectX zeichnen und dann **IDCompositionSurface::EndDraw aufrufen.** In diesem Fall stellt Microsoft DirectComposition sicher, dass bitmap-Inhalt und die visuellen Eigenschaften gleichzeitig aktualisiert werden.

### <a name="batching"></a>Batching

Sie können mehrere Änderungen an demselben Visual oder mehrere Änderungen an verschiedenen Visuals innerhalb desselben Frames commiten. Wenn Sie mehrere Änderungen am gleichen Visual innerhalb desselben Frames vornehmen, beachten Sie folgende Punkte:

-   Wenn Sie mehrere Änderungen an derselben Eigenschaft eines Visuals vornehmen, wird nur die letzte Änderung angewendet. Wenn Sie beispielsweise die Deckkraft auf 0, dann auf 0,5 und schließlich auf 1,0 festlegen, wird nur eine Deckkraft von 1,0 auf das Visual angewendet.
-   Wenn Sie mehrere Eigenschaften desselben Visuals ändern, wendet DirectComposition die Änderungen zuerst auf das Visual und dann auf alle untergeordneten Visuals an. Die Eigenschaften werden unabhängig von der Reihenfolge, in der Sie sie angeben, in der folgenden Reihenfolge angewendet:

    1.  Offset
    2.  Transformieren
    3.  Abschneiden
    4.  Auswirkung

    Die folgende Abbildung zeigt das Ergebnis der Anwendung aller vier Eigenschaften auf ein Visual.

    ![Ergebnis der Anwendung aller vier Eigenschaften auf ein Visual](images/order-of-properties.png)

    Denken Sie daran, dass alle Änderungen gleichzeitig im Kontext desselben Frames auf das Visual angewendet werden. Dies bedeutet, dass die Änderungen am Visual aus Sicht des Benutzers sofort erfolgen.

-   Für die Transform-Eigenschaft können Sie [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) verwenden, um eine Gruppe von Transformationen zu erstellen, die auf ein Visual gleichzeitig angewendet werden. DirectComposition wendet die Transformationen in der von Ihnen angegebenen Reihenfolge an.
-   Für die Effect-Eigenschaft können Sie [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) verwenden, um eine Gruppe von Effekten anzuwenden. DirectComposition wendet die Effekte in der von Ihnen angegebenen Reihenfolge an. Darüber hinaus führen 3D-Perspektiventransformationen zu einer Flachung der visuellen Struktur, nachdem alle 3D-Transformationen im aktuellen Visual angewendet wurden. Dadurch wird sichergestellt, dass das resultierende Visual so nah wie möglich an 3D aussieht.

### <a name="synchronization"></a>Synchronisierung

Ihre Anwendung kann DirectComposition aus mehreren Threads gleichzeitig aufrufen. Die Ausführungsrichtung ist für sequenzielle Aufrufe garantiert, jedoch nicht für gleichzeitige Aufrufe. Wenn z. B. Thread A ein Visual ändert und Thread B gleichzeitig einen Commit für den Batch ausgeführt, ist nicht definiert, ob diese visuelle Änderung im Commitbatch enthalten ist oder ob ein neuer Batch gestartet wird. Wenn Ihre Anwendung andererseits andere Synchronisierungsmechanismen verwendet, um sicherzustellen, dass eine Methode vor der anderen aufgerufen wird, wird die Aufruf reihenfolge von DirectComposition als verarbeitet, als ob beide Aufrufe in dieser Reihenfolge von einem einzelnen Thread ausgegeben würden.

### <a name="cross-device-visual-trees"></a>Geräteübergreifende visuelle Strukturen

DirectComposition-Objekte sind nicht threadgebunden. Sie können mehrere Threads verwenden, um denselben Satz von Objekten zu ändern. Beachten Sie jedoch die folgenden Probleme, wenn Sie dasselbe Geräteobjekt freigeben.

-   Beide Threads müssen [**IDCompositionDevice::Commit aufrufen können.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) Wenn nur einer der Threads **IDCompositionDevice::Commit** aufruft, kann der andere Thread keine Änderungen an DirectComposition ausführen.
-   Transaktionsverhalten kann verloren gehen, wenn ein Thread [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) aufruft, während der andere Thread weiterhin Änderungen vorsteuert, die Teil derselben Transaktion sein sollen.

Wenn Sie mehrere gleichzeitige Transaktionen für DirectComposition ausführen müssen, müssen Sie mehrere Geräteobjekte verwenden, möglicherweise aus mehreren Threads. In diesem Szenario wird dieselbe visuelle Struktur von beiden Geräteobjekten gemeinsam genutzt, und jedes Geräteobjekt committ seine eigenen Transaktionen.

Die folgende Abbildung zeigt eine visuelle Struktur, die von zwei Geräteobjekten gemeinsam genutzt wird. Visuals 1, 2, 4 und 5 befinden sich im Besitz des einen oder des anderen Geräts, visual 3 wird jedoch von beiden Geräten gemeinsam genutzt und kann daher verwendet werden, um zwei Unterstrukturen in einer einzelnen, größeren visuellen Struktur zu verbinden. Durch das Freigeben der visuellen Struktur können die beiden Geräte asynchron aus zwei verschiedenen Threads bearbeitet werden.

![eine visuelle Struktur, die von zwei Geräten gemeinsam genutzt wird](images/shared-visual-tree-1.png)

Um die Nützlichkeit der Gemeinsamen Nutzung einer visuellen Struktur zwischen zwei Geräten zu veranschaulichen, sollten Sie eine Architektur in Betracht ziehen, die Toucheingaben mit geringer Latenz ermöglicht. Die Architektur könnte zwei Threads verwenden, einen, der die meisten Benutzeroberflächenaufgaben verarbeitet, und einen zweiten Thread, der für die Verarbeitung von Toucheingabeereignissen entwickelt wurde. Der Touchthread aktualisiert die Transformation eines bestimmten Visuals basierend auf der Benutzereingabegeste. Durch Aktualisieren der Transformation kann der Touchthread die gesamte Teilstruktur unter diesem Visual dem Finger des Benutzers folgen, hoch- oder herunterskalieren, während der Benutzer eine Multi-Touch-Geste ausgeführt hat, und so weiter. Der UI-Thread behält den Großteil der Kompositionsstruktur, und der Touchthread besitzt nur die wenigen Visuals, die für die asynchrone Touchantwort gekennzeichnet sind. Die folgende Abbildung zeigt eine vereinfachte Version einer solchen Kompositionsstruktur:

![Eine visuelle Struktur, die von einem Ui-Thread und einem Touchthread gemeinsam genutzt wird](images/shared-visual-tree-2.png)

In der Regel ändert der UI-Thread nur die Visuals, die er ausschließlich besitzt, und der Touchthread ändert nur das freigegebene Visual. Die einzige Ausnahme tritt auf, wenn eine Touch-aktivierte Teilstruktur erstellt oder zerstört wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)
</dt> <dt>

[**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)
</dt> <dt>

[**IDCompositonDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[DirectComposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 
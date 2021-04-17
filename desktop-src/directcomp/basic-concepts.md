---
title: Grundlegende Konzepte (directcomposition)
description: Dieses Thema enthält eine Übersicht über die grundlegenden Konzepte von Microsoft directcomposition.
ms.assetid: F442BDCA-C913-4438-BFFA-D3F28B68EE85
keywords:
- Directcomposition-Konzepte
- Grundlegende Konzepte von directcomposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0550dc12cb0dcc5262701658d8e3883ee1ce8d82
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104553506"
---
# <a name="basic-concepts"></a>Grundlegende Konzepte

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

Dieses Thema enthält eine Übersicht über die grundlegenden Konzepte von Microsoft directcomposition. Sie enthält die folgenden Abschnitte:

-   [Aufbau](#composition-target-window)
-   [Visuals](#visuals)
    -   [Visuelle Struktur](#visual-tree)
    -   [Eigenschaften eines visuellen Objekts](#properties-of-a-visual-object)
-   [Geräteobjekt](#device-object)
-   [Fenster "Kompositions Ziel"](#composition-target-window)
-   [Transaktionale Komposition](#transactional-composition)
    -   [Batching](#batching)
    -   [Synchronisierung](#synchronization)
    -   [Geräte übergreifende visuelle Strukturen](#cross-device-visual-trees)
-   [Zugehörige Themen](#related-topics)

## <a name="composition"></a>Aufbau

Directcomposition definiert eine *Komposition* als eine Auflistung von Bitmaps, die kombiniert und bearbeitet werden, indem verschiedene Transformationen, Effekte und Animationen angewendet werden, um ein visuelles Ergebnis in einer Anwendungs Benutzeroberfläche zu erzeugen. Directcomposition funktioniert nur mit Bitmapinhalt. Vektoren oder Text werden nicht unterstützt. Directcomposition stellt keinen Bitmapinhalt bereit. Stattdessen werden Schnittstellen bereitstellen, in denen Benutzer mit D2D, DXGI oder ihren eigenen Textur Inhalt zeichnen können.

Eine directcomposition-Anwendung erstellt zwei Sätze von Objekten, um eine Szene zu verfassen: Bitmaps, die zusammengesetzt werden, und visuelle Elemente, die die räumlichen Beziehungen zwischen den Bitmaps definieren. Weitere Informationen zu den bitmapobjekten, die von directcomposition unterstützt werden, finden Sie unter [Bitmap-Objekte](bitmap-surfaces.md).

## <a name="visuals"></a>Visuals

*Visualisierungen* (oder *visuelle Objekte*) sind die grundlegenden Elemente von directcomposition. Dabei handelt es sich um die grundlegenden Bausteine, die Sie zum Erstellen von Kompositionen und Animationen in der Benutzeroberfläche Ihrer Anwendung verwenden.

In Programmier begriffen ist ein visuelles Objekt ein Objekt, das über einen Satz von Eigenschaften verfügt und eine Schnittstelle verfügbar macht, mit der Sie den Wert der Eigenschaften festlegen können. Die Content-Eigenschaft eines visuellen Elements ordnet eine bestimmte Bitmap dem visuellen Element zu, während andere Eigenschaften steuern, wie directcomposition die Visualisierung positioniert und bearbeitet, während Sie auf dem Bildschirm gerendert wird.

Weitere Informationen finden Sie unter [Eigenschaften eines visuellen](#properties-of-a-visual-object)Elements.

### <a name="visual-tree"></a>Visuelle Struktur

Directcomposition erstellt eine Komposition aus einer hierarchischen Auflistung von visuellen Objekten, die als *visuelle* Struktur bezeichnet werden. Das visuelle Element im Stammverzeichnis einer Struktur wird als Stamm Element bezeichnet und kann einem *oder mehreren unter* *geordneten visuellen Elementen* zugeordnet werden. Ein untergeordnetes visuelles Element kann über ein oder mehrere untergeordnete Visuals verfügen. Alle visuellen Elemente, die über zugeordnete untergeordnete Visualisierungen verfügen, werden als über *geordnete* *Visualisierung bezeichnet* Eine bestimmte Visualisierung wird zusammen mit allen untergeordneten und nachfolgenden visuellen Elementen als *visuelle Unterstruktur* bezeichnet.

Die Position eines visuellen Elements in der Struktur hilft bei der Bestimmung der Bildschirmposition und der z-Reihenfolge in Bezug auf die anderen visuellen Elemente in der Komposition. Das visuelle Stamm Element wird relativ zur oberen linken Ecke des Client Bereichs des Zielfensters positioniert, in dem die Komposition gerendert wird. Alle untergeordneten visuellen Elemente werden relativ zur oberen linken Ecke des übergeordneten visuellen Elements (oder der durch die transformparent-Eigenschaft angegebenen Visualisierung) positioniert und vor dem übergeordneten Element in der z-Reihenfolge angezeigt.

Die folgende Abbildung zeigt eine Zusammensetzung der visuellen Elemente und die Struktur der visuellen Struktur, mit der die Komposition erzeugt wird. Visual 1 ist das visuelle Stamm Element und auch das übergeordnete Element der untergeordneten visuellen Elemente 2 und 3, bei denen es sich um gleich geordnete Visuals handelt. Visual 3 verfügt über zwei eigene untergeordnete Visuals, Visuals 4 und 5. In der Gesamtheit bilden die Visualisierungen 3 bis 5 eine visuelle Unterstruktur.

![eine Komposition von visuellen Elementen und der entsprechenden visuellen Struktur](images/visuals-and-corresponding-tree.png)

Eine übergeordnete Visualisierung behält eine geordnete Liste der untergeordneten visuellen Elemente bei. Wenn gleich geordnete visuelle Elemente so positioniert sind, dass Sie einander überlappen, legt directcomposition die z-Reihenfolge der gleich geordneten Elemente basierend auf der Reihenfolge fest, in der Sie in der Liste der untergeordneten Elemente der übergeordneten Visualisierung angezeigt werden. Ein gleich geordnetes Element, das später in der Liste angezeigt wird, wird vor allen neben geordneten Elementen platziert, die zuvor in der Liste angezeigt werden. Die folgende Abbildung zeigt die z-Reihenfolge der überlappenden untergeordneten Visuals.

![die z-Reihenfolge der überlappenden untergeordneten Visuals](images/overlapping-child-visuals.png)

### <a name="properties-of-a-visual-object"></a>Eigenschaften eines visuellen Objekts

Ein visuelles Objekt macht eine Reihe von Eigenschaften verfügbar, die es Ihnen ermöglichen, den Bitmapinhalt für das visuelle Element festzulegen und zu steuern, wie directcomposition den visuellen Inhalt positioniert und bearbeitet. In den folgenden Abschnitten werden die einzelnen Eigenschaften ausführlich beschrieben.

-   [Inhaltseigenschaft](#content-property)
-   [Clip-Eigenschaft](#clip-property)
-   [Bordermode-Eigenschaft](#bordermode-property)
-   [Bitmapinterpolationmode (Eigenschaft)](#bitmapinterpolationmode-property)
-   [Compositemode-Eigenschaft](#compositemode-property)
-   [OffsetX-und OffsetY-Eigenschaften](#offsetx-and-offsety-properties)
-   [Effect-Eigenschaft](#effect-property)
-   [Transform-Eigenschaft](#transform-property)
-   [Transformparent-Eigenschaft](#transformparent-property)

### <a name="content-property"></a>Inhaltseigenschaft

Die Content-Eigenschaft eines visuellen Elements gibt den Bitmapinhalt an, der dem visuellen Element zugeordnet ist. Dies ist die Bitmap, die directcomposition verwendet, wenn Sie das visuelle Element in eine Komposition einschließen.

Sie legen die Content-Eigenschaft eines visuellen Elements fest, indem Sie die [**idcompositionvisual:: setContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) -Methode aufrufen.

Weitere Informationen zu den Typen von Bitmapinhalten, die von directcomposition unterstützt werden, finden Sie unter [Bitmap-Objekte](bitmap-surfaces.md).

### <a name="clip-property"></a>Clip-Eigenschaft

Die Clip-Eigenschaft eines visuellen Elements gibt einen rechteckigen Bereich an, der als *Clippingbereich* (oder *Clip Rechteck*) bezeichnet wird. Wenn ein visuelles Element gerendert wird, wird nur der Teil des visuellen Elements angezeigt, der in den Ausschneide Bereich fällt, während alle Inhalte, die sich außerhalb des Clippingbereichs befinden, abgeschnitten werden (d. h. nicht angezeigt). Directcomposition unterstützt Clippingbereiche, die über abgerundete oder quadratische Ecken verfügen.

Sie legen die Clip-Eigenschaft eines visuellen Elements fest, indem Sie die [**idcompositionvisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) -Methode aufrufen.

Weitere Informationen finden Sie unter [Clipping](clipping.md).

### <a name="bordermode-property"></a>Bordermode-Eigenschaft

Die bordermode-Eigenschaft gibt an, wie die Ränder von Bitmaps und mit dieser Visualisierung verknüpften Clips oder mit visuellen Elementen in der Teilstruktur, die auf diesem visuellen Element liegt, zusammengesetzt werden.

Der Border-Modus wirkt sich darauf aus, wie die Ränder einer Bitmap zusammengesetzt werden, wenn die Bitmap so transformiert wird, dass die Ränder nicht an ganzzahligen Koordinaten ausgerichtet sind. Er wirkt sich auch darauf aus, wie der Inhalt an den Ecken eines Clips mit abgerundeten Ecken abgeschnitten wird, und am Rand eines Clips, der transformiert wird, sodass die Ränder nicht an ganzzahlige Koordinaten ausgerichtet sind.

Weitere Informationen finden Sie unter [**idcompositionvisual:: setbordermode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode).

### <a name="bitmapinterpolationmode-property"></a>Bitmapinterpolationmode (Eigenschaft)

Die bitmapinterpolationmode-Eigenschaft weist directcomposition an, eine Bitmap zu verfassen, wenn Sie transformiert wird, sodass keine 1:1-Entsprechung zwischen Pixeln in der Bitmap und Pixel auf dem Bildschirm vorhanden ist.

Sie legen die bitmapinterpolationmode-Eigenschaft eines visuellen Elements fest, indem Sie die [**idcompositionvisual:: setbitmapinterpolationmode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode) -Methode aufrufen.

### <a name="compositemode-property"></a>Compositemode-Eigenschaft

Die compositemode-Eigenschaft teilt directcomposition mit, wie der Bitmapinhalt eines visuellen Elements mit dem Renderziel kombiniert werden soll. Eine Beschreibung der unterstützten zusammengesetzten Modi finden Sie unter [**dcomposition \_ Composite \_ Mode**](/windows/desktop/api/DcompTypes/ne-dcomptypes-dcomposition_composite_mode).

Sie legen die compositemode-Eigenschaft eines visuellen Elements fest, indem Sie die [**idcompositionvisual:: setcompositemode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode) -Methode aufrufen.

### <a name="offsetx-and-offsety-properties"></a>OffsetX-und OffsetY-Eigenschaften

Die Eigenschaften OffsetX und OffsetY weisen directcomposition an, wo eine Visualisierung horizontal und vertikal positioniert werden soll. Sie definieren die zweidimensionale festgelegte Position, von der alle Transformationen und Effekte für das visuelle Element berechnet werden.

Für eine visuelle Stamm Visualisierung definieren die OffsetX-Eigenschaft und die OffsetY-Eigenschaft die x-Koordinate und die y-Koordinate eines Punkts in Relation zur oberen linken Ecke des Fensters, das die Visualisierung hostet. Bei einem untergeordneten visuellen Element sind die Koordinaten relativ zur linken oberen Ecke des übergeordneten Elements, oder, wenn die [transformparent-Eigenschaft](#transformparent-property) angegeben ist, die obere linke Ecke des angegebenen visuellen Elements. Wenn ein visuelles Element gerendert wird, wird es so positioniert, dass die obere linke Ecke des visuellen Elements mit den angegebenen Koordinaten übereinstimmt.

Sie legen die Eigenschaften OffsetX und OffsetY eines visuellen Elements fest, indem Sie die [**idcompositionvisual:: setoffsetx**](/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)) -und [**setoffsety**](/previous-versions/windows/desktop/legacy/hh449131(v=vs.85)) -Methode aufrufen.

### <a name="effect-property"></a>Effect-Eigenschaft

Mit der Eigenschaft "Effect" können Sie einen Effekt oder eine Gruppe von Effekten angeben, mit dem die Zusammensetzung eines visuellen Elements und seiner Unterstruktur geändert wird. Sie können z. b. Effekte angeben, die die Deckkraft eines visuellen Elements steuern, das visuelle Element mit einer anderen Bitmap auf verschiedene Weise kombinieren und perspektivische Transformationen auf die Visualisierung anwenden.

Sie legen die Effect-Eigenschaft eines visuellen Elements fest, indem Sie die [**idcompositionvisual:: SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) -Methode aufrufen.

Weitere Informationen finden Sie unter [Effekte](effects.md).

### <a name="transform-property"></a>Transform-Eigenschaft

Die Transform-Eigenschaft gibt eine zweidimensionale (2D) Transformation oder eine Gruppe von 2D-Transformationen an, damit directcomposition für das visuelle Element durchgeführt wird. Eine Transformation (oder Transformation) ist ein Vorgang, der das Koordinatensystem eines visuellen Elements relativ zu seinem übergeordneten Element oder relativ zu dem durch die [transformparent-Eigenschaft](#transformparent-property)angegebenen visuellen Element ändert. Mithilfe von Transformationen können Sie die Position, die Größe oder die Art eines visuellen Elements ändern, indem Sie es an eine andere Position (Übersetzung) verschieben, die Größe vergrößern oder verkleinern (Skalieren), Sie drehen (Drehen), ihre Form verzerrt (schieden) und so weiter.

Sie legen die Transform-Eigenschaft eines visuellen Elements fest, indem Sie die [**idcompositionvisual:: setTransform**](/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)) -Methode aufrufen.

Weitere Informationen finden Sie unter [Transformationen](transforms.md).

### <a name="transformparent-property"></a>Transformparent-Eigenschaft

Das Koordinatensystem eines visuellen Elements wird durch die Eigenschaften OffsetX, OffsetY und Transform geändert. Normalerweise definieren diese Eigenschaften das Koordinatensystem eines visuellen Elements relativ zu seinem unmittelbar übergeordneten Element. Wenn Sie ein anderes visuelles Element als das übergeordnete Element als Grundlage für das Koordinatensystem eines untergeordneten visuellen Elements verwenden möchten, verwenden Sie die transformparent-Eigenschaft, um für Transformations Zwecke ein anderes visuelles Element als "übergeordnetes Element" anzugeben.

Sie legen die transformparent-Eigenschaft eines visuellen Elements fest, indem Sie die [**idcompositionvisual:: settransformparent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent) -Methode aufrufen.

## <a name="device-object"></a>Geräteobjekt

Um directcomposition verwenden zu können, müssen Sie eine Vielzahl von Component Object Model (com)-Objekten erstellen und bearbeiten. Das erste Objekt, das Sie erstellen müssen, ist das directcomposition- *Geräte Objekt* , da es als Factory zum Erstellen aller anderen Objekte dient, die in einer Komposition verwendet werden.

Sie erstellen ein Geräte Objekt, indem Sie die [**dcompositioncreatedevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) -Funktion aufrufen, die einen [**idcompositiondevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) -Schnittstellen Zeiger zurückgibt. Diese Schnittstelle stellt einen Satz von Methoden zur Verfügung, mit denen Sie visuelle Objekte erstellen, Objekte Ausschneiden, Objekte, Objekte transformieren, Objekte transformieren können usw.

Das Geräte Objekt dient einem anderen Zweck, abgesehen von einer Factory zum Erstellen anderer Objekte. Sie macht eine Methode namens [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) verfügbar, die eine visuelle Struktur zur Verarbeitung an directcomposition übergibt. Weitere Informationen finden Sie unter [transaktionale Komposition](#transactional-composition).

Wenn Sie mehrere Instanzen des Geräte Objekts in der Anwendung erstellen können, müssen alle Objekte, die Sie in einer bestimmten Komposition verwenden, vom gleichen Geräte Objekt erstellt werden – mit einer Ausnahme: Sie können visuelle Objekte aus verschiedenen Geräte Objekten in derselben visuellen Struktur kombinieren. Wenn Sie dies tun, behandelt directcomposition die visuelle Struktur wie gewohnt, mit dem Unterschied, dass Änderungen an einem bestimmten visuellen Objekt in der Struktur nur wirksam werden, wenn die [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) -Methode für das Geräte Objekt aufgerufen wird, das das visuelle Objekt erstellt hat.

Die Möglichkeit, visuelle Elemente von verschiedenen Geräten in derselben visuellen Struktur zu verwenden, ermöglicht es mehreren Threads, eine einzelne visuelle Struktur zu erstellen und zu bearbeiten und gleichzeitig zwei unabhängige Geräte zu verwalten, die zum asynchronen Ausführen von Änderungen verwendet werden können. Weitere Informationen finden Sie unter [Geräte übergreifende visuelle](#cross-device-visual-trees)Struktur.

## <a name="composition-target-window"></a>Fenster "Kompositions Ziel"

Eine visuelle Struktur muss an ein Fenster gebunden werden, bevor eine der visuellen Elemente der Struktur auf dem Bildschirm angezeigt werden kann. Das Fenster, das als *Kompositions Zielfenster* bezeichnet wird, kann ein Fenster der obersten Ebene oder ein untergeordnetes Fenster sein. Außerdem kann das Zusammenfassungs Zielfenster ein geschichtetes Fenster sein. Das heißt, er kann über das Fenster " [**WS \_ Ex \_**](/windows/desktop/winmsg/extended-window-styles) -Fenster" verfügen.

Directcomposition ermöglicht es einer Anwendung, maximal zwei visuelle Strukturen an jedes Fenster zu binden. Die visuellen Strukturen enthalten ein Element, das sich auf dem Fenster selbst, aber hinter allen untergeordneten Fenstern des Fensters und einem weiteren Element befindet, das sich oberhalb des Fensters und oberhalb der untergeordneten Fenster zusammensetzt. Das heißt, jedes Fenster hat vier konzeptionelle Ebenen, und alle Ebenen werden auf den sichtbaren Bereich des Zielfensters zugeschnitten. Die folgende Abbildung zeigt die vier konzeptionellen Ebenen eines Fensters.

![die konzeptionellen Ebenen eines Fensters](images/directcomposition-layers.png)

## <a name="transactional-composition"></a>Transaktionale Komposition

Directcomposition verwendet ein transaktionales Modell, in dem Sie einen Batch Satz von Änderungen an einem visuellen Element erstellen und dann die Menge auf directcomposition für die gleichzeitige Verarbeitung "übertragen". Sie können dasselbe directcomposition-visuelle Objekt ändern und die Änderungen beliebig oft übernehmen. Wenn die Desktopfenster-Manager (DWM) Batches aufnimmt, werden alle ausstehenden Batches übernommen und auf den nächsten Frame in der Reihenfolge angewendet, in der Sie ein Commit ausgeführt haben.

Alle Änderungen innerhalb eines einzelnen Commit werden garantiert auf einen einzelnen Frame angewendet. Da DWM Batches einmal pro Frame sammelt, können Sie ein bestimmtes Objekt nur einmal pro Rahmen ändern. Nachfolgende Commits, die verschiedene Objekte ändern, können auch auf den aktuellen Frame angewendet werden, aber directcomposition garantiert nicht, dass die Änderungen im gleichen Frame auftreten.

Mit den Methoden [**idcompositionsurface:: beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) und [**idcompositionsurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) können Sie Renderingupdates mit visuellen Updates synchronisieren. Sie können z. b. " **idcompositionsurface:: beginDraw**" aufrufen, die Eigenschaften "OffsetX" und "Clip" eines visuellen Elements aktualisieren, " [**idcompositiondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)" aufrufen, Inhalte mit Microsoft DirectX zeichnen und dann " **idcompositionsurface:: EndDraw**" aufrufen. In diesem Fall stellt Microsoft directcomposition sicher, dass bitmapinhalte und die visuellen Eigenschaften gleichzeitig aktualisiert werden.

### <a name="batching"></a>Batching

Sie können mehrere Änderungen an derselben Visualisierung oder an mehreren Änderungen an verschiedenen visuellen Elementen innerhalb desselben Frames durchsetzen. Beachten Sie die folgenden Punkte, wenn Sie mehrere Änderungen an demselben visuellen Element innerhalb desselben Frames vornehmen:

-   Wenn Sie mehrere Änderungen an derselben Eigenschaft eines visuellen Elements vornehmen, wird nur die letzte Änderung angewendet. Wenn Sie z. b. die Deckkraft auf 0 (null), dann auf 0,5 und schließlich auf 1,0 festlegen, wird nur eine Deckkraft von 1,0 auf das visuelle Element angewendet.
-   Wenn Sie mehrere Eigenschaften desselben visuellen Elements ändern, wendet directcomposition die Änderungen zuerst auf das visuelle Element und dann auf alle untergeordneten visuellen Elemente an. Die Eigenschaften werden in der folgenden Reihenfolge unabhängig von der Reihenfolge angewendet, in der Sie Sie angeben:

    1.  Offset
    2.  Transformieren
    3.  Abschneiden
    4.  Wirkung

    Die folgende Abbildung zeigt das Ergebnis der Anwendung aller vier Eigenschaften auf ein visuelles Element.

    ![Ergebnis der Anwendung aller vier Eigenschaften auf ein visuelles Element](images/order-of-properties.png)

    Beachten Sie, dass alle Änderungen im Kontext desselben Frames gleichzeitig auf das visuelle Element angewendet werden. Dies bedeutet, dass die Änderungen an der Visualisierung aus der Sicht des Benutzers sofort erfolgen.

-   Für die Transform-Eigenschaft können Sie [**idcompositiondevice:: foratetransformgroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) verwenden, um eine Gruppe von Transformationen zu erstellen, die auf ein visuelles Element gleichzeitig angewendet werden. Die Transformationen werden von directcomposition in der von Ihnen angegebenen Reihenfolge angewendet.
-   Für die Eigenschaft "Effect" können Sie " [**idcompositioneffectgroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) " verwenden, um eine Gruppe von Effekten anzuwenden. Directcomposition wendet die Effekte in der von Ihnen angegebenen Reihenfolge an. Außerdem führen 3D-Perspektiven Transformationen zu einer Vereinfachung der visuellen Struktur, nachdem alle 3D-Transformationen in der aktuellen Visualisierung angewendet wurden. Dadurch wird sichergestellt, dass die resultierende Visualisierung so nah wie möglich in 3D aussieht.

### <a name="synchronization"></a>Synchronization

Die Anwendung kann directcomposition gleichzeitig aus mehreren Threads abrufen. Die Ausführungsreihenfolge wird für sequenzielle Aufrufe, jedoch nicht für gleichzeitige Aufrufe sichergestellt. Wenn z. B. Thread a ein visuelles Element ändert und Thread B gleichzeitig einen Commit für den Batch ausführt, wird nicht definiert, ob die visuelle Änderung in den zugezählten Batch eingeschlossen ist oder ob ein neuer Batch gestartet wird. Wenn Ihre Anwendung dagegen andere Synchronisierungs Mechanismen verwendet, um sicherzustellen, dass eine Methode vor der anderen aufgerufen wird, berücksichtigt directcomposition die Aufruf Reihenfolge und verarbeitet sie so, als ob beide Aufrufe in dieser Reihenfolge von einem einzelnen Thread ausgegeben werden.

### <a name="cross-device-visual-trees"></a>Geräte übergreifende visuelle Strukturen

Directcomposition-Objekte sind nicht Thread gebunden. Sie können mehrere Threads verwenden, um denselben Satz von Objekten zu ändern. Beachten Sie jedoch die folgenden Probleme bei der Freigabe desselben Geräte Objekts.

-   Beide Threads müssen in der Lage sein, [**idcompositiondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)aufzurufen. Wenn nur einer der Threads **idcompositiondevice:: Commit** aufruft, kann der andere Thread seine Änderungen nicht an directcomposition committen.
-   Das Transaktionsverhalten geht möglicherweise verloren, wenn ein Thread [**idcompositiondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) aufruft, während der andere Thread weiterhin Änderungen vornimmt, die Teil derselben Transaktion sein sollen.

Wenn Sie mehrere gleichzeitige Transaktionen für directcomposition durchführen müssen, müssen Sie mehrere Geräte Objekte verwenden, die möglicherweise von mehreren Threads verwendet werden. In diesem Szenario wird dieselbe visuelle Struktur von beiden Geräte Objekten gemeinsam genutzt, und jedes Geräte Objekt führt einen Commit für seine eigenen Transaktionen aus.

Die folgende Abbildung zeigt eine visuelle Struktur, die von zwei Geräte Objekten gemeinsam genutzt wird. Die Visualisierungen 1, 2, 4 und 5 befinden sich im Besitz eines Geräts, aber Visual 3 wird von beiden Geräten gemeinsam genutzt und kann daher verwendet werden, um zwei Teil Strukturen mit einer einzelnen, größeren visuellen Struktur zu verbinden. Durch die gemeinsame Nutzung der visuellen Struktur können die beiden Geräte asynchron aus zwei verschiedenen Threads manipuliert werden.

![eine visuelle Struktur, die von zwei Geräten gemeinsam genutzt wird](images/shared-visual-tree-1.png)

Um die Nützlichkeit der gemeinsamen Verwendung einer visuellen Struktur zwischen zwei Geräten zu veranschaulichen, sollten Sie eine Architektur in Erwägung nehmen, die Berührungs Eingaben mit geringer Latenz ermöglicht. Die Architektur könnte zwei Threads verwenden, eine, die die meisten Benutzeroberflächen Aufgaben verarbeitet, und einen zweiten Thread, der für die Verarbeitung von Fingereingabe Ereignissen dediziert ist. Der touchthread aktualisiert die Transformation eines bestimmten visuellen Elements auf der Grundlage der Benutzereingabe Geste. Durch Aktualisieren der Transformation kann der touchthread die gesamte Teilstruktur unterhalb dieses visuellen Elements nach dem Finger des Benutzers machen, nach oben oder unten skalieren, wenn der Benutzer eine Multitouch-Bewegung ausführt, usw. Der UI-Thread behält den größten Teil der Kompositionsstruktur bei, und der Berührungs Thread besitzt nur die wenigen visuellen Elemente, die für die asynchrone Berührungs Antwort gekennzeichnet sind. Die folgende Abbildung zeigt eine vereinfachte Version eines solchen Kompositions Baums:

![eine visuelle Struktur, die von einem UI-Thread und einem Berührungs Thread gemeinsam genutzt wird.](images/shared-visual-tree-2.png)

Der UI-Thread ändert in der Regel nur die visuellen Elemente, die er besitzt, und der Berührungs Thread ändert nur die freigegebene Visualisierung. Die einzige Ausnahme tritt auf, wenn eine Berührungs aktivierte Teilstruktur erstellt oder zerstört wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Idcompositionsurface:: beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)
</dt> <dt>

[**Idcompositionsurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)
</dt> <dt>

[**Idcompositondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[Directcomposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 
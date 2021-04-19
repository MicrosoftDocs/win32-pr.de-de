---
title: Animation (directcomposition)
description: In diesem Thema werden die Grundlagen der Microsoft directcomposition-Animation erläutert.
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7462a10fd83b45c1b90450fdde806ef306a2f6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341982"
---
# <a name="animation-directcomposition"></a>Animation (directcomposition)

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden die Grundlagen der Microsoft directcomposition-Animation erläutert. Die Lektion enthält die folgenden Themen:

-   [Was ist eine Animation?](#what-is-an-animation)
-   [Eigenschaften, die animiert werden können](#properties-that-can-be-animated)
-   [Animations Funktionen](#animation-functions)
-   [Animations Segmente](#animation-segments)
    -   [Kubisches Segment](#cubic-segment)
    -   [Sinusoidal-Segment](#sinusoidal-segment)
    -   [Segment wiederholen](#repeat-segment)
    -   [Segment Ende](#end-segment)
-   [Kompatibilität mit Windows Animation Manager](#compatibility-with-windows-animation-manager)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-an-animation"></a>Was ist eine Animation?

*Animation* ist eine optische Illusion, die erstellt wird, indem in einem bestimmten Zeitraum schnell inkrementelle Änderungen an einem visuellen Element vorgenommen werden, während die Visualisierung nach jeder Änderung neu gezeichnet wird. Da die Neuzeichnungen schnell ausgeführt werden, spürt das Gehirn die inkrementellen Änderungen als eine einzelne, sich ändernde Szene auf, genau wie bei einem Film oder einer Live Aktion.

In der folgenden Tabelle werden einige der typischen Möglichkeiten der Verwendung von Animationen beschrieben.

| Animation                 | BESCHREIBUNG                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bildlauf                 | Verwenden Sie Animationen zum Hinzufügen von Funktionen wie "Physik-emulating Momentum" zu einem scrolllisten-Steuerelement.                                                                                                                                                           |
| Szenen Übergänge         | Verwenden Sie Animationen, um Navigations Szenen Übergänge zu erstellen, die die Kontinuität zwischen Aufgaben in einem Workflow bereitstellen. Navigations Szenen Übergänge stellen Kontext bereit, der den Benutzer anzeigt, wo Sie sich befinden, wo Sie sich befinden und wo Sie als nächstes wechseln müssen. |
| Fenster übergreifende Interaktionen | Animieren Sie Benutzeroberflächen Elemente verschiedener Anwendungen auf eine Weise, die eine nahtlose Kontinuität zwischen Ihnen ermöglicht, um dem Benutzer zu helfen, Aufgaben auszuführen, die den Wechsel von einer Anwendung zu einer anderen ermöglichen.                                         |



 

## <a name="properties-that-can-be-animated"></a>Eigenschaften, die animiert werden können

In directcomposition animieren Sie ein visuelles Element durch Anwenden von Animationen auf einzelne Eigenschaften der Objekte, die die Visualisierung definieren. Wenn Sie ein visuelles Element z. b. horizontal auf den Bildschirm verschieben möchten, wenden Sie die Animation auf die OffsetX-Eigenschaft des visuellen Elements an. Wenn Sie eine einfache animierte 2D-Drehung eines visuellen Elements durchführen möchten, wenden Sie die Animation auf die Angle-Eigenschaft eines 2D-Transformations Objekts an, und wenden Sie dann das 2D-Transformations Objekt auf die Transform-Eigenschaft des visuellen Elements an.

Directcomposition ermöglicht das Anwenden von Animationen auf jede Objekt Eigenschaft, die einen skalaren Wert annimmt. Sie können gleichzeitige Animationen auf mehrere Eigenschaften und mehrere Objekte anwenden.

Directcomposition führt Animationen in einem separaten Thread aus. Sie können eine Animation oder einen Satz von Animationen starten und dann andere Aufgaben an Ihren Anwendungsthreads ausführen oder sogar Threads in den Standbymodus versetzen, während die Kompositions-Engine die Animationen mit der entsprechenden Framerate ausführt.

## <a name="animation-functions"></a>Animations Funktionen

Directcomposition animiert eine Objekt Eigenschaft, die auf einer von Ihnen definierten Animations Funktion basiert. Eine *Animations Funktion* ist ein Konstrukt, das angibt, wie sich der Wert einer Objekt Eigenschaft über einen bestimmten Zeitraum ändert. Sie können z. b. eine Animations Funktion definieren, die den Wert einer Eigenschaft im Verlauf von 4 Sekunden von 1 auf 360 ändert. Wenn Sie dann die Animations Funktion auf die Angle-Eigenschaft eines 2D-Transformations Objekts Drehung anwenden und dann das Transform-Objekt auf die Transform-Eigenschaft eines visuellen Elements anwenden, würde die Animations Funktion die Visualisierung im Verlauf von 4 Sekunden in einem vollständigen Kreis drehen.

Eine Animations Funktion wird durch ein *Animations Objekt* dargestellt, das durch einen Aufrufen der [**idcompositiondevice:: up Animation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) -Methode erstellt wird. Sie erstellen eine Animations Funktion mithilfe der Methoden der [**idcompositionanimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) -Schnittstelle eines Animations Objekts, um *Animations Segmente* nacheinander an das Array anzufügen, das die Animations Funktion definiert. Wenn Sie ein Segment anfügen, geben Sie einen NULL basierten Offset an, der die Anfangszeit des Segments relativ zum Anfang der Animations Funktion markiert. Animations Segmente müssen in zunehmender Reihenfolge der Anfangszeiten angehängt werden. Wenn Sie versuchen, ein Animations Segment anzufügen, dessen Anfangszeit vor oder gleich einem vorangehenden Segment ist, tritt ein Fehler auf. Eine Animations Funktion kann eine angegebene Endzeit aufweisen, die angibt, wann die Funktion abgeschlossen werden soll.

Sofern nicht anders angegeben, wird eine Animations Funktion gestartet, wenn der Desktopfenster-Manager (DWM) den Befehl empfängt, um die Animation auszuführen. Jedes Segment wird ausgeführt, bis die Startzeit des nächsten Segments erreicht ist. Alle diskontinuierlichen Änderungen, die im animierten Eigenschafts Wert zwischen Segmenten auftreten, gelten als diskrete Änderungen.

Sie wenden eine Animations Funktion auf eine Eigenschaft an, indem Sie den Eigenschafts Wert auf den [**idcompositionanimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) -Zeiger des Animations Objekts festlegen, das die Animations Funktion darstellt. Das gleiche Animations Objekt kann auf mehrere Eigenschaften desselben Objekts und auf die Eigenschaften anderer Objekte angewendet werden, die vom gleichen Gerät erstellt wurden.

## <a name="animation-segments"></a>Animations Segmente

Animations Segmente sind die grundlegenden zeitlichen Definitionen einer Animations Funktion. Dabei handelt es sich um die primitiven, aus denen komplexere und übergeordnete Animations Funktionen erstellt werden. Ein Animations Segment wird aus einer Reihe von Parametern erstellt, die die Funktion und die Uhrzeit, zu der das Segment beginnt, relativ zum Anfang der Animations Funktion beschreiben. Für jedes Segment verläuft die Zeit (*t*) entlang der horizontalen Achse und beginnt bei *t* = 0.

### <a name="cubic-segment"></a>Kubisches Segment

Die zeitliche Steuerung eines kubischen Segments wird durch einen kubischen polynomal definiert. Für eine gegebene Zeiteingabe (*t*) wird der Ausgabewert durch die folgende Gleichung angegeben:

*x*(*t*) = *bei*³ + *BT*² + *CT*  +  *d*

Das folgende Diagramm zeigt eine Animations Funktion, die zwei kubische Segmente enthält. Im ersten Segment wird ein Wert von 0 (null) zu 16 über 4 Sekunden übergegangen, während der zweite Wert in den nächsten 4 Sekunden den Wert linear von 16 in 0 ändert. Der erste Übergang erfolgt entlang dieses kubischen Polynomen:

*x*(*t*) = *t*³-6 *t*² + 12 *t*

der zweite Übergang erfolgt an dieser:

*x*(*t*) =-4 *t* + 16

![Diagramm einer Animations Funktion mit zwei kubischen Segmenten](images/cubicsegment.png)

Mithilfe der [**idcompositionanimation:: addcubic**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic) -Methode fügen Sie einer Animations Funktion ein kubisches Segment hinzu.

### <a name="sinusoidal-segment"></a>Sinusoidal-Segment

Die zeitliche Steuerung eines Sinus förmigem-Segments wird durch die folgende Gleichung definiert:

*x*(*t*) = *Bias*  +  *Amplitude* \* Sin (*t* \* *Frequency* \* 2 \* Pi + *Phase* \* PI/180,0)

Sie fügen ein Sinus förmigem-Segment zu einer Animations Funktion hinzu, indem Sie die [**idcompositionanimation:: addsinusoidal**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal) -Methode verwenden.

### <a name="repeat-segment"></a>Segment wiederholen

Ein Wiederholungs Segment wiederholt einen angegebenen vorangehenden Teil einer Animations Funktion. Ein Wiederholungs Segment bewirkt, dass der angegebene Teil der Animations Funktion eine unbegrenzte Schleife durchläuft, bis das nächste Segment erreicht oder das angegebene Ende der Animation erreicht wird. Der vorherige Teil einer Animation besteht aus anderen Segmenten, einschließlich anderer Wiederholungs Segmente. Ein Wiederholungs Segment kann nicht als erstes Segment in einer Animations Funktion verwendet werden.

Das folgende Diagramm zeigt eine Animations Funktion, die zwei eckige Segmente mit jeweils einer Dauer von 4 Sekunden umfasst, gefolgt von einem Wiederholungs Segment, das 12 Sekunden dauert. Das Wiederholungs Segment beginnt 8 Sekunden in der Animation und wiederholt die vorhergehenden 6 Sekunden der Animation zweimal, bis das Endsegment um 20 Sekunden erreicht wird.

![Diagramm einer Animations Funktion, die zwei kubische Segmente und ein Wiederholungs Segment enthält](images/repeatsegment.png)

Verwenden Sie zum Hinzufügen eines Wiederholungs Segments zu einer Animations Funktion die [**idcompositionanimation:: adresspeat**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat) -Methode.

### <a name="end-segment"></a>Segment Ende

Nachdem Sie eine Animations Funktion aus Segmenten erstellt haben, können Sie ein Endsegment anfügen, um die Animation zu einem bestimmten Zeitpunkt zu beenden. Wenn Sie kein Endsegment anfügen, wird das letzte Segment der Animations Funktion unbegrenzt ausgeführt.

Sie fügen ein Endsegment an, indem Sie die [**idcompositionanimation:: End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) -Methode aufrufen und einen Offset vom Anfang der Animations Funktion angeben, die den Endpunkt der Funktion angibt. Der Offset muss größer sein als der Anfangs Offset des vorangehenden Segments. Außerdem kann ein Endsegment nicht als erstes primitiv in einer Animations Funktion verwendet werden.

Wenn Sie " [**Ende**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end)" aufgerufen haben, geben Sie auch einen Endwert für die zu animierende Eigenschaft an. Die-Eigenschaft wird auf den angegebenen endgültigen Wert festgelegt, wenn der Endpunkt der Animations Funktion erreicht wird.

Nachdem Sie ein Endsegment angefügt haben, können Sie keine weiteren Segmente an die Animations Funktion anfügen. Das heißt, dass alle Methodenaufrufe für das Animations Objekt mit Ausnahme von [**idcompositionanimation:: Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset)fehlschlagen. Beim Aufrufen von **Reset** wird das Animations Objekt zum Bereinigen des Zustands zurückgegeben, in dem die Animations Funktion keine Segmente enthält. an diesem Punkt können Sie erneut Segmente hinzufügen.

## <a name="compatibility-with-windows-animation-manager"></a>Kompatibilität mit Windows Animation Manager

Windows Animation Manager (Windows-Animation) gibt Animations primitive in einem Format aus, das mit der directcomposition-API kompatibel ist. Dies bedeutet, dass directcomposition Animationen auf der Grundlage von Animations primitiven erstellen kann, die von der Windows-Animation erstellt wurden.

Weitere Informationen finden Sie unter [Windows Animation Manager](/windows/desktop/UIAnimation/-main-portal), the [**IUIAnimationVariable2:: getcurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) Method und [Managing directcomposition Animation with Windows Animation Manager v2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directcomposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 

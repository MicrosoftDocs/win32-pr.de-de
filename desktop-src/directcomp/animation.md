---
title: Animation (DirectComposition)
description: In diesem Thema werden die Grundlagen der Microsoft DirectComposition-Animation erläutert.
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b1f021d5a11fac70f47d5fe87f9389d2ad3e3108d224835fb295a8c3216354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119133"
---
# <a name="animation-directcomposition"></a>Animation (DirectComposition)

> [!NOTE]
> Für Apps auf Windows 10 empfehlen wir die Verwendung von Windows.UI.Composition-APIs anstelle von DirectComposition. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene.](/windows/uwp/composition/visual-layer-in-desktop-apps)

In diesem Thema werden die Grundlagen der Microsoft DirectComposition-Animation erläutert. Die Lektion enthält die folgenden Themen:

-   [Was ist eine Animation?](#what-is-an-animation)
-   [Eigenschaften, die animiert werden können](#properties-that-can-be-animated)
-   [Animationsfunktionen](#animation-functions)
-   [Animationssegmente](#animation-segments)
    -   [Kubisches Segment](#cubic-segment)
    -   [Sinusoidales Segment](#sinusoidal-segment)
    -   [Segment wiederholen](#repeat-segment)
    -   [Endsegment](#end-segment)
-   [Kompatibilität mit Windows Animation Manager](#compatibility-with-windows-animation-manager)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-an-animation"></a>Was ist eine Animation?

*Animation* ist eine optische Täuschung, die durch schnelle inkrementelle Änderungen an einem Visual über einen bestimmten Zeitraum erstellt wird, während das Visual nach jeder Änderung neu gedrammt wird. Da die Neuzeichnungen schnell erfolgen, nimmt das Gehirn die inkrementellen Änderungen als eine einzelne sich ändernde Szene wahr, genau wie in einem Film oder Video der Liveaktion.

In der folgenden Tabelle werden einige der typischen Methoden zur Verwendung von Animationen beschrieben.

| Animation                 | Beschreibung                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bildlauf                 | Verwenden Sie Animationen, um einem Bildlauflisten-Steuerelement Features wie physikalische Emulationsfeatures hinzuzufügen.                                                                                                                                                           |
| Szenenübergänge         | Verwenden Sie Animationen, um Navigationsszenenübergänge zu erstellen, die Kontinuität zwischen Aufgaben in einem Workflow bereitstellen. Navigationsszenenübergänge bieten Kontext, der dem Benutzer zeigt, wo er sich auftrat, wo er sich befinden und wo er als Nächstes wechseln muss. |
| Fensterübergreifende Interaktionen | Animieren Von Benutzeroberflächenelementen verschiedener Anwendungen auf eine Weise, die die Wahrnehmung der nahtlosen Kontinuität zwischen ihnen vermittelt, um dem Benutzer beim Ausführen von Aufgaben zu helfen, die den Wechsel von einer Anwendung zu einer anderen beinhalten.                                         |



 

## <a name="properties-that-can-be-animated"></a>Eigenschaften, die animiert werden können

In DirectComposition animieren Sie ein Visual, indem Sie Animationen auf einzelne Eigenschaften der Objekte anwenden, die das Visual definieren. Wenn Sie z. B. ein Visual horizontal über den Bildschirm verschieben möchten, wenden Sie animation auf die OffsetX-Eigenschaft des Visuals an. Wenn Sie eine einfache animierte 2D-Drehung eines Visuals verwenden möchten, wenden Sie animation auf die Angle-Eigenschaft eines 2D-Transformationsobjekts an und wenden dann das 2D-Transformationsobjekt auf die Transform-Eigenschaft des Visuals an.

Mit DirectComposition können Sie Animationen auf jede Objekteigenschaft anwenden, die einen Skalarwert verwendet. Sie können gleichzeitige Animationen auf mehrere Eigenschaften und Objekte anwenden.

DirectComposition führt Animationen in einem separaten Thread aus. Sie können eine Animation oder einen Satz von Animationen starten und dann andere Arbeit an Ihren Anwendungsthreads ausführen oder threads sogar in den Ruhezustand setzen, während die Kompositions-Engine die Animationen mit der entsprechenden Framerate ausarbeitiert.

## <a name="animation-functions"></a>Animationsfunktionen

DirectComposition animiert eine Objekteigenschaft basierend auf einer von Ihnen definierten Animationsfunktion. Eine *Animationsfunktion ist* ein Konstrukt, das angibt, wie sich der Wert einer Objekteigenschaft über einen bestimmten Zeitraum ändert. Beispielsweise können Sie eine Animationsfunktion definieren, die den Wert einer Eigenschaft im Laufe von 4 Sekunden von 1 in 360 ändert. Wenn Sie dann die Animationsfunktion auf die Angle-Eigenschaft eines 2D-Transformationsobjekts anwenden und dann das Transformationsobjekt auf die Transform-Eigenschaft eines Visuals anwenden, würde die Animationsfunktion das Visual im Laufe von 4 Sekunden in einem vollständigen Kreis drehen.

Eine Animationsfunktion wird durch ein *Animationsobjekt dargestellt,* das durch einen Aufruf der [**IDCompositionDevice::CreateAnimation-Methode erstellt**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) wurde. Sie erstellen eine Animationsfunktion, indem Sie die Methoden der [**IDCompositionAnimation-Schnittstelle**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) eines Animationsobjekts verwenden, um Animationssegmente nach und nach an das Array anfügen, das die Animationsfunktion definiert.  Beim Anfügen eines Segments geben Sie einen nullbasierten Offset an, der die Anfangszeit des Segments relativ zum Anfang der Animationsfunktion markiert. Animationssegmente müssen in zunehmender Reihenfolge der Startzeiten angefügt werden. Beim Versuch, ein Animationssegment anfügen, dessen Startzeit vor oder gleich einem vorherigen Segment liegt, wird ein Fehler angezeigt. Eine Animationsfunktion kann eine angegebene Endzeit haben, die angibt, wann die Funktion beendet werden soll.

Sofern nicht anders angegeben, wird eine Animationsfunktion gestartet, wenn der Desktopfenster-Manager (DWM) den Befehl zum Ausführen der Animation empfängt. Jedes Segment wird ausgeführt, bis die Startzeit des nächsten Segments erreicht ist. Alle nicht mehr reagierenden Änderungen, die im Wert der animierten Eigenschaft zwischen Segmenten auftreten, werden als diskrete Änderungen betrachtet.

Sie wenden eine Animationsfunktion auf eine Eigenschaft an, indem Sie den Eigenschaftswert auf den [**IDCompositionAnimation-Zeiger**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) des Animationsobjekts festlegen, das die Animationsfunktion darstellt. Dasselbe Animationsobjekt kann auf mehrere Eigenschaften desselben Objekts sowie auf die Eigenschaften anderer Objekte angewendet werden, die von demselben Gerät erstellt wurden.

## <a name="animation-segments"></a>Animationssegmente

Animationssegmente sind die grundlegenden Zeitsteuerungsdefinitionen einer Animationsfunktion. sie sind die Grundtypen, aus denen komplexere Animationsfunktionen und Animationsfunktionen höherer Ebene erstellt werden. Ein Animationssegment wird aus einer Reihe von Parametern erstellt, die die Funktion und den Zeitpunkt des Beginns des Segments relativ zum Anfang der Animationsfunktion beschreiben. Für jedes Segment verschreitet die Zeit (*t*) entlang der horizontalen Achse und beginnt bei *t* = 0.

### <a name="cubic-segment"></a>Kubisches Segment

Der Zeitpunkt eines kubischen Segments wird durch ein kubisches Polynom definiert. Für eine bestimmte Zeiteingabe (*t*) wird der Ausgabewert durch die folgende Gleichung angegeben:

*x*(*t*) = *bei* 2 + *bt* TASTE + *CT*  +  *D*

Das folgende Diagramm zeigt eine Animationsfunktion, die zwei kubische Segmente enthält. Das erste Segment überträgt einen Wert von 0 in 16 über 4 Sekunden, und das zweite ändert den Wert in den nächsten 4 Sekunden linear von 16 in 0. Der erste Übergang erfolgt entlang dieses kubischen Polynoms:

*x*(*t*) = *t* 2 - 6 *t*× 12 *t*

und der zweite Übergang erfolgt entlang dieses:

*x*(*t*) = - 4 *t* + 16

![Diagramm einer Animationsfunktion mit zwei kubischen Segmenten](images/cubicsegment.png)

Sie fügen einer Animationsfunktion mithilfe der [**IDCompositionAnimation::AddCubic-Methode**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic) ein kubisches Segment hinzu.

### <a name="sinusoidal-segment"></a>Sinusoidales Segment

Die zeitliche Steuerung eines sinusförmigen Segments wird durch die folgende Gleichung definiert:

*x*(*t*) = *Bias*  +  *Amplitude* \* sin(*t* \* *Frequency* \* 2 PI + \* *Phase* \* PI/180.0)

Sie fügen einer Animationsfunktion mithilfe der [**IDCompositionAnimation::AddSinusoidal-Methode ein sinusförmiges Segment**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal) hinzu.

### <a name="repeat-segment"></a>Segment wiederholen

Ein Wiederholungssegment wiederholt einen angegebenen vorangehenden Teil einer Animationsfunktion. Ein Wiederholungssegment bewirkt, dass der angegebene Teil der Animationsfunktion unbegrenzt in eine Schleife einschlang, bis das nächste Segment gefunden wird oder das angegebene Ende der Animation erreicht ist. Der vorherige Teil einer Animation besteht aus anderen Segmenten, einschließlich anderer Wiederholungssegmente. Ein Wiederholungssegment kann nicht als erstes Segment in einer Animationsfunktion verwendet werden.

Das folgende Diagramm zeigt eine Animationsfunktion, die zwei kubische Segmente mit jeweils 4 Sekunden Dauer gefolgt von einem Wiederholungssegment von 12 Sekunden umfasst. Das Wiederholungssegment beginnt 8 Sekunden in der Animation und wiederholt die vorherigen 6 Sekunden der Animation zweimal, bis das Endsegment bei 20 Sekunden erreicht ist.

![Diagramm einer Animationsfunktion, die zwei kubische Segmente und ein Wiederholungssegment enthält](images/repeatsegment.png)

Um einer Animationsfunktion ein Wiederholungssegment hinzuzufügen, verwenden Sie die [**IDCompositionAnimation::AddRepeat-Methode.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat)

### <a name="end-segment"></a>Endsegment

Nachdem Sie eine Animationsfunktion aus Segmenten erstellt haben, können Sie ein Endsegment anfügen, damit die Animationsfunktion zu einem bestimmten Zeitpunkt beendet wird. Wenn Sie kein Endsegment anfügen, wird das letzte Segment der Animationsfunktion unbegrenzt ausgeführt.

Sie fügen ein Endsegment an, indem Sie die [**IDCompositionAnimation::End-Methode**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) aufrufen und einen Offset vom Anfang der Animationsfunktion angeben, der den Endpunkt der Funktion angibt. Der Offset muss größer als der Anfangsoffset des vorherigen Segments sein. Außerdem kann ein Endsegment nicht als erste Primitive in einer Animationsfunktion verwendet werden.

Wenn Sie End [**aufrufen,**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end)geben Sie auch einen endgültigen Wert für die animierte Eigenschaft an. Die -Eigenschaft wird auf den angegebenen endgültigen Wert in dem Moment festgelegt, an dem der Endpunkt der Animationsfunktion erreicht ist.

Nach dem Anfügen eines Endsegments können Sie keine anderen Segmente an die Animationsfunktion anfügen. Das heißt, dass alle Methodenaufrufe für das Animationsobjekt mit Ausnahme [**von IDCompositionAnimation::Reset fehlschlagen.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset) Der **Aufruf von Reset** gibt das Animationsobjekt zurück, um den Zustand zu bereinigt, in dem die Animationsfunktion keine Segmente enthält. An diesem Punkt können Sie wieder Segmente hinzufügen.

## <a name="compatibility-with-windows-animation-manager"></a>Kompatibilität mit Windows Animation Manager

Windows Animation Manager (Windows Animation) gibt Animationsprimitiven in einem Format aus, das mit der DirectComposition-API kompatibel ist. Dies bedeutet, dass DirectComposition Animationen basierend auf Animationsprimitiven erstellen kann, die von der animation Windows werden.

Weitere Informationen finden Sie unter [Windows Animation Manager](/windows/desktop/UIAnimation/-main-portal), der [**IUIAnimationVariable2::GetCurve-Methode**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) und [Managing DirectComposition Animation with Windows Animation Manager v2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectComposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 

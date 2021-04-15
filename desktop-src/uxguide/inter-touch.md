---
title: Touch
description: Alle Microsoft Windows-Anwendungen sollten eine gute Berührungs Funktion aufweisen. Das Erstellen einer solchen Vorgehensweise ist einfacher, als Sie sich vorstellen.
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a44a95ad963d3563418ed0492e55606824011f31
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554475"
---
# <a name="touch"></a>Touch

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Alle Microsoft Windows-Anwendungen sollten eine gute Berührungs Funktion aufweisen. Das Erstellen einer solchen Vorgehensweise ist einfacher, als Sie sich vorstellen.

"Berühren" bezieht sich auf die Verwendung von einem oder mehreren Fingern, um Eingaben über eine Geräte Anzeige bereitzustellen und mit Windows und apps zu interagieren. Eine Touchscreen-optimierte App verfügt über ein UI-und Interaktionsmodell, das den größeren, weniger präzisen Kontaktbereichen der Fingereingabe, den verschiedenen Formfaktoren von Fingereingabe Geräten und den zahlreichen, von Benutzern bei der Verwendung eines Finger Eingabegeräts übernehmen kann.

![Interaktion von Benutzern mit Tablet mithilfe von Touchscreen](images/inter_touch_image1.jpeg)

Jedes Eingabegerät hat seine Stärken. Die Tastatur eignet sich am besten für Texteingaben und gibt Befehle mit minimaler Handbewegung an. Die Maus eignet sich am besten für effiziente und präzise zeige. Die Fingereingabe eignet sich am besten für die Objekt Bearbeitung und die Bereitstellung von Ein Stift eignet sich am besten für einen frei Form Ausdruck, wie bei Handschrift und Zeichen.

Windows 8.1 ist für die Reaktionsfähigkeit, Genauigkeit und Benutzerfreundlichkeit mit Berührungs Optimierung optimiert, während herkömmliche Eingabemethoden (z. b. Maus, Stift und Tastatur) vollständig unterstützt werden. Die Geschwindigkeit, Genauigkeit und das taktischere Feedback, die herkömmliche Eingabemodi bieten, sind für viele Benutzer vertraut und ansprechend und möglicherweise besser für bestimmte Interaktions Szenarien geeignet.

In separaten Themen finden Sie Richtlinien, die sich auf Maus, Stift und Barrierefreiheit beziehen.

Wenn Sie die Interaktion mit ihrer app in Betracht kommen:

Gehen Sie nicht davon aus, dass eine Benutzeroberfläche, die für eine Maus funktioniert, auch gut für die Fingereingabe geeignet ist. Obwohl eine gute Mausunterstützung ein Einstieg ist, sind für eine gute Berührungs Funktion einige zusätzliche Anforderungen zu erfüllen.

Gehen Sie davon aus, dass eine Benutzeroberfläche, die für einen Finger geeignet ist, auch für einen Stift gut funktioniert. Wenn Sie Ihre APP touchfähig machen, können Sie auch eine gute Stift Unterstützung bereitstellen. Der Hauptunterschied besteht darin, dass Finger einen blunter-Tipp haben, sodass Sie größere Ziele benötigen.

Mit der Fingereingabe können Sie Objekte und die Benutzeroberfläche direkt bearbeiten, was zu einer schnelleren, natürlicheren und ansprechender Benutzeroberfläche führt.

## <a name="provide-a-great-touch-experience"></a>Sorgen Sie für eine gute Berührungs Funktion

Sie sollten sicherstellen, dass Benutzer wichtige und wichtige Aufgaben effizient mithilfe von Finger Eingaben durchführen können. Bestimmte App-Funktionen, wie z. b. Text-oder Pixel Bearbeitung, sind jedoch möglicherweise nicht für die Fingereingabe geeignet und können für das am besten geeignete Eingabegerät reserviert werden.

Wenn Sie nicht viel mit der Entwicklung von Touchscreen-apps vertraut sind, ist es am besten, dies zu erlernen. Holen Sie sich einen Touchscreen-fähigen Computer, bewegen Sie die Maus und die Tastatur, und verwenden Sie nur Ihre Finger, um mit Ihrer APP zu interagieren. Wenn Sie über ein Tablet verfügen, experimentieren Sie mit dem halten an verschiedenen Positionen, z. b. in Ihrem Schoß, in einer Tabelle oder in den Armen, während Sie arbeiten. Versuchen Sie, es in hoch-und Querformat zu verwenden.

Touchscreen-optimierte apps, die am besten mit der Berührungs Interaktion funktionieren, sind in der Regel:

-   **Natürlich und intuitiv.** Interaktionen sind so konzipiert, dass Sie mit der Interaktion von Benutzern in der realen Welt übereinstimmen.
-   **Weniger intrusiv.** Die Verwendung von Finger Eingaben ist unbeaufsichtigt und daher weniger stark ablenkend als bei der Eingabe oder dem Klicken auf.
-   **Tabel.** Touchgeräte sind kompakter, da viele Aufgaben ohne Tastatur, Maus, Stift oder Touchpad abgeschlossen werden können. Sie sind auch flexibler, weil eine Arbeitsoberfläche nicht erforderlich ist.
-   **Direkt und Engagement.** Mit toucheingaben haben Sie die Meinung, dass Sie Objekte auf dem Bildschirm direkt bearbeiten.
-   **Weniger genau.** Benutzer können Objekte nicht genau mit einer Maus oder einem Stift vergleichen.

Der Fingerabdruck bietet eine natürliche und reale Interaktion. Direkte Manipulation und Animation vervollständigen diesen Eindruck, indem Sie Objekten einen realistischen, dynamischen Bewegungs-und feedfeedback geben. Nehmen wir beispielsweise ein Kartenspiel. Es ist nicht nur bequem und leicht, Karten mit einem Finger zu ziehen. die Erfahrung ist ein Gefühl der realen Welt, wenn Sie die Karten genau wie ein physisches Kartenspiel verschieben, gleiten und drehen können. Und wenn Sie versuchen, eine Karte zu verschieben, die nicht verschoben werden kann, ist es besser, die Karte Gegenstand zu halten, die Bewegung aber nicht zu verhindern, und sich bei der Veröffentlichung wieder an der Stelle zu befinden, um eindeutig anzugeben, dass die Aktion erkannt wurde, aber nicht ausgeführt werden kann.

Wenn Ihre APP bereits gut entworfen wurde, ist es ganz einfach, eine gute Fingereingabe zu bieten. Zu diesem Zweck ein gut konzipiertes Programm:

-   **Stellt sicher, dass die meisten wichtigen Aufgaben mit einem Finger effizient ausgeführt werden können** (zumindest bei den Aufgaben, die nicht viel Eingaben oder eine detaillierte Pixel Bearbeitung beinhalten).
-   **Verwendet große Steuerelemente zur Berührung.** Allgemeine Steuerelemente haben eine minimale Größe von 23x23 Pixel (13 x 13 DLUs), und die am häufigsten verwendeten Steuerelemente sind mindestens 40 x 40 Pixel (23x22-DLUs). Um ein nicht reagierendes Verhalten zu vermeiden, sollten Benutzeroberflächen Elemente mindestens 5 Pixel (3 DLUs) zwischen den Leerraum aufweisen. Stellen Sie für andere Steuerelemente sicher, dass Sie mindestens ein 23x23 Pixel (13 x 13 dlu)-Click-Ziel haben, auch wenn Ihre statische Darstellung wesentlich kleiner ist. Siehe Standard Steuerelement Größenanpassung.
-   **Unterstützt Maus Eingaben.** Die interaktiven Steuerelemente haben klare, sichtbare Kosten. Objekte verfügen über Standardverhalten für die Standard Maus Interaktionen (Single und Double Left-click, Right-Click, Drag und Hover).
-   **Unterstützt Tastatureingaben.** Die APP bietet Standard Zuweisungen für Tastenkombinationen, insbesondere für Navigations-und Bearbeitungsbefehle, die auch durch Touchgesten generiert werden können.
-   **Gewährleistet die Barrierefreiheit.** Verwendet die Benutzeroberflächen Automatisierung oder Microsoft Active Accessibility (MSAA), um programmgesteuerten Zugriff auf die Benutzeroberfläche für Hilfstechnologien bereitzustellen. Die APP antwortet entsprechend den Änderungen an Ausrichtung, Design, Gebiets Schema und System Metrik.
-   **Eliminiert unnötige Interaktionen.** Verwenden Sie die sichersten und sichersten Standardwerte, um den Verlust von Daten oder den System Zugriff zu verhindern. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählt die APP die wahrscheinlichste oder bequeme Option aus.
-   **Stellt eine Berührungs Entsprechung für den Hover bereit.** Verlassen Sie sich nicht auf den Mauszeiger als einzige Möglichkeit zum Ausführen einer Aktion.
-   **Stellt sicher, dass Gesten sofort wirksam werden.** Halten Sie Kontaktpunkte während der Bewegung reibungslos unter den Fingern des Benutzers, sodass die Gesten direkt auf die Bewegung des Benutzers angewendet werden.
-   **Verwendet Standard Gesten, wann immer dies möglich ist.** Benutzerdefinierte Gesten nur für Interaktionen, die für Ihre APP eindeutig sind.
-   **Gewährleistet, dass unerwünschte oder zerstörerische Befehle umgekehrt oder korrigiert werden können.** Versehentliche Aktionen sind bei Verwendung von "berühren" wahrscheinlicher.

## <a name="guidelines-for-touch-input"></a>Richtlinien für Berührungs Eingaben

Mit der Toucheingabe kann Ihre Windows-App physische Gesten verwenden, um die direkte Bearbeitung von UI-Elementen zu emulieren.

Beachten Sie diese bewährten Methoden, wenn Sie Ihre Touchscreen-fähige App entwerfen:

**Die Reaktionsfähigkeit ist entscheidend für das Erstellen von Berührungs Erlebnissen, die sich direkt und ansprechend Verhalten** Um sich direkt vertraut zu machen, müssen Gesten sofort wirksam werden, und die Kontaktpunkte eines Objekts müssen bei der Bewegung reibungslos bleiben. Die Auswirkungen von Finger Eingaben sollten direkt der Bewegung des Benutzers zugeordnet werden. wenn der Benutzer z. b. seine Finger um 90 Grad rotiert, sollte das Objekt auch 90 Grad drehen. Jede Verzögerung, eine unkorrekte Antwort, ein Verlust von Kontakten oder ungenaue Ergebnisse zerstört die Wahrnehmung der direkten Bearbeitung und der Qualität.

**Konsistenz ist für das Erstellen von Finger Eingaben, die sich in natürlicher und intuitiver Natur fühlen** Nachdem Benutzer eine Standard Geste gelernt haben, erwarten Sie, dass diese Geste für alle apps dieselbe Wirkung hat. Um Verwirrung und Frustration zu vermeiden, weisen Sie Standard Gesten niemals nicht dem Standard entsprechende Bedeutungen zu. Verwenden Sie stattdessen benutzerdefinierte Gesten für Interaktionen, die für Ihr Programm eindeutig sind.

Als nächstes beschreiben wir die Windows-Berührungs Sprache, aber bevor wir fortfahren, finden Sie hier eine kurze Liste der grundlegenden Fingereingabe Begriffe.

-   **Geste**

    Eine Geste besteht aus dem physischen Act oder der Bewegung, die bzw. der von dem Eingabegerät (Finger, Fingern, Stift/Stift, Maus usw.) ausgeführt wird. Wenn Sie z. b. einen Befehl starten, aktivieren oder aufrufen möchten, verwenden Sie eine einzelne Fingereingabe für ein Touch-oder Touchpad-Gerät (äquivalent zu einem Klick mit der linken Maustaste mit einer Maus, einem Tippen mit einem Stift oder der Eingabetaste auf der Tastatur).

-   **Manipulation**

    Eine Manipulation ist die unmittelbare Echtzeitreaktion oder-Antwort, die ein Objekt oder eine Benutzeroberfläche auf eine Geste hat. Beispielsweise bewirken die Folie-und die Schwenk Gesten in der Regel, dass ein Element oder eine Benutzeroberfläche verschoben wird.

    Das Endergebnis einer Bearbeitung, die Darstellung durch das Objekt auf dem Bildschirm und in der Benutzeroberfläche ist die Interaktion.

-   **Interaktion**

    Interaktionen hängen davon ab, wie eine Manipulation interpretiert wird, und dem Befehl oder der Aktion, die sich aus der Bearbeitung ergeben. Beispielsweise können Objekte sowohl mit der Folie als auch mit der Schwenkbewegung verschoben werden, die Ergebnisse unterscheiden sich jedoch abhängig davon, ob ein Entfernungs Schwellenwert überschritten wird. Folie kann verwendet werden, um ein Objekt zu ziehen oder eine Ansicht zu schwenken, während mithilfe von schwenken ein Element ausgewählt oder eine APP-Leiste angezeigt werden kann.

### <a name="the-windows-touch-language"></a>Die Windows-Berührungs Sprache

Windows bietet einen präzisen Satz von touchinteraktionen, die im gesamten System verwendet werden. Wenn Sie diese Berührungs Sprache einheitlich anwenden, ist Ihre APP vertraut, was Benutzern bereits bekannt ist. Dies erhöht die Benutzer Zuverlässigkeit, indem die APP leichter zu erlernen und zu verwenden ist. Weitere Informationen zur Implementierung der touchsprache finden Sie unter Gesten, Manipulationen und Interaktionen.

**Halten Sie sich zum Erlernen**

Die Geste "drücken und halten" zeigt ausführliche Informationen oder visuelle Elemente an (z. b. eine QuickInfo oder ein Kontextmenü), ohne einen Commit für eine Aktion oder einen Befehl auszuführen. Das Schwenken ist immer noch möglich, wenn eine gleitende Bewegung gestartet wird, während das visuelle Element angezeigt wird.

> [!IMPORTANT]
> In Fällen, in denen horizontales und vertikales schwenken aktiviert ist, können Sie die Option drücken und halten verwenden.

 

Einstiegs Status: ein oder zwei Finger in Kontakt mit dem Bildschirm.

Bewegung: keine Bewegung.

Beendigungs Status: Letzter fingerpfeil beendet die Geste.

Auswirkung: zeigen Sie weitere Informationen an.

![Tippen \- \- Sie auf \-learn.png](images/inter-touch-image2.png)

Die Bewegung und halten.

**Darauf zeigen (Hover)**

Hover ist eine nützliche Interaktion, da Benutzer zusätzliche Informationen über Tipps erhalten können, bevor eine Aktion initiiert wird. Wenn Sie diese Tipps anzeigen, sind die Benutzer sicherer und können Fehler reduzieren.

Leider wird Hover nicht von Touch-Technologien unterstützt, sodass Benutzer nicht auf einen Finger zeigen können. Die einfache Lösung für dieses Problem besteht darin, den Mauszeiger in vollem Umfang zu nutzen, aber nur auf eine Weise, die nicht zum Ausführen einer Aktion erforderlich ist. In der Praxis bedeutet dies in der Regel, dass die Aktion auch durch klicken, jedoch nicht notwendigerweise auf die gleiche Weise ausgeführt werden kann.

![Screenshot mit einem Beispiel für die Hover-Interaktion neben einem Beispiel für die Klick Aktion.](images/inter-touch-image13.png)

In diesem Beispiel können Benutzer das heutige Datum anzeigen, indem Sie entweder mit der Maus darauf zeigen oder klicken.

**Auf "Primary Action" tippen**

Durch Tippen auf ein Element wird die primäre Aktion aufgerufen, z.b. das Starten einer APP oder das Ausführen eines Befehls.

Eintrags Status: ein Finger in Kontakt mit dem Bildschirm oder Touchpad und vor dem Zeit Schwellenwert für eine Press-und halteinteraktion.

Bewegung: keine Bewegung.

Beendigungs Zustand: mit dem Finger nach oben wird die Geste beendet.

Auswirkung: Starten Sie eine APP, oder führen Sie einen Befehl aus.

![Touchscreen \- \-primary.png](images/inter-touch-image3.png)

Die Tap-Geste.

**Folie zu schwenken**

Folie wird hauptsächlich zum Schwenken von Interaktionen verwendet, kann aber auch zum Verschieben verwendet werden (wobei Schwenken auf eine Richtung eingeschränkt ist), zeichnen oder schreiben. Folie kann auch verwendet werden, um kleine, stark gepackte Elemente durch Bereinigungs zu erreichen (mit dem Finger über verknüpfte Objekte, z. b. Options Felder).

Einstiegs Status: ein oder zwei Finger in Kontakt mit dem Bildschirm.

Bewegung: ziehen Sie den Zieh Vorgang, wobei sich alle weiteren verbleibenden Finger in der gleichen Position relativ zueinander befinden.

Beendigungs Status: Letzter fingerpfeil beendet die Geste.

Effekt: Verschieben Sie das zugrunde liegende Objekt direkt und sofort, wenn die Finger bewegt werden. Stellen Sie sicher, dass Sie den Kontaktpunkt während der Bewegung unter dem Finger halten.

![\-slide.png berühren](images/inter-touch-image4.png)

Die Schwenkbewegung.

**Zum auswählen, zum Befehl und zum Verschieben schwenken**

Wenn Sie den Finger in eine kurze Entfernung bewegen (in der Reihenfolge, in der die Schwenken auf eine Richtung beschränkt ist), werden die Objekte in einer Liste oder einem Raster ausgewählt. Hiermit wird die APP-Leiste mit relevanten Befehlen angezeigt, wenn Objekte ausgewählt werden.

Einstiegs Status: ein oder mehrere Finger berühren den Bildschirm.

Bewegung: ziehen Sie eine kurze Entfernung, und heben Sie den Entfernungs Schwellenwert für eine Verschiebe Interaktion auf.

Beendigungs Status: Letzter fingerpfeil beendet die Geste.

Auswirkung: das zugrunde liegende Objekt ist ausgewählt oder verschoben, oder die APP-Leiste wird angezeigt. Stellen Sie sicher, dass Sie den Kontaktpunkt während der Bewegung unter dem Finger halten.

![d: \\ sdkenlistment \\ m \- UX \- Design \\ m \- UX \- Design \\ Images \\ Touchscreen \-swipe.png](images/inter-touch-image5.png)

Die Schwenkbewegung.

**Zusammendrücken/Aufziehen: Zoom**

Die Gesten-und streckungs Gesten werden für drei Arten von Interaktionen verwendet: optischer Zoom, Größe der Größe und Semantik Zoom.

Optischer Zoom passt die Vergrößerungs Ebene des gesamten Inhalts Bereichs an, um eine ausführlichere Ansicht der Inhalte zu erhalten. Im Gegensatz dazu ist die Größenänderung eine Technik, mit der die relative Größe von einem oder mehreren Objekten in einem Inhalts Bereich angepasst werden kann, ohne die Ansicht in den Inhalts Bereich zu ändern.

Der semantische Zoom ist ein Berührungs optimiertes Verfahren für die Darstellung und Navigation von strukturierten Daten oder Inhalten in einer einzelnen Ansicht (z. b. die Ordnerstruktur eines Computers, eine Bibliothek mit Dokumenten oder ein Fotoalbum), ohne dass dafür ein Schwenken, Scrollen oder Strukturansicht-Steuerelemente erforderlich sind. Der semantische Zoom bietet zwei verschiedene Ansichten desselben Inhalts, indem Sie beim Verkleinern weitere Details anzeigen, wenn Sie vergrößern und verkleinern.

Eintrags Status: zwei Finger im Kontakt mit dem Bildschirm zur gleichen Zeit.

Bewegung: die Finger bewegen sich entlang einer Achse nach unten (gestreckt) oder zusammen (durch Spannen).

Beendigungs Status: jeder Finger nach oben beendet die Geste.

Effect: vergrößern oder verkleinern Sie das zugrunde liegende Objekt direkt und direkt, indem Sie es auf der Achse voneinander trennen. Stellen Sie sicher, dass die Kontaktpunkte im Verlauf der Bewegung unter dem Finger gehalten werden.

![Landing \-areazoom.png](images/inter-touch-image6.png)

Die Zoom Bewegung.

**Zum drehen drehen**

Das Drehen mit zwei oder mehr Fingern bewirkt, dass ein Objekt gedreht wird. Drehen Sie das Gerät selbst, um den ganzen Bildschirm zu drehen.

Eintrags Status: zwei Finger im Kontakt mit dem Bildschirm zur gleichen Zeit.

Bewegung: eine oder beide Finger drehen sich um die andere und bewegen sich senkrecht zur Linie zwischen Ihnen.

Beendigungs Status: jeder Finger nach oben beendet die Geste.

Effekt: Drehen Sie das zugrunde liegende Objekt um denselben Betrag, in dem sich die Finger gedreht haben. Stellen Sie sicher, dass die Kontaktpunkte im Verlauf der Bewegung unter dem Finger gehalten werden.

![\-turn.png berühren](images/inter-touch-image7.png)

Die Drehungs Bewegung.

Die Drehung ist nur für bestimmte Objekttypen sinnvoll, sodass Sie keiner System-Windows-Interaktion zugeordnet ist.

Die Rotation wird häufig von unterschiedlichen Personen unterschiedlich durchgeführt. Einige Leute bevorzugen, einen Finger um einen pivotfinger herum drehen zu müssen, während andere lieber beide Finger in einer Kreisbewegung drehen. Die meisten Benutzer verwenden eine Kombination der beiden, wobei ein Finger mehr als die andere ist. Obwohl die glatte Drehung in einen beliebigen Winkel die beste Interaktion ist, ist es in vielen Kontexten, wie z. b. der Foto Anzeige, am besten, die nächstgelegene 90-Grad-Drehung zu erhalten, sobald der Benutzer das Los geht. Bei der Fotobearbeitung können Sie eine kleine Drehung verwenden, um das Foto zu korrigieren.

**Aus Edge für App-Befehle schwenken**

Wenn Sie mit dem Finger eine kurze Entfernung vom unteren oder oberen Rand des Bildschirms wischen, werden die APP-Befehle in einer APP-Leiste angezeigt.

Einstiegs Status: ein oder mehrere Finger berühren das Bezel.

Bewegung: ziehen Sie eine kurze Entfernung auf den Bildschirm, und ziehen Sie den Lift.

Beendigungs Status: Letzter fingerpfeil beendet die Geste.

Auswirkung: die APP-Leiste wird angezeigt.

![\- \- untere \-edge.png berühren](images/inter-touch-image8.png)

![Fingereingabe \- \- \-edge.png](images/inter-touch-image9.png)

Die Schwenkbewegung von der Randbewegung.

Entwickler: Weitere Informationen finden Sie unter [**directmanipulation- \_ konfigurationsenumeration**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration) .

### <a name="control-usage"></a>Verwendung steuern

Hier finden Sie einige Richtlinien für die Optimierung von Steuerelementen für die Berührungs Verwendung.

-   **Verwenden Sie allgemeine Steuerelemente.** Die meisten gängigen Steuerelemente sind darauf ausgelegt, eine gute Berührungs Funktion zu unterstützen.
-   **Wählen Sie benutzerdefinierte Steuerelemente, die zur Unterstützung von Finger Eingaben entworfen** Möglicherweise benötigen Sie benutzerdefinierte Steuerelemente zur Unterstützung der besonderen Benutzerfreundlichkeit Ihres Programms. Benutzerdefinierte Steuerelemente auswählen:
    -   Kann groß genug für die einfache Ausrichtung und Bearbeitung sein.
    -   Verschieben Sie bei der Manipulation die Art und Weise, in der reale Objekte verschoben und reagiert werden, wie z. b. durch Dynamik und Reibung.
    -   Durch die Möglichkeit, Fehler zu beheben.
    -   Gibt an, dass die Ungenauigkeit beim Klicken und ziehen nicht korrekt ist. Objekte, die in der Nähe Ihres Ziels abgelegt werden, sollten an die richtige Stelle fallen.
    -   Wenn sich der Finger über dem Steuerelement befindet, haben Sie ein klares visuelles Feedback.
-   **Verwenden Sie eingeschränkte Steuerelemente.** Eingeschränkte Steuerelemente wie Listen und Schieberegler können bei der Erstellung einfacher Finger Eingaben besser als nicht eingeschränkte Steuerelemente wie Textfelder sein, da Sie die Notwendigkeit von Texteingaben verringern.
-   **Geben Sie entsprechende Standardwerte an.** Wählen Sie das sicherste (um Datenverlust oder System Zugriff zu vermeiden) und die sicherste Option standardmäßig aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Option aus, wodurch unnötige Interaktionen vermieden werden.
-   **Automatische Vervollständigung von Text angeben.** Stellt eine Liste der wahrscheinlichsten oder zuletzt eingegebenen Werte bereit, um die Texteingabe erheblich zu vereinfachen.
-   Stellen Sie **für wichtige Aufgaben, die Mehrfachauswahl verwenden**, eine Option zum Verwenden einer Kontrollkästchen-Liste bereit, wenn normalerweise eine standardmäßige Mehrfachauswahl Liste verwendet wird.

### <a name="control-sizes-and-touch-targeting"></a>Steuerelement Größen und Berührungs Ziele

Aufgrund der großen Oberfläche des Fingertips können kleine Steuerelemente, die zu eng beieinander liegen, schwierig sein, genau darauf ausgerichtet zu sein.

Als allgemeine Regel gilt: eine Steuerelement Größe von 23x23 Pixel (13 x 13 DLUs) ist eine gute minimale interaktive Steuerelement Größe für alle Eingabegeräte. Im Gegensatz dazu sind die Dreh Steuerelemente bei 15x11 Pixel viel zu klein, um effektiv mit der Fingereingabe verwendet zu werden.

![Screenshot, der die Breite und Höhe der Auswahl Schaltflächen nach oben und unten anzeigt, wobei 9 DLUs (15 Pixel) breit und 5 DLUs (9 Pixel) hoch sind.](images/inter-touch-image14.png)

Beachten Sie, dass die minimale Größe tatsächlich auf physischem Gebiet basiert, nicht auf layoutmetriken wie z. b. Pixel oder DLUs. Research gibt an, dass der minimale Zielbereich für effiziente, genaue Interaktion mit einem Finger 6x6 Millimeter (mm) ist. Dieser Bereich übersetzt layoutmetriken wie folgt:



| Schriftart             | Millimeter | Relative Pixel | DLUs  |
|------------------|-------------|-----------------|-------|
| 9 Punkt Segoe UI | 6x6         | 23x23           | 13x13 |
| 8-Punkt-Tahoma   | 6x6         | 23x23           | 15x14 |



 

Außerdem wird durch die Untersuchung angezeigt, dass eine minimale Größe von 10X10 mm (ca. 40 x 40 Pixel) eine höhere Geschwindigkeit und Genauigkeit ermöglicht und die Benutzer auch benutzerfreundlich sind. Verwenden Sie diese größere Größe für Befehls Schaltflächen, die für die wichtigsten oder häufig verwendeten Befehle verwendet werden.

Das Ziel ist nicht, dass Sie über riesige Steuerelemente verfügen.

![Screenshot, der die Microsoft Word-Symbolleiste mit hervorgehobener Schaltfläche "a B C-Rechtschreib &-Grammatik" anzeigt, mit einer 41 dlu-Höhe und 40 dlu-Breite.](images/inter-touch-image15.png)

In diesem Beispiel verwendet Microsoft Word für die wichtigsten Befehle Schaltflächen, die größer als 10X10 mm sind.

![Screenshot, der den Windows-Rechner anzeigt.](images/inter-touch-image16.png)

Diese Version des Rechners verwendet für die am häufigsten verwendeten Befehle Schaltflächen, die größer als 10X10 mm sind.

Es gibt keine perfekte Größe für Berührungs Ziele. Unterschiedliche Größen können für unterschiedliche Situationen verwendet werden. Aktionen mit schwerwiegenden Konsequenzen (z. b. DELETE und Close) oder häufig verwendete Aktionen sollten große Berührungs Ziele verwenden. Selten verwendete Aktionen mit geringfügigen folgen können kleine Ziele verwenden.

**Zielgrößen-Richtlinien für benutzerdefinierte Steuerelemente**



| Größen Richtlinie                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![mindestens 7 x 7 empfohlene Mindestgröße](images/inter_touch_image10.jpeg)<br/>      | **7x7 mm: empfohlene Mindestgröße**<br/> 7x7 mm ist eine gute Mindestgröße, wenn das falsche Ziel in einer oder zwei Gesten oder innerhalb von fünf Sekunden korrigiert werden kann. Die Auffüll Zeichen zwischen Zielen sind ebenso wichtig wie die Zielgröße.<br/>                               |
| ![9x9 empfohlene Größe für Genauigkeit](images/inter_touch_image11.jpeg)<br/> | **Wenn die Genauigkeit wichtig ist**<br/> Schließen, löschen und andere Aktionen mit schwerwiegenden Folgen können versehentliche Abzweigungen nicht leisten. Verwenden Sie 9x9 mm-Ziele, wenn beim Berühren des falschen Ziels mehr als zwei Gesten, fünf Sekunden oder eine wesentliche Kontext Änderung erforderlich ist.<br/>     |
| ![Mindestgröße von 5 x 5](images/inter_touch_image12.jpeg)<br/>                  | **Wenn es nicht passt**<br/> Wenn Sie sich für die Arbeit sorgen, ist es in Ordnung, 5 x 5 mm-Ziele zu verwenden, solange das falsche Ziel durch eine Bewegung korrigiert werden kann. Die Verwendung von 2 mm Abstand zwischen Zielen ist in diesem Fall äußerst wichtig.<br/> |



 

**Richtlinien für die Zielgröße für allgemeine Steuerelemente**

-   **Verwenden Sie für allgemeine Steuerelemente die empfohlenen Steuerelement Größen.** Die empfohlene Größe des Steuer Elements erfüllt die minimale Größe 23x23 Pixel (13x13 dlu), mit Ausnahme von Kontrollkästchen und Options Feldern (Ihre Text Breite wird etwas kompensiert), Spin-Steuerelemente (die nicht mit Finger Eingaben verwendet werden können, aber redundant sind) und Splitters.

    ![Screenshot, der ein Beispiel für allgemeine Steuerelemente, einschließlich Audiosteuerelemente, der Schaltfläche "Internet jetzt Durchsuchen" und eines Datei-Explorer-Fensters zeigt.](images/inter-touch-image17.png)

    Die empfohlenen Steuerelement Größen sind einfach touchabel.

-   **Verwenden Sie für Befehls Schaltflächen, die für die wichtigsten oder häufig verwendeten Befehle verwendet werden, eine minimale Größe von 40 x 40 Pixeln (23x22 DLUs), wenn dies praktikabel ist.** Dadurch erhalten Sie eine höhere Geschwindigkeit und Genauigkeit und sind auch für Benutzer besser geeignet.

    ![Screenshot, der mehrere Größen der e-Mail-Schaltfläche "Senden" anzeigt, wobei die kleinste und die größte Größe von links nach rechts beginnen.](images/inter-touch-image18.png)

    Verwenden Sie bei Bedarf größere Befehls Schaltflächen für wichtige oder häufig verwendete Befehle.

-   **Für andere Steuerelemente:**

    -   **Verwenden Sie größere Click-Ziele.** Legen Sie die Zielgröße bei kleinen Steuerelementen größer als das statisch sichtbare Benutzeroberflächen Element. Beispielsweise können 16x16-Pixel-Symbol Schaltflächen über eine 23x23 Pixel Click-Schaltfläche verfügen, und Textelemente können über Auswahl Rechtecke verfügen, die 8 Pixel breiter als der Text und 23 Pixel hoch sind.

        Richtig:

        ![Screenshot, der eine Symbolleiste mit der richtigen Zielgröße anzeigt.](images/inter-touch-image19.png)

        Falsch:

        ![Screenshot, der eine U I-Struktur mit einem falsch formatierten Zielbereich anzeigt.](images/inter-touch-image20.png)

        Richtig:

        ![Screenshot, der eine U I-Struktur mit der richtigen Größe für den Zielbereich anzeigt.](images/inter-touch-image21.png)

        In den richtigen Beispielen sind die Click-Ziele größer als die statisch sichtbaren Benutzeroberflächen Elemente.

    -   **Verwenden Sie redundante Click-Ziele.** Es ist zulässig, dass Click-Ziele kleiner als die Mindestgröße sind, wenn das Steuerelement über redundante Funktionen verfügt.

        Beispielsweise sind die vom Strukturansicht-Steuerelement verwendeten, progressiven Offenlegungs Dreiecke nur 6x9 Pixel, ihre Funktionalität ist jedoch mit den zugehörigen Element Bezeichnungen redundant.

        ![Screenshot, der eine U I-Struktur mit redundanten Klick Zielen anzeigt](images/inter-touch-image22.png)

        Die Dreiecke der Strukturansicht sind zu klein, um problemlos touchfähig zu sein, Sie sind jedoch in der Funktionalität mit ihren größeren zugeordneten Bezeichnungen redundant.

        Beachten Sie Systemmetriken. Nicht hart codieren von Größen. Falls erforderlich, können Benutzer die Systemmetriken oder dpi-Werte ändern, um Ihre Anforderungen zu erfüllen. Behandeln Sie dies jedoch als letztes Mittel, da Benutzer normalerweise nicht die Systemeinstellungen anpassen müssen, damit die Benutzeroberfläche verwendbar ist.

        ![Screenshot, der eine Standardmenü Höhe auf der linken Seite und eine größere Menü Höhe auf der rechten Seite anzeigt.](images/inter-touch-image23.png)

        In diesem Beispiel wurde die Systemmetrik für die Menü Höhe geändert.

Bearbeiten von Text

Das Bearbeiten von Text ist eine der anspruchsvollsten Interaktionen bei der Verwendung eines Fingers. Durch die Verwendung von eingeschränkten Steuerelementen, der entsprechenden Standardwerte und der automatischen Vervollständigung entfällt oder verringert sich die Notwendigkeit, Text einzugeben. Wenn Ihre APP jedoch die Bearbeitung von Text umfasst, können Sie Benutzer produktiver machen, indem Sie die Eingabe Benutzeroberfläche bei Verwendung von "Fingereingabe" standardmäßig um 150% erhöhen.

Ein e-Mail-Programm könnte z. b. die Benutzeroberfläche mit normaler touchable-Größe anzeigen, zoomt aber die Eingabe-UI auf 150 Prozent, um Nachrichten

![Screenshot, der eine e-Mail-Nachricht anzeigt](images/inter-touch-image24.png)

In diesem Beispiel wird die Eingabe Benutzeroberfläche auf 150 Prozent vergrößert.

### <a name="control-layout-and-spacing"></a>Layout und Abstand von Steuerelementen

Der Abstand zwischen Steuerelementen ist ein bedeutender Faktor für das einfache touchable von Steuerelementen. Die Zielgruppen Steuerung ist schneller, aber weniger präzise, wenn Sie einen Finger als Zeigegerät verwenden, was dazu führt, dass Benutzer eher außerhalb des vorgesehenen Ziels tippen. Wenn interaktive Steuerelemente sehr nah beieinander platziert werden, aber nicht tatsächlich berühren, klicken Benutzer möglicherweise auf inaktiven Bereich zwischen den Steuerelementen. Da das Klicken auf inaktiven Speicherplatz weder Ergebnis noch visuelles Feedback hat, sind die Benutzer häufig unsicher, was schief gelaufen ist.

**Passen Sie den Abstand basierend auf dem verwendeten Eingabegerät dynamisch an.** Dies ist besonders nützlich bei vorübergehenden Benutzeroberflächen wie Menüs und Flyouts.

**Geben Sie mindestens 5 Pixel (3 DLUs) zwischen den Zielregionen interaktiver Steuerelemente an.** Wenn kleine Steuerelemente zu stark voneinander entfernt sind, muss der Benutzer mit der Genauigkeit tippen, um zu vermeiden, dass auf das falsche Objekt angetippt wird.

**Vereinfachen Sie die Unterscheidung von Steuerelementen in Gruppen, indem Sie mehr als den empfohlenen vertikalen Abstand zwischen Steuerelementen verwenden.** Options Felder mit einer Höhe von 19 Pixeln sind z. b. kürzer als die empfohlene Mindestgröße von 23 Pixeln. Wenn vertikaler Speicherplatz verfügbar ist, können Sie ungefähr denselben Effekt wie die empfohlene Größe erzielen, indem Sie den standardmäßigen 7 Pixeln weitere 4 Pixel Abstand hinzufügen.

Richtig:

![Screenshot, der ein Standardbeispiel für den vertikalen Abstand zwischen Steuerelementen anzeigt.](images/inter-touch-image25.png)

Empfohlen:

![Screenshot, der ein Beispiel für Steuerelemente mit einem vertikalen Abstand zeigt.](images/inter-touch-image26.png)

Im Beispiel "besser" können Sie durch den zusätzlichen Abstand zwischen den Options Feldern leichter unterschieden werden.

Es kann Situationen geben, in denen zusätzlicher Abstand bei der Verwendung von Finger Eingaben wünschenswert ist, aber nicht bei Verwendung der Maus oder der Tastatur. Verwenden Sie in solchen Fällen nur einen komplexeren Entwurf, wenn eine Aktion mithilfe von "berühren" initiiert wird.

**Wählen Sie ein Layout aus, in dem die Steuerelemente nah an der Stelle platziert werden, an der Sie wahrscheinlich verwendet werden.** Behalten Sie die Aufgaben Interaktionen innerhalb eines kleinen Bereichs bei, wenn dies möglich ist, und suchen Sie die Steuerelemente, die sich in der Nähe des Orts befinden Vermeiden Sie längere Entfernungs Bewegungen, insbesondere bei häufigen Aufgaben und bei Drags.

Beachten Sie, dass die aktuelle Zeigerposition die nächstgelegene ist, die ein Ziel sein kann, sodass Sie für den Abruf trivial ist. Daher profitieren Kontextmenüs von der vollständigen Verwendung von FTTS, ebenso wie die von Microsoft Office verwendeten Mini Symbolleisten.

![Screenshot, der ein Beispiel für ein Kontextmenü und eine Mini Symbolleiste aus Microsoft Office nebeneinander zeigt.](images/inter-touch-image27.png)

**Vermeiden Sie das Platzieren kleiner Steuerelemente in der Nähe des Randes der APP oder der Anzeige.** Kleine Ziele in der Nähe der Kanten können schwierig zu berühren sein (die Anzeige von "bezels" kann sich auf Kanten Gesten beeinträchtigen). Um sicherzustellen, dass Steuerelemente problemlos als Ziel festzulegen sind, wenn ein Fenster maximiert ist, legen Sie entweder mindestens 23x23 Pixel (13 x 13 DLUs) fest, oder platzieren Sie Sie von der Fensterkante.

**Verwenden Sie den empfohlenen Abstand.** Der empfohlene Abstand ist Berührungs freundlich. Wenn Ihre APP jedoch von größerer Größe und Abstand profitieren kann, sollten Sie die empfohlene Größe und den Abstand bei Bedarf als Minimalwerte beachten.

**Geben Sie mindestens 5 Pixel (3 DLUs) zwischen interaktiven Steuerelementen an.** Dadurch wird Verwirrung verhindert, wenn Benutzer außerhalb des vorgesehenen Ziels tippen.

Fügen Sie in der Gruppe von Steuerelementen, wie z. b. Befehls Verknüpfungen, Kontrollkästchen, Options Felder und zwischen den Gruppen, mehr als den empfohlenen vertikalen Abstand hinzu. Dies erleichtert die Unterscheidung.

**Fügen Sie ggf. mehr als den empfohlenen vertikalen Abstand hinzu, wenn eine Aktion mithilfe von "berühren" initiiert wird.** Dadurch wird die Unterscheidung von Objekten vereinfacht, ohne dass mehr Platz zur Verwendung einer Tastatur oder Maus verwendet wird. Vergrößern Sie den Abstand um einen Drittel der normalen Größe oder mindestens 8 Pixel.

![image](images/inter-touch-image28.png)

In diesem Beispiel sind Windows 7-Task leisten-Sprung Listen geräumiger, wenn Sie mithilfe von Touchscreen angezeigt werden.

### <a name="interaction"></a>Interaktion

Wenn Sie die richtigen Steuerelemente verwenden, sind Sie nur ein Teil der Methode zu einer Touchscreen optimierten app. Außerdem müssen Sie das gesamte Interaktionsmodell beachten, das von diesen Steuerelementen unterstützt wird. Hier finden Sie einige Richtlinien, die Ihnen dabei helfen.

-   **Bewegen Sie den Mauszeiger.** Hover wird von den meisten Touchtechnologien nicht unterstützt, sodass Benutzer mit solchen Touchscreens keine Aufgaben ausführen können, für die ein Mauszeiger erforderlich ist.
-   **Für apps, die eine Texteingabe benötigen, integrieren Sie das Feature für die Berührungs Tastatur vollständig wie** folgt:
    -   Bereitstellen geeigneter Standardwerte für Benutzereingaben.
    -   Bereitstellen von Empfehlungen zur automatischen Vervollständigung.

    > [!Note]  
    > Entwickler: Weitere Informationen zur Integration der touchtastatur finden Sie unter [**itextinputpanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel).

     

-   **Hiermit wird Benutzern das Vergrößern der Inhalts Benutzeroberfläche ermöglicht, wenn das Programm Aufgaben enthält, die Text bearbeiten müssen.** Bei Verwendung der Fingereingabe empfiehlt es sich, automatisch zu 150 Prozent zu zoomen.
-   **Sorgen Sie für ein reibungsloses, reaktionsfähiges schwenken und Zoomen, wenn dies angebracht ist.** Zeichnen Sie schnell nach einer schwenken oder einem Zoom, um reaktionsfähig zu bleiben. Dies ist erforderlich, damit direkte Manipulation wirklich direkt ist.
-   **Stellen Sie während eines schwenken oder Zoom Punkts sicher, dass die Kontaktpunkte während der Bewegung unter dem Finger bleiben.** Andernfalls ist die schwenken oder der Zoom schwer zu steuern.
-   **Da Gesten gespeichert werden, weisen Sie Ihnen Bedeutungen zu, die über mehrere apps hinweg konsistent sind.** Setzen Sie Gesten mit fester Semantik nicht mit unterschiedlichen Bedeutungen. Verwenden Sie stattdessen eine geeignete App-spezifische Geste.

### <a name="forgiveness"></a>Erl

Die direkte Bearbeitung sorgt für natürliche, ausdrucksstarke, effiziente und ansprechende Berührungen. Wenn eine direkte Bearbeitung vorliegt, kann es jedoch zu einer versehentlichen Bearbeitung und somit zu einer Notwendigkeit von Vergebung kommen.

Mit "Vergebung" können Sie eine nicht gewünschte Aktion problemlos umkehren oder korrigieren. Durch die Bereitstellung von rückgängig machen Sie einen Eindruck, dass Sie eine einfache physische Trennung zwischen häufig verwendeten Befehlen und destruktiven Befehlen ermöglichen und es den Benutzern ermöglichen, Fehler problemlos zu beheben. Die zugeordnete Vergebung verhindert, dass unerwünschte Aktionen zuerst durchgeführt werden können. dazu können Sie eingeschränkte Steuerelemente und Bestätigungen für riskante Aktionen oder Befehle verwenden, die unbeabsichtigte Folgen haben.

-   **Stellen Sie einen Befehl rückgängig bereit.** Es ist am besten, eine einfache Methode zum rückgängig machen aller Befehle bereitzustellen, aber Ihre APP verfügt möglicherweise über einige Befehle, deren Auswirkung nicht rückgängig gemacht werden kann.
-   **Stellen Sie bei Bedarf gutes Feedback zur Verfügung, aber nehmen Sie keine Aktionen vor.** Dies ermöglicht es Benutzern, Fehler zu beheben, bevor Sie Sie vornehmen.
-   **Wenn dies praktikabel ist, können Benutzer problemlos Fehler beheben.** Wenn eine Aktion bei Finger aufwärts wirksam wird, gestatten Sie Benutzern, Fehler zu korrigieren, indem Sie bewegen, während der Finger immer noch nicht angezeigt wird.
-   **Wenn dies praktikabel ist, geben Sie an, dass eine direkte Manipulation nicht durchgeführt werden kann** Erlauben Sie die Verschiebung, aber lassen Sie das Objekt bei der Freigabe wieder zurück, um anzugeben, dass die Aktion erkannt wurde, aber nicht ausgeführt werden kann.
-   **Löschen Sie die physische Trennung zwischen häufig verwendeten Befehlen und destruktiven Befehlen.** Andernfalls können Benutzer die destruktive Befehle versehentlich berühren. Ein Befehl gilt als destruktiv, wenn seine Auswirkung weit verbreitet ist und er entweder nicht einfach rückgängig gemacht werden kann oder der Effekt nicht sofort erkennbar ist.
-   **Bestätigen Sie Befehle für riskante Aktionen oder Befehle, die unbeabsichtigte Folgen haben.** Verwenden Sie für diesen Zweck ein Bestätigungs Dialogfeld.
-   **Sie sollten ggf. alle anderen Aktionen bestätigen, die Benutzer bei der Verwendung von Finger Eingaben versehentlich ausführen, und die entweder unbemerkt oder schwer rückgängig gemacht werden können.** Diese werden normalerweise als Routine Bestätigungen bezeichnet und werden basierend auf der Annahme davon abgeraten, dass Benutzer solche Befehle nicht oft versehentlich mit einer Maus oder Tastatur ausgeben. Um unnötige Bestätigungen zu vermeiden, stellen Sie diese Bestätigungen nur dann vor, wenn der Befehl mithilfe von "berühren" initiiert wurde.

    Routine Bestätigungen sind für Interaktionen akzeptabel, die häufig von Benutzern versehentlich verwendet werden.

    Entwickler: Sie können mithilfe der [**Eingabe \_ Nachrichten \_ Quellen**](/windows/win32/api/winuser/ns-winuser-input_message_source) -API zwischen Mausereignissen und Berührungs Ereignissen unterscheiden.


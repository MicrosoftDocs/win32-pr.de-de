---
title: Touch
description: Alle Microsoft Windows-Anwendungen sollten eine hervorragende Toucherfahrung bieten. Und das Erstellen einer solchen Benutzeroberfläche ist einfacher als Sie denken.
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 68f73b7da9cf33dc20a3c0534044558e514284f024f11609ef9af4760ec79a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119029675"
---
# <a name="touch"></a>Touch

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Alle Microsoft Windows-Anwendungen sollten eine hervorragende Toucherfahrung bieten. Und das Erstellen einer solchen Benutzeroberfläche ist einfacher als Sie denken.

Toucheingabe bezieht sich darauf, mit einem oder mehreren Fingern Eingaben über eine Geräteanzeige bereitzustellen und mit Windows und Apps zu interagieren. Eine touchoptimierte App verfügt über eine Benutzeroberfläche und ein Interaktionsmodell, die für die größeren, weniger präzisen Kontaktbereiche der Berührung, die verschiedenen Formfaktoren von Touchgeräten und die vielen Positionen und Klammern ausgelegt sind, die Benutzer bei der Verwendung eines Touchgeräts annehmen können.

![Benutzer interagiert mit Tablet per Toucheingabe](images/inter_touch_image1.jpeg)

Jedes Eingabegerät hat seine Stärken. Die Tastatur eignet sich am besten für die Texteingabe und das Erteilen von Befehlen mit minimaler Handbewegung. Die Maus ist am besten geeignet, um effizient und präzise zu zeigen. Die Toucheingabe eignet sich am besten für objektmanipulation und einfache Befehle. Ein Stift eignet sich am besten für Freiformausdrücke, wie bei Handschrift und Zeichnung.

Windows 8.1 ist für Reaktionsfähigkeit, Genauigkeit und Benutzerfreundlichkeit mit Toucheingabe optimiert, während herkömmliche Eingabemethoden (z. B. Maus, Stift und Tastatur) vollständig unterstützt werden. Die Geschwindigkeit, Genauigkeit und taktilen Feedbacks, die herkömmliche Eingabemodi bieten, sind für viele Benutzer vertraut und ansprechend und möglicherweise besser für bestimmte Interaktionsszenarien geeignet.

Richtlinien im Zusammenhang mit Maus, Stift und Barrierefreiheit finden Sie in separaten Themen.

Wenn Sie über die Interaktionserfahrung für Ihre App nachdenken:

Gehen Sie nicht davon aus, dass eine Benutzeroberfläche auch gut für die Fingereingabe funktioniert, wenn sie gut für eine Maus funktioniert. Obwohl eine gute Mausunterstützung ein Anfang ist, hat eine gute Toucherfahrung einige zusätzliche Anforderungen.

Angenommen, eine Benutzeroberfläche funktioniert gut für einen Finger und funktioniert auch gut für einen Stift. Ihre App touchierbar zu machen, ist ein langer Weg, um auch eine gute Stiftunterstützung bereitzustellen. Der Hauptunterschied besteht darin, dass Finger eine bluntere Spitze haben, sodass sie größere Ziele benötigen.

Mit Toucheingabe können Sie Objekte und die Benutzeroberfläche direkt bearbeiten, was eine schnellere, natürlichere und ansprechendere Erfahrung ermöglicht.

## <a name="provide-a-great-touch-experience"></a>Bereitstellen einer hervorragenden Toucherfahrung

Sie sollten sicherstellen, dass Benutzer wichtige und wichtige Aufgaben mithilfe von Toucheingaben effizient ausführen können. Bestimmte App-Funktionen, z. B. Text- oder Pixelbearbeitung, sind jedoch möglicherweise nicht für Toucheingaben geeignet und können für das am besten geeignete Eingabegerät reserviert werden.

Wenn Sie nicht über viel Erfahrung mit der Entwicklung von Touch-Apps verfügen, ist es am besten, mit diesen Informationen zu lernen. Holen Sie sich einen Touchcomputer, legen Sie Maus und Tastatur beiseite, und verwenden Sie nur Ihre Finger, um mit Ihrer App zu interagieren. Wenn Sie über ein Tablet verfügen, experimentieren Sie damit, es an verschiedenen Positionen zu halten, z. B. auf dem Runde, flach auf einem Tisch oder in den Arm, während Sie stehen. Versuchen Sie, es im Hochformat und im Querformat zu verwenden.

Touchoptimierte Apps, die am besten mit touchbasierter Interaktion funktionieren, sind in der Regel:

-   **Natürlich und intuitiv.** Interaktionen sind so konzipiert, dass sie der Interaktion von Benutzern mit Objekten in der realen Welt entsprechen.
-   **Weniger intrusiv.** Die Toucheingabe ist unbeaufsichtigt und daher deutlich weniger ablenkend als das Eingeben oder Klicken.
-   **Tragbar.** Touchgeräte sind kompakter, da viele Aufgaben ohne Tastatur, Maus, Stift oder Touchpad ausgeführt werden können. Sie sind auch flexibler, da keine Arbeitsoberfläche erforderlich ist.
-   **Direkt und ansprechend.** Durch Toucheingaben haben Sie das Gefühl, dass Sie Objekte direkt auf dem Bildschirm bearbeiten.
-   **Weniger genau.** Benutzer können Objekte im Vergleich zu einer Maus oder einem Stift nicht so genau mit Touch erreichen.

Touch bietet ein natürliches, reales Interaktions-Gefühl. Direkte Bearbeitung und Animation vervollständigen diesen Eindruck, indem sie Objekten eine realistische, dynamische Bewegung und Feedback geben. Betrachten Sie beispielsweise ein Kartenspiel. Es ist nicht nur praktisch und einfach, Karten mit einem Finger zu ziehen, sondern die Erfahrung nimmt auch ein ansprechendes, reales Gefühl an, wenn Sie die Karten wie bei einem physischen Kartenstapel drehen können. Und wenn Sie versuchen, eine Karte zu verschieben, die nicht verschoben werden kann, ist es besser, die Karte zu verhindern, aber nicht zu verhindern, und sich wieder an Ort und Stelle zu bewegen, um eindeutig anzugeben, dass die Aktion erkannt wurde, aber nicht ausgeführt werden kann.

Wenn Ihre App bereits gut entworfen wurde, ist es glücklicherweise einfach, eine großartige Toucherfahrung bereitzustellen. Zu diesem Zweck ein gut entworfenes Programm:

-   **Stellt sicher,** dass die wichtigsten Aufgaben effizient mit einem Finger ausgeführt werden können (zumindest die Aufgaben, die nicht viel Eingabe oder detaillierte Pixelbearbeitung erfordern).
-   **Verwendet große Steuerelemente für die Toucheingabe.** Allgemeine Steuerelemente haben eine Mindestgröße von 23 x 23 Pixeln (13 x 13 DLUs), und die am häufigsten verwendeten Steuerelemente sind mindestens 40 x 40 Pixel (23x22 DLUs). Um nicht reagierende Verhaltensweisen zu vermeiden, sollten Benutzeroberflächenelemente über mindestens 5 Pixel (3 DLUs) Abstand zwischen ihnen verfügen. Stellen Sie für andere Steuerelemente sicher, dass sie über ein Klickziel von mindestens 23 x 23 Pixeln (13 x 13 DLU) verfügen, auch wenn ihre statische Darstellung viel kleiner ist. Weitere Informationen finden Sie unter Größen von Standardsteuerelements.
-   **Unterstützt Mauseingaben.** Die interaktiven Steuerelemente verfügen über klare, sichtbare Möglichkeiten. Objekte weisen Standardverhalten für die standardmäßigen Mausinteraktionen auf (einfaches und doppeltes Klicken mit der linken Maustaste, Rechtsklick, Ziehen und Bewegen des Mauszeigers).
-   **Unterstützt Tastatureingaben.** Die App bietet Standardmäßige Tastenkombinationszuweisungen, insbesondere für Navigations- und Bearbeitungsbefehle, die auch über Touchgesten generiert werden können.
-   **Stellt die Barrierefreiheit sicher.** Verwendet Benutzeroberflächenautomatisierung oder Microsoft Active Accessibility (MSAA), um programmgesteuerten Zugriff auf die Benutzeroberfläche für Hilfstechnologien bereitzustellen. Die App reagiert entsprechend auf Änderungen an Ausrichtung, Design, Gebietsschema und Systemmetrik.
-   **Beseitigt unnötige Interaktionen.** Um Daten- oder Systemzugriffsverluste zu verhindern, verwenden Sie die sichersten und sichersten Standardwerte. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählt die App die wahrscheinlichste oder bequemste Option aus.
-   **Stellt touch-Entsprechung für das Bewegen des Mauszeigers bereit.** Verlassen Sie sich nicht darauf, dass Sie mit dem Mauszeiger darauf zeigen, um eine Aktion auszuführen.
-   **Stellt sicher, dass Gesten sofort wirksam werden.** Halten Sie die Kontaktpunkte während der gestenweiten Geste unter den Fingern des Benutzers, was die Auswirkung der Gestenzuordnung direkt auf die Bewegung des Benutzers bereitstellt.
-   **Verwendet nach Möglichkeit Standardgesten.** Benutzerdefinierte Gesten nur für Interaktionen, die für Ihre App eindeutig sind.
-   **Stellt sicher, dass unerwünschte oder destruktive Befehle umgekehrt oder korrigiert werden können.** Versehentliche Aktionen sind wahrscheinlicher, wenn Toucheingaben verwendet werden.

## <a name="guidelines-for-touch-input"></a>Richtlinien für Toucheingaben

Mit Toucheingabe kann Ihre Windows-App physische Gesten verwenden, um die direkte Bearbeitung von Benutzeroberflächenelementen zu emulieren.

Berücksichtigen Sie diese bewährten Methoden beim Entwerfen Ihrer Touch-fähigen App:

**Reaktionsfähigkeit ist entscheidend für die Erstellung von Toucherfahrungen, die sich direkt und ansprechend anfühlen.** Um direkt zu sein, müssen Gesten sofort wirksam werden, und die Kontaktpunkte eines Objekts müssen während der gesamten Geste reibungslos unter den Fingern des Benutzers bleiben. Die Auswirkung der Toucheingabe sollte direkt der Bewegung des Benutzers zugeordnet werden. Wenn der Benutzer also beispielsweise seine Finger um 90 Grad dreht, sollte sich das Objekt ebenfalls um 90 Grad drehen. Jede Verzögerung, ungenaue Reaktion, Kontaktverlust oder ungenaue Ergebnisse zerstören die Wahrnehmung der direkten Manipulation und der Qualität.

**Konsistenz ist entscheidend für die Erstellung von Toucherfahrungen, die sich natürlich und intuitiv anfühlen.** Sobald Benutzer eine Standardgeste erlernen, erwarten sie, dass diese Geste für alle Apps die gleiche Wirkung hat. Um Verwirrung und Frust zu vermeiden, weisen Sie Standardgesten niemals nicht standardmäßige Bedeutungen zu. Verwenden Sie stattdessen benutzerdefinierte Gesten für Interaktionen, die für Ihr Programm eindeutig sind.

Als Nächstes beschreiben wir die Windows Touchsprache, aber bevor wir weitermachen, finden Sie hier eine kurze Liste der grundlegenden Toucheingabebegriffe.

-   **Geste**

    Eine Geste ist die physische Aktion oder Bewegung, die auf dem Eingabegerät (Finger, Finger, Stift/Stift, Maus usw.) ausgeführt wird. Um beispielsweise einen Befehl zu starten, zu aktivieren oder aufzurufen, verwenden Sie einen einfachen Tippen mit dem Finger für ein Touch- oder Touchpadgerät (entspricht einem Linksklick mit einer Maus, einem Tippen mit einem Stift oder der EINGABETASTE auf einer Tastatur).

-   **Manipulation**

    Eine Manipulation ist die sofortige Reaktion oder Reaktion in Echtzeit, die ein Objekt oder eine Benutzeroberfläche auf eine Geste hat. Beispielsweise führen sowohl die Schiebe- als auch die Wischgeste in der Regel dazu, dass sich ein Element oder eine Benutzeroberfläche in irgendeiner Weise bewegt.

    Das Endergebnis einer Bearbeitung, wie sie durch das -Objekt auf dem Bildschirm und in der Benutzeroberfläche manifestiert wird, ist die Interaktion.

-   **Interaktion**

    Interaktionen hängen davon ab, wie eine Manipulation interpretiert wird, und von dem Befehl oder der Aktion, die bzw. die sich aus der Bearbeitung ergibt. Beispielsweise können Objekte mithilfe der Schiebe- und Wischgesten verschoben werden, aber die Ergebnisse unterscheiden sich, je nachdem, ob ein Entfernungsschwellenwert überschritten wird. Folie kann verwendet werden, um ein Objekt zu ziehen oder eine Ansicht zu schwenken, während Wischbewegung verwendet werden kann, um ein Element auszuwählen oder eine App-Leiste anzuzeigen.

### <a name="the-windows-touch-language"></a>Die Windows Touchsprache

Windows bietet einen präzisen Satz von Touchinteraktionen, die im gesamten System verwendet werden. Wenn Sie diese Touchsprache konsistent anwenden, wird Ihre App mit dem vertraut, was Benutzer bereits wissen. Dies erhöht das Vertrauen der Benutzer, da Ihre App einfacher zu erlernen und zu verwenden ist. Weitere Informationen zur Implementierung von Touchsprachen finden Sie unter Gesten, Bearbeitungen und Interaktionen.

**Halten Sie gedrückt, um zu lernen.**

Die Geste zum Drücken und Halten zeigt detaillierte Informationen oder Lernvisuals (z. B. eine QuickInfo oder ein Kontextmenü) an, ohne einen Commit für eine Aktion oder einen Befehl durchzuführen. Schwenken ist weiterhin möglich, wenn eine gleitende Geste gestartet wird, während das Visual angezeigt wird.

> [!IMPORTANT]
> Sie können für die Auswahl drücken und halten, wenn horizontales und vertikales Schwenken aktiviert ist.

 

Eingangszustand: Ein oder zwei Finger in Kontakt mit dem Bildschirm.

Bewegung: Keine Bewegung.

Beendigungszustand: Der letzte Finger nach oben beendet die Geste.

Effekt: Zeigt weitere Informationen an.

![Toucheingabe \- \- zum \-learn.png](images/inter-touch-image2.png)

Die Geste zum Drücken und Halten.

**Darauf zeigen (Hover)**

Der Mauszeiger ist eine nützliche Interaktion, da Benutzer zusätzliche Informationen durch Tipps abrufen können, bevor sie eine Aktion initiieren. Wenn Sie sich diese Tipps ansehen, können Benutzer sich sicherer fühlen und Fehler reduzieren.

Leider wird das Bewegen des Mauszeigers von Touchtechnologien nicht unterstützt, sodass Benutzer nicht mit dem Mauszeiger zeigen können, wenn sie einen Finger verwenden. Die einfache Lösung für dieses Problem besteht darin, den Mauszeiger vollständig zu nutzen, aber nur auf eine Weise, die nicht erforderlich ist, um eine Aktion auszuführen. In der Praxis bedeutet dies in der Regel, dass die Aktion auch durch Klicken ausgeführt werden kann, jedoch nicht unbedingt auf die gleiche Weise.

![Screenshot, der ein Beispiel für die Interaktion mit dem Mauszeiger neben einem Beispiel für die Klickaktion zeigt.](images/inter-touch-image13.png)

In diesem Beispiel können Benutzer das heutige Datum anzeigen, indem sie entweder mit dem Mauszeiger zeigen oder darauf klicken.

**Tippen Sie auf die primäre Aktion.**

Durch Tippen auf ein Element wird seine primäre Aktion aufgerufen, z. B. das Starten einer App oder das Ausführen eines Befehls.

Eingangszustand: Ein Finger, der mit dem Bildschirm oder Touchpad in Kontakt ist und vor dem Zeitschwellenwert für eine Interaktion durch Drücken und Halten aufgehoben wurde.

Bewegung: Keine Bewegung.

Beendigungszustand: Der Finger nach oben beendet die Geste.

Auswirkung: Starten Sie eine App, oder führen Sie einen Befehl aus.

![Tippen \-primary.png \-](images/inter-touch-image3.png)

Die Tippbewegung.

**Schieben zum Schwenken**

Die Folie wird hauptsächlich zum Schwenken von Interaktionen verwendet, kann aber auch zum Verschieben (wobei das Schwenken auf eine Richtung beschränkt ist) sowie zum Zeichnen oder Schreiben verwendet werden. Folie kann auch verwendet werden, um kleine, stark gepackte Elemente durch Bereinigung anzuzielen (indem der Finger über verwandte Objekte wie Optionsfelder gleitet).

Eingangszustand: Ein oder zwei Finger in Kontakt mit dem Bildschirm.

Bewegung: Ziehen Sie , wobei alle zusätzlichen Finger relativ zueinander an derselben Position verbleiben.

Beendigungszustand: Der letzte Finger nach oben beendet die Geste.

Effekt: Verschieben Sie das zugrunde liegende Objekt direkt und sofort, während sich die Finger bewegen. Achten Sie darauf, den Kontaktpunkt während der Geste unter dem Finger zu halten.

![touch \-slide.png](images/inter-touch-image4.png)

Die Schwenkbewegung.

**Wischen zum Auswählen, Befehl und Verschieben**

Verschiebt den Finger einen kurzen Abstand, senkrecht zur Schwenkrichtung (wobei das Schwenken auf eine Richtung beschränkt ist), wählt Objekte in einer Liste oder einem Raster aus. Zeigen Sie die App-Leiste mit relevanten Befehlen an, wenn Objekte ausgewählt werden.

Eingangszustand: Mindestens ein Finger berührt den Bildschirm.

Bewegung: Ziehen Sie einen kurzen Abstand, und heben Sie ihn an, bevor der Entfernungsschwellenwert für eine Bewegungsinteraktion auftritt.

Beendigungszustand: Der letzte Finger nach oben beendet die Geste.

Auswirkung: Das zugrunde liegende Objekt wird ausgewählt oder verschoben, oder die App-Leiste wird angezeigt. Achten Sie darauf, den Kontaktpunkt während der Geste unter dem Finger zu halten.

![d: \\ sdkenlistment \\ m \- ux design m \- \\ \- ux design images touch \- \\ \\ \-swipe.png](images/inter-touch-image5.png)

Die Wischbewegung.

**Zusammendrücken/Aufziehen: Zoom**

Die Gesten "Pinch" und "Stretch" werden für drei Arten von Interaktionen verwendet: optischer Zoom, Größenänderung und semantischer Zoom.

Der optische Zoom passt die Vergrößerungsebene des gesamten Inhaltsbereichs an, um eine detailliertere Ansicht des Inhalts zu erhalten. Im Gegensatz dazu ist die Größenänderung eine Technik zum Anpassen der relativen Größe eines oder mehrerer Objekte innerhalb eines Inhaltsbereichs, ohne die Ansicht in den Inhaltsbereich zu ändern.

Der semantische Zoom ist eine touchoptimierte Technik zum Darstellen und Navigieren von strukturierten Daten oder Inhalten in einer einzelnen Ansicht (z. B. der Ordnerstruktur eines Computers, einer Bibliothek mit Dokumenten oder einem Fotoalben), ohne dass Steuerelemente zum Schwenken, Scrollen oder Strukturansicht erforderlich sind. Der semantische Zoom bietet zwei verschiedene Ansichten desselben Inhalts, indem Sie beim Vergrößern mehr Details und beim Verkleinern weniger Details anzeigen können.

Eingangszustand: Zwei Finger, die gleichzeitig mit dem Bildschirm in Kontakt treten.

Bewegung: Finger bewegen sich auf einer Achse voneinander (Gestreckt) oder zusammen (Zusammendrücken).

Beendigungszustand: Jeder Finger nach oben beendet die Geste.

Effekt: Vergrößern oder verkleinern Sie das zugrunde liegende Objekt direkt und sofort, wenn sich die Finger auf der Achse trennen oder nähern. Achten Sie darauf, die Kontaktpunkte während der Geste unter dem Finger zu halten.

![Landing \-areazoom.png](images/inter-touch-image6.png)

Die Zoomgeste.

**Turn to rotate (Drehen aktivieren)**

Das Drehen mit zwei oder mehr Fingern bewirkt, dass ein Objekt gedreht wird. Drehen Sie das Gerät selbst, um den ganzen Bildschirm zu drehen.

Eingangszustand: Zwei Finger, die gleichzeitig mit dem Bildschirm in Kontakt treten.

Bewegung: Der eine oder beide Finger drehen sich um den anderen und bewegen sich senkrecht zur Linie zwischen ihnen.

Beendigungszustand: Jeder Finger nach oben beendet die Geste.

Effekt: Drehen Sie das zugrunde liegende Objekt in derselben Menge, in der sich die Finger gedreht haben. Achten Sie darauf, die Kontaktpunkte während der Geste unter dem Finger zu halten.

![touch \-turn.png](images/inter-touch-image7.png)

Die Drehbewegung.

Die Drehung ist nur für bestimmte Objekttypen sinnvoll, sodass sie nicht einem System Windows Interaktion zugeordnet wird.

Die Rotation wird häufig von verschiedenen Personen unterschiedlich durchgeführt. Einige Ziehen es vor, einen Finger um einen Pivotfinger zu drehen, während andere es vorziehen, beide Finger in einer kreisförmigen Bewegung zu drehen. Die meisten Benutzer verwenden eine Kombination der beiden, wobei ein Finger mehr bewegt als der andere. Während die gleichmäßige Drehung in einen beliebigen Winkel die beste Interaktion ist, empfiehlt es sich in vielen Kontexten, z. B. bei der Fotoanzeige, sich auf die nächste 90-Grad-Drehung zu setzen, sobald der Benutzer loslässt. Bei der Fotobearbeitung können Sie eine kleine Drehung verwenden, um das Foto zu begradigen.

**Wischen vom Edge für App-Befehle**

Wenn Sie den Finger kurz vom unteren oder oberen Rand des Bildschirms wischen, werden App-Befehle in einer App-Leiste angezeigt.

Einstiegszustand: Ein oder mehrere Finger berühren die Blende.

Bewegung: Ziehen Sie einen kurzen Abstand auf den Bildschirm, und heben Sie ihn an.

Beendigungszustand: Der letzte Finger nach oben beendet die Geste.

Auswirkung: App-Leiste wird angezeigt.

![touch \- swipe \- bottom \-edge.png](images/inter-touch-image8.png)

![touch \- swipe \- side \-edge.png](images/inter-touch-image9.png)

Die Wischbewegung von der Kante.

Entwickler: Weitere Informationen finden Sie unter [**DIRECTMANIPULATION \_ CONFIGURATION-Enumeration.**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration)

### <a name="control-usage"></a>Steuern der Nutzung

Hier stellen wir einige Richtlinien für die Optimierung von Steuerelementen für die Touchnutzung bereit.

-   **Verwenden sie allgemeine Steuerelemente.** Die gängigsten Steuerelemente sind so konzipiert, dass sie eine gute Toucherfahrung unterstützen.
-   **Wählen Sie benutzerdefinierte Steuerelemente aus, die die Toucheingabe unterstützen sollen.** Möglicherweise benötigen Sie benutzerdefinierte Steuerelemente, um die speziellen Funktionen Ihres Programms zu unterstützen. Wählen Sie benutzerdefinierte Steuerelemente aus, die:
    -   Kann groß genug sein, um eine einfache Ausrichtung und Bearbeitung zu erreichen.
    -   Wenn sie bearbeitet werden, bewegen und reagieren Sie auf die Art und Weise, wie sich reale Objekte bewegen und reagieren, z. B. durch Bewegung und Reibung.
    -   Sie sind verzeihend, indem Sie es Benutzern ermöglichen, Fehler leicht zu korrigieren.
    -   Sie verzeihen ungenauigkeit durch Klicken und Ziehen. Objekte, die in der Nähe ihres Ziels gelöscht werden, sollten an der richtigen Stelle liegen.
    -   Erhalten Sie klares visuelles Feedback, wenn sich der Finger über dem Steuerelement befindet.
-   **Verwenden Sie eingeschränkte Steuerelemente.** Eingeschränkte Steuerelemente wie Listen und Schieberegler können besser sein, wenn sie für die einfache Toucheingabe konzipiert sind, als schränkte Steuerelemente wie Textfelder, da sie den Bedarf an Texteingaben reduzieren.
-   **Geben Sie die entsprechenden Standardwerte an.** Wählen Sie standardmäßig die sicherste Option (um Datenverlust oder Systemzugriff zu verhindern) und die sicherste Option aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Option aus, um unnötige Interaktionen zu vermeiden.
-   **Geben Sie die automatische Vervollständigung von Text an.** Stellt eine Liste der wahrscheinlichsten Werte bzw. der letzten Eingabewerte zur einfacheren Texteingabe zur.
-   **Stellen Sie für wichtige Aufgaben,** die mehrfache Auswahl verwenden, eine Option zur Verwendung einer Kontrollkästchenliste zur Verfügung, wenn normalerweise eine Standardmäßige Mehrfachauswahlliste verwendet wird.

### <a name="control-sizes-and-touch-targeting"></a>Steuerelementgrößen und Touchadressierung

Aufgrund des großen Oberflächenbereichs der Fingerspitze können kleine Steuerelemente, die zu nah beieinander liegen, schwierig präzise als Ziel verwendet werden.

Im Allgemeinen ist eine Steuerelementgröße von 23 x 23 Pixel (13 x 13 DLUs) eine gute minimale interaktive Steuerelementgröße für jedes Eingabegerät. Im Gegensatz dazu sind die Drehungssteuerelemente bei 15 x 11 Pixeln viel zu klein, um sie effektiv mit touch verwenden zu können.

![Screenshot: Breite und Höhe der Schaltflächen für die Auswahl nach oben und unten mit einer Breite von 9 DLUs (15 Pixel) und einer Höhe von 5 DLUs (9 Pixel)](images/inter-touch-image14.png)

Beachten Sie, dass die Mindestgröße tatsächlich auf dem physischen Bereich basiert, nicht auf Layoutmetriken wie Pixeln oder DLUs. Untersuchungen deuten darauf hin, dass der minimale Zielbereich für eine effiziente, genaue Interaktion mit einem Finger 6 x 6 Millimeter (mm) beträgt. Dieser Bereich wird in Layoutmetriken wie die folgenden übersetzt:



| Schriftart             | Millimeter | Relative Pixel | DLUs  |
|------------------|-------------|-----------------|-------|
| 9 Punkt Segoe UI | 6x6         | 23 x 23           | 13x13 |
| 8 Punkt Tahoma   | 6x6         | 23 x 23           | 15 x 14 |



 

Darüber hinaus zeigen Untersuchungen, dass eine Mindestgröße von 10 x 10 mm (ca. 40 x 40 Pixel) eine bessere Geschwindigkeit und Genauigkeit ermöglicht und den Benutzern auch ein besseres Gefühl gibt. Wenn dies praktisch ist, verwenden Sie diese größere Größe für Befehlsschaltflächen, die für die wichtigsten oder am häufigsten verwendeten Befehle verwendet werden.

Das Ziel ist nicht, über riesige Steuerelemente zu verfügen, sondern nur über Steuerelemente, die problemlos mit Touch touch verwendet werden können.

![Screenshot, der die symbolleiste Microsoft Word mit hervorgehobener Schaltfläche "A B C Spelling & Grammar" mit einer Höhe von 41 DLU und einer Breite von 40 DLU zeigt.](images/inter-touch-image15.png)

In diesem Beispiel verwendet Microsoft Word Schaltflächen, die größer als 10x10 mm sind, für die wichtigsten Befehle.

![Screenshot, der den Windows zeigt.](images/inter-touch-image16.png)

Diese Version des Rechners verwendet Schaltflächen, die größer als 10x10 mm sind, für die am häufigsten verwendeten Befehle.

Es gibt keine perfekte Größe für Touchziele. Unterschiedliche Größen funktionieren für unterschiedliche Situationen. Aktionen mit schwerwiegenden Folgen (z. B. Löschen und Schließen) oder häufig verwendete Aktionen sollten große Touchziele verwenden. Selten verwendete Aktionen mit geringfügigen Folgen können kleine Ziele verwenden.

**Richtlinien für die Zielgröße für benutzerdefinierte Steuerelemente**



| Größenrichtlinie                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Empfohlene Mindestgröße von 7 x 7](images/inter_touch_image10.jpeg)<br/>      | **7 x 7 mm: Empfohlene Mindestgröße**<br/> 7x7 mm ist eine gute Mindestgröße, wenn das Berühren des falschen Ziels mit einer oder zwei Gesten oder innerhalb von fünf Sekunden korrigiert werden kann. Das Auf padding zwischen Zielen ist genauso wichtig wie die Zielgröße.<br/>                               |
| ![Empfohlene Größe von 9 x 9 für Genauigkeit](images/inter_touch_image11.jpeg)<br/> | **Wenn Genauigkeit wichtig ist**<br/> Schließen, Löschen und andere Aktionen mit schwerwiegenden Folgen können sich keine versehentlichen Tippen leisten. Verwenden Sie 9 x 9 mm-Ziele, wenn das Berühren des falschen Ziels mehr als zwei Gesten, fünf Sekunden oder eine größere Kontextänderung erfordert, um dies zu korrigieren.<br/>     |
| ![Mindestgröße von 5 x 5](images/inter_touch_image12.jpeg)<br/>                  | **Wenn es einfach nicht passt**<br/> Wenn Sie die passenden Dinge suchen, ist es in Ordnung, 5x5 mm-Ziele zu verwenden, solange die Berührung des falschen Ziels mit einer Geste korrigiert werden kann. Die Verwendung von 2 mm Auf padding zwischen Zielen ist in diesem Fall äußerst wichtig.<br/> |



 

**Richtlinien zur Zielgröße für allgemeine Steuerelemente**

-   **Verwenden Sie für allgemeine Steuerelemente die empfohlenen Steuerelementgrößen.** Die empfohlene Steuerelementgröße erfüllt die Mindestgröße von 23 x 23 Pixeln (13 x 13 DLU), mit Ausnahme von Kontrollkästchen und Optionsfeldern (deren Textbreite ein gewisses Ausmaß ausgleicht), Drehsteuerelementen (die nicht mit Touch touch verwendet werden können, aber redundant sind) und Splittern.

    ![Screenshot eines Beispiels für allgemeine Steuerelemente, einschließlich Audiosteuerelementen, der Schaltfläche "Jetzt im Internet durchsuchen" und eines Datei-Explorer-Fensters.](images/inter-touch-image17.png)

    Die empfohlenen Steuerelementgrößen sind leicht zu berühren.

-   **Verwenden Sie für Befehlsschaltflächen, die für die wichtigsten oder am häufigsten verwendeten Befehle verwendet werden, nach Möglichkeit eine Mindestgröße von 40 x 40 Pixel (23 x 22 DLUs).** Dies führt zu einer besseren Geschwindigkeit und Genauigkeit und ist auch für Benutzer komfortabler.

    ![Screenshot, der mehrere Größen einer E-Mail-Schaltfläche "Senden" zeigt, bei der die kleinsten bis größten Größen von links nach rechts beginnen.](images/inter-touch-image18.png)

    Verwenden Sie nach Möglichkeit größere Befehlsschaltflächen für wichtige oder häufig verwendete Befehle.

-   **Für andere Steuerelemente:**

    -   **Verwenden Sie größere Klickziele.** Bei kleinen Steuerelementen sollten Sie die Zielgröße größer als das statisch sichtbare Benutzeroberflächenelement machen. Beispielsweise können Symbolschaltflächen mit 16 x 16 Pixeln über 23 x 23 Pixel Klickzielschaltflächen verfügen, und Textelemente können Auswahlrechtecke aufweisen, die 8 Pixel breiter als der Text und 23 Pixel hoch sind.

        Richtig:

        ![Screenshot: Symbolleiste mit der richtigen Zielgröße](images/inter-touch-image19.png)

        Falsch:

        ![Screenshot: U I-Struktur mit falsch dimensioniertem Zielbereich](images/inter-touch-image20.png)

        Richtig:

        ![Screenshot: U I-Struktur mit der richtigen Größe für den Zielbereich](images/inter-touch-image21.png)

        In den richtigen Beispielen sind die Klickziele größer als die statisch sichtbaren Benutzeroberflächenelemente.

    -   **Verwenden Sie redundante Klickziele.** Es ist akzeptabel, dass Klickziele kleiner als die Mindestgröße sind, wenn dieses Steuerelement über redundante Funktionen verfügt.

        Beispielsweise sind die progressiven Offenlegungsdreiecke, die vom Strukturansicht-Steuerelement verwendet werden, nur 6 x 9 Pixel, aber ihre Funktionalität ist mit ihren zugeordneten Elementbezeichnungen redundant.

        ![Screenshot, der eine U I-Struktur mit redundanten Klickzielen zeigt.](images/inter-touch-image22.png)

        Die Dreiecke der Strukturansicht sind zu klein, um leicht zu berühren, aber sie sind in der Funktionalität mit ihren größeren zugeordneten Bezeichnungen redundant.

        Systemmetriken werden beachtet. Keine hartcodierten Größen. Bei Bedarf können Benutzer die Systemmetriken oder dpi ändern, um ihre Anforderungen zu erfüllen. Behandeln Sie dies jedoch als letzten Ausweg, da Benutzer die Systemeinstellungen normalerweise nicht anpassen müssen, um die Benutzeroberfläche nutzbar zu machen.

        ![Screenshot: Standardmenühöhe auf der linken Seite und größere Menühöhe auf der rechten Seite](images/inter-touch-image23.png)

        In diesem Beispiel wurde die Systemmetrik für die Menühöhe geändert.

Bearbeiten von Text

Das Bearbeiten von Text ist eine der anspruchsvollsten Interaktionen bei Verwendung eines Fingers. Durch die Verwendung von eingeschränkten Steuerelementen, entsprechenden Standardwerten und automatischer Vervollständigung wird die Texteingabe entfällt oder reduziert. Wenn Ihre App jedoch das Bearbeiten von Text umfasst, können Sie Benutzer produktiver machen, indem Sie die Eingabebenutzeroberfläche standardmäßig auf bis zu 150 Prozent zoomen, wenn Toucheingaben verwendet werden.

Beispielsweise könnte ein E-Mail-Programm die Benutzeroberfläche mit normaler berührbarer Größe anzeigen, aber die Eingabebenutzeroberfläche auf 150 Prozent zoomen, um Nachrichten zu verfassen.

![Screenshot: E-Mail-Adresse](images/inter-touch-image24.png)

In diesem Beispiel wird die Eingabebenutzeroberfläche auf 150 Prozent vergrößert.

### <a name="control-layout-and-spacing"></a>Layout und Abstand von Steuerelementen

Der Abstand zwischen Steuerelementen ist ein wichtiger Faktor, um Steuerelemente leicht zu berühren. Das Ziel ist schneller, aber weniger präzise, wenn ein Finger als Zeigegerät verwendet wird, was dazu führt, dass Benutzer häufiger außerhalb ihres vorgesehenen Ziels tippen. Wenn interaktive Steuerelemente sehr nah beieinander platziert werden, sich aber nicht tatsächlich berühren, können Benutzer auf inaktiven Raum zwischen den Steuerelementen klicken. Da das Klicken auf einen inaktiven Bereich kein Ergebnis oder visuelles Feedback hat, sind Benutzer häufig unsicher, was schief gelaufen ist.

**Passen Sie den Abstand basierend auf dem verwendeten Eingabegerät dynamisch an.** Dies ist besonders nützlich bei vorübergehenden Benutzeroberflächen wie Menüs und Flyouts.

**Stellen Sie mindestens 5 Pixel (3 DLUs) Speicherplatz zwischen den Zielregionen interaktiver Steuerelemente zur Verfügung.** Wenn die Leerzeichen kleiner Steuerelemente zu eng sind, muss der Benutzer präzise tippen, um zu vermeiden, dass auf das falsche Objekt tippt.

**Vereinfachen Sie die Unterscheidung von Steuerelementen innerhalb von Gruppen, indem Sie mehr als den empfohlenen vertikalen Abstand zwischen Steuerelementen verwenden.** Beispielsweise sind Optionsfelder mit einer Höhe von 19 Pixeln kürzer als die empfohlene Mindestgröße von 23 Pixeln. Wenn vertikaler Speicherplatz verfügbar ist, können Sie ungefähr den gleichen Effekt wie bei der empfohlenen Größe erzielen, indem Sie den standardmäßigen 7 Pixeln weitere 4 Pixel Abstand hinzufügen.

Richtig:

![Screenshot: Standardbeispiel für vertikalen Abstand zwischen Steuerelementen](images/inter-touch-image25.png)

Empfohlen:

![Screenshot: Beispiel für Steuerelemente mit vertikalem Abstand](images/inter-touch-image26.png)

Im besseren Beispiel erleichtert der zusätzliche Abstand zwischen den Optionsfeldern die Unterscheidung.

Es kann Situationen geben, in denen zusätzliche Abstande wünschenswert sind, wenn Toucheingaben verwendet werden, aber nicht bei Verwendung der Maus oder Tastatur. Verwenden Sie in solchen Fällen nur dann einen läufigeren Entwurf, wenn eine Aktion mit touch initiiert wird.

**Wählen Sie ein Layout aus, das Steuerelemente in der Nähe des Orts platziert, an dem sie am wahrscheinlichsten verwendet werden.** Halten Sie Aufgabeninteraktionen nach Möglichkeit in einem kleinen Bereich, und suchen Sie Steuerelemente in der Nähe des Orts, an dem sie am wahrscheinlichsten verwendet werden. Vermeiden Sie Handbewegungen mit langer Entfernung, insbesondere bei häufigen Aufgaben und bei Ziehbewegungen.

Beachten Sie, dass die aktuelle Zeigerposition am nächsten liegt, die einem Ziel am nächsten liegt, was das Erfassen trivial macht. Daher nutzen Kontextmenüs das Fitts-Recht genauso wie die mini-Symbolleisten, die von der Microsoft Office.

![Screenshot, der ein Beispiel für ein Kontextmenü und eine Minisymbolleiste von Microsoft Office nebeneinander zeigt.](images/inter-touch-image27.png)

**Platzieren Sie kleine Steuerelemente nicht in der Nähe des Rands der App oder der Anzeige.** Kleine Ziele in der Nähe von Rändern können schwierig zu berühren sein (Display-Blenden können Kantengesten beeinträchtigen). Um sicherzustellen, dass Steuerelemente beim Maximieren eines Fensters einfach als Ziel festgelegt werden können, legen Sie sie entweder auf mindestens 23 x 23 Pixel (13 x 13 DLUs) fest, oder platzieren Sie sie weg vom Fensterrand.

**Verwenden Sie den empfohlenen Abstand.** Der empfohlene Abstand ist touch-nutzerfreundlich. Wenn Ihre App jedoch von größerer Größe und größerem Abstand profitieren kann, sollten Sie die empfohlene Größen- und Abstandsgröße als Mindestgröße betrachten.

**Stellen Sie mindestens 5 Pixel (3 DLUs) Speicherplatz zwischen interaktiven Steuerelementen zur Verfügung.** Dies verhindert Verwirrung, wenn Benutzer außerhalb ihres vorgesehenen Ziels tippen.

Fügen Sie in Gruppen von Steuerelementen, z. B. Befehlslinks, Kontrollkästchen und Optionsfeldern, sowie zwischen den Gruppen mehr als den empfohlenen vertikalen Abstand hinzu. Dies erleichtert die Unterscheidung.

**Erwägen Sie, mehr als den empfohlenen vertikalen Abstand dynamisch zu verwenden, wenn eine Aktion mit touch initiiert wird.** Dadurch lassen sich Objekte einfacher unterscheiden, ohne bei Verwendung einer Tastatur oder Maus mehr Platz zu nehmen. Erhöhen Sie den Abstand um ein Drittel seiner normalen Größe oder um mindestens 8 Pixel.

![image](images/inter-touch-image28.png)

In diesem Beispiel sind Windows 7 Taskleisten-Sprunglisten schwieriger, wenn sie mit touch angezeigt werden.

### <a name="interaction"></a>Interaktion

Wenn Sie die richtigen Steuerelemente verwenden, erhalten Sie nur einen Teil des Wegs zu einer touchoptimierten App. Sie müssen auch das gesamte Interaktionsmodell berücksichtigen, das diese Steuerelemente unterstützen. Hier finden Sie einige Richtlinien, die Ihnen dabei helfen.

-   **Machen Sie den Hover redundant.** Das Hovern wird von den meisten Touchtechnologien nicht unterstützt, sodass Benutzer mit solchen Touchscreens keine Aufgaben ausführen können, für die das Hovern erforderlich ist.
-   **Für Apps, die Texteingaben benötigen, integrieren Sie das Touchtastaturfeature vollständig, indem** Sie:
    -   Bereitstellen geeigneter Standardwerte für Benutzereingaben.
    -   Geben Sie gegebenenfalls Vorschläge zur automatischen Vervollstehung an.

    > [!Note]  
    > Entwickler: Weitere Informationen zur Integration der Touchtastatur finden Sie unter [**ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel).

     

-   **Benutzern das Zoomen der Inhaltsbenutzeroberfläche ermöglichen, wenn Ihr Programm Über aufgaben verfügt, die die Bearbeitung von Text erfordern.** Erwägen Sie, automatisch auf 150 Prozent zu zoomen, wenn touch verwendet wird.
-   **Sorgen Sie für ein reibungsloses, reaktionsfähiges Schwenken und Zoomen, wenn dies sinnvoll ist.** Sie können nach einem Schwenken oder Zoomen schnell neu gezeichnet werden, um reaktionsfähig zu bleiben. Dies ist erforderlich, damit sich die direkte Bearbeitung wirklich direkt anfühlt.
-   **Stellen Sie während eines Schwenkens oder Zooms sicher, dass die Kontaktpunkte während der gesamten Geste unter dem Finger bleiben.** Andernfalls ist das Schwenken oder Zoomen schwierig zu steuern.
-   **Da Gesten auswendig sind, weisen Sie ihnen Bedeutungen zu, die appsübergreifend konsistent sind.** Geben Sie Gesten mit fester Semantik keine unterschiedlichen Bedeutungen. Verwenden Sie stattdessen eine entsprechende app-spezifische Geste.

### <a name="forgiveness"></a>Vergebung

Die direkte Manipulation macht touch natürlich, ausdrucksstark, effizient und ansprechend. Bei direkter Manipulation kann es jedoch zu versehentlichen Manipulationen und somit zur Notwendigkeit von Verunrendung kommt.

Selbstgefädigtheit ist die Fähigkeit, eine unerwünschte Aktion einfach umzukehren oder zu korrigieren. Sie machen eine Berührungserfahrung, indem Sie rückgängig machen, ein gutes visuelles Feedback geben, eine klare physische Trennung zwischen häufig verwendeten Befehlen und destruktiven Befehlen haben und Es Benutzern ermöglichen, Fehler einfach zu korrigieren. Im Zusammenhang mit Dereinstigkeit wird verhindert, dass unerwünschte Aktionen von anfang an stattfinden. Dies können Sie tun, indem Sie eingeschränkte Steuerelemente und Bestätigungen für riskante Aktionen oder Befehle verwenden, die unbeabsichtigte Folgen haben.

-   **Geben Sie den Befehl Rückgängig an.** Es ist am besten, eine einfache Möglichkeit zum Rückgängig machen aller Befehle zu bieten, aber Ihre App kann über einige Befehle verfügen, deren Auswirkungen nicht rückgängig gemacht werden können.
-   **Geben Sie nach Möglichkeit ein gutes Feedback, aber ergreifen Sie keine Maßnahmen, bis Sie mit dem Finger nach oben sind.** Auf diese Weise können Benutzer Fehler korrigieren, bevor sie sie machen.
-   **Ermöglichen Sie es Benutzern nach Möglichkeit, Fehler einfach zu korrigieren.** Wenn eine Aktion auf dem Finger nach oben wirksam wird, können Benutzer Fehler beheben, indem sie gleiten, während der Finger noch unten ist.
-   **Geben Sie nach Möglichkeit an, dass eine direkte Manipulation nicht durch Widerstand gegen die Bewegung durchgeführt werden kann.** Lassen Sie die Bewegung zu, aber lassen Sie das Objekt wieder an Ort und Stelle zurücksetzen, wenn es freigegeben wird, um eindeutig anzugeben, dass die Aktion erkannt wurde, aber nicht durchgeführt werden kann.
-   **Eine klare physische Trennung zwischen häufig verwendeten Befehlen und destruktiven Befehlen.** Andernfalls können Benutzer versehentlich destruktive Befehle berühren. Ein Befehl wird als destruktiv betrachtet, wenn sein Effekt weit verbreitet ist und entweder nicht einfach rückgängig gemacht werden kann oder der Effekt nicht sofort erkennbar ist.
-   **Bestätigen Sie Befehle für riskante Aktionen oder Befehle, die unbeabsichtigte Folgen haben.** Verwenden Sie zu diesem Zweck ein Bestätigungsdialogfeld.
-   **Erwägen Sie, alle anderen Aktionen zu bestätigen, die Benutzer bei verwendung von Touch versehentlich ausführen und die entweder unbemerkt bleiben oder schwer rückgängig zu machen sind.** Normalerweise werden diese als routinemäßige Bestätigungen bezeichnet und werden davon abgeraten, da Benutzer solche Befehle nicht häufig per Maus oder Tastatur ausführen. Um unnötige Bestätigungen zu verhindern, stellen Sie diese Nur dann vor, wenn der Befehl per Touch initiiert wurde.

    Routinemäßige Bestätigungen sind für Interaktionen akzeptabel, die Benutzer häufig versehentlich mit touch verwenden.

    Entwickler: Sie können mithilfe der INPUT MESSAGE SOURCE-API zwischen Maus- und [**\_ \_ Touchereignissen**](/windows/win32/api/winuser/ns-winuser-input_message_source) unterscheiden.


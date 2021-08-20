---
title: Touch
description: Alle Microsoft Windows-Anwendungen sollten eine hervorragende Toucherfahrung haben. Und das Erstellen einer solchen Erfahrung ist einfacher, als Sie denken.
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
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Alle Microsoft Windows-Anwendungen sollten eine hervorragende Toucherfahrung haben. Und das Erstellen einer solchen Erfahrung ist einfacher, als Sie denken.

Toucheingabe bezieht sich auf die Verwendung eines oder mehrere Finger, um Eingaben über eine Geräteanzeige zu ermöglichen und mit Windows und Apps zu interagieren. Eine touchoptimierte App verfügt über ein Benutzeroberflächen- und Interaktionsmodell, das für die größeren, weniger präzisen Berührungsbereiche, die verschiedenen Formfaktoren von Touchgeräten und die vielen Positionen und Greifer ausgelegt ist, die Benutzer bei der Verwendung eines Touchgeräts übernehmen können.

![Benutzer interagiert mit Tablet mit touch](images/inter_touch_image1.jpeg)

Jedes Eingabegerät hat seine Stärken. Die Tastatur ist am besten für die Texteingabe und das Ausführen von Befehlen mit minimaler Handbewegung. Die Maus ist am besten für effizientes, präzises Zeigen. Touch ist am besten für die Objektbearbeitung und das Ausführen einfacher Befehle. Ein Stift ist am besten für Freiformausdruck, wie bei Handschrift und Zeichnung.

Windows 8.1 ist für Reaktionsfähigkeit, Genauigkeit und Benutzerfreundlichkeit mit Toucheingabe optimiert und unterstützt gleichzeitig vollständig herkömmliche Eingabemethoden (z. B. Maus, Stift und Tastatur). Die Geschwindigkeit, Genauigkeit und taktiles Feedback, die herkömmliche Eingabemodi bieten, sind für viele Benutzer vertraut und ansprechend und möglicherweise besser für bestimmte Interaktionsszenarien geeignet.

Richtlinien zu Maus, Stift und Barrierefreiheit finden Sie in separaten Themen.

Wenn Sie über die Interaktionserfahrung für Ihre App nachdenken:

Gehen Sie nicht davon aus, dass eine Benutzeroberfläche, die gut für eine Maus funktioniert, auch gut für touch funktioniert. Eine gute Mausunterstützung ist zwar ein Anfang, aber eine gute Toucherfahrung hat einige zusätzliche Anforderungen.

Gehen Sie davon aus, dass eine Benutzeroberfläche, die gut für einen Finger funktioniert, auch gut für einen Stift funktioniert. Ihre App berührbar zu machen, ist ein langer Weg, auch eine gute Stiftunterstützung zu bieten. Der Hauptunterschied ist, dass Finger eine bluntere Spitze haben, sodass sie größere Ziele benötigen.

Mit touch können Sie Objekte und die Benutzeroberfläche direkt bearbeiten, was eine schnellere, natürlichere und ansprechendere Erfahrung ermöglicht.

## <a name="provide-a-great-touch-experience"></a>Bereitstellen einer großartigen Toucherfahrung

Sie sollten sicherstellen, dass Benutzer wichtige und wichtige Aufgaben effizient mit touch-Eingaben ausführen können. Bestimmte App-Funktionen wie Text- oder Pixelbearbeitung eignen sich jedoch möglicherweise nicht für Toucheingaben und können für das am besten geeignete Eingabegerät reserviert werden.

Wenn Sie nicht viel Erfahrung mit der Entwicklung von Touch-Apps haben, ist es am besten, indem Sie lernen. Holen Sie sich einen Touch-fähigen Computer, legen Sie Maus und Tastatur beiseite, und verwenden Sie nur Ihre Finger, um mit Ihrer App zu interagieren. Wenn Sie über ein Tablet verfügen, experimentieren Sie damit, es an unterschiedlichen Positionen zu halten, z. B. auf Dem Runde, flach auf einem Tisch oder in den Arme, während Sie stehen. Versuchen Sie, es im Hochformat und im Querformat zu verwenden.

Touchoptimierte Apps, die am besten mit Touchinteraktion funktionieren, sind in der Regel:

-   **Natürlich und intuitiv.** Interaktionen sind so konzipiert, dass sie der Interaktion von Benutzern mit Objekten in der realen Welt entsprechen.
-   **Weniger intrusiv.** Die Verwendung von Touch ist im Hintergrund und daher viel weniger störend als das Eingeben oder Klicken.
-   **Tragbar.** Touchgeräte sind kompakter, da viele Aufgaben ohne Tastatur, Maus, Stift oder Touchpad durchgeführt werden können. Sie sind auch flexibler, da keine Arbeitsoberfläche erforderlich ist.
-   **Direkt und ansprechend.** Durch die Touch-Touch-Touch-Verbindung haben Sie das Gefühl, objekte direkt auf dem Bildschirm zu bearbeiten.
-   **Weniger genau.** Benutzer können Objekte im Vergleich zu einer Maus oder einem Stift nicht so genau als Ziel verwenden.

Touch bietet ein natürliches, reales Interaktions-Gefühl. Direkte Manipulation und Animation vervollständigen diesen Eindruck, indem Sie Objekten eine realistische, dynamische Bewegung und Feedback geben. Betrachten Sie beispielsweise ein Kartenspiel. Es ist nicht nur praktisch und einfach, Karten mit einem Finger zu ziehen, sondern auch ein ansprechendes reales Gefühl, wenn Sie die Karten genau wie bei einem physischen Kartenspiel drehen und drehen können. Und wenn Sie versuchen, eine Karte zu verschieben, die nicht verschoben werden kann, ist es eine bessere Erfahrung, die Karte zu unterstützen, aber nicht die Bewegung zu verhindern, und sich wieder an Ort und Stelle zu setzen, wenn sie freigegeben wird, um eindeutig anzugeben, dass die Aktion erkannt wurde, aber nicht durchgeführt werden kann.

Wenn Ihre App bereits gut entworfen wurde, ist es einfach, eine großartige Toucherfahrung zu bieten. Zu diesem Zweck ist ein gut entworfenes Programm:

-   **Stellt sicher, dass die** wichtigsten Aufgaben effizient mit einem Finger ausgeführt werden können (zumindest die Aufgaben, die keine große Menge an Eingaben oder ausführliche Pixelbearbeitungen umfassen).
-   **Verwendet große Steuerelemente für touch.** Allgemeine Steuerelemente haben eine Mindestgröße von 23 x 23 Pixel (13 x 13 DLUs), und die am häufigsten verwendeten Steuerelemente sind mindestens 40 x 40 Pixel (23 x 22 DLUs). Um nicht reagierende Verhalten zu vermeiden, sollten Benutzeroberflächenelemente mindestens 5 Pixel (3 DLUs) Platz zwischen ihnen haben. Stellen Sie bei anderen Steuerelementen sicher, dass sie ein Klickziel von mindestens 23 x 23 Pixel (13 x 13 DLU) haben, auch wenn ihre statische Darstellung viel kleiner ist. Weitere Informationen finden Sie unter Standard-Steuerelement-Größen.
-   **Unterstützt Mauseingaben.** Die interaktiven Steuerelemente verfügen über klare, sichtbare Bezahlbarkeiten. Objekte haben Standardverhalten für die standardmäßigen Mausinteraktionen (einzelner und doppelter Linkklick, Rechtsklick, Ziehen und Zeigen).
-   **Unterstützt Tastatureingaben.** Die App bietet Standardmäßige Tastenkombinationszuweisungen, insbesondere für Navigations- und Bearbeitungsbefehle, die auch über Touchgesten generiert werden können.
-   **Stellt die Barrierefreiheit sicher.** Verwendet Benutzeroberflächenautomatisierung oder Microsoft Active Accessibility (MSAA), um programmgesteuerten Zugriff auf die Benutzeroberfläche für Hilfstechnologien zu ermöglichen. Die App reagiert entsprechend auf Änderungen an Ausrichtung, Design, Locale und Systemmetrik.
-   **Beseitigt unnötige Interaktionen.** Verwenden Sie die sichersten und sichersten Standardwerte, um Datenverluste oder Systemzugriffe zu verhindern. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählt die App die wahrscheinlichste oder bequemste Option aus.
-   **Stellt eine Touch-Entsprechung für den Hover-Wert zur** Verlassen Sie sich nicht darauf, dass Sie mit dem Hover eine Aktion ausführen.
-   **Stellt sicher, dass Gesten sofort wirksam werden.** Halten Sie die Kontaktpunkte während der gestenweiten Geste reibungslos unter den Fingern des Benutzers, was die Auswirkung der Gestenzuordnung direkt auf die Bewegung des Benutzers ausdrungen kann.
-   **Verwendet nach Möglichkeit Standardgesten.** Benutzerdefinierte Gesten nur für Interaktionen, die für Ihre App eindeutig sind.
-   **Stellt sicher, dass unerwünschte oder destruktive Befehle umgekehrt oder korrigiert werden können.** Versehentliche Aktionen sind wahrscheinlicher, wenn Touch verwendet wird.

## <a name="guidelines-for-touch-input"></a>Richtlinien für Toucheingaben

Mit touch kann Ihre Windows-App physische Gesten verwenden, um die direkte Bearbeitung von Benutzeroberflächenelementen zu emulieren.

Berücksichtigen Sie beim Entwerfen Ihrer Touch-fähigen App die folgenden bewährten Methoden:

**Reaktionsfähigkeit ist wichtig, um Touch-Erfahrungen zu erstellen, die sich direkt und ansprechend anfühlen.** Um direkt zu sein, müssen Gesten sofort wirksam werden, und die Kontaktpunkte eines Objekts müssen während der gesamten Geste reibungslos unter den Fingern des Benutzers bleiben. Der Effekt der Toucheingabe sollte direkt der Bewegung des Benutzers folgen. Wenn der Benutzer z. B. die Finger um 90 Grad dreht, sollte sich das Objekt auch um 90 Grad drehen. Verzögerungen, abgesenkte Antworten, Kontaktverluste oder ungenaue Ergebnisse zerstören die Wahrnehmung der direkten Manipulation und der Qualität.

**Konsistenz ist wichtig, um Touch-Erfahrungen zu erstellen, die sich natürlich und intuitiv anfühlen.** Sobald Benutzer eine Standardgeste erlernen, erwarten sie, dass diese Geste in allen Apps die gleiche Wirkung hat. Weisen Sie Standardgesten niemals nicht standardmäßige Bedeutungen zu, um Verwirrung und Frust zu vermeiden. Verwenden Sie stattdessen benutzerdefinierte Gesten für Interaktionen, die für Ihr Programm eindeutig sind.

Als Nächstes beschreiben wir die Windows Touchsprache, aber bevor wir losgehen, finden Sie hier eine kurze Liste der grundlegenden Toucheingabebegriffe.

-   **Geste**

    Eine Geste ist die physische Aktivität oder Bewegung, die auf dem Eingabegerät (Finger, Finger, Stift/Stift, Maus und so weiter) ausgeführt wird. Wenn Sie beispielsweise einen Befehl starten, aktivieren oder aufrufen möchten, tippen Sie mit einem einzigen Finger auf ein Toucheingabe- oder Touchpadgerät (entspricht einem Linksklick mit einer Maus, einem Tippen mit einem Stift oder der EINGABETASTE auf einer Tastatur).

-   **Manipulation**

    Eine Manipulation ist die sofortige Echtzeitreaktion oder Reaktion eines Objekts oder einer Benutzeroberfläche auf eine Geste. Beispielsweise bewirken die Schiebe- und Wischgesten in der Regel, dass sich ein Element oder eine Benutzeroberfläche in irgendeiner Weise bewegt.

    Das Endergebnis einer Manipulation, wie sie durch das -Objekt auf dem Bildschirm und in der Benutzeroberfläche manifestiert wird, ist die Interaktion.

-   **Interaktion**

    Interaktionen hängen davon ab, wie eine Bearbeitung interpretiert wird und welchen Befehl oder welche Aktion sich aus der Bearbeitung ergibt. Objekte können z. B. mithilfe der Schiebe- und Wischgesten verschoben werden, aber die Ergebnisse unterscheiden sich je nachdem, ob ein Entfernungsschwellenwert überschritten wird. Eine Folie kann verwendet werden, um ein Objekt zu ziehen oder eine Ansicht zu schwenken, während sie zum Auswählen eines Elements oder Anzeigen einer App-Leiste verwendet werden kann.

### <a name="the-windows-touch-language"></a>Die Windows Touchsprache

Windows bietet einen präzisen Satz von Touchinteraktionen, die im gesamten System verwendet werden. Durch die durchgängige Anwendung dieser Touchsprache ist Ihre App mit dem vertraut, was Benutzer bereits wissen. Dies erhöht das Vertrauen der Benutzer, da Ihre App einfacher zu erlernen und zu verwenden ist. Weitere Informationen zur Implementierung der Touchsprache finden Sie unter Gesten, Manipulationen und Interaktionen.

**Halten Sie gedrückt, um zu lernen.**

Die Press and Hold-Geste zeigt detaillierte Informationen oder visuelle Elemente (z. B. eine QuickInfo oder ein Kontextmenü) an, ohne eine Aktion oder einen Befehl zu committen. Schwenken ist weiterhin möglich, wenn eine gleitende Geste gestartet wird, während das Visual angezeigt wird.

> [!IMPORTANT]
> In Fällen, in denen horizontales und vertikales Schwenken aktiviert ist, können Sie Drücken und Halten für die Auswahl verwenden.

 

Einstiegszustand: Ein oder zwei Finger, die mit dem Bildschirm in Kontakt sind.

Bewegung: Keine Bewegung.

Beendigungszustand: Der letzte Finger nach oben beendet die Geste.

Auswirkung: Zeigen Sie weitere Informationen an.

![Touch \- \- drücken, um \-learn.png](images/inter-touch-image2.png)

Die Press-and-Hold-Geste.

**Darauf zeigen (Hover)**

Das Hovern ist eine nützliche Interaktion, da es Benutzern ermöglicht, zusätzliche Informationen über Tipps zu erhalten, bevor eine Aktion initiiert wird. Wenn Sie diese Tipps sehen, können Benutzer sich sicherer fühlen und Fehler reduzieren.

Leider wird das Zeigen von Touchtechnologien nicht unterstützt, sodass Benutzer nicht mit dem Finger zeigen können. Die einfache Lösung für dieses Problem besteht in der vollständigen Nutzung des Hoverns, aber nur in einer Weise, die zum Ausführen einer Aktion nicht erforderlich ist. In der Praxis bedeutet dies in der Regel, dass die Aktion auch durch Klicken ausgeführt werden kann, aber nicht unbedingt auf die gleiche Weise.

![Screenshot, der ein Beispiel für die Hoverinteraktion neben einem Beispiel für die Klickaktion zeigt.](images/inter-touch-image13.png)

In diesem Beispiel können Benutzer das heutige Datum sehen, indem sie mit der Maustaste darauf klicken oder darauf klicken.

**Tippen Für primäre Aktion tippen**

Durch Tippen auf ein Element wird die primäre Aktion aufgerufen, z. B. das Starten einer App oder das Ausführen eines Befehls.

Einstiegszustand: Ein Finger, der mit dem Bildschirm oder Touchpad in Kontakt ist und vor dem Zeitschwellenwert für eine Press-and-Hold-Interaktion aufgehoben wird.

Bewegung: Keine Bewegung.

Beendigungszustand: Der Finger nach oben beendet die Geste.

Auswirkung: Starten Sie eine App, oder führen Sie einen Befehl aus.

![Tippen \- Sie auf \-primary.png](images/inter-touch-image3.png)

Die Tippbewegung.

**Schieben in Schwenken**

Folie wird hauptsächlich zum Schwenken von Interaktionen verwendet, kann aber auch zum Verschieben (wo schwenken auf eine Richtung beschränkt ist), zum Zeichnen oder zum Schreiben verwendet werden. Schieberegler können auch verwendet werden, um kleine, dichte gepackte Elemente durch Bereinigung (Gleiten des Fingers über verwandte Objekte wie Optionsfelder) als Ziel zu verwenden.

Einstiegszustand: Ein oder zwei Finger, die mit dem Bildschirm in Kontakt sind.

Bewegung: Ziehen Sie , während alle zusätzlichen Finger relativ zueinander an der gleichen Position bleiben.

Beendigungszustand: Der letzte Finger nach oben beendet die Geste.

Auswirkung: Verschieben Sie das zugrunde liegende Objekt direkt und sofort, wenn sich die Finger bewegen. Achten Sie darauf, den Kontaktpunkt während der gesamten Geste unter dem Finger zu halten.

![Touch \-slide.png](images/inter-touch-image4.png)

Die Schwenkgeste.

**Wischen zum Auswählen, Befehlen und Verschieben**

Verschiebt den Finger um einen kurzen Abstand zur Schwenkrichtung (wobei schwenken auf eine Richtung beschränkt ist), wählt Objekte in einer Liste oder einem Raster aus. Zeigen Sie die App-Leiste mit relevanten Befehlen an, wenn Objekte ausgewählt werden.

Einstiegszustand: Ein oder mehrere Finger berühren den Bildschirm.

Bewegung: Ziehen Sie eine kurze Entfernung, und heben Sie sie auf, bevor der Entfernungsschwellenwert für eine Bewegungsinteraktion auftritt.

Beendigungszustand: Der letzte Finger nach oben beendet die Geste.

Auswirkung: Das zugrunde liegende Objekt wird ausgewählt oder verschoben, oder die App-Leiste wird angezeigt. Achten Sie darauf, den Kontaktpunkt während der gesamten Geste unter dem Finger zu halten.

![d: \\ sdkenlistment \\ m \- ux design m \- \\ \- ux design images touch \- \\ \\ \-swipe.png](images/inter-touch-image5.png)

Die Wischgeste.

**Zusammendrücken/Aufziehen: Zoom**

Die Stift- und Streckgesten werden für drei Arten von Interaktionen verwendet: optischer Zoom, Größenvergrößerung und semantischer Zoom.

Der optische Zoom passt die Vergrößerungsstufe des gesamten Inhaltsbereichs an, um eine detailliertere Ansicht des Inhalts zu erhalten. Im Gegensatz dazu ist die Größenvergrößerung ein Verfahren zum Anpassen der relativen Größe eines oder mehrere Objekte innerhalb eines Inhaltsbereichs, ohne die Ansicht in den Inhaltsbereich zu ändern.

Semantischer Zoom ist ein touchoptimiertes Verfahren zum Präsentieren und Navigieren strukturierter Daten oder Inhalte innerhalb einer einzelnen Ansicht (z. B. die Ordnerstruktur eines Computers, eine Bibliothek von Dokumenten oder ein Fotoalb), ohne dass Steuerelemente für Schwenken, Scrollen oder Strukturansichten benötigt werden. Der semantische Zoom bietet zwei verschiedene Ansichten desselben Inhalts, da Sie beim Vergrößern mehr Details und beim Verkleinern weniger Details sehen können.

Einstiegszustand: Zwei Finger, die gleichzeitig mit dem Bildschirm in Kontakt sind.

Bewegung: Finger bewegen sich entlang einer Achse voneinander ab (strecken) oder zusammen (zusammendringen).

Beendigungszustand: Jeder Finger nach oben beendet die Geste.

Auswirkung: Zoomen Sie das zugrunde liegende Objekt direkt und direkt heraus, wenn sich die Finger trennen oder sich auf der Achse nähern. Achten Sie darauf, dass die Kontaktpunkte während der gesamten Geste unter dem Finger bleiben.

![Landing \-areazoom.png](images/inter-touch-image6.png)

Die Zoomgeste.

**Turn to rotate**

Wenn Sie mit zwei oder mehr Fingern drehen, wird ein Objekt gedreht. Drehen Sie das Gerät selbst, um den ganzen Bildschirm zu drehen.

Einstiegszustand: Zwei Finger, die gleichzeitig mit dem Bildschirm in Kontakt sind.

Bewegung: Ein oder beide Finger drehen sich um den anderen und bewegen sich senkrecht zur Linie zwischen ihnen.

Beendigungszustand: Jeder Finger nach oben beendet die Geste.

Auswirkung: Drehen Sie das zugrunde liegende Objekt auf die gleiche Menge, in der sich die Finger gedreht haben. Achten Sie darauf, dass die Kontaktpunkte während der gesamten Geste unter dem Finger bleiben.

![Touch \-turn.png](images/inter-touch-image7.png)

Die Drehbewegung.

Die Drehung ist nur für bestimmte Objekttypen sinnvoll, daher wird sie nicht einem System zugeordnet, Windows werden.

Die Rotation wird häufig von verschiedenen Personen unterschiedlich durchgeführt. Einige Personen ziehen es vor, einen Finger um einen Pivotfinger zu drehen, während andere es vorziehen, beide Finger in einer kreisförmigen Bewegung zu drehen. Die meisten Personen verwenden eine Kombination der beiden, bei der ein Finger mehr bewegt wird als der andere. Obwohl eine gleichmäßige Drehung zu einem beliebigen Winkel die beste Interaktion ist, ist es in vielen Kontexten, z. B. bei der Fotoanzeige, am besten, sich auf die nächste Drehung von 90 Grad zu setzen, sobald der Benutzer loslässt. Bei der Fotobearbeitung können Sie das Foto mit einer kleinen Drehung begradig machen.

**Wischen vom Edge für App-Befehle**

Wenn Sie den Finger aus kurzer Entfernung vom unteren oder oberen Rand des Bildschirms wischen, werden App-Befehle in einer App-Leiste angezeigt.

Einstiegszustand: Ein oder mehrere Finger berühren die Blende.

Bewegung: Ziehen Sie einen kurzen Abstand auf den Bildschirm, und heben Sie ihn an.

Beendigungszustand: Der letzte Finger nach oben beendet die Geste.

Auswirkung: Die App-Leiste wird angezeigt.

![touch \- swipe \- bottom \-edge.png](images/inter-touch-image8.png)

![Touch \- wischen \- \- seitlichedge.png](images/inter-touch-image9.png)

Die Wischbewegung von der Kante.

Entwickler: Weitere Informationen finden Sie unter [**DIRECTMANIPULATION \_ CONFIGURATION-Enumeration.**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration)

### <a name="control-usage"></a>Steuern der Nutzung

Hier stellen wir einige Richtlinien zum Optimieren von Steuerelementen für die Touchverwendung zur Verfügung.

-   **Verwenden Sie allgemeine Steuerelemente.** Die gängigsten Steuerelemente sind so konzipiert, dass sie eine gute Toucherfahrung unterstützen.
-   **Wählen Sie benutzerdefinierte Steuerelemente aus, die für touch-Unterstützung konzipiert sind.** Möglicherweise benötigen Sie benutzerdefinierte Steuerelemente, um die speziellen Erfahrungen Ihres Programms zu unterstützen. Wählen Sie benutzerdefinierte Steuerelemente aus, die:
    -   Kann groß genug dimensioniert werden, um eine einfache Ziel- und Bearbeitungsgröße zu haben.
    -   Wenn sie bearbeitet werden, bewegen und reagieren Sie auf die Art und Weise, wie reale Objekte bewegt und reagieren, z. B. durch Bewegung und Spannungen.
    -   Sie sind verzeihend, indem Sie es Benutzern ermöglichen, Fehler einfach zu korrigieren.
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

In diesem Beispiel sind Windows 7 Taskleisten-Sprunglisten bei der Anzeige per Touch-Touch-Vorgang schwieriger.

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


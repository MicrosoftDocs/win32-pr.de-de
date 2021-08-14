---
title: Stift
description: Alle Microsoft Windows-Anwendungen sollten stiftfähig sein. Dies ist einfacher, als Sie denken.
ms.assetid: 45635d5a-c9ff-47d0-89ef-a9c48ac67594
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 90c953fe1c287741bec266bfe6516a6a8922692b213292d2f17cccebf561cb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853375"
---
# <a name="pen"></a>Stift

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Alle Microsoft Windows-Anwendungen sollten stiftfähig sein. Dies ist einfacher, als Sie denken.

Stifteingabe bezieht sich auf die Art und Weise Windows Sie mithilfe eines Stifts direkt mit einem Computer interagieren können. Ein Stift kann zum Zeigen und auch für Gesten, einfache Texteingaben und das Erfassen freiformfreier Gedanken in Freihandeingaben verwendet werden.

Der für die Eingabe verwendete Stift verfügt über einen feinen, reibungslosen Tipp, der präzises Zeigen, Schreiben oder Zeichnen von Ink unterstützt. Der Stift kann auch über eine optionale Stiftschaltfläche (zum Ausführen von Rechtsklicks) und einen Radierer (zum Löschen von Freihandhand) verfügen. Die meisten Stifte unterstützen den Mauszeiger.

![Abbildung eines typischen Stifts ](images/inter-pen-image1.png)

Ein typischer Stift.

Wenn der Stift für die Handschrift verwendet wird, können die Striche des Benutzers mithilfe der Handschrifterkennung in Text konvertiert werden. Die Striche können genauso beibehalten werden, wie sie geschrieben wurden, wobei die Erkennung im Hintergrund durchgeführt wird, um das Suchen und Kopieren als Text zu unterstützen. Solche nicht konvertierten Striche werden als "Digital Ink" bezeichnet.

![Screenshot der Handschrift auf einer Seite ](images/inter-pen-image2.png)

Ein Beispiel für eine Ink-Eingabe.

Die meisten Windows Programme sind bereits stiftfreundlicher, da ein Stift anstelle einer Maus verwendet werden kann, der Stift für die wichtigsten Aufgaben und Interaktionen reibungslos funktioniert und das Programm auf Gesten reagiert. Ein Programm wird handschriftlich, wenn es bei der handschriftlichen Texteingabe hilft. Ein Programm wird ink-fähig, wenn es Ink direkt verarbeiten kann, anstatt zu verlangen, dass Stiftstriche in Text oder entsprechende Mausbewegungen übersetzt werden müssen. Dies ermöglicht Benutzern das Schreiben, Zeichnen und Hinzufügen von Kommentaren in frei fließenden, qualitativ hochwertigen digitalen Freihandfarben. Das Erfassen von Ink unterscheidet sich vom Sammeln von Mausereignissen, da Ink eine höhere Auflösung und eine höhere Abtastrate erfordert und auch mit druck- und neigungsartigem Druck differenziert werden kann. Informationen zum Erstellen handschriftlicher und freihandfähiger Programme finden Sie unter [Integrieren von Freihand-](/previous-versions/windows/desktop/ms700674(v=vs.85)) und [Texteingaben mit dem Stift](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Beim Positionieren eines Stifts ist ein Cursor weniger erforderlich, da sich die Spitze selbst darstellt. Für die Zielunterstützung stellt Windows jedoch einen kleinen Stiftcursor bereit, der die aktuelle Stiftposition angibt. Im Gegensatz zum Mauszeiger, den er ersetzt, wird der Stiftcursor nicht benötigt, es sei denn, der Stift befindet sich in der Nähe der Anzeige, sodass er nach einigen Sekunden Inaktivität verschwindet, um eine nicht kontrollierte Ansicht der Informationen zu ermöglichen.

Die meisten stiftfreundlichen Programme unterstützen Gesten. Eine Geste ist eine schnelle Bewegung des Stifts auf einem Bildschirm, den der Computer als Befehl interpretiert, anstatt als Mausbewegung, Schreib- oder Zeichnungsbewegung. Eine der schnellsten und einfachsten Gesten, die sie ausführen können, ist ein Flimmer. Ein Flimmer ist eine einfache Geste, die zur Navigation oder einem Bearbeitungsbefehl führt. Navigationsflimmer umfassen Ziehen nach oben, Ziehen nach unten, Zurück- und Vorwärtsbewegung, während Bearbeitungsflimmer das Kopieren, Einfügen, Rückgängigmachen und Löschen umfassen.

Alle Zeiger mit Ausnahme des ausgelasteten Zeigers verfügen über einen Single-Pixel-Hot Spot, der die genaue Bildschirmposition des Zeigers definiert. Der Hot Spot bestimmt, welches Objekt von der Interaktion betroffen ist. Objekte definieren eine heiße Zone, bei der es sich um den Bereich handelt, in dem der Hotspots als über dem Objekt betrachtet wird. In der Regel stimmt die heiße Zone mit den Rahmen eines Objekts überein, kann jedoch größer sein, um die Interaktion zu vereinfachen.

**Da ein Stift präziser als ein Finger zeigen kann, funktioniert die Benutzeroberfläche auch gut für einen Stift, wenn sie gut für die Fingereingabe funktioniert.** Daher konzentriert sich dieser Artikel hauptsächlich auf das Hinzufügen von Stiftunterstützung zu Programmen, die bereits für die Toucheingabe entwickelt wurden.

**Hinweis:** Richtlinien in Bezug auf [Maus,](inter-mouse.md) [Barrierefreiheit](inter-accessibility.md)und [Touch](inter-touch.md) werden in separaten Artikeln vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Die Verwendung eines Stifts für die Eingabe weist die folgenden Merkmale auf:

-   **Natürlich und intuitiv.** Jeder weiß, wie er mit einem Stift zeigen und tippen kann. Objektinteraktionen sind so konzipiert, dass sie der konsistenten Interaktion von Benutzern mit Objekten in der realen Welt entsprechen.
-   **Ausdrucksstark.** Striche eines Stifts sind einfach zu steuern, sodass das Schreiben, Zeichnen, Skizzieren, Zeichnen und Kommentieren einfacher ist als mit einer Maus.
-   **Persönlicher.** Ebenso wie eine handschriftliche Notiz oder Signatur persönlicher als eine typisierte Ist, ist die Verwendung einer digital handschriftlichen Notiz oder Signatur auch persönlicher.
-   **Weniger intrusiv.** Die Verwendung eines Stifts ist unbeaufsichtigt und daher viel weniger ablenkend als das Eingeben oder Klicken, insbesondere in sozialen Situationen wie Besprechungen.
-   **Tragbar.** Ein Computer mit Stiftfunktion kann kompakter sein, da die meisten Aufgaben ohne Tastatur, Maus oder Touchpad ausgeführt werden können. Sie kann flexibler sein, da sie keine Arbeitsoberfläche erfordert. Sie ermöglicht neue Orte und Szenarien für die Verwendung eines Computers.
-   **Direkt und ansprechend.** Wenn Sie einen Stift verwenden, haben Sie das Gefühl, dass Sie direkt mit den Objekten auf dem Bildschirm interagieren, während Sie bei Verwendung eines Maus- oder Touchpads immer Handbewegungen mit separaten Zeigerbewegungen auf dem Bildschirm koordinieren müssen, die sich im Vergleich indirekt anfühlen.

**Alle Windows Programme sollten über eine gute Stifterfahrung verfügen.** Benutzer sollten in der Lage sein, die wichtigsten Aufgaben Ihres Programms effizient mithilfe eines Stifts auszuführen. Einige Aufgaben, z. B. Eingabe oder detaillierte Pixelbearbeitung, sind für einen Stift nicht geeignet, sollten aber zumindest möglich sein.

Glücklicherweise ist es einfach, eine gute Stiftunterstützung bereitzustellen, wenn Ihr Programm bereits gut entworfen und touchfreundlicher ist. Zu diesem Zweck ein gut entworfenes Programm:

-   **Verfügt über eine gute Mausunterstützung.** Die interaktiven Steuerelemente verfügen über klare, sichtbare Erschwinglichkeitszustände und zeigen Aufzeigerzustände für Zeigerfeedback. Objekte weisen Standardverhalten für die standardmäßigen Mausinteraktionen auf (einfaches und doppeltes Klicken mit der linken Maustaste, Rechtsklick, Ziehen und Bewegen des Mauszeigers). Die [Zeigerform](inter-mouse.md) ändert sich entsprechend, um den Typ der direkten Bearbeitung anzugeben.
-   **Verfügt über eine gute Tastaturunterstützung.** Das Programm macht Benutzer effizient, indem standardmäßig Tastenzuweisungen zur Verfügung gestellt werden, insbesondere für Navigations- und Bearbeitungsbefehle, die auch über Gesten generiert werden können.
-   **Verfügt über Steuerelemente, die groß genug für die Toucheingabe sind.** Die Steuerelemente haben eine Mindestgröße von 23 x 23 Pixeln (13 x 13 Dialogeinheiten \[ \] DLUs), und die am häufigsten verwendeten Steuerelemente sind mindestens 40 x 40 Pixel (23 x 22 DLUs). Um ein nicht reagierendes Verhalten zu vermeiden, sollten keine kleinen Lücken zwischen den Zielen vorhanden sein, auf die die Benutzeroberflächenelemente gesetzt werden sollten, sodass benachbarte Ziele entweder berühren oder mindestens 5 Pixel (3 DLUs) abstanden.
-   **Der Zugriff ist möglich.** Verwendet Microsoft Active Accessibility (MSAA), um programmgesteuerten Zugriff auf die Benutzeroberfläche für Hilfstechnologien bereitzustellen. Das Programm reagiert entsprechend auf Änderungen an Design- und Systemmetriken.
-   **Funktioniert gut und sieht in 120 dpi (Punkte pro Zoll) gut aus. Dies** ist die empfohlene Standardanzeigeauflösung für Stiftcomputer.
-   **Verwendet allgemeine Steuerelemente.** Die gängigsten Steuerelemente sind so konzipiert, dass sie eine gute Stifterfahrung unterstützen. Bei Bedarf verwendet das Programm gut implementierte benutzerdefinierte Steuerelemente, die zur Unterstützung einfacher Zielgruppenadressierung und interaktiver Bearbeitung konzipiert sind.
-   **Verwendet eingeschränkte Steuerelemente.** Wenn eingeschränkte Steuerelemente wie Listen und Schieberegler für die einfache Zielgruppenadressierung konzipiert sind, können sie besser als uneingeschränkte Steuerelemente wie Textfelder sein, da sie die Notwendigkeit von Texteingaben reduzieren.
-   **Stellt geeignete Standardwerte bereit.** Das Programm wählt standardmäßig die sicherste Option (um Daten- oder Systemzugriffsverluste zu verhindern) und die sicherste Option aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählt das Programm die wahrscheinlichste oder bequemste Option aus, sodass unnötige Interaktionen vermieden werden.
-   **Stellt die automatische Vervollständigung von Text bereit.** Stellt eine Liste der wahrscheinlichsten oder letzten Eingabewerte bereit, um die Texteingabe wesentlich zu vereinfachen.

Leider ist das Gegenteil auch der Fall, wenn Ihr Programm nicht gut entworfen ist. Dessen Nachteile werden besonders für Benutzer offensichtlich sein, die einen Stift verwenden.

### <a name="model-for-pen-interaction"></a>Modell für Stiftinteraktion

Wenn Sie keine Erfahrung mit der Verwendung eines Stifts haben, ist die beste Einführung, indem Sie lernen. Rufen Sie einen Stiftcomputer ab, legen Sie die Maus und die Tastatur beiseite, und erledigen Sie die Aufgaben, die Sie normalerweise nur mit einem Stift ausführen. Stellen Sie sicher, dass Sie sowohl Ink-fähige Programme wie Windows Journal als auch Programme ausprobieren, die nicht für Ink aktiviert sind. Wenn Sie über einen Tablet-PC verfügen, experimentieren Sie damit, ihn an verschiedenen Positionen zu halten, z. B. auf dem Runde, flach auf einem Tisch oder in den Händen, während Sie stehen. Versuchen Sie, ihn im Hochformat und im Querformat zu verwenden und den Stift zum Schreiben und nur zum Zeigen in der linken und rechten Hand zu halten.

Wenn Sie mit einem Stift experimentieren, werden Sie Dies feststellen:

-   **Kleine Steuerelemente sind schwierig zu verwenden.** Die Größe der Steuerelemente wirkt sich stark auf Ihre Fähigkeit aus, effektiv zu interagieren. Steuerelemente mit einer Größe von 10 x 10 Pixeln funktionieren für einen Stift sinnvoll, größere Steuerelemente sind jedoch noch komfortabler zu verwenden. Beispielsweise sind [Drehsteuerelemente](ctrl-spin-controls.md) (15 x 11 Pixel) zu klein für die einfache Verwendung mit einem Stift.
-   **Händigkeit ist ein Faktor.** Ihre Hand deckt manchmal Dinge ab, mit denen Sie möglicherweise interagieren möchten. Beispielsweise sind Kontextmenüs für rechtshändige Benutzer schwer zu verwenden, wenn sie rechts neben dem Klickpunkt angezeigt werden. Daher ist es besser, wenn sie auf der linken Seite angezeigt werden. Windows können Benutzer ihre Hand im Tablet PC Einstellungen Systemsteuerungselement angeben.
-   **Aufgabenlokalität ist hilfreich.** Sie können den Mauszeiger zwar mit einer 3-Zoll-Mausbewegung über einen 14-Zoll-Bildschirm bewegen, aber bei Verwendung eines Stifts müssen Sie ihre Hand auf die volle 14 Zoll bewegen. Das wiederholte Verschieben zwischen Zielen, die weit voneinander entfernt sind, kann mühsam sein. Daher ist es viel besser, Aufgabeninteraktionen nach Möglichkeit innerhalb des Bereichs einer ruhenden Hand zu halten. Kontextmenüs sind praktisch, da sie keine Handbewegung erfordern.
-   **Texteingabe und -auswahl sind schwierig.** Lange Texteingaben sind bei der Verwendung eines Stifts besonders schwierig, sodass die automatische Vervollständigung und akzeptable Standardtextwerte Aufgaben wirklich vereinfachen können. Die Textauswahl kann auch recht schwierig sein, sodass Aufgaben einfacher sind, wenn sie keine präzise Cursorplatzierung erfordern.
-   **Kleine Ziele in der Nähe des Rands der Anzeige können sehr schwierig zu tippen sein.** Einige Displayblenden werden hervorstechen, und einige Touchscreentechnologien sind an den Rändern weniger empfindlich, sodass Steuerelemente in der Nähe des Edges schwieriger zu verwenden sind. Beispielsweise können die Schaltflächen Minimieren, Maximieren/Wiederherstellen und Schließen auf der Titelleiste schwieriger zu verwenden sein, wenn ein Fenster maximiert wird.

### <a name="control-location"></a>Steuerungsspeicherort

Die Aufgabenlokalität reduziert mühsame, sich wiederholende Bildschirmübergreifende Bewegungen. Um Handbewegungen zu minimieren, suchen Sie Steuerelemente in der Nähe der Stelle, an der sie am wahrscheinlichsten verwendet werden.

**Falsch:**

![Screenshot der von Tools getrennten Farbpalette ](images/inter-pen-image3.png)

In diesem Beispiel von Windows XP ist die Farbpalette zu weit von der Stelle entfernt, an der sie wahrscheinlich verwendet wird.

Beachten Sie, dass der aktuelle Standort des Benutzers am nächsten liegt, der einem Ziel am nächsten liegt, sodass es trivial ist, es zu erhalten. Daher nutzen Kontextmenüs das [Fitts-Gesetz](inter-mouse.md)in vollem Umfang, ebenso wie die Minisymbolleisten, die von Microsoft Office verwendet werden.

![Screenshot von Zeigern in der Nähe von Menüs ](images/inter-pen-image4.png)

Die position des aktuellen Zeigers ist immer am einfachsten zu erhalten.

Kleine Ziele in der Nähe des Anzeigerands können schwierig zu erreichen sein, daher vermeiden Sie das Platzieren kleiner Steuerelemente in der Nähe von Fensterrändern. Um sicherzustellen, dass Steuerelemente beim Maximieren eines Fensters einfach als Ziel verwendet werden können, legen Sie sie entweder auf mindestens 23 x 23 Pixel (13 x 13 DLUs) fest, oder platzieren Sie sie vom Fensterrand weg.

### <a name="pen-interactions"></a>Stiftinteraktionen

**Systemgesten**

Systemgesten werden von Windows definiert und verarbeitet. Daher haben alle Windows Programme Zugriff darauf. Diese Gesten weisen entsprechende Maus-, Tastatur- und Anwendungsbefehlsmeldungen auf:



| System-Geste                                                           | Synthetisierte äquivalente Meldung                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Zeigen mit dem Mauszeiger (sofern unterstützt)<br/>                          | Mauszeigerzeiger<br/>                        |
| Tippen Sie auf (nach unten und oben).<br/>                               | Mausklick mit der linken Maustaste<br/>                   |
| Doppelt tippen (zweimal nach unten und nach oben)<br/>                  | Doppelklicken mit der Maus mit der linken Maustaste<br/>            |
| Halten Sie gedrückt (nach unten, anhalten, nach oben).<br/>                | Rechtsklick mit der Maus<br/>                  |
| Ziehen (nach unten, verschieben, nach oben)<br/>                           | Maus nach links ziehen<br/>                    |
| Drücken, Halten und Ziehen (nach unten, Anhalten, Verschieben, Nach oben)<br/>   | Maus mit der rechten Maustaste ziehen<br/>                   |
| Auswählen (nach unten, Verschieben über auswählbare Objekte, nach oben)<br/> | Mausauswahl<br/>                       |



 

**Entwickler:** Weitere Informationen finden Sie unter [SystemGesture-Enumeration.](/previous-versions/ms552724(v=vs.100))

**Flicks**

Bei Flimmern handelt es sich um einfache Gesten, die in etwa der Entsprechung von Tastenkombinationen entsprechen. Navigationsflimmer umfassen Ziehen nach oben, Ziehen nach unten, Zurück- und Vorwärtsbewegung. Bearbeitungsflimmer umfassen Kopieren, Einfügen, Rückgängigmachen und Löschen. Um Flimmer zu verwenden, muss Ihr Programm nur auf die zugehörigen Tastatureingabebefehle reagieren.

![Diagramm, das Flattgesten und deren Standardzuweisungen in Windows 7 zeigt.](images/inter-pen-image5.png)

Die acht Fingerbewegungen und ihre Standardzuweisungen in Windows 7. Die Navigationsflimmer wurden so geändert, dass sie dem Schwenken (wo sich das Objekt mit der Geste bewegt) anstelle eines Bildlaufs (wobei sich das Objekt in der entgegengesetzten Richtung der Geste bewegt) entspricht.

![Abbildung von Gesten für Die Bewegung, z. B. die Bewegungsbewegung ](images/inter-pen-image6.png)

Die acht Fingerbewegungen und ihre Standardzuweisungen in Windows Vista.

Die Navigationsflimmer weisen eine natürliche Zuordnung auf, sodass sie leicht zu erlernen und zu merken sind. Bei den Bearbeitungsflimmern handelt es sich um Diagonalen, die eine größere Genauigkeit erfordern, und ihre Zuordnungen sind nicht so natürlich (Blättern in Richtung der zu löschenden Papierkorb, Gleiten in richtung Zurückpfeil zum Rückgängig machen), sodass diese standardmäßig nicht aktiviert sind. Alle Flimmeraktionen können mithilfe des Steuerelements Stift und Eingabegeräte angepasst werden.



| Flick                                     | Synthetisierte äquivalente Meldung                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Linke Flacker-Seite<br/>                | Befehl "Weiterleiten" (Befehl "Zurück" für Windows Vista)<br/> |
| Rechtes Flimmern<br/>               | Befehl "Zurück" (Befehl "Weiterleiten" für Windows Vista)<br/> |
| Flimmern nach oben<br/>                  | Tastatur scrollen nach unten<br/>                             |
| Flackern nach unten<br/>                | Tastaturbildlauf nach oben<br/>                               |
| Bildlauf nach links diagonal<br/>    | Tastaturlöschung<br/>                                  |
| Nach unten nach links flattern, diagonal<br/>  | Tastatur rückgängig<br/>                                    |
| Nach rechts nach oben flattern diagonal<br/>   | Tastaturkopie<br/>                                    |
| Nach unten nach rechts flattern<br/> | Einfügen per Tastatur<br/>                                   |



 

**Anwendungsgesten**

Anwendungen können auch andere Gesten definieren und verarbeiten. Die Microsoft-Gestenerkennung kann mehr als [40 Gesten](../tablet/application-gestures-and-semantic-behavior.md)erkennen. Um Anwendungsgesten zu verwenden, muss Ihr Programm die erkannten Gesten definieren und dann die resultierenden Ereignisse behandeln.

**Reaktionsfähigkeit und Konsistenz**

**Reaktionsfähigkeit ist entscheidend für die Erstellung von Stifterfahrungen, die sich direkt und ansprechend anfühlen.** Um direkt zu sein, müssen Gesten sofort wirksam werden, und die Kontaktpunkte eines Objekts müssen während der gesamten Geste reibungslos unter dem Stift bleiben. Jede Verzögerung, ungenaue Reaktion, Kontaktverlust oder ungenaue Ergebnisse zerstören die Wahrnehmung der direkten Manipulation und der Qualität.

**Konsistenz ist entscheidend für die Erstellung von Stifterfahrungen, die sich natürlich und intuitiv anfühlen.** Sobald Benutzer eine Standardgeste erlernen, erwarten sie, dass diese Geste für alle anwendbaren Programme die gleiche Wirkung hat. Um Verwirrung und Frust zu vermeiden, weisen Sie Standardgesten niemals nicht standardmäßige Bedeutungen zu. Verwenden Sie stattdessen benutzerdefinierte Gesten für Interaktionen, die für Ihr Programm eindeutig sind.

**Bearbeiten von Ink und Text**

Das Bearbeiten von Ink und Text gehört zu den schwierigsten Interaktionen bei der Verwendung eines Stifts. Durch die Verwendung von eingeschränkten Steuerelementen, geeigneten Standardwerten und automatischer Vervollständigung entfällt oder reduziert sich die Notwendigkeit der Eingabe von Text. Wenn Ihr Programm jedoch text- oder ink-Bearbeitung umfasst, können Sie die Produktivität der Benutzer steigern, indem Sie **die Eingabebenutzeroberfläche automatisch auf bis zu 150 Prozent vergrößern, wenn ein Stift verwendet wird.**

Beispielsweise könnte ein E-Mail-Programm die Benutzeroberfläche in normaler Größe anzeigen, aber die Eingabebenutzeroberfläche auf 150 Prozent vergrößern, um Nachrichten zu verfassen.

![Screenshot der Outlook-Nachricht in großer Schrift ](images/inter-pen-image7.png)

In diesem Beispiel wird die Eingabeoberfläche auf 150 Prozent vergrößert.

**Wenn Sie nur vier Dinge tun...**

1.  1. Sorgen Sie dafür, dass Ihre Windows Programme eine gute Stifterfahrung haben! Benutzer sollten in der Lage sein, die wichtigsten Aufgaben Ihres Programms effizient mithilfe eines Stifts auszuführen (zumindest die Aufgaben, die nicht viel Eingabe oder detaillierte Pixelbearbeitung erfordern).
2.  2. Erwägen Sie, unterstützung für das Schreiben, Zeichnen und Hinzufügen von Kommentaren direkt mithilfe von Ink in den relevantesten Szenarien hinzuzufügen.
3.  3. Um eine direkte und ansprechende Benutzeroberfläche zu erstellen, werden Gesten sofort wirksam, Kontaktpunkte bleiben während der gesamten Geste reibungslos unter dem Stift des Benutzers, und die Gestenzuordnung wird direkt der Bewegung des Benutzers angezeigt.
4.  4. Um ein natürliches und intuitives Erlebnis zu schaffen, unterstützen Sie entsprechende Standardgesten und weisen ihnen ihre Standardbe bedeutung zu. Verwenden Sie benutzerdefinierte Gesten für Interaktionen, die für Ihr Programm eindeutig sind.

## <a name="guidelines"></a>Richtlinien

### <a name="control-usage"></a>Steuern der Nutzung

-   **Verwenden Sie lieber allgemeine Steuerelemente.** Die gängigsten Steuerelemente sind so konzipiert, dass sie eine gute Stifterfahrung unterstützen.
-   **Eingeschränkte Steuerelemente bevorzugen.** Verwenden Sie nach Möglichkeit eingeschränkte Steuerelemente wie Listen und Schieberegler anstelle von nicht eingeschränkten Steuerelementen wie Textfeldern, um die Notwendigkeit von Texteingaben zu reduzieren.
-   **Geben Sie die entsprechenden Standardwerte an.** Wählen Sie standardmäßig die sicherste Option (um Datenverlust oder Systemzugriff zu verhindern) und die sicherste Option aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Option aus, um unnötige Interaktionen zu vermeiden.
-   **Geben Sie die automatische Vervollständigung von Text an.** Geben Sie eine Liste der wahrscheinlichsten oder kürzlich eingegebenen Werte an, um die Texteingabe wesentlich zu vereinfachen.
-   **Wenn für wichtige Aufgaben, die mehrfache Auswahl verwenden, normalerweise eine Standardliste mit Mehrfachauswahl verwendet wird, stellen Sie stattdessen eine Option zur Verwendung einer Kontrollkästchenliste zur Verfügung.**
-   **Systemmetriken werden beachtet.** Verwenden Sie Systemmetriken für alle Größen, die keine Hardwiregrößen haben. Bei Bedarf können Benutzer die Systemmetriken oder dpi ändern, um ihre Anforderungen zu erfüllen. Behandeln Sie dies jedoch als letzten Ausweg, da Benutzer die Systemeinstellungen normalerweise nicht anpassen müssen, um die Benutzeroberfläche nutzbar zu machen.

![Screenshot von Menüs mit normaler und großer Größengröße ](images/inter-pen-image8.png)

In diesem Beispiel wurde die Systemmetrik für die Menühöhe geändert.

### <a name="control-sizing-layout-and-spacing"></a>Steuern von Größe, Layout und Abstand

-   **Verwenden Sie für allgemeine Steuerelemente die empfohlenen Steuerelementgrößen.** Diese sind groß genug für eine gute Stifterfahrung, mit Ausnahme von Drehungssteuerelementen (die nicht mit einem Stift, aber redundant sind) nutzbar sind.
-   **Wählen Sie ein Layout aus, das Steuerelemente in der Nähe des Orts platziert, an dem sie am wahrscheinlichsten verwendet werden.** Halten Sie Aufgabeninteraktionen nach Möglichkeit in einem kleinen Bereich ab. Vermeiden Sie Handbewegungen mit langer Entfernung, insbesondere bei häufigen Aufgaben und bei Ziehbewegungen.
-   **Verwenden Sie den empfohlenen Abstand.** Der empfohlene Abstand ist stiftnutzerfreundlich.
-   **Interaktive Steuerelemente sollten entweder berührend sein oder vorzugsweise mindestens 5 Pixel (3 DLUs) Abstand zwischen ihnen haben.** Dies verhindert Verwirrung, wenn Benutzer außerhalb des vorgesehenen Ziels tippen.
-   **Fügen Sie in Gruppen** von Steuerelementen, z. B. Befehlslinks, Kontrollkästchen und Optionsfeldern, sowie zwischen den Gruppen mehr als den empfohlenen vertikalen Abstand hinzu. Dies erleichtert die Unterscheidung.

### <a name="interaction"></a>Interaktion

-   **Aktivieren Sie für Programme, die zum Akzeptieren von Handschrift entwickelt wurden, die Standard-Inking-Funktion.** Mit der Standardeingabe können Benutzer Ink eingeben, indem sie einfach mit dem Schreiben beginnen, ohne tippen, einen Befehl ausführen oder etwas Besonderes tun zu müssen. Dies ermöglicht die natürlichste Erfahrung mit einem Stift. Bei Programmen, die nicht zum Akzeptieren von Handschrift entwickelt wurden, behandeln Sie Stifteingaben in Textfeldern als Auswahl.
-   **Benutzern das Zoomen der Inhaltsbenutzeroberfläche** ermöglichen, wenn Ihr Programm Über aufgaben hat, die die Bearbeitung von Text erfordern. Erwägen Sie, automatisch auf 150 Prozent zu zoomen, wenn ein Stift verwendet wird.
-   **Da Gesten auswendig sind, weisen Sie ihnen Bedeutungen zu, die programmübergreifend konsistent sind.** Geben Sie Gesten mit fester Semantik keine unterschiedlichen Bedeutungen. Verwenden Sie stattdessen eine entsprechende programmspezifische Geste.

### <a name="handedness"></a>Händigkeit

-   **Wenn ein Fenster kontextbezogen ist, wird es immer in der Nähe des Objekts angezeigt, aus dem es gestartet wurde.** Platzieren Sie sie im Weg, damit das Quellobjekt nicht durch das Fenster abgedeckt wird.
    -   Wenn sie mit der Maus angezeigt wird, platzieren Sie nach Möglichkeit den Kontextfensteroffset nach unten und rechts.

        ![Abbildung des kontextbezogenen Fensters, das rechts vom Objekt platziert wurde ](images/inter-pen-image9.png)

        Kontextfenster in der Nähe des Objekts anzeigen, aus dem es gestartet wurde.

    -   Wenn es mithilfe eines Stifts angezeigt wird, platzieren Sie nach Möglichkeit das Kontextfenster, damit es nicht von der Hand des Benutzers abgedeckt wird. Für rechtshändige Benutzer wird auf der linken Seite angezeigt. andernfalls rechts angezeigt.

        ![Abbildung des kontextbezogenen Fensters links vom Objekt ](images/inter-pen-image10.png)

        Wenn Sie einen Stift verwenden, zeigen Sie auch kontextbezogene Fenster an, damit sie nicht von der Hand des Benutzers abgedeckt werden.

-   **Entwickler:** Sie können mithilfe der [GetMessageExtraInfo-API](../tablet/system-events-and-mouse-messages.md) zwischen Mausereignissen und Stiftereignissen unterscheiden. Sie können die Übergabe des Benutzers [mithilfe](/previous-versions/ms819495(v=msdn.10)) der [SystemParametersInfo-API](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) mit SPI \_ GETMENUDROPALIGNMENT bestimmen.

### <a name="forgiveness"></a>Vergebung

-   **Geben Sie einen Befehl zum Rückgängig machen an.** Im Idealfall sollten Sie rückgängig machen für alle Befehle bereitstellen, aber Ihr Programm verfügt möglicherweise über einige Befehle, deren Auswirkungen nicht rückgängig gemacht werden können.
-   **Stellen Sie ein gutes Hoverfeedback zur Verfügung.** Geben Sie eindeutig an, wann sich der Stift über einem klickbaren Ziel befindet. Ein solches Feedback ist eine hervorragende Möglichkeit, um versehentliche Manipulationen zu verhindern.
-   **Wenn dies praktisch ist, geben Sie ein gutes Feedback, aber ergreifen Sie erst dann Maßnahmen, wenn Sie sich bewegen oder nach oben bewegen.** Auf diese Weise können Benutzer Fehler korrigieren, bevor sie sie machen.
-   **Ermöglichen Sie es Benutzern nach Möglichkeit, Fehler einfach zu korrigieren.** Wenn eine Aktion beim Auffüllen wirksam wird, können Benutzer Fehler beheben, indem sie gleiten, während der Stift noch unten ist.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Stifteingabe:

-   Verweisen Sie auf ein stiftförmiges Stifteingabegerät als Stift. Verwenden Sie bei der ersten Erwähnung den Tablettstift.
-   Verweisen Sie auf die Schaltfläche auf der Seite eines Stifts als Stiftschaltfläche, nicht auf die Schaltfläche mit dem Knopf.
-   Verweisen Sie generisch auf Tastatur, Maus, Trackball, Stift oder Finger als Eingabegerät.
-   Verwenden Sie tippen (und doppelt tippen), anstatt zu klicken, wenn Sie prozedurspezifische Prozeduren für die Verwendung eines Stifts dokumentieren. Tippen bedeutet, dass der Bildschirm gedrückt wird und dann vor einer Haltezeit gezippt wird. Sie kann verwendet werden, um einen Mausklick zu generieren. Verwenden Sie für Interaktionen, bei denen der Stift nicht verwendet wird, weiterhin Klick.


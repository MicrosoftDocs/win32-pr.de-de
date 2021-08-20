---
title: Stift
description: Für alle Microsoft Windows-Anwendungen sollte der Stift aktiviert sein. Dies ist einfacher, als Sie denken.
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
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Für alle Microsoft Windows-Anwendungen sollte der Stift aktiviert sein. Dies ist einfacher, als Sie denken.

Stifteingabe bezieht sich auf die Windows, mit der Sie mithilfe eines Stifts direkt mit einem Computer interagieren können. Ein Stift kann zum Zeigen und auch für Gesten, einfache Texteingaben und das Erfassen freiformfreier Gedanken in Freiform verwendet werden.

Der stift, der für die Eingabe verwendet wird, verfügt über eine feinen, reibungslosen Tipp, der präzises Zeigen, Schreiben oder Zeichnen in Ink unterstützt. Der Stift kann auch über eine optionale Stiftschaltfläche (die zum Ausführen von Rechtsklicks verwendet wird) und einen Radierer (zum Löschen von Freidruck) verfügen. Die meisten Stifte unterstützen das Hovern.

![Abbildung eines typischen Stifts ](images/inter-pen-image1.png)

Ein typischer Stift.

Wenn der Stift für die Handschrift verwendet wird, können die Striche des Benutzers mithilfe der Handschrifterkennung in Text konvertiert werden. Die Striche können so beibehalten werden, wie sie geschrieben wurden, und die Erkennung wird im Hintergrund durchgeführt, um das Suchen und Kopieren als Text zu unterstützen. Solche nicht konvertierten Striche werden als digital ink bezeichnet.

![Screenshot der Handschrift auf einer OneNote-Seite ](images/inter-pen-image2.png)

Ein Beispiel für die Eingabe von Ink.

Die Windows sind bereits stiftfreundlicher, da ein Stift anstelle einer Maus verwendet werden kann, der Stift für die wichtigsten Aufgaben und Interaktionen reibungslos funktioniert und das Programm auf Gesten reagiert. Ein Programm wird handschriftlich, wenn es bei der Eingabe von handschriftlichem Text hilft. Ein Programm wird ink aktiviert, wenn es Ink direkt verarbeiten kann, anstatt dass Stiftstriche in Text oder entsprechende Mausbewegungen übersetzt werden müssen. Auf diese Weise können Benutzer Kommentare in frei strömenden, hochwertigen digitalen Freidruck schreiben, zeichnen und hinzufügen. Das Sammeln von Ink-Daten ist anders als das Sammeln von Mausereignissen, da Ink eine höhere Auflösung und eine höhere Abtastrate erfordert und auch bei Druck und Neigung zu Nuancen beigeraten werden kann. Informationen zum Erstellen von handschriftfreundlichen und ink-fähigen Programmen finden Sie unter [Integrieren von Ink-](/previous-versions/windows/desktop/ms700674(v=vs.85)) und [Texteingaben mithilfe des Stifts](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Beim Positionieren eines Stifts ist ein Cursor weniger notwendig, da die Spitze sich selbst darstellt. Für die Zielunterstützung stellt Windows einen kleinen Stiftcursor zur Verfügung, der die aktuelle Stiftposition angibt. Im Gegensatz zum ersetzten Mauszeiger wird der Stiftcursor nur benötigt, wenn sich der Stift in der Nähe der Anzeige befindet, sodass er nach einigen Sekunden Inaktivität verschwindet, um eine nicht strukturierte Ansicht der Informationen zu ermöglichen.

Die meisten stiftfreundlichen Programme unterstützen Gesten. Eine Geste ist eine schnelle Bewegung des Stifts auf einem Bildschirm, der vom Computer als Befehl und nicht als Mausbewegung, Schreiben oder Zeichnen interpretiert wird. Eine der schnellsten und einfachsten Gesten ist ein Flick. Ein Flick ist eine einfache Geste, die zur Navigation oder einem Bearbeitungsbefehl führt. Navigationsflicks umfassen Ziehen nach oben, Ziehen nach unten, Zurück bewegen und Vorwärtsbewegungen, während Bearbeitungsflicks kopieren, einfügen, rückgängig machen und löschen.

Alle Zeiger mit Ausnahme des ausgelastet-Zeigers verfügen über einen Hotspot mit einem einzelnen Pixel, der die genaue Bildschirmposition des Zeigers definiert. Der Hotspot bestimmt, welches Objekt von der Interaktion betroffen ist. Objekte definieren eine heiße Zone. Dies ist der Bereich, in dem der Hotspot als über dem Objekt betrachtet wird. In der Regel stimmt die heiße Zone mit den Rahmen eines Objekts überein, aber es kann größer sein, um die Interaktion zu vereinfachen.

**Da ein Stift präziser zeigen kann als ein Finger, funktioniert die Benutzeroberfläche auch gut für einen Stift.** Daher konzentriert sich dieser Artikel hauptsächlich auf das Hinzufügen von Stiftunterstützung zu Programmen, die bereits für touch entwickelt wurden.

**Hinweis:** Richtlinien im Zusammenhang [mit Maus,](inter-mouse.md) [Barrierefreiheit](inter-accessibility.md)und [Touch](inter-touch.md) sind in separaten Artikeln dargestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Die Verwendung eines Stifts für die Eingabe hat die folgenden Merkmale:

-   **Natürlich und intuitiv.** Jeder weiß, wie er mit einem Stift zeigt und tippt. Objektinteraktionen sind so konzipiert, dass sie der konsistenten Interaktion von Benutzern mit Objekten in der realen Welt entsprechen.
-   **Ausdrucksstark.** Striche eines Stifts sind einfach zu steuern und erleichtern das Schreiben, Zeichnen, Skizzieren, Zeichnen und Kommentieren, als dies mit einer Maus zu tun.
-   **Persönlicher.** Ebenso wie eine handschriftliche Notiz oder Signatur persönlicher ist als eine typierte, ist die Verwendung eines digital handschriftlichen Hinweises oder einer Signatur auch persönlicher.
-   **Weniger intrusiv.** Die Verwendung eines Stifts ist im Hintergrund und daher viel weniger störend als das Eingeben oder Klicken, insbesondere in sozialen Situationen wie Besprechungen.
-   **Tragbar.** Ein Computer mit Stiftfunktion kann kompakter sein, da die meisten Aufgaben ohne Tastatur, Maus oder Touchpad abgeschlossen werden können. Sie kann flexibler sein, da sie keine Arbeitsoberfläche erfordert. Sie ermöglicht neue Orte und Szenarien für die Verwendung eines Computers.
-   **Direkt und ansprechend.** Wenn Sie einen Stift verwenden, haben Sie das Gefühl, direkt mit den Objekten auf dem Bildschirm zu interagieren, während die Verwendung einer Maus oder eines Touchpads immer erfordert, dass Sie Handbewegungen mit separaten Zeigerbewegungen auf dem Bildschirm koordinieren, die sich im Vergleich indirekt anfühlen.

**Alle Windows-Programme sollten eine gute Stifterfahrung haben.** Benutzer sollten in der Lage sein, die wichtigsten Aufgaben Ihres Programms effizient mithilfe eines Stifts auszuführen. Einige Aufgaben, z. B. die Eingabe oder die ausführliche Pixelbearbeitung, sind für einen Stift nicht geeignet, sollten aber zumindest möglich sein.

Wenn Ihr Programm bereits gut entworfen und touch-nutzerfreundlich ist, ist es einfach, eine gute Stiftunterstützung zu bieten. Zu diesem Zweck ist ein gut entworfenes Programm:

-   **Verfügt über eine gute Mausunterstützung.** Die interaktiven Steuerelemente verfügen über klare, sichtbare Vorgabe und zeigen auf Zustände, um Zeigerfeedback zu erhalten. Objekte haben Standardverhalten für die standardmäßigen Mausinteraktionen (einzelner und doppelter Linkklick, Rechtsklick, Ziehen und Zeigen). Die [Zeigerform ändert sich](inter-mouse.md) entsprechend, um den Typ der direkten Bearbeitung anzugeben.
-   **Verfügt über eine gute Tastaturunterstützung.** Das Programm macht Benutzer effizient, indem standardmäßige Tastenkombinationszuweisungen zur Verfügung stellen, insbesondere für Navigations- und Bearbeitungsbefehle, die auch über Gesten generiert werden können.
-   **Verfügt über Steuerelemente, die groß genug für touch sind.** Die Steuerelemente haben eine Mindestgröße von 23 x 23 Pixel (13x13 Dialogeinheiten-DLUs), und die am häufigsten verwendeten Steuerelemente sind mindestens \[ \] 40 x 40 Pixel (23 x 22 DLUs). Um nicht reagierende Verhalten zu vermeiden, sollten keine kleinen Lücken zwischen Zielen bestehen, in denen die Benutzeroberflächenelemente leerzeichen werden sollten, sodass benachbarte Ziele entweder berührt werden oder mindestens 5 Pixel (3 DLUs) Abstand zwischen ihnen haben.
-   **Ist zugänglich.** Verwendet Microsoft Active Accessibility (MSAA), um programmgesteuerten Zugriff auf die Benutzeroberfläche für Hilfstechnologien zu ermöglichen. Das Programm reagiert entsprechend auf Design- und Systemmetrikänderungen.
-   **Funktioniert gut und sieht gut in 120 dpi (Punkte pro Zoll)** aus. Dies ist die empfohlene Standardanzeigeauflösung für stiftfähige Computer.
-   **Verwendet allgemeine Steuerelemente.** Die gängigsten Steuerelemente sind so konzipiert, dass sie eine gute Stifterfahrung unterstützen. Bei Bedarf verwendet das Programm gut implementierte benutzerdefinierte Steuerelemente, die eine einfache Zielgruppenadressierung und interaktive Bearbeitung unterstützen.
-   **Verwendet eingeschränkte Steuerelemente.** Wenn eingeschränkte Steuerelemente wie Listen und Schieberegler für einfache Zielgruppenadressierung konzipiert sind, können sie besser als schränkte Steuerelemente wie Textfelder sein, da sie die Notwendigkeit von Texteingaben reduzieren.
-   **Stellt entsprechende Standardwerte zur** Das Programm wählt standardmäßig die sicherste Option (um Datenverluste oder Systemzugriffe zu verhindern) und die sicherste Option aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählt das Programm die wahrscheinlichste oder bequemste Option aus, wodurch unnötige Interaktion vermieden wird.
-   **Ermöglicht die automatische Vervollständigung von Text.** Stellt eine Liste der wahrscheinlichsten oder kürzlich eingegebenen Werte zur Einfacherkeit der Texteingaben zur Verfingung von Daten zur 1.

Leider gilt das Gegenteil auch, wenn Ihr Programm nicht gut entworfen wurde. Seine Mängel werden für Benutzer, die einen Stift verwenden, besonders offensichtlich sein.

### <a name="model-for-pen-interaction"></a>Modell für Stiftinteraktion

Wenn Sie noch keine Erfahrung mit der Verwendung eines Stifts haben, ist die beste Einführung, indem Sie lernen, indem Sie dies tun. Holen Sie sich einen Stift-fähigen Computer, halten Sie Maus und Tastatur beiseite, und erledigen Sie die Aufgaben, die Sie normalerweise nur mit einem Stift ausführen. Achten Sie darauf, sowohl ink-fähige Programme wie Windows Journal als auch Programme auszuprobieren, die nicht ink-fähig sind. Wenn Sie über einen Tablet-PC verfügen, experimentieren Sie damit, ihn an unterschiedlichen Positionen zu halten, z. B. auf Dem Runden, flach auf einem Tisch oder in den Arme, während Sie stehen. Versuchen Sie, es im Hochformat und im Querformat zu verwenden, und halten Sie den Stift zum Schreiben und nur zum Zeigen in ihrer linken und rechten Hand.

Wenn Sie mit der Verwendung eines Stifts experimentieren, werden Sie Dies feststellen:

-   **Kleine Steuerelemente sind schwierig zu verwenden.** Die Größe der Steuerelemente wirkt sich stark auf Ihre Fähigkeit aus, effektiv zu interagieren. Steuerelemente mit einer Größe von 10 x 10 Pixeln funktionieren einigermaßen für einen Stift, größere Steuerelemente sind jedoch noch komfortabler zu verwenden. [Drehsteuerelemente](ctrl-spin-controls.md) (15 x 11 Pixel) sind beispielsweise zu klein, um sie problemlos mit einem Stift verwenden zu können.
-   **Die Übergabe ist ein Faktor.** Ihre Hand deckt manchmal Dinge ab, die Sie möglicherweise sehen oder mit denen Sie interagieren möchten. Beispielsweise sind Kontextmenüs für rechtshändige Benutzer schwer zu verwenden, wenn sie rechts vom Klickpunkt angezeigt werden. Es ist also besser, wenn sie auf der linken Seite angezeigt werden. Windows können Benutzer ihre Hand im Tablet PC-Steuerelement Einstellungen angeben.
-   **Task-Lokalität hilft.** Sie können den Mauszeiger zwar mit einer 3-Zoll-Mausbewegung über einen 14-Zoll-Bildschirm bewegen. Bei Verwendung eines Stifts müssen Sie die Hand jedoch auf die vollen 14 Zoll bewegen. Das wiederholte Verschieben zwischen zielen, die weit voneinander entfernt sind, kann mühsam sein, daher ist es viel besser, Aufgabeninteraktionen nach Möglichkeit innerhalb des Bereichs einer ruheenden Hand zu halten. Kontextmenüs sind praktisch, da sie keine Handbewegung erfordern.
-   **Texteingabe und -auswahl sind schwierig.** Die Verwendung eines Stifts für lange Texteingaben ist besonders schwierig, sodass die automatische Vervollständigung und akzeptable Textwerte Aufgaben wirklich vereinfachen können. Die Textauswahl kann auch recht schwierig sein, sodass Aufgaben einfacher sind, wenn sie keine präzise Cursorplatzierung erfordern.
-   **Kleine Ziele in der Nähe des Bildschirmrands können sehr schwierig zu tippen sein.** Einige Display-Blenden stehen vor, und einige Touchscreentechnologien sind weniger empfindlich an den Rändern, wodurch die Verwendung von Steuerelementen in der Nähe des Edges erschwert wird. Beispielsweise können die Schaltflächen Minimieren, Maximieren/Wiederherstellen und Schließen auf der Titelleiste schwieriger zu verwenden sein, wenn ein Fenster maximiert ist.

### <a name="control-location"></a>Steuerungsposition

Task-Lokalität reduziert mühsam wiederholte bildschirmübergreifende Bewegungen. Um Handbewegungen zu minimieren, suchen Sie Steuerelemente in der Nähe des Orts, an dem sie am wahrscheinlichsten verwendet werden.

**Falsch:**

![Screenshot der farbpalette getrennt von Tools ](images/inter-pen-image3.png)

In diesem Beispiel Windows XP ist die Farbpalette zu weit von dem Ort entfernt, an dem sie wahrscheinlich verwendet wird.

Beachten Sie, dass der aktuelle Standort des Benutzers dem ziel am nächsten liegt, was das Erwerben trivial macht. Daher nutzen Kontextmenüs das [Fitts'-Gesetz](inter-mouse.md)in vollem Sinne, ebenso wie die mini-Symbolleisten, die von Microsoft Office.

![Screenshot von Zeigern in der Nähe von Menüs ](images/inter-pen-image4.png)

Die aktuelle Zeigerposition ist immer am einfachsten zu erhalten.

Kleine Ziele in der Nähe des Anzeigerands können schwierig zu erreichen sein. Platzieren Sie daher keine kleinen Steuerelemente in der Nähe von Fensterrändern. Um sicherzustellen, dass Steuerelemente beim Maximieren eines Fensters einfach als Ziel festgelegt werden können, legen Sie sie entweder auf mindestens 23 x 23 Pixel (13 x 13 DLUs) fest, oder platzieren Sie sie vom Fensterrand.

### <a name="pen-interactions"></a>Stiftinteraktionen

**Systemgesten**

Systemgesten werden von der -Windows. Daher haben alle Windows Zugriff darauf. Diese Gesten verfügen über entsprechende Maus-, Tastatur- und Anwendungsbefehlsmeldungen:



| System-Geste                                                           | Synthetisierte äquivalente Nachricht                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Hovern (falls unterstützt)<br/>                          | Mauszeigerzeiger<br/>                        |
| Tippen (nach unten und nach oben)<br/>                               | Klicken mit der Maus mit der linken Maustaste<br/>                   |
| Doppeltippen (zweimal nach unten und nach oben)<br/>                  | Doppelklicken mit der Maus mit der linken Maustaste<br/>            |
| Halten Sie gedrückt (nach unten, anhalten, nach oben).<br/>                | Rechtsklick mit der Maus<br/>                  |
| Ziehen (nach unten, nach oben)<br/>                           | Maus nach links ziehen<br/>                    |
| Drücken, Halten und Ziehen (nach unten, Anhalten, Verschieben, Nach oben)<br/>   | Ziehen mit der rechten Maustaste<br/>                   |
| Wählen Sie (nach unten, über auswählbare Objekte, nach oben)<br/> | Mausauswahl<br/>                       |



 

**Entwickler:** Weitere Informationen finden Sie unter [SystemGesture-Enumeration.](/previous-versions/ms552724(v=vs.100))

**Flicks**

Flicks sind einfache Gesten, die in etwa den Tastenkombinationen entsprechen. Navigationsflicks umfassen Ziehen nach oben, Ziehen nach unten, Zurück- und Vorwärtsbewegung. Bearbeitungsflicks umfassen Kopieren, Einfügen, Rückgängig und Löschen. Um Flicks zu verwenden, muss Ihr Programm nur auf die zugehörigen Tastatureingabebefehle reagieren.

![Diagramm mit Denkbewegungen und ihren Standardzuweisungen in Windows 7.](images/inter-pen-image5.png)

Die acht Flickgesten und ihre Standardzuweisungen in Windows 7. Die Navigationsflicks wurden so geändert, dass sie dem Schwenken (bei dem das Objekt mit der Geste bewegt wird) entsprechen, anstatt zu scrollen (wobei sich das Objekt in die entgegengesetzte Richtung der Geste bewegt).

![Abbildung von Blättern, z. B. der Bewegung ](images/inter-pen-image6.png)

Die acht Flickgesten und ihre Standardzuweisungen in Windows Vista.

Die Navigationsflicks verfügen über eine natürliche Zuordnung, sodass sie leicht zu erlernen und zu merken sind. Die Bearbeitungsflicks sind Diagonalen, die mehr Genauigkeit erfordern, und ihre Zuordnungen sind nicht so natürlich (zu löschende Papierkorb, Nach-unten-Pfeilrichtung zum Rückgängig machen), sodass diese nicht standardmäßig aktiviert sind. Alle Flickaktionen können mit dem Stift und dem Systemsteuerungselement Eingabegeräte angepasst werden.



| Flick                                     | Synthetisierte äquivalente Nachricht                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Nach links blättern<br/>                | Forward-Befehl (Befehl "Zurück" für Windows Vista)<br/> |
| Nach rechts blättern<br/>               | Befehl "Zurück" (Befehl "Weiter" für Windows Vista)<br/> |
| Flick up<br/>                  | Tastatur scrollen nach unten<br/>                             |
| Nach unten blättern<br/>                | Tastatur scrollen nach oben<br/>                               |
| Nach oben nach links diagonal blättern<br/>    | Tastaturlöschung<br/>                                  |
| Nach links nach unten blättern (diagonal)<br/>  | Tastatur rückgängig machen<br/>                                    |
| Nach oben rechts diagonal blättern<br/>   | Tastaturkopie<br/>                                    |
| Nach rechts nach unten diagonal blättern<br/> | Tastatur einfügen<br/>                                   |



 

**Anwendungsgesten**

Anwendungen können auch andere Gesten definieren und verarbeiten. Die Microsoft-Gestenerkennung kann über [40 Gesten erkennen.](../tablet/application-gestures-and-semantic-behavior.md) Um Anwendungsgesten zu verwenden, muss ihr Programm die gesten definieren, die es erkennt, und dann die resultierenden Ereignisse behandeln.

**Reaktionsfähigkeit und Konsistenz**

**Reaktionsfähigkeit ist entscheidend für die Erstellung von Stifterfahrungen, die direkt und ansprechend sind.** Um direkt zu sein, müssen Gesten sofort wirksam werden, und die Kontaktpunkte eines Objekts müssen während der gesamten Geste reibungslos unter dem Stift bleiben. Verzögerungen, abgesenkte Antworten, Kontaktverluste oder ungenaue Ergebnisse zerstören die Wahrnehmung der direkten Manipulation und der Qualität.

**Konsistenz ist wichtig, um Stifterfahrungen zu erstellen, die sich natürlich und intuitiv anfühlen.** Sobald Benutzer eine Standardgeste erlernen, erwarten sie, dass diese Geste in allen anwendbaren Programmen die gleiche Wirkung hat. Weisen Sie Standardgesten niemals nicht standardmäßige Bedeutungen zu, um Verwirrung und Frust zu vermeiden. Verwenden Sie stattdessen benutzerdefinierte Gesten für Interaktionen, die für Ihr Programm eindeutig sind.

**Bearbeiten von Ink und Text**

Das Bearbeiten von Ink und Text gehört zu den anspruchsvollsten Interaktionen bei Verwendung eines Stifts. Durch die Verwendung von eingeschränkten Steuerelementen, entsprechenden Standardwerten und automatischer Vervollständigung wird die Texteingabe entfällt oder reduziert. Wenn Ihr Programm jedoch das Bearbeiten von Text oder Ink umfasst, können Sie Benutzer produktiver machen, indem Sie die Eingabebenutzeroberfläche standardmäßig auf bis zu **150** Prozent zoomen, wenn ein Stift verwendet wird.

Beispielsweise könnte ein E-Mail-Programm die Benutzeroberfläche in normaler Größe anzeigen, aber die Eingabebenutzeroberfläche auf 150 Prozent zoomen, um Nachrichten zu verfassen.

![Screenshot der Outlook-Nachricht in großer Schrift ](images/inter-pen-image7.png)

In diesem Beispiel wird die Eingabebenutzeroberfläche auf 150 Prozent vergrößert.

**Wenn Sie nur vier Dinge tun...**

1.  1. Sorgen Sie dafür Windows dass Ihre Programme über eine gute Stifterfahrung verfügen! Benutzer sollten in der Lage sein, die wichtigsten Aufgaben Ihres Programms effizient mithilfe eines Stifts auszuführen (zumindest die Aufgaben, die keine große Menge an Eingaben oder ausführliche Pixelbearbeitungen umfassen).
2.  2. Erwägen Sie das Hinzufügen von Unterstützung für das Schreiben, Zeichnen und Hinzufügen von Kommentaren direkt mithilfe von Ink in den relevantesten Szenarien.
3.  3. Um eine direkte und ansprechende Benutzeroberfläche zu erstellen, werden Gesten sofort wirksam, Kontaktpunkte bleiben während der gesamten Geste reibungslos unter dem Stift des Benutzers, und die Gesten werden direkt der Bewegung des Benutzers angezeigt.
4.  4. Um ein natürliches und intuitives Erlebnis zu schaffen, unterstützen Sie entsprechende Standardgesten und weisen ihnen ihre Standardbe bedeutung zu. Verwenden Sie benutzerdefinierte Gesten für Interaktionen, die für Ihr Programm eindeutig sind.

## <a name="guidelines"></a>Richtlinien

### <a name="control-usage"></a>Steuern der Nutzung

-   **Verwenden Sie lieber allgemeine Steuerelemente.** Die gängigsten Steuerelemente sind so konzipiert, dass sie eine gute Stifterfahrung unterstützen.
-   **Bevorzugen Sie eingeschränkte Steuerelemente.** Verwenden Sie nach Möglichkeit eingeschränkte Steuerelemente wie Listen und Schieberegler anstelle von nicht eingeschränkten Steuerelementen wie Textfeldern, um die Notwendigkeit von Texteingaben zu reduzieren.
-   **Geben Sie die entsprechenden Standardwerte an.** Wählen Sie standardmäßig die sicherste Option (um Datenverlust oder Systemzugriff zu verhindern) und die sicherste Option aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Option aus, um unnötige Interaktionen zu vermeiden.
-   **Geben Sie die automatische Vervollständigung von Text an.** Geben Sie eine Liste der wahrscheinlichsten oder kürzlich eingegebenen Werte an, um die Texteingabe erheblich zu vereinfachen.
-   **Wenn für wichtige Aufgaben, die mehrfache Auswahl verwenden, normalerweise eine Standardliste mit Mehrfachauswahl verwendet wird, stellen Sie stattdessen eine Option zur Verwendung einer Kontrollkästchenliste zur Verfügung.**
-   **Systemmetriken werden beachtet.** Verwenden Sie Systemmetriken für alle Größen, die keine Hardwiregrößen haben. Bei Bedarf können Benutzer die Systemmetriken oder dpi ändern, um ihre Anforderungen zu erfüllen. Behandeln Sie dies jedoch als letzten Ausweg, da Benutzer die Systemeinstellungen normalerweise nicht anpassen müssen, um die Benutzeroberfläche nutzbar zu machen.

![Screenshot von Menüs mit normaler und großer Größengröße ](images/inter-pen-image8.png)

In diesem Beispiel wurde die Systemmetrik für die Menühöhe geändert.

### <a name="control-sizing-layout-and-spacing"></a>Steuern von Größe, Layout und Abstand

-   **Verwenden Sie für allgemeine Steuerelemente die empfohlenen Steuerelementgrößen.** Diese sind groß genug für eine gute Stifterfahrung, mit Ausnahme von Drehungssteuerelementen (die nicht mit einem Stift, aber redundant sind) nutzbar sind.
-   **Wählen Sie ein Layout aus, das Steuerelemente in der Nähe des Orts platziert, an dem sie am wahrscheinlichsten verwendet werden.** Halten Sie Aufgabeninteraktionen nach Möglichkeit in einem kleinen Bereich. Vermeiden Sie Handbewegungen mit langer Entfernung, insbesondere bei häufigen Aufgaben und bei Ziehbewegungen.
-   **Verwenden Sie den empfohlenen Abstand.** Der empfohlene Abstand ist stiftnutzerfreundlich.
-   **Interaktive Steuerelemente sollten entweder berührend sein oder vorzugsweise mindestens 5 Pixel (3 DLUs) Abstand zwischen ihnen haben.** Dies verhindert Verwirrung, wenn Benutzer außerhalb des vorgesehenen Ziels tippen.
-   **Fügen Sie in Gruppen** von Steuerelementen, z. B. Befehlslinks, Kontrollkästchen und Optionsfeldern, sowie zwischen den Gruppen mehr als den empfohlenen vertikalen Abstand hinzu. Dies erleichtert die Unterscheidung.

### <a name="interaction"></a>Interaktion

-   **Aktivieren Sie für Programme, die für die Annahme von Handschrift konzipiert sind, die Standard-Inking-Funktion.** Mit der Standardeingabe können Benutzer Ink eingeben, indem sie einfach mit dem Schreiben beginnen, ohne tippen, einen Befehl ausführen oder etwas Besonderes tun zu müssen. Dadurch wird die natürlichste Erfahrung mit einem Stift ermöglicht. Bei Programmen, die nicht zum Akzeptieren von Handschrift entwickelt wurden, behandeln Sie Stifteingaben in Textfeldern als Auswahl.
-   **Benutzern das Zoomen der Inhaltsbenutzeroberfläche ermöglichen,** wenn Ihr Programm Über aufgaben verfügt, die die Bearbeitung von Text erfordern. Erwägen Sie, automatisch auf 150 Prozent zu zoomen, wenn ein Stift verwendet wird.
-   **Da Gesten auswendig sind, weisen Sie ihnen Bedeutungen zu, die programmübergreifend konsistent sind.** Geben Sie Gesten mit fester Semantik keine unterschiedlichen Bedeutungen. Verwenden Sie stattdessen eine entsprechende programmspezifische Geste.

### <a name="handedness"></a>Händigkeit

-   **Wenn ein Fenster kontextbezogen ist, wird es immer in der Nähe des Objekts angezeigt, von dem es gestartet wurde.** Platzieren Sie sie im Weg, damit das Quellobjekt nicht durch das Fenster abgedeckt wird.
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
-   Verwenden Sie tippen (und doppelt tippen), anstatt zu klicken, wenn Sie prozedurspezifische Prozeduren für die Verwendung eines Stifts dokumentieren. Tippen bedeutet, den Bildschirm zu drücken und dann vor einer Haltezeit zu heben. Sie kann verwendet werden, um einen Mausklick zu generieren. Verwenden Sie für Interaktionen, bei denen der Stift nicht verwendet wird, weiterhin Klick.


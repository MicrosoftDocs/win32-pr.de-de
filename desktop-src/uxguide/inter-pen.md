---
title: Stift
description: Alle Microsoft Windows-Anwendungen sollten Stift fähig sein. Und das ist einfacher, als Sie es nachzudenken.
ms.assetid: 45635d5a-c9ff-47d0-89ef-a9c48ac67594
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 35994f345306bd3a270f8d8cf9760e7d07183941
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869383"
---
# <a name="pen"></a>Stift

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Alle Microsoft Windows-Anwendungen sollten Stift fähig sein. Und das ist einfacher, als Sie es nachzudenken.

Pen Input bezieht sich auf die Art und Weise, wie Sie mit einem Stift direkt mit einem Computer interagieren können. Ein Stift kann verwendet werden, um auch auf Gesten, einfache Texteingaben und das Erfassen von Freiform-Gedanken in digitaler Hand Eingaben zu zeigen.

Der für die Eingabe verwendete Stift verfügt über einen guten, glatten Tipp, der das präzise zeigen, schreiben oder zeichnen in frei Hand Eingaben unterstützt. Der Stift kann auch eine optionale Stift Schaltfläche (mit Rechtsklick) und Radierer (verwendet zum Löschen von frei Hand Eingaben) enthalten. Die meisten Stifte unterstützen den Hover.

![Abbildung eines typischen Stifts ](images/inter-pen-image1.png)

Ein typischer Stift.

Wenn der Stift für die Handschrift verwendet wird, können die Striche des Benutzers mithilfe der Handschrifterkennung in Text konvertiert werden. Die Striche können genauso wie Sie geschrieben werden, wobei die Erkennung im Hintergrund durchgeführt wird, um das Suchen und kopieren als Text zu unterstützen. Solche nicht konvertierten Striche werden als digitaler frei Hand Eingaben bezeichnet.

![Screenshot der Handschrift auf der OneNote-Seite ](images/inter-pen-image2.png)

Ein Beispiel für eine frei Hand Eingabe.

Die meisten Windows-Programme sind bereits Stift freundlich, da ein Stift anstelle einer Maus verwendet werden kann. der Stift funktioniert für die meisten wichtigen Aufgaben und Interaktionen reibungslos, und das Programm antwortet auf Gesten. Ein Programm wird Handschrift freundlich, wenn es mit Hand schriftlichem Texteingaben unterstützt. Ein Programm wird frei Hand fähig, wenn es frei Hand Eingaben direkt verarbeiten kann, anstatt dass Stift Striche in Text oder äquivalente Mausbewegungen übersetzt werden müssen. Dies ermöglicht Benutzern das Schreiben, zeichnen und Hinzufügen von Kommentaren in kostenlosem, qualitativ hochwertiger digitaler frei Hand Eingaben. Das Sammeln von frei Hand Eingaben unterscheidet sich von der Erfassung von Mausereignissen, da Freihand eine höhere Auflösung und eine höhere Samplingrate erfordert und außerdem Nuance mit Druck und Neigung hinzugefügt werden kann Informationen zum Erstellen von Handschrift freundlichen und frei Hand fähigen Programmen finden Sie unter [integrieren](/previous-versions/windows/desktop/ms700674(v=vs.85)) von frei Hand [Eingaben und Text Eingaben mit dem Stift](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Bei der Positionierung eines Stifts ist ein Cursor weniger erforderlich, da der Tipp sich selbst repräsentiert. Für die Unterstützung von Unterstützung bietet Windows jedoch einen kleinen Stift Cursor, der die aktuelle Stift Position angibt. Anders als der Mauszeiger, der durch ihn ersetzt wird, wird der Stift Cursor nicht benötigt, es sei denn, der Stift befindet sich in der Nähe der Anzeige, sodass er nach einigen Sekunden Inaktivität verschwindet, um eine nicht gesperrte Ansicht von Informationen zuzulassen

Die meisten Stift freundlichen Programme unterstützen Gesten. Eine Geste ist eine schnelle Bewegung des Stifts auf einem Bildschirm, den der Computer als Befehl interpretiert, nicht als Mausbewegung, schreiben oder zeichnen. Eine der schnellsten und einfachsten Gesten ist ein Flick. Ein Flick ist eine einfache Geste, die zur Navigation oder zum Bearbeitungs Befehl führt. Navigations schnelle Stift Bewegungen umfassen "Drag up", "Drag", "Move" und "Forward", während das Bearbeiten von schnelle Stift Bewegungen kopieren, einfügen, rückgängig und löschen einschließt.

Alle Zeiger außer dem ausgelasteten Zeiger verfügen über einen einzelnen Pixel-Hotspot, der die exakte Bildschirmposition des Zeigers definiert. Der Hotspot bestimmt, welches Objekt von der Interaktion betroffen ist. -Objekte definieren eine heiße Zone, bei der es sich um den Bereich handelt, in dem der Hotspot als über dem Objekt betrachtet wird. In der Regel stimmt die Hot-Zone mit den Rahmen eines Objekts überein, kann jedoch größer sein, um die Interaktion zu vereinfachen.

**Da ein Stift mehr als einen Finger zeigen kann, funktioniert die Benutzeroberfläche auch für einen Stift gut, wenn die Benutzeroberfläche für die Fingereingabe geeignet ist.** Folglich konzentriert sich dieser Artikel hauptsächlich auf das Hinzufügen von Stift Unterstützung für Programme, die bereits für die Fingereingabe konzipiert wurden.

**Hinweis:** Richtlinien, die sich auf [Maus](inter-mouse.md), [Barrierefreiheit](inter-accessibility.md)und Fingereingabe beziehen [, werden in](inter-touch.md) separaten Artikeln dargestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Die Verwendung eines Stifts für die Eingabe weist die folgenden Eigenschaften auf:

-   **Natürlich und intuitiv.** Jeder weiß, wie Sie auf einen Stift zeigen und tippen. Objekt Interaktionen sind so konzipiert, dass Sie auf konsistente Weise mit Objekten in der realen Welt interagieren.
-   **Ausdrückliche.** Striche eines Stifts können leicht gesteuert werden, sodass das Schreiben, zeichnen, neigen, zeichnen und kommentieren einfacher ist, als dies mit einer Maus.
-   **Persönlicher.** Ebenso wie eine handschriftliche Notiz oder eine Signatur, die eine typisierte Notiz ist, ist die Verwendung einer Digital handschriftlichen Notiz oder Signatur auch persönlicher.
-   **Weniger intrusiv.** Die Verwendung eines Stifts ist unbeaufsichtigt und daher weniger stark ablenkend als bei der Eingabe oder dem klicken, insbesondere in sozialen Situationen wie Besprechungen.
-   **Tabel.** Ein Computer mit einer Stift Funktion kann kompakter sein, da die meisten Aufgaben ohne Tastatur, Maus oder Touchpad abgeschlossen werden können. Sie kann flexibler sein, da Sie keine Arbeitsoberfläche erfordert. Sie ermöglicht neue Orte und Szenarios für die Verwendung eines Computers.
-   **Direkt und Engagement.** Wenn Sie einen Stift verwenden, haben Sie das Gefühl, dass Sie direkt mit den Objekten auf dem Bildschirm interagieren, während Sie mit der Maus oder dem Touchpad immer die Handbewegungen mit separaten Zeiger Bewegungen auf dem Bildschirm koordinieren müssen, die indirekt durch Vergleiche zueinander stehen.

**Alle Windows-Programme sollten eine gute Stift Darstellung haben.** Benutzer sollten in der Lage sein, die wichtigsten Aufgaben Ihres Programms effizient mithilfe eines Stifts auszuführen. Einige Aufgaben, z. b. Typisierung oder detaillierte Pixel Bearbeitung, eignen sich nicht für einen Stift, Sie sollten jedoch zumindest möglich sein.

Wenn Ihr Programm bereits gut entworfen wurde und Berührungs freundlich ist, ist es einfach, eine gute Stift Unterstützung zu bieten. Zu diesem Zweck ein gut konzipiertes Programm:

-   **Bietet eine gute Mausunterstützung.** Die interaktiven Steuerelemente verfügen über klare, sichtbare Kosten und haben Hover-Status für Zeiger Feedback. Objekte verfügen über Standardverhalten für die Standard Maus Interaktionen (Single und Double Left-click, Right-Click, Drag und Hover). Die [Form des Zeigers](inter-mouse.md) ändert sich entsprechend, um den Typ der direkten Bearbeitung anzugeben.
-   **Bietet eine gute Tastatur Unterstützung.** Das Programm vereinfacht Benutzer durch die Bereitstellung von Standardtasten Zuweisungen, insbesondere für Navigations-und Bearbeitungsbefehle, die auch durch Gesten generiert werden können.
-   **Verfügt über Steuerelemente, die für den Touchscreen groß genug sind** Die Steuerelemente haben eine minimale Größe von 23x23 Pixel (13 x 13 Dialogfeld Einheiten \[ -DLUs \] ), und die am häufigsten verwendeten Steuerelemente sind mindestens 40 x 40 Pixel (23x22-DLUs). Um ein nicht reagierendes Verhalten zu vermeiden, sollten zwischen den Zielen keine kleinen Lücken bestehen, in denen die Benutzeroberflächen Elemente einen Abstand aufweisen, sodass angrenzende Ziele entweder berühren oder mindestens 5 Pixel (3 DLUs) enthalten.
-   **Ist verfügbar.** Verwendet Microsoft Active Accessibility (MSAA), um programmgesteuerten Zugriff auf die Benutzeroberfläche für Hilfstechnologien bereitzustellen. Das Programm antwortet entsprechend auf Design-und systemmetrikänderungen.
-   **Funktioniert gut und sieht in 120 dpi (Punkte pro Zoll) gut aus** . Dies ist die empfohlene Standard Anzeige Auflösung für Computer mit aktiviertem Stift.
-   **Verwendet allgemeine Steuerelemente.** Die meisten gängigen Steuerelemente sind darauf ausgelegt, eine gute Stift Darstellung zu unterstützen. Bei Bedarf verwendet das Programm gut implementierte benutzerdefinierte Steuerelemente, die zur Unterstützung einfacher Ziel-und interaktiver Bearbeitung entworfen wurden.
-   **Verwendet eingeschränkte Steuerelemente.** Wenn eine einfache Zielplattform entwickelt wurde, können eingeschränkte Steuerelemente wie Listen und Schieberegler besser als nicht eingeschränkte Steuerelemente wie Textfelder sein, da Sie den Bedarf an Texteingaben verringern.
-   **Stellt geeignete Standardwerte bereit.** Das Programm wählt die sicherste Option (um Datenverluste oder System Zugriffe zu verhindern) und die sicherste Option standardmäßig aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählt das Programm die wahrscheinlichste oder bequeme Option aus, wodurch unnötige Interaktionen vermieden werden.
-   **Stellt automatische Text Vervollständigung bereit.** Stellt eine Liste der wahrscheinlichsten oder vor kurzem eingegebenen Werte bereit, um die Texteingabe erheblich zu vereinfachen.

Leider trifft das Gegenteil auch dann zu, wenn das Programm nicht gut entworfen wurde. seine Mängel werden für Benutzer, die einen Stift verwenden, besonders offensichtlich.

### <a name="model-for-pen-interaction"></a>Modell für Stift Interaktion

Wenn Sie mit der Verwendung eines Stifts nicht vertraut sind, können Sie sich mit der besten Einführung vertraut machen. Holen Sie sich einen Stift fähigen Computer, platzieren Sie die Maus und die Tastatur, und führen Sie die Aufgaben aus, die Sie normalerweise mithilfe eines Stifts durchführen. Stellen Sie sicher, dass Sie sowohl frei Hand fähige Programme, wie z. b. Windows Journal, als auch Programme verwenden, die nicht frei Hand fähig sind. Wenn Sie über einen Tablet PC verfügen, experimentieren Sie mit dem halten an verschiedenen Positionen, z. b. in Ihrem Schoß, in einer Tabelle oder in den Armen, während Sie arbeiten. Versuchen Sie, es in hoch-und Querformat zu verwenden, und halten Sie den Stift zum Schreiben und nur zum zeigen in der linken und der rechten Ecke.

Wenn Sie mit der Verwendung eines Stifts experimentieren, werden Sie Folgendes feststellen:

-   **Kleine Steuerelemente sind schwer zu verwenden.** Die Größe der Steuerelemente wirkt sich stark auf die Fähigkeit aus, effektiv zu interagieren. Steuerelemente, die 10X10 Pixel sind, funktionieren in gewisser Weise für einen Stift, aber größere Steuerelemente sind noch besser zu verwenden. So sind z. b. [Dreh Steuerelemente](ctrl-spin-controls.md) (15x11 Pixel) zu klein für die einfache Verwendung mit einem Stift.
-   **Die häntigkeit ist ein Faktor.** Ihre Hand behandelt manchmal Dinge, die Sie möglicherweise anzeigen oder mit ihnen interagieren möchten. Beispielsweise können Kontextmenüs für Benutzer mit rechtsübergabe nur schwer zu verwenden sein, wenn Sie auf der rechten Seite des Klick Punkts angezeigt werden. es ist also besser, wenn Sie auf der linken Seite angezeigt werden. Mithilfe von Windows können Benutzer ihre häntigkeit in den System Steuerungselementen der Tablet PC-Einstellungen angeben.
-   **Die Aufgaben Lokalität hilft.** Während Sie den Mauszeiger über einen 14-Zoll-Bildschirm mit einer 3-Zoll-Mausbewegung bewegen können, erfordert die Verwendung eines Stifts, dass Sie den gesamten 14 Zoll bewegen. Das wiederholte Verschieben zwischen weit entfernten Zielen kann mühsam sein. es ist daher viel besser, Aufgaben Interaktionen innerhalb des Bereichs einer Ruhe Hand beizubehalten, wenn dies möglich ist. Kontextmenüs sind praktisch, da Sie keine Handbewegung erfordern.
-   **Die Text Eingabe und-Auswahl sind schwierig.** Lange Texteingaben sind besonders schwierig, wenn Sie einen Stift verwenden, sodass die automatische Vervollständigung und akzeptable Standard Textwerte die Aufgaben wirklich vereinfachen können. Die Text Auswahl kann auch recht schwierig sein, sodass Aufgaben einfacher sind, wenn Sie keine exakte Cursor Platzierung benötigen.
-   **Kleine Ziele, die sich in der Nähe des Edge der Anzeige befinden, können sehr schwer tippen.** Einige Anzeige-bezels stehen aus, und einige Touchscreen-Technologien sind an den Rändern weniger sensibel, was die Verwendung von Steuerelementen in der Nähe des Edge erschwert. Die Schaltflächen Minimieren, maximieren, wiederherstellen und schließen auf der Titelleiste können z. b. schwieriger zu verwenden sein, wenn ein Fenster maximiert ist.

### <a name="control-location"></a>Steuerungs Position

Die tasklokalität verringert mühsame, sich wiederholende Kreuz Bildschirm Bewegungen. Um die Handbewegungen zu minimieren, suchen Sie die Steuerelemente in der Nähe der Stelle, an der Sie wahrscheinlich verwendet werden.

**Falsch:**

![Screenshot der Farbpalette, die von den Tools getrennt ist ](images/inter-pen-image3.png)

In diesem Beispiel aus Windows XP ist die Farbpalette zu weit von der Stelle her, an der Sie häufig verwendet wird.

Beachten Sie, dass die aktuelle Position des Benutzers die nächstgelegene ist, die ein Ziel sein kann, sodass es trivial ist. Daher profitieren Kontextmenüs von der vollständigen Verwendung von [FTTS](inter-mouse.md), ebenso wie die von Microsoft Office verwendeten Mini Symbolleisten.

![Screenshot der Zeiger in der Nähe von Menüs ](images/inter-pen-image4.png)

Die aktuelle Zeigerposition ist immer die einfachste Möglichkeit zum Abrufen.

Kleine Ziele in der Nähe des Anzeige Rands können schwer zu erreichen sein. vermeiden Sie daher das Platzieren kleiner Steuerelemente in der Nähe der Fensterkanten Um sicherzustellen, dass Steuerelemente problemlos als Ziel festzulegen sind, wenn ein Fenster maximiert ist, legen Sie entweder mindestens 23x23 Pixel (13 x 13 DLUs) fest, oder platzieren Sie Sie von der Fensterkante.

### <a name="pen-interactions"></a>Stift Interaktionen

**System Gesten**

System Gesten werden von Windows definiert und behandelt. Folglich haben alle Windows-Programme Zugriff darauf. Diese Gesten verfügen über entsprechende Maus-, Tastatur-und Anwendungs Befehls Meldungen:



| System-Geste                                                           | Äquivalente Nachricht mit synthetischen Größen                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Hover (wenn unterstützt)<br/>                          | Mauszeiger<br/>                        |
| Tippen Sie (nach oben und nach oben)<br/>                               | Maus mit der linken Maustaste<br/>                   |
| Doppel tippen (zweimal nach unten oder nach oben)<br/>                  | Maus Doppel mit der linken Maustaste<br/>            |
| Gedrückt halten (nach unten, anhalten, nach oben)<br/>                | Mit der rechten Maustaste klicken<br/>                  |
| Ziehen Sie (nach unten, verschieben, nach oben).<br/>                           | Mouseleft-Drag<br/>                    |
| Drücken, halten und ziehen (nach unten, anhalten, verschieben, nach oben)<br/>   | Mouseright-Drag<br/>                   |
| Select (nach unten, über auswählbare Objekte nach oben)<br/> | Maus auswählen<br/>                       |



 

**Entwickler:** Weitere Informationen finden Sie unter [systemgesten-Enumeration](/previous-versions/ms552724(v=vs.100)).

**Schnelle Stift Bewegungen**

Flicks sind einfache Gesten, die ungefähr gleichwertig mit Tastenkombinationen sind. Navigations schnelle Stift Bewegungen umfassen "Drag up", "Drag", "zurück" und "Vorwärts". Das Bearbeiten von schnelle Stift Bewegungen umfasst kopieren, einfügen, rückgängig und löschen. Um Flicks verwenden zu können, muss das Programm nur auf die zugehörigen Tastatureingaben-Befehle reagieren.

![Diagramm, das Flick Gesten und deren Standard Zuweisungen in Windows 7 anzeigt.](images/inter-pen-image5.png)

Die acht Flick Gesten und deren Standard Zuweisungen in Windows 7. Die Navigations schnelle Stift Bewegungen wurden geändert, sodass Sie dem Schwenken entsprechen (wobei das Objekt mit der Bewegung bewegt wird), anstatt einen Bildlauf durchführen zu müssen (wobei das Objekt in umgekehrter Richtung der Bewegung bewegt wird).

![Abbildung von Flick Gesten, wie z. b. die Verschiebungs Bewegung ](images/inter-pen-image6.png)

Die acht Flick Gesten und deren Standard Zuweisungen in Windows Vista.

Die navigationflicks haben eine natürliche Zuordnung, sodass Sie leicht zu erlernen und zu merken sind. Bei den Bearbeitungs schnelle Stift Bewegungen handelt es sich um Diagonalen, die mehr Genauigkeit erfordern und deren Zuordnungen nicht so natürlich sind (zum Löschen zum Papierkorb bewegen, in den rückwärts Pfeilrichtung zum Rückgängigmachen umschalten), sodass diese standardmäßig nicht aktiviert sind. Alle Flick Aktionen können mithilfe des System Steuerungs Elements Stift und Eingabegeräte angepasst werden.



| Umzu                                     | Äquivalente Nachricht mit synthetischen Größen                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Links nach links<br/>                | Vorwärts Befehl (zurück-Befehl für Windows Vista)<br/> |
| Nach rechts<br/>               | Befehl "zurück" (vorwärts Befehl für Windows Vista)<br/> |
| Aufflicke<br/>                  | Tastatur Scrollen nach unten<br/>                             |
| Nach unten<br/>                | Tastatur Scrollen nach oben<br/>                               |
| Linksbündig linksbündig<br/>    | Tastatur löschen<br/>                                  |
| Diagonal nach unten links<br/>  | Tastatur rückgängig machen<br/>                                    |
| Rechts diagonal aufflicke<br/>   | Tastatur Kopie<br/>                                    |
| Diagonal nach unten rechts Diagonal<br/> | Tastatur einfügen<br/>                                   |



 

**Anwendungs Gesten**

Anwendungen können auch andere Gesten definieren und behandeln. Die Gestenerkennung von Microsoft kann über [40 Gesten](../tablet/application-gestures-and-semantic-behavior.md)erkennen. Um Anwendungs Gesten zu verwenden, muss das Programm die Gesten definieren, die es erkennt, und dann die resultierenden Ereignisse behandeln.

**Reaktionsfähigkeit und Konsistenz**

**Die Reaktionsfähigkeit ist für das Erstellen von Stift-Erlebnissen, die sich direkt und ansprechend Verhalten** Um sich direkt vertraut zu machen, müssen Gesten sofort wirksam werden, und die Kontaktpunkte eines Objekts müssen während der Bewegung reibungslos im Stift bleiben. Jede Verzögerung, eine unkorrekte Antwort, ein Verlust von Kontakten oder ungenaue Ergebnisse zerstört die Wahrnehmung der direkten Bearbeitung und der Qualität.

**Die Konsistenz ist für das Erstellen von Stift-Erlebnissen, die sich auf natürliche und intuitive Natur** Nachdem Benutzer eine Standard Geste gelernt haben, erwarten Sie, dass diese Geste für alle anwendbaren Programme dieselbe Wirkung hat. Um Verwirrung und Frustration zu vermeiden, weisen Sie Standard Gesten niemals nicht dem Standard entsprechende Bedeutungen zu. Verwenden Sie stattdessen benutzerdefinierte Gesten für Interaktionen, die für Ihr Programm eindeutig sind.

**Bearbeitung von frei Hand Eingaben und Text**

Die Bearbeitung von frei Hand Eingaben und Text gehört zu den anspruchsvollsten Interaktionen bei der Verwendung eines Stifts. Durch die Verwendung von eingeschränkten Steuerelementen, der entsprechenden Standardwerte und der automatischen Vervollständigung entfällt oder verringert sich die Notwendigkeit, Text einzugeben. Wenn das Programm jedoch Text oder frei Hand Eingaben umfasst, **können Sie Benutzer produktiver machen, indem Sie die Eingabe Benutzeroberfläche bei Verwendung eines Stifts automatisch auf 150 Prozent vergrößern.**

Ein e-Mail-Programm könnte z. b. die Benutzeroberfläche in normaler Größe anzeigen, zoomt aber die Eingabe-UI auf 150 Prozent, um Meldungen zu verfassen

![Screenshot der Outlook-Nachricht in der großen Schriftart ](images/inter-pen-image7.png)

In diesem Beispiel wird die Eingabe Benutzeroberfläche auf 150 Prozent vergrößert.

**Wenn Sie nur vier Dinge tun...**

1.  1. Sorgen Sie dafür, dass Ihre Windows-Programme eine gute Stift Darstellung haben! Benutzer sollten in der Lage sein, die wichtigsten Aufgaben Ihres Programms effizient mithilfe eines Stifts auszuführen (zumindest bei den Aufgaben, die nicht viel typisieren oder eine detaillierte Pixel Bearbeitung erfordern).
2.  2. Fügen Sie Unterstützung für das direkte schreiben, zeichnen und Hinzufügen von Kommentaren in den relevantesten Szenarios in Erwägung.
3.  3. Um eine direkte und ansprechende Benutzerfunktion zu schaffen, werden Gesten sofort wirksam, und die Kontaktpunkte im Stift des Benutzers werden während der Bewegung reibungslos gehalten, und die Aktion wird direkt auf die Bewegung des Benutzers angewendet.
4.  4. Um eine natürliche und intuitive Darstellung zu schaffen, unterstützen Sie geeignete Standard Gesten und weisen diese Ihrer Standard Bedeutungen zu. Verwenden Sie benutzerdefinierte Gesten für Interaktionen, die für Ihr Programm eindeutig sind.

## <a name="guidelines"></a>Richtlinien

### <a name="control-usage"></a>Verwendung steuern

-   **Verwenden Sie allgemeine Steuerelemente.** Die meisten gängigen Steuerelemente sind darauf ausgelegt, eine gute Stift Darstellung zu unterstützen.
-   **Eingeschränkte Steuerelemente bevorzugen.** Verwenden Sie möglichst eingeschränkte Steuerelemente wie Listen und Schieberegler anstelle von nicht eingeschränkten Steuerelementen wie Textfeldern, um den Bedarf an Texteingaben zu verringern.
-   **Geben Sie entsprechende Standardwerte an.** Wählen Sie das sicherste (um Datenverlust oder System Zugriff zu vermeiden) und die sicherste Option standardmäßig aus. Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequeme Option aus, wodurch unnötige Interaktionen vermieden werden.
-   **Stellen Sie die automatische Vervollständigung von Text bereit.** Stellen Sie eine Liste der wahrscheinlichsten oder vor kurzem eingegebenen Werte bereit, um die Texteingabe erheblich zu vereinfachen.
-   **Stellen Sie für wichtige Aufgaben, die Mehrfachauswahl verwenden, eine Option zum Verwenden einer Kontrollkästchen-Liste bereit, wenn normalerweise eine standardmäßige Mehrfachauswahl Liste verwendet wird.**
-   **Beachten Sie Systemmetriken.** Verwenden Sie Systemmetriken für alle Größen nicht Hardware-Größen. Falls erforderlich, können Benutzer die Systemmetriken oder dpi-Werte ändern, um Ihre Anforderungen zu erfüllen. Behandeln Sie dies jedoch als letztes Mittel, da Benutzer normalerweise nicht die Systemeinstellungen anpassen müssen, damit die Benutzeroberfläche verwendbar ist.

![Screenshot von Menüs mit normaler und großer Größe ](images/inter-pen-image8.png)

In diesem Beispiel wurde die Systemmetrik für die Menü Höhe geändert.

### <a name="control-sizing-layout-and-spacing"></a>Steuern der Größe, des Layouts und des Abstands

-   **Verwenden Sie für allgemeine Steuerelemente die empfohlenen Steuerelement Größen.** Diese sind für eine gute Stift Darstellung groß genug, außer bei Dreh Steuerelementen (die nicht mit einem Stift verwendbar sind, aber redundant sind).
-   **Wählen Sie ein Layout aus, in dem die Steuerelemente nah an der Stelle platziert werden, an der Sie wahrscheinlich verwendet werden.** Behalten Sie die Aufgaben Interaktionen innerhalb eines kleinen Bereichs bei, wenn möglich. Vermeiden Sie längere Entfernungs Bewegungen, insbesondere bei häufigen Aufgaben und bei Drags.
-   **Verwenden Sie den empfohlenen Abstand.** Der empfohlene Abstand ist Stift freundlich.
-   **Interaktive Steuerelemente sollten entweder berühren oder vorzugsweise mindestens 5 Pixel (3 DLUs) enthalten.** Dadurch wird Verwirrung verhindert, wenn Benutzer außerhalb des beabsichtigten Ziels tippen.
-   Fügen Sie in der Gruppe von Steuerelementen, wie z. b. Befehls Verknüpfungen, Kontrollkästchen, Options Felder und zwischen den Gruppen, **mehr als den empfohlenen vertikalen Abstand hinzu** . Dies erleichtert die Unterscheidung.

### <a name="interaction"></a>Interaktion

-   **Aktivieren Sie für Programme, die eine Handschrift akzeptieren sollen, das Standard Inking.** Mit dem Standard-Freihand können Benutzer frei Hand Eingaben eingeben, indem Sie einfach mit dem Schreiben beginnen, ohne auf einen Befehl tippen oder etwas Besonderes tun zu müssen. Dadurch wird die natürlichste Darstellung mit einem Stift ermöglicht. Behandeln Sie für Programme, die nicht zur Annahme von Handschrift entworfen wurden, Stift Eingaben in Textfeldern als Auswahl.
-   Hiermit wird **Benutzern das Vergrößern der Inhalts Benutzeroberfläche ermöglicht** , wenn das Programm Aufgaben enthält, die Text bearbeiten müssen. Bei Verwendung eines Stifts empfiehlt es sich, automatisch auf 150 Prozent zu zoomen.
-   **Da Gesten gespeichert werden, weisen Sie Ihnen Bedeutungen zu, die zwischen verschiedenen Programmen konsistent sind.** Setzen Sie Gesten mit fester Semantik nicht mit unterschiedlichen Bedeutungen. Verwenden Sie stattdessen eine geeignete Programm spezifische Geste.

### <a name="handedness"></a>Händigkeit

-   **Wenn ein Fenster kontextbezogen ist, sollten Sie es immer in der Nähe des Objekts anzeigen, von dem es gestartet wurde.** Platzieren Sie die Methode so, dass das Quell Objekt nicht durch das Fenster abgedeckt wird.
    -   Wenn Sie mit der Maus angezeigt werden, können Sie, wenn möglich, den Kontext des Kontext Fensters nach unten und nach rechts platzieren.

        ![Abbildung des Kontext Fensters, das rechts vom Objekt platziert wird ](images/inter-pen-image9.png)

        Kontext Fenster in der Nähe des Objekts anzeigen, von dem es gestartet wurde.

    -   Wenn Sie mithilfe eines Stifts angezeigt werden, platzieren Sie, wenn möglich, das Kontext Fenster, sodass es nicht von der Hand des Benutzers abgedeckt wird. Zeigen Sie für Benutzer mit rechten Hand auf der linken Seite an. Andernfalls rechts anzeigen.

        ![Abbildung des Kontext Fensters, das sich links vom Objekt befindet ](images/inter-pen-image10.png)

        Wenn Sie einen Stift verwenden, zeigen Sie auch Kontext Fenster an, sodass Sie nicht von der Hand des Benutzers abgedeckt werden.

-   **Entwickler:** Mithilfe der [getMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) -API können Sie zwischen Mausereignissen und Stift Ereignissen unterscheiden. Mithilfe der [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -API mit SPI getmenudropalignment können Sie die Benutzer [häntigkeit](/previous-versions/ms819495(v=msdn.10)) ermitteln \_ .

### <a name="forgiveness"></a>Erl

-   **Stellen Sie einen Befehl rückgängig bereit.** Im Idealfall sollten Sie für alle Befehle rückgängig machen, aber das Programm verfügt möglicherweise über einige Befehle, deren Auswirkung nicht rückgängig gemacht werden kann.
-   **Geben Sie gutes Hover-Feedback.** Geben Sie eindeutig an, wenn sich der Stift über einem klickbaren Ziel befindet. Dieses Feedback ist eine hervorragend Möglichkeit, eine versehentliche Bearbeitung zu verhindern.
-   **Stellen Sie, wenn dies praktikabel ist, gutes Feedback zum Stift, aber führen Sie keine Aktionen aus, bis eine Bewegung oder ein Stift angezeigt wird.** Dies ermöglicht es Benutzern, Fehler zu beheben, bevor Sie Sie vornehmen.
-   **Wenn dies praktikabel ist, können Benutzer problemlos Fehler beheben.** Wenn eine Aktion für den Stift wirksam wird, gestatten Sie Benutzern, Fehler zu korrigieren, indem Sie schieben, während der Stift immer noch nicht ausgeführt wird.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Stift Eingabe:

-   Informationen finden Sie in einem Stift förmigen Stift-Eingabegerät als Stift. Verwenden Sie bei der ersten Erwähnung den Tablettstift.
-   Verweisen Sie auf die Schaltfläche auf der Seite eines Stifts als Stift Schaltfläche und nicht auf die Schaltfläche "Barrel".
-   Lesen Sie generisch auf Tastatur, Maus, Trackball, Stift oder Finger als Eingabegerät.
-   Verwenden Sie beim Dokumentieren von Prozeduren, die für die Verwendung eines Stifts spezifisch sind, Tap (und Doppel tippen) anstelle von Click. Tippen Sie auf Mittel, um den Bildschirm zu drücken und dann vor einer Haltezeit zu warten. Sie kann verwendet werden, um einen Mausklick zu generieren. Verwenden Sie für Interaktionen, die nicht den Stift enthalten, weiterhin Click.


---
title: Maus und Zeiger
description: Die Maus ist das primäre Eingabegerät, das für die Interaktion mit Objekten in Windows verwendet wird.
ms.assetid: 4d99287d-e908-4c8b-b4f6-6e8c91c6c93e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6462c69216ee9acb5149a01a805503cea721bb1c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961081"
---
# <a name="mouse-and-pointers"></a>Maus und Zeiger

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Die Maus ist das primäre Eingabegerät, das für die Interaktion mit Objekten in Windows verwendet wird. Die Maus Funktionalität kann auch andere Zeigegeräte umfassen, z. b. trackballs, Touchpads und Zeiger auf Notebook-Computer, Stifte, die mit der Windows-Tablet-und Touch-Technologie verwendet werden, und auf Computern mit Touchscreens, auch als Finger.

> [!NOTE]
> Richtlinien für [Barrierefreiheit](inter-accessibility.md), [Stift](inter-pen.md)und Finger [Eingabe werden in](inter-touch.md) separaten Artikeln dargestellt.

Wenn Sie die Maus physisch bewegen, wird der Grafik Zeiger (auch als Cursor bezeichnet) auf dem Bildschirm verschoben. Der-Zeiger verfügt über eine Vielzahl von Formen zum Angeben des aktuellen Verhaltens.

![Screenshot mit fünf typischen Maus Zeigern ](images/inter-mouse-image1.png)

*Typische Mauszeiger*

Maus Geräte verfügen häufig über eine primär Schaltfläche (in der Regel die linke Schaltfläche), eine sekundäre Schaltfläche (normalerweise die Rechte) und ein Mausrad zwischen den beiden. Durch Positionieren des Zeigers und klicken auf die primären und sekundären Schaltflächen der Maus können Benutzer Objekte auswählen und Aktionen für diese ausführen. Bei den meisten Interaktionen wird durch Drücken einer Maustaste, während sich der Cursor über einem Ziel befindet, das ausgewählte Ziel angezeigt, und durch das Freigeben der Schaltfläche werden alle dem Ziel zugeordneten Aktionen ausgeführt.

Alle Zeiger, mit Ausnahme des ausgelasteten Zeigers, haben einen einzelnen Pixel-Hotspot, der die exakte Bildschirmposition der Maus definiert. Der Hotspot bestimmt, welches Objekt von Mausaktionen betroffen ist. -Objekte definieren eine heiße Zone, bei der es sich um den Bereich handelt, in dem der Hotspot als über dem Objekt betrachtet wird. In der Regel fällt die Hot-Zone mit den Rahmen eines Objekts an, aber Sie ist möglicherweise größer, um die Absicht des Benutzers zu vereinfachen.

Die Einfügemarke ist der blinkende vertikale Balken, der angezeigt wird, wenn der Benutzer in ein Textfeld oder einen anderen Text-Editor tippt. Die Einfügemarke ist unabhängig vom-Zeiger (Standardmäßig blendet Windows den Zeiger aus, während der Benutzer die Eingabe durchläuft).

![Screenshot von Textfeld mit Cursor ](images/inter-mouse-image2.png)

*Die Einfügemarke*

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="the-mouse-is-intuitive"></a>Die Maus ist intuitiv

Bei der Maus handelt es sich um ein erfolgreiches Eingabegerät, da es für die typische menschliche Hand leicht verwendet werden kann. Die Zeiger basierte Interaktion ist erfolgreich, da Sie intuitiv ist und eine Vielzahl von Erfahrungen ermöglicht.

**Gut entworfene Benutzeroberflächen Objekte (User Interface, UI) haben eine solche Funktion, bei der es sich um visuelle und Verhaltenseigenschaften eines Objekts handelt, die die Verwendung der Anwendung vorschlagen.** Der Zeiger fungiert als Proxy für die Hand und ermöglicht Benutzern die Interaktion mit Bildschirm Objekten, ähnlich wie bei physischen Objekten. Wir haben ein gedrücktes Verständnis der Art und Weise, wie das Personal funktioniert. wenn es also so aussieht, dass es per Push übermittelt werden kann, versuchen wir es per Push. Wenn es so aussieht, als ob es zu sehen ist, versuchen wir, es zu erfassen. Folglich können Benutzer ermitteln, wie Sie Objekte mit starker Aufforstung verwenden, indem Sie Sie betrachten und ausprobieren.

![Screenshot einer Schaltfläche und eines Schiebereglers](images/inter-mouse-image3.png)

*Schaltflächen und Schieberegler haben starke Kosten*

Im Gegensatz dazu ist es schwieriger, Objekte mit schlechten Kosten zu ermitteln. Bei solchen Objekten ist häufig eine Bezeichnung oder eine Anweisung erforderlich, um Sie zu erläutern.

![Screenshot von Linktext und Internet Earth-Symbol](images/inter-mouse-image4.png)

*Linktext und-Symbole haben eine schlechte Kosten*

### <a name="some-aspects-of-mouse-use-are-not-intuitive"></a>Einige Aspekte der Maus Verwendung sind nicht intuitiv.

Wenn Sie **mit der rechten Maustaste klicken, doppelklicken und mit UMSCHALTTASTE oder STRG-schlüsselmodifizierertaste klicken, sind drei Maus Interaktionen** vorhanden, die nicht intuitiv sind, da Sie keine echten Gegenstücke haben. Anders als bei Tastenkombinationen und Zugriffstasten werden diese Maus Interaktionen in der Regel nicht in der Benutzeroberfläche dokumentiert. Dies deutet darauf hin, dass für die Durchführung grundlegender Aufgaben, insbesondere für Anfänger durch Anfänger, mit der rechten Maustaste, Doppelklick und Tastatur modifiziererer nicht erforderlich sein sollten. Außerdem wird vorgeschlagen, dass diese erweiterten Interaktionen ein konsistentes, vorhersagbares Verhalten aufweisen müssen, um effektiv verwendet zu werden.

### <a name="single-click-or-double-click"></a>Klicken oder Doppelklicken Sie auf?

Doppelklicken Sie auf dem Windows-Desktop so ausführlich, dass es nicht wie eine erweiterte Interaktion erscheint. Wenn Sie z. b. Ordner, Programme oder Dokumente im Bereich "Datei" von Windows-Explorer öffnen, werden Sie durch Doppelklicken. Wenn Sie eine Verknüpfung auf dem Windows-Desktop öffnen, wird auch ein Doppelklick verwendet. Im Gegensatz dazu erfordert das Öffnen von Ordnern oder Programmen im Startmenü nur einen Mausklick.

Auswählbare Objekte verwenden einen einfachen Mausklick, um die Auswahl auszuführen, sodass Sie einen Doppelklick zum öffnen benötigen, während nicht auswählbare Objekte nur einen Mausklick öffnen müssen. Dieser Unterschied wird von vielen Benutzern nicht verstanden (durch Klicken auf das Programmsymbol klicken Sie auf ein Programmsymbol, richtig?) und das Ergebnis ist, dass einige Benutzer einfach auf Symbole klicken, bis Sie die gewünschten Elemente erhalten.

### <a name="direct-manipulation"></a>Direkte Manipulation

Das direkte interagieren mit Objekten wird als direkte Bearbeitung bezeichnet. Das zeigen, klicken, auswählen, verschieben, Ändern der Größe, aufteilen, scrollen, Schwenken und Zoomen sind allgemeine direkte Manipulationen. Im Gegensatz dazu könnte die Interaktion mit einem Objekt über das Eigenschaften Fenster oder ein anderes Dialogfeld als indirekte Bearbeitung beschrieben werden.

**Wenn eine direkte Bearbeitung vorliegt, kann es jedoch zu einer versehentlichen Bearbeitung und somit zu einer Notwendigkeit von Vergebung kommen.** Mit "Vergebung" können Sie eine nicht gewünschte Aktion problemlos umkehren oder korrigieren. Sie können direkte Manipulationen durch Bereitstellen von Rückgängigmachen durchführen und gutes visuelles Feedback geben und Benutzern das einfache Beheben von Fehlern ermöglichen. Die zugeordnete Vergebung verhindert, dass unerwünschte Aktionen zuerst durchgeführt werden können. dazu können Sie eingeschränkte Steuerelemente und Bestätigungen für riskante Aktionen oder Befehle verwenden, die unbeabsichtigte Folgen haben.

### <a name="standard-mouse-button-interactions"></a>Standard mäßige Maustasten Interaktionen

Die Standard Maus Interaktionen hängen von einer Vielzahl von Faktoren ab, einschließlich der angeklickten Maustasten, der Anzahl der angeklickten Versuche, der Position während der Klicks und der Angabe, ob Tastatur modifiziererer gedrückt wurden. Im folgenden finden Sie eine Zusammenfassung der Auswirkungen dieser Faktoren auf die Interaktion:

- Bei den meisten Objekten wird bei einem linken Doppelklick nur ein einziger Mausklick durchführt, und der Standardbefehl wird durchführt. Der Standardbefehl wird im Kontextmenü identifiziert.
- Bei einigen Typen von auswählbaren Objekten erweitert jedes Klick die Auswirkung des Click. Wenn Sie z. b. in einem Textfeld mit einem Klick auf ein Textfeld klicken, wird der Eingabe Speicherort festgelegt, ein Doppelklick auf ein Wort ausgewählt und ein dreimal Klick auf einen Satz oder Absatz
- Klicken Sie mit der rechten Maustaste auf zeigt das Kontextmenü eines Objekts an.
- Halten Sie die Maus noch immer, während Sie auf den Mauszeiger zeigen.
- Wenn Sie die Maus gedrückt halten, während Sie die Maustasten drücken, bedeutet dies, dass Sie auf die Auswahl klicken Wenn Sie die Maus bewegen, werden die Auswahl von verschieben, Ändern der Größe, aufteilen, ziehen und mehrerer Objekte angezeigt.
- Mit der UMSCHALTTASTE wird die Auswahl zusammenhängend erweitert.
- Mit der STRG-Taste wird die Auswahl erweitert, indem Sie den Auswahl Zustand des Elements, auf das geklickt wird, umschalten, ohne die Auswahl anderer Objekte zu beeinträchtigen.

### <a name="simple-mouse-interactions"></a>Einfache Maus Interaktionen

In der folgenden Tabelle werden häufige Maus Interaktionen und-Effekte beschrieben.

| Einfache Aktion | Interaktion | Typische Auswirkung |
|:---|:---|:---|
| Hinwies<br/>          | Positionieren Sie den Zeiger auf ein bestimmtes Objekt, ohne auf eine beliebige Maustaste zu klicken.<br/>                                                                                                                                                                                                                                      | Ziel zeigt den Hover-Zustand und alle dynamischen Kosten an.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| End<br/>          | Positionieren Sie den Zeiger auf ein bestimmtes Objekt, ohne auf eine beliebige Maustaste zu klicken und mindestens eine Sekunde zu verschieben.<br/>                                                                                                                                                                                             | Ziel zeigt die QuickInfo, den Infotipp oder eine entsprechende an.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Einen<br/>          | Positionieren Sie den Zeiger auf ein bestimmtes, nicht auswählbares Objekt, und lassen Sie die Maustaste los, ohne zu verschieben. Wenn Sie auf die Maustaste klicken, wird das Klicken auf die Maustaste losgelassen, damit Benutzer den Klick abbrechen können, indem Sie den Mauszeiger auf das Ziel bewegen. Aus diesem Grund gibt die Maus drücken nur das ausgewählte Ziel an.<br/> | Aktivieren Sie für einzelne Klicks mit der Schaltfläche primär das Objekt. Aktivieren Sie für Doppelklicks mit der Schaltfläche primär das Objekt, und führen Sie den Standardbefehl aus. Zeigen Sie für die Schaltfläche Sekundär das Kontextmenü des-Objekts an.<br/>                                                                                                                                                                                         |
| Wählen Sie Folgendes aus:<br/>         | Positionieren Sie den Zeiger auf ein bestimmtes, auswählbares Objekt, und lassen Sie die Maustaste los.<br/>                                                                                                                                                                                                                        | Wählen Sie für einzelne Klicks mit der Schaltfläche primär das Objekt aus. Wenn die Benutzer die Maus ziehen, wählen Sie einen zusammenhängenden Bereich von Objekten aus. Wählen Sie für Doppelklicks mit der Schaltfläche primär das Objekt aus, und führen Sie den Standardbefehl aus.<br/> Bei Text wird mit der rechten primären Schaltfläche die Einfügemarke festgelegt, die zweite auf der Einfügemarke Word und der dritte Klick den Satz bzw. Absatz.<br/> |
| Pressing<br/>          | Positionieren Sie den Zeiger auf ein bestimmtes Objekt, und drücken Sie eine Maustaste, ohne Sie zu veröffentlichen.<br/>                                                                                                                                                                                                                              | Aktivieren Sie für Funktionen zur automatischen Wiederholung (z. b. Drücken eines Bild Lauf Pfeils zum fortlaufenden scrollen) wiederholt. Gibt andernfalls den Anfang einer Verschiebung, die Größe der Größe, die Teilung oder den Zieh Vorgang an, es sei denn, es folgt ein Release ohne verschieben.<br/>                                                                                                                                                                                               |
| Wird durchlaufen<br/>          | Bewegen Sie das Mausrad.<br/>                                                                                                                                                                                                                                                                                                  | Fenster führt einen vertikalen Bildlauf in Richtung der Mausrad Bewegung durch.<br/>                                                                                                                                                                                                                                                                                                                                                      |

### <a name="pointer-shapes"></a>Zeiger Formen

In der folgenden Tabelle werden allgemeine Zeiger Formen und-Verwendungen beschrieben.

| Form | Name | Verwendung |
|:---|:---|:---|
| ![Screenshot des Zeigers mit der Form "Pfeil" ](images/inter-mouse-image5.png)<br/>           | Normale Auswahl<br/>    | Wird für die meisten-Objekte verwendet.<br/>                                             |
| ![Bildschirm Abbildung von Hand mit Index Zeige Zeige ](images/inter-mouse-image6.png)<br/>    | Link auswählen<br/>      | Wird für Text-und Grafik Links verwendet, die aufgrund ihrer schwachen Kosten für Sie verwendet werden.<br/> |
| ![Screenshot des Zeigers mit der Form "i-Beam" ](images/inter-mouse-image7.png)<br/>          | Text auswählen<br/>      | Wird für Text verwendet, um einen Speicherort zwischen Zeichen anzugeben.<br/>           |
| ![Screenshot eines Zeigers mit einer großen Pluszeichen-Form ](images/inter-mouse-image8.png)<br/> | Genauigkeits Auswahl<br/> | Wird für Grafiken und andere zweidimensionale Interaktionen verwendet.<br/>            |

### <a name="compound-mouse-interactions"></a>Zusammengesetzte Maus Interaktionen

In der folgenden Tabelle werden häufige Maus Interaktionen beschrieben.

| Verbund Aktion | Interaktion | Typische Auswirkung | Zeiger |
|:---|:---|:---|:---|
| Verschieben<br/>                | Wenn verschieben ein (durch Angabe eines Befehls eingegebener) Modus ist, geben Sie den Modus ein, positionieren Sie den Mauszeiger über einem verschiebbaren Objekt, klicken Sie auf die Schaltfläche, und bewegen Sie die Maus, in diesem Fall ändert sich die Form des Zeigers, um den Modus anzugeben.<br/> Positionieren Sie andernfalls den Zeiger über den Grabber eines verschiebbaren Objekts, drücken Sie die Schaltfläche, und bewegen Sie die Maus. in diesem Fall muss der Zeiger die Form nicht ändern.<br/> | Objekt Verschiebung in Richtung der Zeiger Bewegung.<br/>            | Verschieben<br/> ![Screenshot eines Zeigers mit vier Pfeilen ](images/inter-mouse-image9.png)<br/> wird verwendet, um ein Fenster in beliebiger Richtung zu verschieben.<br/> Pfanne<br/> ![Screenshot des Zeigers mit der Form "Hand" ](images/inter-mouse-image10.png)<br/> Wird verwendet, um ein Objekt innerhalb eines Fensters in beliebiger Richtung zu verschieben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Größenänderung<br/>              | Positionieren Sie den Mauszeiger über einem in der Größe geänderten Rahmen oder mit der Größenanpassung, drücken Sie eine Maustaste, und bewegen Sie die Maus.<br/>                                                                                                                                                                                                                                                                                 | Objektgröße ändert sich in Richtung der Zeiger Bewegung.<br/>          | vertikale und horizontale Größenänderung<br/> ![Screenshot, der auf-ab-Zeiger zeigt.](images/inter-mouse-image11.png)![Screenshot von nach-unten-und rechts zeigenden Zeigern ](images/inter-mouse-image12.png)<br/> wird verwendet, um die Größe einer einzelnen Dimension zu ändern.<br/> Diagonale Größe ändern<br/> ![bb545459. mouse13 (en-US, MSDN. 10). png](images/inter-mouse-image13.png)![Bildschirm Abbildung von diagonalen Zeigern mit Pfeil Tipps](images/inter-mouse-image14.png)<br/> wird zur gleichzeitigen Größenänderung von zwei Dimensionen verwendet.<br/> Größenänderung von Zeilen und Spalten<br/> ![bb545459. mouse15 (en-US, MSDN. 10). png](images/inter-mouse-image15.png)![Screenshot von Pfeil Zeigern mit Querbalken ](images/inter-mouse-image16.png)<br/> Wird verwendet, um die Größe einer Zeile oder Spalte in einem Raster zu ändern.<br/> |
| Teilen<br/>             | Positionieren Sie den Zeiger über einen Splitter, drücken Sie eine Maustaste, und bewegen Sie die Maus, und lassen Sie die Maustaste los.<br/>                                                                                                                                                                                                                                                                                                          | der Rahmen für den Rahmen des geteilten Bereichs wird in Richtung der Zeiger Bewegung verschoben<br/> | Fenster Aufteilungen<br/> ![bb545459. mouse17 (en-US, MSDN. 10). png](images/inter-mouse-image17.png)![Screenshot von Pfeil Zeigern mit doppelter quer Leiste ](images/inter-mouse-image18.png)<br/> Wird verwendet, um die Größe eines geteilten Bereichs vertikal oder horizontal zu ändern.<br/> |
| Drag & Drop<br/> | Positionieren Sie den Zeiger auf ein gültiges Objekt zum ziehen, drücken Sie eine Maustaste, und bewegen Sie die Maus zu einem Ablage Ziel, und lassen Sie die Maustaste los.<br/> | das Objekt wird verschoben oder in das Ablage Ziel kopiert.<br/>             | normale Auswahl<br/> ![Screenshot von Foto, Standard Zeiger und Infotipp ](images/inter-mouse-image19.png)<br/> wird über gültige Zieh Ziele verwendet. kann auch über einen InfoTipp verfügen, der bestimmte Auswirkungen angibt.<br/> nicht verfügbar<br/> ![Screenshot eines kleinen blockierten/Offline-Symbols ](images/inter-mouse-image20.png)<br/> Wird verwendet, um anzugeben, dass eine Oberfläche kein gültiges Ablage Ziel ist.<br/> |

### <a name="activity-indicators"></a>Aktivitätsindikatoren

In der folgenden Tabelle sind Zeiger aufgeführt, die Benutzern angezeigt werden, wenn Sie eine Aktion ausführen, die mehr als ein paar Sekunden in Anspruch nimmt.

| Form | Name | Verwendung |
|:---|:---|:---|
| ![Screenshot, der einen ringförmigen "ausgelasteten" Zeiger zeigt.](images/inter-mouse-image21.png)<br/>          | Ausgelasteter Zeiger<br/>                  | Wird verwendet, um auf die Reaktionszeit eines Fensters zu warten.<br/>                                  |
| ![Screenshot des ringförmigen Zeigers und Pfeils](images/inter-mouse-image22.png)<br/> | Arbeiten im Hintergrund Zeiger<br/> | Wird verwendet, um zu zeigen, zu klicken, zu drücken oder auszuwählen, während eine Aufgabe im Hintergrund abgeschlossen ist.<br/> |

### <a name="hand-pointers"></a>Hand Zeiger

Text-und Grafik Links verwenden einen Hand-oder "Link Select"-Zeiger (eine Hand mit dem Index Zeige Zeiger) ![Bildschirm Abbildung von Hand mit Index Zeige Zeige ](images/inter-mouse-image6.png)) aufgrund ihrer schwachen Kosten. Links haben möglicherweise andere visuelle Hinweise, um anzugeben, dass es sich um Verknüpfungen handelt (z. b. Unterstriche und Sonderplatzierung). die Anzeige des Hand Zeigers bei Hover ist der definitive Hinweis auf einen Link.

**Um Verwechslungen zu vermeiden, ist es zwingend erforderlich, den Hand Zeiger nicht für andere Zwecke zu verwenden.** Beispielsweise verfügen Befehls Schaltflächen bereits über eine starke Aufforstung, sodass Sie keinen Hand Zeiger benötigen. Der Hand Zeiger muss "dieses Ziel ist ein Link" und nichts anderes bedeuten.

### <a name="custom-pointers"></a>Benutzerdefinierte Zeiger

Windows unterstützt die Erstellung von benutzerdefinierten Zeigern. Weitere Informationen finden Sie unter [Festlegen des Cursor Bilds](../learnwin32/setting-the-cursor-image.md) und [Benutzereingabe: erweitertes Beispiel](../learnwin32/user-input--extended-example.md).

Viele Anwendungen bieten eine Palette von Steuerelementen mit benutzerdefinierten Zeigern, um Anwendungsfunktionen zu unterstützen.

![Screenshot der Palette mit einem Spray-can-Zeiger ](images/inter-mouse-image23.png)

*Microsoft Paint enthält eine Palette verschiedener Funktionen, die jeweils einen eindeutigen Zeiger enthalten.*

### <a name="fitts-law"></a>Gesetze

Das Gesetz "" ist ein bekanntes Prinzip in grafischer Benutzeroberflächen-Entwurfs Ergonomie, das im Wesentlichen Folgendes bedeutet:

- Je länger ein Ziel ist, desto länger dauert es, es mit der Maus zu erhalten.
- Der kleinere Zielwert ist, desto länger dauert es, bis es mit der Maus abgerufen wird.

Daher sind große Ziele gut. Stellen Sie sicher, dass der gesamte Zielbereich klickbar ist.

| Falsch | Richtig (das gesamte Ziel ist klickbar) |
|:---|:---|
| ![Screenshot des Symbols, auf das nur die Beschriftung geklickt werden kann ](images/inter-mouse-image24.png) | ![Screenshot eines klickbaren Symbols und einer klickbaren Bezeichnung ](images/inter-mouse-image25.png) |

Sie können die Größe eines Ziels dynamisch ändern, wenn Sie darauf zeigen, dass es einfacher zu finden ist.

![Screenshot der Zeichen Zuordnung mit einer erweiterten Zahl ](images/inter-mouse-image26.png)

*Ein Ziel wird größer, wenn der Benutzer darauf zeigt, dass es einfacher zu finden ist.*

Und Close-Ziele sind ebenfalls gut. Suchen Sie nach klickbaren Elementen in der Nähe, wo Sie wahrscheinlich verwendet werden. In der folgenden Abbildung ist die Farbpalette zu weit von der Tool Auswahl entfernt.

![Screenshot der Farbpalette, die von den Tools getrennt ist ](images/inter-mouse-image27.png)

*Die Farbpalette ist zu weit von der Stelle, an der Sie wahrscheinlich verwendet wird*

Beachten Sie, dass die aktuelle Zeigerposition des Benutzers so nah ist, wie ein Ziel sein kann, sodass der Abruf trivial ist. Daher profitieren Kontextmenüs von der vollständigen Verwendung von FTTS, ebenso wie die Mini Symbolleisten, die von Microsoft Office verwendet werden.

![Screenshot der Zeiger in der Nähe der Dropdown Liste ](images/inter-mouse-image28.png)

*Die aktuelle Zeigerposition ist immer am einfachsten zu erhalten.*

Beachten Sie auch alternative Eingabegeräte beim Bestimmen von Objektgrößen. Beispielsweise beträgt die minimale Zielgröße, die für die Fingereingabe empfohlen wird, 23x23 Pixel (13 x 13 DLUs).

### <a name="environments-without-a-mouse"></a>Umgebungen ohne Maus

Nicht alle Windows-Umgebungen haben eine Maus. Beispielsweise haben Kioske selten eine Maus und verfügen in der Regel über einen Touchscreen. Dies bedeutet, dass Benutzer einfache Interaktionen ausführen können, wie z. b. das Klicken mit der linken Maustaste und möglicherweise Drag & Drop. Sie können jedoch nicht darauf zeigen, mit der rechten Maustaste klicken oder doppelklicken. Diese Situation ist einfach zu entwerfen, da diese Einschränkungen in der Regel im Voraus bekannt sind.

Die Verwendung einer Maus erfordert eine fein motorische Qualifikation, daher können nicht alle Benutzer eine Maus verwenden. Um die Verfügbarkeit Ihrer Software für die breiteste Zielgruppe zu erreichen, müssen Sie sicherstellen, dass alle Interaktionen, bei denen es sich nicht um die notwendigen Funktionen handelt, die Tastatur verwenden können

Weitere Informationen und Richtlinien finden Sie unter [Barrierefreiheit](inter-accessibility.md).

**Wenn Sie nur vier Dinge tun...**

1.  Mit den Standard Effekten können Sie das Verhalten der Maus Interaktionen mit den Standard Effekten konsistent gestalten.
2.  Erweiterte Aufgaben, die für fortgeschrittene Benutzer entwickelt wurden, werden durch erweiterte Maus Interaktionen (Benutzer mit Rechtsklick, mehrere Klicks oder modifiziererschlüssel) beschränkt.
3.  Ordnen Sie erweiterte, vorhersagbare Verhalten von Maus Interaktionen zu, damit Sie effektiv verwendet werden können.
4.  Stellen Sie sicher, dass Ihr Programm die Möglichkeit bietet, unerwünschte Aktionen (insbesondere bei destruktiven Befehlen) umzukehren oder zu korrigieren. Versehentliche Aktionen sind wahrscheinlicher, wenn direkte Manipulationen verwendet werden.

## <a name="guidelines"></a>Richtlinien

### <a name="click-affordance"></a>Klicken Sie auf die Kosten

- **Benutzer müssen niemals auf ein Objekt klicken, um festzustellen, ob es klickbar ist.** Benutzer müssen in der Lage sein, die klickbarkeit allein bei der visuellen Prüfung zu bestimmen.
  - Die primäre Benutzeroberfläche (z. b. "Commit"-Schaltflächen) muss über ein statisches Click- Benutzer müssen nicht darauf zeigen, um die primäre Benutzeroberfläche zu ermitteln.
  - Bei der sekundären Benutzeroberfläche (z. b. sekundäre Befehle oder progressives Offenlegung) können Ihre Klick Möglichkeiten angezeigt werden.
  - [Text Verknüpfungen](ctrl-links.md) sollten den Linktext statisch vorschlagen und dann mit dem Mauszeiger auf den Mauszeiger (Unterstreichung oder andere Präsentations Änderung, mit [Hand Zeiger](#hand-pointers)) angezeigt werden.
  - [Grafik links](ctrl-links.md) zeigen nur einen Hand Zeiger auf den Mauszeiger.
- **Verwenden Sie den Zeiger "Hand" (oder "Link Select") nur für Text-und Grafik links.** Andernfalls müssten Benutzer auf Objekte klicken, um zu bestimmen, ob es sich um Verknüpfungen handelt.

### <a name="standard-mouse-button-interactions"></a>Standard mäßige Maustasten Interaktionen

In der folgenden Tabelle werden die Maustasten Interaktionen zusammengefasst, die in den meisten Fällen angewendet werden:



| Interaktion                                    | Wirkung                                                                                                                                                                                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Darauf zeigen (Hover)<br/>                    | Ziel zeigt die QuickInfo, den Infotipp oder eine entsprechende an.<br/>                                                                                                                                                                                           |
| Einzelner Linksklick<br/>        | Aktiviert oder wählt das-Objekt aus. Bei Text wird die Einfügemarke festgelegt.<br/>                                                                                                                                                                           |
| Einzelner Rechtsklick<br/>       | Wählt das-Objekt aus und zeigt das zugehörige Kontextmenü an.<br/>                                                                                                                                                                                              |
| Doppelklicken Sie mit der linken Maustaste<br/>        | Aktiviert oder wählt das-Objekt aus und führt den Standardbefehl aus. Wählt für Text auf der Einfügemarke Word aus (bei einem dritten Klick wird der Satz oder Absatz ausgewählt).<br/>                                                                            |
| Doppelklicken Sie mit der rechten Maustaste<br/>       | Identisch mit einem Klick mit der rechten Maustaste.<br/>                                                                                                                                                                                                                    |
| UMSCHALT mit einem linken Mausklick<br/>  | Bei auswählbaren Objekten wird die Auswahl zusammenhängend erweitert. Andernfalls identisch mit einem linken Mausklick mit möglichen Änderungen. Beispielsweise führt in Paint das Zeichnen eines Oval mit dem UMSCHALT schlüsselmodifizierer zum Zeichnen eines Kreises.<br/>                  |
| UMSCHALT mit einem Rechtsklick<br/> | Identisch mit der Umschalttaste mit der linken Maustaste.<br/>                                                                                                                                                                                                               |
| UMSCHALT Doppel Linksklick<br/>  | Identisch mit der Umschalttaste mit der linken Maustaste, und führt den Standardbefehl für die gesamte Auswahl aus.<br/>                                                                                                                                                     |
| UMSCHALT Doppel Rechtsklick<br/> | Identisch mit der Umschalttaste mit der linken Maustaste.<br/>                                                                                                                                                                                                               |
| STRG mit der linken Maustaste<br/>   | Bei auswählbaren Objekten wird die Auswahl durch Umschalten des Auswahl Status des Elements, auf das geklickt wird, erhöht, ohne dass sich dies auf die Auswahl anderer Objekte auswirkt (sodass die Auswahl nicht zusammenhängend ist). Andernfalls identisch mit einem linken Mausklick.<br/> |
| STRG mit einem Rechtsklick<br/>  | Identisch mit der STRG-Taste mit der linken Maustaste.<br/>                                                                                                                                                                                                                |
| STRG Doppel Linksklick<br/>   | Identisch mit der STRG-Taste mit der linken Maustaste, und führt den Standardbefehl für die gesamte Auswahl aus.<br/>                                                                                                                                                      |
| STRG Doppel Rechtsklick<br/>  | Identisch mit der STRG-Taste mit der linken Maustaste.<br/>                                                                                                                                                                                                                |



 

### <a name="mouse-interaction"></a>Maus Interaktion

- **Legen Sie für Click mindestens 16x16 Pixel fest, damit alle Eingabegeräte problemlos auf Sie klicken können.** Für [die](inter-touch.md)Fingereingabe beträgt die empfohlene mindeststeuergröße 23x23 Pixel (13 x 13 DLUs). Es empfiehlt sich, die Größe kleiner Ziele dynamisch zu ändern, wenn der Benutzer darauf zeigt, dass Sie leichter zu finden sind.

    In diesem Beispiel sind die Drehfeld-Steuerelement Schaltflächen zu klein, um effektiv mit berühren oder einem Stift verwendet werden zu können.

    ![Screenshot des Drehfeld-Steuer Elements mit kleinen Pfeilen ](images/inter-mouse-image29.png) 

- **Legen Sie Aufteilungen um mindestens fünf Pixel breit, damit Sie von jedem Eingabegerät problemlos auf Sie klicken können.** Es empfiehlt sich, die Größe kleiner Ziele dynamisch zu ändern, wenn der Benutzer darauf zeigt, dass Sie leichter zu finden sind.

    In diesem Beispiel ist der Splitter im Windows-Explorer-Navigationsbereich zu schmal, um effektiv mit einer Maus oder einem Stift verwendet zu werden.

    ![Screenshot des schmalen, fast unsichtbaren Splitters ](images/inter-mouse-image30.png)

- **Stellen Sie Benutzern einen Fehler Rand räumlich bereit.** Hiermit wird eine Mausbewegung (z. b. drei Pixel) zugelassen, wenn Benutzer eine Maustaste loslassen. Benutzer bewegen die Maus manchmal etwas, wenn Sie die Maustaste loslassen, sodass die Mausposition direkt vor Schaltflächen Releases besser die Absicht des Benutzers widerspiegelt, als die Position unmittelbar nach.
- **Stellen Sie Benutzern vorübergehend einen Fehler Rand bereit.** Verwenden Sie die System Doppelklick-Geschwindigkeit, um zwischen einzelnen und doppelten Klicks zu unterscheiden.
- **Die Mausklicks werden bei der Maustaste gedrückt.** Hiermit wird Benutzern das Abbrechen von Mausaktionen gestattet, indem die Maus aus gültigen Zielen entfernt wird, bevor die Maustaste losgelassen wird. Bei den meisten Maus Interaktionen wird durch das Drücken einer Maustaste nur das ausgewählte Ziel angegeben, und durch das Freigeben der Schaltfläche wird die Aktion aktiviert. Automatische Wiederholungs Funktionen (z. b. das Drücken eines Bild Lauf Pfeils zum fortlaufenden scrollen) sind eine Ausnahme.
- [Erfassen Sie die Maus](/windows/win32/api/winuser/nf-winuser-setcapture) zum auswählen, verschieben, Ändern der Größe, aufteilen und ziehen.
- Verwenden Sie die ESC-Taste, um Benutzern das Abbrechen von zusammengesetzten Maus Interaktionen zu ermöglichen, z. b. verschieben, Ändern der Größe, aufteilen und ziehen
- **Wenn ein Objekt doppelte Klicks nicht unterstützt, die Benutzer aber wahrscheinlich davon ausgehen, dass dies der Fall ist, interpretieren Sie einen "Doppelklick" als einen Mausklick.** Nehmen Sie an, dass der Benutzer eine einzelne Aktion anstelle von zwei ausgeführt hat.

    Da Benutzer wahrscheinlich davon ausgehen, dass die Task leisten Schaltflächen doppelte Klicks unterstützen, sollte ein Doppelklick als einzelner Klick behandelt werden.

    ![Screenshot der Task leisten Schaltfläche und des Standard Zeigers ](images/inter-mouse-image31.png)

- **Ignorieren Sie redundante Mausklicks, während das Programm inaktiv ist.** Wenn der Benutzer z. b. 10 Mal auf eine Schaltfläche klickt, während ein Programm inaktiv ist, wird dies als einzelner Klick interpretiert.
- **Verwenden Sie keine doppelten zieht oder-Akkorde.** Ein doppelter Zieh Vorgang ist eine Zieh Aktion, die mit einem Doppelklick begonnen wird, und ein Akkord ist, wenn mehrere Maustasten gleichzeitig gedrückt werden. Diese Interaktionen sind nicht Standard, nicht auffundbar, sind schwer zu erfüllen und werden wahrscheinlich versehentlich ausgeführt.
- **Verwenden Sie alt nicht als Modifizierer für Maus Interaktionen.** Die Alt-Taste ist für den Zugriff auf die Symbolleiste und Zugriffstasten reserviert.
- **Verwenden Sie UMSCHALT + STRG nicht als Modifizierer für Maus Interaktionen.** Dies wäre zu schwierig zu verwenden.
- **Bewegen Sie den Mauszeiger.** Um das Programm touchabel zu gestalten, nutzen Sie den Mauszeiger vollständig, aber nur auf eine Weise, die für eine Aktion nicht erforderlich ist. Dies bedeutet in der Regel, dass eine Aktion auch durch klicken, jedoch nicht notwendigerweise auf die gleiche Weise ausgeführt werden kann. Hover wird von den meisten Touchtechnologien nicht unterstützt, sodass Benutzer mit solchen Touchscreens keine Aufgaben ausführen können, für die ein Mauszeiger erforderlich ist.

### <a name="mouse-wheel"></a>Mausrad

- **Das Mausrad wirkt sich auf das Steuerelement, den Bereich oder das Fenster aus, über dem sich der Zeiger derzeit befindet.** Dadurch werden unbeabsichtigte Ergebnisse vermieden.
- **Bewirken Sie, dass das Mausrad wirksam wird, ohne auf den Eingabefokus zu klicken.** Der Mauszeiger ist ausreichend.
- **Sorgen Sie dafür, dass das Mausrad das Objekt mit dem spezifischsten Bereich beeinflusst.** Wenn sich beispielsweise der Zeiger über einem Bild lauffähigen Listenfeld-Steuerelement in einem scrollbaren Bereich innerhalb eines Bild lauffähigen Fensters befindet, wirkt sich das Mausrad auf das Listenfeld-
- **Ändern Sie den Eingabefokus nicht, wenn Sie das Mausrad verwenden.**
- Lassen Sie das Mausrad folgende Auswirkungen:
  - Für scrollbare Fenster, Bereiche und Steuerelemente:
    - **Wenn Sie das Mausrad drehen, wird ein vertikaler Bildlauf durchgeführt.** Damit das Rad eine natürliche Zuordnung hat, sollte das Drehen des Mausrades nicht horizontal durchlaufen werden, da dies Disorienting und unerwartet ist.
      - **Wenn die STRG-Taste gedrückt wird, wird das-Objekt durch Drehen des Mausrades vergrößert, wobei die** Zoom-Taste vergrößert und die Zoom-Taste nach unten gedreht wird.
      - **Wenn Sie das Mausrad kippen, wird das Objekt horizontal bewegt.**
  - Für Zoombare Fenster und Bereiche (ohne Scrollleisten):
    - **Drehen des Mausrades zoomt das Objekt,** bei dem die Drehung der zoomungs-und Drehungs nach unten vergrößert wird.
    - Das Kippen des Mausrades hat keine Auswirkungen.
  - Für Registerkarten:
    - Wenn Sie **das Mausrad drehen, kann die aktuelle Registerkarte** unabhängig von der Ausrichtung der Registerkarten geändert werden.
    - Das Kippen des Mausrades hat keine Auswirkungen.
  - Wenn die UMSCHALTTASTE und die Alt-Taste gedrückt sind, hat das Mausrad keine Auswirkung.
- **Verwenden Sie die Windows-Systemeinstellungen für die vertikale Bild Lauf Größe (zum Drehen) und die horizontale scrollgröße (für das Kippen).** Diese Einstellungen können über das Element der Maussteuerung konfiguriert werden.
- **Wenn Sie das Mausrad schneller drehen, wird der Bildlauf schneller durchzuführen.** Auf diese Weise können Benutzer große Dokumente effizienter scrollen.
- **Bei Bild lauffähigen Fenstern sollten Sie auf die Maustaste klicken, um das Fenster in den Lesemodus zu versetzen.** Der Lesemodus ist ein spezielles Bild Lauf Ursprungs Symbol und führt einen Bildlauf im Fenster in Richtung und Geschwindigkeit relativ zum scrollursprung aus.

![Screenshot der Seite mit Bild Lauf-Ursprung-Symbol ](images/inter-mouse-image32.png)

*Internet Explorer unterstützt den Lesemodus, der das Bild Lauf-Ursprung-Symbol enthält.*

### <a name="hiding-the-pointer"></a>Ausblenden des Zeigers

- **Blenden Sie den Zeiger nicht aus.** Ausnahmen:
  - Präsentations Anwendungen, die im Vollbild-Präsentationsmodus ausgeführt werden, können den Zeiger ausblenden. Der Zeiger muss jedoch sofort wieder hergestellt werden, wenn Benutzer die Maus bewegen, und er kann nach zwei Sekunden Inaktivität wieder ausgeblendet werden.
  - Umgebungen ohne Maus (z. b. Kiosk) können den Zeiger dauerhaft ausblenden.
- Standardmäßig verbirgt Windows den Zeiger, während der Benutzer in ein Textfeld tippt. Diese Windows-Systemeinstellung kann über das Element der Maussteuerung konfiguriert werden.

### <a name="activity-pointers"></a>Aktivitäts Zeiger

Die Aktivitäts Zeiger in Windows sind der ausgelastete Zeiger (![Screenshot des ringförmigen Zeigers ](images/inter-mouse-image33.png)) und im Hintergrund Zeiger arbeiten (![Screenshot des ringförmigen Zeigers und Pfeils ](images/inter-mouse-image34.png)).

- Zeigen Sie den ausgelasteten Zeiger an, wenn Benutzer mehr als eine Sekunde warten müssen, bis eine Aktion beendet ist. Beachten Sie, dass der ausgelastete Zeiger keinen Hotspot hat, sodass Benutzer nicht auf eine beliebige Stelle klicken können, während Sie angezeigt wird.
- Zeigen Sie den "Working in background"-Zeiger an, wenn Benutzer mehr als eine Sekunde warten müssen, bis eine Aktion ausgeführt wird, das Programm jedoch reaktionsfähig ist und kein anderes visuelles Feedback vorhanden ist, dass die Aktion nicht fertiggestellt ist.
- Kombinieren Sie keine Aktivitäts Zeiger mit Status leisten oder Fortschritts Animationen.

### <a name="caret"></a>Einfügemarke

- **Zeigen Sie die Einfügemarke erst an, wenn das Texteingabe Fenster oder Steuerelement den Eingabefokus besitzt.** Die Einfügemarke schlägt Benutzern den Eingabefokus vor, aber ein Fenster oder ein Steuerelement kann die Einfügemarke ohne Eingabefokus anzeigen. Stehlen Sie den Eingabefokus natürlich nicht, sodass die Einfügemarke in einem kontextorientierten Dialogfeld angezeigt werden kann.

    Der Windows-Anmelde Informationsverwaltung wird außerhalb des Kontexts mit dem Caretzeichen, aber ohne Eingabefokus angezeigt. Folglich geben Benutzer Ihr Kennwort an unerwarteten Stellen ein.

    ![Screenshot der Anmelde Informationsverwaltung ohne Fokus ](images/inter-mouse-image35.png)

- **Platzieren Sie die Einfügemarke, in der die Benutzer höchstwahrscheinlich zuerst eingeben.** In der Regel ist dies entweder die letzte Stelle, an der der Benutzer eingegeben hat, oder am Ende des Texts.

### <a name="accessibility"></a>Eingabehilfen

- Für Benutzer, die die Maus überhaupt nicht verwenden können, lassen Sie die Maus mit der Tastatur redundant.
  - Benutzer sollten in der Lage sein, alles mit der Tastatur zu tun, die Sie mit der Maus ausführen können, mit Ausnahme von Aktionen, bei denen eine fein motorische Qualifikation erforderlich ist, wie z. b. zeichnen und spielen
  - Benutzer sollten in der Lage sein, alles mit der Maus zu tun, die Sie mit der Tastatur ausführen können, mit Ausnahme des effizienten Text Eintrags.
- Benutzern mit eingeschränkter Fähigkeit, die Maus zu verwenden:
  - Doppelklicken und ziehen Sie nicht die einzige Möglichkeit, um eine Aktion auszuführen.

Weitere Informationen und Richtlinien finden Sie unter [Barrierefreiheit](inter-accessibility.md).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Maus:

- Vermeiden Sie die Verwendung der Plural-MICE. Wenn Sie auf mehr als eine Maus verweisen müssen, verwenden Sie Maus Geräte.
- Verwenden Sie die Maustaste, um die linke Maustaste anzuzeigen. Verwenden Sie keine primäre Maustaste. Verwenden Sie auch die Rechte Maustaste anstelle der sekundären Maustaste. Unabhängig von der Richtigkeit verstehen Benutzer diese Begriffe, und Benutzer, die Ihre Schaltflächen neu programmieren, machen die geistige Verschiebung.
- Verwenden Sie Wheel für den drehenden Teil des Mausrades und die Radtaste, um auf den klickbaren Teil zu verweisen.
- Verwenden Sie Verben wie Click, Point und Drag, um auf Mausaktionen zu verweisen. Benutzer drehen das Rad vertikal, neigen es horizontal und klicken auf die Schaltfläche mit dem Mausrad.
- Verwenden Sie Drag und Not Drag & Drop, um ein Dokument oder einen Ordner zu verschieben. Es ist zulässig, Drag & Drop als Adjektiv zu verwenden, wie in "Verschieben des Ordners ist ein Drag & Drop-Vorgang."
- Doppelklicken Sie immer mit der rechten Maustaste auf als Verben.
- Verwenden Sie klicken Sie auf, und klicken Sie nicht auf. Klicken Sie auf (wie im Fenster "klicken Sie auf das Fenster") ist akzeptabel.

Beim Verweisen auf Mauszeiger:

- Verweisen Sie auf den Mauszeiger als Zeiger. Verwenden Sie den Cursor nur in der technischen Dokumentation.
- Verwenden Sie für Zeiger mit Aktivitätsindikatoren einen ausgelasteten Zeiger für den Zeiger, der nur aus einem Aktivitätsindikator besteht, und arbeiten Sie im Hintergrund Zeiger für den Kombinations Zeiger und den Aktivitätsindikator.
- Verwenden Sie für die anderen Zeiger Typen keine beschreibenden Bezeichnungen, um auf den Zeiger zu verweisen. Verwenden Sie ggf. eine Grafik, um zu beschreiben, wie der Mauszeiger auf dem Bildschirm angezeigt werden kann.

**Beispiele:**

- Zeigen Sie auf den Fensterrahmen.
- Klicken Sie mit der Maus auf die Schaltfläche **minimieren** .
- Halten Sie die UMSCHALTTASTE gedrückt, und klicken Sie auf die Rechte Maustaste.
- Wenn der Zeiger zu einem wird ![Screenshot des Pfeils mit zwei Kreuz leisten](images/inter-mouse-image18.png), ziehen Sie den Mauszeiger, um die geteilte Linie zu verschieben.

## <a name="see-also"></a>Siehe auch

- [Richtlinien für die Barrierefreiheit](inter-accessibility.md)
- [Richtlinien zur Berührungs Interaktion](inter-touch.md)
- [Richtlinien für Stift Interaktion](inter-pen.md)
- [Text Verknüpfungen](ctrl-links.md)
- [Grafik Verknüpfungen](ctrl-links.md)
- [Erfassen der Maus](/windows/win32/api/winuser/nf-winuser-setcapture)
- [Festlegen des Cursor Bilds](../learnwin32/setting-the-cursor-image.md)
- [Benutzereingabe: erweitertes Beispiel](../learnwin32/user-input--extended-example.md)
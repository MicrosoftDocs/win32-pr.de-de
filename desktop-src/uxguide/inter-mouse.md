---
title: Maus und Zeiger
description: Die Maus ist das primäre Eingabegerät, das für die Interaktion mit Objekten in Windows verwendet wird.
ms.assetid: 4d99287d-e908-4c8b-b4f6-6e8c91c6c93e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e973ad46ec864c20ad7eef5708388f86e8489909df1fdae609106d1ca65d4614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119030323"
---
# <a name="mouse-and-pointers"></a>Maus und Zeiger

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Die Maus ist das primäre Eingabegerät, das für die Interaktion mit Objekten in Windows verwendet wird. Mausfunktionen können auch andere zeigede Geräte umfassen, z. B. Trackballs, Touchpads und zeigede Steckhalter, die in Notebookcomputer integriert sind, Stifte, die mit Windows Tablet- und Touchtechnologie verwendet werden, und auf Computern mit Touchscreens sogar den Finger eines Benutzers.

> [!NOTE]
> Richtlinien für [Barrierefreiheit,](inter-accessibility.md) [Stift](inter-pen.md)und [Fingereingabe](inter-touch.md) werden in separaten Artikeln vorgestellt.

Wenn Sie den Mauszeiger physisch bewegen, wird der Grafische Zeiger (auch als Cursor bezeichnet) auf dem Bildschirm bewegt. Der Zeiger verfügt über eine Vielzahl von Formen, um sein aktuelles Verhalten anzugeben.

![Screenshot von fünf typischen Mauszeigern ](images/inter-mouse-image1.png)

*Typische Mauszeiger*

Mausgeräte verfügen häufig über eine primäre Schaltfläche (normalerweise die linke Schaltfläche), eine sekundäre Schaltfläche (normalerweise die rechte) und ein Mausrad zwischen den beiden. Durch Positionieren des Zeigers und Klicken auf die primären und sekundären Schaltflächen mit der Maus können Benutzer Objekte auswählen und Aktionen dafür ausführen. Bei den meisten Interaktionen zeigt das Drücken einer Maustaste, während sich der Cursor über einem Ziel befindet, das ausgewählte Ziel an, und das Loslassen der Schaltfläche führt alle Aktionen aus, die dem Ziel zugeordnet sind.

Alle Zeiger, mit Ausnahme des ausgelasteten Zeigers, verfügen über einen Single-Pixel-Hot Spot, der die genaue Bildschirmposition der Maus definiert. Der Hotspots bestimmt, welches Objekt von Mausaktionen betroffen ist. Objekte definieren eine heiße Zone, bei der es sich um den Bereich handelt, in dem der Hotspots als über dem Objekt betrachtet wird. In der Regel stimmt die heiße Zone mit den Rahmen eines Objekts überein, aber es kann größer sein, um die Benutzerabsicht zu vereinfachen.

Das Caretzeichen ist die blinkende vertikale Leiste, die angezeigt wird, wenn der Benutzer in ein Textfeld oder einen anderen Text-Editor eingibt. Das Caretchen ist unabhängig vom Zeiger (standardmäßig blendet Windows den Zeiger aus, während der Benutzer eingibt).

![Screenshot des Textfelds mit Cursor ](images/inter-mouse-image2.png)

*Der Caret*

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="the-mouse-is-intuitive"></a>Die Maus ist intuitiv.

Die Maus war ein erfolgreiches Eingabegerät, da sie für die typische menschliche Hand einfach zu verwenden ist. Die zeigerbasierte Interaktion war erfolgreich, da sie intuitiv ist und eine vielzahl von Erfahrungen ermöglicht.

**Gut entworfene Benutzeroberflächenobjekte werden als angebote bezeichnet, bei denen es sich um visuelle und Verhaltenseigenschaften eines Objekts handelt, die darauf hinweisen, wie es verwendet wird.** Der Zeiger fungiert als Proxy für die Hand, sodass Benutzer ähnlich wie mit physischen Objekten mit Bildschirmobjekten interagieren können. Wir Menschen wissen genau, wie die menschliche Hand funktioniert. Wenn also etwas so aussieht, als könnte es gepusht werden, versuchen wir, es zu pushen. Wenn es so aussieht, als ob es gepackt werden kann, versuchen wir, es zu greifen. Folglich können Benutzer herausfinden, wie Objekte mit starker Freundlichkeit verwendet werden, indem sie sich diese ansehen und ausprobieren.

![Screenshot einer Schaltfläche und eines Schiebereglers](images/inter-mouse-image3.png)

*Schaltflächen und Schieberegler bieten eine hohe Durchlässigkeit*

Im Gegensatz dazu ist es schwieriger, Objekte mit schlechter Erschwinglichkeit zu erkennen. Solche Objekte erfordern häufig eine Bezeichnung oder Anweisung, um sie zu erklären.

![Screenshot von Linktext und Interneterdensymbol](images/inter-mouse-image4.png)

*Linktext und Symbole weisen schlechtes Preis-/Unterlassungsstatus auf*

### <a name="some-aspects-of-mouse-use-are-not-intuitive"></a>Einige Aspekte der Mausverwendung sind nicht intuitiv.

**Beim Rechtsklick, Doppelklicken und Klicken mit den Tastenmodifizierern UMSCHALT ODER STRG handelt es sich um drei Mausinteraktionen, die nicht intuitiv sind,** da sie keine echten Entsprechungen haben. Im Gegensatz zu Tastenkombinationen und Zugriffstasten werden diese Mausinteraktionen in der Regel an keiner Stelle auf der Benutzeroberfläche dokumentiert. Dies deutet darauf hin, dass rechtsklickende, doppelklickende und Tastaturmodifizierer nicht erforderlich sein sollten, um grundlegende Aufgaben auszuführen, insbesondere nicht durch benutzerverhindtende Benutzer. Außerdem wird empfohlen, dass diese erweiterten Interaktionen ein konsistentes, vorhersagbares Verhalten aufweisen müssen, um effektiv verwendet werden zu können.

### <a name="single-click-or-double-click"></a>Einzelklick oder Doppelklick?

Doppelklicken wird auf dem Windows Desktop so umfassend verwendet, dass es möglicherweise nicht wie eine erweiterte Interaktion aussieht. Beispielsweise wird das Öffnen von Ordnern, Programmen oder Dokumenten im Dateibereich von Windows Explorer durch Doppelklicken ausgeführt. Das Öffnen einer Verknüpfung auf dem Windows Desktop verwendet auch Doppelklicken. Im Gegensatz dazu erfordert das Öffnen von Ordnern oder Programmen im Startmenü einen einzigen Klick.

Auswählbare Objekte verwenden single-click, um die Auswahl durchzuführen, sodass sie zum Öffnen einen Doppelklick erfordern, während nicht auswählbare Objekte nur einen einzigen Klick zum Öffnen erfordern. Diese Unterscheidung wird von vielen Benutzern nicht verstanden (wenn Sie auf ein Programmsymbol klicken, klicken Sie auf ein Programmsymbol, rechts?), und daher klicken einige Benutzer einfach auf Symbole, bis sie die gewünschten Informationen erhalten.

### <a name="direct-manipulation"></a>Direkte Manipulation

Die direkte Interaktion mit Objekten wird als direkte Bearbeitung bezeichnet. Zeigen, Klicken, Auswählen, Verschieben, Ändern der Größe, Teilen, Scrollen, Schwenken und Zoomen sind häufige direkte Bearbeitungen. Im Gegensatz dazu kann die Interaktion mit einem Objekt über sein Eigenschaftenfenster oder ein anderes Dialogfeld als indirekte Bearbeitung beschrieben werden.

**Wenn es jedoch eine direkte Manipulation gibt, kann es zu einer versehentlichen Manipulation kommen, und daher ist eine Freundlichkeit erforderlich.** Freundlichkeit ist die Fähigkeit, eine unerwünschte Aktion einfach umzukehren oder zu korrigieren. Sie nehmen direkte Manipulationen vor, indem Sie rückgängig machen, ein gutes visuelles Feedback geben und es Benutzern ermöglichen, Fehler einfach zu korrigieren. Im Zusammenhang mit der Freundlichkeit wird verhindert, dass unerwünschte Aktionen überhaupt ausgeführt werden. Dies können Sie tun, indem Sie eingeschränkte Steuerelemente und Bestätigungen für riskante Aktionen oder Befehle verwenden, die unbeabsichtigte Folgen haben.

### <a name="standard-mouse-button-interactions"></a>Standardinteraktionen für Maustasten

Die standardmäßigen Mausinteraktionen hängen von einer Vielzahl von Faktoren ab, z. B. der Maustaste, auf die geklickt wird, der Anzahl der Klicks, der Position während der Klicks und davon, ob Tastaturmodifizierer gedrückt wurden. Im Folgenden wird zusammengefasst, wie sich diese Faktoren in der Regel auf die Interaktion auswirken:

- Bei den meisten Objekten führt das linke Doppelklicken einen einzigen Linksklick und den Standardbefehl aus. Der Standardbefehl wird im Kontextmenü identifiziert.
- Bei einigen Typen von auswählbaren Objekten erweitert jeder Klick den Effekt des Klicks. Wenn Sie z. B. mit nur einem Klick in ein Textfeld klicken, wird die Eingabeposition festgelegt, durch Doppelklicken wird ein Wort ausgewählt, und beim Dreifachklick wird ein Satz oder Absatz ausgewählt.
- Durch Klicken mit der rechten Maustaste wird das Kontextmenü eines Objekts angezeigt.
- Wenn Sie die Maus während des Zeigens halten, wird mit dem Mauszeiger darauf zeigen.
- Wenn Sie die Maus beim Drücken der Maustasten belassen, wird durch Klicken und Auswahl einzelner Objekte angezeigt. Das Bewegen der Maus gibt das Verschieben, Ändern der Größe, Teilen, Ziehen und Auswahl mehrerer Objekte an.
- Die UMSCHALTTASTE erweitert die Auswahl zusammenhängend.
- Die STRG-TASTE erweitert die Auswahl, indem der Auswahlstatus des angeklickten Elements umgeklickt wird, ohne dass sich dies auf die Auswahl anderer Objekte auswirkt.

### <a name="simple-mouse-interactions"></a>Einfache Mausinteraktionen

In der folgenden Tabelle werden häufige Mausinteraktionen und -effekte beschrieben.

| Einfache Aktion | Interaktion | Typischer Effekt |
|:---|:---|:---|
| Zeigen<br/>          | Positionieren Sie den Zeiger auf ein bestimmtes Objekt, ohne auf Maustasten zu klicken.<br/>                                                                                                                                                                                                                                      | Ziel zeigt seinen Mauszeigerzustand und alle dynamischen Möglichkeiten an.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| Schwebt<br/>          | Positionieren Sie den Zeiger auf ein bestimmtes Objekt, ohne auf Maustasten zu klicken und sich mindestens eine Sekunde lang zu bewegen.<br/>                                                                                                                                                                                             | Ziel zeigt quicktip, infotip oder equivalent an.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Klicken<br/>          | Positionieren Sie den Zeiger auf ein bestimmtes, nicht auswählbares Objekt, und drücken Sie eine Maustaste, ohne sich zu bewegen. Das Klicken auf die Maustaste wird wirksam, damit Benutzer den Klick abbrechen können, indem sie den Mauszeiger vom Ziel bewegen. Daher zeigt die Maus nur das ausgewählte Ziel an.<br/> | Aktivieren Sie das -Objekt für Einfache Klicks mit der primären Schaltfläche. Aktivieren Sie für Doppelklicks mit der primären Schaltfläche das -Objekt, und führen Sie den Standardbefehl aus. Zeigen Sie für die sekundäre Schaltfläche das Kontextmenü des Objekts an.<br/>                                                                                                                                                                                         |
| Wählen Sie Folgendes aus:<br/>         | Positionieren Sie den Zeiger auf ein bestimmtes, auswählbares Objekt, und drücken Sie eine Maustaste, und lassen Sie sie los.<br/>                                                                                                                                                                                                                        | Wählen Sie für einfache Klicks mit der primären Schaltfläche das Objekt aus. Wenn die Benutzer die Maus ziehen, wählen Sie einen zusammenhängenden Bereich von Objekten aus. Wählen Sie für Doppelklicks mit der primären Schaltfläche das Objekt aus, und führen Sie den Standardbefehl aus.<br/> Für Text legt die rechte primäre Schaltfläche die Einfügemarke fest, das zweite wählt wort an der Einfügemarke aus, und der dritte Klick wählt den Satz oder Absatz aus.<br/> |
| Drücken von<br/>          | Positionieren Sie den Zeiger auf ein bestimmtes Objekt, und drücken Sie eine Maustaste, ohne loszulassen.<br/>                                                                                                                                                                                                                              | Aktivieren Sie für Funktionen mit automatischer Wiederholung (z. B. das Drücken eines Bildlaufpfeils zum fortlaufenden Scrollen) wiederholt. Andernfalls wird der Beginn einer Verschiebung, Größenänderung, Teilung oder Ziehbewegung angegeben, es sei denn, es folgt ein Release ohne Verschiebung.<br/>                                                                                                                                                                                               |
| Wheeling<br/>          | Mausrad bewegen.<br/>                                                                                                                                                                                                                                                                                                  | Fenster scrollt vertikal in Richtung Mausradbewegung.<br/>                                                                                                                                                                                                                                                                                                                                                      |

### <a name="pointer-shapes"></a>Zeigerformen

In der folgenden Tabelle werden gängige Zeigerformen und -verwendungen beschrieben.

| Formen | Name | Verwendung |
|:---|:---|:---|
| ![Screenshot des Zeigers mit Pfeilform ](images/inter-mouse-image5.png)<br/>           | Normale Auswahl<br/>    | Wird für die meisten Objekte verwendet.<br/>                                             |
| ![Screenshot der Hand mit zeigem Zeigefinger ](images/inter-mouse-image6.png)<br/>    | Linkauswahl<br/>      | Wird für Text- und Grafiklinks aufgrund ihres schwachen Affordances verwendet.<br/> |
| ![Screenshot des Zeigers mit Form "i-balken" ](images/inter-mouse-image7.png)<br/>          | Textauswahl<br/>      | Wird für Text verwendet, um eine Position zwischen Zeichen anzugeben.<br/>           |
| ![Screenshot des Zeigers mit großer Pluszeichenform ](images/inter-mouse-image8.png)<br/> | Genauigkeitsauswahl<br/> | Wird für grafische und andere zweidimensionale Interaktionen verwendet.<br/>            |

### <a name="compound-mouse-interactions"></a>Zusammengesetzte Mausinteraktionen

In der folgenden Tabelle werden häufige Mausinteraktionen beschrieben.

| Verbundaktion | Interaktion | Typischer Effekt | Zeiger |
|:---|:---|:---|:---|
| Verschieben<br/>                | Wenn das Verschieben ein Modus ist (durch Ausführen eines Befehls eingegeben), geben Sie den Modus ein, positionieren Sie den Zeiger auf ein verschiebbares Objekt, drücken Sie die Taste, und bewegen Sie die Maus, lassen Sie die Maustaste los. In diesem Fall ändert der Zeiger die Form, um den Modus anzugeben.<br/> Andernfalls positionieren Sie den Zeiger über dem Greifer eines verschiebbaren Objekts, drücken Sie die Taste, und bewegen Sie die Maus, und lassen Sie die Maustaste los. In diesem Fall muss der Zeiger die Form nicht ändern.<br/> | -Objekt wird in Richtung der Zeigerbewegung bewegt.<br/>            | Verschieben<br/> ![Screenshot des Zeigers mit vier Pfeilen ](images/inter-mouse-image9.png)<br/> wird verwendet, um ein Fenster in eine beliebige Richtung zu verschieben.<br/> Pfanne<br/> ![Screenshot des Zeigers mit Handform ](images/inter-mouse-image10.png)<br/> Wird verwendet, um ein Objekt innerhalb eines Fensters in eine beliebige Richtung zu verschieben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Größenänderung<br/>              | Positionieren Sie den Mauszeiger über einem vergrößerbaren Rahmen, oder ändern Sie die Größe, drücken Sie eine Maustaste, bewegen Sie die Maus, und lassen Sie dann die Maustaste los.<br/>                                                                                                                                                                                                                                                                                 | Die Objektgröße wird in Richtung der Zeigerbewegung geändert.<br/>          | Vertikale und horizontale Größenvergrößerung<br/> ![Screenshot: Nach unten zeigende Zeiger](images/inter-mouse-image11.png)![Screenshot von Nach-oben-links-Zeigern ](images/inter-mouse-image12.png)<br/> wird verwendet, um die Größe einer einzelnen Dimension zu ändern.<br/> Diagonale Größenvergrößerung<br/> ![bb545459.mouse13(en-us,msdn.10).png](images/inter-mouse-image13.png)![Screenshot von diagonalen Zeigern mit Pfeilspitzen](images/inter-mouse-image14.png)<br/> wird verwendet, um die Größe von zwei Dimensionen gleichzeitig zu ändern.<br/> Zeilen- und Spaltengröße ändern<br/> ![bb545459.mouse15(en-us,msdn.10).png](images/inter-mouse-image15.png)![Screenshot von Pfeilze0ern mit Querleiste ](images/inter-mouse-image16.png)<br/> Wird verwendet, um die Größe einer Zeile oder Spalte in einem Raster zu ändern.<br/> |
| Teilen<br/>             | Positionieren Sie den Mauszeiger über einem Splitter, drücken Sie eine Maustaste, bewegen Sie die Maus, und lassen Sie dann die Maustaste los.<br/>                                                                                                                                                                                                                                                                                                          | Der Rahmen des geteilten Bereichs wird in Richtung der Zeigerbewegung bewegt.<br/> | Fensterteilungen<br/> ![bb545459.mouse17(en-us,msdn.10).png](images/inter-mouse-image17.png)![Screenshot von Pfeilze0ern mit doppelter Querleiste ](images/inter-mouse-image18.png)<br/> Wird verwendet, um die Größe eines geteilten Bereichs vertikal oder horizontal zu ändern.<br/> |
| Drag & Drop<br/> | Positionieren Sie den Zeiger auf ein gültiges Objekt zum Ziehen, drücken Sie eine Maustaste, bewegen Sie die Maus zu einem Ablageziel, und lassen Sie dann die Maustaste los.<br/> | Das -Objekt wird in das Abbruchziel verschoben oder kopiert.<br/>             | normal select<br/> ![Screenshot von Foto, Standardzeiger und Infotip ](images/inter-mouse-image19.png)<br/> wird über gültige Ziehziele verwendet. kann auch über eine Infotip verfügen, um bestimmte Auswirkungen anzugeben.<br/> nicht verfügbar<br/> ![Screenshot des kleinen blockierten/offline-Symbols ](images/inter-mouse-image20.png)<br/> Wird verwendet, um anzugeben, dass eine Oberfläche kein gültiges Abbruchziel ist.<br/> |

### <a name="activity-indicators"></a>Aktivitätsindikatoren

Die folgende Tabelle zeigt Zeiger, die Benutzern angezeigt werden, wenn sie eine Aktion ausführen, die länger als einige Sekunden dauert.

| Formen | Name | Verwendung |
|:---|:---|:---|
| ![Screenshot, der einen ringförmigen "ausgelasteten" Zeiger zeigt.](images/inter-mouse-image21.png)<br/>          | Zeiger "Ausgelastet"<br/>                  | Wird verwendet, um darauf zu warten, dass ein Fenster reagiert.<br/>                                  |
| ![Screenshot eines ringförmigen Zeigers und Pfeils](images/inter-mouse-image22.png)<br/> | Arbeiten im Hintergrundzeiger<br/> | Wird verwendet, um zu zeigen, zu klicken, zu drücken oder auszuwählen, während eine Aufgabe im Hintergrund abgeschlossen wird.<br/> |

### <a name="hand-pointers"></a>Handze0er

Text- und Grafiklinks verwenden einen Hand- oder Linkauswahlzeiger (eine Hand mit zeigem Zeigefinger). ![Screenshot der Hand mit zeigem Zeigefinger ](images/inter-mouse-image6.png)) aufgrund ihres schwachen Vorhaltungs. Während Links möglicherweise andere visuelle Hinweise enthalten, die darauf hinweisen, dass es sich um Links handelt (z. B. Unterstreichungen und spezielle Platzierung), ist die Anzeige des Handzeigers beim Zeigen die definitive Angabe eines Links.

**Um Verwirrung zu vermeiden, ist es zwingend erforderlich, den Handzeiger nicht für andere Zwecke zu verwenden.** Beispielsweise verfügen Befehlsschaltflächen bereits über ein starkes Leisten, sodass sie keinen Handzeiger benötigen. Der Handzeiger muss "this target is a link" (Dieses Ziel ist ein Link) und nichts anderes bedeuten.

### <a name="custom-pointers"></a>Benutzerdefinierte Zeiger

Windows unterstützt die Erstellung benutzerdefinierter Zeiger. Weitere Informationen finden Sie unter [Festlegen des Cursorbilds und](../learnwin32/setting-the-cursor-image.md) der [Benutzereingabe: Erweitertes Beispiel.](../learnwin32/user-input--extended-example.md)

Viele Anwendungen stellen eine Palette von Steuerelementen mit benutzerdefinierten Zeigern zur Unterstützung der Anwendungsfunktionalität zur Verfügung.

![Screenshot der Palette mit Spray-Can-Zeiger ](images/inter-mouse-image23.png)

*Microsoft Paint enthält eine Palette verschiedener Funktionen mit jeweils einem eindeutigen Zeiger.*

### <a name="fitts-law"></a>Fitts' Law

Fitts' Law ist ein bekanntes Prinzip in Designdesigns für grafische Benutzeroberflächen, das im Wesentlichen Besagt:

- Je weiter ein Ziel entfernt ist, je länger es dauert, es mit der Maus zu erhalten.
- Je kleiner ein Ziel ist, desto länger dauert es, es mit der Maus zu erhalten.

Daher sind große Ziele gut. Achten Sie darauf, dass der gesamte Zielbereich klickbar ist.

| Falsch | Richtig (das gesamte Ziel kann angeklickt werden) |
|:---|:---|
| ![Screenshot des Symbols, auf das nur auf die Bezeichnung geklickt werden kann ](images/inter-mouse-image24.png) | ![Screenshot des klickbaren Symbols und der klickbaren Bezeichnung ](images/inter-mouse-image25.png) |

Sie können die Größe eines Ziels dynamisch ändern, wenn Sie darauf verweisen, um das Erwerben zu vereinfachen.

![Screenshot der Zeichenzuordnung mit vergrößerter Zahl ](images/inter-mouse-image26.png)

*Ein Ziel wird größer, wenn der Benutzer darauf zeigt, dass es einfacher zu erhalten ist.*

Und auch nahe Ziele sind gut. Suchen Sie nach klickbaren Elementen in der Nähe des Orts, an dem sie wahrscheinlich verwendet werden. In der folgenden Abbildung ist die Farbpalette zu weit von der Toolauswahl entfernt.

![Screenshot der Farbpalette, getrennt von Tools ](images/inter-mouse-image27.png)

*Die Farbpalette ist zu weit von dem Ort entfernt, an dem sie wahrscheinlich verwendet wird.*

Beachten Sie, dass die aktuelle Zeigerposition des Benutzers so nah wie ein Ziel ist, was das Erfassen trivial macht. Daher nutzen Kontextmenüs das Fitts-Gesetz genauso wie die mini-Symbolleisten, die von der Microsoft Office.

![Screenshot von Zeigern in der Nähe der Dropdownliste ](images/inter-mouse-image28.png)

*Die aktuelle Zeigerposition ist immer am einfachsten zu erhalten.*

Berücksichtigen Sie auch alternative Eingabegeräte, wenn Sie Objektgrößen bestimmen. Die für Touch touch empfohlene Mindestzielgröße beträgt beispielsweise 23 x 23 Pixel (13 x 13 DLUs).

### <a name="environments-without-a-mouse"></a>Umgebungen ohne Maus

Nicht alle Windows haben eine Maus. Kioske haben z. B. selten eine Maus und verfügen stattdessen in der Regel über einen Touchscreen. Dies bedeutet, dass Benutzer einfache Interaktionen ausführen können, z. B. das Klicken mit der linken Maustaste und das Ziehen und Ablegen. Sie können jedoch nicht mit der Maustaste darauf klicken, mit der rechten Maustaste klicken oder doppelklicken. Diese Situation ist einfach zu entwerfen, da diese Einschränkungen in der Regel im Voraus bekannt sind.

Die Verwendung einer Maus erfordert fein motorische Fähigkeiten, und daher können nicht alle Benutzer eine Maus verwenden. Stellen Sie sicher, dass alle Interaktionen, für die keine feinen motorischen Fähigkeiten erforderlich sind, stattdessen über die Tastatur ausgeführt werden können, um Ihre Software für eine möglichst große Zielgruppe zugänglich zu machen.

Weitere Informationen und Richtlinien finden Sie unter [Barrierefreiheit.](inter-accessibility.md)

**Wenn Sie nur vier Dinge tun...**

1.  Verhalten von Mausinteraktionen konsistent mit ihren Standardeffekten, und verwenden Sie dabei nach Bedarf die Standardzeiger.
2.  Beschränken Sie erweiterte Mausinteraktionen (solche, die Rechtsklicks, mehrere Klicks oder Modifizierertasten erfordern) auf erweiterte Aufgaben für fortgeschrittene Benutzer.
3.  Weisen Sie erweiterte Mausinteraktionen konsistentes, vorhersagbares Verhalten zu, damit sie effektiv verwendet werden können.
4.  Stellen Sie sicher, dass Ihr Programm die Möglichkeit bietet, unerwünschte Aktionen umzukehren oder zu korrigieren, insbesondere für destruktive Befehle. Versehentliche Aktionen sind bei verwendung der direkten Bearbeitung wahrscheinlicher.

## <a name="guidelines"></a>Richtlinien

### <a name="click-affordance"></a>Klicken Sie auf "Affordance".

- **Erfordern Sie niemals, dass Benutzer auf ein Objekt klicken, um zu bestimmen, ob es angeklickt werden kann.** Benutzer müssen die Klickbarkeit allein durch visuelle Überprüfung bestimmen können.
  - Die primäre Benutzeroberfläche (z. B. Commitschaltflächen) muss über ein statisches Klick-Affordance verfügen. Benutzer sollten nicht darauf bewegen müssen, um die primäre Benutzeroberfläche zu entdecken.
  - Die sekundäre Benutzeroberfläche (z. B. sekundäre Befehle oder Steuerelemente für die progressive Offenlegung) kann ihr Klick-Affordance beim Zeigen anzeigen.
  - [Textlinks](ctrl-links.md) sollten linktext statisch vorschlagen und dann ihr Klick-Affordance [](#hand-pointers)(Unterstrich oder andere Präsentationsänderung, mit Handzeiger) anzeigen, wenn Sie darauf zeigen.
  - [Grafiklinks](ctrl-links.md) zeigen nur einen Handzeiger an, wenn darauf gezeigt wird.
- **Verwenden Sie den Handzeiger (oder "Linkauswahl") nur für Text- und Grafiklinks.** Andernfalls müssten Benutzer auf Objekte klicken, um zu ermitteln, ob es sich um Links handelt.

### <a name="standard-mouse-button-interactions"></a>Standardinteraktionen mit der Maustaste

In der folgenden Tabelle sind die Interaktionen mit der Maustaste zusammengefasst, die in den meisten Fällen gelten:



| Interaktion                                    | Wirkung                                                                                                                                                                                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Darauf zeigen (Hover)<br/>                    | Das Ziel zeigt seine QuickInfo, Infotip oder entsprechung an.<br/>                                                                                                                                                                                           |
| Einzelner Linkklick<br/>        | Aktiviert oder wählt das Objekt aus. Legt für Text die Einfügemarke fest.<br/>                                                                                                                                                                           |
| Einzelner Rechtsklick<br/>       | Wählt das Objekt aus und zeigt das Kontextmenü an.<br/>                                                                                                                                                                                              |
| Doppelklicken Mit der linken Maustaste<br/>        | Aktiviert oder wählt das Objekt aus und führt den Standardbefehl aus. Für Text wählt wort an der Einfügemarke aus (ein dritter Klick wählt den Satz oder Absatz aus).<br/>                                                                            |
| Doppelklicken Mit der rechten Maustaste<br/>       | Identisch mit einem einzigen Rechtsklick.<br/>                                                                                                                                                                                                                    |
| Umschalten mit nur einem Klick mit der linken Maustaste<br/>  | Bei auswählbaren Objekten erweitert zusammenhängend die Auswahl. Andernfalls identisch mit einem einzelnen Linksklick mit möglichen Änderungen. Wenn Sie beispielsweise in Paint, führt das Zeichnen eines Ovals mit dem Umschalttastenmodifizierer zum Zeichnen eines Kreises.<br/>                  |
| Einfaches Klicken mit der rechten Maustaste umschalten<br/> | Identisch mit Umschalten mit nur einem Klick mit der linken Maustaste.<br/>                                                                                                                                                                                                               |
| Doppelklicken mit der linken Maustaste umschalten<br/>  | Identisch mit Umschalten mit nur einem Klick mit der linken Maustaste, und führt den Standardbefehl für die gesamte Auswahl aus.<br/>                                                                                                                                                     |
| Doppelklicken mit der rechten Maustaste umschalten<br/> | Identisch mit Umschalten mit nur einem Klick mit der linken Maustaste.<br/>                                                                                                                                                                                                               |
| STRG– einzelner Linkklick<br/>   | Bei auswählbaren Objekten erweitert die Auswahl, indem der Auswahlzustand des geklickten Elements umgekniffen wird, ohne die Auswahl anderer Objekte zu beeinflussen (sodass die Auswahl nicht zusammenhängend ist). Andernfalls ist dies identisch mit einem einzigen Klick mit der linken Maustaste.<br/> |
| STRG– einmaliger Rechtsklick<br/>  | Identisch mit DER STRG-TASTE, indem Sie mit der linken Maustaste klicken.<br/>                                                                                                                                                                                                                |
| Doppelklicken Sie mit der STRG-TASTE auf die linke Maustaste.<br/>   | Identisch mit STRG, indem Sie mit der linken Maustaste klicken, und führt den Standardbefehl für die gesamte Auswahl aus.<br/>                                                                                                                                                      |
| Doppelklicken Sie mit der rechten Maustaste auf STRG.<br/>  | Identisch mit DER STRG-TASTE, indem Sie mit der linken Maustaste klicken.<br/>                                                                                                                                                                                                                |



 

### <a name="mouse-interaction"></a>Mausinteraktion

- **Klicken Sie auf mindestens 16 x 16 Pixel, damit sie problemlos von einem beliebigen Eingabegerät angeklickt werden können.** Für [touch](inter-touch.md)beträgt die empfohlene Mindestgröße für das Steuerelement 23 x 23 Pixel (13 x 13 DLUs). Erwägen Sie, die Größe kleiner Ziele dynamisch zu ändern, wenn der Benutzer darauf hindeinformationen, um sie leichter zu erhalten.

    In diesem Beispiel sind die Drehungssteuerungsschaltflächen zu klein, um effektiv mit touch oder einem Stift verwendet zu werden.

    ![Screenshot des Drehungssteuer steuerelements mit kleinen Pfeilen ](images/inter-mouse-image29.png) 

- **Erstellen Sie Splitter mit einer Breite von mindestens fünf Pixeln, damit sie problemlos von jedem Eingabegerät angeklickt werden können.** Erwägen Sie, die Größe kleiner Ziele dynamisch zu ändern, wenn der Benutzer darauf hindeinformationen, um sie leichter zu erhalten.

    In diesem Beispiel ist der Splitter im Navigationsbereich Windows Explorer zu schmal, um effektiv mit einer Maus oder einem Stift verwendet zu werden.

    ![Screenshot eines schmalen, fast unsichtbaren Splitters ](images/inter-mouse-image30.png)

- **Stellen Sie benutzern einen räumlichen Fehlerrand zur Verfügung.** Lassen Sie mausbewegungen (z. B. drei Pixel) zu, wenn Benutzer eine Maustaste los lassen. Benutzer bewegen die Maus manchmal etwas, wenn sie die Maustaste los lassen, sodass die Mausposition direkt vor der Freigabe der Schaltfläche die Absicht des Benutzers besser widerspiegelt als die Position direkt danach.
- **Geben Sie Benutzern einen Fehlerrand in zeitlicher Hinsicht an.** Verwenden Sie die Doppelklickgeschwindigkeit des Systems, um zwischen Einzel- und Doppelklicks zu unterscheiden.
- **Haben Klicks, wird die Maustaste nach oben wirksam.** Ermöglichen Sie Es Benutzern, Mausaktionen zu verablassen, indem Sie die Maus von gültigen Zielen entfernen, bevor Sie die Maustaste loslassen. Bei den meisten Mausinteraktionen zeigt das Drücken einer Maustaste nur das ausgewählte Ziel an, und das Loslassen der Schaltfläche aktiviert die Aktion. Funktionen zur automatischen Wiederholung (z. B. das Drücken eines Bildlaufpfeils zum fortlaufenden Scrollen) sind eine Ausnahme.
- [Erfassen Sie die Maus](/windows/win32/api/winuser/nf-winuser-setcapture) zum Auswählen, Verschieben, Ändern der Größe, Teilen und Ziehen.
- Verwenden Sie die ESC-TASTE, damit Benutzer zusammengesetzte Mausinteraktionen wie Verschieben, Ändern der Größe, Teilen und Ziehen verabbruchen können.
- **Wenn ein Objekt keine Doppelklicks unterstützt, benutzer aber wahrscheinlich davon ausgehen, dass es dies tut, interpretieren Sie einen "Doppelklick" als einen einzigen Klick.** Angenommen, der Benutzer hat eine einzelne Aktion anstelle von zwei beabsichtigt.

    Da Benutzer wahrscheinlich davon ausgehen, dass Taskleistenschaltflächen Doppelklicks unterstützen, sollte ein "Doppelklick" als einzelner Klick behandelt werden.

    ![Screenshot der Taskleistenschaltfläche und des Standardzeigers ](images/inter-mouse-image31.png)

- **Redundante Mausklicks ignorieren, während das Programm inaktiv ist.** Wenn der Benutzer beispielsweise 10 Mal auf eine Schaltfläche klickt, während ein Programm inaktiv ist, interpretieren Sie dies als einfachen Klick.
- **Verwenden Sie keine doppelten Zieh- oder Chords.** Ein doppelter Ziehpunkt ist eine Ziehaktion, die mit einem Doppelklick begonnen wird, und ein Chord ist, wenn mehrere Maustasten gleichzeitig gedrückt werden. Diese Interaktionen sind nicht standardmäßig, nicht erkennbar, schwierig durchzuführen und werden höchstwahrscheinlich versehentlich durchgeführt.
- **Verwenden Sie ALT nicht als Modifizierer für Mausinteraktionen.** Die ALT-TASTE ist für den Zugriff auf die Symbolleiste und Zugriffsschlüssel reserviert.
- **Verwenden Sie UMSCHALT+STRG nicht als Modifizierer für Mausinteraktionen.** Dies wäre zu schwierig zu verwenden.
- **Sorgen Sie dafür, dass der Mauszeiger redundant ist.** Um Ihr Programm anstreifbar zu machen, nutzen Sie den Mauszeiger in vollem Umfang, aber nur auf eine Weise, die nicht erforderlich ist, um eine Aktion auszuführen. Dies bedeutet in der Regel, dass eine Aktion auch durch Klicken ausgeführt werden kann, aber nicht unbedingt auf die gleiche Weise. Der Mauszeiger wird von den meisten Touchtechnologien nicht unterstützt, sodass Benutzer mit solchen Touchscreens keine Aufgaben ausführen können, die zeigen müssen.

### <a name="mouse-wheel"></a>Mausrad

- **Damit sich das Mausrad auf das Steuerelement, den Bereich oder das Fenster auswirkt, über dem sich der Zeiger derzeit befindet.** Dadurch werden unbeabsichtigte Ergebnisse vermieden.
- **Sorgen Sie dafür, dass das Mausrad wirksam wird, ohne auf das Mausrad zu klicken oder den Eingabefokus zu haben.** Der Mauszeiger ist ausreichend.
- **Sorgen Sie dafür, dass sich das Mausrad auf das Objekt mit dem spezifischsten Bereich auswirkt.** Wenn sich der Zeiger beispielsweise über einem bildlauffähigen Listenfeld-Steuerelement in einem bildlauffähigen Bereich innerhalb eines bildlauffähigen Fensters befindet, wirkt sich das Mausrad auf das Listenfeld-Steuerelement aus.
- **Ändern Sie den Eingabefokus nicht, wenn Sie das Mausrad verwenden.**
- Geben Sie dem Mausrad die folgenden Effekte:
  - Für scrollbare Fenster, Bereiche und Steuerelemente:
    - **Durch Drehen des Mausrads wird das Objekt vertikal gescrollt, wobei nach oben gescrollt wird.** Damit das Rad eine natürliche Zuordnung hat, sollte das Drehen des Mausrads nie horizontal scrollen, da dies desorientierend und unerwartet ist.
      - **Wenn die STRG-TASTE gedrückt wird, vergrößert die Drehung des Mausrads das Objekt,** wobei das Drehen nach oben vergrößert und nach unten verkleinern wird.
      - **Beim Drehen des Mausrads wird das Objekt horizontal gescrollt.**
  - Für zoombare Fenster und Bereiche (ohne Scrollleisten):
    - **Durch drehen des Mausrads wird das Objekt vergrößert,** wobei das Drehen nach oben vergrößert und das Drehen nach unten verkleinern wird.
    - Das Neigen des Mausrads hat keine Auswirkungen.
  - Für Registerkarten:
    - **Durch Drehen des Mausrads kann die aktuelle Registerkarte** unabhängig von der Ausrichtung der Registerkarten geändert werden.
    - Das Neigen des Mausrads hat keine Auswirkungen.
  - Wenn umschalten und ALT gedrückt sind, hat das Mausrad keine Auswirkungen.
- **Verwenden Sie die Windows Systemeinstellungen für die vertikale Bildlaufgröße (zum Drehen) und die horizontale Bildlaufgröße (zum Neigen).** Diese Einstellungen können über das Systemsteuerungselement Maus konfiguriert werden.
- **Wenn Sie das Mausrad schneller drehen, können Sie schneller scrollen.** Auf diese Weise können Benutzer einen effizienteren Bildlauf für große Dokumente durchführen.
- **Ziehen Sie für scrollbare Fenster in Betracht, das Fenster durch Klicken auf das Mausrad in den Readermodus zu versetzen.** Der Readermodus verzweigt ein spezielles Bildlaufursprungssymbol und führt einen Bildlauf im Fenster in Richtung und Geschwindigkeit relativ zum Scrollursprung durch.

![Screenshot der Seite mit Scrollursprungssymbol ](images/inter-mouse-image32.png)

*Internet Explorer unterstützt den Readermodus, der das Scrollursprungssymbol enthält.*

### <a name="hiding-the-pointer"></a>Ausblenden des Zeigers

- **Blenden Sie den Zeiger nicht aus.** Ausnahmen:
  - Präsentationsanwendungen, die im Vollbildpräsentationsmodus ausgeführt werden, können den Zeiger ausblenden. Der Zeiger muss jedoch sofort wiederhergestellt werden, wenn Benutzer den Mauszeiger bewegen, und kann nach zwei Sekunden Inaktivität erneut angezeigt werden.
  - Umgebungen ohne Maus (z. B. Kioske) können den Zeiger dauerhaft ausblenden.
- Standardmäßig blendet Windows den Zeiger aus, während der Benutzer in ein Textfeld eingibt. Diese Windows Systemeinstellung kann über das Steuerelement Maussteuerung konfiguriert werden.

### <a name="activity-pointers"></a>Aktivitätszeiger

Die Aktivitätszeiger in Windows sind der ausgelastete Zeiger (![Screenshot des ringförmigen Zeigers ](images/inter-mouse-image33.png)) und der im Hintergrund arbeitende Zeiger (![Screenshot: Ringförmiger Zeiger und Pfeil ](images/inter-mouse-image34.png)).

- Zeigt den ausgelasteten Zeiger an, wenn Benutzer mehr als eine Sekunde warten müssen, bis eine Aktion abgeschlossen ist. Beachten Sie, dass der ausgelastete Zeiger keinen Hotspot hat, sodass Benutzer während der Anzeige auf nichts klicken können.
- Zeigt den Funktionierenden im Hintergrundzeiger an, wenn Benutzer mehr als eine Sekunde warten müssen, bis eine Aktion abgeschlossen ist, das Programm aber reaktionsfähig ist und kein anderes visuelles Feedback vorhanden ist, dass die Aktion nicht abgeschlossen ist.
- Kombinieren Sie Aktivitätszeiger nicht mit Statusleisten oder Statusanimationen.

### <a name="caret"></a>Einfügemarke

- **Zeigen Sie das Caretzeichen erst an, wenn das Texteingabefenster oder -steuerelement den Eingabefokus besitzt.** Das Caretelement schlägt Benutzern den Eingabefokus vor, aber ein Fenster oder Steuerelement kann das Caretelement ohne Eingabefokus anzeigen. Sie dürfen den Eingabefokus natürlich nicht stehlen, damit ein Kontextdialogfeld das Caretfeld anzeigen kann.

    Die Windows Anmeldeinformationsverwaltung wird außerhalb des Kontexts mit dem Caretpunkt, aber ohne Eingabefokus angezeigt. Daher geben Benutzer ihr Kennwort an unerwarteten Stellen ein.

    ![Screenshot des Anmeldeinformations-Managers ohne Fokus ](images/inter-mouse-image35.png)

- **Platzieren Sie das Caretzeichen an der Stelle, an der Benutzer am wahrscheinlichsten zuerst eingeben.** In der Regel ist dies entweder der letzte Ort, den der Benutzer eingibt, oder am Ende des Texts.

### <a name="accessibility"></a>Zugriff

- Für Benutzer, die die Maus überhaupt nicht verwenden können, machen Sie die Maus mit der Tastatur redundant.
  - Benutzer sollten in der Lage sein, alles mit der Tastatur zu tun, was sie mit der Maus können, mit Ausnahme von Aktionen, für die fein motorische Fähigkeiten wichtig sind, z. B. Zeichnen und Spielen.
  - Benutzer sollten mit der Maus alles tun können, was sie mit der Tastatur können, mit Ausnahme effizienter Texteingaben.
- Für Benutzer mit eingeschränkter Möglichkeit zur Verwendung der Maus:
  - Führen Sie kein Doppelklicken und Ziehen aus, um eine Aktion auszuführen.

Weitere Informationen und Richtlinien finden Sie unter [Barrierefreiheit.](inter-accessibility.md)

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Maus:

- Vermeiden Sie die Verwendung der Pluralmaus; Wenn Sie auf mehrere Mauszeiger verweisen müssen, verwenden Sie Mausgeräte.
- Verwenden Sie die Maustaste, um die linke Maustaste anzugeben. Verwenden Sie keine primäre Maustaste. Verwenden Sie auf ähnliche Weise die rechte Maustaste anstelle der sekundären Maustaste. Unabhängig von der Genauigkeit verstehen Benutzer diese Begriffe, und Benutzer, die ihre Schaltflächen neu erstellen, bewirken die mentale Verschiebung.
- Verwenden Sie das Rad für den drehenden Teil des Mausrads und die Radschaltfläche, um auf den klickbaren Teil zu verweisen.
- Verwenden Sie Verben wie Klicken, Zeigen und Ziehen, um auf Mausaktionen zu verweisen. Benutzer drehen das Rad vertikal, neigen es horizontal, und klicken auf die Radschaltfläche.
- Verwenden Sie Drag & Drop(nicht Drag & Drop), um ein Dokument oder einen Ordner zu verschieben. Es ist akzeptabel, Drag & Drop als Adjektiv zu verwenden, wie in "Verschieben des Ordners ist ein Drag & Drop-Vorgang".
- Doppelklicken Sie immer mit einem Bindestrich, und klicken Sie mit der rechten Maustaste als Verben.
- Klicken Sie auf klicken, nicht auf . Ein Klicken in (wie in "In das Fenster klicken") ist akzeptabel.

Beim Verweisen auf Mauszeiger:

- Verweisen Sie auf den Mauszeiger als Zeiger. Verwenden Sie cursor nur in der technischen Dokumentation.
- Verwenden Sie für Zeiger mit Aktivitätsindikatoren einen ausgelasteten Zeiger für den Zeiger, der nur aus einem Aktivitätsindikator besteht, und arbeiten Sie im Hintergrundzeiger für den Kombinationszeiger und den Aktivitätsindikator.
- Verwenden Sie für die anderen Zeigertypen keine beschreibenden Bezeichnungen, um auf den Zeiger zu verweisen. Verwenden Sie bei Bedarf eine Grafik, um zu beschreiben, wie der Mauszeiger auf dem Bildschirm angezeigt werden kann.

**Beispiele:**

- Zeigen Sie auf den Fensterrahmen.
- Klicken Sie mit der Maus auf die **Schaltfläche Minimieren.**
- Halten Sie die UMSCHALTTASTE gedrückt, und klicken Sie mit der rechten Maustaste.
- Wenn der Zeiger zu einem wird ![Screenshot des Pfeils mit zwei Querleisten](images/inter-mouse-image18.png)ziehen Sie den Zeiger, um die geteilte Linie zu verschieben.

## <a name="see-also"></a>Weitere Informationen

- [Richtlinien für die Barrierefreiheitsinteraktion](inter-accessibility.md)
- [Richtlinien für die Touchinteraktion](inter-touch.md)
- [Richtlinien für die Stiftinteraktion](inter-pen.md)
- [Textlinks](ctrl-links.md)
- [Grafiklinks](ctrl-links.md)
- [Erfassen der Maus](/windows/win32/api/winuser/nf-winuser-setcapture)
- [Festlegen des Cursorbilds](../learnwin32/setting-the-cursor-image.md)
- [Benutzereingabe: Erweitertes Beispiel](../learnwin32/user-input--extended-example.md)
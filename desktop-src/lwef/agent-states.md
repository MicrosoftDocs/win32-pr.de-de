---
title: Agent-Status
description: Agent-Status
ms.assetid: 8c3c5b12-81af-4ba5-b834-9f0a7ff5d075
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c371b1a2126129c03f16ce7fc7c2f95cca955a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206415"
---
# <a name="agent-states"></a>Agent-Status

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Microsoft-Agent-Animations Dienste geben automatisch bestimmte Animationen für Sie wieder. Wenn Sie z. b. die Befehle " [**muveto**](moveto-method.md) " oder " [**gestureat**](gestureat-method.md) " verwenden, spielen die Animations Dienste eine passende Animation. Entsprechend spielen die Dienste nach dem Leerlauf Timeout automatisch Animationen. Um diese Zustände zu unterstützen, können Sie entsprechende Animationen definieren und Sie dann den Zuständen zuweisen. Sie können weiterhin jede Animation, die Sie direkt definieren, mithilfe der [**Play**](play-method.md) -Methode abspielen, auch wenn Sie Sie einem Zustand zuweisen.

Sie können dem gleichen Zustand mehrere Animationen zuweisen, und die Animations Dienste wählen nach dem Zufallsprinzip eine ihrer Animationen aus. Dadurch kann Ihr Zeichen eine weitaus natürlichere Vielfalt im Verhalten aufweisen.

Obwohl Animationen, die Sie Zuständen zuweisen, Verzweigungs Rahmen einschließen können, vermeiden Sie Schleifen Schleifen (Animationen, die sich immer im Branch befinden). Andernfalls müssen Sie die Methode " [**Ende**](play-method.md) " verwenden, bevor Sie eine weitere Animation wiedergeben können.

Es ist wichtig, für jeden Zustand, der für das Zeichen auftritt, mindestens eine Animation zu definieren und zuzuweisen. Wenn Sie diese Animationen und Zustands Zuweisungen nicht angeben, verhält sich das Zeichen möglicherweise nicht ordnungsgemäß für den Benutzer. Wenn jedoch kein Zustand für ein bestimmtes Zeichen auftritt, müssen Sie diesem Zustand keine Animation zuweisen. Wenn die Host Anwendung z. b. nie die Methode " [**muveto**](moveto-method.md) " aufruft, können Sie das Erstellen **und Zuweisen von** Verschiebungs Zustands Animationen überspringen.



| State              | Verwendungs Beispiel                                                                         |
|--------------------|----------------------------------------------------------------------------------------|
| **Gesturingdown**  | Wenn die [**gestureat**](gestureat-method.md) -Animations Methode verarbeitet wird.          |
| **Gesturingleft**  | Wenn die [**gestureat**](gestureat-method.md) -Animations Methode verarbeitet wird.          |
| **Gesturingright** | Wenn die [**gestureat**](gestureat-method.md) -Animations Methode verarbeitet wird.          |
| **Gesturingup**    | Wenn die [**gestureat**](gestureat-method.md) -Animations Methode verarbeitet wird.          |
| **Hörvermögen**        | Wenn der Anfang der gesprochenen Eingabe erkannt wird.                                        |
| **Zieher**         | Wenn der Benutzer oder die Anwendung das Zeichen verbirgt.                                  |
| **IdlingLevel1**   | Wenn das Zeichen den Status der **Leerlauf** Zeit beginnt.                                        |
| **IdlingLevel2**   | Wenn das Zeichen den zweiten Status der **idtebene** startet.                           |
| **IdlingLevel3**   | Wenn das Zeichen den endgültigen Status der **idtebene** startet.                            |
| **Raum**      | Wenn das Zeichen mit dem lauschen beginnt (der Benutzer drückt zuerst die EINGABETASTE für die Spracheingabe). |
| **"Wvingdown"**     | Wenn die Animations Methode " [**muveto**](moveto-method.md) " verarbeitet wird.                |
| **"Wvingleft"**     | Wenn die Animations Methode " [**muveto**](moveto-method.md) " verarbeitet wird.                |
| **"Wvingright"**    | Wenn die Animations Methode " [**muveto**](moveto-method.md) " verarbeitet wird.                |
| **"Wvingup"**       | Wenn die Animations Methode " [**muveto**](moveto-method.md) " verarbeitet wird.                |
| **Anzeige**        | Wenn der Benutzer oder die Anwendung das Zeichen anzeigt.                                  |
| **Isch**       | Wenn die [**sprach**](speak-method.md) Animations Methode verarbeitet wird.                  |



 

### <a name="the-hearing-and-listening-states"></a>Der gehörende und die Abhör Zustände

Die Animation, die Sie dem **lauschenden** Zustand zuweisen, wird abgespielt, wenn der Benutzer den Push-to-Talk-Hot-Schlüssel für die Spracheingabe drückt. Erstellen Sie eine kurze Animation, die das Zeichen als aufmerksam ansieht, und weisen Sie Sie zu. Entsprechend definieren Sie die **Rückgabe** Animation so, dass Sie eine kurze Dauer hat, damit das Zeichen seine **hörzustands** Animation abspielt, wenn der Benutzer spricht. Eine Animation für den **hörzustand** sollte auch kurz sein und so entworfen werden, dass der Benutzer weiß, dass das Zeichen aktiv an dem, was der Benutzer sagt, lauscht. Kopftilts oder andere leichte Gesten sind geeignet. Stellen Sie mehrere **hörzustands** Animationen bereit, um eine natürliche Variabilität bereitzustellen.

### <a name="the-gesturing-states"></a>Die Status Zustände

Wenn Sie die [**gestureat**](gestureat-method.md) -Methode verwenden möchten, müssen **Sie Status Animationen** nur erstellen und zuweisen. **Status Animationen** werden wiedergegeben, wenn der Microsoft-Agent einen Aufrufen der **gestureat** -Methode verarbeitet. Wenn Sie mundüberlagerungen für Ihre **gesturenden** Zustands Animationen definieren, kann das Zeichen als Gesten sprechen.

Die Animations Dienste bestimmen den Speicherort des Zeichens und seine Beziehung zum Speicherort der in der-Methode angegebenen Koordinaten und geben eine passende Animation wieder. Die Richtung ist immer in Bezug auf das Zeichen. Beispielsweise sollte **gestureright** eine Geste für das Zeichen rechts sein.

### <a name="the-showing-and-hiding-states"></a>Die Anzeige und das Ausblenden von Zuständen

Die **Anzeige** und **das** ausblenden geben die zugewiesenen Animationen wieder, wenn der Benutzer oder die Host Anwendung anfordert, das Zeichen anzuzeigen oder auszublenden. Diese Zustände legen auch den **sichtbaren** Zustand des Zeichen Rahmens entsprechend fest. Beachten Sie beim Definieren von Animationen für diese Zustände, dass ein Zeichen an jeder Bildschirmposition angezeigt oder dort angezeigt werden kann. Da der Benutzer ein beliebiges Zeichen anzeigen oder ausblenden kann, unterstützt immer mindestens eine Animation für diese Zustände.

Animationen, die Sie dem Ansichts Zustand zuweisen, enden **in der Regel** mit einem Frame, der das neutrale Positions Bild des Zeichens enthält. Umgekehrt beginnen **Zustands Animationen** in der Regel mit der neutralen Position.  Die Anzeige **und das** Ausblenden von Zustands Animationen können jeweils einen leeren Frame enthalten, um einen Übergang vom aktuellen Zustand des Zeichens bereitzustellen.

### <a name="the-idling-states"></a>Die idlinger Zustände

Die **idlinger** Zustände sind progressiv. Die Animations Dienste beginnen mit der Verwendung der Zuweisungen der Ebene 1 für den ersten Leerlauf Zeitraum und verwenden die Animationen der Ebene 2 für das zweite. Danach wechselt der Leerlauf Zeitraum zu den zugewiesenen Animationen der Ebene 3 und verbleibt in diesem Zustand, bis er abgebrochen wird, z. b. Wenn eine neue Animations Anforderung beginnt.

Entwerfen Sie Animationen für die **idetzustände** , um den Zustand des Zeichens zu kommunizieren, aber nicht, um den Benutzer abzuleiten. Die Animationen sollten die Reaktionsfähigkeit des Zeichens auf eine feine, aber deutliche Weise widerspiegeln. Wenn Sie z. b. ein-oder blinkende aufrufen, sind Sie gute Animationen, die dem **IdlingLevel1** -Zustand zugewiesen werden. Das Lesen von Animationen funktioniert gut für den **IdlingLevel2** -Status. Der Standbymodus oder die Überwachung von Musik mit Kopfhörern sind gute Beispiele für Animationen, die dem **IdlingLevel3** -Zustand zugewiesen werden. Animationen, die viele oder große Bewegungen enthalten, eignen sich nicht gut für Animationen im Leerlauf, da Sie die Aufmerksamkeit des Benutzers zeichnen. Da **idlinger** -Zustands Animationen häufig abgespielt werden, stellen Sie mehrere **idck** State-Animationen bereit, insbesondere für die Zustände **IdlingLevel1** und **IdlingLevel2** .

Beachten Sie, dass eine Anwendung die automatische Leerlauf Verarbeitung für ein Zeichen deaktivieren und den **Leerlauf** Zustand der Zeichen verwalten kann. Die **agentidationszustände** sind so konzipiert, dass Sie alle Situationen vermeiden können, in denen das Zeichen keine Animation spielen muss. Ein Zeichen Bild, das nach einer kurzen Zeitspanne nicht geändert wird, ähnelt einer Anwendung, die für eine lange Zeit einen Warte Zeigern anzeigt, der von der Sense-Funktion und Interaktivität entfernt wird. Das Aufrechterhalten der Illusion nimmt nicht viel Zeit in Anspruch: manchmal nur ein animierter blinkt, ein sichtbare Effekt oder eine Text Verschiebung.

### <a name="the-speaking-state"></a>Der Sprech Status

Die Animations Dienste verwenden den **Sprech** Zustand, wenn eine sprach Animation für die aktuelle Animation nicht gefunden werden kann. Weisen Sie diesem Zustand eine einfache sprach Animation zu. Beispielsweise können Sie einen einzelnen Frame verwenden, der aus der neutralen Position des Zeichens mit mundüberlagerungen besteht.

### <a name="the-moving-states"></a>Die verschiebenden Zustände

Die Verschieb **enden** Zustände werden wiedergegeben, wenn eine Anwendung die Methode " [**muveto**](moveto-method.md) " aufruft Die Animations Dienste bestimmen basierend auf der aktuellen Position des Zeichens und den angegebenen Koordinaten, welche Animation abgespielt werden soll. Die Richtung der Bewegung basiert auf der Position des Zeichens. Daher sollte die Animation, die Sie der Animation " **muvingleft** " zuweisen, auf der linken Seite des Zeichens basieren. Wenn Sie die Methode " **muveto** " nicht verwenden, können Sie das Erstellen und Zuweisen einer Animation überspringen.

Das **verschieben** von Zustands Animationen sollte das Zeichen in seine Verschiebungs Position animieren. Der letzte Frame dieser Animation wird angezeigt, wenn der Rahmen des Zeichens auf dem Bildschirm verschoben wird. Es gibt keine Unterstützung für das Animieren des Zeichens, während der Rahmen verschoben wird.

### <a name="standard-animation-set"></a>Standard Animations Satz

Sie können zwar ein benutzerdefiniertes Zeichen für die Animationen entwerfen, die Sie verwenden möchten, aber der Microsoft-Agent definiert einen Standard Animations Satz. Zeichen, die dieser Definition entsprechen, können als Standard Zeichen ausgewählt werden.

In der folgenden Tabelle sind die im Standard Animations Satz enthaltenen Animationen aufgeführt. Auch wenn Sie ein benutzerdefiniertes Zeichen erstellen, können Sie die Liste als Leitfaden für das Entwerfen Ihrer eigenen Zeichen verwenden. Zeichen, die den Standard Animations Satz unterstützen, müssen mindestens die folgenden Animationen unterstützen.



| Animation                        | Verwendungs Beispiel                                                                                           | Beispiel Animation                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bestätigen**                  | Wenn das Zeichen die Anforderung des Benutzers bestätigt.                                                      | Zeichen Knoten oder blinkt "OK" Handgesten. Beachten Sie, dass diese Animation das Zeichen an seine neutrale Position zurückgeben soll.<br/>                                                                                  |
| **Warnung**<sup>1, 2</sup>          | , Wenn das Zeichen auf Anweisungen wartet, die in der Regel abgespielt werden, nachdem der Benutzer den Empfangsmodus eingeschaltet hat. | Das Zeichen steht vor, atmet und blinkende gelegentlich, aber es wird eine klare Anweisung erwartet.                                                                                                                             |
| **Ankündigung**<sup>: 1, 2</sup>       | Wenn das Zeichen Informationen für den Benutzer gefunden hat.                                                   | Zeichen Gesten durch das anwecken von Augenbrauen und Hand oder öffnet einen Umschlag.                                                                                                                                                  |
| **Blink**                        | Wenn das Zeichen in der Sprache oder im Leerlauf abgeschlossen ist.                                                            | Das Zeichen gibt natürlich die Augen.                                                                                                                                                                                       |
| **Verwirrt**<sup>1, 2</sup>       | Wenn das Zeichen nicht weiß, was zu tun ist.                                                        | Das Zeichen ist in den Kopf.                                                                                                                                                                                              |
| **Gratuliere**<sup>1, 2</sup>   | Wenn das Zeichen oder der Benutzer eine Aufgabe abgeschlossen hat (eine stärkere Form der **Bestätigungs** Animation).          | Das Zeichen führt eine glücklerbewegung durch und vermittelt "yes!"                                                                                                                                                              |
| **Ablehnen**<sup>1, 2</sup>        | , Wenn das Zeichen die Anforderung des Benutzers nicht oder ablehnt.                                             | Der Zeichen Kopf schüttelt den Kopf und stellt "No can do."                                                                                                                                                                            |
| **DoMagic1**                     | Das Zeichen wird vorbereitet, um etwas anzuzeigen.                                                                 | Zeichen Wellen (Hände oder Wand Zeichen).                                                                                                                                                                                         |
| **DoMagic2**                     | Zeichen schließt die Anzeige von etwas ab.                                                                | Zeichen schließt die magische Bewegung ab.                                                                                                                                                                                     |
| **Dontrecognize**<sup>1, 2</sup>  | , Wenn das Zeichen die Anforderung des Benutzers nicht erkannt hat.                                                  | Das Zeichen ist Hand an Ohr.                                                                                                                                                                                           |
| **Erläuterung**<sup>1, 2</sup>        | Wenn das Zeichen etwas für den Benutzer erläutert.                                                       | Zeichen Gesten, als ob etwas erläutert wird.                                                                                                                                                                         |
| **Gesturedown**:<sup>1, 2</sup>    | Wenn das Zeichen auf etwas darunter verweisen muss.                                                 | Zeichen Punkte nach unten.                                                                                                                                                                                                 |
| **Gestureleft**<sup>1, 2</sup>    | Wenn das Zeichen auf der linken Seite auf etwas verweisen muss.                                              | Zeichen Punkte mit Links oder Symbolen in einem Pfeil, der nach links zeigt.                                                                                                                                                 |
| **Gestureright**<sup>1, 2</sup>   | Wenn das Zeichen auf etwas rechts zeigen muss.                                             | Zeichen Punkte mit der rechten oder der Symbole in einem Pfeil, der nach rechts zeigt.                                                                                                                                               |
| **Gestureup**<sup>1, 2</sup>      | Wenn das Zeichen auf etwas oberhalb des Elements zeigen muss.                                                 | Zeichen Punkte.                                                                                                                                                                                                   |
| **Getatgende**                 | Wenn das Zeichen den Benutzer über etwas wichtiges Benachrichtigen muss.                                   | Zeichen Wellen werden nach oben und unten angezeigt.                                                                                                                                                                            |
| **Getattentionfort gesetzt**        | , Um die Wichtigkeit der Benachrichtigung hervorzuheben.                                                         | Eine Fortsetzung oder Wiederholung der anfänglichen Geste.                                                                                                                                                                       |
| **Getattentionreturn**           | Wenn das Zeichen die **getatvon** -oder **getattentionfortanhalteranimation** abgeschlossen hat.                | Das Zeichen wird an seine neutrale Position zurückgegeben.                                                                                                                                                                             |
| **Gruß**<sup>1, 2</sup>          | Wenn der Benutzer das System startet.                                                                      | Zeichen Lächeln und-Wellen.                                                                                                                                                                                            |
| **Hearing1**                     | Wenn das Zeichen den Anfang einer gesprochenen Äußerung hört (aktiv lauschen).                           | Das Zeichen wird vorwärts und Nods angezeigt oder zeigt die Antwort auf die Spracheingabe an. Hinweis: Diese Animation durchläuft einen Zwischenframe, der auftritt, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>   |
| **Hearing2**                     | Wenn das Zeichen den Anfang einer gesprochenen Äußerung hört (aktiv lauschen).                           | Eine andere Variation des Animations Typs, der in **Hearing1**-Hinweis verwendet wird: Diese Animation wird zu einem Zwischenframe geführt, der auftritt, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>                      |
| **Ausblenden**                         | Wenn der Benutzer das Zeichen verschließt.                                                                   | Das Zeichen entfernt sich selbst vom Bildschirm.                                                                                                                                                                                    |
| **Idle1 \_ 1**                     | Wenn das Zeichen keine Aufgabe hat und der Benutzer nicht mit dem Zeichen interagiert.                       | Das Zeichen blinkt oder sucht, verbleiben an der neutralen Position oder gibt es zurück.                                                                                                                                   |
| **Idle1 \_ 2**                     | Wenn das Zeichen keine Aufgabe hat und der Benutzer nicht mit dem Zeichen interagiert.                       | Eine andere Variation des Animations Typs, der in **Idle1 \_ 1** verwendet wird.                                                                                                                                                       |
| **Idle2 \_ 1**                     | Wenn sich das Zeichen seit einiger Zeit im Leerlauf befunden hat.                                                          | Das Zeichen, das sich in einem anderen Buch oder in der neutralen Position verbleiben soll.                                                                                                                                   |
| **Idle2 \_ 2**                     | Wenn sich das Zeichen seit einiger Zeit im Leerlauf befunden hat.                                                          | Eine andere Variation des Animations Typs, der in **Idle2 \_ 1** verwendet wird.                                                                                                                                                       |
| **Idle3 \_ 1**                     | Wenn sich das Zeichen seit längerer Zeit im Leerlauf befunden hat.                                                        | Zeichen.                                                                                                                                                                                                       |
| **Idle3 \_ 2**                     | Wenn sich das Zeichen seit längerer Zeit im Leerlauf befunden hat.                                                        | Das Zeichen wird auf dem Kopfhörer zum lauschen auf Musik angezeigt. Hinweis: Diese Animation durchläuft einen Zwischenframe, der auftritt, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>                          |
| **Suche**                     | Wenn das Zeichen nach unten suchen muss.                                                                   | Das Zeichen wird durchsucht.                                                                                                                                                                                                  |
| **Lookleft**                     | , Wenn das Zeichen nach links aussehen muss.                                                                   | Das Zeichen wird links angezeigt.                                                                                                                                                                                           |
| **Lookright**                    | Wenn das Zeichen nach rechts aussehen muss.                                                                  | Das Zeichen wird auf der rechten Seite angezeigt.                                                                                                                                                                                          |
| **Suche**                       | Wenn das Zeichen gesucht werden muss.                                                                     | Das Zeichen wird nachgeschlagen.                                                                                                                                                                                                    |
| **Nach unten**                     | Wenn das Zeichen den Vorgang nach unten vorbereitet.                                                                | Zeichen Übergänge zu einer durch-/ablaufzeilen-Position.                                                                                                                                                               |
| **"Muveleft"**                     | Wenn das Zeichen auf das Verschieben nach links vorbereitet wird.                                                                | Zeichen Übergänge zu einer über-/Schreib-Left-Position.                                                                                                                                                               |
| **Überprüfen**                    | Wenn das Zeichen auf die Verschiebung nach rechts vorbereitet wird.                                                               | Zeichen Übergänge in eine nach-/Schreib-right-Position.                                                                                                                                                              |
| **MoveUp**                       | Wenn sich das Zeichen auf einen aufwärts Pfeil vorbereitet.                                                                  | Zeichen Übergänge zu einer über-/Einfügeposition.                                                                                                                                                                 |
| **Zufrieden** mit <sup>1, 2</sup>        | Wenn das Zeichen mit der Anforderung oder der Auswahl des Benutzers zufrieden ist.                                         | Zeichen Lächeln.                                                                                                                                                                                                      |
| **Prozess**                      | Wenn das Zeichen einen Typ generischer Aufgaben ausführt.                                                   | Zeichen drückt Schaltflächen oder verwendet einen Tooltyp.                                                                                                                                                                   |
| **Verarbeitung**                   | Wenn das Zeichen mit der Arbeit an einer generischen Aufgabe ausgelastet ist.                                                    | Zeichen Schreiber im Papierblatt oder verwendet einen Tooltyp. Hinweis: Diese Animation durchläuft einen Zwischenframe, der auftritt, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>                      |
| **Lesen**                         | Wenn das Zeichen etwas für den Benutzer liest.                                                          | Das Zeichen zeigt Buch oder Papier, Lesevorgänge an und zeigt den Benutzer an.                                                                                                                                                       |
| **Fortsetzung**                | Wenn das Zeichen dem Benutzer weiter gelesen wird.                                                            | Das Zeichen wird erneut gelesen, und anschließend wird der Benutzer angezeigt.                                                                                                                                                                        |
| **"Read Return"**                   | Wenn das Zeichen die **Lese** -oder die **fortgesetzte** Animation abschließt.                                | Das Zeichen wird an seine neutrale Position zurückgegeben.                                                                                                                                                                             |
| **Lektüre**                      | Wenn das Zeichen etwas liest, aber keine Eingaben akzeptieren kann.                                              | Lesezeichen aus einem Papierblatt. Hinweis: Diese Animation wird zu einigen Zwischenframes durchlaufen, die auftreten, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>                                           |
| **Restpose**                     | Wenn das Zeichen von seiner neutralen Position aus spricht.                                                     | Das Zeichen steht mit gelocktem, aber aufmerksamer Zustand.                                                                                                                                                                   |
| **Traurig**<sup>1, 2</sup>            | Wenn das Zeichen mit der Auswahl des Benutzers enttäuscht ist.                                               | Das Zeichen ist Frowns oder wird enttäuscht angezeigt.                                                                                                                                                                                |
| **Suche**                       | Wenn Zeichen nach etwas sucht.                                                                   | Das Zeichen wird durch die Datei-oder einen anderen Container durchsucht, der nach etwas sucht.                                                                                                                                       |
| **Suchen**                    | Wenn das Zeichen nach benutzerdefinierten Informationen sucht.                                              | Das Zeichen wird durch die Datei-oder einen anderen Container durchsucht, der nach etwas sucht. Hinweis: Diese Animation wird zu einigen Zwischenframes durchlaufen, die auftreten, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/> |
| **Anzeigen**                         | Wenn das Zeichen startet oder nach dem aufgerufenen zurückgegeben wird.                                            | Das Zeichen wird auf dem Bildschirm nach oben oder auf dem Bildschirm angezeigt.                                                                                                                                                    |
| **Startabhör**<sup>1, 2</sup> | Wenn das Zeichen lauscht.                                                                         | Das Zeichen legt die Hand in den Hand.                                                                                                                                                                                            |
| **Stopp** Überwachung:<sup>1, 2</sup>  | Wenn das Zeichen nicht mehr lauscht.                                                                      | Mit dem Zeichen werden die Hände in den Hand Zeiger                                                                                                                                                                                        |
| **Vorschlagen**<sup>1, 2</sup>        | Wenn das Zeichen einen Tipp oder einen Vorschlag für den Benutzer enthält.                                                 | Glühbirne wird neben Zeichen angezeigt.                                                                                                                                                                                  |
| **Überrascht**<sup>: 1, 2</sup>      | Wenn das Zeichen durch die Aktion oder Auswahl des Benutzers überrascht wird.                                          | Zeichen wivergrößert Augen, öffnet den Mund.                                                                                                                                                                                    |
| **Nach** Frage <sup>1, 2</sup>          | Wenn das Zeichen etwas denkt.                                                          | Das Zeichen wird nach oben und ist Hand an Head.                                                                                                                                                                             |
| **Unsicher**<sup>: 1, 2</sup>      | Wenn das Zeichen erforderlich ist, muss der Benutzer eine Anforderung bestätigen.                                                  | Das Zeichen sieht Quiz, vermittelt ("sind Sie sicher?")                                                                                                                                                                   |
| **Wave**<sup>1, 2</sup>           | Wenn sich der Benutzer entscheidet, den Server oder das System herunterzufahren.                                                 | Zeichen Wellen "Good-Bye" oder "Hello".                                                                                                                                                                                     |
| **Schreiben**                        | Wenn das Zeichen Anweisungen vom Benutzer abhört.                                          | Das Zeichen zeigt Papier und Schreibvorgänge an und zeigt den Benutzer an.                                                                                                                                                              |
| **Write-Vorgang fortgesetzt**               | Wenn das Zeichen weiterhin Anweisungen vom Benutzer überwacht.                                   | Zeichen Schreibvorgänge auf einem Papierblatt und Rückblicke auf den Benutzer.                                                                                                                                                           |
| **Beschreibeturn**                  | Wenn das Zeichen die **Write** -oder Write- **Fortsetzung** -Animation abgeschlossen hat.                              | Das Zeichen wird an seine neutrale Position zurückgegeben.                                                                                                                                                                             |
| **Lassungs**                      | Wenn das Zeichen Informationen für den Benutzer ausgibt.                                                  | Zeichen Schreibvorgänge im Papierblatt. Hinweis: Diese Animation wird durchlaufen.<br/>                                                                                                                                             |



 

  Animation erfordert Mund Überlagerungen und einen definierten sprechenden Frame.

  Animation erfordert eine zugewiesene Return-Animation, die entweder auf der Beendigungs Verzweigung oder einer expliziten Rückgabe Animation basiert.

Außerdem muss ein Zeichen über die folgenden Zustands Zuweisungen verfügen.



| State          | Erforderliche Animationen                           |
|----------------|-----------------------------------------------|
| Gesturingdown  | Gesturedown                                   |
| Gesturingleft  | Gestureleft                                   |
| Gesturingright | Gestureright                                  |
| Gesturingup    | Gestureup                                     |
| Hörvermögen        | Hearing1, Hearing2                            |
| Zieher         | Ausblenden                                          |
| IdlingLevel1   | Blink, Idle1 \_ 1, Idle1 \_ 2                     |
| IdlingLevel2   | Blink, Idle1 \_ 1, Idle1 \_ 2, Idle2 \_ 1, Idle2 \_ 2 |
| IdlingLevel3   | Idle3 \_ 1, Idle3 \_ 2                            |
| Raum      | Warnung                                         |
| "Wvingdown"     | Nach unten                                      |
| "Wvingleft"     | "Muveleft"                                      |
| "Wvingright"    | Überprüfen                                     |
| "Wvingup"       | MoveUp                                        |
| Anzeige        | Anzeigen                                          |
| Isch       | Restpose                                      |



 

 

 






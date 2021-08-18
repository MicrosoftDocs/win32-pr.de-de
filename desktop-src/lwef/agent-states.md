---
title: Agent-Zustände
description: Agent-Zustände
ms.assetid: 8c3c5b12-81af-4ba5-b834-9f0a7ff5d075
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbfb927cbe9ad703e733caa827df7c5a63bac67b93d49edbb8f59884c89b6ee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976800"
---
# <a name="agent-states"></a>Agent-Zustände

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Die Microsoft Agent-Animationsdienste geben automatisch bestimmte Animationen für Sie wieder. Wenn Sie beispielsweise die Befehle [**MoveTo**](moveto-method.md) oder [**GestureAt**](gestureat-method.md) verwenden, geben die Animationsdienste eine entsprechende Animation wieder. Entsprechend geben die Dienste nach dem Leerlauf-Time out automatisch Animationen wieder. Um diese Zustände zu unterstützen, können Sie entsprechende Animationen definieren und diese dann den Zuzuständen zuweisen. Sie können weiterhin jede Animation wiederspielen, die Sie direkt mithilfe der [**Play-Methode**](play-method.md) definieren, auch wenn Sie sie einem Zustand zuweisen.

Sie können mehrere Animationen demselben Zustand zuweisen, und die Animationsdienste wählen nach dem Zufallsprinzip eine Ihrer Animationen aus. Dadurch kann ihr Zeichen eine viel natürlichere Vielfalt im Verhalten zeigen.

Obwohl Animationen, die Sie Zuzuständen zuweisen, Verzweigungsframes enthalten können, vermeiden Sie Schleifenanimationen (Animationen, die für immer verzweigt sind). Andernfalls müssen Sie die [**Stop-Methode verwenden,**](play-method.md) bevor Sie eine andere Animation wieder geben können.

Es ist wichtig, mindestens eine Animation für jeden Zustand zu definieren und zu zuweisen, der für das Zeichen auftritt. Wenn Sie diese Animationen und Zustandszuweisungen nicht zur Verfügung haben, scheint sich Ihr Zeichen für den Benutzer möglicherweise nicht ordnungsgemäß zu verhalten. Wenn jedoch für ein bestimmtes Zeichen kein Zustand auftritt, müssen Sie diesem Zustand keine Animation zuweisen. Wenn Ihre Hostanwendung beispielsweise nie die [**MoveTo-Methode**](moveto-method.md) aufruft, können Sie das Erstellen und Zuweisen von Animationen zum **Verschieben** des Zustands überspringen.



| State              | Beispiel für die Verwendung                                                                         |
|--------------------|----------------------------------------------------------------------------------------|
| **GesturingDown**  | Wenn die [**GestureAt-Animationsmethode**](gestureat-method.md) verarbeitet wird.          |
| **GesturingLeft**  | Wenn die [**GestureAt-Animationsmethode**](gestureat-method.md) verarbeitet wird.          |
| **GesturingRight** | Wenn die [**GestureAt-Animationsmethode**](gestureat-method.md) verarbeitet wird.          |
| **GesturingUp**    | Wenn die [**GestureAt-Animationsmethode**](gestureat-method.md) verarbeitet wird.          |
| **Hörvermögen**        | Wenn der Anfang der gesprochenen Eingabe erkannt wird.                                        |
| **Versteckt**         | Wenn der Benutzer oder die Anwendung das Zeichen ausblendet.                                  |
| **IdlingLevel1**   | Wenn das Zeichen den **Idlingzustand** beginnt.                                        |
| **IdlingLevel2**   | Wenn das Zeichen den zweiten Zustand der **Idlingebene** beginnt.                           |
| **IdlingLevel3**   | Wenn das Zeichen den endgültigen Zustand der **Idlingebene** beginnt.                            |
| **Hören**      | Wenn das Zeichen mit dem Lauschen beginnt (der Benutzer drückt zuerst die hot-Taste der Spracheingabe). |
| **MovingDown**     | Wenn die [**MoveTo-Animationsmethode**](moveto-method.md) verarbeitet wird.                |
| **MovingLeft**     | Wenn die [**MoveTo-Animationsmethode**](moveto-method.md) verarbeitet wird.                |
| **MovingRight**    | Wenn die [**MoveTo-Animationsmethode**](moveto-method.md) verarbeitet wird.                |
| **MovingUp**       | Wenn die [**MoveTo-Animationsmethode**](moveto-method.md) verarbeitet wird.                |
| **Anzeige**        | Wenn der Benutzer oder die Anwendung das Zeichen zeigt.                                  |
| **Sprechen**       | Wenn die [**Speak-Animationsmethode**](speak-method.md) verarbeitet wird.                  |



 

### <a name="the-hearing-and-listening-states"></a>Die Zustände "Hören" und "Lauschen"

Die Animation, die Sie dem **Zustand** Lauschen zuweisen, wird abspielt, wenn der Benutzer die Push-to-Talk-Taste für die Spracheingabe drückt. Erstellen Sie eine kurze Animation, und weisen Sie sie zu, damit das Zeichen lebsam ausschaut. Definieren Sie auf ähnliche Weise die **Return-Animation** so, dass sie eine kurze Dauer hat, sodass das Zeichen seine **Animation** zum Hörzustand wiederträgt, wenn der Benutzer spricht. Eine **Animation zum** Hörzustand sollte ebenfalls kurz sein und den Benutzer darüber informieren, dass das Zeichen aktiv auf das lausst, was der Benutzer sagt. Kopfneigungen oder andere leichte Gesten sind geeignet. Um natürliche Variabilität zu ermöglichen, stellen Sie mehrere Animationen des **Hörzustands** zur Verfügung.

### <a name="the-gesturing-states"></a>Die Gesturierungszustände

**Gesturing-Zustandsanimationen** müssen nur erstellt und zugewiesen werden, wenn Sie die [**GestureAt-Methode verwenden**](gestureat-method.md) möchten. **Gesturingzustandsanimationen** werden wieder verwendet, wenn Microsoft Agent einen Aufruf der **GestureAt-Methode** verarbeitet. Wenn Sie für **Gesturing-Zustandsanimationen** überlagerte Überlagerungen definieren, kann das Zeichen während der Gesten sprechen.

Die Animationsdienste bestimmen die Position des Zeichens und seine Beziehung zur Position der in der -Methode angegebenen Koordinaten und geben eine entsprechende Animation wieder. Die Gesturierungsrichtung ist immer in Bezug auf das Zeichen; Beispielsweise sollte **GestureRight** eine Geste rechts vom Zeichen sein.

### <a name="the-showing-and-hiding-states"></a>Die Ein- und Ausblenden-Zustände

Der **Ein-** **und Ausblenden-Zustände** geben die zugewiesenen Animationen wieder, wenn der Benutzer oder die Hostanwendung das Ein- oder Ausblenden des Zeichens an fordert. Diese Zustände legen auch den Sichtbar-Zustand des **Zeichenrahmens entsprechend** fest. Beachten Sie beim Definieren von Animationen für diese Zustände, dass ein Zeichen an jeder Bildschirmposition angezeigt oder umranden kann. Da der Benutzer ein beliebiges Zeichen ein- oder ausblenden kann, unterstützt immer mindestens eine Animation für diese Zustände.

Animationen, die Sie dem **Anzeigezustand** zuweisen, enden in der Regel mit einem Frame, der das neutrale Positionsbild des Zeichens enthält. Umgekehrt beginnen **Hiding** State-Animationen in der Regel mit der neutralen Position. **Ein-** **und Ausblenden von** Zustandsanimationen können einen leeren Frame am Anfang bzw. Ende enthalten, um einen Übergang vom aktuellen Zustand des Zeichens zu ermöglichen.

### <a name="the-idling-states"></a>Die Leerungszustände

Die **Idlingzustände** sind progressiv. Die Animationsdienste beginnen mit der Verwendung der Zuweisungen der Ebene 1 für den ersten Leerlaufzeitraum und verwenden die Animationen der Ebene 2 für die zweite. Danach geht der Leerlaufzyklus zu den zugewiesenen Animationen der Ebene 3 über und verbleibt in diesem Zustand, bis er abgebrochen wird, z. B. wenn eine neue Animationsanforderung beginnt.

Entwerfen Sie Animationen für **die Idlingzustände,** um den Zustand des Zeichens zu kommunizieren, aber nicht, um den Benutzer abzulenken. Die Animationen sollten die Reaktionsfähigkeit des Zeichens auf subtile, aber klare Weise widerspiegeln. Beispielsweise sind das Um- oder Blinken gute Animationen, die dem **IdlingLevel1-Zustand zugewiesen werden** können. Das Lesen von Animationen funktioniert gut für den **IdlingLevel2-Zustand.** Das Ein-/Aus- oder Lauschen auf Musik mit Füllungen sind gute Beispiele für Animationen, die dem **IdlingLevel3-Zustand zugewiesen werden** sollen. Animationen, die viele oder große Bewegungen enthalten, eignen sich nicht gut für Animationen im Leerlauf, da sie die Aufmerksamkeit des Benutzers auf sich ziehen. Da  Idlingzustandsanimationen häufig abgespielt werden, stellen Sie mehrere **Idlingzustandsanimationen** zur Verfügung, insbesondere für die Zustände **IdlingLevel1** und **IdlingLevel2.**

Beachten Sie, dass eine Anwendung die automatische Leerlaufverarbeitung für ein Zeichen deaktivieren und den **Idlingzustand** des Zeichens selbst verwalten kann. Die Agent **Idling-Zustände** sind so konzipiert, dass Sie jede Situation vermeiden können, in der das Zeichen keine Animation wieder zu spielen hat. Ein Zeichenbild, das sich nach kurzer Zeit nicht ändert, ist wie eine Anwendung, die einen Wartezeiger für einen längeren Zeitraum zeigt, was das Gefühl der Erwartbarkeit und Interaktivität abwandelt. Die Aufrechterhaltung der Täuschung dauert nicht viel: manchmal nur ein animiertes Blinken, sichtbares Licht oder Eine-Körper-Verschiebung.

### <a name="the-speaking-state"></a>Der Sprechzustand

Die Animationsdienste verwenden den **Sprechzustand,** wenn eine Sprechanimation für die aktuelle Animation nicht gefunden werden kann. Weisen Sie diesem Zustand eine einfache Sprechanimation zu. Beispielsweise können Sie einen einzelnen Frame verwenden, der aus der neutralen Position des Zeichens mit Überlagerungen besteht.

### <a name="the-moving-states"></a>Die sich bewegenden Zustände

Die  Move-Zustände werden abspielt, wenn eine Anwendung die [**MoveTo-Methode**](moveto-method.md) aufruft. Die Animationsdienste bestimmen basierend auf der aktuellen Position des Zeichens und den angegebenen Koordinaten, welche Animation abspielt werden soll. Die Bewegungsrichtung basiert auf der Position des Zeichens. Daher sollte die Animation, die Sie der **MovingLeft-Animation** zuweisen, auf der linken Seite des Zeichens basieren. Wenn Sie die **MoveTo-Methode** nicht verwenden, können Sie das Erstellen und Zuweisen einer Animation überspringen.

**Bewegende** Zustandsanimationen sollten das Zeichen an seine bewegende Position animieren. Der letzte Frame dieser Animation wird angezeigt, wenn der Rahmen des Zeichens auf dem Bildschirm verschoben wird. Es gibt keine Unterstützung für das Animieren des Zeichens, während sich der Frame bewegt.

### <a name="standard-animation-set"></a>Standardanimationssatz

Sie können zwar ein benutzerdefiniertes Zeichen so entwerfen, dass es die Animationen enthält, die Sie verwenden möchten, microsoft-Agent definiert jedoch einen Standardanimationssatz. Zeichen, die dieser Definition entsprechen, können als Standardzeichen ausgewählt werden.

In der folgenden Tabelle sind die Animationen aufgeführt, die im Standardanimationssatz enthalten sind. Auch wenn Sie ein benutzerdefiniertes Zeichen erstellen, sollten Sie die Liste als Leitfaden zum Entwerfen eigener Zeichen verwenden. Zeichen, die den Standardanimationssatz unterstützen, müssen mindestens die folgenden Animationen unterstützen.



| Animation                        | Beispiel für die Verwendung                                                                                           | Beispielanimation                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bestätigen**                  | Wenn das Zeichen die Anforderung des Benutzers bestätigt.                                                      | Zeichen nods or flashes "OK"-Handgeste. Beachten Sie, dass diese Animation das Zeichen an seine neutrale Position zurückgeben sollte.<br/>                                                                                  |
| **Warnung**<sup>1,2</sup>          | Wenn das Zeichen auf Anweisungen wartet, wird es in der Regel wiedergegeben, nachdem der Benutzer den Überwachungsmodus aktiviert hat. | Gesichter mit Zeichen vorn, mäßig, hin und wieder blinkend, aber deutlich auf Anweisung wartend.                                                                                                                             |
| **Ankündigung:**<sup>1,2</sup>       | Wenn das Zeichen Informationen für den Benutzer gefunden hat.                                                   | Zeichengesten durch Auslösen von Augen und Hand oder Öffnen eines Umschlags.                                                                                                                                                  |
| **Blink**                        | Wenn das Zeichen mit dem Sprechen oder Leerlauf fertig ist.                                                            | Das Zeichen blinkt auf natürliche Weise mit den Augen.                                                                                                                                                                                       |
| **Verwechselt**<sup>1,2</sup>       | Wenn das Zeichen nicht versteht, was zu tun ist.                                                        | Der Kopf des Zeichens wird ab scratcht.                                                                                                                                                                                              |
| <sup>1,2</sup>   | Wenn das Zeichen oder der Benutzer eine Aufgabe abschließt (eine stärkere Form der **Acknowledge-Animation).**          | Character führt eine Glückwunschgeste aus und übermittelt "Ja!"                                                                                                                                                              |
| **Ablehnen**<sup>1,2</sup>        | Wenn das Zeichen die Anforderung des Benutzers nicht erfüllen oder ablehnen kann.                                             | Das Zeichen schüttelt den Kopf, vermittelt "no can do".                                                                                                                                                                            |
| **DoMagic1**                     | Zeichen bereitet die Anzeige von etwas vor.                                                                 | Zeichenwellenhand oder -stab.                                                                                                                                                                                         |
| **DoMagic2**                     | Das Zeichen schließt die Anzeige von etwas ab.                                                                | Das Zeichen schließt die magische Geste ab.                                                                                                                                                                                     |
| **DontRecognize**<sup>1,2</sup>  | Wenn das Zeichen die Anforderung des Benutzers nicht erkannt hat.                                                  | Das Zeichen hält Hand an Gehör.                                                                                                                                                                                           |
| **Erläuterung**<sup>1,2</sup>        | Wenn das Zeichen dem Benutzer etwas erklärt.                                                       | Zeichengesten, als ob etwas erklärt würde.                                                                                                                                                                         |
| **GestureDown**<sup>1,2</sup>    | Wenn das Zeichen auf etwas darunter zeigen muss.                                                 | Zeichen zeigt nach unten.                                                                                                                                                                                                 |
| **GestureLeft**<sup>1,2</sup>    | Wenn das Zeichen auf etwas links zeigen muss.                                              | Zeichenpunkte mit der linken Hand oder wandeln sich in einen Pfeil nach links um.                                                                                                                                                 |
| **GestureRight**<sup>1,2</sup>   | Wenn das Zeichen auf etwas auf seiner rechten Seite zeigen muss.                                             | Zeichenpunkte mit der rechten Hand oder wandeln sich in einen Pfeil um, der nach rechts zeigt.                                                                                                                                               |
| **GestureUp**<sup>1,2</sup>      | Wenn das Zeichen auf etwas darüber zeigen muss.                                                 | Zeichen zeigt nach oben.                                                                                                                                                                                                   |
| **GetAttention**                 | Wenn das Zeichen den Benutzer über etwas Wichtiges benachrichtigen muss.                                   | Zeichen winken Hände oder springt nach oben und unten.                                                                                                                                                                            |
| **GetAttentionContinued**        | Um die Wichtigkeit der Benachrichtigung hervorzuheben.                                                         | Eine Fortsetzung oder Wiederholung der anfänglichen Geste.                                                                                                                                                                       |
| **GetAttentionReturn**           | Wenn das Zeichen die **Animation GetAttention** oder **GetAttentionContinued** abgeschlossen hat.                | Das Zeichen kehrt zu seiner neutralen Position zurück.                                                                                                                                                                             |
| **Greet**<sup>1,2</sup>          | Wenn der Benutzer das System startet.                                                                      | Zeichenlächeln und Wellen.                                                                                                                                                                                            |
| **Hörvermögen1**                     | Wenn das Zeichen den Anfang einer gesprochenen Äußerung (aktiv lauscht) anhört.                           | Das Zeichen lehnt sich nach vorn und nodiert, oder der Kopf zeigt die Antwort auf die Spracheingabe an. Hinweis: Diese Animation wechselt zu einem Zwischenframe, der auftritt, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>   |
| **Hörvermögen2**                     | Wenn das Zeichen den Anfang einer gesprochenen Äußerung (aktiv lauscht) anhört.                           | Eine weitere Variante des Animationstyps, der in **Hearing1** verwendet wird Hinweis: Diese Animation schleift zu einem Zwischenframe, der auftritt, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>                      |
| **Ausblenden**                         | Wenn der Benutzer das Zeichen verwarnt.                                                                   | Das Zeichen entfernt sich selbst vom Bildschirm.                                                                                                                                                                                    |
| **Idle1 \_ 1**                     | Wenn das Zeichen keine Aufgabe hat und der Benutzer nicht mit dem Zeichen interagiert.                       | Das Zeichen blinkt oder sieht sich um, verbleibt in der neutralen Position oder kehrt zur neutralen Position zurück.                                                                                                                                   |
| **Idle1 \_ 2**                     | Wenn das Zeichen keine Aufgabe hat und der Benutzer nicht mit dem Zeichen interagiert.                       | Eine weitere Variante des Animationstyps, der in **Idle1 \_ 1** verwendet wird.                                                                                                                                                       |
| **Idle2 \_ 1**                     | Wenn sich das Zeichen seit einiger Zeit im Leerlauf befindet.                                                          | Zeichen yawns or reads magazine remaining in or returning to the neutral position.                                                                                                                                   |
| **Idle2 \_ 2**                     | Wenn sich das Zeichen seit einiger Zeit im Leerlauf befindet.                                                          | Eine weitere Variante des Animationstyps, der in **Idle2 \_ 1** verwendet wird.                                                                                                                                                       |
| **Idle3 \_ 1**                     | Wenn sich das Zeichen über einen längeren Zeitraum im Leerlauf befindet.                                                        | Zeichen-Gähns.                                                                                                                                                                                                       |
| **Idle3 \_ 2**                     | Wenn sich das Zeichen über einen längeren Zeitraum im Leerlauf befindet.                                                        | Das Zeichen wird in den Standbymodus versetzt oder eingeschaltet, um Musik zu hören. Hinweis: Diese Animation wechselt zu einem Zwischenframe, der auftritt, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>                          |
| **LookDown**                     | Wenn das Zeichen nach unten suchen muss.                                                                   | Zeichen sucht nach unten.                                                                                                                                                                                                  |
| **LookLeft**                     | Wenn das Zeichen nach links aussehen muss.                                                                   | Das Zeichen sieht nach links.                                                                                                                                                                                           |
| **LookRight**                    | Wenn das Zeichen richtig aussehen muss.                                                                  | Das Zeichen sucht nach rechts.                                                                                                                                                                                          |
| **Lookup**                       | Wenn das Zeichen gesucht werden muss.                                                                     | Das Zeichen sucht.                                                                                                                                                                                                    |
| **Movedown**                     | Wenn sich das Zeichen auf den Wechsel nach unten vorbereitet.                                                                | Zeichenübergänge zu einer Lauf-/Abstiegsposition.                                                                                                                                                               |
| **MoveLeft**                     | Wenn sich das Zeichen darauf vorbereitet, nach links zu verschieben.                                                                | Zeichenübergänge zu einer zu fußenden/linken Position.                                                                                                                                                               |
| **MoveRight**                    | Wenn sich das Zeichen auf die Verschiebung nach rechts vorbereitet.                                                               | Zeichenübergänge zu einer lauf- bzw. geraden rechten Position.                                                                                                                                                              |
| **MoveUp**                       | Wenn sich das Zeichen darauf vorbereitet, nach oben zu wechseln.                                                                  | Zeichenübergänge zu einer Lauf-/Auflaufposition.                                                                                                                                                                 |
| <sup>1,2</sup>        | Wenn das Zeichen mit der Anforderung oder Auswahl des Benutzers zufrieden ist.                                         | Zeichen lächelt.                                                                                                                                                                                                      |
| **Process**                      | Wenn das Zeichen einen generischen Task ausführt.                                                   | Zeichen drückt Schaltflächen oder verwendet eine Art von Tool.                                                                                                                                                                   |
| **Verarbeitung**                   | Wenn das Zeichen mit der Arbeit an einer generischen Aufgabe beschäftigt ist.                                                    | Zeichenkätzchen auf Papierauflage oder verwenden eine Art von Tool. Hinweis: Diese Animation wechselt zu einem Zwischenframe, der auftritt, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>                      |
| **Lesen**                         | Wenn das Zeichen etwas für den Benutzer liest.                                                          | Zeichen zeigt Buch oder Papier an, liest und blickt auf den Benutzer zurück.                                                                                                                                                       |
| **ReadContinued**                | Wenn das Zeichen dem Benutzer weiter liest.                                                            | Das Zeichen liest erneut und blickt dann auf den Benutzer zurück.                                                                                                                                                                        |
| **ReadReturn**                   | Wenn das Zeichen die **Read-** oder **ReadContinued-Animation** abschließt.                                | Das Zeichen kehrt zu seiner neutralen Position zurück.                                                                                                                                                                             |
| **Aktuell gelesen**                      | Wenn das Zeichen etwas liest, aber keine Eingaben akzeptieren kann.                                              | Zeichenlesezeichen aus einem Papier. Hinweis: Diese Animation schleift einige Zwischenframes, die auftreten, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/>                                           |
| **RestPose**                     | Wenn das Zeichen von seiner neutralen Position aus spricht.                                                     | Zeichen stehen mit gelockerten, aber heiteren Positionen.                                                                                                                                                                   |
| **Leider**<sup>1,2</sup>            | Wenn das Zeichen mit der Auswahl des Benutzers zufrieden ist.                                               | Das Zeichen stirnrunzelt oder sieht ungern aus.                                                                                                                                                                                |
| **Suche**                       | Wenn zeichen nach etwas sucht.                                                                   | Zeichen wird durch den Dateischubladen oder einen anderen Container gemischt, der nach etwas sucht.                                                                                                                                       |
| **Suche**                    | Wenn das Zeichen nach benutzerdefinierten Informationen sucht.                                              | Zeichen wird durch den Dateischubladen oder einen anderen Container gemischt, der nach etwas sucht. Hinweis: Diese Animation schleift einige Zwischenframes, die auftreten, nachdem das Zeichen an eine geeignete Position verschoben wurde.<br/> |
| **Anzeigen**                         | Wenn das Zeichen gestartet oder zurückgegeben wird, nachdem es abgeschwenkt wurde.                                            | Das Zeichen wird in einem Feuerpuff angezeigt, strahlt ein oder führt auf dem Bildschirm.                                                                                                                                                    |
| **StartListening**<sup>1,2</sup> | Wenn das Zeichen lauscht.                                                                         | Das Zeichen legt die Hand auf das Gehör.                                                                                                                                                                                            |
| **StopListening**<sup>1,2</sup>  | Wenn das Zeichen nicht mehr lauscht.                                                                      | Mit dem Zeichen werden Hände über die Hand gelegt.                                                                                                                                                                                        |
| **Vorschlag**<sup>1,2</sup>        | Wenn das Zeichen einen Tipp oder Vorschlag für den Benutzer enthält.                                                 | Die Glühbirne wird neben dem Zeichen angezeigt.                                                                                                                                                                                  |
| **Überraschend**<sup>1,2</sup>      | Wenn das Zeichen durch die Aktion oder Auswahl des Benutzers überraschend ist.                                          | Das Zeichen erweitert die Augen, öffnet die Augen.                                                                                                                                                                                    |
| **Denken Sie**<sup>an 1,2</sup>          | Wenn das Zeichen an etwas denken soll.                                                          | Das Zeichen sucht nach oben und hält die Hand auf dem Kopf.                                                                                                                                                                             |
| **Unsicher**<sup>1,2</sup>      | Wenn der Benutzer für das Zeichen eine Anforderung bestätigen muss.                                                  | Character looks quizzical, conveys ("Are you sure?")                                                                                                                                                                   |
| **Wave**<sup>1,2</sup>           | Wenn der Benutzer entscheidet, den Server oder das System herunterzufahren.                                                 | Zeichenwellen good-bye oder hello.                                                                                                                                                                                     |
| **Schreiben**                        | Wenn das Zeichen auf Anweisungen des Benutzers lauscht.                                          | Das Zeichen zeigt Papier, Schreibt und blickt auf den Benutzer zurück.                                                                                                                                                              |
| **WriteContinued**               | Wenn das Zeichen weiterhin auf Anweisungen des Benutzers lauscht.                                   | Zeichen schreibt auf einem Blatt Papier und blickt auf den Benutzer zurück.                                                                                                                                                           |
| **WriteReturn**                  | Wenn das Zeichen die **Write-** oder **WriteContinued-Animation** abschließt.                              | Das Zeichen kehrt zu seiner neutralen Position zurück.                                                                                                                                                                             |
| **Schreiben**                      | Wenn das Zeichen Informationen für den Benutzer schreibt.                                                  | Zeichen-Schreibvorgänge auf Papier. Hinweis: Diese Animationsschleifen.<br/>                                                                                                                                             |



 

  Für die Animation sind Überlagerungen des Lappens und ein definierter Sprechrahmen erforderlich.

  Für die Animation ist eine zugewiesene Return-Animation erforderlich, die entweder auf deren Exitverzweigung oder auf einer expliziten Return-Animation basiert.

Darüber hinaus muss ein Zeichen die folgenden Zustandszuweisungen aufweisen.



| State          | Erforderliche Animationen                           |
|----------------|-----------------------------------------------|
| GesturingDown  | GestureDown                                   |
| GesturingLeft  | GestureLeft                                   |
| GesturingRight | GestureRight                                  |
| GesturingUp    | GestureUp                                     |
| Hörvermögen        | Hörvermögen1, Hörvermögen2                            |
| Versteckt         | Ausblenden                                          |
| IdlingLevel1   | Blink, Idle1 \_ 1, Idle1 \_ 2                     |
| IdlingLevel2   | Blink, Idle1 \_ 1, Idle1 \_ 2, Idle2 \_ 1, Idle2 \_ 2 |
| IdlingLevel3   | Idle3 \_ 1, Idle3 \_ 2                            |
| Hören      | Warnung                                         |
| MovingDown     | Movedown                                      |
| MovingLeft     | MoveLeft                                      |
| MovingRight    | MoveRight                                     |
| MovingUp       | MoveUp                                        |
| Anzeige        | Anzeigen                                          |
| Sprechen       | RestPose                                      |



 

 

 






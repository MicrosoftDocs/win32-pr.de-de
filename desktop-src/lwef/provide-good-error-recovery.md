---
title: Bereitstellen einer guten Fehlerwiederherstellung
description: Bereitstellen einer guten Fehlerwiederherstellung
ms.assetid: 48e00638-9274-49db-93ec-ed444f526441
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2abc32e1bdf6422e2d8d6422a17e0b881c6ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036213"
---
# <a name="provide-good-error-recovery"></a>Bereitstellen einer guten Fehlerwiederherstellung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Wie bei jeder gut entworfenen Oberfläche sollte der interaktive Prozess die Umstände minimieren, die zu Fehlern führen. Es ist jedoch nur selten möglich, alle Fehler zu beseitigen. Daher ist die Unterstützung einer guten Fehlerwiederherstellung wichtig, um die Zuverlässigkeit und den Interesse des Benutzers zu wahren. Im allgemeinen umfasst die Fehlerwiederherstellung das Erkennen eines Fehlers, das Ermitteln der Ursache und das Definieren einer Möglichkeit, den Fehler zu beheben. Benutzer reagieren besser auf kooperative Schnittstellen, die mit dem Benutzer zusammenarbeiten, um eine Aufgabe zu erledigen.

Der erste Schritt bei der Sprachfehler Wiederherstellung ist das Erkennen der Fehlerbedingung. Die Spracherkennung kann aufgrund einer Vielzahl von Fehlern fehlschlagen. Fehlerbedingungen können normalerweise durch ungültige Eingabe, explizite Benutzer Korrektur oder Abbruch oder Benutzer Wiederholung erkannt werden.

Ein *Ablehnungs Fehler* tritt auf, wenn die Erkennungs-Engine keine Entsprechung für das hat, was der Benutzer gesagt hat. Hintergrundrauschen oder frühe Starts sind auch Häufige Gründe für einen Erkennungs Fehler, sodass der Benutzer aufgefordert wird, einen Befehl wiederholen zu können. Dies ist häufig eine gute erste Lösung. Wenn der Ausdruck jedoch außerhalb der aktuellen aktiven Grammatik liegt, kann das Problem durch die Aufforderung des Benutzers zum erneuten formulieren der Anforderung gelöst werden. Der Unterschied bei der Formulierung kann zu einer Entsprechung mit etwas in der aktuellen Grammatik führen. Eine weitere Alternative besteht darin, die entsprechenden erwarteten Eingabeoptionen aufzulisten oder vorzuschlagen.

Eine gute Strategie für die Ablehnung der Fehlerwiederherstellung besteht darin, diese Techniken zu kombinieren, um den Benutzer wieder auf den Weg zu bringen. Beispielsweise können Sie beginnen, indem Sie auf den anfänglichen Fehler mit einem abgefragativen like "huh" reagieren. oder "was?" oder eine Handbewegung. Eine kurze Antwort erhöht die Wahrscheinlichkeit, dass die wiederholte Anweisung des Benutzers nicht fehlschlägt, da der Benutzer zu früh gesprochen hat. Bei einem wiederholten Fehler verbessert die nachfolgende Anforderung zum erneuten formulieren die Wahrscheinlichkeit, dass etwas in der gegebenen Grammatik übereinstimmt. Von hier aus können Sie durch die Bereitstellung expliziter Befehle die Wahrscheinlichkeit einer entsprechenden Entsprechung erhöhen. Dieses Verfahren wird im folgenden Beispiel veranschaulicht:



|            |                                                                            |
|------------|----------------------------------------------------------------------------|
| User:      | Ich möchte eine Pizza im Chicago-Stil mit sarvies.                             |
| Art | (Hand an Ohr) Nicht wahr?                                                         |
| User:      | Ich möchte eine Chicago-Pizza mit sarvies.                                     |
| Art | (Kopf schütteln) Bitte formulieren Sie Ihre Anforderung neu.                                 |
| User:      | Ich sagte die Chicago-Pizza mit sarvies.                                      |
| Art | Ignorieren Es tut mir leid. Erzählen Sie mir den Stil der gewünschten Pizza.                    |
| User:      | Chicago mit sarvies.                                                   |
| Art | Es ist immer noch kein Glück. So können Sie Folgendes sagen: "Chicago", "Hawaiisch" oder "Combo". |



 

Um die Fehlerbehandlung natürlicher zu gestalten, stellen Sie sicher, dass Sie bei der Reaktion auf Fehler einen gewissen Grad an zufälliger Variation angeben. Außerdem besteht eine natürliche Reaktion von Benutzern auf eine Anforderung zum Wiederholen einer Antwort darin, das Volume zu übertreiben oder zu vergrößern, wenn die Anweisung wiederholt wird. Es kann nützlich sein, den Benutzer gelegentlich und eindeutig daran zu erinnern, dass das übertreiben oder das gestiegene Volume das Erkennen von Wörtern erschwert.

Die Progressive Unterstützung sollte mehr als das Auftreten des Fehlers in die Aufmerksamkeit des Benutzers bewirken. Er sollte den Benutzer dazu bewegen, in der aktuellen Grammatik zu sprechen, indem er nachfolgend weitere informative Nachrichten bereitstellt. Schnittstellen, die zu verstehen scheinen, fördern ein hohes Maß an Zufriedenheit und Toleranz vom Benutzer.

Ersetzungs *Fehler*, bei denen die Sprach-Engine die Eingabe erkennt, aber mit dem falschen Befehl übereinstimmt, können schwieriger aufgelöst werden, da die Sprach-Engine eine passende Äußerung erkennt. Eine fehlende Übereinstimmung kann auch auftreten, wenn die Sprach-Engine überflüssige Sounds als gültige Eingabe interpretiert (auch als *Einfügefehler* bezeichnet). In diesen Fällen ist die Unterstützung des Benutzers erforderlich, um den Fehlerzustand zu identifizieren. Zu diesem Zweck können Sie wiederholen, was die Sprach-Engine zurückgegeben hat, und den Benutzer zur Bestätigung auffordern, bevor Sie fortfahren:



|            |                                                   |
|------------|---------------------------------------------------|
| User:      | Ich möchte eine Pizza im Chicago-Stil.                   |
| Art | Sagten Sie, dass Sie eine "Chicago-Style Pizza" haben?   |
| User:      | Ja.                                              |
| Art | Welche zusätzlichen Zutaten möchten Sie darauf? |
| User:      | Sarvies.                                        |
| Art | Haben Sie "sarvies" gesagt?                          |
| User:      | Ja.                                              |



 

Die Verwendung dieser Technik für jede Äußerung wird jedoch ineffizient und tiresome. Um dies zu behandeln, schränken Sie die Bestätigung auf Situationen ein, die erhebliche negative Folgen haben, oder erhöhen Sie die Komplexität der unmittelbaren Aufgabe. Wenn es für den Benutzer einfach ist, Änderungen vorzunehmen oder umzukehren, können Sie möglicherweise keine Bestätigung Ihrer Auswahl anfordern. Ebenso müssen Sie, wenn Sie die Auswahlmöglichkeiten sichtbar machen, möglicherweise keine explizite Korrektur bereitstellen. Wenn Sie z. b. ein Element aus einer Liste auswählen, ist die Überprüfung möglicherweise nicht erforderlich, da der Benutzer die Ergebnisse sehen und leicht ändern kann. Sie können auch Vertrauen und Alternative Ergebnisse verwenden, um einen Schwellenwert für die Bestätigung anzugeben. Sie können den Schwellenwert anpassen, indem Sie einen Verlauf der Aktionen des Benutzers in einer bestimmten Situation beibehalten und die Überprüfung basierend auf der konsistenten Benutzer Bestätigung eliminieren. Beachten Sie schließlich die multimodale Natur der-Schnittstelle. Die Bestätigung von der Maus oder der Tastatur ist möglicherweise auch angebracht.

Wählen Sie den Wortlaut der Bestätigungen sorgfältig aus. Beispiel: "hat Sie gesagt...?" oder "Ich denke, Sie sagten..." sind Sie besser als "möchten Sie wirklich...?" Da die ersten Ausdrücke implizieren, dass die Genauigkeit des gelesenen (Erkennungs-) Zeichen abgefragt wird, nicht dass der Benutzer möglicherweise falsch gesprochen hat.

Beachten Sie auch die Grammatik für eine Antwort. Beispielsweise generiert eine negative Antwort wahrscheinlich einen Ablehnungs Fehler, der eine zusätzliche Aufforderung erfordert, wie im folgenden Beispiel gezeigt:



|            |                          |
|------------|--------------------------|
| User:      | Ich möchte einen Pfeffer. |
| Art | Haben Sie "No Ham" gesagt?    |
| User:      | Nein, ich habe pepperoni gesagt.    |
| Art | Wie das?                     |
| User:      | Peperoni.               |



 

Wenn Sie Ihre Grammatik so ändern, dass Sie Präfixe zur Handhabung natürlicher Antworten enthält, erhöht sich die Effizienz des Wiederherstellungsprozesses, insbesondere dann, wenn der Benutzer die Überprüfungs Aufforderung nicht bestätigt. In diesem Beispiel könnte die Bestätigung in einem einzigen Schritt verarbeitet worden sein, indem die Grammatik für die "Pfeffer-" geändert wurde, indem auch "No I Said pepperoni", "I Said pepperoni" und "No pepperoni" (No pepperoni) geändert werden.

Ersetzungs Fehler können auch mithilfe der alternativen Übereinstimmungen behandelt werden, die von der Sprach-Engine als Korrektur Bestätigung zurückgegeben werden:



|           |                                                                                        |
|-----------|----------------------------------------------------------------------------------------|
| Benutzer      | Ich möchte einen Pfeffer.                                                               |
| Zeichen | (Hört "No Ham" als beste Entsprechung, "pepperoni" als erste Alternative) Haben Sie "No Ham" gesagt? |
| Benutzer      | Nein, Pepperoni.                                                                         |
| Zeichen | (Hört weiterhin "kein Ham" als beste Entsprechung, bietet aber jetzt die erste Alternative) "Pepperoni"?    |



 

Auf ähnliche Weise können Sie einen Verlauf allgemeiner Ersetzungs Fehler beibehalten. Wenn ein bestimmter Fehler häufig auftritt, sollten Sie die Alternative zum ersten Mal anbieten.

Vermeiden Sie in jeder Erkennungs Fehlersituation den Benutzer. Wenn das Zeichen vorschlägt oder sogar impliziert, dass der Benutzer die Verantwortung trägt oder das Zeichen nicht gleichgültig ist, wird der Benutzer möglicherweise beleidigt. Wählen Sie hier auch sorgfältig die Formulierungen aus, die die Verantwortung explizit annehmen, für die Situation geeignet sind, und verwenden Sie Vielfalt, um eine natürlichere Antwort zu erstellen. Vermeiden Sie beim Ausdrücken einer Entschuldigung mehrdeutige Wörter wie "Oops" oder "uh-oh", die als Schuld für den Benutzer interpretiert werden könnten. Verwenden Sie stattdessen Ausdrücke wie "tut mir leid" oder "mein Fehler". Bei wiederholten oder schwerwiegenderen Fehlern wird möglicherweise eine ausführlichere Entschuldigung verwendet, wie z. b. "Ich bin wirklich leid." Beachten Sie auch die Persönlichkeit des Zeichens beim Bestimmen der Art der Antwort. Eine andere Möglichkeit besteht darin, eine externe Situation zu machen. Kommentare wie z. b. "Junge, es gibt eine laute Ausgabe", machen die Verantwortung für den Benutzer und das Zeichen. Es kann auch hilfreich sein, den Benutzer über die kooperative Interaktion der Interaktion zu informieren. betrachten Sie beispielsweise die folgenden Begriffe:

Der Microsoft-Agent unterstützt auch ein automatisches Feedback zur Erkennung. Wenn eine Äußerung erkannt wird, zeigt der lauscht den Stimm Text der besten Übereinstimmung an. Sie können einen eigenen Text festlegen, der auf der Grundlage der Vertrauensstellungs Einstellung für einen von Ihnen definierten Befehl angezeigt wird.

Aufgrund eines möglichen Fehlers müssen Sie immer eine Bestätigung für alle Entscheidungen treffen, die schwerwiegende negative Folgen haben und nicht rückgängig gemacht werden können. Natürlich sollten Sie eine Bestätigung benötigen, wenn die Ergebnisse einer Aktion destruktiv sein könnten. Beachten Sie jedoch auch, dass eine Bestätigung für Situationen erforderlich ist, in denen ein langwieriger Prozess oder Vorgang abgebrochen wird

 

 





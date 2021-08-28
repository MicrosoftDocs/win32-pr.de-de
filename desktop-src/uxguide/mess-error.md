---
title: Fehlermeldungen (Entwurfsgrundlagen)
description: Eine Fehlermeldung warnt Benutzer über ein Problem, das bereits aufgetreten ist.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0ceffd3d1fecccd8342cb1e634735653bdba9722
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469017"
---
# <a name="error-messages-design-basics"></a>Fehlermeldungen (Entwurfsgrundlagen)

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine Fehlermeldung warnt Benutzer über ein Problem, das bereits aufgetreten ist. Im Gegensatz dazu werden Benutzer in einer Warnmeldung über eine Bedingung benachrichtigt, die in Zukunft ein Problem verursachen kann. Fehlermeldungen können mithilfe modaler Dialogfelder, direkt vorhandener Nachrichten, Benachrichtigungen oder Sprechblasen angezeigt werden.

![Screenshot der Fehlermeldung: Kann nicht umbenannt werden](images/mess-error-image1.png)

Eine typische modale Fehlermeldung.

Effektive Fehlermeldungen informieren Benutzer darüber, dass ein Problem aufgetreten ist, erläutern, warum es aufgetreten ist, und stellen eine Lösung bereit, damit Benutzer das Problem beheben können. Benutzer sollten entweder eine Aktion ausführen oder ihr Verhalten als Ergebnis einer Fehlermeldung ändern.

Gut geschriebene, hilfreiche Fehlermeldungen sind entscheidend für eine hochwertige Benutzererfahrung. Schlecht geschriebene Fehlermeldungen führen zu geringer Produktzufriedenheit und sind eine führende Ursache für vermeidbare Kosten für technischen Support. Unnötige Fehlermeldungen unterbrechen den Benutzerflow.

**Hinweis:** Richtlinien im Zusammenhang mit [Dialogfeldern,](win-dialog-box.md) [Warnmeldungen, Bestätigungen,](mess-confirm.md) [Standardsymbolen,](vis-std-icons.md) [Benachrichtigungen](mess-notif.md)und [Layout](vis-layout.md) werden in separaten Artikeln dargestellt. [](mess-warn.md)

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

- **Stellt die Benutzeroberfläche (UI) ein Problem dar, das bereits aufgetreten ist?** Wenn nicht, ist die Meldung kein Fehler. Wenn der Benutzer über eine Bedingung benachrichtigt wird, die in Zukunft ein Problem verursachen kann, verwenden Sie eine Warnmeldung.
- **Kann das Problem ohne Verwirrung verhindert werden?** Wenn ja, verhindern Sie stattdessen das Problem. Verwenden Sie beispielsweise Steuerelemente, die auf gültige Werte beschränkt sind, anstatt uneingeschränkte Steuerelemente zu verwenden, die möglicherweise Fehlermeldungen erfordern. Außerdem würde das Deaktivieren von Steuerelementen beim Klicken zu einem Fehler führen, solange offensichtlich ist, warum das Steuerelement deaktiviert ist.
- **Kann das Problem automatisch behoben werden?** Wenn ja, behandeln Sie das Problem, und unterdrücken Sie die Fehlermeldung.
- **Führen Benutzer wahrscheinlich eine Aktion aus oder ändern ihr Verhalten als Ergebnis der Nachricht?** Wenn dies nicht der Lage ist, kann der Benutzer durch die Bedingung nicht unterbrochen werden. Daher ist es besser, den Fehler zu unterdrücken.
- **Ist das Problem relevant, wenn Benutzer aktiv andere Programme verwenden?** Wenn ja, sollten Sie das Problem mithilfe eines [Infobereichssymbols](winenv-notification.md)anzeigen.
- **Steht das Problem nicht im Zusammenhang mit der aktuellen Benutzeraktivität, erfordert es keine sofortige Benutzeraktion, und können Benutzer es frei ignorieren?** Verwenden Sie in diesem Falle stattdessen eine [Aktionsfehlerbenachrichtigung.](mess-notif.md)
- **Bezieht sich das Problem auf den Status einer Hintergrundaufgabe in einem primären Fenster?** Falls ja, sollten Sie das Problem mithilfe einer [Statusleiste](ctrl-status-bars.md)anzeigen.
- **Sind die IT-Experten der primären Zielbenutzer?** Falls ja, sollten Sie einen alternativen Feedbackmechanismus verwenden, z. B. [Protokolldateieinträge](glossary.md) oder E-Mail-Warnungen. IT-Experten bevorzugen Protokolldateien dringend für nicht kritische Informationen.

## <a name="design-concepts"></a>Entwurfskonzepte

**Merkmale von fehlerhaften Fehlermeldungen**

Es sollte keine Überraschung sein, dass es viele heitere, nicht hilfreiche und schlecht geschriebene Fehlermeldungen gibt. Und da Fehlermeldungen häufig mit modalen Dialogen angezeigt werden, unterbrechen sie die aktuelle Aktivität des Benutzers und fordern, bestätigt zu werden, bevor der Benutzer fortfahren kann.

Ein Teil des Problems besteht darin, dass es so viele Möglichkeiten gibt, dies zu verfehlen. Sehen Sie sich diese Beispiele aus der Error Message Hall of Aussage an:

**Unnötige Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: Fehler bei der Anwendung ](images/mess-error-image2.png)

Dieses Beispiel aus Windows XP ist möglicherweise die schlechteste Fehlermeldung überhaupt. Es gibt an, dass ein Programm nicht gestartet werden konnte, da Windows selbst gerade heruntergefahren wird. Es gibt nichts, was der Benutzer dagegen tun kann oder dies sogar tun möchte (der Benutzer hat sich entschieden, Windows schließlich herunterzufahren). Und durch das Anzeigen dieser Fehlermeldung verhindert Windows das Herunterfahren!

**Das Problem:** Die Fehlermeldung selbst ist das Problem. Abgesehen davon, dass die Fehlermeldung verworfen wird, müssen Benutzer nichts tun.

**Häufigste Ursache:** Berichterstellung für alle Fehlerfälle, unabhängig von den Zielen oder Sicht des Benutzers.

**Empfohlene Alternative:** Melden Sie keine Fehler, die Benutzern egal sind.

**Fehlermeldungen zu "Erfolg"**

**Falsch:**

![Screenshot der Fehlermeldung: Entfernungsfehler ](images/mess-error-image3.png)

Diese Fehlermeldung hat dazu geführt, dass der Benutzer Windows nicht sofort nach dem Entfernen des Programms neu startet. Das Entfernen des Programms war aus Sicht des Benutzers erfolgreich.

**Das Problem:** Aus Sicht des Benutzers tritt kein Fehler auf. Abgesehen davon, dass die Fehlermeldung verworfen wird, müssen Benutzer nichts tun.

**Häufigste Ursache:** Die Aufgabe wurde aus Sicht des Benutzers erfolgreich abgeschlossen, ist aber aus Sicht des Deinstallationsprogramms fehlgeschlagen.

**Empfohlene Alternative:** Melden Sie keine Fehler für Bedingungen, die Benutzer als akzeptabel betrachten.

**Vollständig unbrauchbare Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: unbekannter Fehler ](images/mess-error-image4.png)

Benutzer erfahren, dass ein Fehler aufgetreten ist, haben aber keine Vorstellung davon, was der Fehler war oder wie er behoben werden soll. Und nein, das ist nicht in Ordnung!

**Das Problem:** Die Fehlermeldung stellt kein bestimmtes Problem dar, und es gibt keine Benutzer, die dafür sorgen können.

**Häufigste Ursache:** Höchstwahrscheinlich weist das Programm eine schlechte Fehlerbehandlung auf.

**Empfohlene Alternative:** Entwerfen Sie eine gute Fehlerbehandlung im Programm.

**Nicht verständliche Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: Sicherung nicht abgeschlossen ](images/mess-error-image5.png)

In diesem Beispiel ist die Problem-Anweisung klar, aber die ergänzende Erklärung ist völlig verwirrend.

**Das Problem:** Die Problem-Anweisung oder -Lösung ist nicht verständlich.

**Häufigste Ursache:** Erläuterung des Problems aus der Codesicht anstelle der des Benutzers.

**Empfohlene Alternative:** Schreiben Sie einen Fehlermeldungstext, den Ihre Zielbenutzer leicht verstehen können. Stellen Sie Lösungen bereit, die Benutzer tatsächlich ausführen können. Entwerfen Sie die Fehlermeldungserfahrung Ihres Programms, ohne dass Programmierer Fehlermeldungen an Ort und Stelle erstellen.

**Fehlermeldungen, die zu stark kommunizieren**

**Falsch:**

![Screenshot der extrem ausführlichen Meldung ](images/mess-error-image6.png)

In diesem Beispiel versucht die Fehlermeldung scheinbar, jeden Problembehandlungsschritt zu erklären.

**Das Problem:** Zu viele Informationen.

**Häufigste Ursache:** Geben Sie zu viele Details an, oder versuchen Sie, einen komplizierten Problembehandlungsprozess innerhalb einer Fehlermeldung zu erklären.

**Empfohlene Alternative:** Vermeiden Sie unnötige Details. Vermeiden Sie außerdem Problembehandlungen. Wenn eine Problembehandlung erforderlich ist, konzentrieren Sie sich auf die wahrscheinlichsten Lösungen, und erläutern Sie den Rest, indem Sie mit dem entsprechenden Thema in der Hilfe verknüpfen.

**Unnötig unerklärliche Fehlermeldungen**

**Falsch:**

![Screenshot der Meldung: Objekt kann nicht gefunden werden ](images/mess-error-image7.png)

Die Unfähigkeit des Programms, ein Objekt zu finden, klingt fatal. Und unter der Annahme, dass es sich um eine schwerwiegende Antwort handelt, warum ist die Antwort OK?

**Das Problem:** Der Ton des Programms ist unnötig mäßig oder drastisch.

**Häufigste Ursache:** Das Problem ist auf einen Fehler zurückzuführen, der aus Programmsicht schwerwiegende Auswirkungen hat.

**Empfohlene Alternative:** Wählen Sie die Sprache basierend auf dem Standpunkt des Benutzers sorgfältig aus.

**Fehlermeldungen, die Benutzern die Verantwortung geben**

**Falsch:**

![Screenshot der Meldung: ungültiges Zeichen ](images/mess-error-image8.png)

Warum sollen Benutzer sich als Verkriminaler fühlen?

**Das Problem:** Die Fehlermeldung wird so formuliert, dass der Benutzer einen Fehler verursacht.

**Führende Ursache:** Unempfindliche Ausdrücke, die sich auf das Verhalten des Benutzers konzentrieren, anstatt auf das Problem.

**Empfohlene Alternative:** Konzentrieren Sie sich auf das Problem, nicht auf die Benutzeraktion, die zu dem Problem geführt hat, und verwenden Sie bei Bedarf die passive Stimme.

**Silly-Fehlermeldungen**

**Falsch:**

![Screenshot der Meldung: Fehler im Fehlerbericht ](images/mess-error-image9.png)

In diesem Beispiel ist die Problem-Anweisung recht ironisch, und es werden keine Lösungen bereitgestellt.

**Das Problem:** Fehlermeldungen, die dumm oder nicht sequitors sind.

**Häufigste Ursache:** Erstellen von Fehlermeldungen, ohne auf ihren Kontext zu achten.

**Empfohlene Alternative:** Lassen Sie Ihre Fehlermeldungen von einem Writer erstellen und überprüfen. Berücksichtigen Sie bei der Überprüfung der Fehler den Kontext und den Benutzerzustand.

**Fehlermeldungen des Programmierers**

**Falsch:**

![Screenshot der Meldung: Adresse der Zugriffsverletzung ](images/mess-error-image10.png)

In diesem Beispiel gibt die Fehlermeldung an, dass im Programm ein Fehler aufgetreten ist. Diese Fehlermeldung hat nur für den Programmierer eine Bedeutung.

**Das Problem:** Nachrichten, die entwicklern helfen sollen, Fehler zu finden, sind in der Releaseversion des Programms enthalten. Diese Fehlermeldungen haben keine Bedeutung oder keinen Wert für Benutzer.

**Führende Ursache:** Programmierer verwenden die normale Benutzeroberfläche, um Nachrichten an sich selbst zu senden.

**Empfohlene Alternative:** Entwickler müssen alle derartigen Nachrichten bedingt kompilieren, damit sie automatisch aus der Releaseversion eines Produkts entfernt werden. Verschwenden Sie keine Zeit damit, Fehler wie diese für Benutzer zu verursachen, da ihre einzige Zielgruppe die Programmierer sind.

**Schlecht dargestellte Fehlermeldungen**

**Falsch:**

![Screenshot der Meldung: Unerwarteter Fehler ](images/mess-error-image11.png)

Dieses Beispiel weist viele häufige Präsentationsfehler auf.

**Das Problem:** Alle Details werden in der Fehlermeldungspräsentation falsch angezeigt.

**Führende Ursache:** Die Richtlinien für Fehlermeldungen sind nicht bekannt und werden nicht angewendet. Verwenden Sie keine Writer und Editoren, um die Fehlermeldungen zu erstellen und zu überprüfen.

Die Art der Fehlerbehandlung ist so, dass viele dieser Fehler sehr einfach zu machen sind. Es ist unerwünslich zu erkennen, dass die meisten Fehlermeldungen für die Hall of Aushängesentschärft sein können.

**Die Merkmale von guten Fehlermeldungen**

Im Gegensatz zu den vorherigen fehlerhaften Beispielen weisen gute Fehlermeldungen Folgendes auf:

- **Ein Problem.** Gibt an, dass ein Problem aufgetreten ist.
- **Eine Ursache.** Erläutert, warum das Problem aufgetreten ist.
- **Eine Lösung.** Stellt eine Lösung bereit, damit Benutzer das Problem beheben können.

Darüber hinaus werden gute Fehlermeldungen in einer Weise angezeigt, die wie dies ist:

- **Relevanten.** Die Meldung stellt ein Problem dar, das den Benutzern wichtig ist.
- **Umsetzbare.** Benutzer sollten entweder eine Aktion ausführen oder ihr Verhalten als Ergebnis der Nachricht ändern.
- **Benutzerzentriert.** In der Meldung wird das Problem in Bezug auf Aktionen oder Ziele von Zielbenutzern beschrieben, nicht in Bezug auf das, was der Code nicht betrifft.
- **Kurze.** Die Nachricht ist so kurz wie möglich, aber nicht kürzer.
- **Klar.** Die Nachricht verwendet eine einfache Sprache, damit die Zielbenutzer das Problem und die Lösung leicht verstehen können.
- **Bestimmten.** In der Meldung wird das Problem mithilfe einer bestimmten Sprache beschrieben, wobei bestimmte Namen, Speicherorte und Werte der beteiligten Objekte angegeben werden.
- **Höflich.** Benutzer sollten nicht dafür verantwortlich gemacht werden oder sich nicht verunreinigen lassen.
- **Selten.** Wird selten angezeigt. Häufig angezeigte Fehlermeldungen sind ein Anzeichen für einen fehlerhaften Entwurf.

Indem Sie ihre Fehlerbehandlungserfahrung so entwerfen, dass sie diese Merkmale aufweist, können Sie die Fehlermeldungen Ihres Programms aus der Fehlermeldungssumerierung heraushalten.

**Vermeiden unnötiger Fehlermeldungen**

Häufig ist die beste Fehlermeldung keine Fehlermeldung. Viele Fehler können durch einen besseren Entwurf vermieden werden, und es gibt häufig bessere Alternativen zu Fehlermeldungen. In der Regel ist es besser, einen Fehler zu verhindern, als einen Fehler zu melden.

Die offensichtlichsten Fehlermeldungen, die vermieden werden müssen, sind solche, die nicht umsetzbar sind. Wenn Benutzer die Nachricht wahrscheinlich schließen, ohne etwas zu tun oder zu ändern, lassen Sie die Fehlermeldung aus.

Einige Fehlermeldungen können entfernt werden, da sie aus Sicht des Benutzers keine Probleme darstellen. Angenommen, der Benutzer hat versucht, eine Datei zu löschen, die gerade gelöscht wird. Obwohl dies aus Codesicht ein unerwarteter Fall sein kann, betrachten Benutzer dies nicht als Fehler, da ihr gewünschtes Ergebnis erreicht wird.

**Falsch:**

![Screenshot der Meldung: Datei kann nicht gelöscht werden ](images/mess-error-image12.png)

Diese Fehlermeldung sollte entfernt werden, da die Aktion aus Sicht des Benutzers erfolgreich war.

Ein weiteres Beispiel: Angenommen, der Benutzer bricht eine Aufgabe explizit ab. Aus Sicht des Benutzers ist die folgende Bedingung kein Fehler.

**Falsch:**

![Screenshot der Meldung: Sicherung kann nicht abgeschlossen werden ](images/mess-error-image13.png)

Diese Fehlermeldung sollte auch entfernt werden, da die Aktion aus Sicht des Benutzers erfolgreich war.

Manchmal können Fehlermeldungen vermieden werden, indem sie sich auf die Ziele der Benutzer und nicht auf die Technologie konzentrieren. Überprüfen Sie dabei, was ein Fehler tatsächlich ist. Liegt das Problem mit den Zielen des Benutzers oder mit der Fähigkeit Ihres Programms, diese zu erfüllen? Wenn die Aktion des Benutzers in der realen Welt sinnvoll ist, sollte dies auch in der Software sinnvoll sein.

Nehmen wir beispielsweise an, dass ein Benutzer innerhalb eines E-Commerce-Programms versucht, ein Produkt mithilfe der Suche zu finden, aber die Literalsuchabfrage hat keine Übereinstimmungen, und das gewünschte Produkt ist nicht mehr vorrätig. Technisch gesehen ist dies ein Fehler, aber anstatt eine Fehlermeldung zu geben, könnte das Programm:

- Suchen Sie weiterhin nach Produkten, die der Abfrage am besten entsprechen.
- Wenn die Suche offensichtliche Fehler enthält, empfiehlt automatisch eine korrigierte Abfrage.
- Behandeln Sie häufig auftretende Probleme wie Rechtschreibfehler, alternative Rechtschreibungen und nicht übereinstimmende Pluralisierungs- und Verbfälle automatisch.
- Geben Sie an, wann das Produkt vorrätig ist.

Solange die Anforderung des Benutzers angemessen ist, sollte ein gut entworfenes E-Commerce-Programm angemessene Ergebnisse und keine Fehler zurückgeben.

Eine weitere hervorragende Möglichkeit, Fehlermeldungen zu vermeiden, besteht darin, Probleme überhaupt zu vermeiden. Sie können Fehler verhindern, indem Sie:

- **Verwenden von eingeschränkten Steuerelementen.** Verwenden Sie Steuerelemente, die auf gültige Werte beschränkt sind. Steuerelemente wie Listen, Schieberegler, Kontrollkästchen, Optionsfelder und Datums- und Uhrzeitauswahl sind auf gültige Werte beschränkt, während Textfelder häufig nicht sind und möglicherweise Fehlermeldungen erfordern. Sie können Textfelder jedoch einschränken, um nur bestimmte Zeichen und eine maximale Anzahl von Zeichen zu akzeptieren.
- **Verwenden von eingeschränkten Interaktionen.** Erlauben Sie Benutzern bei Ziehvorgängen, nur gültige Ziele zu löschen.
- **Verwenden deaktivierter Steuerelemente und Menüelemente.** Deaktivieren Sie Steuerelemente und Menüelemente, wenn Benutzer leicht ableiten können, warum das Steuerelement oder Menüelement deaktiviert ist.
- **Bereitstellen guter Standardwerte.** Benutzer sind weniger wahrscheinlich, Eingabefehler zu machen, wenn sie die Standardwerte akzeptieren können. Auch wenn Benutzer sich entscheiden, den Wert zu ändern, informiert der Standardwert Benutzer über das erwartete Eingabeformat.
- **Die Dinge einfach funktionieren.** Benutzer machen weniger Fehler, wenn die Aufgaben für sie nicht erforderlich sind oder automatisch ausgeführt werden. Wenn Benutzer kleine Fehler machen, aber ihre Absicht klar ist, wird das Problem automatisch behoben. Beispielsweise können Sie kleinere Formatierungsprobleme automatisch beheben.

**Bereitstellen der erforderlichen Fehlermeldungen**

Manchmal müssen Sie tatsächlich eine Fehlermeldung bereitstellen. Benutzer machen Fehler, Netzwerke und Geräte funktionieren nicht mehr, Objekte können nicht gefunden oder geändert werden, Aufgaben können nicht abgeschlossen werden, und Programme haben Fehler. Im Idealfall würden diese Probleme weniger häufig auftreten, z. B. können wir unsere Software so entwerfen, dass viele Arten von Benutzerfehlern verhindert werden, aber es ist nicht realistisch, all diese Probleme zu verhindern. Und wenn eines dieser Probleme auftritt, führt eine hilfreiche Fehlermeldung dazu, dass Benutzer schnell wieder auf dem Richtigen sind.

Eine gängige Annahme ist, dass Fehlermeldungen die schlechteste Benutzererfahrung sind und um alle Kosten vermieden werden sollten. Es ist jedoch genauer zu sagen, dass Benutzerverwechslungen die schlechteste Erfahrung sind und um alle Kosten vermieden werden sollten. Manchmal sind diese Kosten eine hilfreiche Fehlermeldung.

Ziehen Sie deaktivierte Steuerelemente in Betracht. In den meisten Jahren ist es offensichtlich, warum ein Steuerelement deaktiviert ist. Daher ist das Deaktivieren des Steuerelements eine gute Möglichkeit, eine Fehlermeldung zu vermeiden. Was passiert jedoch, wenn der Grund, warum ein Steuerelement deaktiviert ist, nicht offensichtlich ist? Der Benutzer kann nicht fortfahren, und es gibt kein Feedback, um das Problem zu bestimmen. Jetzt bleibt der Benutzer hängen und muss entweder das Problem lösen oder technischen Support erhalten. In solchen Fällen ist es viel besser, das Steuerelement aktiviert zu lassen und stattdessen eine hilfreiche Fehlermeldung zu geben.

**Falsch:**

![Screenshot der Nachricht: Wo speichern Sie die Sicherung? ](images/mess-error-image14.png)

Warum ist die Schaltfläche Weiter hier deaktiviert? Lassen Sie es besser aktiviert, und vermeiden Sie Benutzerverwechslungen, indem Sie eine hilfreiche Fehlermeldung geben.

Wenn Sie nicht sicher sind, ob Sie eine Fehlermeldung senden sollten, beginnen Sie mit dem Verfassen der Fehlermeldung, die Sie möglicherweise geben. Wenn Benutzer wahrscheinlich entweder eine Aktion ausführen oder ihr Verhalten als Ergebnis ändern, geben Sie die Fehlermeldung an. Wenn Benutzer die Nachricht dagegen wahrscheinlich verlassen, ohne etwas zu tun oder zu ändern, sollten Sie die Fehlermeldung weglassen.

**Entwerfen für eine gute Fehlerbehandlung**

Obwohl das Erstellen eines guten Fehlermeldungstexts schwierig sein kann, ist dies manchmal ohne eine gute Unterstützung der Fehlerbehandlung durch das Programm nicht möglich. Betrachten Sie diese Fehlermeldung:

**Falsch:**

![Screenshot der Meldung: Unbekannter Fehler ](images/mess-error-image15.png)

Wahrscheinlich ist das Problem tatsächlich unbekannt, da die Unterstützung für die Fehlerbehandlung des Programms nicht besteht.

Es ist zwar möglich, dass es sich um eine sehr schlecht geschriebene Fehlermeldung handelt, sie spiegelt jedoch wahrscheinlich die fehlende gute Fehlerbehandlung durch den zugrunde liegenden Code wider, es sind keine spezifischen Informationen zum Problem bekannt.

Um spezifische, umsetzbare, benutzerzentrierte Fehlermeldungen zu erstellen, muss der Fehlerbehandlungscode Ihres Programms spezifische, auf hoher Ebene enthaltende Fehlerinformationen bereitstellen:

- Jedem Problem sollte ein eindeutiger Fehlercode zugewiesen sein.
- Wenn ein Problem mehrere Ursachen hat, sollte das Programm nach Möglichkeit die spezifische Ursache ermitteln.
- Wenn das Problem über Parameter verfügt, müssen die Parameter beibehalten werden.
- Probleme auf niedriger Ebene müssen auf einer ausreichend hohen Ebene behandelt werden, damit die Fehlermeldung aus Sicht des Benutzers angezeigt werden kann.

Gute Fehlermeldungen sind nicht nur ein Problem mit der Benutzeroberfläche, sondern ein Softwareentwurfsproblem. Eine gute Fehlermeldung ist nicht etwas, das später nicht mehr verwendet werden kann.

**Problembehandlung (und wie sie vermieden wird)**

Problembehandlungsergebnisse, wenn ein Problem mit mehreren verschiedenen Ursachen mit einer einzelnen Fehlermeldung gemeldet wird.

**Falsch:**

![Diagramm einer Meldung mit drei Ursachen ](images/mess-error-image16.png)

**Richtig:**

![Diagramm mit drei Meldungen, die jeweils eine Ursache angeben](images/mess-error-image17.png)

Problembehandlungsergebnisse, wenn mehrere Probleme mit einer einzelnen Fehlermeldung gemeldet werden.

Im folgenden Beispiel konnte ein Element nicht verschoben werden, da es bereits verschoben oder gelöscht wurde oder der Zugriff verweigert wurde. Wenn das Programm die Ursache leicht ermitteln kann, warum muss der Benutzer die spezifische Ursache ermitteln?

**Falsch:**

![Screenshot der Meldung mit zwei Ursachen ](images/mess-error-image18.png)

Was ist das? Nun muss der Benutzer eine Problembehandlung durchführen.

Das Programm kann ermitteln, ob der Zugriff verweigert wurde. Daher sollte dieses Problem mit einer bestimmten Fehlermeldung gemeldet werden.

**Richtig:**

![Screenshot der Meldung mit angabe einer Ursache ](images/mess-error-image19.png)

Bei einer bestimmten Ursache ist keine Problembehandlung erforderlich.

Verwenden Sie Nachrichten mit mehreren Ursachen nur, wenn die spezifische Ursache nicht bestimmt werden kann. In diesem Beispiel wäre es für das Programm schwierig zu bestimmen, ob das Element verschoben oder gelöscht wurde. Daher kann hier eine einzelne Fehlermeldung mit mehreren Ursachen verwendet werden. Es ist jedoch unwahrscheinlich, dass sich Benutzer darum kümmern, wenn sie z. B. eine gelöschte Datei nicht verschieben können. Für diese Ursachen ist die Fehlermeldung nicht einmal erforderlich.

**Behandeln unbekannter Fehler**

In einigen Fällen kennen Sie das Problem, die Ursache oder die Lösung nicht. Wenn es nicht unklug wäre, den Fehler zu unterdrücken, ist es besser, sich über das Fehlen von Informationen im Vordezüglich zu informieren, als Probleme, Ursachen oder Lösungen zu präsentieren, die möglicherweise nicht richtig sind.

Wenn ihr Programm z. B. über eine nicht behandelte Ausnahme verfügt, ist die folgende Fehlermeldung geeignet:

![Screenshot der Meldung: Unbekannter Fehler aufgetreten ](images/mess-error-image20.png)

Wenn Sie einen unbekannten Fehler nicht unterdrücken können, ist es besser, sich mit dem Fehlen von Informationen im Überblick zu informieren.

Stellen Sie andererseits spezifische, umsetzbare Informationen zur Verfügung, wenn dies in den meisten Zeit hilfreich sein wird.

![Screenshot: Meldung Office Communicator "Server nicht verfügbar" ](images/mess-error-image21.png)

Diese Fehlermeldung eignet sich für einen unbekannten Fehler, wenn die Netzwerkkonnektivität in der Regel das Problem ist.

**Bestimmen des geeigneten Nachrichtentyps**

Einige Probleme können je nach Schwerpunkt und Ausdruck als Fehler, Warnung oder Informationen dargestellt werden. Angenommen, eine Webseite kann kein nicht signiertes ActiveX basierend auf der aktuellen Windows Internet Explorer laden:

- **Fehler.** "Diese Seite kann kein nicht signiertes ActiveX laden." (Wird als vorhandenes Problem formuliert.)
- **Warnung.** "Diese Seite verhält sich möglicherweise nicht wie erwartet, da Windows Internet Explorer nicht zum Laden von nicht signierten ActiveX konfiguriert ist." oder "Zulassen, dass diese Seite ein nicht signiertes ActiveX Installiert? Dies aus nicht vertrauenswürdigen Quellen kann Ihren Computer schaden." (Beide werden als Bedingungen formuliert, die zukünftige Probleme verursachen können.)
- **Informationen.** "Sie haben konfiguriert, Windows Internet Explorer, um nicht signierte ActiveX zu blockieren." (Wird als Faktenauszug formuliert.)

**Um den geeigneten Nachrichtentyp zu bestimmen, konzentrieren Sie sich auf den wichtigsten Aspekt des Problems, den Benutzer kennen müssen oder mit dem sie handeln müssen.** Wenn ein Problem den Benutzer am Fortfahren blockiert, sollten Sie es in der Regel als Fehler präsentieren. wenn der Benutzer fortfahren kann, stellen Sie ihn als Warnung vor. Erstellen Sie [die Hauptanweisung](text-ui.md) oder einen anderen entsprechenden Text basierend auf diesem Fokus, und wählen Sie dann ein Symbol[(Standard](vis-std-icons.md) oder anderweitig) aus, das dem Text entspricht. Der Hauptanweisungstext und die Symbole sollten immer übereinstimmen.

**Fehlermeldungspräsentation**

Die meisten Fehlermeldungen in Windows werden über modale Dialogfelder angezeigt (wie die meisten Beispiele in diesem Artikel), aber es gibt andere Optionen:

- Direkt
- Ballons
- Benachrichtigungen
- Symbole für den Benachrichtigungsbereich
- Statusleisten
- Protokolldateien (für Fehler, die an IT-Experten ausgerichtet sind)

Das Einfügen von Fehlermeldungen in modale Dialogfelder hat den Vorteil, dass die unmittelbare Aufmerksamkeit und Bestätigung des Benutzers gefordert wird. Dies ist jedoch auch ihr Hauptnachteil, wenn diese Aufmerksamkeit nicht erforderlich ist.

![Screenshot der Nachricht: Beenden Ihrer Arbeit ](images/mess-error-image22.png)

Müssen Sie Benutzer wirklich unterbrechen, damit sie auf die Schaltfläche Schließen klicken können? Falls nicht, sollten Sie Alternativen zur Verwendung eines modalen Dialogfelds in Betracht ziehen.

Modale Dialoge sind eine gute Wahl, wenn der Benutzer das Problem unmittelbar vor dem Fortfahren bestätigen muss, andernfalls aber häufig eine schlechte Wahl. Im Allgemeinen sollten Sie es vorziehen, die leichteste Präsentation zu verwenden, die die Arbeit gut erledigt.

**Vermeiden von Überkommunikation**

Im Allgemeinen [lesen Benutzer nicht, sie überprüfen](vis-layout.md). Je mehr Text vorhanden ist, desto schwieriger ist die Überprüfung des Texts, und je wahrscheinlicher Benutzer den Text überhaupt nicht lesen. Daher ist es wichtig, den Text auf seine Grundlagen zu reduzieren und bei Bedarf progressive Offenlegung und Hilfelinks zu verwenden, um zusätzliche Informationen bereitzustellen.

Es gibt viele extreme Beispiele, aber sehen wir uns ein typisches beispiel an. Das folgende Beispiel weist die meisten Attribute einer guten Fehlermeldung auf, aber der Text ist nicht präzise und erfordert eine Motivation zum Lesen.

**Falsch:**

![Screenshot der ausführlichen Meldung ](images/mess-error-image23.png)

Dieses Beispiel ist eine gute Fehlermeldung, wird jedoch überschrieben.

Was ist der gesamte Text, der wirklich sagt? Ungefähr so wie hier gezeigt:

**Richtig:**

![Screenshot der Meldung: CD-Aufzeichnung nicht erkannt ](images/mess-error-image24.png)

Diese Fehlermeldung enthält im Wesentlichen die gleichen Informationen, ist aber wesentlich präziser.

Wenn Sie die Details mithilfe der Hilfe angeben, weist diese Fehlermeldung einen [invertierten Pyramidenstil](text-ui.md) auf.

Weitere Richtlinien und Beispiele zur Überkommunikation finden Sie unter [Benutzeroberfläche Text](text-ui.md).

**Wenn Sie nur acht Dinge tun**

1. Entwerfen Sie Ihr Programm für die Fehlerbehandlung.
2. Geben Sie keine unnötigen Fehlermeldungen an.
3. Vermeiden Sie Benutzerwechslungen, indem Sie die erforderlichen Fehlermeldungen senden.
4. Stellen Sie sicher, dass die Fehlermeldung ein Problem, eine Ursache und eine Lösung enthält.
5. Stellen Sie sicher, dass die Fehlermeldung relevant, umsetzbar, kurz, klar, spezifisch, zusichtig und selten ist.
6. Entwerfen Sie Fehlermeldungen aus der Sicht des Benutzers, nicht aus der Sicht des Programms.
7. Vermeiden Sie es, den Benutzer in die Problembehandlung einzubeziehen. Verwenden Sie für jede erkennbare Ursache eine andere Fehlermeldung.
8. Verwenden Sie die methode mit der geringsten Gewichtungsdarstellung, die die Arbeit gut erledigt.

**Verwendungsmuster**

Fehlermeldungen weisen mehrere Verwendungsmuster auf:


| | | <strong>Systemprobleme</strong><br /> Das Betriebssystem, das Hardwaregerät, das Netzwerk oder das Programm ist ausgefallen oder befindet sich nicht in dem Zustand, der zum Ausführen einer Aufgabe erforderlich ist. <br /> | Viele Systemprobleme können vom Benutzer gelöst werden: <br /><ul><li>Geräteprobleme können gelöst werden, indem sie das Gerät einschalten, das Gerät erneut verbinden und Medien einfügen.</li><li>Netzwerkprobleme können gelöst werden, indem sie die physische Netzwerkverbindung überprüfen und <strong>netzwerkdiagnose und reparieren</strong>ausführen.</li><li>Programmprobleme können gelöst werden, indem Programmoptionen geändert oder das Programm neu gestartet werden.</li></ul><img src="images/mess-error-image25.png" alt="Screen shot of message: Can't find a camera " /><br /> In diesem Beispiel kann das Programm keine Kamera finden, um eine Benutzeraufgabe auszuführen.<br /><img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br /> In diesem Beispiel muss ein Feature aktiviert werden, das zum Ausführen einer Aufgabe erforderlich ist.<br /> | | <strong>Dateiprobleme</strong><br /> Eine Datei oder ein Ordner, die bzw. der für eine vom Benutzer initiierte Aufgabe erforderlich ist, wurde nicht gefunden, wird bereits verwendet oder hat nicht das erwartete Format. <br /> | <img src="images/mess-error-image27.png" alt="Screen shot of message: Can't delete file " /><br /> In diesem Beispiel kann die Datei oder der Ordner nicht gelöscht werden, da sie nicht gefunden wurde.<br /><img src="images/mess-error-image28.png" alt="Screen shot of message: Can't play this file " /><br /> In diesem Beispiel unterstützt das Programm das angegebene Dateiformat nicht.<br /> | | <strong>Sicherheitsprobleme</strong><br /> Der Benutzer verfügt nicht über die Berechtigung für den Zugriff auf eine Ressource oder über ausreichende Berechtigungen zum Ausführen einer vom Benutzer initiierten Aufgabe. <br /> | <img src="images/mess-error-image29.png" alt="Screen shot of message: You don't have permission " /><br /> In diesem Beispiel verfügt der Benutzer nicht über die Berechtigung für den Zugriff auf eine Ressource.<br /><img src="images/mess-error-image30.png" alt="Screen shot of message: You don't have privilege " /><br /> In diesem Beispiel verfügt der Benutzer nicht über die Berechtigung, eine Aufgabe auszuführen.<br /> | | <strong>Aufgabenprobleme</strong><br /> Es liegt ein bestimmtes Problem vor, bei dem eine vom Benutzer initiierte Aufgabe ausgeführt wird (mit Ausnahme eines Systems, einer datei nicht gefundenen Datei, eines Dateiformats oder eines Sicherheitsproblems). <br /> | <img src="images/mess-error-image31.png" alt="Screen shot of message: Data can't be pasted " /><br /> In diesem Beispiel können die Zwischenablagedaten nicht in Paint eingefügt werden.<br /><img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can't be installed " /><br /> In diesem Beispiel kann der Benutzer kein Softwareupgrade installieren.<br /> | | <strong>Benutzereingabeprobleme</strong><br /> Der Benutzer hat einen Wert eingegeben, der falsch oder inkonsistent mit anderen Benutzereingaben ist. <br /> | <img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br /> In diesem Beispiel hat der Benutzer einen falschen Zeitwert eingegeben.<br /><img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br /> In diesem Beispiel hat die Benutzereingabe nicht das richtige Format.<br /> | 


## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

- **Verwenden Sie Aufgabendialoge nach Bedarf,** um ein konsistentes Aussehen und Layout zu erzielen. Aufgabendialogfelder erfordern Windows Vista oder höher, sodass sie nicht für frühere Versionen von Windows geeignet sind. Wenn Sie ein Meldungsfeld verwenden müssen, trennen Sie die Hauptanweisung durch zwei Zeilenumbrüche von der ergänzenden Anweisung.

### <a name="user-input-errors"></a>Benutzereingabefehler

- **Verhindern oder reduzieren Sie Benutzereingabefehler nach Möglichkeit wie folgt:**
  - Verwenden von Steuerelementen, die auf gültige Werte beschränkt sind.
  - Das Deaktivieren von Steuerelementen und Menüelementen beim Klicken würde zu einem Fehler führen, solange offensichtlich ist, warum das Steuerelement oder Menüelement deaktiviert ist.
  - Bereitstellen guter Standardwerte.

**Falsch:**

![Screenshot des Textfelds mit Sprecherlautstärke ](images/mess-error-image35.png)

In diesem Beispiel wird ein uneingeschränktes Textfeld für eingeschränkte Eingaben verwendet. Verwenden Sie stattdessen einen Schieberegler.

- **Verwenden Sie die moduslose Fehlerbehandlung (direkt auftretende Fehler oder Sprechblasen) für kontextbezogene Benutzereingabeprobleme.**
- **Verwenden Sie Sprechblasen für nicht kritische Benutzereingabeprobleme mit nur einem Punkt, die erkannt wurden, während sie in einem Textfeld oder unmittelbar nach dem Verlust des Fokus in einem Textfeld erkannt wurden.** [Für Sprechblasen](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) ist kein verfügbarer Bildschirmbereich oder das dynamische Layout erforderlich, das zum Anzeigen von Nachrichten an Ort und Stelle erforderlich ist. Zeigt nur einen einzelnen Sprechblasen gleichzeitig an. Da das Problem nicht kritisch ist, ist kein Fehlersymbol erforderlich. Sprechblasen werden beim Klicken, beim Beheben des Problems oder nach einem Timeout entfernt.

![Screenshot der Meldung: falsches Zeichen ](images/mess-error-image36.png)

In diesem Beispiel weist ein Sprechblasen auf ein Eingabeproblem hin, während es sich noch im -Steuerelement hält.

- **Verwenden Sie direkt fehler für die verzögerte Fehlererkennung.** In der Regel werden Fehler gefunden, indem Sie auf eine Commitschaltfläche klicken. (Verwenden Sie keine [direkten Fehler](glossary.md) für Einstellungen, für die sofort ein Commit ausgeführt wird.) Es können mehrere fehlerverdingende Fehler gleichzeitig auftreten. Verwenden Sie normalen Text und ein 16 x 16 Pixel großes Fehlersymbol, und platzieren Sie sie nach Möglichkeit direkt neben dem Problem. Direkt auftretende Fehler werden nur dann entfernt, wenn der Benutzer einen Commit vorgibt und keine anderen Fehler gefunden werden.

![Screenshot der Meldung: falsche E-Mail-Adresse ](images/mess-error-image37.png)

In diesem Beispiel wird ein direkt auftretender Fehler für einen Fehler verwendet, der durch Klicken auf die Commitschaltfläche gefunden wurde.

- **Verwenden Sie modale Fehlerbehandlung (Aufgabendialoge oder Meldungsfelder) für alle anderen Probleme,** einschließlich Fehlern, die mehrere Steuerelemente betreffen oder nicht kontextbezogene oder nicht eingabebezogene Fehler sind, die durch Klicken auf eine Commitschaltfläche gefunden werden.
- **Wenn ein Benutzereingabeproblem gemeldet wird, legen Sie den Eingabefokus auf das erste Steuerelement mit den falschen Daten fest.** Scrollen Sie das Steuerelement bei Bedarf in die Ansicht. Wenn das Steuerelement ein Textfeld ist, wählen Sie den gesamten Inhalt aus. Es sollte immer offensichtlich sein, worauf die Fehlermeldung verweist.
- **Löschen Sie keine falschen Eingaben.** Lassen Sie es stattdessen so, dass der Benutzer das Problem sehen und beheben kann, ohne von vorn anfangen zu müssen.
  - **Ausnahme:** Deaktivieren Sie falsche Kennwort- und PIN-Textfelder, da Benutzer maskierte Eingaben nicht effektiv korrigieren können.

### <a name="troubleshooting"></a>Problembehandlung

- **Vermeiden Sie das Erstellen von Problemen bei der Problembehandlung.** Verlassen Sie sich nicht auf eine einzelne Fehlermeldung, um ein Problem mit mehreren verschiedenen erkennbaren Ursachen zu melden.
- **Verwenden Sie für jede erkennbare Ursache eine andere Fehlermeldung (in der Regel eine andere ergänzende Anweisung).** Wenn eine Datei beispielsweise aus mehreren Gründen nicht geöffnet werden kann, geben Sie für jeden Grund eine separate ergänzende Anweisung an.
- **Verwenden Sie eine Nachricht mit mehreren Ursachen nur, wenn die spezifische Ursache nicht bestimmt werden kann.** Stellen Sie in diesem Fall die Lösungen in der Reihenfolge der Wahrscheinlichkeit vor, dass das Problem behoben wird. Auf diese Weise können Benutzer das Problem effizienter lösen.

### <a name="icons"></a>Symbole

- **Modale Fehlermeldungsdialogfelder verfügen nicht über Titelleistensymbole.** Titelleistensymbole werden als visueller Unterschied zwischen primären und sekundären Fenstern verwendet.
- **Verwenden Sie ein Fehlersymbol.** Ausnahmen:
  - Wenn der Fehler ein Benutzereingabeproblem ist, das mithilfe eines modalen Dialogfelds oder einer Sprechblase angezeigt wird, verwenden Sie kein Symbol. Dies steht gegen den ermutigenden Tonfall Windows. Für die fehlermeldungsbasierten Meldungen sollte jedoch ein kleines Fehlersymbol (16 x 16 Pixel) verwendet werden, um sie eindeutig als Fehlermeldungen zu identifizieren.

     ![Screenshot der Nachricht im falschen Postformat](images/mess-error-image38.png)

     ![Screenshot des Zu langen Computernamens der Nachricht](images/mess-error-image39.png)

     In diesen Beispielen benötigen Benutzereingabeprobleme keine Fehlersymbole.

     ![Screenshot: Falsches Format der Nachrichtentelefonnummer](images/mess-error-image40.png)

     In diesem Beispiel benötigt eine fehlermeldung ein kleines Fehlersymbol, um sie eindeutig als Fehlermeldung zu identifizieren.

- Wenn das Problem für ein Feature mit einem Symbol (und nicht einem Benutzereingabeproblem) auftritt, können Sie das Featuresymbol mit einer Fehlerüberlagerung verwenden. Verwenden Sie in diesem Fall auch den Funktionsnamen als Betreff des Fehlers.

    ![Screenshot der Meldung, dass der Media Player die Datei nicht wiedererknen kann ](images/mess-error-image41.png)

    In diesem Beispiel verfügt das Featuresymbol über eine Fehlerüberlagerung, und das Feature ist das Subjekt des Fehlers.

- **Verwenden Sie keine Warnsymbole für Fehler.** Dies wird häufig durchgeführt, um die Darstellung weniger schwerwiegend zu machen. Fehler sind keine Warnungen.

    **Falsch:**

    ![Screenshot: Schnelles Wechseln von Nachrichten nicht aktiviert ](images/mess-error-image42.png)

    In diesem Beispiel wird fälschlicherweise ein Warnsymbol verwendet, damit sich der Fehler weniger schwerwiegend anfühlt.

Weitere Richtlinien und Beispiele finden Sie unter [Standardsymbole.](vis-std-icons.md)

### <a name="progressive-disclosure"></a>Schrittweise Offenlegung

- **Verwenden Sie die Schaltfläche Details progressive Offenlegung ein-/ausblenden, um erweiterte oder detaillierte Informationen in einer Fehlermeldung auszublenden.** Dadurch wird die Fehlermeldung für die typische Verwendung vereinfacht. Blenden Sie die erforderlichen Informationen nicht aus, da Benutzer sie möglicherweise nicht finden.

![Screenshot der Meldung: ActiveSync kann sich nicht anmelden ](images/mess-error-image43.png)

In diesem Beispiel können Benutzer mit der Schaltfläche für die progressive Offenlegung einen Drilldown auf weitere Details anzeigen, wenn sie dies wünschen, oder die Benutzeroberfläche vereinfachen, wenn dies nicht der Fall ist.

- **Verwenden Sie Details nur dann ein-/ausblenden, wenn tatsächlich weitere Details zu finden sind.** Erstellen Sie nicht nur die vorhandenen Informationen in einem ausführlicheren Format.
- **Verwenden Sie keine Details ein-/ausblenden, um Hilfeinformationen anzuzeigen.** Verwenden Sie stattdessen Hilfelinks.

Bezeichnungsrichtlinien finden Sie unter [Progressive Disclosure Controls](ctrl-progressive-disclosure-controls.md).

**Diese Meldung nicht mehr anzeigen**

- **Wenn diese Option für eine Fehlermeldung benötigt wird, überprüfen Sie den Fehler und dessen Häufigkeit.** Wenn sie alle Merkmale eines guten Fehlers aufweist (relevant, umsetzbar und selten), sollte es für Benutzer nicht sinnvoll sein, ihn zu unterdrücken.

Weitere Richtlinien finden Sie unter [Dialogfelder](win-dialog-box.md).

### <a name="default-values"></a>Standardwerte

- **Wählen Sie die sicherste, am wenigsten destruktive oder sicherste Antwort als Standard aus.** Wenn die Sicherheit kein Faktor ist, wählen Sie den wahrscheinlichsten oder bequemsten Befehl aus.

### <a name="help"></a>Hilfe

- **Entwerfen Sie Fehlermeldungen, um die Notwendigkeit von Hilfe zu vermeiden.** Normalerweise sollten Benutzer keinen externen Text lesen müssen, um das Problem zu verstehen und zu lösen, es sei denn, die Lösung erfordert mehrere Schritte.
- **Stellen Sie sicher, dass der Hilfeinhalt relevant und hilfreich ist.** Es sollte keine ausführliche Neuform der Fehlermeldung sein, sondern es sollte nützliche Informationen enthalten, die über den Bereich der Fehlermeldung hinausgehen, z. B. Möglichkeiten, das Problem in der Zukunft zu vermeiden. Geben Sie keinen Hilfelink an, nur weil dies der Reihe nach ist.
- **Verwenden Sie spezifische, präzise und relevante Hilfelinks, um auf Hilfeinhalte zu zugreifen.** Verwenden Sie zu diesem Zweck keine Befehlsschaltflächen oder progressive Offenlegung.
- **Für Fehlermeldungen, die Sie nicht spezifisch und umsetzbar machen können, sollten Sie Links zu Onlinehilfeinhalten bereitstellen.** Dadurch können Sie Benutzern zusätzliche Informationen bereitstellen, die Sie aktualisieren können, nachdem das Programm veröffentlicht wurde.

Weitere Richtlinien finden Sie unter [Hilfe.](winenv-help.md)

### <a name="error-codes"></a>Fehlercodes

- **Für Fehlermeldungen, die Sie nicht spezifisch und umsetzbar machen können oder von der Hilfe profitieren, sollten Sie auch Fehlercodes bereitstellen.** Benutzer verwenden diese Fehlercodes häufig, um im Internet nach zusätzlichen Informationen zu suchen.
- **Geben Sie immer eine Textbeschreibung des Problems und der Lösung an.** Hängen Sie nicht nur vom Fehlercode für diesen Zweck ab.

**Falsch:**

![Screenshot der Nachricht: Datei kann nicht geöffnet werden ](images/mess-error-image44.png)

In diesem Beispiel wird ein Fehlercode als Ersatz für einen Lösungstext verwendet.

- **Weisen Sie einen eindeutigen Fehlercode für jede unterschiedliche Ursache zu.** Dadurch wird die Problembehandlung vermieden.
- **Wählen Sie Fehlercodes aus, die im Internet leicht durchsuchbar sind.** Wenn Sie 32-Bit-Codes verwenden, verwenden Sie eine Hexadezimaldarstellung mit einem führenden "0x" und Großbuchstaben.

**Richtig:**

1234

0xC0001234

**Falsch:**

-1

-67113524

- **Verwenden Sie Details ein-/ausblenden, um Fehlercodes anzuzeigen.** Ausdruck als Fehlercode: <error code> .

![Screenshot der Meldung: Programm wurde nicht initialisiert ](images/mess-error-image45.png)

In diesem Beispiel wird ein Fehlercode verwendet, um eine Fehlermeldung zu ergänzen, die von weiteren Informationen profitieren kann.

### <a name="sound"></a>Sound

- **Begleiten Sie Fehlermeldungen nicht mit einem Soundeffekt oder Signalton.** Dies ist nicht erforderlich.
  - **Ausnahme:** Geben Sie den Soundeffekt Kritisches Beenden wieder, wenn das Problem für den Betrieb des Computers entscheidend ist und der Benutzer sofort Maßnahmen ergreifen muss, um schwerwiegende Folgen zu verhindern.

## <a name="text"></a>Text

**Allgemein**

- **Entfernen Sie redundanten Text.** Suchen Sie in Titeln, Hauptanweisungen, ergänzenden Anweisungen, Befehlslinks und Commitschaltflächen. Lassen Sie im Allgemeinen vollständigen Text in Anweisungen und interaktiven Steuerelementen, und entfernen Sie alle Redundanzen von den anderen Stellen.
- **Verwenden Sie benutzerzentrierte Erklärungen.** Beschreiben Sie das Problem in Bezug auf Benutzeraktionen oder -ziele, nicht in Bezug auf die Unfreundlichkeit der Software. Verwenden Sie die Sprache, die die Zielbenutzer verstehen und verwenden. Vermeiden Sie den technischen Jargon.

**Falsch:**

![Screenshot der Nachricht: eingabesynchroner Aufruf ](images/mess-error-image46.png)

**Richtig:**

![Screenshot der Nachricht: Der Empfang eines Anrufs ist ausgelastet. ](images/mess-error-image47.png)

In diesen Beispielen spricht die richtige Version die Sprache des Benutzers, während die falsche Version zu technisch ist.

- **Verwenden Sie nicht die folgenden Wörter:**
  - Fehler, Fehler (verwenden Sie stattdessen Problem)
  - Failed to (use unable to instead)
  - Ungültig, ungültig, ungültig (verwenden Sie stattdessen falsch)
  - Abbrechen, Beenden, Beenden (stattdessen beenden)
  - Schwerwiegend, schwerwiegend (verwenden Sie stattdessen "schwerwiegend")

Diese Begriffe sind unnötig und stehen im Gegensatz zum ermutigenden Tonfall Windows. Bei [ordnungsgemäßer Verwendung](vis-std-icons.md)teilt das Fehlersymbol ausreichend mit, dass ein Problem vor liegt.

**Falsch:**

![Screenshot der Meldung: schwerwiegender Fehler! ](images/mess-error-image48.png)

**Richtig:**

![Screenshot der Meldung: Sicherung muss gleichzeitig geschlossen werden ](images/mess-error-image49.png)

Im falschen Beispiel sind die Begriffe "schwerwiegende" und "Fehler" nicht erforderlich.

- Verwenden Sie keinen Ausdruck, der den Benutzer verantwortlich macht oder einen Benutzerfehler impliziert. Vermeiden Sie es, Sie und im Ausdruck zu verwenden. Obwohl die aktive Stimme im Allgemeinen bevorzugt wird, verwenden Sie die passive Stimme, wenn der Benutzer das Subjekt ist, und können sich für den Fehler verantwortlich machen, wenn die aktive Stimme verwendet wird.

**Falsch:**

![Screenshot der Meldung, die Sie bei der falschen Anmeldung eingegeben haben ](images/mess-error-image50.png)

**Richtig:**

![Screenshot der Nachricht: falsches Kennwort ](images/mess-error-image51.png)

Im falschen Beispiel wird der Benutzer mithilfe der aktiven Stimme dafür verantwortlich gemacht.

- **Seien Sie spezifisch.** Vermeiden Sie ungenaue Formulierungen, z. B. Syntaxfehler und unzulässige Operation. Geben Sie bestimmte Namen, Speicherorte und Werte der beteiligten Objekte an.

**Falsch:**

Die Datei wurde nicht gefunden.

Der Datenträger ist voll.

Der Wert liegt nicht im Bereich.

Das Zeichen ist ungültig.

Gerät nicht verfügbar.

Diese Probleme wären viel einfacher mit bestimmten Namen, Speicherorten und Werten zu lösen.

- **Geben Sie keine wahrscheinlich unwahrscheinlichen Probleme, Ursachen oder Lösungen, um spezifisch zu sein.** Geben Sie kein Problem, eine Ursache oder eine Lösung an, es sei denn, es ist wahrscheinlich richtig. Es ist beispielsweise besser zu sagen, dass ein unbekannter Fehler aufgetreten ist, als etwas, das wahrscheinlich ungenau ist.
- Vermeiden Sie das Wort **"bitte",** außer in Situationen, in denen der Benutzer aufgefordert wird, etwas Unwesentliches (z. B. Warten) zu tun, oder die Software für die Situation verantwortlich ist.

**Richtig:**

Warten Sie, während Windows die Dateien auf Ihren Computer kopiert.

- **Verwenden Sie das Wort "sorry"** nur in Fehlermeldungen, die zu schwerwiegenden Problemen für den Benutzer führen (z. B. Datenverlust oder Nichtnutzung des Computers). Bitte entlogen Sie sich nicht, wenn das Problem während der normalen Funktionsweise des Programms aufgetreten ist (z. B. wenn der Benutzer warten muss, bis eine Netzwerkverbindung gefunden wurde).

**Richtig:**

Leider hat Fabrikam Backup ein nicht behebbares Problem erkannt und wurde heruntergefahren, um Dateien auf Ihrem Computer zu schützen.

- **Verweisen Sie auf Produkte mit ihren Kurznamen.** Verwenden Sie keine vollständigen Produktnamen oder Markensymbole. Geben Sie den Unternehmensnamen nur an, wenn Benutzer den Unternehmensnamen dem Produkt zuordnen. Schließen Sie keine Programmversionsnummern ein.

**Falsch:**

![Screenshot: Meldung "Dieses Microsoft Office Outlook kann nicht geöffnet werden" ](images/mess-error-image52.png)

**Richtig:**

![Screenshot der Nachricht: Dieses Element kann nicht geöffnet werden ](images/mess-error-image53.png)

Im falschen Beispiel werden vollständige Produktnamen und Markensymbole verwendet.

- **Verwenden Sie doppelte Anführungszeichen um Objektnamen.** Dies erleichtert die Analyse des Texts und vermeidet potenziell peinliche Anweisungen.
  - **Ausnahme:** Vollqualifizierte Dateipfade, URLs und Domänennamen müssen nicht in doppelten Anführungszeichen enthalten sein.

**Richtig:**

![Screenshot der Nachricht: "Mein Haus" ist nicht verfügbar ](images/mess-error-image54.png)

In diesem Beispiel wäre die Fehlermeldung verwirrend, wenn der Objektname nicht in Anführungszeichen steht.

- **Vermeiden Sie das Starten von Sätzen mit Objektnamen.** Dies ist häufig schwierig zu analysieren.
- **Verwenden Sie keine Ausrufezeichen oder Wörter mit groß geschriebenen Buchstaben.** Ausrufezeichen und Großbuchstaben machen es so, als ob Sie den Benutzer anschreiten.

Weitere Richtlinien und Beispiele finden Sie unter [Stil und Ton.](text-style-tone.md)

**Titel**

- **Verwenden Sie den Titel, um den Befehl oder das Feature zu identifizieren, von dem der Fehler stammt.** Ausnahmen:
  - Wenn ein Fehler von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.
  - Wenn dieser Titel redundant oder verwirrend mit der Main-Anweisung wäre, verwenden Sie stattdessen den Programmnamen.
- **Verwenden Sie den Titel nicht, um das Problem** zu erläutern oder zusammenzufassen, das der Zweck der Hauptanweisung ist.

**Falsch:**

![Screenshot: Meldung "Neuer Ordner kann nicht umbenannt werden" ](images/mess-error-image55.png)

In diesem Beispiel wird der Titel fälschlicherweise verwendet, um das Problem zu erklären.

- Verwenden Sie die Groß-/Groß-/Formatvorlage, ohne die Interpunktion zu beenden.

**Hauptanweisungen**

- **Verwenden Sie die Main-Anweisung, um das Problem in einer eindeutigen, einfachen, spezifischen Sprache zu beschreiben.**
- **Seien Sie präzise, verwenden Sie nur einen einzelnen vollständigen Satz.** Sehen Sie sich die Hauptanweisung auf die wesentlichen Informationen an. Sie können den Betreff implizit be lassen, wenn es sich um Ihr Programm oder den Benutzer handelt. Geben Sie den Grund für das Problem an, wenn Sie dies präzise tun können. Wenn Sie mehr erklären müssen, verwenden Sie eine zusätzliche Anweisung.

**Falsch:**

![Screenshot der Meldung: Upgrade kann nicht installiert werden ](images/mess-error-image56.png)

In diesem Beispiel wird die gesamte Fehlermeldung in die Main-Anweisung eingelesen, was das Lesen schwierig macht.

- **Seien Sie spezifisch, wenn Objekte beteiligt sind, geben Sie ihre Namen an.**
- **Vermeiden Sie es, vollständige Dateipfade und URLs in die Hauptanweisung zu setzen.** Verwenden Sie stattdessen einen Kurznamen (z. B. den Dateinamen), und geben Sie den vollständigen Namen (z. B. den Dateipfad) in die ergänzende Anweisung ein. Sie können jedoch einen einzelnen vollständigen Dateipfad oder eine url in die Main-Anweisung eingeben, wenn die Fehlermeldung andernfalls keine zusätzliche Anweisung benötigt.

![Screenshot der Nachricht: Fabrikam-Datei kann nicht gelöscht werden ](images/mess-error-image57.png)

In diesem Beispiel befindet sich nur der Dateiname in der main-Anweisung. Der vollständige Pfad befindet sich in der ergänzenden Anweisung.

- **Geben Sie den vollständigen Dateipfad und die URL überhaupt nicht an, wenn dies aus dem Kontext offensichtlich ist.**

![Screenshot der Nachricht: Neuer Ordner kann nicht umbenannt werden ](images/mess-error-image58.png)

In diesem Beispiel umbenennt der Benutzer eine Datei aus Windows Explorer. In diesem Fall ist der vollständige Dateipfad nicht erforderlich, da er im Kontext offensichtlich ist.

- Verwenden Sie nach Möglichkeit present tense.
- Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
- Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine -Anweisung ist. Wenn es sich bei der Anweisung um eine Frage handelt, fügen Sie ein abschließendes Fragezeichen ein.

**Hauptanweisungsvorlagen**

Es gibt zwar keine strengen Regeln für den Ausdruck, aber verwenden Sie nach Möglichkeit die folgenden Hauptanweisungsvorlagen:

- [Optionaler Name des Betreffs] kann nicht [Aktion ausführen]
- [optionaler Name des Betreffs] kann [Aktion ausführen] nicht, da [Grund]
- [Optionaler Betreffname] kann [Aktion ausführen] nicht auf "[Objektname]"
- [optionaler Betreffname] kann [Aktion ausführen] nicht auf "[Objektname]" aus [Grund]
- Es ist nicht genügend [Ressource] vorhanden, um [Aktion ausführen]
- [Betreffname] ist für [Zweck] kein [Objektname] erforderlich.
- [Gerät oder Einstellung] ist deaktiviert, sodass [unerwünschte Ergebnisse]
- [Gerät oder Einstellung] ist nicht [verfügbar \| gefunden \| aktiviert \| aktiviert]
- "[Objektname]" ist derzeit nicht verfügbar.
- Der Benutzername oder das Kennwort ist falsch.
- Sie verfügen nicht über die Berechtigung für den Zugriff auf "[Objektname]".
- Sie haben keine Berechtigung zum Ausführen einer Aktion.
- [Programmname] hat ein schwerwiegendes Problem und muss sofort geschlossen werden.

Nehmen Sie natürlich nach Bedarf Änderungen vor, damit die Hauptanweisung grammatikalisch korrekt ist und den Richtlinien der Hauptanweisung entspricht.

**Zusätzliche Anweisungen**

- Verwenden Sie die ergänzende Anweisung für Folgendes:
  - Geben Sie zusätzliche Details zum Problem an.
  - Erläutern Sie die Ursache des Problems.
  - Listet die Schritte auf, die der Benutzer ausführen kann, um das Problem zu beheben.
  - Stellen Sie Maßnahmen bereit, um zu verhindern, dass das Problem erneut auftritt.
- **Schlagen Sie nach Möglichkeit eine praktische, hilfreiche Lösung vor, damit Benutzer das Problem beheben können.** Stellen Sie jedoch sicher, dass die vorgeschlagene Lösung das Problem wahrscheinlich löst. Verschwenden Sie die Zeit der Benutzer nicht, indem Sie mögliche, aber unwahrscheinliche Lösungen vorschlagen.

**Falsch:**

![Screenshot der Meldung: Nicht genügend Arbeitsspeicher ](images/mess-error-image59.png)

In diesem Beispiel sind das Problem und die empfohlene Lösung zwar möglich, aber sehr unwahrscheinlich.

- **Wenn das Problem ein falscher Wert ist, den der Benutzer eingegeben hat, verwenden Sie die ergänzende Anweisung, um die richtigen Werte zu erläutern.** Benutzer sollten diese Informationen nicht aus einer anderen Quelle bestimmen müssen.
- **Stellen Sie keine Lösung bereit, wenn sie einfach aus der Problem-Anweisung abgeleitet werden kann.**

![Screenshot der Meldung: Falscher Zeitwert ](images/mess-error-image33.png)

In diesem Beispiel ist keine zusätzliche Anweisung erforderlich. Die Lösung kann einfach aus der Problem-Anweisung abgeleitet werden.

- **Wenn die Lösung mehrere Schritte enthält, geben Sie die Schritte in der Reihenfolge an, in der sie abgeschlossen werden sollen.** Vermeiden Sie jedoch lösungen mit mehreren Schritten, da Benutzer Schwierigkeiten haben, sich mehr als zwei oder drei einfache Schritte zu merken. Wenn weitere Schritte erforderlich sind, lesen Sie das entsprechende Hilfethema.
- **Halten Sie zusätzliche Anweisungen kurz.** Geben Sie nur an, was Benutzer wissen müssen. Unnötige Details weglassen. Ziel: maximal drei Sätze mittlerer Länge.
- **Um Fehler zu vermeiden, während Benutzer Anweisungen ausführen, setzen Sie die Ergebnisse vor die Aktion.**

**Richtig:**

Klicken Sie auf OK, um Windows neu zu starten.

**Falsch:**

Klicken Sie auf OK, um Windows neu zu starten.

Im falschen Beispiel klicken Benutzer eher zufällig auf OK.

- **Es wird nicht empfohlen, sich an einen Administrator zu wenden, es sei denn, dies ist eine der wahrscheinlichsten Lösungen für das Problem.** Reservieren Sie solche Lösungen für Probleme, die wirklich nur von einem Administrator gelöst werden können.

**Falsch:**

![Screenshot der Meldung: Server nicht verfügbar ](images/mess-error-image60.png)

In diesem Beispiel liegt das Problem wahrscheinlich in der Netzwerkverbindung des Benutzers, sodass es sich nicht lohnt, sich an einen Administrator zu wenden.

- **Es wird nicht empfohlen, sich an den technischen Support zu wenden.** Die Option, sich an den technischen Support zu wenden, um ein Problem zu lösen, ist immer verfügbar und muss nicht durch Fehlermeldungen heraufgestuft werden. Konzentrieren Sie sich stattdessen auf das Schreiben hilfreicher Fehlermeldungen, damit Benutzer Probleme lösen können, ohne sich an den technischen Support wenden zu müssen.

**Falsch:**

![Screenshot: Meldung "Dieses Element kann nicht geöffnet werden" ](images/mess-error-image61.png)

In diesem Beispiel empfiehlt die Fehlermeldung fälschlicherweise, sich an den technischen Support zu wenden.

- Verwenden Sie vollständige Sätze, Groß- und Großschreibung im Satzstil und endende Interpunktion.

**Commitschaltflächen**

- Wenn die Fehlermeldung Befehlsschaltflächen oder Befehlslinks enthält, die das Problem lösen, befolgen Sie die entsprechenden Richtlinien in [Dialogfeldern.](win-dialog-box.md)
- Wenn das Programm aufgrund des Fehlers beendet werden muss, geben Sie die Schaltfläche Programm beenden an. Verwenden Sie zu diesem Zweck nicht Close, um Verwirrung zu vermeiden.
- Andernfalls geben Sie eine Schaltfläche Schließen an. Verwenden Sie ok nicht für Fehlermeldungen, da diese Formulierung impliziert, dass Probleme in Ordnung sind.
  - **Ausnahme:** Verwenden Sie OK, wenn Ihr Fehlerberichtsmechanismus feste Bezeichnungen aufweist (wie bei der MessageBox-API).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Fehler:

- Informationen zu Fehlern finden Sie in der Hauptanweisung. Wenn die Hauptanweisung lang oder ausführlich ist, fassen Sie sie zusammen.
- Bei Bedarf können Sie als Meldung auf ein Fehlermeldungsdialogfeld verweisen. Beziehen Sie sich nur in der Programmierung und anderen technischen Dokumentationen auf als Fehlermeldung.
- Formatieren Sie den Text nach Möglichkeit fett. Andernfalls setzen Sie den Text nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

**Beispiel:** Wenn Sie die Meldung **There is no CD disc in the drive (Es ist kein CD-Datenträger in der Laufwerkmeldung** vorhanden) erhalten, fügen Sie eine neue CD-Festplatte in das Laufwerk ein, und versuchen Sie es erneut.

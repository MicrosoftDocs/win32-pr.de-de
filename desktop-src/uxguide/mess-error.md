---
title: Fehlermeldungen (Entwurfsgrundlagen)
description: Eine Fehlermeldung warnt Benutzer über ein Problem, das bereits aufgetreten ist.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 50e9d945baf736329d38334a94ede6158621167c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984103"
---
# <a name="error-messages-design-basics"></a>Fehlermeldungen (Entwurfsgrundlagen)

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Eine Fehlermeldung warnt Benutzer über ein Problem, das bereits aufgetreten ist. Im Gegensatz dazu warnt eine Warnmeldung Benutzer über eine Bedingung, die in Zukunft zu einem Problem führen kann. Fehlermeldungen können über modale Dialogfelder, in-place-Nachrichten, Benachrichtigungen oder Sprechblasen angezeigt werden.

![Screenshot der Fehlermeldung: Kann nicht umbenannt werden](images/mess-error-image1.png)

Eine typische modale Fehlermeldung.

Effektive Fehlermeldungen informieren Benutzer darüber, dass ein Problem aufgetreten ist, erläutern, warum es aufgetreten ist, und stellen eine Lösung zur Verfügung, damit Benutzer das Problem beheben können. Benutzer sollten entweder eine Aktion ausführen oder ihr Verhalten als Ergebnis einer Fehlermeldung ändern.

Gut geschriebene, hilfreiche Fehlermeldungen sind entscheidend für eine hochwertige Benutzererfahrung. Schlecht geschriebene Fehlermeldungen führen zu einer niedrigen Produktzufriedenheit und sind eine führende Ursache für vermeidbare Kosten für den technischen Support. Unnötige Fehlermeldungen führen zu einem Fehler beim Benutzerfluss.

**Hinweis:** Richtlinien für [Dialogfelder,](win-dialog-box.md) [Warnmeldungen,](mess-warn.md) [Bestätigungen,](mess-confirm.md) [Standardsymbole,](vis-std-icons.md)Benachrichtigungen und [Layout](vis-layout.md) werden in separaten Artikeln dargestellt. [](mess-notif.md)

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

- **Liegt auf der Benutzeroberfläche ein Problem vor, das bereits aufgetreten ist?** Wenn dies nicht der Fehler ist, ist die Meldung kein Fehler. Wenn der Benutzer über eine Bedingung benachrichtigt wird, die in Zukunft ein Problem verursachen kann, verwenden Sie eine Warnmeldung.
- **Kann das Problem ohne Verwechslungen verhindert werden?** Falls ja, verhindern Sie stattdessen das Problem. Verwenden Sie beispielsweise Steuerelemente, die auf gültige Werte beschränkt sind, anstatt constrained-Steuerelemente zu verwenden, die möglicherweise Fehlermeldungen erfordern. Außerdem würde das Deaktivieren von Steuerelementen beim Klicken zu einem Fehler führen, solange offensichtlich ist, warum das Steuerelement deaktiviert ist.
- **Kann das Problem automatisch behoben werden?** Falls ja, behandeln Sie das Problem, und unterdrücken Sie die Fehlermeldung.
- **Werden Benutzer wahrscheinlich eine Aktion ausführen oder ihr Verhalten als Ergebnis der Nachricht ändern?** Ander denn, die Bedingung rechtfertigen keine Unterbrechung des Benutzers, daher ist es besser, den Fehler zu unterdrücken.
- **Ist das Problem relevant, wenn Benutzer aktiv andere Programme verwenden?** Falls ja, sollten Sie das Problem mithilfe eines [Benachrichtigungsbereichssymbols anzeigen.](winenv-notification.md)
- **Bezieht sich das Problem nicht auf die aktuelle Benutzeraktivität, erfordert es keine sofortige Benutzeraktion und kann benutzer es frei ignorieren?** Wenn dies der Fehler ist, verwenden Sie [stattdessen eine Aktionsfehlerbenachrichtigung.](mess-notif.md)
- **Bezieht sich das Problem auf den Status einer Hintergrundaufgabe innerhalb eines primären Fensters?** Falls ja, sollten Sie das Problem mithilfe einer [Statusleiste anzeigen.](ctrl-status-bars.md)
- **Sind die primären Zielbenutzer IT-Experten?** Falls ja, sollten Sie einen alternativen Feedbackmechanismus verwenden, z. B. [Protokolldateieinträge](glossary.md) oder E-Mail-Warnungen. IT-Experten bevorzugen Protokolldateien für nicht kritische Informationen.

## <a name="design-concepts"></a>Entwurfskonzepte

**Die Merkmale schlechter Fehlermeldungen**

Es sollte nicht überraschend sein, dass es viele lästige, nicht hilfreiche und schlecht geschriebene Fehlermeldungen gibt. Und da Fehlermeldungen häufig mit modalen Dialogen angezeigt werden, unterbrechen sie die aktuelle Aktivität des Benutzers und fordern, bestätigt zu werden, bevor der Benutzer fortfahren kann.

Ein Teil des Problems ist, dass es so viele Möglichkeiten gibt, dies falsch zu machen. Betrachten Sie diese Beispiele aus der Error Message Hall of 100:

**Unnötige Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: Anwendung fehlgeschlagen ](images/mess-error-image2.png)

Dieses Beispiel aus Windows XP ist möglicherweise die schlechteste Fehlermeldung, die jemals aufgetreten ist. Es gibt an, dass ein Programm nicht gestartet werden konnte, Windows programm selbst gerade heruntergefahren wird. Es gibt nichts, was der Benutzer tun kann oder auch nur tun möchte (der Benutzer hat sich entschieden, die Windows zu beenden). Und durch das Anzeigen dieser Fehlermeldung verhindert Windows, dass er selbst heruntergefahren wird!

**Das Problem:** Die Fehlermeldung selbst ist das Problem. Abgesehen davon, dass die Fehlermeldung verworfen wird, müssen Benutzer nichts tun.

**Führende Ursache:** Melden aller Fehlerfälle, unabhängig von den Zielen oder der Sicht der Benutzer.

**Empfohlene Alternative:** Melden Sie keine Fehler, die Benutzern egal sind.

**Fehlermeldungen "Erfolgreich"**

**Falsch:**

![Screenshot der Fehlermeldung: Entfernungsfehler ](images/mess-error-image3.png)

Diese Fehlermeldung ist darauf aufgetreten, dass der Benutzer die Anwendung nicht Windows nach dem Entfernen des Programms neu gestartet hat. Das Entfernen des Programms war aus Sicht des Benutzers erfolgreich.

**Das Problem:** Aus Sicht des Benutzers ist kein Fehler aufgetreten. Abgesehen davon, dass die Fehlermeldung verworfen wird, müssen Benutzer nichts tun.

**Führende Ursache:** Die Aufgabe wurde aus Sicht des Benutzers erfolgreich abgeschlossen, aber aus Sicht des Deinstallationsprogramms ist ein Fehler fehlgeschlagen.

**Empfohlene Alternative:** Melden Sie keine Fehler für Bedingungen, die Benutzer als akzeptabel betrachten.

**Vollständig unbnbare Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: Unbekannter Fehler ](images/mess-error-image4.png)

Benutzer erfahren, dass ein Fehler aufgetreten ist, haben aber keine Vorstellung davon, was der Fehler war oder wie er zu tun ist. Und nein, das ist nicht in Ordnung!

**Das Problem:** Die Fehlermeldung gibt kein bestimmtes Problem aus, und es gibt nichts, was Benutzer tun können.

**Führende Ursache:** Höchstwahrscheinlich verfügt das Programm über eine schlechte Fehlerbehandlung.

**Empfohlene Alternative:** Entwerfen Sie eine gute Fehlerbehandlung im Programm.

**Unverständliche Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: Sicherung nicht abgeschlossen ](images/mess-error-image5.png)

In diesem Beispiel ist die Problemerklärung klar, aber die ergänzende Erklärung ist völlig unklar.

**Das Problem:** Die Problemerklärung oder -lösung ist nicht verständlich.

**Führende Ursache:** Erläuterung des Problems aus der Sicht des Codes anstelle der des Benutzers.

**Empfohlene Alternative:** Schreiben Sie Fehlermeldungstext, den Ihre Zielbenutzer leicht verstehen können. Stellen Sie Lösungen zur Verfügung, die Benutzer tatsächlich ausführen können. Entwerfen Sie die Fehlermeldungserfahrung Ihres Programms, ohne dass Programmierer Fehlermeldungen vor Ort verfassen.

**Fehlermeldungen, die zu viele Nachrichten enthalten**

**Falsch:**

![Screenshot der äußerst ausführlichen Meldung ](images/mess-error-image6.png)

In diesem Beispiel versucht die Fehlermeldung scheinbar, jeden Problembehandlungsschritt zu erläutern.

**Das Problem:** Zu viele Informationen.

**Führende Ursache:** Geben Sie zu viele Details an, oder versuchen Sie, einen komplizierten Problembehandlungsprozess innerhalb einer Fehlermeldung zu erklären.

**Empfohlene Alternative:** Vermeiden Sie unnötige Details. Vermeiden Sie außerdem Problembehandlungen. Wenn eine Problembehandlung erforderlich ist, konzentrieren Sie sich auf die wahrscheinlichsten Lösungen, und erläutern Sie den Rest, indem Sie einen Link zum entsprechenden Thema in der Hilfe verwenden.

**Unnötigerweise fehlerverlässig**

**Falsch:**

![Screenshot der Nachricht: Objekt nicht finden ](images/mess-error-image7.png)

Die Unfähigkeit des Programms, ein Objekt zu finden, klingt unerhört wie eine Katastrophe. Und unter der Annahme, dass es sich um eine schwerwiegende Situation handelt, warum ist die Antwort OK?

**Das Problem:** Der Ton des Programms ist unnötig lässig oder drastisch.

**Führende Ursache:** Das Problem ist auf einen Fehler zurück, der aus Sicht des Programms schwerwiegender erscheint.

**Empfohlene Alternative:** Wählen Sie die Sprache basierend auf dem Standpunkt des Benutzers sorgfältig aus.

**Fehlermeldungen, die Benutzern die Vorwürfe machen**

**Falsch:**

![Screenshot der Nachricht: ungültiges Zeichen ](images/mess-error-image8.png)

Warum haben Benutzer das Gefühl, dass sie sich als ein Verskribungsbenutzer fühlen?

**Das Problem:** Die Fehlermeldung wird so formuliert, dass der Benutzer einen Fehler macht.

**Führende Ursache:** Nicht beachteter Ausdruck, der sich auf das Verhalten des Benutzers und nicht auf das Problem konzentriert.

**Empfohlene Alternative:** Konzentrieren Sie sich auf das Problem, nicht auf die Benutzeraktion, die zu dem Problem geführt hat, indem Sie bei Bedarf die passive Stimme verwenden.

**Silly-Fehlermeldungen**

**Falsch:**

![Screenshot der Meldung: Fehler im Fehlerbericht ](images/mess-error-image9.png)

In diesem Beispiel ist die Problem-Anweisung ziemlich ironisch, und es werden keine Lösungen bereitgestellt.

**Das Problem:** Fehlermeldungen, die silly oder nicht sequitors sind.

**Führende Ursache:** Erstellen von Fehlermeldungen, ohne auf ihren Kontext zu achten.

**Empfohlene Alternative:** Lassen Sie Ihre Fehlermeldungen von einem Writer erstellt und überprüft werden. Berücksichtigen Sie beim Überprüfen der Fehler den Kontext und den Berücksichtigungszustand des Benutzers.

**Fehlermeldungen des Programmierers**

**Falsch:**

![Screenshot der Nachricht: Adresse der Zugriffsverletzung ](images/mess-error-image10.png)

In diesem Beispiel gibt die Fehlermeldung an, dass das Programm einen Fehler enthält. Diese Fehlermeldung hat nur für den Programmierer Bedeutung.

**Das Problem:** Meldungen, die den Entwicklern des Programms helfen sollen, Fehler zu finden, bleiben in der Releaseversion des Programms erhalten. Diese Fehlermeldungen haben keine Bedeutung oder keinen Wert für Benutzer.

**Führende Ursache:** Programmierer, die die normale Benutzeroberfläche verwenden, um Nachrichten an sich selbst zu senden.

**Empfohlene Alternative:** Entwickler müssen alle diese Nachrichten bedingt kompilieren, damit sie automatisch aus der Releaseversion eines Produkts entfernt werden. Verschwenden Sie keine Zeit damit, Fehler wie diese für Benutzer zu machen, da ihre einzige Zielgruppe die Programmierer ist.

**Schlecht angezeigte Fehlermeldungen**

**Falsch:**

![Screenshot der Nachricht: Unerwarteter Fehler ](images/mess-error-image11.png)

Dieses Beispiel hat viele häufige Präsentationsfehler.

**Das Problem:** Abrufen aller Details, die in der Fehlermeldungspräsentation falsch sind.

**Führende Ursache:** Die Richtlinien für Fehlermeldungen sind nicht zu kennen und gelten nicht. Verwenden Sie keine Writer und Editoren, um die Fehlermeldungen zu erstellen und zu überprüfen.

Die Art der Fehlerbehandlung ist so, dass viele dieser Fehler sehr einfach zu machen sind. Es ist lässend zu erkennen, dass es sich bei den meisten Fehlermeldungen um Lässungen für die Hall of Zun geerbt haben könnte.

**Die Merkmale von guten Fehlermeldungen**

Im Gegensatz zu den vorherigen schlechten Beispielen haben gute Fehlermeldungen:

- **Ein Problem.** Gibt an, dass ein Problem aufgetreten ist.
- **Eine Ursache.** Erklärt, warum das Problem aufgetreten ist.
- **Eine Lösung.** Stellt eine Lösung zur Verfügung, damit Benutzer das Problem beheben können.

Darüber hinaus werden gute Fehlermeldungen in einer Weise angezeigt, die wie dies ist:

- **Relevanten.** Die Meldung stellt ein Problem dar, das für Benutzer von Bennen ist.
- **Umsetzbare.** Benutzer sollten entweder eine Aktion ausführen oder ihr Verhalten als Ergebnis der Nachricht ändern.
- **Benutzerzentriert.** Die Meldung beschreibt das Problem in Bezug auf Zielbenutzeraktionen oder -ziele, nicht in Bezug auf die Unfreundlichkeit des Codes.
- **Kurze.** Die Nachricht ist so kurz wie möglich, aber nicht kürzer.
- **Klar.** Die Nachricht verwendet Nur-Sprache, damit die Zielbenutzer das Problem und die Lösung leicht verstehen können.
- **Bestimmten.** Die Meldung beschreibt das Problem mithilfe einer bestimmten Sprache und gibt bestimmte Namen, Speicherorte und Werte der beteiligten Objekte an.
- **Höflich.** Den Benutzern sollte nicht die Vorwürfe gemacht oder gemacht werden, dass sie sich ungnädig fühlen.
- **Selten.** Wird selten angezeigt. Häufig angezeigte Fehlermeldungen sind ein Anzeichen für einen fehlerhaften Entwurf.

Indem Sie Ihre Fehlerbehandlung so gestalten, dass sie diese Merkmale aufweist, können Sie die Fehlermeldungen Ihres Programms aus der Error Message Hall of 1007 heraushalten.

**Vermeiden unnötiger Fehlermeldungen**

Häufig ist die beste Fehlermeldung keine Fehlermeldung. Viele Fehler können durch einen besseren Entwurf vermieden werden, und es gibt häufig bessere Alternativen zu Fehlermeldungen. Es ist in der Regel besser, einen Fehler zu verhindern, als einen Fehler zu melden.

Die offensichtlichsten Fehlermeldungen, die vermieden werden sollten, sind solche, die nicht umsetzbar sind. Wenn Benutzer die Nachricht wahrscheinlich verlassen, ohne etwas zu tun oder zu ändern, sollten Sie die Fehlermeldung weglassen.

Einige Fehlermeldungen können entfernt werden, da sie aus Sicht des Benutzers keine Probleme sind. Angenommen, der Benutzer hat versucht, eine Datei zu löschen, die bereits gelöscht wird. Obwohl dies aus Codesicht ein unerwarteter Fall sein kann, betrachten Benutzer dies nicht als Fehler, da das gewünschte Ergebnis erreicht wird.

**Falsch:**

![Screenshot der Nachricht: Datei kann nicht gelöscht werden ](images/mess-error-image12.png)

Diese Fehlermeldung sollte entfernt werden, da die Aktion aus Sicht des Benutzers erfolgreich war.

Angenommen, der Benutzer bricht eine Aufgabe explizit ab. Aus Sicht des Benutzers ist die folgende Bedingung kein Fehler.

**Falsch:**

![Screenshot der Meldung: Sicherung kann nicht abgeschlossen werden ](images/mess-error-image13.png)

Diese Fehlermeldung sollte ebenfalls entfernt werden, da die Aktion aus Sicht des Benutzers erfolgreich war.

Manchmal können Fehlermeldungen beseitigt werden, indem der Fokus auf die Ziele der Benutzer und nicht auf die Technologie gesetzt wird. Überlegen Sie dabei, was ein Fehler tatsächlich ist. Liegt das Problem mit den Zielen des Benutzers oder der Fähigkeit Ihres Programms, diese zu erfüllen? Wenn die Aktion des Benutzers in der realen Welt sinnvoll ist, sollte sie auch in der Software sinnvoll sein.

Angenommen, in einem E-Commerce-Programm versucht ein Benutzer, ein Produkt mithilfe der Suche zu finden, aber die literale Suchabfrage hat keine Übereinstimmungen, und das gewünschte Produkt ist nicht auf Lager. Technisch gesehen ist dies ein Fehler, aber anstatt eine Fehlermeldung zu geben, könnte das Programm:

- Suchen Sie weiterhin nach Produkten, die der Abfrage am besten entsprechen.
- Wenn die Suche offensichtliche Fehler enthält, empfehlen Sie automatisch eine korrigierte Abfrage.
- Behandeln Sie häufige Probleme automatisch, z. B. Rechtschreibfehler, alternative Schreibweisen und nicht übereinstimmende Pluralisierungs- und Verbfälle.
- Geben Sie an, wann das Produkt vor lagert.

Solange die Anforderung des Benutzers angemessen ist, sollte ein gut entworfenes E-Commerce-Programm angemessene Ergebnisse und keine Fehler zurückgeben.

Eine weitere hervorragende Möglichkeit, Fehlermeldungen zu vermeiden, besteht in der Vermeidung von Problemen. Sie können Fehler verhindern, indem Sie:

- **Verwenden von eingeschränkten Steuerelementen.** Verwenden Sie Steuerelemente, die auf gültige Werte beschränkt sind. Steuerelemente wie Listen, Schieberegler, Kontrollkästchen, Optionsfelder und Datums- und Uhrzeitauswahl sind auf gültige Werte beschränkt, während Textfelder häufig nicht sind und möglicherweise Fehlermeldungen erfordern. Sie können Textfelder jedoch so einschränken, dass sie nur bestimmte Zeichen akzeptieren und eine maximale Anzahl von Zeichen akzeptieren.
- **Verwenden eingeschränkter Interaktionen.** Lassen Sie für Ziehvorgänge zu, dass Benutzer nur auf gültigen Zielen ablegen.
- **Verwenden deaktivierter Steuerelemente und Menüelemente.** Deaktivieren Sie Steuerelemente und Menüelemente, wenn Benutzer leicht erkennen können, warum das Steuerelement oder Menüelement deaktiviert ist.
- **Bereitstellen guter Standardwerte.** Benutzer machen weniger Eingabefehler, wenn sie die Standardwerte akzeptieren können. Selbst wenn benutzer sich entscheiden, den Wert zu ändern, informiert der Standardwert Benutzer über das erwartete Eingabeformat.
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
- **Warnung.** "Diese Seite verhält sich möglicherweise nicht wie erwartet, da Windows Internet Explorer nicht zum Laden von nicht signierten ActiveX konfiguriert ist." oder "Zulassen, dass auf dieser Seite ein nicht signiertes ActiveX wird? Dies aus nicht vertrauenswürdigen Quellen kann Ihren Computer schaden." (Beide werden als Bedingungen formuliert, die zukünftige Probleme verursachen können.)
- **Informationen.** "Sie haben die Windows Internet Explorer, um nicht signierte ActiveX zu blockieren." (Wird als Faktenauszug formuliert.)

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

Modale Dialoge sind eine gute Wahl, wenn der Benutzer das Problem unmittelbar vor dem Fortfahren bestätigen muss, andernfalls aber häufig eine schlechte Wahl. Im Allgemeinen sollten Sie die darstellung mit der geringsten Gewichtung bevorzugen, die die Aufgabe gut macht.

**Vermeiden von Überkommunikation**

Im Allgemeinen [lesen Benutzer nicht, sie scannen](vis-layout.md). Desto mehr Text gibt es, desto schwieriger ist es, den Text zu scannen, und desto wahrscheinlicher lesen Benutzer den Text überhaupt nicht. Daher ist es wichtig, den Text auf das Wesentliche zu reduzieren und bei Bedarf progressive Offenlegungs- und Hilfelinks zu verwenden, um zusätzliche Informationen zur Verfügung zu stellen.

Es gibt viele extreme Beispiele, aber sehen wir uns ein typisches beispiel an. Das folgende Beispiel enthält die meisten Attribute einer guten Fehlermeldung, aber der Text ist nicht präzise und erfordert eine Motivation zum Lesen.

**Falsch:**

![Screenshot der ausführlichen Meldung ](images/mess-error-image23.png)

Dieses Beispiel ist eine gute Fehlermeldung, aber es wird zu viele Nachrichten ausgegeben.

Was ist der ganze Text, der wirklich sagt? Ungefähr so wie hier gezeigt:

**Richtig:**

![Screenshot der Nachricht: CD-Aufzeichnung nicht erkannt ](images/mess-error-image24.png)

Diese Fehlermeldung enthält im Wesentlichen die gleichen Informationen, ist aber viel präziser.

Mithilfe der Hilfe zur Bereitstellung der Details verfügt diese Fehlermeldung über eine [invertierte Pyramidendarstellung.](text-ui.md)

Weitere Richtlinien und Beispiele zur Überkommunikation finden Sie unter [Benutzeroberfläche Text](text-ui.md).

**Wenn Sie nur acht Dinge tun**

1. Entwerfen Sie Ihr Programm für die Fehlerbehandlung.
2. Geben Sie keine unnötigen Fehlermeldungen an.
3. Vermeiden Sie Benutzerverwechslungen, indem Sie die erforderlichen Fehlermeldungen senden.
4. Stellen Sie sicher, dass die Fehlermeldung ein Problem, eine Ursache und eine Lösung liefert.
5. Stellen Sie sicher, dass die Fehlermeldung relevant, umsetzbar, kurz, klar, spezifisch, zufällig und selten ist.
6. Entwerfen Sie Fehlermeldungen aus Sicht des Benutzers, nicht aus sicht des Programms.
7. Verwenden Sie für jede erkennbare Ursache keine andere Fehlermeldung, wenn Sie den Benutzer in die Problembehandlung mit einverursachen.
8. Verwenden Sie die leichteste Präsentationsmethode, die die Aufgabe gut übernimmt.

**Verwendungsmuster**

Fehlermeldungen haben mehrere Verwendungsmuster:


| Bezeichnung | Wert |
|--------|-------|
| <strong>Systemprobleme</strong><br /> Das Betriebssystem, Hardwaregerät, Netzwerk oder Programm ist ausgefallen oder befindet sich nicht im Zustand, der zum Ausführen einer Aufgabe erforderlich ist. <br /> | Viele Systemprobleme können vom Benutzer gelöst werden: <br /><ul><li>Geräteprobleme können durch Einschalten des Geräts, erneutes Verbinden des Geräts und Einfügen von Medien gelöst werden.</li><li>Netzwerkprobleme können durch Überprüfen der physischen Netzwerkverbindung und Ausführen von <strong>Netzwerkdiagnose und -reparatur gelöst werden.</strong></li><li>Programmprobleme können gelöst werden, indem Programmoptionen geändert oder das Programm neu gestartet wird.</li></ul><img src="images/mess-error-image25.png" alt="Screen shot of message: Can't find a camera " /><br /> In diesem Beispiel kann das Programm keine Kamera finden, um eine Benutzeraufgabe auszuführen.<br /><img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br /> In diesem Beispiel muss ein Feature aktiviert werden, das zum Ausführen einer Aufgabe erforderlich ist.<br /> | 
| <strong>Dateiprobleme</strong><br /> Eine Datei oder ein Ordner, die für eine vom Benutzer initiierte Aufgabe erforderlich ist, wurde nicht gefunden, wird bereits verwendet oder hat nicht das erwartete Format. <br /> | <img src="images/mess-error-image27.png" alt="Screen shot of message: Can't delete file " /><br /> In diesem Beispiel kann die Datei oder der Ordner nicht gelöscht werden, da sie nicht gefunden wurde.<br /><img src="images/mess-error-image28.png" alt="Screen shot of message: Can't play this file " /><br /> In diesem Beispiel unterstützt das Programm das gegebene Dateiformat nicht.<br /> | 
| <strong>Sicherheitsprobleme</strong><br /> Der Benutzer verfügt nicht über die Berechtigung für den Zugriff auf eine Ressource oder über ausreichende Berechtigungen zum Ausführen einer vom Benutzer initiierten Aufgabe. <br /> | <img src="images/mess-error-image29.png" alt="Screen shot of message: You don't have permission " /><br /> In diesem Beispiel verfügt der Benutzer nicht über die Berechtigung für den Zugriff auf eine Ressource.<br /><img src="images/mess-error-image30.png" alt="Screen shot of message: You don't have privilege " /><br /> In diesem Beispiel hat der Benutzer nicht die Berechtigung, eine Aufgabe auszuführen.<br /> | 
| <strong>Aufgabenprobleme</strong><br /> Es liegt ein bestimmtes Problem beim Ausführen einer vom Benutzer initiierten Aufgabe vor (mit Einem anderen System, einer nicht gefundenen Datei, einem Dateiformat oder einem Sicherheitsproblem). <br /> | <img src="images/mess-error-image31.png" alt="Screen shot of message: Data can't be pasted " /><br /> In diesem Beispiel können die Zwischenablagedaten nicht in die Paint.<br /><img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can't be installed " /><br /> In diesem Beispiel kann der Benutzer kein Softwareupgrade installieren.<br /> | 
| <strong>Benutzereingabeprobleme</strong><br /> Der Benutzer hat einen Wert eingegeben, der falsch oder inkonsistent mit anderen Benutzereingaben ist. <br /> | <img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br /> In diesem Beispiel hat der Benutzer einen falschen Zeitwert eingegeben.<br /><img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br /> In diesem Beispiel hat die Benutzereingabe nicht das richtige Format.<br /> | 


## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

- **Verwenden Sie Taskdialoge, wenn dies angemessen ist,** um ein konsistentes Aussehen und Layout zu erzielen. Taskdialogfelder erfordern Windows Vista oder höher, sodass sie nicht für frühere Versionen von Windows. Wenn Sie ein Meldungsfeld verwenden müssen, trennen Sie die Hauptanweisung von der ergänzenden Anweisung durch zwei Zeilenumbrüche.

### <a name="user-input-errors"></a>Benutzereingabefehler

- **Verhindern oder reduzieren Sie Benutzereingabefehler nach Möglichkeit durch:**
  - Verwenden von Steuerelementen, die auf gültige Werte beschränkt sind.
  - Das Deaktivieren von Steuerelementen und Menüelementen beim Klicken würde zu einem Fehler führen, solange offensichtlich ist, warum das Steuerelement oder Menüelement deaktiviert ist.
  - Bereitstellen guter Standardwerte.

**Falsch:**

![Screenshot des Textfelds mit Sprecherlautstärkebeschriftung ](images/mess-error-image35.png)

In diesem Beispiel wird ein nicht eingeschränktes Textfeld für eingeschränkte Eingaben verwendet. Verwenden Sie stattdessen einen Schieberegler.

- **Verwenden Sie die moduslose Fehlerbehandlung (Fehler oder Sprechblasen) für kontextbezogene Benutzereingabeprobleme.**
- **Verwenden Sie Sprechblasen** für nicht kritische Einzelpunkt-Benutzereingabeprobleme, die während eines Textfelds oder unmittelbar nach dem Verlust des Fokus durch ein Textfeld erkannt wurden. [Für](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) Sprechblasen ist kein verfügbarer Bildschirmbereich oder das dynamische Layout erforderlich, das zum Anzeigen von meldungen an Ort und Stelle erforderlich ist. Zeigt immer nur einen einzelnen Balloon an. Da das Problem nicht kritisch ist, ist kein Fehlersymbol erforderlich. Sprechblasen gehen beim Klicken, beim Beheben des Problems oder nach einem Timeout weg.

![Screenshot der Nachricht: falsches Zeichen ](images/mess-error-image36.png)

In diesem Beispiel weist eine Sprechblase auf ein Eingabeproblem hin, das sich noch im Steuerelement befing.

- **Verwenden Sie für die verzögerte Fehlererkennung** Dies sind in der Regel Fehler, die durch Klicken auf eine Commitschaltfläche gefunden werden. (Verwenden Sie keine [direkt verfügbaren Fehler für](glossary.md) Einstellungen, für die sofort ein Committed erfolgt.) Es können mehrere Fehler gleichzeitig auftreten. Verwenden Sie normalen Text und ein 16 x 16 Pixel großes Fehlersymbol, und platzieren Sie sie nach Möglichkeit direkt neben dem Problem. Direkt aufgetretene Fehler werden nur dann entfernt, wenn der Benutzer committ und keine anderen Fehler gefunden werden.

![Screenshot der Nachricht: falsche E-Mail-Adresse ](images/mess-error-image37.png)

In diesem Beispiel wird für einen Fehler, der durch Klicken auf die Schaltfläche "Commit" gefunden wurde, ein fehlerfehler verwendet.

- **Verwenden Sie die modale** Fehlerbehandlung (Aufgabendialogfelder oder Meldungsfelder) für alle anderen Probleme, einschließlich Fehler, die mehrere Steuerelemente umfassen oder nicht kontextbezogene oder nicht eingabebezogene Fehler sind, die durch Klicken auf eine Commitschaltfläche gefunden werden.
- **Wenn ein Benutzereingabeproblem gemeldet wird, legen Sie den Eingabefokus auf das erste Steuerelement mit den falschen Daten fest.** Scrollen Sie das Steuerelement bei Bedarf in die Ansicht. Wenn das Steuerelement ein Textfeld ist, wählen Sie den gesamten Inhalt aus. Es sollte immer offensichtlich sein, worauf die Fehlermeldung verweist.
- **Löschen Sie nicht die falsche Eingabe.** Lassen Sie es stattdessen so, dass der Benutzer das Problem sehen und beheben kann, ohne von vorn zu beginnen.
  - **Ausnahme:** Löschen Sie falsche Kennwort- und PIN-Textfelder, da Benutzer maskierte Eingaben nicht effektiv korrigieren können.

### <a name="troubleshooting"></a>Problembehandlung

- **Vermeiden Sie das Erstellen von Problemen bei der Problembehandlung.** Verlassen Sie sich nicht auf eine einzelne Fehlermeldung, um ein Problem mit verschiedenen erkennbaren Ursachen zu melden.
- **Verwenden Sie für jede erkennbare Ursache eine andere Fehlermeldung (in der Regel eine andere ergänzende Anweisung).** Wenn eine Datei beispielsweise aus verschiedenen Gründen nicht geöffnet werden kann, geben Sie für jeden Grund eine separate ergänzende Anweisung an.
- **Verwenden Sie eine Meldung mit mehreren Ursachen nur, wenn die spezifische Ursache nicht bestimmt werden kann.** Stellen Sie in diesem Fall die Lösungen in der Reihenfolge vor, mit der das Problem wahrscheinlich behoben werden kann. Auf diese Weise können Benutzer das Problem effizienter lösen.

### <a name="icons"></a>Symbole

- **Modale Fehlermeldungsdialogfelder verfügen nicht über Titelleistensymbole.** Titelleistensymbole werden als visuelle Unterscheidung zwischen primären und sekundären Fenstern verwendet.
- **Verwenden Sie ein Fehlersymbol.** Ausnahmen:
  - Wenn es sich bei dem Fehler um ein Benutzereingabeproblem handelt, das über ein modales Dialogfeld oder eine Sprechblase angezeigt wird, verwenden Sie kein Symbol. Dies entspricht dem ermutigenden Ton der Windows. Für direkt angezeigte Fehlermeldungen sollte jedoch ein kleines Fehlersymbol (16 x 16 Pixel) verwendet werden, um sie eindeutig als Fehlermeldungen zu identifizieren.

     ![Screenshot der Meldung mit falschem Postformat](images/mess-error-image38.png)

     ![Screenshot: Name des Meldungscomputers zu lang](images/mess-error-image39.png)

     In diesen Beispielen benötigen Benutzereingabeprobleme keine Fehlersymbole.

     ![Screenshot: Falsches Format der Telefonnummer der Nachricht](images/mess-error-image40.png)

     In diesem Beispiel benötigt eine direkt angezeigte Fehlermeldung ein kleines Fehlersymbol, um sie eindeutig als Fehlermeldung zu identifizieren.

- Wenn das Problem für ein Feature mit einem Symbol (und nicht einem Benutzereingabeproblem) auftritt, können Sie das Featuresymbol mit einer Fehlerüberlagerung verwenden. Verwenden Sie in diesem Beispiel auch den Funktionsnamen als Fehlerthema.

    ![Screenshotnachricht: Media Player kann Datei nicht wiedergeben ](images/mess-error-image41.png)

    In diesem Beispiel weist das Featuresymbol eine Fehlerüberlagerung auf, und das Feature ist das Subjekt des Fehlers.

- **Verwenden Sie keine Warnsymbole für Fehler.** Dies geschieht häufig, um die Darstellung weniger schwerwiegend zu gestalten. Fehler sind keine Warnungen.

    **Falsch:**

    ![Screenshot: Schnelles Wechseln der Nachricht nicht aktiviert ](images/mess-error-image42.png)

    In diesem Beispiel wird fälschlicherweise ein Warnsymbol verwendet, damit der Fehler weniger schwerwiegend ist.

Weitere Richtlinien und Beispiele finden Sie unter [Standardsymbole.](vis-std-icons.md)

### <a name="progressive-disclosure"></a>Schrittweise Offenlegung

- **Verwenden Sie eine Schaltfläche details progressive Offenlegung anzeigen/ausblenden, um erweiterte oder detaillierte Informationen in einer Fehlermeldung auszublenden.** Dadurch wird die Fehlermeldung für die typische Verwendung vereinfacht. Blenden Sie die benötigten Informationen nicht aus, da benutzer sie möglicherweise nicht finden.

![Screenshot der Meldung: ActiveSync kann sich nicht anmelden ](images/mess-error-image43.png)

In diesem Beispiel hilft die Schaltfläche für die progressive Offenlegung Benutzern, einen Drilldown zu weiteren Details zu ermöglichen, wenn sie dies wünschen, oder vereinfacht die Benutzeroberfläche, falls sie dies nicht tun.

- **Verwenden Sie Details nicht anzeigen/ausblenden, es sei denn, es gibt wirklich mehr Details.** Stellen Sie nicht einfach die vorhandenen Informationen in einem ausführlicheren Format wieder her.
- **Verwenden Sie details nicht anzeigen/ausblenden, um Hilfeinformationen anzuzeigen.** Verwenden Sie stattdessen Hilfelinks.

Informationen zu Bezeichnungsrichtlinien finden Sie unter Steuerungen für [die progressive Offenlegung.](ctrl-progressive-disclosure-controls.md)

**Diese Meldung nicht erneut anzeigen**

- **Wenn eine Fehlermeldung diese Option benötigt, überprüfen Sie den Fehler und seine Häufigkeit.** Wenn er alle Merkmale eines guten Fehlers aufweist (relevant, umsetzbar und selten), sollte es für Benutzer nicht sinnvoll sein, ihn zu unterdrücken.

Weitere Richtlinien finden Sie unter [Dialogfelder](win-dialog-box.md).

### <a name="default-values"></a>Standardwerte

- **Wählen Sie die sicherste, am wenigsten destruktive oder sicherste Antwort als Standard aus.** Wenn sicherheit kein Faktor ist, wählen Sie den wahrscheinlichsten oder bequemsten Befehl aus.

### <a name="help"></a>Hilfe

- **Entwerfen Sie Fehlermeldungen, um Hilfe zu vermeiden.** Normalerweise sollten Benutzer keinen externen Text lesen müssen, um das Problem zu verstehen und zu lösen, es sei denn, die Lösung erfordert mehrere Schritte.
- **Stellen Sie sicher, dass der Hilfeinhalt relevant und hilfreich ist.** Es sollte sich nicht um eine ausführliche Neubelegung der Fehlermeldung, sondern um nützliche Informationen handelt, die außerhalb des Gültigkeitsbereichs der Fehlermeldung liegen, z. B. Möglichkeiten, das Problem in Zukunft zu vermeiden. Geben Sie keinen Hilfelink an, nur weil Sie dies tun können.
- **Verwenden Sie spezifische, präzise, relevante Hilfelinks, um auf Hilfeinhalte zuzugreifen.** Verwenden Sie zu diesem Zweck keine Befehlsschaltflächen oder die progressive Offenlegung.
- **Für Fehlermeldungen, die Sie nicht spezifisch und handlungsfähig machen können, sollten Sie Links zu Onlinehilfeinhalten bereitstellen.** Auf diese Weise können Sie Benutzern zusätzliche Informationen bereitstellen, die Sie nach der Veröffentlichung des Programms aktualisieren können.

Weitere Richtlinien finden Sie unter [Hilfe.](winenv-help.md)

### <a name="error-codes"></a>Fehlercodes

- **Bei Fehlermeldungen, die Sie nicht spezifisch und handlungsfähig machen können oder die von der Hilfe profitieren, sollten Sie auch Fehlercodes bereitstellen.** Benutzer verwenden diese Fehlercodes häufig, um im Internet nach zusätzlichen Informationen zu suchen.
- **Geben Sie immer eine Textbeschreibung des Problems und der Lösung an.** Verlassen Sie sich zu diesem Zweck nicht nur auf den Fehlercode.

**Falsch:**

![Screenshot der Meldung: Datei kann nicht geöffnet werden ](images/mess-error-image44.png)

In diesem Beispiel wird ein Fehlercode als Ersatz für einen Projektmappentext verwendet.

- **Weisen Sie für jede unterschiedliche Ursache einen eindeutigen Fehlercode zu.** Dadurch wird die Problembehandlung vermieden.
- **Wählen Sie Fehlercodes aus, die im Internet leicht durchsuchbar sind.** Wenn Sie 32-Bit-Codes verwenden, verwenden Sie eine hexadezimale Darstellung mit einem führenden "0x" und Großbuchstaben.

**Richtig:**

1234

0xC0001234

**Falsch:**

-1

-67113524

- **Verwenden Sie Details anzeigen/ausblenden, um Fehlercodes anzuzeigen.** Ausdruck als Fehlercode: <error code> .

![Screenshot der Meldung: Programm wurde nicht initialisiert ](images/mess-error-image45.png)

In diesem Beispiel wird ein Fehlercode verwendet, um eine Fehlermeldung zu ergänzen, die von weiteren Informationen profitieren kann.

### <a name="sound"></a>Sound

- **Begleitet fehlermeldungen nicht mit einem Soundeffekt oder Signalton.** Dies ist undurchdringlich und unnötig.
  - **Ausnahme:** Wiedergeben des Soundeffekts "Kritisch beenden", wenn das Problem für den Betrieb des Computers entscheidend ist und der Benutzer sofortige Maßnahmen ergreifen muss, um schwerwiegende Folgen zu vermeiden.

## <a name="text"></a>Text

**Allgemein**

- **Entfernen Sie redundanten Text.** Suchen Sie in Titeln, Hauptanweisungen, zusätzlichen Anweisungen, Befehlslinks und Commitschaltflächen danach. Lassen Sie im Allgemeinen vollständigen Text in Anweisungen und interaktiven Steuerelementen, und entfernen Sie alle Redundanzen von den anderen Stellen.
- **Verwenden Sie benutzerzentrierte Erklärungen.** Beschreiben Sie das Problem in Bezug auf Benutzeraktionen oder -ziele, nicht in Bezug auf die Probleme der Software. Verwenden Sie die Sprache, die die Zielbenutzer verstehen und verwenden. Vermeiden Sie technischen Jargon.

**Falsch:**

![Screenshot der Meldung: Eingabesynchroner Aufruf ](images/mess-error-image46.png)

**Richtig:**

![Screenshot der Meldung: Empfang eines Anrufs ausgelastet ](images/mess-error-image47.png)

In diesen Beispielen spricht die richtige Version die Sprache des Benutzers, während die falsche Version zu technisch ist.

- **Verwenden Sie nicht die folgenden Wörter:**
  - Fehler, Fehler (stattdessen Problem verwenden)
  - Fehler bei (verwenden Sie stattdessen nicht)
  - Ungültig, ungültig, ungültig (stattdessen falsch verwenden)
  - Abbrechen, Beenden, Beenden (stattdessen beenden)
  - Schwerwiegend, schwerwiegend (verwenden Sie stattdessen "schwerwiegend")

Diese Begriffe sind unnötig und stehen im Gegensatz zum ermutigenden Ton der Windows. Bei [ordnungsgemäßer Verwendung](vis-std-icons.md)kommuniziert das Fehlersymbol ausreichend, dass ein Problem vorliegt.

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

![Screenshot, der eine Microsoft Office Outlook Meldung "Dieses Element kann nicht geöffnet werden" zeigt. ](images/mess-error-image52.png)

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
- [Programmname] hat ein schwerwiegendes Problem aufgetreten und muss sofort geschlossen werden.

Nehmen Sie natürlich nach Bedarf Änderungen vor, damit die Hauptanweisung grammatikalisch korrekt ist und die Richtlinien der Hauptanweisung erfüllt.

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

In diesem Beispiel ist keine zusätzliche Anweisung erforderlich. die Lösung kann einfach aus der Problem-Anweisung abgeleitet werden.

- **Wenn die Lösung mehrere Schritte enthält, geben Sie die Schritte in der Reihenfolge an, in der sie abgeschlossen werden sollen.** Vermeiden Sie jedoch lösungen mit mehreren Schritten, da Benutzer schwierigkeiten haben, sich mehr als zwei oder drei einfache Schritte zu merken. Wenn weitere Schritte erforderlich sind, lesen Sie das entsprechende Hilfethema.
- **Halten Sie zusätzliche Anweisungen kurz.** Geben Sie nur an, was Benutzer wissen müssen. Unnötige Details auslassen. Ziel: maximal drei Sätze mittlerer Länge.
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
- Formatieren Sie den Text nach Möglichkeit fett. Setzen Sie den Text andernfalls nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

**Beispiel:** Wenn Sie die Meldung **Es ist kein CD-Datenträger in der Laufwerkmeldung** angezeigt wird, fügen Sie einen neuen CD-Datenträger in das Laufwerk ein, und versuchen Sie es erneut.

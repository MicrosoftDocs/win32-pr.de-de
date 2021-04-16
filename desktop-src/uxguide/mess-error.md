---
title: Fehlermeldungen (Entwurfsgrundlagen)
description: Eine Fehlermeldung warnt Benutzer über ein bereits aufgetretene Problem.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0a8ee17093618dc8a192cfad8ce962f7ed04fc76
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104568010"
---
# <a name="error-messages-design-basics"></a>Fehlermeldungen (Entwurfsgrundlagen)

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Eine Fehlermeldung warnt Benutzer über ein bereits aufgetretene Problem. Im Gegensatz dazu warnt eine Warnmeldung Benutzer über eine Bedingung, die in der Zukunft ein Problem verursachen könnte. Fehlermeldungen können mithilfe von modalen Dialogfeldern, direkten Nachrichten, Benachrichtigungen oder Luftballons angezeigt werden.

![Screenshot der Fehlermeldung: Umbenennen nicht möglich](images/mess-error-image1.png)

Eine typische modale Fehlermeldung.

Effektive Fehlermeldungen informieren Benutzer, dass ein Problem aufgetreten ist, erläutern, warum es passiert ist, und stellen eine Lösung bereit, damit Benutzer das Problem beheben können. Benutzer sollten entweder eine Aktion ausführen oder Ihr Verhalten im Ergebnis einer Fehlermeldung ändern.

Gut geschriebene, hilfreiche Fehlermeldungen sind von entscheidender Bedeutung für eine Qualität des Benutzer Erlebnisses. Schlecht geschriebene Fehlermeldungen führen zu einer geringen Produktzufriedenheit und sind eine führende Ursache für vermeidbare technische Supportkosten. Unnötige Fehlermeldungen brechen den Benutzer Fluss ab.

**Hinweis:** Richtlinien, die sich auf [Dialogfelder](win-dialog-box.md), [Warnmeldungen](mess-warn.md), [Bestätigungen](mess-confirm.md), [Standardsymbole](vis-std-icons.md), [Benachrichtigungen](mess-notif.md)und [Layout](vis-layout.md) beziehen, werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

- **Stellt die Benutzeroberfläche (UI) ein bereits aufgetretene Problem dar?** Andernfalls handelt es sich bei der Meldung nicht um einen Fehler. Wenn der Benutzer über eine Bedingung benachrichtigt wird, die zu einem späteren Zeitpunkt ein Problem verursachen könnte, verwenden Sie eine Warnmeldung.
- **Kann das Problem ohne Verwirrung vermieden werden?** Wenn dies der Fall ist, verhindern Sie das Problem. Verwenden Sie z. b. Steuerelemente, die auf gültige Werte beschränkt sind, anstatt nicht eingeschränkte Steuerelemente zu verwenden, die möglicherweise Fehlermeldungen erfordern. Deaktivieren Sie außerdem Steuerelemente, wenn Sie auf "Fehler" klicken, so lange es offensichtlich ist, warum das Steuerelement deaktiviert ist.
- **Kann das Problem automatisch korrigiert werden?** Wenn dies der Fall ist, sollten Sie das Problem behandeln und die Fehlermeldung unterdrücken.
- **Werden Benutzer wahrscheinlich eine Aktion ausführen oder Ihr Verhalten als Ergebnis der Nachricht ändern?** Wenn dies nicht der Fall ist, wird die Unterbrechung des Benutzers durch die Bedingung nicht rechtfertigen, sodass der Fehler besser unterdrückt werden kann
- **Ist das Problem relevant, wenn Benutzer aktiv andere Programme verwenden?** Wenn dies der Fall ist, sollten Sie das Problem mithilfe eines [Benachrichtigungs Bereichs Symbols](winenv-notification.md)überprüfen.
- **Steht das Problem nicht in Zusammenhang mit der aktuellen Benutzeraktivität, erfordert es keine sofortige Benutzeraktion und kann von Benutzern frei ignoriert werden?** Wenn dies der Fall ist, verwenden Sie stattdessen eine [Aktions Fehler Benachrichtigung](mess-notif.md) .
- **Bezieht sich das Problem auf den Status einer Hintergrundaufgabe innerhalb eines primären Fensters?** Wenn dies der Fall ist, sollten Sie das Problem mithilfe einer [Statusleiste](ctrl-status-bars.md)anzeigen.
- **Sind die primären Ziel Benutzer IT-Experten?** Wenn dies der Fall ist, sollten Sie einen alternativen Feedback Mechanismus verwenden, z.b. [Protokolldatei](glossary.md) Einträge oder e-Mail-Benachrichtigungen. IT-Experten bevorzugen Protokolldateien für nicht wichtige Informationen.

## <a name="design-concepts"></a>Entwurfskonzepte

**Die Merkmale von schlechten Fehlermeldungen**

Es sollte nicht überraschend sein, dass es viele Fehlermeldungen gibt, die fehlerhaft, nicht hilfreich und unzureichend geschrieben sind. Und da Fehlermeldungen häufig mithilfe von modalen Dialogfeldern angezeigt werden, unterbrechen Sie die aktuelle Aktivität des Benutzers und verlangen, dass Sie bestätigt werden, bevor der Benutzer den Vorgang fortsetzen kann.

Ein Teil des Problems ist, dass es so viele Möglichkeiten gibt, das Problem zu beheben. Beachten Sie diese Beispiele in der Fehlermeldung Hall of Shame:

**Unnötige Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: Fehler bei der Anwendung. ](images/mess-error-image2.png)

Dieses Beispiel aus Windows XP ist möglicherweise die schlechteste Fehlermeldung. Es zeigt an, dass ein Programm nicht gestartet werden konnte, da Windows selbst gerade heruntergefahren wird. Es gibt nichts, was der Benutzer in diesem Fall tun kann oder was Sie tun möchten (der Benutzer hat sich entschieden, Windows herunterzufahren). Und wenn Sie diese Fehlermeldung anzeigen, verhindert Windows das Herunterfahren.

**Das Problem:** Die Fehlermeldung selbst ist das Problem. Abgesehen davon, dass die Fehlermeldung verworfen wird, gibt es für die Benutzer nichts zu tun.

**Führende Ursache:** Alle Fehlerfälle werden gemeldet, unabhängig von den Zielen oder der Sicht der Benutzer.

**Empfohlene Alternative:** Melden Sie keine Fehler, die Benutzern nicht wichtig sind.

**Erfolgs Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: Entfernungs Fehler ](images/mess-error-image3.png)

Diese Fehlermeldung ist darauf zurückzuführen, dass der Benutzer nicht sofort nach der Programm Entfernung neu gestartet wird. Die Programm Entfernung war aus Sicht des Benutzers erfolgreich.

**Das Problem:** Aus Sicht des Benutzers gibt es keinen Fehler. Abgesehen davon, dass die Fehlermeldung verworfen wird, gibt es für die Benutzer nichts zu tun.

**Führende Ursache:** Die Aufgabe wurde erfolgreich aus der Sicht des Benutzers abgeschlossen, konnte jedoch nicht aus der Sicht des Programms deinstalliert werden.

**Empfohlene Alternative:** Keine Fehlermeldung für Bedingungen, die von Benutzern als akzeptabel angesehen werden.

**Vollständig nutzlose Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: Unbekannter Fehler. ](images/mess-error-image4.png)

Benutzer erfahren, dass ein Fehler aufgetreten ist, aber Sie haben keine Ahnung, was der Fehler war oder was zu tun ist. Und Nein, das ist nicht OK!

**Das Problem:** Die Fehlermeldung gibt kein bestimmtes Problem aus, und Benutzer können damit nichts tun.

**Führende Ursache:** Höchstwahrscheinlich weist das Programm eine schlechte Fehlerbehandlung auf.

**Empfohlene Alternative:** Entwerfen Sie eine gute Fehlerbehandlung im Programm.

**Nicht verständliche Fehlermeldungen**

**Falsch:**

![Screenshot der Fehlermeldung: Sicherung ist nicht vollständig. ](images/mess-error-image5.png)

In diesem Beispiel ist die Problem Erklärung klar, aber die ergänzende Erläuterung ist vollkommen.

**Das Problem:** Die Problem Erklärung oder Lösung ist unverständlich.

**Führende Ursache:** Die Erläuterung des Problems aus der Sicht des Codes anstelle der des Benutzers.

**Empfohlene Alternative:** Schreiben Sie Fehlermeldungs Text, der ihren Ziel Benutzern leicht verständlich ist. Bereitstellen von Lösungen, die Benutzer tatsächlich durchführen können. Entwerfen Sie die Fehlermeldung des Programms, dass Programmierer keine Fehlermeldungen an der Stelle verfassen.

**Übermäßige Fehlermeldungen**

**Falsch:**

![Screenshot der äußerst ausführlichen Meldung ](images/mess-error-image6.png)

In diesem Beispiel versucht die Fehlermeldung, jeden Fehler Behebungs Schritt zu erläutern.

**Das Problem:** Zu viele Informationen.

**Führende Ursache:** Es werden zu viele Details angezeigt, oder es wurde versucht, einen komplizierten Problem Behandlungsprozess in einer Fehlermeldung zu erläutern.

**Empfohlene Alternative:** Vermeiden Sie unnötige Details. Vermeiden Sie außerdem Problembehandlung. Wenn eine Problembehandlung erforderlich ist, konzentrieren Sie sich auf die wahrscheinlichsten Lösungen, und erläutern Sie den Rest, indem Sie eine Verknüpfung mit dem entsprechenden Thema in der Hilfe herstellen.

**Unnötigerweise harte Fehlermeldungen**

**Falsch:**

![Screenshot der Meldung: Objekt kann nicht gefunden werden. ](images/mess-error-image7.png)

Das Programm ist nicht in der Lage, ein Objekt zu finden, klingt kaum etwas. Und wenn es sich um eine Katastrophe handelt, warum ist die Antwort in Ordnung?

**Das Problem:** Der Ton des Programms ist unnötig hart oder dramatisch.

**Führende Ursache:** Das Problem ist auf einen Fehler zurückzuführen, der aus der Sicht des Programms schwerwiegend erscheint.

**Empfohlene Alternative:** Wählen Sie die Sprache auf der Grundlage der Sicht des Benutzers sorgfältig aus.

**Fehlermeldungen, die Benutzer als Schuld zuweisen**

**Falsch:**

![Screenshot der Meldung: Ungültiges Zeichen ](images/mess-error-image8.png)

Warum fühlen sich die Benutzer als kriminell?

**Das Problem:** Die Fehlermeldung wird so formuliert, dass der Benutzer eine Fehlermeldung sendet.

**Führende Ursache:** Unempfindliche Formulierung, bei der es sich um das Verhalten des Benutzers und nicht um das Problem handelt.

**Empfohlene Alternative:** Konzentrieren Sie sich auf das Problem, nicht auf die Benutzeraktion, die zu dem Problem geführt hat, und verwenden Sie die passive Stimme nach Bedarf.

**Dumme Fehlermeldungen**

**Falsch:**

![Screenshot der Meldung: Fehler im Fehlerbericht ](images/mess-error-image9.png)

In diesem Beispiel ist die Problem Erklärung ziemlich ironisch, und es werden keine Lösungen bereitgestellt.

**Das Problem:** Fehlermeldungs Anweisungen, bei denen es sich um dumme oder nicht-sequenzielle handelt.

**Führende Ursache:** Erstellen von Fehlermeldungen ohne Beachtung ihres Kontexts.

**Empfohlene Alternative:** Lassen Sie die Fehlermeldungen von einem Writer erstellt und überprüft werden. Berücksichtigen Sie den Kontext und den Benutzer Zustand, wenn Sie die Fehler überprüfen.

**Programmierer-Fehlermeldungen**

**Falsch:**

![Screenshot der Meldung: Zugriffs Verletzungs Adresse ](images/mess-error-image10.png)

In diesem Beispiel gibt die Fehlermeldung an, dass ein Fehler im Programm vorliegt. Diese Fehlermeldung ist nur für den Programmierer von Bedeutung.

**Das Problem:** Nachrichten, die den Entwicklern des Programms helfen sollen, Fehler zu finden, bleiben in der Releaseversion des Programms erhalten. Diese Fehlermeldungen haben keine Bedeutung oder einen Wert für Benutzer.

**Führende Ursache:** Programmierer, die die normale Benutzeroberfläche verwenden, um Nachrichten zu erstellen.

**Empfohlene Alternative:** Entwickler müssen alle diese Nachrichten bedingt kompilieren, damit Sie automatisch aus der Releaseversion eines Produkts entfernt werden. Verschwenden Sie keine Zeit, wenn Sie versuchen, Fehler wie diese für Benutzer verständlich zu machen, da ihre einzige Zielgruppe die Programmierer sind.

**Fehlermeldungen mit schlechter Präsentation**

**Falsch:**

![Screenshot der Meldung: Unerwarteter Fehler ](images/mess-error-image11.png)

Dieses Beispiel enthält viele gängige Präsentations Fehler.

**Das Problem:** Alle Details werden in der Fehlermeldungs Präsentation falsch angezeigt.

**Führende Ursache:** Die Richtlinien für die Fehlermeldung werden nicht kennen und angewendet. Die Verwendung von Writer und Editoren zum Erstellen und Überprüfen der Fehlermeldungen wird nicht verwendet.

Die Art der Fehlerbehandlung ist so, dass viele dieser Fehler sehr einfach zu erstellen sind. Es ist beunruhigend zu erkennen, dass die meisten Fehlermeldungen für die Hall of Shame als Kandidaten gelten könnten.

**Die Merkmale von guten Fehlermeldungen**

Im Gegensatz zu den vorherigen, schlechten Beispielen haben gute Fehlermeldungen Folgendes:

- **Ein Problem.** Gibt an, dass ein Problem aufgetreten ist.
- **Eine Ursache.** Erläutert, warum das Problem aufgetreten ist.
- **Eine-Lösung.** Bietet eine Lösung, mit der Benutzer das Problem beheben können.

Außerdem werden gute Fehlermeldungen wie folgt dargestellt:

- **Dienliche.** Die Meldung stellt ein Problem dar, das Benutzern wichtig ist.
- **Verwertbare.** Benutzer sollten entweder eine Aktion ausführen oder Ihr Verhalten als Ergebnis der Nachricht ändern.
- **Benutzer zentriert.** In der Meldung wird das Problem in Bezug auf die Ziel Benutzeraktionen oder-Ziele beschrieben, nicht in Bezug auf den Code, mit dem der Code nicht zufrieden ist.
- **Kurze.** Die Nachricht ist so kurz wie möglich, aber nicht kürzer.
- **Klartext.** In der Meldung wird eine einfache Sprache verwendet, damit die Ziel Benutzer Probleme und Lösungen leicht verstehen können.
- **Zugeschnitten.** In der Meldung wird das Problem in einer bestimmten Sprache beschrieben. dabei werden bestimmte Namen, Speicherorte und Werte der betroffenen Objekte bereit gegeben.
- **Liche.** Benutzer sollten nicht beschuldigt werden, oder Sie werden nicht als dumm fest gemacht.
- **Ere.** Wird nur selten angezeigt. Häufig angezeigte Fehlermeldungen sind ein Anzeichen für ein ungültiges Design.

Wenn Sie die Fehlerbehandlung für diese Merkmale entwerfen, können Sie die Fehlermeldungen Ihres Programms aus der Fehlermeldungs-Hall der Schande bewahren.

**Vermeiden unnötiger Fehlermeldungen**

Häufig ist die beste Fehlermeldung keine Fehlermeldung. Viele Fehler können durch einen besseren Entwurf vermieden werden, und es gibt häufig bessere Alternativen zu Fehlermeldungen. Es ist in der Regel besser, einen Fehler zu vermeiden, als einen Bericht zu melden.

Die offensichtlichsten Fehlermeldungen, die vermieden werden können, sind solche, die nicht durchführbar sind. Wenn Benutzer die Nachricht wahrscheinlich ohne Änderung verwerfen, lassen Sie die Fehlermeldung Weg.

Einige Fehlermeldungen können gelöscht werden, da Sie keine Probleme aus der Sicht des Benutzers haben. Angenommen, der Benutzer hat versucht, eine Datei zu löschen, die bereits gerade gelöscht wird. Dies kann ein unerwarteter Fall aus der Sicht des Codes sein. Benutzer betrachten dies jedoch nicht als Fehler, da das gewünschte Ergebnis erreicht wird.

**Falsch:**

![Screenshot der Meldung: Datei kann nicht gelöscht werden ](images/mess-error-image12.png)

Diese Fehlermeldung sollte gelöscht werden, da die Aktion aus Sicht des Benutzers erfolgreich war.

Ein weiteres Beispiel ist, dass der Benutzer eine Aufgabe explizit abbricht. Aus Sicht des Benutzers ist die folgende Bedingung kein Fehler.

**Falsch:**

![Screenshot der Meldung: Sicherung kann nicht vollständig ausgeführt werden ](images/mess-error-image13.png)

Diese Fehlermeldung sollte auch gelöscht werden, da die Aktion aus Sicht des Benutzers erfolgreich war.

Manchmal können Fehlermeldungen vermieden werden, indem Sie sich auf die Ziele der Benutzer anstatt auf die Technologie konzentrieren. Überdenken Sie dabei, was ein Fehler wirklich ist. Liegt das Problem bei den Benutzer Zielen oder der Fähigkeit Ihres Programms, Sie zu erfüllen? Wenn die Aktion des Benutzers in der realen Welt sinnvoll ist, sollte dies auch in Software sinnvoll sein.

Nehmen wir beispielsweise an, dass ein Benutzer in einem e-Commerce-Programm versucht, ein Produkt mithilfe von Search zu finden, aber die Literale Suchabfrage hat keine Übereinstimmungen, und das gewünschte Produkt ist nicht mehr vorrätig. Technisch gesehen handelt es sich hierbei um einen Fehler, aber anstelle einer Fehlermeldung könnte das Programm Folgendes ausführen:

- Suchen Sie weiterhin nach Produkten, die der Abfrage am ehesten entsprechen.
- Wenn bei der Suche offensichtliche Fehler auftreten, sollten Sie automatisch eine korrigierte Abfrage empfehlen.
- Behandeln Sie häufige Probleme, wie z. b. falsche Schreibweise, Alternative Rechtschreibprüfungen und nicht übereinstimmende pluralisierungs-und Verb Fälle.
- Geben Sie an, wann das Produkt in der Aktien Version angezeigt wird.

Solange die Anforderung des Benutzers angemessen ist, sollte ein gut konzipiertes e-Commerce-Programm sinnvolle Ergebnisse als Fehler zurückgeben.

Eine weitere gute Möglichkeit, Fehlermeldungen zu vermeiden, besteht darin, Probleme an erster Stelle zu vermeiden. Sie können Fehler vermeiden, indem Sie Folgendes ausführen:

- **Verwenden von eingeschränkten Steuerelementen.** Verwenden Sie Steuerelemente, die auf gültige Werte beschränkt sind. Steuerelemente wie Listen, Schieberegler, Kontrollkästchen, Options Felder und Datums-und Uhrzeit-Picker sind auf gültige Werte beschränkt, während Textfelder oft nicht sind und möglicherweise Fehlermeldungen erfordern. Sie können jedoch Textfelder einschränken, um nur bestimmte Zeichen zu akzeptieren und eine maximale Anzahl von Zeichen zu akzeptieren.
- **Verwenden von eingeschränkten Interaktionen.** Erlauben Sie Benutzern bei Drag-Vorgängen nur das Ablegen gültiger Ziele.
- **Verwenden deaktivierter Steuerelemente und Menü Elemente.** Deaktivieren Sie Steuerelemente und Menü Elemente, wenn Benutzer leicht ableiten können, warum das Steuerelement oder das Menü Element deaktiviert ist.
- **Gute Standardwerte werden bereitgestellt.** Die Wahrscheinlichkeit, dass Benutzer die Standardwerte übernehmen können, ist weniger wahrscheinlich. Selbst wenn Benutzer sich entscheiden, den Wert zu ändern, können Benutzer mit dem Standardwert das erwartete Eingabeformat erkennen.
- **Alles funktioniert einfach.** Es ist weniger wahrscheinlich, dass Benutzerfehler machen, wenn die Aufgaben unnötig sind oder automatisch ausgeführt werden. Wenn Benutzer kleine Fehler machen, deren Absicht aber klar ist, wird das Problem automatisch behoben. Beispielsweise können kleinere Formatierungs Probleme automatisch behoben werden.

**Bereitstellen von erforderlichen Fehlermeldungen**

Manchmal müssen Sie tatsächlich eine Fehlermeldung angeben. Benutzer führen zu Fehlern, Netzwerke und Geräte funktionieren nicht mehr, Objekte können nicht gefunden oder geändert werden, Aufgaben können nicht abgeschlossen werden, und Programme haben Fehler. Im Idealfall würden diese Probleme seltener auftreten. Wir können unsere Software so entwerfen, dass viele Arten von Benutzerfehlern vermieden werden, aber es ist nicht realistisch, alle diese Probleme zu vermeiden. Und wenn eines dieser Probleme auftritt, werden Benutzer durch eine hilfreiche Fehlermeldung schnell wieder auf den Fuß gelangen.

Eine gängige Annahme ist, dass Fehlermeldungen die schlechteste Benutzer Leistung sind und bei allen Kosten vermieden werden sollten. es ist jedoch genauer gesagt zu sagen, dass die Benutzer Verwirrung das Schlimmste ist, und sollte bei allen Kosten vermieden werden. Manchmal sind diese Kosten eine hilfreiche Fehlermeldung.

Deaktivieren Sie deaktivierte Steuerelemente In den meisten Fällen ist es offensichtlich, warum ein Steuerelement deaktiviert ist, sodass das Deaktivieren des Steuer Elements eine gute Möglichkeit ist, eine Fehlermeldung zu vermeiden. Was aber, wenn der Grund für die Deaktivierung eines Steuer Elements nicht offensichtlich ist? Der Benutzer kann nicht fortfahren, und es gibt kein Feedback, um das Problem zu ermitteln. Jetzt ist der Benutzer nicht mehr da und muss entweder das Problem ableiten oder technischen Support erhalten. In solchen Fällen ist es viel besser, das Steuerelement aktiviert zu lassen und stattdessen eine hilfreiche Fehlermeldung zu erhalten.

**Falsch:**

![Screenshot der Meldung: wo speichern Sie die Sicherung? ](images/mess-error-image14.png)

Warum wird die Schaltfläche "weiter" hier deaktiviert? Sie sollten es besser aktivieren und die Benutzer Verwirrung vermeiden, indem Sie eine hilfreiche Fehlermeldung senden.

Wenn Sie nicht sicher sind, ob Sie eine Fehlermeldung erhalten sollten, erstellen Sie zunächst die Fehlermeldung, die Sie möglicherweise erhalten. Wenn Benutzer wahrscheinlich entweder eine Aktion ausführen oder Ihr Verhalten als Ergebnis ändern, geben Sie die Fehlermeldung an. Wenn Benutzer die Nachricht jedoch wahrscheinlich ohne Änderung verwerfen, lassen Sie die Fehlermeldung Weg.

**Entwerfen für eine gute Fehlerbehandlung**

Obwohl das Erstellen von gutem Fehlermeldungs Text eine Herausforderung darstellen kann, ist es manchmal unmöglich, ohne eine gute Fehlerbehandlung durch das Programm zu unterstützen. Beachten Sie diese Fehlermeldung:

**Falsch:**

![Screenshot der Meldung: Unbekannter Fehler. ](images/mess-error-image15.png)

Die Wahrscheinlichkeit ist, dass das Problem wirklich unbekannt ist, weil die Fehler Behandlungs Unterstützung des Programms fehlt.

Obwohl es möglich ist, dass es sich hierbei um eine sehr schlecht geschriebene Fehlermeldung handelt, ist es wahrscheinlicher, dass die fehlende gute Fehlerbehandlung durch den zugrunde liegenden Code nicht bekannt ist.

Um bestimmte, Handlungs relevante, Benutzer zentrierte Fehlermeldungen zu erstellen, muss der Fehler Behandlungs Code des Programms bestimmte, Allgemeine Fehlerinformationen bereitstellen:

- Jedem Problem sollte ein eindeutiger Fehlercode zugewiesen werden.
- Wenn ein Problem mehrere Ursachen hat, sollte das Programm die jeweilige Ursache ermitteln, wann immer dies möglich ist.
- Wenn das Problem über Parameter verfügt, müssen die Parameter beibehalten werden.
- Probleme auf niedriger Ebene müssen auf einer ausreichend hohen Ebene behandelt werden, damit die Fehlermeldung aus der Sicht des Benutzers angezeigt werden kann.

Gute Fehlermeldungen sind nicht nur ein Problem mit der Benutzeroberfläche, sondern ein Software Entwurfsproblem. Ein guter Fehler bei der Fehlermeldung ist, dass Sie zu einem späteren Zeitpunkt nicht mehr in den Griff haben können.

**Problembehandlung (und Vorgehensweise beim vermeiden)**

Fehler Behebungs Ergebnisse, wenn ein Problem mit mehreren unterschiedlichen Gründen mit einer einzelnen Fehlermeldung gemeldet wird.

**Falsch:**

![Diagramm einer Nachricht, die drei Gründe angibt ](images/mess-error-image16.png)

**Richtig:**

![Diagramm mit drei Nachrichten, die jeweils eine Ursache angeben](images/mess-error-image17.png)

Problembehandlung, wenn mehrere Probleme mit einer einzelnen Fehlermeldung gemeldet werden.

Im folgenden Beispiel konnte ein Element nicht verschoben werden, da es bereits verschoben oder gelöscht wurde oder der Zugriff verweigert wurde. Wenn das Programm die Ursache leicht ermitteln kann, warum sollten Sie den Benutzer belasten, um die genaue Ursache zu ermitteln?

**Falsch:**

![Screenshot der Meldung, die zwei Gründe angibt ](images/mess-error-image18.png)

Und das ist das? Der Benutzer muss jetzt Probleme beheben.

Das Programm kann ermitteln, ob der Zugriff verweigert wurde, sodass dieses Problem mit einer bestimmten Fehlermeldung gemeldet werden sollte.

**Richtig:**

![Screenshot der Nachricht, die eine Ursache angibt ](images/mess-error-image19.png)

Mit einer bestimmten Ursache ist keine Problembehandlung erforderlich.

Verwenden Sie Nachrichten mit mehreren Ursachen nur, wenn die jeweilige Ursache nicht ermittelt werden kann. In diesem Beispiel wäre es für das Programm schwierig zu bestimmen, ob das Element verschoben oder gelöscht wurde, sodass hier eine einzelne Fehlermeldung mit mehreren Gründen verwendet werden kann. Es ist jedoch unwahrscheinlich, dass Benutzer darauf achten, dass Sie z. b. eine gelöschte Datei nicht verschieben konnten. Aus diesen Gründen ist die Fehlermeldung nicht einmal erforderlich.

**Behandeln von unbekannten Fehlern**

In einigen Fällen wissen Sie das Problem, die Ursache oder die Lösung wirklich nicht. Wenn es nicht erforderlich wäre, den Fehler zu unterdrücken, ist es besser, den Mangel an Informationen zu beheben, als Probleme, Ursachen oder Lösungen zu präsentieren, die möglicherweise nicht richtig sind.

Wenn das Programm z. b. eine nicht behandelte Ausnahme aufweist, ist die folgende Fehlermeldung geeignet:

![Screenshot der Meldung: Unbekannter Fehler aufgetreten. ](images/mess-error-image20.png)

Wenn Sie einen unbekannten Fehler nicht unterdrücken können, ist es besser, sich über fehlende Informationen zu informieren.

Stellen Sie andererseits bestimmte, aussagekräftige Informationen bereit, wenn dies in den meisten Fällen hilfreich sein wird.

![Screenshot, der die Meldung "Server nicht verfügbar" für Office Communicator anzeigt ](images/mess-error-image21.png)

Diese Fehlermeldung ist für einen unbekannten Fehler geeignet, wenn die Netzwerk Konnektivität in der Regel das Problem ist.

**Bestimmen des geeigneten Nachrichten Typs**

Einige Probleme können je nach Betonung und Formulierung als Fehler, Warnung oder Informationen angezeigt werden. Nehmen Sie beispielsweise an, eine Webseite kann ein nicht signiertes ActiveX-Steuerelement nicht auf Grundlage der aktuellen Windows Internet Explorer-Konfiguration laden:

- **Zeit.** "Auf dieser Seite kann kein nicht signiertes ActiveX-Steuerelement geladen werden." (Als vorhandenes Problem formuliert.)
- **Davor.** "Diese Seite verhält sich möglicherweise nicht wie erwartet, da Windows Internet Explorer nicht zum Laden von nicht signierten ActiveX-Steuerelementen konfiguriert ist." oder "Diese Seite darf ein nicht signiertes ActiveX-Steuerelement installieren? Wenn Sie dies aus nicht vertrauenswürdigen Quellen machen, kann dies Ihren Computer beeinträchtigen. " (Beide werden als Bedingungen formuliert, die möglicherweise zukünftige Probleme verursachen.)
- **Informationen.** "Sie haben Windows Internet Explorer so konfiguriert, dass nicht signierte ActiveX-Steuerelemente blockiert werden." (Als eine-Anweisung formuliert.)

**Um den richtigen Nachrichtentyp zu bestimmen, konzentrieren Sie sich auf den wichtigsten Aspekt des Problems, das Benutzer kennen oder reagieren müssen.** Wenn ein Problem darin besteht, dass der Benutzer nicht mehr fortfahren kann, sollten Sie es in der Regel als Fehler darstellen. Wenn der Benutzer fortfahren kann, stellen Sie ihn als Warnung dar. Erstellen Sie die [Haupt Anweisung](text-ui.md) oder einen anderen entsprechenden Text basierend auf diesem Fokus, und wählen Sie dann ein Symbol ([Standard](vis-std-icons.md) oder anderweitig), das mit dem Text übereinstimmt. Der Hauptanweisungs Text und die Symbole sollten immer mit dem Text identisch sein

**Darstellung der Fehlermeldung**

Die meisten Fehlermeldungen in Windows-Programmen werden mithilfe von modalen Dialogfeldern angezeigt (wie die meisten Beispiele in diesem Artikel), aber es gibt noch weitere Optionen:

- Direkt
- Ballons
- Benachrichtigungen
- Benachrichtigungs Bereichs Symbole
- Statusleisten
- Protokolldateien (für Fehler, die auf IT-Experten abzielen)

Das Einfügen von Fehlermeldungen in modale Dialogfelder hat den Vorteil, dass die sofortige Aufmerksamkeit und die Bestätigung des Benutzers gefordert werden. Dies ist jedoch auch der primäre Nachteil, wenn diese Aufmerksamkeit nicht erforderlich ist.

![Screenshot der Meldung: beendet das, was Sie tun ](images/mess-error-image22.png)

Müssen Sie Benutzer wirklich unterbrechen, damit Sie auf die Schaltfläche "Schließen" klicken können? Falls nicht, sollten Sie Alternativen zur Verwendung eines modalen Dialog Felds in Erwägung gezogen.

Modale Dialogfelder sind eine gute Wahl, wenn der Benutzer das Problem vor dem fortsetzen bestätigen muss, aber häufig eine schlechte Wahl. Im Allgemeinen empfiehlt es sich, die leichtesten Gewichtungs Präsentation zu verwenden, die den Auftrag gut erfüllt.

**Vermeiden der über Kommunikation**

Im allgemeinen [Lesen Benutzer nicht, Sie scannen](vis-layout.md). Umso mehr Text vorhanden ist, desto schwieriger ist es, den Text zu scannen, und desto wahrscheinlicher ist es, dass Benutzer den Text überhaupt nicht lesen. Daher ist es wichtig, den Text auf seine Grundlagen zu reduzieren und die Progressive Offenlegung und Hilfe Links zu verwenden, wenn dies erforderlich ist, um zusätzliche Informationen bereitzustellen.

Es gibt viele extreme Beispiele, aber sehen wir uns ein typisches Beispiel an. Im folgenden Beispiel wird der größte Teil der Attribute einer Fehlermeldung angezeigt, der Text ist jedoch nicht präzise und erfordert Motivation zum Lesen.

**Falsch:**

![Screenshot der ausführlichen Meldung ](images/mess-error-image23.png)

Bei diesem Beispiel handelt es sich um eine gute Fehlermeldung, die jedoch über kommuniziert.

Was ist alles, was dieser Text wirklich sagt? Ungefähr so wie hier gezeigt:

**Richtig:**

![Screenshot der Meldung: CD Recorder nicht erkannt ](images/mess-error-image24.png)

Diese Fehlermeldung weist im Wesentlichen die gleichen Informationen auf, ist aber weitaus präziser.

Wenn Sie die Details mithilfe der Hilfe bereitstellen, enthält diese Fehlermeldung einen [umgekehrten pyramidenstil](text-ui.md) .

Weitere Richtlinien und Beispiele für die übermäßige Kommunikation finden Sie unter [Benutzeroberflächen Text](text-ui.md).

**Wenn Sie nur acht Dinge ausführen**

1. Entwerfen Sie das Programm für die Fehlerbehandlung.
2. Übergeben Sie keine unnötigen Fehlermeldungen.
3. Vermeiden Sie Benutzer Verwirrung, indem Sie erforderliche Fehlermeldungen erteilen.
4. Stellen Sie sicher, dass die Fehlermeldung Probleme, Ursachen und Lösungen enthält.
5. Stellen Sie sicher, dass die Fehlermeldung relevant, handlungsfähig, kurz, klar, spezifisch, höflich und selten ist.
6. Entwerfen von Fehlermeldungen aus der Sicht des Benutzers, nicht aus der Sicht des Programms.
7. Vermeiden Sie die Einbindung des Benutzers bei der Problembehandlung verwenden Sie für jede erkennbare Ursache eine andere Fehlermeldung.
8. Verwenden Sie die Methode mit der leichtesten Gewichtungsmethode, die den Auftrag gut erfüllt.

**Verwendungsmuster**

Fehlermeldungen weisen mehrere Verwendungs Muster auf:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>System Probleme</strong><br/> Das Betriebssystem, das Hardware Gerät, das Netzwerk oder das Programm ist ausgefallen oder weist nicht den zum Ausführen eines Tasks erforderlichen Zustand auf. <br/></td>
<td>Viele System Probleme können vom Benutzer gelöst werden: <br/>
<ul>
<li>Geräte Probleme können gelöst werden, indem das Gerät eingeschaltet, das Gerät erneut angeschlossen und Medien eingefügt werden.</li>
<li>Netzwerkprobleme können gelöst werden, indem Sie die physische Netzwerkverbindung überprüfen und die <strong>Diagnose und Reparatur des Netzwerks</strong>ausführen.</li>
<li>Programm Probleme können gelöst werden, indem Programmoptionen geändert oder das Programm neu gestartet wird.</li>
</ul>
<img src="images/mess-error-image25.png" alt="Screen shot of message: Can&#39;t find a camera " /><br/> In diesem Beispiel kann das Programm keine Kamera finden, um eine Benutzer Aufgabe auszuführen.<br/> <img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br/> In diesem Beispiel muss ein Feature, das zum Ausführen einer Aufgabe erforderlich ist, aktiviert werden.<br/></td>
</tr>
<tr class="even">
<td><strong>Datei Probleme</strong><br/> Eine Datei oder ein Ordner, der für eine vom Benutzer initiierte Aufgabe erforderlich ist, wurde nicht gefunden, wird bereits verwendet oder weist nicht das erwartete Format auf. <br/></td>
<td><img src="images/mess-error-image27.png" alt="Screen shot of message: Can&#39;t delete file " /><br/> In diesem Beispiel kann die Datei oder der Ordner nicht gelöscht werden, da Sie nicht gefunden wurde.<br/> <img src="images/mess-error-image28.png" alt="Screen shot of message: Can&#39;t play this file " /><br/> In diesem Beispiel unterstützt das Programm das angegebene Dateiformat nicht.<br/></td>
</tr>
<tr class="odd">
<td><strong>Sicherheitsprobleme</strong><br/> Der Benutzer verfügt nicht über die Berechtigung für den Zugriff auf eine Ressource oder über ausreichende Berechtigungen, um eine vom Benutzer initiierte Aufgabe auszuführen. <br/></td>
<td><img src="images/mess-error-image29.png" alt="Screen shot of message: You don&#39;t have permission " /><br/> In diesem Beispiel verfügt der Benutzer nicht über die Berechtigung, auf eine Ressource zuzugreifen.<br/> <img src="images/mess-error-image30.png" alt="Screen shot of message: You don&#39;t have privilege " /><br/> In diesem Beispiel verfügt der Benutzer nicht über die Berechtigung zum Ausführen einer Aufgabe.<br/></td>
</tr>
<tr class="even">
<td><strong>Aufgaben Probleme</strong><br/> Es gibt ein bestimmtes Problem beim Ausführen einer vom Benutzer initiierten Aufgabe (außer einem System, einer Datei nicht gefunden, einem Dateiformat oder einem Sicherheitsproblem). <br/></td>
<td><img src="images/mess-error-image31.png" alt="Screen shot of message: Data can&#39;t be pasted " /><br/> In diesem Beispiel können die Zwischenablage Daten nicht in Paint eingefügt werden.<br/> <img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can&#39;t be installed " /><br/> In diesem Beispiel kann der Benutzer kein Software Upgrade installieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>Probleme bei der Benutzereingabe</strong><br/> Der Benutzer hat einen Wert eingegeben, der falsch oder inkonsistent mit anderen Benutzereingaben ist. <br/></td>
<td><img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br/> In diesem Beispiel hat der Benutzer einen falschen Uhrzeitwert eingegeben.<br/> <img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br/> In diesem Beispiel weist die Benutzereingabe nicht das richtige Format auf.<br/></td>
</tr>
</tbody>
</table>

## <a name="guidelines"></a>Richtlinien

### <a name="presentation"></a>Präsentation

- **Verwenden Sie nach Bedarf Aufgaben Dialogfelder** , um ein konsistentes Aussehen und Layout zu erzielen. Aufgaben Dialogfelder erfordern Windows Vista oder höher, sodass Sie nicht für frühere Versionen von Windows geeignet sind. Wenn Sie ein Meldungs Feld verwenden müssen, trennen Sie die Haupt Anweisung von der ergänzenden Anweisung mit zwei Zeilenumbrüchen.

### <a name="user-input-errors"></a>Benutzereingabe Fehler

- **Verhindern oder verringern Sie nach Möglichkeit Benutzereingabe Fehler wie folgt:**
  - Verwenden von Steuerelementen, die auf gültige Werte beschränkt sind.
  - Das Deaktivieren von Steuerelementen und Menü Elementen, wenn Sie auf klicken, führt zu einem Fehler, solange offensichtlich ist, warum das Steuerelement oder das Menü Element deaktiviert ist.
  - Gute Standardwerte werden bereitgestellt.

**Falsch:**

![Screenshot des Textfelds mit der Lautstärke Bezeichnung des Lautsprechers ](images/mess-error-image35.png)

In diesem Beispiel wird ein nicht eingeschränktes Textfeld für eingeschränkte Eingaben verwendet. Verwenden Sie stattdessen einen Schieberegler.

- **Verwenden Sie für kontextabhängige Benutzereingaben Probleme mit der nicht modalem Fehlerbehandlung (direkte Fehler oder Luftballons).**
- **Verwenden Sie für nicht kritische einpunktbenutzer-Eingabe Probleme, die bei einem Textfeld erkannt werden, oder unmittelbar nachdem ein Textfeld den Fokus verliert.** Für [Luftballons](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) ist kein verfügbarer Bildschirmbereich oder das dynamische Layout erforderlich, das zum Anzeigen von direkten Nachrichten erforderlich ist. Zeigen Sie jeweils nur eine Sprechblase an. Da das Problem nicht entscheidend ist, ist kein Fehler Symbol erforderlich. Beim Klicken auf das Problem, wenn das Problem behoben ist oder nach einem Timeout, werden die Ballons entfernt.

![Screenshot der Meldung: falsches Zeichen ](images/mess-error-image36.png)

In diesem Beispiel gibt eine Sprechblase ein Eingabeproblem an, während Sie sich noch im-Steuerelement befinden.

- Verwenden Sie direkte Fehler bei der **Erkennung verzögerter Fehler,** normalerweise durch Klicken auf die Schaltfläche Commit gefundene Fehler. (Verwenden Sie keine direkten [Fehler](glossary.md) für Einstellungen, für die sofort ein Commit ausgeführt wird.) Es können mehrere direkte Fehler gleichzeitig vorhanden sein. Verwenden Sie den normalen Text und ein 16x16-Pixel-Fehler Symbol, und platzieren Sie diese direkt neben dem Problem, wenn dies möglich ist. Direkte Fehler werden nicht entfernt, es sei denn, der Benutzer führt einen Commit aus, und es werden keine weiteren Fehler gefunden.

![Screenshot der Meldung: falsche e-Mail-Adresse ](images/mess-error-image37.png)

In diesem Beispiel wird ein direkter Fehler für einen Fehler verwendet, der durch Klicken auf die Schaltfläche Commit gefunden wurde.

- **Verwenden Sie die modale Fehlerbehandlung (Task Dialogfelder oder Meldungs Felder) für alle anderen Probleme,** einschließlich Fehlern, die mehrere Steuerelemente betreffen, oder nicht kontextabhängige oder nicht-Eingabefehler durch Klicken auf die Schaltfläche Commit gefunden werden.
- **Wenn ein Benutzereingabe Problem gemeldet wird, legen Sie den Eingabefokus auf das erste Steuerelement mit den falschen Daten fest.** Scrollen Sie ggf. in das Steuerelement. Wenn das Steuerelement ein Textfeld ist, wählen Sie den gesamten Inhalt aus. Es sollte immer offensichtlich sein, auf welche Fehlermeldung verwiesen wird.
- **Löschen Sie falsche Eingaben nicht.** Belassen Sie Sie stattdessen so, dass der Benutzer das Problem sehen und beheben kann, ohne zu beginnen.
  - **Ausnahme:** Löschen Sie falsches Kennwort, und Heften Sie Textfelder ein, da Benutzer die maskierte Eingabe nicht effektiv korrigieren

### <a name="troubleshooting"></a>Problembehandlung

- **Vermeiden Sie die Problembehandlung.** Verlassen Sie sich nicht auf eine einzelne Fehlermeldung, um ein Problem mit verschiedenen erkennbaren Gründen zu melden.
- **Verwenden Sie für jede erkennbare Ursache eine andere Fehlermeldung (in der Regel eine andere ergänzende Anweisung).** Wenn eine Datei z. b. aus verschiedenen Gründen nicht geöffnet werden kann, geben Sie eine separate ergänzende Anweisung aus jedem Grund an.
- **Verwenden Sie eine Meldung mit mehreren Ursachen nur dann, wenn die jeweilige Ursache nicht ermittelt werden kann.** Stellen Sie in diesem Fall die Lösungen in der Reihenfolge der Wahrscheinlichkeit dar, dass Sie das Problem beheben. Dadurch können Benutzer das Problem effizienter lösen.

### <a name="icons"></a>Symbole

- **Modale Fehlermeldungs Dialogfelder haben keine Titelleisten Symbole.** Symbole der Titelleiste werden als visueller Unterschied zwischen primären und sekundären Fenstern verwendet.
- **Verwenden Sie ein Fehler Symbol.** Ausnahmen:
  - Wenn es sich bei dem Fehler um ein Problem mit der Benutzereingabe handelt, das in einem modalen Dialogfeld oder in einer Sprechblase angezeigt wird, Dies ist gegen den ermutigenden Farbton von Windows. Bei direkten Fehlermeldungen sollte jedoch ein kleines Fehler Symbol (16x16 Pixel) verwendet werden, um Sie als Fehlermeldungen eindeutig zu identifizieren.

     ![Screenshot der Nachricht mit fehlerhaftem Post Format](images/mess-error-image38.png)

     ![Screenshot des Nachrichten Computer namens zu lang](images/mess-error-image39.png)

     In diesen Beispielen benötigen Benutzereingabe Probleme keine Fehler Symbole.

     ![Screenshot des falschen Formats der Nachrichten Telefonnummer](images/mess-error-image40.png)

     In diesem Beispiel benötigt eine direkte Fehlermeldung ein kleines Fehler Symbol, um es eindeutig als Fehlermeldung zu identifizieren.

- Wenn das Problem für eine Funktion ist, die über ein Symbol verfügt (und nicht über ein Benutzereingabe Problem), können Sie das Funktions Symbol mit einem Fehler Overlay verwenden. Wenn Sie dies tun, verwenden Sie den Funktionsnamen auch als Betreff des Fehlers.

    ![Screenshot der Nachricht ](images/mess-error-image41.png)

    In diesem Beispiel enthält das Feature-Symbol eine Fehler Überlagerung, und die Funktion ist der Betreff des Fehlers.

- **Verwenden Sie keine Warn Symbole für Fehler.** Dies erfolgt häufig, damit die Darstellung weniger schwerwiegend ist. Fehler sind keine Warnungen.

    **Falsch:**

    ![Screenshot der schnellen Umstellung von Nachrichten nicht aktiviert ](images/mess-error-image42.png)

    In diesem Beispiel wird fälschlicherweise ein Warnsymbol verwendet, damit der Fehler weniger schwerwiegend ist.

Weitere Richtlinien und Beispiele finden Sie unter [Standard Symbole](vis-std-icons.md).

### <a name="progressive-disclosure"></a>Schrittweise Offenlegung

- **Verwenden Sie die Schaltfläche Details progressives offenlegen/ausblenden, um erweiterte oder ausführliche Informationen in einer Fehlermeldung auszublenden.** Dies vereinfacht die Fehlermeldung für die typische Verwendung. Blenden Sie erforderliche Informationen nicht aus, da Sie von Benutzern möglicherweise nicht gefunden werden.

![Screenshot der Meldung: "ActiveSync kann nicht angemeldet werden" ](images/mess-error-image43.png)

In diesem Beispiel kann der Benutzer mit der Schaltfläche "Progressive Offenlegung" Weitere Details anzeigen, wenn Sie dies wünschen, oder die Benutzeroberfläche vereinfachen, wenn dies nicht der Fall ist.

- **Verwenden Sie keine Details zum anzeigen/ausblenden, es sei denn, es gibt wirklich weitere Details.** Geben Sie die vorhandenen Informationen nicht nur in einem ausführlicheren Format wieder.
- **Verwenden Sie keine Details zum anzeigen/ausblenden, um Hilfe Informationen anzuzeigen.** Verwenden Sie stattdessen Hilfe Links.

Informationen zur Bezeichnung finden Sie unter [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md)von Steuerelementen.

**Diese Meldung nicht mehr anzeigen**

- **Wenn eine Fehlermeldung diese Option erfordert, überdenken Sie den Fehler und die Häufigkeit.** Wenn Sie alle Merkmale eines guten Fehlers hat (relevant, Handlungs relevant und unregelmäßig), sollte es für Benutzer nicht sinnvoll sein, Sie zu unterdrücken.

Weitere Richtlinien finden Sie unter [Dialog Felder](win-dialog-box.md).

### <a name="default-values"></a>Standardwerte

- **Wählen Sie die sicherste, am wenigsten zerstörerische oder sicherste Antwort als Standard aus.** Wenn Sicherheit kein Faktor ist, wählen Sie den wahrscheinlichsten oder den bequemen Befehl aus.

### <a name="help"></a>Hilfe

- **Entwerfen Sie Fehlermeldungen, um die Notwendigkeit von Hilfe zu vermeiden.** Normalerweise sollten Benutzer keinen externen Text lesen, um das Problem zu verstehen und zu lösen, es sei denn, für die Lösung sind mehrere Schritte erforderlich.
- **Stellen Sie sicher, dass der Hilfe Inhalt relevant und hilfreich ist.** Es sollte keine ausführliche neuanweisung der Fehlermeldung sein, sondern sollte nützliche Informationen enthalten, die den Bereich der Fehlermeldung sprengen, wie z. b. Möglichkeiten, um das Problem in Zukunft zu vermeiden. Stellen Sie keinen Hilfe Link bereit, nur weil Sie dies tun können.
- **Verwenden Sie bestimmte, präzise und relevante Hilfe Links, um auf Hilfe Inhalte zuzugreifen.** Verwenden Sie für diesen Zweck keine Befehls Schaltflächen oder Progressive Offenlegung.
- **Wenn Sie Fehlermeldungen festlegen können, die nicht spezifisch und handlungsfähig sind, sollten Sie Links zu Online Hilfe Inhalten bereitstellen.** Auf diese Weise können Sie Benutzern zusätzliche Informationen bereitstellen, die Sie nach der Veröffentlichung des Programms aktualisieren können.

Weitere Richtlinien finden Sie in der [Hilfe](winenv-help.md).

### <a name="error-codes"></a>Fehlercodes

- **Wenn Sie Fehlermeldungen erhalten, die nicht spezifisch und handlungsfähig sind oder von der Hilfe profitieren, sollten Sie auch Fehlercodes bereitstellen.** Benutzer verwenden diese Fehlercodes häufig, um weitere Informationen im Internet zu durchsuchen.
- **Geben Sie immer eine Textbeschreibung des Problems und der Lösung an.** Verlassen Sie sich nicht nur auf den Fehlercode zu diesem Zweck.

**Falsch:**

![Screenshot der Meldung: die Datei kann nicht geöffnet werden. ](images/mess-error-image44.png)

In diesem Beispiel wird ein Fehlercode als Ersatz für einen projektmappentext verwendet.

- **Weisen Sie für jede andere Ursache einen eindeutigen Fehlercode zu.** Dadurch wird die Problembehandlung vermieden.
- **Wählen Sie Fehlercodes aus, die im Internet problemlos durchsuchbar sind.** Wenn Sie 32-Bit-Codes verwenden, verwenden Sie eine hexadezimale Darstellung mit einem führenden "0x"-Zeichen und einem Großbuchstaben.

**Richtig:**

1234

0xc0001234

**Falsch:**

-1

-67113524

- **Verwenden Sie die Details zum anzeigen/ausblenden, um Fehlercodes anzuzeigen.** Ausdruck als Fehlercode: <error code> .

![Screenshot der Meldung: das Programm wurde nicht initialisiert. ](images/mess-error-image45.png)

In diesem Beispiel wird ein Fehlercode verwendet, um eine Fehlermeldung zu ergänzen, die von weiteren Informationen profitieren kann.

### <a name="sound"></a>Sound

- **Führen Sie keine weiteren Fehlermeldungen mit einem Soundeffekt oder einem Signal aus.** Dabei handelt es sich um jarringverfahren und unnötig.
  - **Ausnahme:** Wenn das Problem für den Betrieb des Computers wichtig ist, können Sie den kritischen Sound wiedergeben, und der Benutzer muss Sofortmaßnahmen ergreifen, um schwerwiegende Folgen zu vermeiden.

## <a name="text"></a>Text

**Allgemein**

- **Entfernen Sie den redundanten Text.** Suchen Sie nach dem Titel, den Haupt Anweisungen, zusätzlichen Anweisungen, Befehls Verknüpfungen und Commit-Schaltflächen. Im Allgemeinen sollten Sie voll Text in Anweisungen und interaktiven Steuerelementen belassen und Redundanz von den anderen Orten entfernen.
- **Verwenden Sie Benutzer zentrierte Erläuterungen.** Beschreiben Sie das Problem im Hinblick auf Benutzeraktionen oder-Ziele, nicht in Bezug auf die unzufriedene Software. Verwenden Sie die Sprache, die die Ziel Benutzer verstehen und verwenden. Vermeiden Sie technische Fachjargon.

**Falsch:**

![Screenshot der Meldung: Eingabe-synchroner Rückruf ](images/mess-error-image46.png)

**Richtig:**

![Screenshot der Nachricht: der Empfang eines Aufrufes ist ausgelastet. ](images/mess-error-image47.png)

In diesen Beispielen wird die Sprache des Benutzers von der richtigen Version gesprochen, während die falsche Version übermäßig technisch ist.

- **Verwenden Sie nicht die folgenden Wörter:**
  - Fehler, Fehler (verwenden Sie stattdessen Problem)
  - Fehler bei (Verwendung nicht möglich).
  - Ungültig, ungültig, ungültig (verwenden Sie stattdessen falsch)
  - Abbrechen, beenden, beenden (verwenden Sie stattdessen "beenden")
  - Katastrophal, schwerwiegend (verwenden Sie stattdessen Ernst)

Diese Begriffe sind unnötig und im Gegensatz zum ermutigenden Ton von Windows. Wenn das Fehler Symbol [ordnungsgemäß verwendet](vis-std-icons.md)wird, kommuniziert es ausreichend, dass ein Problem vorliegt.

**Falsch:**

![Screenshot der Meldung: Schwerwiegender Fehler! ](images/mess-error-image48.png)

**Richtig:**

![Screenshot der Meldung: die Sicherung muss gleichzeitig geschlossen werden. ](images/mess-error-image49.png)

Im falschen Beispiel sind die Begriffe "katastrophal" und "Fehler" unnötig.

- Verwenden Sie keinen Ausdruck, der den Benutzer BLT oder einen Benutzerfehler impliziert. Vermeiden Sie die Verwendung von und ihrer in der Formulierung. Obwohl die aktive Stimme in der Regel bevorzugt ist, verwenden Sie die passive Stimme, wenn der Benutzer der Betreff ist, und könnten sich für den Fehler verantwortlich machen, wenn die aktive Stimme verwendet wurde.

**Falsch:**

![Screenshot der Meldung, dass Sie eine falsche Anmeldung eingegeben haben ](images/mess-error-image50.png)

**Richtig:**

![Screenshot der Meldung: falsches Kennwort ](images/mess-error-image51.png)

Im falschen Beispiel wird der Benutzer mit der aktiven Stimme umbenannt.

- **Sie sollten spezifisch sein.** Vermeiden Sie eine vage Formulierung, wie z. b. Syntax Fehler und ungültigen Vorgang. Geben Sie bestimmte Namen, Speicherorte und Werte der betroffenen Objekte an.

**Falsch:**

Die Datei wurde nicht gefunden.

Der Datenträger ist voll.

Der Wert liegt außerhalb des zulässigen Bereichs.

Das Zeichen ist ungültig.

Gerät nicht verfügbar.

Diese Probleme können mit bestimmten Namen, Positionen und Werten leichter gelöst werden.

- **Geben Sie möglicherweise unwahrscheinlich Probleme, Ursachen oder Lösungen zu einem bestimmten Versuch an.** Geben Sie kein Problem, keine Ursache oder Lösung an, es sei denn, es ist wahrscheinlich Recht. Beispielsweise ist es besser zu sagen, dass ein unbekannter Fehler aufgetreten ist, als etwas, das wahrscheinlich ungenau ist.
- **Vermeiden Sie das Wort "bitte",** außer in Situationen, in denen der Benutzer aufgefordert wird, etwas unpraktisch zu machen (z. b. warten), oder wenn die Software für die Situation verantwortlich ist.

**Richtig:**

Bitte warten Sie, während die Dateien von Windows auf Ihren Computer kopiert werden.

- **Verwenden Sie das Wort "Sorry" nur in Fehlermeldungen, die zu schwerwiegenden Problemen für den Benutzer führen** (z. b. Datenverlust oder nicht die Verwendung des Computers). Entschuldigen Sie nicht, wenn das Problem während der normalen Funktionsweise des Programms aufgetreten ist (z. b. wenn der Benutzer auf eine Netzwerkverbindung warten muss).

**Richtig:**

Leider hat die Fabrikam-Sicherung ein nicht BEHEB bares Problem erkannt und zum Schutz von Dateien auf Ihrem Computer heruntergefahren.

- **Weitere Informationen finden Sie unter Produkte mit Ihren Kurznamen.** Verwenden Sie keine vollständigen Produktnamen oder Marken Symbole. Schließen Sie den Firmennamen nicht ein, es sei denn, die Benutzer ordnen den Firmennamen dem Produkt zu. Fügen Sie keine Programm Versionsnummern ein.

**Falsch:**

![Screenshot, der zeigt, dass die Meldung "dieses Element kann nicht geöffnet werden" Microsoft Office. ](images/mess-error-image52.png)

**Richtig:**

![Screenshot der Meldung: dieses Element kann nicht geöffnet werden. ](images/mess-error-image53.png)

Im falschen Beispiel werden vollständige Produktnamen und Marken Symbole verwendet.

- **Verwenden Sie doppelte Anführungszeichen, um Objektnamen zu verwenden.** Dadurch wird der Text leichter analysiert und potenziell peinliche Anweisungen vermieden.
  - **Ausnahme:** Voll qualifizierte Dateipfade, URLs und Domänen Namen müssen nicht in doppelten Anführungszeichen stehen.

**Richtig:**

![Screenshot der Meldung: "mein Haus" ist nicht verfügbar. ](images/mess-error-image54.png)

In diesem Beispiel ist die Fehlermeldung verwirrend, wenn der Objektname nicht in Anführungszeichen steht.

- **Vermeiden Sie das Starten von Sätzen mit Objektnamen.** Dies ist oft schwierig zu analysieren.
- **Verwenden Sie keine Ausrufezeichen oder Wörter mit allen Großbuchstaben.** Ausrufezeichen und Großbuchstaben machen das Gefühl, dass Sie am Benutzer schreien.

Weitere Richtlinien und Beispiele finden Sie unter [Stil und Ton](text-style-tone.md).

**Titel**

- **Verwenden Sie den Titel, um den Befehl oder das Feature zu identifizieren, von dem der Fehler verursacht wurde.** Ausnahmen:
  - Wenn ein Fehler von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.
  - Wenn der Titel mit der Main-Anweisung redundant oder verwirrend wäre, sollten Sie stattdessen den Programmnamen verwenden.
- **Verwenden Sie den Titel nicht, um das Problem zu erläutern oder zusammenzufassen** , das den Zweck der Main-Anweisung darstellt.

**Falsch:**

![Screenshot mit der Meldung "neuer Ordner kann nicht umbenannt werden" ](images/mess-error-image55.png)

In diesem Beispiel wird der Titel fälschlicherweise verwendet, um das Problem zu erläutern.

- Verwenden Sie die Groß-/Kleinschreibung im Titel, ohne die Beendigung zu beenden

**Haupt Anleitung**

- **Verwenden Sie die main-Anweisung, um das Problem in Klartext zu beschreiben.**
- **Bei der präzisen Verwendung wird nur ein einzelner, kompletter Satz verwendet.** PiST die Haupt Anweisung der wichtigen Informationen. Sie können den Betreff implizit lassen, wenn es sich um Ihr Programm oder den Benutzer handelt. Fügen Sie den Grund für das Problem ein, wenn Sie dies möglich machen. Wenn Sie etwas anderes erläutern müssen, verwenden Sie eine ergänzende Anweisung.

**Falsch:**

![Screenshot der Meldung: das Upgrade kann nicht installiert werden. ](images/mess-error-image56.png)

In diesem Beispiel wird die gesamte Fehlermeldung in die Haupt Anweisung eingefügt, sodass Sie schwer lesbar ist.

- **Geben Sie einen bestimmten Namen an, wenn Objekte beteiligt sind.**
- **Vermeiden Sie es, vollständige Dateipfade und URLs in der Haupt Anweisung zu platzieren.** Verwenden Sie stattdessen einen Kurznamen (z. b. den Dateinamen), und legen Sie den vollständigen Namen (z. b. den Dateipfad) in der ergänzenden Anweisung ab. Sie können jedoch einen einzelnen vollständigen Dateipfad oder eine URL in der Haupt Anweisung platzieren, wenn die Fehlermeldung nicht anderweitig eine ergänzende Anweisung benötigt.

![Screenshot der Meldung: die Fabrikam-Datei kann nicht gelöscht werden. ](images/mess-error-image57.png)

In diesem Beispiel befindet sich nur der Dateiname in der Main-Anweisung. Der vollständige Pfad ist in der ergänzenden Anweisung.

- **Lassen Sie den vollständigen Dateipfad und die URL nicht zu, wenn Sie im Kontext offensichtlich ist.**

![Screenshot der Meldung: neuer Ordner kann nicht umbenannt werden. ](images/mess-error-image58.png)

In diesem Beispiel benennt der Benutzer eine Datei aus Windows-Explorer um. In diesem Fall ist der vollständige Dateipfad nicht erforderlich, da er aus dem Kontext ersichtlich ist.

- Verwenden Sie die aktuelle Spannung, wann immer möglich.
- Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
- Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine-Anweisung ist. Wenn die Anweisung eine Frage ist, müssen Sie ein endgültiges Fragezeichen einschließen.

**Haupt Anweisungs Vorlagen**

Obwohl es keine strengen Regeln für das formulieren gibt, versuchen Sie nach Möglichkeit, die folgenden Haupt Anweisungs Vorlagen zu verwenden:

- [Optionaler Betreffname] nicht [Aktion ausführen]
- [Optionaler Antragsteller Name] nicht [Aktion ausführen] aufgrund von [Grund]
- [Optionaler Antragsteller Name] nicht [Ausführen einer Aktion] auf "[Objektname]"
- [Optionaler Antragsteller Name] nicht [Durchführen einer Aktion] für "[Object Name]", da [Reason]
- Es ist nicht genügend [Ressource] für [Aktion ausführen] vorhanden.
- [Name des Antragstellers] hat keinen [Object Name] für [Zweck] erforderlich
- [Gerät oder Einstellung] ist ausgeschaltet, sodass [unerwünschte Ergebnisse]
- [Gerät oder Einstellung] ist nicht [verfügbar \| gefunden \| \| aktiviert)
- "[Object Name]" ist zurzeit nicht verfügbar.
- Der Benutzername oder das Kennwort ist falsch.
- Sie verfügen nicht über die Berechtigung für den Zugriff auf "[Objektname]".
- Sie haben keine Berechtigung zum [Ausführen von Aktionen].
- [Programmname] hat ein schwerwiegendes Problem und muss sofort geschlossen werden.

Nehmen Sie natürlich Änderungen nach Bedarf vor, damit die Haupt Anweisung ordnungsgemäß ist, und befolgen Sie die Haupt Anweisungs Richtlinien.

**Ergänzende Anweisungen**

- Verwenden Sie die ergänzende Anweisung für Folgendes:
  - Weitere Informationen zu diesem Problem.
  - Erläutern Sie die Ursache des Problems.
  - Auflisten der Schritte, die der Benutzer ausführen kann, um das Problem zu beheben.
  - Stellen Sie Maßnahmen bereit, um zu verhindern, dass das Problem erneut auftritt.
- **Wenn möglich, sollten Sie eine praktische, hilfreiche Lösung vorschlagen, damit Benutzer das Problem beheben können.** Stellen Sie jedoch sicher, dass die vorgeschlagene Lösung das Problem wahrscheinlich löst. Verschwenden Sie die Zeit der Benutzer nicht, indem Sie mögliche, aber unwahrscheinliche Lösungen vorschlagen.

**Falsch:**

![Screenshot der Meldung: nicht genügend Arbeitsspeicher ](images/mess-error-image59.png)

In diesem Beispiel sind die Probleme und die empfohlene Lösung sehr unwahrscheinlich.

- **Wenn das Problem ein falscher Wert ist, den der Benutzer eingegeben hat, verwenden Sie die ergänzende Anweisung, um die richtigen Werte zu erläutern.** Benutzer sollten diese Informationen nicht aus einer anderen Quelle ermitteln müssen.
- **Stellen Sie keine Projekt Mappe bereit, wenn Sie von der Problem Anweisung trivial abgeleitet werden kann.**

![Screenshot der Meldung: falscher Zeitwert ](images/mess-error-image33.png)

In diesem Beispiel ist keine ergänzende Anweisung erforderlich. die Lösung kann in der Problem Anweisung trivial abgeleitet werden.

- **Wenn die Lösung mehrere Schritte umfasst, stellen Sie die Schritte in der Reihenfolge dar, in der Sie abgeschlossen werden sollten.** Vermeiden Sie jedoch mehrstufige Lösungen, da Benutzer Schwierigkeiten haben, mehr als zwei oder drei einfache Schritte zu merken. Wenn weitere Schritte erforderlich sind, lesen Sie das entsprechende Hilfethema.
- **Halten Sie ergänzende Anweisungen kurz.** Geben Sie nur an, was Benutzer wissen müssen. Lassen Sie unnötige Details aus. Ziel: maximal drei Sätze mit mittlerer Länge.
- **Um Fehler zu vermeiden, während Benutzeranweisungen ausführen, fügen Sie die Ergebnisse vor der Aktion ein.**

**Richtig:**

Um Windows neu zu starten, klicken Sie auf OK.

**Falsch:**

Klicken Sie zum Neustarten von Windows auf OK.

Im falschen Beispiel klicken Benutzer mit der Wahrscheinlichkeit, dass Sie versehentlich auf OK klicken.

- **Es empfiehlt sich nicht, einen Administrator zu kontaktieren, es sei denn, dies ist eine der wahrscheinlichsten Lösungen für das Problem.** Reservieren Sie solche Lösungen für Probleme, die nur von einem Administrator gelöst werden können.

**Falsch:**

![Screenshot der Meldung: Server nicht verfügbar ](images/mess-error-image60.png)

In diesem Beispiel ist das Problem wahrscheinlich mit der Netzwerkverbindung des Benutzers, daher ist es nicht sinnvoll, einen Administrator zu kontaktieren.

- **Sie sollten sich nicht an den technischen Support wenden.** Die Option, sich an den technischen Support zu wenden, um ein Problem zu beheben, ist immer verfügbar und muss nicht durch Fehlermeldungen herauf gestuft werden. Konzentrieren Sie sich stattdessen auf das Schreiben hilfreicher Fehlermeldungen, damit Benutzer Probleme lösen können, ohne sich an den technischen Support zu wenden.

**Falsch:**

![Screenshot, der die Meldung "dieses Element kann nicht geöffnet werden" anzeigt. ](images/mess-error-image61.png)

In diesem Beispiel empfiehlt die Fehlermeldung fälschlicherweise die Kontaktaufnahme mit dem technischen Support.

- Verwenden Sie vollständige Sätze, die Groß-/Kleinschreibung und die endinterpunktions Zeichen.

**Commit-Schaltflächen**

- Wenn die Fehlermeldung Befehls Schaltflächen oder Befehls Verknüpfungen enthält, mit denen das Problem gelöst wird, befolgen Sie die entsprechenden Richtlinien in [Dialog Feldern](win-dialog-box.md).
- Wenn das Programm aufgrund des Fehlers beendet werden muss, geben Sie eine Schaltfläche zum Beenden des Programms an. Um Verwirrung zu vermeiden, verwenden Sie für diesen Zweck nicht Close.
- Stellen Sie andernfalls eine Schaltfläche Schließen bereit. Verwenden Sie für Fehlermeldungen nicht OK, da diese Formulierung impliziert, dass Probleme in Ordnung sind.
  - **Ausnahme:** Verwenden Sie OK, wenn Ihr Fehler Berichterstattungs Mechanismus über behobene Bezeichnungen verfügt (wie bei der MessageBox-API).

## <a name="documentation"></a>Dokumentation

Beim Verweis auf Fehler:

- Informationen zu Fehlern finden Sie in der Haupt Anweisung. Wenn die Haupt Anweisung lang oder ausführlich ist, fassen Sie sie zusammen.
- Falls erforderlich, können Sie als Meldung auf das Dialogfeld Fehlermeldung verweisen. Weitere Informationen finden Sie als Fehlermeldung nur in der Programmierung und in anderen technischen Dokumentationen.
- Formatieren Sie den Text nach Möglichkeit fett formatiert. Andernfalls sollten Sie den Text nur bei Bedarf in Anführungszeichen setzen, um Verwechslungen zu vermeiden.

**Beispiel:** Wenn eine Laufwerk Nachricht **keine CD-CD** enthält, fügen Sie eine neue CD-CD in das Laufwerk ein, und wiederholen Sie den Vorgang.
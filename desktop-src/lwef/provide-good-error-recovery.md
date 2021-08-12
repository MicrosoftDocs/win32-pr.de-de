---
title: Bereitstellen einer guten Fehlerwiederherstellung
description: Bereitstellen einer guten Fehlerwiederherstellung
ms.assetid: 48e00638-9274-49db-93ec-ed444f526441
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486e6db4365e9a279c844e7637ca3281a66b51a2e47d6d2d74d374ab4c55f146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246920"
---
# <a name="provide-good-error-recovery"></a>Bereitstellen einer guten Fehlerwiederherstellung

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

Wie bei jeder gut entworfenen Schnittstelle sollte der interaktive Prozess die Umstände minimieren, die zu Fehlern führen. Es ist jedoch selten möglich, alle Fehler zu beseitigen. Daher ist die Unterstützung einer guten Fehlerwiederherstellung von entscheidender Bedeutung, um das Vertrauen und Dasein des Benutzers zu erhalten. Im Allgemeinen umfasst die Fehlerwiederherstellung das Erkennen eines Fehlers, das Ermitteln der Ursache und das Definieren einer Methode zum Beheben des Fehlers. Benutzer reagieren besser auf schnittstellen, die kooperativ sind und mit dem Benutzer zusammenarbeiten, um eine Aufgabe zu erfüllen.

Der erste Schritt bei der Wiederherstellung von Sprachfehlern ist die Erkennung der Fehlerbedingung. Die Spracherkennung kann aufgrund einer Vielzahl von Fehlern fehlschlagen. Fehlerbedingungen können in der Regel als Ergebnis einer ungültigen Eingabe, einer expliziten Benutzerkorrektur oder eines Abbruchs oder einer Benutzerwiederholung erkannt werden.

Ein *Ablehnungsfehler tritt* auf, wenn die Erkennungs-Engine keine Übereinstimmung mit dem hat, was der Benutzer gesagt hat. Hintergrundgeräusche oder frühe Starts sind auch häufige Ursachen für Erkennungsfehler. Daher ist es häufig eine gute erste Lösung, den Benutzer auf die Wiederholung eines Befehls zu bitten. Wenn sich der Ausdruck jedoch außerhalb der aktuellen aktiven Grammatik befindet, kann die Aufforderung des Benutzers, die Anforderung umzuformulieren, das Problem lösen. Der Unterschied in der Formulierung kann zu einer Übereinstimmung mit etwas in der aktuellen Grammatik führen. Das Auflisten oder Vorschlagen geeigneter erwarteter Eingabeoptionen ist eine weitere Alternative.

Eine gute Strategie für die Wiederherstellung von Ablehnungsfehlern besteht in der Kombination dieser Techniken, um den Benutzer wieder auf Kurs zu bringen und immer mehr Unterstützung zu bieten, wenn der Fehler weiterhin auftritt. Sie können beispielsweise mit einem Interrogativ wie "Huh?" auf den anfänglichen Fehler reagieren. oder "Was?" oder eine Hand-zu-Die-Hand-Geste. Eine kurze Antwort erhöht die Wahrscheinlichkeit, dass die wiederholte Anweisung des Benutzers nicht fehlschlägt, da der Benutzer zu früh sprach. Bei einem wiederholten Fehler erhöht die nachfolgende Anforderung zur Neuformulierung die Wahrscheinlichkeit, dass etwas innerhalb der angegebenen Grammatik abgleicht. Von hier aus erhöht die Bereitstellung expliziter Eingabeaufforderungen akzeptierter Befehle die Wahrscheinlichkeit einer Übereinstimmung weiter. Dieses Verfahren wird im folgenden Beispiel veranschaulicht:

**Benutzer:** Ich möchte eine Pizza im Chicago-Stil mit Anchopuls.

**Character**: (Hand to Ear) Huh?

**Benutzer:** Ich möchte eine Chicago-Pizza mit anchopuls.

**Zeichen:**(Kopf schütteln) Bitte umformulieren Sie Ihre Anforderung.

**Benutzer:** Ich habe Chicago pizza, with anchopuls(Pizza in Chicago) mit einemChopuls gesagt.

**Zeichen:**(Shrug) I'sorry. Teilen Sie mir den Pizzastil mit, den Sie wünschen.

**Benutzer:** Chicago, mit anchopuls.

**Zeichen:** Immer noch kein Zufall. Folgendes können Sie sagen: "Chicago", "Sollanisch" oder "Kombination".

Damit sich die Fehlerbehandlung natürlicher anfühlt, stellen Sie sicher, dass Sie bei der Reaktion auf Fehler ein gewisses Maß an Zufälligkeit bereitstellen. Darüber hinaus besteht eine natürliche Reaktion des Benutzers auf jede Anforderung zum Wiederholen einer Antwort in der Überhitzung oder Erhöhung des Volumens, wenn die Anweisung wiederholt wird. Es kann hilfreich sein, den Benutzer gelegentlich daran zu erinnern, normal und eindeutig zu sprechen, da die Sprechmaschine die Wörter durch die Sprechweise oder eine höhere Lautstärke schwieriger erkennen kann.

Progressive Unterstützung sollte mehr tun, als den Fehler auf den Benutzer aufmerksam zu machen. Sie sollte den Benutzer beim Sprechen in der aktuellen Grammatik leiten, indem er nacheinander informativere Meldungen liefert. Schnittstellen, die zu verstehen scheinen, fördern ein hohes Maß an Zufriedenheit und Toleranz für den Benutzer.

*Ersetzungsfehler,* bei denen die Sprach-Engine die Eingabe erkennt, aber mit dem falschen Befehl übereinstimmen, sind schwieriger aufzulösen, da die Sprach-Engine eine übereinstimmende Äußerung erkennt. Ein Konflikt kann auch auftreten, wenn die Sprach-Engine unneindeutige Sounds als gültige Eingabe interpretiert (auch als Einfügefehler *bekannt).* In diesen Situationen ist die Unterstützung des Benutzers erforderlich, um den Fehlerzustand zu identifizieren. Hierzu können Sie wiederholen, was die Sprach-Engine zurückgegeben hat, und den Benutzer bitten, dies zu bestätigen, bevor Sie fortfahren:

**Benutzer:** Ich möchte eine Pizza im Chicago-Stil.

**Zeichen:** Haben Sie gesagt, dass Sie eine Pizza im Chicago-Stil möchten?

**Benutzer:** Ja.

**Zeichen:** Welche zusätzlichen Bestandteile möchten Sie verwenden?

**Benutzer:** Anchowähls.

**Zeichen:** Haben Sie "anchopuls" gesagt?

**Benutzer:** Ja.

Die Verwendung dieser Technik für jede Äußerung wird jedoch ineffizient und ermüdend. Um dies zu behandeln, beschränken Sie die Bestätigung auf Situationen, die erhebliche negative Folgen haben, oder erhöhen Sie die Komplexität der unmittelbaren Aufgabe. Wenn es für den Benutzer einfach ist, Änderungen vorzunehmen oder umzukehren, können Sie möglicherweise vermeiden, eine Bestätigung seiner Auswahl an fordern. Wenn Sie Auswahlmöglichkeiten sichtbar machen, müssen Sie möglicherweise keine explizite Korrektur vornehmen. Wenn Sie beispielsweise ein Element aus einer Liste auswählen, ist möglicherweise keine Überprüfung erforderlich, da der Benutzer die Ergebnisse sehen und leicht ändern kann. Sie können auch Konfidenz und alternative Bewertungen verwenden, um einen Schwellenwert für die Bestätigung zu geben. Sie können den Schwellenwert anpassen, indem Sie einen Verlauf der Aktionen des Benutzers in einer bestimmten Situation behalten und die Überprüfung basierend auf einer konsistenten Benutzerbestätigung beseitigen. Berücksichtigen Sie abschließend die multi-modale Natur der Schnittstelle. Eine Bestätigung mit der Maus oder Tastatur kann ebenfalls geeignet sein.

Wählen Sie den Wortlaut der Bestätigungen sorgfältig aus. Beispiel: "Haben Sie gesagt...?" oder "I think you said..." sind besser als "Möchten Sie wirklich...?" da die ersten Ausdrücke implizieren, dass die Genauigkeit des Lauschens (Erkennung) des Zeichens abgefragt wird, nicht, dass der Benutzer möglicherweise falsch gepoket hat.

Berücksichtigen Sie auch die Grammatik für eine Antwort. Eine negative Antwort generiert z. B. wahrscheinlich einen Ablehnungsfehler, der eine zusätzliche Eingabeaufforderung erfordert, wie im folgenden Beispiel gezeigt:

**Benutzer:** Ich möchte eine Paprikaoni.

**Zeichen:** Haben Sie "no ham" gesagt?

**Benutzer:** Nein, ich habe "paponi" gesagt.

**Zeichen:** Huh?

**Benutzer:** Paponi.

Wenn Sie Ihre Grammatik so ändern, dass sie Präfixe enthält, um Variationen natürlicher Antworten zu verarbeiten, erhöht sich die Effizienz des Wiederherstellungsprozesses, insbesondere wenn der Benutzer die Überprüfungsaufforderung nicht bestätigt. In diesem Beispiel hätte die Bestätigung in einem einzigen Schritt behandelt werden können, indem die Grammatik für die "Paprikaoni" geändert wurde, indem auch "no I said paponi", "I said paponi" und "no paponi" (keine Paprikaoni) angegeben wurden.

Sie können Ersetzungsfehler auch mit den alternativen Übereinstimmungen behandeln, die von der Sprach-Engine als Korrekturbestätigung zurückgegeben werden:

**Benutzer:** Ich möchte eine Paprikaoni.

**Character**: (Hears "no ham" as best match, "peponi" as first alternative) Did you say "no ham"?

**Benutzer:** Nein, paponi.

**Character**: (No Ham" wird immer noch als beste Übereinstimmung hören, bietet aber jetzt die erste Alternative) "Paprika"?

Auf ähnliche Weise können Sie einen Verlauf häufiger Ersetzungsfehler behalten und, wenn ein bestimmter Fehler häufig auftritt, die Alternative zum ersten Mal anbieten.

Vermeiden Sie in jeder Erkennungsfehlersituation, dem Benutzer die Lädung zu geben. Wenn das Zeichen vorschlägt oder sogar impliziert, dass der Benutzer dafür verantwortlich ist, oder das Zeichen dem Fehler indifferent erscheint, kann der Benutzer beleidigt werden. Wählen Sie hier auch sorgfältig eine Formulierung aus, die explizit verantwortungsbeantwortend ist, für die Situation geeignet ist und die Vielfalt verwendet, um eine natürlichere Antwort zu schaffen. Vermeiden Sie beim Ausdrücken einer Apologie mehrdeutige Wörter wie "oops" oder "oh", die als Beleidigen des Benutzers interpretiert werden könnten. Verwenden Sie stattdessen Ausdrücke wie "I'morry" oder "My mistake". Wiederholte oder schwerwiegendere Fehler können eine aufwendigere Apologie verwenden, z. B. "Ich bedaure das wirklich". Berücksichtigen Sie auch die Persönlichkeit des Zeichens, wenn Sie den Typ der Antwort bestimmen. Eine weitere Möglichkeit besteht in der Verantwortlichung einer externen Situation. Kommentare wie "Belässig, es ist laut," nehmen dem Benutzer und dem Zeichen die Verantwortung. Es kann auch hilfreich sein, den Benutzer an den kooperativen Charakter der Interaktion zu erinnern: Betrachten Sie Ausdrücke wie "Sehen wir uns an, was wir tun können, um diese Arbeit zu ermöglichen."

Microsoft Agent unterstützt auch einige automatisches Feedback zur Erkennung. Wenn eine Äußerung erkannt wird, zeigt der Lauschende Tipp den Stimmtext der besten gehörten Übereinstimmung an. Sie können ihren eigenen Text festlegen, der basierend auf der Konfidenzeinstellung für einen von Ihnen festgelegten Befehl angezeigt wird.

Aufgrund des Fehlerpotenzials ist immer eine Bestätigung für alle Entscheidungen erforderlich, die schwerwiegende negative Folgen haben und nicht rückgängig gemacht werden können. Natürlich sollten Sie eine Bestätigung verlangen, wenn die Ergebnisse einer Aktion destruktiv sein könnten. Erwägen Sie jedoch auch eine Bestätigung für Situationen, in denen ein längerer Prozess oder Vorgang abgebrochen wird.

 

 





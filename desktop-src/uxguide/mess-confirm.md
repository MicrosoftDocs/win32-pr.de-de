---
title: Bestätigungen
description: Eine Bestätigung ist ein modales Dialogfeld, in dem gefragt wird, ob der Benutzer mit einer Aktion fortfahren möchte.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 321cab040423df3a6dc0069d568d66c85e3aa8cc
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524524"
---
# <a name="confirmations"></a>Bestätigungen

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine Bestätigung ist ein modales Dialogfeld, in dem gefragt wird, ob der Benutzer mit einer Aktion fortfahren möchte.

![Screenshot: Editor "Möchten Sie Änderungen speichern?" .](images/mess-confirm-image1.png)

Eine typische Bestätigung.

Bestätigungen weisen die folgenden wesentlichen Merkmale auf:

-   Sie werden als direktes Ergebnis einer vom Benutzer initiierten Aktion angezeigt.
-   Sie überprüfen, ob der Benutzer mit der Aktion fortfahren möchte.
-   Sie bestehen aus einer einfachen Frage und mindestens zwei Antworten.

Bestätigungen sind besonders nützlich, wenn der Benutzer für die Aktion eine relevante und eindeutige Auswahl treffen muss, die später nicht getroffen werden kann. Diese Auswahl beinhaltet häufig ein Gewisses an Risiko, das für den Benutzer nicht offensichtlich ist, aber das Risiko ist für Bestätigungen nicht entscheidend. Diese Elemente sind erforderlich, um die Unterbrechung der Reaktion auf einen modalen Dialog zu rechtfertigen.

Im Gegensatz dazu stellen [Warnmeldungen](mess-warn.md) eine Bedingung dar, die in Zukunft ein Problem verursachen kann. Ihr grundlegendes Merkmal ist, dass sie Risiken mit sich bringen:

-   Sie umfassen den möglichen Verlust einer oder mehrerer der folgenden Punkte:
    -   Eine wertvolle Ressource, z. B. Datenverlust oder finanzieller Verlust.
    -   Systemzugriff oder -integrität.
    -   Datenschutz oder Kontrolle über vertrauliche Informationen.
    -   Die Zeit des Benutzers (eine erhebliche Menge, z. B. 30 Sekunden oder mehr).
-   Sie haben unerwartete oder unbeabsichtigte Folgen.
-   Sie erfordern jetzt eine korrekte Behandlung, da Fehler nicht einfach behoben werden können und sogar nicht rückgängig gemacht werden können.

Wenn eine Bestätigung ein Risiko mit sich bringt, kann sie auch als Warnung betrachtet werden. Daher gelten auch die Warnmeldungsrichtlinien.

**Hinweis:** Richtlinien im Zusammenhang mit [Dialogfeldern,](win-dialog-box.md) [Fehlermeldungen,](mess-error.md) [Layout](vis-layout.md)und [Warnmeldungen](mess-warn.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Wird dem Benutzer eine Frage gestellt, um mit einer Aktion fortzufahren, die über zwei oder mehr Antworten verfügt?** Wenn nicht, ist die Nachricht keine Bestätigung.
-   **Stellt die Benutzeroberfläche einen Fehler oder ein Problem dar, das aufgetreten ist?** Verwenden Sie in diesem Falle stattdessen eine [Fehlermeldung.](mess-error.md)
-   **Erfordert das Fortfahren mit der Aktion, dass der Benutzer eine Auswahl treffen muss, die keinen geeigneten Standardwert hat?** In diesem Falle kann eine Bestätigung angemessen sein.
-   **Gibt es einen alternativen Entwurf, der die Notwendigkeit der Bestätigung entfällt?** Die Notwendigkeit einer Bestätigung deutet manchmal auf einen Entwurfsfehler hin. Häufig gibt es eine bessere Entwurfsalternative, für die keine Bestätigung erforderlich ist.
-   **Führt der Benutzer eine riskante Aktion aus?** In diesem Falle ist eine Bestätigung geeignet, wenn die Aktion erhebliche Folgen hat oder nicht einfach rückgängig zu werden ist.
-   **Wird der Benutzer eine Aufgabe verwerfen?** Wenn ja, bestätigen Sie dies nicht. Gehen Sie davon aus, dass Benutzer die Konsequenzen verstehen, die sich daraus ergeben, dass eine Aufgabe nicht abgeschlossen wird.
-   **Hat die Aktion Konsequenzen, die Benutzer möglicherweise nicht kennen?** In diesem Falle kann eine Bestätigung angemessen sein.
-   **Führen Benutzer aufgrund des aktuellen Kontexts wahrscheinlich eine fehlerhafte Aktion aus?** In diesem Falle kann eine Bestätigung angemessen sein.
-   **Führen Benutzer die Aktion häufig aus?** Ziehen Sie in diesem Falle einen alternativen Entwurf in Betracht. Häufige Bestätigungen sind ängstlich und haben wenig Nutzen, da Benutzer lernen, ohne Zudenkungen zu reagieren.
-   **Hat die Aktion Auswirkungen auf die Sicherheit?** In diesem Falle ist möglicherweise auch dann eine Bestätigung erforderlich, wenn in den vorherigen Tests etwas anderes angegeben ist.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="unnecessary-confirmations-are-annoying"></a>Unnötige Bestätigungen sind ungern

Die erste windows-Bestätigung, die jemals erstellt wurde, sieht wie folgt aus:

![Screenshot von "Are you sure?" Bestätigung ](images/mess-confirm-image2.png)

Die ursprüngliche bestätigungsaufhärkung.

Dies war ein sehr schlechter Start. Wenn Sie möchten, dass Benutzer Ihr Programm hassen, sollten Sie einfach Bestätigungen wie diese durchgehen lassen. Um zu verstehen, warum, berücksichtigen Sie den Standpunkt des Benutzers. Der Benutzer hat lediglich aufgefordert, eine Aktion gemäß der Definition einer Bestätigung auszuführen, es sei denn, etwas wurde versehentlich angeklickt oder gedrückt, natürlich möchte der Benutzer fortfahren.

Nicht nur unnötige Bestätigungen sind ungern, sie sind auch nicht effektiv, um den Benutzer vor Fehlern zu schützen. Benutzer erkennen schnell, wenn ein Programm unnötige Bestätigungen hat und ihre natürliche Reaktion darin besteht, sie so schnell wie möglich zu verwerfen, oft ohne Lesen. Folglich sind solche Bestätigungen nicht viel mehr, als diesen Aufgaben einen zusätzlichen Schritt hinzuzufügen.

Verwenden Sie keine Bestätigungen, nur weil es die Möglichkeit gibt, dass Benutzer einen Fehler machen. **Stattdessen sind Bestätigungen am effektivsten, wenn sie verwendet werden, um Aktionen zu bestätigen, die erhebliche oder unbeabsichtigte Folgen haben.** Gute Bestätigungen geben nie das Offensichtliche an. Sie sollten etwas kommunizieren, das Benutzer aus einem guten Grund kennen müssen, um nicht fortzufahren. Und sie werden nur verwendet, wenn sie wirklich von einer Aktion benötigt werden, z. B. wenn Benutzer aufgefordert werden, Änderungen nur dann zu speichern, wenn Änderungen gespeichert werden sollten. Dies erfordert die Aufmerksamkeit des Benutzers nur, wenn dies wirklich gerechtfertigt ist.

Für andere Arten von Bestätigungen gibt es häufig eine bessere Entwurfsalternative als das Erzwingen der Beantwortung einer Frage durch die Benutzer.

### <a name="consider-the-design-alternatives"></a>Berücksichtigen der Entwurfsalternativen

Hier sind einige Entwurfsalternativen, die routinemäßige Bestätigungen überflüssig machen:

-   **Fehler verhindern.** Entwerfen Sie Aufgaben so, dass schwerwiegende Fehler versehentlich schwer zu machen sind. Trennen Sie beispielsweise destruktive Befehle physisch von anderen Befehlen, und müssen mehrere Aktionen abgeschlossen werden.
-   **Geben Sie rückgängig an.** Bieten Sie die Möglichkeit, Aktionen rückgängig zu machen. Beispielsweise erfordert das Löschen einer Datei in Microsoft Windows in der Regel keine Bestätigung, da gelöschte Dateien aus dem Papierkorb wiederhergestellt werden können. Beachten Sie Folgendes: Wenn eine Aktion sehr einfach auszuführen ist, reicht es möglicherweise aus, wenn Benutzer die Aktion wiederholen.
-   **Geben Sie Feedback.** Machen Sie unerwünschte Ergebnisse offensichtlich. Die Bereitstellung von Rückgängig machen allein reicht nicht aus, wenn Benutzer nicht erkennen, wann sie einen Fehler machen. Beispielsweise sollte die Auswirkung der direkten Bearbeitung (z. B. ein Drag & Drop-Vorgang) immer offensichtlich sein.
-   **Nehmen Sie das wahrscheinliche Ergebnis an, aber erleichtern Sie es, sich zu ändern.** Wenn Sie nicht sicher sind, was Benutzer wünschen, aber es eine wahrscheinliche, sichere und sichere Auswahl gibt, nehmen Sie diese Auswahl an, machen Sie klar, was passiert ist, und vereinfachen Sie die Änderung mithilfe eines Kontextmenüs. Microsoft Word geht beispielsweise davon aus, dass Benutzer Wörter richtig schreiben möchten. Wenn ein falsch geschriebenes Wort erkannt wird und die wahrscheinlich richtige Schreibweise bekannt ist, führt Word automatisch die Korrektur durch, ermöglicht benutzern jedoch das Zurücksetzen.
-   **Entfernen Sie die Auswahl vollständig.** Wenn die Auswahl nicht wichtig ist, ist es den Benutzern einfach egal. Es ist besser, ihr Programm zu [vereinfachen](/previous-versions//dn742474(v=vs.85)) und die Auswahl zu vermeiden.

### <a name="make-confirmations-require-thought"></a>Machen Sie sich Gedanken über Bestätigungen.

Damit eine Bestätigung über einen Wert verfügen kann, müssen Benutzer den Grund verstehen, warum sie nicht fortfahren möchten. Manchmal ist der Grund offensichtlich, z. B. wenn Benutzer ein Dokument mit Änderungen schließen, die nicht gespeichert wurden:

![Screenshot: "Möchten Sie Änderungen speichern?" ausgegeben wird.](images/mess-confirm-image3.png)

In diesem Beispiel ist der Grund für die Bestätigung offensichtlich.

In anderen Situationen ist der Grund möglicherweise nicht so offensichtlich.

Bei der Auswahl von Commitschaltflächenbezeichnungen für Dialogfelder besteht die [allgemeine Richtlinie](win-dialog-box.md) darin, Bezeichnungen auszuwählen, die bestimmte Antworten auf die Hauptanweisung sind. Dies führt zu einer effizienten Entscheidungsfindung, da Benutzer eine Mindestmenge an Text lesen müssen, um fortzufahren. Dieses Effizienzziel kann jedoch für Bestätigungen kontraproduktiv sein. Betrachten Sie das folgende Beispiel:

**Falsch:**

![Screenshot der Bestätigung mit Der Deinstallationsschaltfläche ](images/mess-confirm-image4.png)

In diesem Beispiel erfordert die richtige Antwort Gedanken.

Wenn Sie diese Bestätigung unmittelbar nach dem Ausführen des Deinstallationsbefehls durch den Benutzer präsentieren, lautet die Antwort des Benutzers wahrscheinlich "Natürlich möchte ich deinstallieren!" Der Benutzer klickt auf Deinstallieren, ohne einen zweiten Gedanken zu machen.

Für Bestätigungen möchten wir nicht, dass Benutzer voreigen, emotionalen Entscheidungen treffen. Um Benutzer dazu zu ermutigen, über ihre Antwort nach nachdenken zu können, müssen wir eine kleine Entscheidungsfindungsgeschwindigkeit bereitstellen. Wenn dies praktisch ist, ist es in der Regel besser, commit-Schaltflächen sorgfältig zu formulieren. Beispielsweise können wir eine zusätzliche Sprache verwenden, um anzugeben, dass es einen Grund gibt, nicht fortzufahren.

**Besser:**

![Screenshot der Schaltfläche "Deinstallation trotzdem" ](images/mess-confirm-image5.png)

In diesem Beispiel wird der Schaltflächenbezeichnung "Commit" "anyway" hinzugefügt, um anzugeben, dass die Bestätigung einen Grund dafür gibt, nicht fortzufahren.

Wenn dieser Ansatz nicht praktikabel ist, können wir die Schaltflächen Ja/Nein für Commits verwenden.

**Außerdem ist es besser:**

![Screenshot der Bestätigung mit Ja/Nein-Schaltflächen ](images/mess-confirm-image6.png)

In diesem Beispiel erzwingt die Verwendung von Ja/Nein-Commitschaltflächen, dass Benutzer zumindest die Hauptanweisung lesen müssen.

### <a name="provide-all-the-information"></a>Geben Sie alle Informationen an.

Wenn Sie eine Frage stellen möchten, müssen Sie genügend Informationen bereitstellen, damit Benutzer diese Frage intelligent beantworten können. Betrachten Sie das Dialogfeld Dateier ersetzt bestätigen von Windows XP:

![Screenshot des Dialogfelds "Datei ersetzen bestätigen" ](images/mess-confirm-image7.png)

Das Dialogfeld Windows XP Confirm File Replace (Datei ersetzen bestätigen)

Stellt diese Bestätigung alle Informationen zur Verfügung, die Benutzer möglicherweise benötigen, um die Frage zu beantworten? Bevor Sie antworten, sollten Sie die gängigsten Benutzerszenarien berücksichtigen:

-   Kopieren (oder verschieben) Sie die andere Datei, und ersetzen Sie dabei die vorhandene Datei.
-   Behalten Sie die vorhandene Datei bei, ohne die andere Datei zu kopieren oder zu verschieben.
-   Behalten Sie die neuere Datei bei , oder kopieren Sie sie (oberstes Szenario).
-   Behalten Sie entweder die vorhandene Datei bei, oder kopieren Sie die andere Datei, je nach Kriterien wie Dateiinhalt und -größe.
-   Behalten Sie die vorhandene Datei bei, und kopieren Sie die andere Datei unter einem anderen Namen.
-   Brechen Sie den Vorgang ab, wenn etwas falsch oder unerwartet ist.

Benutzer können Szenario 1 erreichen, indem sie auf Ja und Szenario 2 durch Klicken auf Nein klicken. Sie können Szenario 3 erreichen, indem sie die Dateidaten vergleichen und auf die entsprechende Schaltfläche klicken. Beachten Sie jedoch, wie viel Zeit benötigt wird, um die neuere Datei zu bestimmen und dann die entsprechende Schaltfläche zu bestimmen, insbesondere für das wahrscheinlich häufigste Szenario.

Die Szenarien 4, 5 und 6 sind ebenfalls überraschend schwierig. Die Dateigrößen werden aufgerundet, sodass beispielsweise nicht bestimmt werden kann, ob diese Dateien die gleiche Größe haben oder ob es sich um dieselbe Datei handelt. Die Symbole gelten für die Anwendung, die zum Öffnen der Datei verwendet wird, sodass Benutzer die Dateien öffnen müssen, um ihre Inhalte zu überprüfen und zu vergleichen. Miniaturansichten des Dateiinhalts wären viel nützlicher, um die Frage zu beantworten.

Die Bestätigung zum Kopieren von Dateien aus Windows Vista bietet eine wesentlich bessere Verarbeitung dieser Szenarien, indem weitere Informationen angegeben und die Option hinzugefügt wird, um beide Dateien zu behalten:

![Screenshot des Dialogfelds "Datei kopieren" ](images/mess-confirm-image8.png)

Die Bestätigung zum Kopieren der Windows Vista-Datei.

### <a name="provide-specific-useful-information"></a>Bereitstellen spezifischer, nützlicher Informationen

Wenn Sie eine Frage stellen möchten, stellen Sie sicher, dass die Benutzer die Frage und die Auswirkungen der alternativen Antworten verstehen. Betrachten Sie diese Windows Internet Explorer-Sicherheitsbestätigung:

![Screenshot der Bestätigung mit einer ungenauen Frage ](images/mess-confirm-image9.png)

Eine ungenaue Sicherheitsbestätigung.

Diese Bestätigung stellt eine Frage, die Benutzer möglicherweise nicht intelligent beantworten können. Der Benutzer hat angefordert, dass Windows Internet Explorer Eine Seite anzeigen soll. Diese Meldung rät davon implizit ab, indem er den Text formuliert und Nein als Standardauswahl hervorhebt.

Das spezifische Sicherheitsproblem, das die Seite darstellt, ist nicht ausreichend erklärt, daher ist das Risiko des Fortsetzens nicht klar. Welche Informationen in der Bestätigung würden dazu führen, dass der Benutzer jemals auf Nein klickt? Aufgrund der Unschärfe der Nachricht wird die Bestätigung die Benutzer wahrscheinlich nicht davon abraten, fortzuführen, aber sie werden sich darüber nicht schlecht fühlen.

Damit diese Bestätigung nützlich ist, muss sie spezifischere Informationen bereitstellen, die dazu führen können, dass der Benutzer sich gegen den Vorgang entscheidet. Im Allgemeinen sollten Sie für jede Antwort in einer Bestätigung die Szenarien berücksichtigen, die sie erfordern, und stellen Sie sicher, dass genügend Informationen bereitgestellt werden, damit Benutzer sie auswählen können. Stellen Sie Auswahlmöglichkeiten und keine Spalten zur Verfügung.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Ermitteln, ob eine Bestätigung erforderlich ist

Wenn Sie sich die Szenarien und die Wahrscheinlichkeit der Auswahl der einzelnen Antworten durchdenknen, ist dies ein systematischer Weg, um zu bestimmen, ob eine Bestätigung erforderlich ist. Wenn Benutzer wahrscheinlich alle Antworten auswählen, ist die Bestätigung erforderlich und nützlich. Wenn jedoch nur eine Antwort wahrscheinlich ist (z. B. 98 Prozent der Zeit), ist die Bestätigung eindeutig unnötig und sollte entfernt werden. Beachten Sie, dass Bestätigungen im Zusammenhang mit Sicherheits-, Rechtlichen- und Sicherheitsproblemen mögliche Ausnahmen sind.

![Screenshot von "Möchten Sie Einstellungen ändern?" ](images/mess-confirm-image10.png)

Ist diese Bestätigung erforderlich? Wählen Benutzer jemals Nein aus? Dies ist möglich, aber sehr unwahrscheinlich. Diese Bestätigung sollte entfernt werden.

**Wenn Sie nur drei Dinge tun...**

1. Stellen Sie sicher, dass Ihre Bestätigung wirklich erforderlich ist. Es sollte einen legitimen und eindeutigen Grund geben, nicht fortzufahren, und es kann sein, dass Benutzer dies manchmal nicht machen.

2. Wenn der Grund für die Bestätigung nicht sofort offensichtlich ist, wählen Sie Commitschaltflächen aus, die Benutzer dazu ermutigen, ihre Antwort zu überlegen. In der Regel erfolgt dies, indem die Bestätigung als Ja oder Nein-Frage formuliert und vollständig selbsterklärende oder Ja/Nein-Antworten angegeben werden.

3. Berücksichtigen Sie alle Szenarien, und stellen Sie die Informationen zur Verfügung, die erforderlich sind, um die Frage intelligent zu beantworten.

## <a name="usage-patterns"></a>Verwendungsmuster

Bestätigungen haben mehrere Verwendungsmuster:



|   Verwendung                                                                                                                                                                    |    Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Routinemäßige Bestätigungen**<br/> vergewissern Sie sich, dass der Benutzer mit einer routinemäßigen Aktion mit geringem Risiko fortfahren möchte. <br/>                                              | Diese Bestätigungen werden in der Regel mit "Sind Sie sicher... ?" bezeichnet. und verfügen häufig über das Kontrollkästchen Diese Meldung nicht mehr anzeigen, um deren Generanz zu minimieren. <br/> ![Screenshot von "Ordner in Papierkorb verschieben?" ](images/mess-confirm-image11.png)<br/> ![Screenshot von "Nachricht nicht mehr anzeigen" ](images/mess-confirm-image12.png)<br/> Beispiele für Routinebestätigungen.<br/> **Hinweis:** Dieses Muster ist in der Regel nicht erforderlich und sollte vermieden werden.<br/>                                                                                                                                                                                                                                                                                        |
| **Bestätigungen riskanter Aktionen**<br/> vergewissern Sie sich, dass der Benutzer mit einer Aktion fortfahren möchte, die ein gewisses Risiko auf sich hat und nicht einfach rückgängig gemacht werden kann. <br/>            | Da sie ein Risiko haben, verfügen diese Bestätigungen in der Regel über ein Warnsymbol. <br/> ![Screenshot, der ein Beispiel für die Bestätigung der Volumeformatierung zeigt.](images/mess-confirm-image13.png)<br/> ![Screenshot, der ein Beispiel für die Bestätigung des dauerhaften Löschens zeigt.](images/mess-confirm-image14.png)<br/> Beispiele für Bestätigungen riskanter Aktionen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Unbeabsichtigte Folgebestätigungen**<br/> bestätigen, dass der Benutzer mit einer Aktion fortfahren möchte, die unerwartete oder unbeabsichtigte Folgen hat. <br/> | Diese Bestätigungen stellen nicht nur eine Frage, sondern weisen auch auf die unbeabsichtigten Folgen hin. da sie unbeabsichtigte Folgen haben, verfügen diese Bestätigungen in der Regel über ein Warnsymbol. <br/> ![Screenshot von "Alle Registerkarten schließen?" Bestätigung ](images/mess-confirm-image15.png)<br/> ![Screenshot von "Installation abbrechen?" Bestätigung ](images/mess-confirm-image16.png)<br/> Beispiele für unbeabsichtigte Folgebestätigungen.<br/> Dieses Muster erfordert jedoch, dass die Konsequenzen wirklich unbeabsichtigt sind. <br/> **Falsche:**<br/> ![Screenshot von "Schlüsselprotokollierung deaktivieren?" Bestätigung ](images/mess-confirm-image17.png)<br/> Die Folgen sind hier beabsichtigt, sodass dies eine routinemäßige Bestätigung ist.<br/> |
| **Erläuterungen**<br/> verdeutlichen, wie der Benutzer mit einer Aktion fortfahren möchte, die potenziell mehrdeutige oder unerwartete Folgen hat. <br/>             | Drag & Drop-Vorgänge können zu Erläuterungen führen, wenn die Auswirkungen des Vorgangs falsch interpretiert werden können. <br/> ![Screenshot von "Nur dieses Vorkommen ändern?"](images/mess-confirm-image18.png)<br/> ![Screenshot von "Immer beim Beenden speichern?" Bestätigung ](images/mess-confirm-image19.png)<br/> Beispiele für Erläuterungen.<br/> **Hinweis:** Dieses Muster sollte vermieden werden, da es besser ist, Aktionen ohne mehrdeutige Folgen zu entwerfen und das wahrscheinlichste gewünschte Ergebnis zu erwarten. <br/>                                                                                                                                                                                                                                     |
| **Sicherheitsbestätigungen**<br/> bestätigen, dass der Benutzer eine Aktion mit Sicherheitsfolgen fortsetzen möchte. <br/>                                   | ![Screenshot von "Möchten Sie diese Software ausführen?" ](images/mess-confirm-image20.png)<br/> ![Screenshot von "Kennwort speichern?" Bestätigung ](images/mess-confirm-image21.png)<br/> Beispiele für Sicherheitsbestätigungen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Ulterior-Motivbestätigungen**<br/> Geben Sie Informationen zu einer Aktion an, aber stellen Sie sie als Bestätigung dar. <br/>                                       | Diese Dialogfelder werden zwar als Bestätigungen angezeigt, ihr eigentliches Ziel ist jedoch die Schulung von Benutzern oder die Ankündigung von Features. <br/> ![Screenshot: Soll diese Symbolleiste auf der Taskleiste angezeigt werden? ](images/mess-confirm-image22.png)<br/> Ein Beispiel für eine Ulterior-Motivbestätigung.<br/> **Hinweis:** Dieses Muster wird nicht empfohlen, da es in der Regel eine bessere, direktere Alternative gibt. [Animationen](vis-animations.md) sind beispielsweise eine bessere Möglichkeit, die Beziehung zwischen Ursache und Auswirkung anzuzeigen. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie die Bestätigungen "Änderungen speichern" nur, wenn wesentliche Änderungen vorhanden sind.** Bestätigen Sie keine Änderungen, die nicht direkt vom Benutzer vorgenommen wurden, z. B. automatisches Neuformatieren von Dokumenten.

**Falsch:**

![Screenshot, der eine Microsoft Office Outlook zeigt: "Möchten Sie Änderungen speichern?" .](images/mess-confirm-image23.png)

Dieses Beispiel ist falsch, wenn es für eine leere E-Mail oder ein leeres Dokument verwendet wird, das vom Benutzer nicht geändert wurde.

### <a name="icons"></a>Symbole

-   Bestätigungen verwenden keine Titelleistensymbole.
-   **Das Inhaltsbereichssymbol für eine Bestätigung basiert auf seinem Entwurfsmuster:**



    | Muster                                                | Symbol                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Routinemäßige Bestätigungen <br/>                | Kein Symbol. <br/>                                                                                                                         |
    | Bestätigungen riskanter Aktionen <br/>           | Warnsymbol. <br/>                                                                                                                    |
    | Bestätigungen unbeabsichtigter Folgen <br/> | Verwenden Sie ein Warnsymbol, wenn ein Risiko besteht, das Featuresymbol, falls verfügbar. andernfalls kein Symbol. <br/>                                          |
    | Erläuterungen <br/>                       | Wenn die Bestätigung ein Dokument umfasst, verwenden Sie die Miniaturansicht des Dokuments. Verwenden Sie andernfalls ggf. das Featuresymbol oder kein Symbol. <br/> |
    | Sicherheitsbestätigungen <br/>               | Warnsymbol. <br/>                                                                                                                    |
    | Ulterior-Motivbestätigungen <br/>        | Kein Symbol. <br/>                                                                                                                         |



 

-   **Verwenden Sie keine Warnsymbole für Routinefragen.** Dies entspricht dem ermutigenden [Ton von Windows](text-style-tone.md) und sorgt dafür, dass die Verwendung Ihres Programms sich wie eine gefährliche Aktivität anfühlt. Angenommen, Benutzer verstehen die Folgen des Abbruchs einer Aufgabe, bevor sie abgeschlossen ist.

**Falsch:**

![Screenshot von "Möchten Sie das Tutorial beenden?" ](images/mess-confirm-image24.png)

In diesem Beispiel wird ein Warnsymbol verwendet, um eine Routinefrage zu stellen.

### <a name="commit-buttons"></a>Commitschaltflächen

-   **Verwenden Sie bestimmte Antworten auf die Hauptanweisung, wenn der Grund für die Bestätigung offensichtlich ist oder selbsterklärend gemacht werden kann.**

![Screenshot von "Möchten Sie Änderungen speichern?" ](images/mess-confirm-image25.png)

In diesem Beispiel ist der Grund für die Bestätigung offensichtlich, daher funktionieren Speichern und Nicht speichern gut.

-   **Verwenden Sie andernfalls die Schaltflächen Ja und Nein, um Bestätigungsantworten zu erhalten.** Dies sorgt dafür, dass Benutzer die Bestätigung vor dem Reagieren bedenken. Verwenden Sie niemals OK und Abbrechen für Bestätigungen.

**Richtig:**

![Screenshot von "Möchten Sie Unterstützungsdateien deinstallieren?" ](images/mess-confirm-image26.png)

In diesem Beispiel werden Benutzer durch Die Verwendung von Ja/Nein-Commitschaltflächen gezwungen, zumindest die Hauptanweisung zu lesen.

**Falsch:**

![Screenshot von "Reservierung stornieren?" ](images/mess-confirm-image27.png)

In diesem Beispiel ist die Verwendung von OK/Abbrechen verwirrend.

-   **Verwenden Sie bestimmte Antworten auf die Hauptanweisung, um ein Programm zu schließen oder Windows neu zu starten.** Verwenden Sie zu diesem Zweck weder Schließen noch Ja/Nein, um Miese zu verhindern.

**Richtig:**

![Screenshot der Schaltfläche "Windows jetzt neu starten"](images/mess-confirm-image28.png)

**Falsch:**

![Screenshot der Schaltfläche "Ja"](images/mess-confirm-image29.png)

Im falschen Beispiel wird Ja verwendet, um Windows neu zu starten.

### <a name="command-links"></a>Befehlslinks

-   **Erwägen Sie für das Präzisierungsmuster die Verwendung von Befehlslinks, um die Alternativen zu verdeutlichen.**

**Annehmbar:**

![Screenshot von "Ein oder alle Vorkommen ändern?" ](images/mess-confirm-image30.png)

**Besser:**

![Screenshot der gleichen Frage mithilfe von Befehlslinks ](images/mess-confirm-image31.png)

Im besseren Beispiel machen Befehlslinks die Alternativen klar.

-   **Zeigen Sie zuerst die am häufigsten verwendeten Befehlslinks an.** Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung entsprechen, aber auch einen logischen Ablauf aufweisen.
-   Wenn ein Befehlslink eine weitere Erläuterung erfordert, **geben Sie eine ergänzende Erklärung an.** Ergänzende Erklärungen beschreiben, warum Benutzer die Option auswählen möchten oder was geschieht, wenn die Option ausgewählt wird.

Weitere Richtlinien und Beispiele finden Sie unter [Befehlslinks.](ctrl-command-links.md)

### <a name="default-values"></a>Standardwerte

-   **Die Standardantwort für eine Bestätigung basiert auf ihrem Entwurfsmuster:**



    | Muster                                                 | Standardantwort                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Routinemäßige Bestätigungen <br/>                | Fortfahren. <br/>                                                            |
    | Bestätigungen riskanter Aktionen <br/>           | Fahren Sie nicht fort (oder die sichere Wahl). <br/>                                 |
    | Bestätigungen unbeabsichtigter Folgen <br/> | Wenn die Folgen signifikant sind, fahren Sie nicht fort. Andernfalls fahren Sie fort. <br/> |
    | Erläuterungen <br/>                       | Die wahrscheinlichste Antwort. <br/>                                           |
    | Sicherheitsbestätigungen <br/>               | Fahren Sie nicht fort. <br/>                                                      |
    | Ulterior-Motivationsbestätigungen <br/>        | Fortfahren. <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a>Diese Meldung nicht mehr anzeigen

-   **Verwenden Sie diese Option nur für die Bestätigungsmuster routine und ulterior motivation.** Wenn die Informationen für die anderen Muster erforderlich sind, sollten sie immer angezeigt werden.
-   **Stellen Sie diese Option nicht zur Verfügung, um die Anzeige einer unnötigen Bestätigung zu rechtfertigen.** Lassen Sie stattdessen einfach die Bestätigung los.

**Falsch:**

![Screenshot von "Diese Erinnerungen verweisen?" ](images/mess-confirm-image32.png)

**Immer noch falsch:**

![Screenshot von "Nachricht nicht mehr anzeigen"](images/mess-confirm-image33.png)

In diesen Beispielen wird durch das Hinzufügen der Option Diese Meldung nicht mehr anzeigen keine unnötige Bestätigung behoben.

Weitere Richtlinien finden Sie unter [Dialogfelder](win-dialog-box.md).

### <a name="bulk-operations"></a>Massenvorgänge

-   Für Bestätigungen, die für Massenvorgänge gelten, geben Sie eine Option an, um die Bestätigung auf den gesamten Vorgang anzuwenden.

![Screenshot von "Do this for all items?" Kontrollkästchen ](images/mess-confirm-image34.png)

Dieses Beispiel verfügt über eine Option für Massenvorgänge.

-   Beseitigen oder verschieben Sie Bestätigungen in einem Massenvorgang.

**Falsch:**

![Screenshot des Dialogfelds "Dateilöschung bestätigen" ](images/mess-confirm-image35.png)

In diesem Beispiel bestätigt Windows-Explorer In Windows XP jede schreibgeschützte Datei während einer Massendatei verschieben. Es ist besser, nur die schreibgeschützten Dateien zu kopieren, ohne sie zu fragen, oder die Verarbeitung dieser Dateien zu verschieben und die Bestätigung am Ende der Aufgabe zu präsentieren.

### <a name="progressive-disclosure&quot;></a>Schrittweise Offenlegung

-   **Wenn Sie erweiterte Informationen in eine Bestätigungsmeldung einschlussen müssen, zeigen Sie sie mithilfe von Schaltflächen für die progressive Offenlegung an (z. B. &quot;Details anzeigen").** Dadurch wird die Bestätigung für die typische Verwendung vereinfacht. Blenden Sie die benötigten Informationen nicht aus, da Benutzer sie möglicherweise nicht finden.
-   **Verwenden Sie nur dann "Details anzeigen", wenn es tatsächlich weitere Details gibt.** Erstellen Sie die vorhandenen Informationen nicht einfach in einem anderen Format.

Bezeichnungsrichtlinien finden Sie unter [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).

### <a name="user-account-control"></a>Benutzerkontensteuerung

-   **Verwenden Sie nicht die Benutzeroberfläche für die Benutzerkontensteuerung (User Account Control, UAC) für die Erhöhung der Rechte als Ersatz für eine Bestätigung.** Wenn eine Aktion eine Bestätigung benötigt, verwenden Sie ein separates Dialogfeld. Während der [Benutzeroberfläche für Rechteerweiterungen](winenv-uac.md)müssen sich Benutzer darauf konzentrieren, ob sie die Aufgabe gestartet haben und ob das Programm vertrauenswürdig ist.
-   **Zeigen Sie die Bestätigung vor der Benutzeroberfläche für die Rechteerweiterung an.** Dadurch werden unnötige Erhöhungen vermieden.

## <a name="text"></a>Text

### <a name="general"></a>Allgemein

-   **Entfernen Sie redundanten Text.** Suchen Sie nach redundantem Text in Titeln, Hauptanweisungen, ergänzenden Anweisungen, Inhaltbereichen, Befehlslinks und Commitschaltflächen. Lassen Sie im Allgemeinen vollständigen Text in Anweisungen und interaktiven Steuerelementen, und entfernen Sie alle Redundanzen von den anderen Stellen.
-   **Verwenden Sie im Text nicht "Warnung" oder "Vorsicht".** Wenn Benutzer mit Vorsicht vorgehen müssen, geben Sie dies stattdessen mithilfe eines Warnsymbols an.

**Falsch:**

![Screenshot der Bestätigung der Volumeformatierung ](images/mess-confirm-image36.png)

In diesem Beispiel ist der Begriff "Warnung" nicht erforderlich.

### <a name="titles"></a>Titel

-   **Verwenden Sie den Titel, um den Befehl oder das Feature zu identifizieren, von dem die Bestätigung stammt. Ausnahmen:**
    -   Wenn eine Bestätigung von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.
    -   Wenn dieser Titel redundant oder verwirrend mit der Main-Anweisung wäre, verwenden Sie stattdessen den Programmnamen.

Wenn die Bestätigung jedoch von einer Aufgabe mit langer Ausführungs ausgeführt wird und gut nach dem Start der Aufgabe angezeigt werden kann, verwenden Sie immer den Befehl oder das Feature, um den Kontext eindeutig zu identifizieren.

-   **Verwenden Sie den Titel nicht, um zu erläutern,** was im Dialog zu tun ist, der der Zweck der Hauptanweisung ist.
-   Wenn dies klarheit schafft, beginnen Sie den Titel mit dem Wort Bestätigen.
-   **Bei Bestätigungen riskanter Aktionen können Sie den Namen des beteiligten Objekts zur zusätzlichen Hervorhebung hinzufügen.**

![Screenshot des Dialogfeldtitels "Format f drive" ](images/mess-confirm-image13.png)

In diesem Beispiel ist das laufwerk, das formatiert werden soll, im Titel enthalten.

-   Verwenden [Sie die Groß-/Groß-/Formatvorlage,](glossary.md)ohne die Interpunktion zu beenden.

### <a name="main-instructions"></a>Hauptanweisungen

-   **Die Hauptanweisung für eine Bestätigung basiert auf ihrem Entwurfsmuster:**



    | Muster                                                 | Main-Anweisung                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Unbeabsichtigte Folgebestätigungen <br/> | gibt die unbeabsichtigte Folge an.<br/> **exception:** Wenn eine Frage, die anfordert, ob der Benutzer fortfahren möchte, die unbeabsichtigte Folge eindeutig impliziert, stellen Sie stattdessen die Frage. <br/> ![Screenshot von "Alle Registerkarten schließen?" Bestätigung ](images/mess-confirm-image15.png)<br/> In diesem Beispiel zeigt die Frage des Benutzers, dass er den Vorgang ausreichend fortgesetzt hat, die Konsequenzen der Aktion.<br/> |
    | Alle anderen <br/>                           | Stellen Sie eine einzelne Frage, um zu bestimmen, ob der Benutzer fortfahren möchte. <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   **Seien Sie präzise, verwenden Sie nur einen einzelnen vollständigen Satz.** Entfernt die Hauptanweisung auf die grundlegenden Informationen. Wenn Sie mehr erklären müssen, verwenden Sie eine zusätzliche Anweisung.
-   **Seien Sie spezifisch, wenn Objekte beteiligt sind, geben Sie ihre vollständigen Namen an.**
-   **Verwenden Sie positive Formulierungen.** Positive Formulierungen sind für Benutzer einfacher zu verstehen.

**Richtig:**

Möchten Sie die Datei- und Druckerfreigabe aktivieren?

**Falsch:**

Möchten Sie die Datei- und Druckerfreigabe deaktivieren?

Der Ausdruck muss jedoch mit dem zugeordneten Befehl übereinstimmen, auch wenn der Befehl negativ formuliert ist. verwenden Sie z. B. disable, um einen Disable-Befehl zu bestätigen.

-   Es gibt zwar keine strengen Regeln für den Ausdruck, aber diese **häufigen Bestätigungsaussätze haben die angegebene Konnotation:**



    | Ausdruck                                                            | Konnotation                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | Sind Sie sicher, dass Sie \[ eine Aktion ausführen \] möchten? <br/> | Bestätigen des direkten Ergebnisses einer Benutzeranforderung. <br/> |
    | Möchten Sie eine \[ Aktion \] ausführen? <br/>           | Bestätigen eines Nebeneffekts einer Benutzeranforderung. <br/>     |
    | Möchten Sie ein \[ Ergebnis \] auswählen? <br/>          | Es ist eine Erläuterung notwendig. <br/>                           |
    | \[Ausführen einer \] Aktion? <br/>                          | Keine Konnotation. <br/>                                 |



 

-   Verwenden Sie für Bestätigungen riskanter Aktionen dauerhaft den Begriff , um anzugeben, dass eine Aktion nicht rückgängig gemacht werden kann.

![Screenshot der Bestätigung des dauerhaften Löschens ](images/mess-confirm-image37.png)

In diesem Beispiel gibt "permanent" an, dass die Aktion nicht rückgängig gemacht werden kann.

-   Verwenden Sie [die Groß-/Groß-/Groß-](glossary.md)

### <a name="supplemental-instructions"></a>Zusätzliche Anweisungen

-   **Die ergänzende Anweisung für eine Bestätigung basiert auf ihrem Entwurfsmuster:**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Muster</strong><br/></td>
    <td><strong>Ergänzende Anweisung</strong><br/></td>
    </tr>
    <tr class="even">
    <td>Unbeabsichtigte Folgebestätigungen <br/></td>
    <td>Stellen Sie eine einzelne Frage, um zu bestimmen, ob der Benutzer fortfahren möchte. <br/></td>
    </tr>
    <tr class="odd">
    <td>Alle anderen <br/></td>
    <td>Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte. Zu diesen Gründen gehören: <br/>
    <ul>
    <li>Potenzieller Verlust einer oder mehrerer der folgenden Punkte: <ul>
    <li>Eine wertvolle Ressource, z. B. Datenverlust oder finanzieller Verlust.</li>
    <li>Systemzugriff oder -integrität.</li>
    <li>Datenschutz oder Kontrolle über vertrauliche Informationen.</li>
    </ul></li>
    <li>Aktionen, die nicht rückgängig gemacht werden können.</li>
    </ul></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Wiederholen Sie die Hauptanweisung nicht mit leicht abweichenden Formulierungen.** Lassen Sie stattdessen die zusätzliche Anweisung aus, wenn nicht mehr hinzugefügt werden muss.
-   Ziehen Sie für **unbeabsichtigte Bestätigungen von Folgen in Betracht, den Begriff trotzdem zu verwenden, um präzise anzugeben, dass es einen Grund gibt, nicht fortzufahren,** falls der Benutzer die Hauptanweisung übersehen hat. Weitere Informationen finden Sie unter Entwurfskonzepte.
-   Verwenden Sie vollständige Sätze, Groß- und Großschreibung im Satzstil und endende Interpunktion.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Bestätigungen:

-   Verweisen Sie auf eine Bestätigung anhand des Titels, wenn der Titel spezifisch für die Bestätigung ist (d. b. nicht der Programmname). Andernfalls verweisen Sie über die Hauptanweisung darauf.
-   Bei Bedarf können Sie auf ein Bestätigungsdialogfeld als Meldung verweisen.
-   Verwenden Sie den genauen Text, einschließlich der Groß-/Großschreibung.
-   Formatieren Sie den Text nach Möglichkeit fett. Andernfalls setzen Sie den Text nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiel: Klicken Sie in der Meldung **Datei kopieren** auf die neuere Datei.


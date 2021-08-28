---
title: Bestätigungen
description: Eine Bestätigung ist ein modales Dialogfeld, in dem gefragt wird, ob der Benutzer mit einer Aktion fortfahren möchte.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: cbfe45319051e79bcbcf57486c99f12e38ab6658
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474446"
---
# <a name="confirmations"></a>Bestätigungen

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine Bestätigung ist ein modales Dialogfeld, in dem gefragt wird, ob der Benutzer mit einer Aktion fortfahren möchte.

![Screenshot: Editor "Möchten Sie Änderungen speichern?" .](images/mess-confirm-image1.png)

Eine typische Bestätigung.

Bestätigungen weisen diese wesentlichen Merkmale auf:

-   Sie werden als direktes Ergebnis einer vom Benutzer initiierten Aktion angezeigt.
-   Sie überprüfen, ob der Benutzer mit der Aktion fortfahren möchte.
-   Sie bestehen aus einer einfachen Frage und zwei oder mehr Antworten.

Bestätigungen sind besonders nützlich, wenn der Benutzer für die Aktion eine relevante und eindeutige Auswahl treffen muss, die später nicht getroffen werden kann. Diese Auswahl beinhaltet häufig ein Gewisses an Risiko, das für den Benutzer nicht offensichtlich ist, aber das Risiko ist für Bestätigungen nicht entscheidend. Diese Elemente sind erforderlich, um die Unterbrechung der Reaktion auf einen modalen Dialog zu rechtfertigen.

Im Gegensatz dazu stellen [Warnmeldungen](mess-warn.md) eine Bedingung dar, die in Zukunft ein Problem verursachen kann. Ihr grundlegendes Merkmal ist, dass sie Risiken mit sich bringen:

-   Sie umfassen den möglichen Verlust einer oder mehrerer der folgenden Punkte:
    -   Eine wertvolle Ressource, z. B. Datenverlust oder finanzieller Verlust.
    -   Systemzugriff oder -integrität.
    -   Datenschutz oder Kontrolle über vertrauliche Informationen.
    -   Die Zeit des Benutzers (ein erheblicher Betrag, z. B. 30 Sekunden oder mehr).
-   Sie haben unerwartete oder unbeabsichtigte Folgen.
-   Sie erfordern jetzt eine korrekte Behandlung, da Fehler nicht einfach behoben werden können und sogar nicht rückgängig gemacht werden können.

Wenn eine Bestätigung ein Risiko mit sich bringt, kann sie auch als Warnung betrachtet werden. Daher gelten auch die Richtlinien für Warnmeldungen.

**Hinweis:** Richtlinien im Zusammenhang mit [Dialogfeldern,](win-dialog-box.md) [Fehlermeldungen,](mess-error.md) [Layout](vis-layout.md)und [Warnmeldungen](mess-warn.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Wird dem Benutzer eine Frage gestellt, um mit einer Aktion fortzufahren, die über zwei oder mehr Antworten verfügt?** Falls nicht, ist die Nachricht keine Bestätigung.
-   **Stellt die Benutzeroberfläche einen Fehler oder ein Problem dar, das aufgetreten ist?** Verwenden Sie in diesem Falle stattdessen eine [Fehlermeldung.](mess-error.md)
-   **Erfordert das Fortfahren mit der Aktion, dass der Benutzer eine Auswahl treffen muss, die nicht über einen geeigneten Standardwert verfügt?** In diesem Falle kann eine Bestätigung angemessen sein.
-   **Gibt es einen alternativen Entwurf, der die Notwendigkeit der Bestätigung entfällt?** Die Notwendigkeit einer Bestätigung deutet manchmal auf einen Entwurfsfehler hin. Häufig gibt es eine bessere Entwurfsalternative, für die keine Bestätigung erforderlich ist.
-   **Führt der Benutzer eine riskante Aktion aus?** In diesem Falle ist eine Bestätigung geeignet, wenn die Aktion erhebliche Konsequenzen hat oder nicht einfach rückgängig zu werden ist.
-   **Wird der Benutzer eine Aufgabe verwerfen?** Wenn ja, bestätigen Sie dies nicht. Gehen Sie davon aus, dass Benutzer die Konsequenzen verstehen, die sich daraus ergeben, dass eine Aufgabe nicht abgeschlossen wird.
-   **Hat die Aktion Konsequenzen, die Benutzer möglicherweise nicht kennen?** In diesem Falle kann eine Bestätigung angemessen sein.
-   **Führen Benutzer aufgrund des aktuellen Kontexts wahrscheinlich eine fehlerhafte Aktion aus?** In diesem Falle kann eine Bestätigung angemessen sein.
-   **Führen Benutzer die Aktion häufig aus?** Ziehen Sie in diesem Falle einen alternativen Entwurf in Betracht. Häufige Bestätigungen sind ängstlich und haben wenig Nutzen, da Benutzer lernen, ohne Zudenkungen zu reagieren.
-   **Hat die Aktion Auswirkungen auf die Sicherheit?** In diesem Falle ist möglicherweise auch dann eine Bestätigung erforderlich, wenn in den vorherigen Tests etwas anderes angegeben ist.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="unnecessary-confirmations-are-annoying"></a>Unnötige Bestätigungen sind ungern

Die erste Windows Bestätigung, die jemals erstellt wurde, sieht wie folgt aus:

![Screenshot von "Are you sure?" Bestätigung ](images/mess-confirm-image2.png)

Die ursprüngliche bestätigung.

Dies war ein sehr schlechter Start. Wenn Sie möchten, dass Benutzer Ihr Programm hassen, sollten Sie einfach Bestätigungen wie diese durchgehen lassen. Um zu verstehen, warum, berücksichtigen Sie den Standpunkt des Benutzers. Der Benutzer hat lediglich aufgefordert, eine Aktion gemäß der Definition einer Bestätigung auszuführen, es sei denn, etwas wurde versehentlich angeklickt oder gedrückt, natürlich möchte der Benutzer fortfahren.

Nicht nur unnötige Bestätigungen sind ungern, sie sind auch nicht effektiv, um den Benutzer vor Fehlern zu schützen. Benutzer erkennen schnell, wenn ein Programm unnötige Bestätigungen hat und ihre natürliche Reaktion darin besteht, sie so schnell wie möglich zu verwerfen, oft ohne Lesen. Folglich sind solche Bestätigungen nicht viel mehr als einen zusätzlichen Schritt zu diesen Aufgaben hinzuzufügen.

Verwenden Sie keine Bestätigungen, nur weil es die Möglichkeit gibt, dass Benutzer einen Fehler machen. **Stattdessen sind Bestätigungen am effektivsten, wenn sie verwendet werden, um Aktionen zu bestätigen, die erhebliche oder unbeabsichtigte Folgen haben.** Gute Bestätigungen geben nie das Offensichtliche an. Sie sollten etwas kommunizieren, das Benutzer aus einem guten Grund kennen müssen, um nicht fortzufahren. Und sie werden nur verwendet, wenn sie wirklich von einer Aktion benötigt werden, z. B. wenn Benutzer aufgefordert werden, Änderungen nur dann zu speichern, wenn Änderungen gespeichert werden sollten. Dies erfordert die Aufmerksamkeit des Benutzers nur, wenn dies wirklich gerechtfertigt ist.

Für andere Arten von Bestätigungen gibt es häufig eine bessere Entwurfsalternative als das Erzwingen der Beantwortung einer Frage durch die Benutzer.

### <a name="consider-the-design-alternatives"></a>Berücksichtigen der Entwurfsalternativen

Hier sind einige Entwurfsalternativen, die routinemäßige Bestätigungen überflüssig machen:

-   **Verhindern sie Fehler.** Entwerfen Sie Aufgaben so, dass schwerwiegende Fehler versehentlich schwer zu machen sind. Trennen Sie beispielsweise destruktive Befehle physisch von anderen Befehlen, und müssen mehrere Aktionen abgeschlossen werden.
-   **Geben Sie rückgängig an.** Bieten Sie die Möglichkeit, Aktionen rückgängig zu machen. Das Löschen einer Datei in Microsoft Windows erfordert in der Regel keine Bestätigung, da gelöschte Dateien aus dem Papierkorb wiederhergestellt werden können. Beachten Sie Folgendes: Wenn eine Aktion sehr einfach auszuführen ist, reicht es möglicherweise aus, wenn Benutzer die Aktion wiederholen.
-   **Geben Sie Feedback.** Machen Sie unerwünschte Ergebnisse offensichtlich. Die Bereitstellung von Rückgängig machen allein reicht nicht aus, wenn Benutzer nicht erkennen, wann sie einen Fehler machen. Beispielsweise sollte die Auswirkung der direkten Bearbeitung (z. B. ein Drag & Drop-Vorgang) immer offensichtlich sein.
-   **Nehmen Sie das wahrscheinliche Ergebnis an, aber erleichtern Sie es, sich zu ändern.** Wenn Sie nicht sicher sind, was Benutzer wünschen, aber es eine wahrscheinliche, sichere und sichere Auswahl gibt, gehen Sie von dieser Auswahl aus, machen Sie klar, was passiert ist, und vereinfachen Sie die Änderung mithilfe eines Kontextmenüs. Beispielsweise geht Microsoft Word davon aus, dass Benutzer Wörter richtig schreiben möchten. Wenn ein falsch geschriebenes Wort erkannt wird und die wahrscheinlich richtige Schreibweise bekannt ist, führt Word automatisch die Korrektur durch, ermöglicht benutzern jedoch das Zurücksetzen.
-   **Entfernen Sie die Auswahl vollständig.** Wenn die Auswahl nicht wichtig ist, ist es den Benutzern einfach egal. Es ist besser, ihr Programm zu [vereinfachen](/previous-versions//dn742474(v=vs.85)) und die Auswahl zu vermeiden.

### <a name="make-confirmations-require-thought"></a>Machen Sie Sichten für Bestätigungen erforderlich.

Damit eine Bestätigung über einen Wert verfügen kann, müssen Benutzer den Grund verstehen, warum sie nicht fortfahren möchten. Manchmal ist der Grund offensichtlich, z. B. wenn Benutzer ein Dokument mit Änderungen schließen, die nicht gespeichert wurden:

![Screenshot: Paint "Möchten Sie Änderungen speichern?" ausgegeben wird.](images/mess-confirm-image3.png)

In diesem Beispiel ist der Grund für die Bestätigung offensichtlich.

In anderen Situationen ist der Grund möglicherweise nicht so offensichtlich.

Beim Auswählen von Commitschaltflächenbezeichnungen für Dialogfelder besteht die [allgemeine Richtlinie](win-dialog-box.md) darin, Bezeichnungen auszuwählen, die bestimmte Antworten auf die Hauptanweisung sind. Dies führt zu einer effizienten Entscheidungsfindung, da Benutzer eine Mindestmenge an Text lesen müssen, um fortfahren zu können. Dieses Effizienzziel kann jedoch für Bestätigungen kontraproduktiv sein. Sehen Sie sich dieses Beispiel an:

**Falsch:**

![Screenshot der Bestätigung mit der Schaltfläche "Deinstallieren" ](images/mess-confirm-image4.png)

In diesem Beispiel muss die richtige Antwort bedacht werden.

Wenn Sie diese Bestätigung sofort nach dem Ausführen des Deinstallationsbefehls durch den Benutzer präsentieren, lautet die Antwort des Benutzers wahrscheinlich "Natürlich möchte ich deinstallieren!" Der Benutzer klickt auf Deinstallieren, ohne einen zweiten Gedanken zu machen.

Für Bestätigungen sollen Benutzer keine übereilten, emotionalen Entscheidungen treffen. Um Benutzer dazu zu ermutigen, über ihre Reaktion nachzudenken, müssen wir eine kleine Geschwindigkeit bei der Entscheidungsfindung bereitstellen. In der Praxis ist es in der Regel besser, dies durch sorgfältiges Ausdrucken von Commitschaltflächen zu erreichen. Beispielsweise können wir eine zusätzliche Sprache verwenden, um anzugeben, dass es einen Grund gibt, nicht fortzufahren.

**Besser:**

![Screenshot der Schaltfläche "Deinstallieren trotzdem" ](images/mess-confirm-image5.png)

In diesem Beispiel wird "anyway" der Commit-Schaltflächenbezeichnung hinzugefügt, um anzugeben, dass die Bestätigung einen Grund dafür gibt, nicht fortzufahren.

Wenn dieser Ansatz nicht praktikabel ist, können wir Ja/Nein-Commitschaltflächen verwenden.

**Außerdem besser:**

![Screenshot der Bestätigung mit Ja/Nein-Schaltflächen ](images/mess-confirm-image6.png)

In diesem Beispiel werden Benutzer durch Die Verwendung von Ja/Nein-Commitschaltflächen gezwungen, zumindest die Hauptanweisung zu lesen.

### <a name="provide-all-the-information"></a>Geben Sie alle Informationen an.

Wenn Sie eine Frage stellen möchten, müssen Sie ausreichend Informationen bereitstellen, damit Benutzer diese Frage intelligent beantworten können. Betrachten Sie das Dialogfeld Dateiersetzung bestätigen aus Windows XP:

![Screenshot des Dialogfelds "Dateiersetzung bestätigen" ](images/mess-confirm-image7.png)

Das Dialogfeld "Dateiersetzung bestätigen" Windows XP.

Enthält diese Bestätigung alle Informationen, die Benutzer möglicherweise benötigen, um die Frage zu beantworten? Bevor Sie antworten, sollten Sie die gängigsten Benutzerszenarien berücksichtigen:

-   Kopieren (oder verschieben) Sie die andere Datei, und ersetzen Sie dabei die vorhandene Datei.
-   Behalten Sie die vorhandene Datei bei, ohne die andere Datei zu kopieren oder zu verschieben.
-   Speichern oder kopieren Sie die neuere Datei (top-Szenario).
-   Behalten Sie entweder die vorhandene Datei bei, oder kopieren Sie die andere Datei, je nach Kriterien wie Dateiinhalt und Größe.
-   Behalten Sie die vorhandene Datei bei, und kopieren Sie die andere Datei mit einem anderen Namen.
-   Brechen Sie den Vorgang ab, wenn etwas falsch oder unerwartet ist.

Benutzer können Szenario 1 erreichen, indem sie auf Ja und Szenario 2 klicken, indem sie auf Nein klicken. Sie können Szenario 3 erreichen, indem sie die Dateidaten vergleichen und auf die entsprechende Schaltfläche klicken. Beachten Sie jedoch, wie viel Sie für die Ermittlung der neueren Datei und dann für das wahrscheinlich gängigste Szenario benötigt, um die entsprechende Schaltfläche zu bestimmen.

Die Szenarien 4, 5 und 6 sind ebenfalls überraschend schwierig. Die Dateigrößen werden aufgerundet, sodass z. B. nicht bestimmt werden kann, ob diese Dateien die gleiche Größe haben oder ob sie dieselbe Datei sind. Die Symbole sind für die Anwendung vorgesehen, die zum Öffnen der Datei verwendet wird, sodass Benutzer die Dateien öffnen müssen, um ihren Inhalt zu überprüfen und zu vergleichen. Miniaturansichten des Dateiinhalts wären bei der Beantwortung der Frage viel nützlicher.

Die Bestätigung zum Kopieren von Dateien aus Windows Vista führt zu einer viel besseren Verarbeitung dieser Szenarien, indem weitere Informationen zur Verfügung gestellt und die Option zum Beibehalten beider Dateien hinzugefügt wird:

![Screenshot des Dialogfelds "Datei kopieren" ](images/mess-confirm-image8.png)

Die Bestätigung Windows Vista-Kopierdatei.

### <a name="provide-specific-useful-information"></a>Bereitstellen spezifischer, nützlicher Informationen

Wenn Sie eine Frage stellen möchten, stellen Sie sicher, dass die Benutzer die Frage und die Auswirkungen der alternativen Antworten verstehen. Beachten Sie diese Windows Internet Explorer Sicherheitsbestätigung:

![Screenshot der Bestätigung mit einer ungenauen Frage ](images/mess-confirm-image9.png)

Eine ungenaue Sicherheitsbestätigung.

Diese Bestätigung stellt eine Frage, die Benutzer möglicherweise nicht intelligent beantworten können. Der Benutzer hat angefordert, dass Windows Internet Explorer eine Seite anzeigen, und diese Meldung rät implizit durch die Formulierung des Texts und durch Hervorhebung von Nein als Standardauswahl davon ab.

Das spezifische Sicherheitsproblem, das die Seite darstellt, wird nicht ausreichend erläutert, sodass das Risiko, fortzufahren, nicht klar ist. Welche Informationen in der Bestätigung würden dazu führen, dass der Benutzer jemals auf Nein klickt? Aufgrund der Ungenaukeit der Nachricht wird die Bestätigung die Benutzer wahrscheinlich nicht davon abraten, den Vorgang fortzusetzen, aber sie werden sich schlecht darüber informieren.

Damit diese Bestätigung nützlich ist, muss sie weitere informationenspezifische Informationen bereitstellen, die dazu führen können, dass der Benutzer entscheidet, nicht fortzufahren. Im Allgemeinen sollten Sie für jede Antwort in einer Bestätigung die Szenarien berücksichtigen, für die sie erforderlich ist, und sicherstellen, dass genügend Informationen bereitgestellt werden, damit Benutzer sie auswählen können. Bereitstellen von Optionen, nicht von Ile.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Bestimmen, ob eine Bestätigung erforderlich ist

Das Durchdenken der Szenarien und die Wahrscheinlichkeit, dass jede Antwort ausgewählt wird, schlägt eine systematische Methode vor, um zu bestimmen, ob eine Bestätigung erforderlich ist. Wenn Benutzer wahrscheinlich alle Antworten auswählen, ist die Bestätigung erforderlich und nützlich. Wenn jedoch nur eine Antwort wahrscheinlich ist (z. B. 98 Prozent der Zeit), ist die Bestätigung eindeutig unnötig und sollte entfernt werden. Beachten Sie, dass Bestätigungen im Zusammenhang mit Sicherheits-, rechtlichen und Sicherheitsproblemen mögliche Ausnahmen sind.

![Screenshot von "Möchten Sie Einstellungen ändern?" ](images/mess-confirm-image10.png)

Ist diese Bestätigung erforderlich? Wählen Benutzer jemals Nein aus? Dies ist möglich, aber sehr unwahrscheinlich. Diese Bestätigung sollte entfernt werden.

**Wenn Sie nur drei Dinge tun...**

1. Stellen Sie sicher, dass Ihre Bestätigung wirklich erforderlich ist. Es sollte einen legitimen und eindeutigen Grund geben, nicht fortzufahren, und es besteht die Möglichkeit, dass Benutzer dies manchmal nicht machen.

2. Wenn der Grund für die Bestätigung nicht sofort offensichtlich ist, wählen Sie Commitschaltflächen aus, die Benutzer dazu ermutigen, über ihre Antwort nachzudenken. In der Regel erfolgt dies, indem die Bestätigung als Ja- oder Nein-Frage und vollständig selbsterklärende oder Ja/Nein-Antworten formulieren werden.

3. Berücksichtigen Sie alle Szenarien, und stellen Sie die Informationen bereit, die erforderlich sind, um die Frage intelligent zu beantworten.

## <a name="usage-patterns"></a>Verwendungsmuster

Bestätigungen weisen mehrere Verwendungsmuster auf:



|   Verwendung                                                                                                                                                                    |    Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Routinemäßige Bestätigungen**<br/> Bestätigen Sie, dass der Benutzer mit einer routinemäßigen Aktion mit geringem Risiko fortfahren möchte. <br/>                                              | Diese Bestätigungen werden in der Regel als "Sind Sie sicher...?" bezeichnet. und verfügen häufig über ein Kontrollkästchen diese Meldung nicht mehr anzeigen, um deren Empfindlichkeit zu minimieren. <br/> ![Screenshot von "Ordner in Papierkorb verschieben?" ](images/mess-confirm-image11.png)<br/> ![Screenshot von "Meldung nicht erneut anzeigen" ](images/mess-confirm-image12.png)<br/> Beispiele für routinemäßige Bestätigungen.<br/> **Hinweis:** Dieses Muster ist in der Regel unnötig und sollte vermieden werden.<br/>                                                                                                                                                                                                                                                                                        |
| **Bestätigungen riskanter Aktionen**<br/> vergewissern Sie sich, dass der Benutzer mit einer Aktion fortfahren möchte, die ein gewisses Risiko mit sich bringt und nicht einfach rückgängig zu machen ist. <br/>            | Da sie ein Risiko haben, weisen diese Bestätigungen in der Regel ein Warnsymbol auf. <br/> ![Screenshot, der ein Beispiel für die Bestätigung der Volumeformatierung zeigt.](images/mess-confirm-image13.png)<br/> ![Screenshot, der ein Beispiel für die Bestätigung des endgültigen Löschens zeigt.](images/mess-confirm-image14.png)<br/> Beispiele für Bestätigungen riskanter Aktionen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Bestätigungen unbeabsichtigter Folgen**<br/> bestätigen, dass der Benutzer mit einer Aktion fortfahren möchte, die unerwartete oder unbeabsichtigte Folgen hat. <br/> | Zusätzlich zum Stellen einer Frage weisen diese Bestätigungen auf die unbeabsichtigten Folgen hin. da sie unbeabsichtigte Folgen haben, weisen diese Bestätigungen in der Regel ein Warnsymbol auf. <br/> ![Screenshot von "Alle Registerkarten schließen?" Bestätigung ](images/mess-confirm-image15.png)<br/> ![Screenshot von "Installation abbrechen?" Bestätigung ](images/mess-confirm-image16.png)<br/> Beispiele für bestätigungen unbeabsichtigter Folgen.<br/> Dieses Muster erfordert jedoch, dass die Folgen wirklich unbeabsichtigt sind. <br/> **Falsche:**<br/> ![Screenshot von "Schlüsselprotokollierung deaktivieren?" Bestätigung ](images/mess-confirm-image17.png)<br/> Die Folgen sind hier beabsichtigt, daher ist dies eine routinemäßige Bestätigung.<br/> |
| **Erläuterungen**<br/> verdeutlichen, wie der Benutzer mit einer Aktion fortfahren möchte, die potenziell mehrdeutige oder unerwartete Folgen hat. <br/>             | Drag & Drop-Vorgänge können zu Erläuterungen führen, wenn die Auswirkungen des Vorgangs falsch interpretiert werden können. <br/> ![Screenshot von "Nur dieses Vorkommen ändern?"](images/mess-confirm-image18.png)<br/> ![Screenshot von "Immer beim Beenden speichern?" Bestätigung ](images/mess-confirm-image19.png)<br/> Beispiele für Erläuterungen.<br/> **Hinweis:** Dieses Muster sollte vermieden werden, da es besser ist, Aktionen ohne mehrdeutige Folgen zu entwerfen und das wahrscheinlich gewünschte Ergebnis vorauszugehen. <br/>                                                                                                                                                                                                                                     |
| **Sicherheitsbestätigungen**<br/> bestätigen, dass der Benutzer mit einer Aktion mit Sicherheitsrisiken fortfahren möchte. <br/>                                   | ![Screenshot von "Möchten Sie diese Software ausführen?" ](images/mess-confirm-image20.png)<br/> ![Screenshot von "Kennwort speichern?" Bestätigung ](images/mess-confirm-image21.png)<br/> Beispiele für Sicherheitsbestätigungen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Ulterior-Motivationsbestätigungen**<br/> Geben Sie Informationen zu einer Aktion an, aber stellen Sie sie als Bestätigung vor. <br/>                                       | Obwohl diese Dialogfelder als Bestätigungen angezeigt werden, ist ihr eigentliches Ziel die Benutzerbildung oder die Ankündigung von Features. <br/> ![Screen shot of want this toolbar on your taskbar? ](images/mess-confirm-image22.png)<br/> Ein Beispiel für eine Hintergedankern-Motivationsbestätigung.<br/> **Hinweis:** Dieses Muster wird nicht empfohlen, da es in der Regel eine bessere, direktere Alternative gibt. Animationen [sind beispielsweise](vis-animations.md) eine bessere Möglichkeit, die Beziehung zwischen Ursache und Effekt zu zeigen. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie die Bestätigungen zum Speichern von Änderungen nur, wenn wesentliche Änderungen vorgenommen wurden.** Bestätigen Sie keine Änderungen, die nicht direkt vom Benutzer vorgenommen wurden, z. B. automatische Neuformatierung von Dokumenten.

**Falsch:**

![Screenshot, der eine Microsoft Office Outlook "Möchten Sie Änderungen speichern?" zeigt. .](images/mess-confirm-image23.png)

Dieses Beispiel ist falsch, wenn es für eine leere E-Mail oder ein leeres Dokument verwendet wird, die vom Benutzer nicht geändert wurde.

### <a name="icons"></a>Symbole

-   Bestätigungen verwenden keine Titelleistensymbole.
-   **Das Inhaltsbereichssymbol für eine Bestätigung basiert auf seinem Entwurfsmuster:**



    | Muster                                                | Symbol                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Routinemäßige Bestätigungen <br/>                | Kein Symbol. <br/>                                                                                                                         |
    | Bestätigungen riskanter Aktionen <br/>           | Warnsymbol. <br/>                                                                                                                    |
    | Unbeabsichtigte Folgebestätigungen <br/> | Verwenden Sie ein Warnsymbol, wenn ein Risiko besteht, das Featuresymbol, falls verfügbar. andernfalls kein Symbol. <br/>                                          |
    | Erläuterungen <br/>                       | Wenn die Bestätigung ein Dokument umfasst, verwenden Sie die Miniaturansicht des Dokuments. Verwenden Sie andernfalls das Featuresymbol (falls verfügbar) oder kein Symbol. <br/> |
    | Sicherheitsbestätigungen <br/>               | Warnsymbol. <br/>                                                                                                                    |
    | Ulterior-Motivationsbestätigungen <br/>        | Kein Symbol. <br/>                                                                                                                         |



 

-   **Verwenden Sie keine Warnsymbole für routinemäßige Fragen.** Dies steht im Gegengewicht zum ermutigenden [Ton](text-style-tone.md) Windows und sorgt dafür, dass sich die Verwendung Ihres Programms wie eine riskante Aktivität anfühlt. Gehen Sie davon aus, dass Benutzer die Konsequenzen des Abbrechens einer Aufgabe verstehen, bevor sie abgeschlossen ist.

**Falsch:**

![Screenshot von "Möchten Sie das Tutorial beenden?" ](images/mess-confirm-image24.png)

In diesem Beispiel wird ein Warnsymbol verwendet, um eine Routinefrage zu stellen.

### <a name="commit-buttons"></a>Commitschaltflächen

-   **Verwenden Sie spezifische Antworten auf die Main-Anweisung, wenn der Grund für die Bestätigung offensichtlich ist oder selbsterklärend gemacht werden kann.**

![Screenshot von "Möchten Sie Änderungen speichern?" ](images/mess-confirm-image25.png)

In diesem Beispiel ist der Grund für die Bestätigung offensichtlich, daher funktionieren Speichern und Nicht speichern gut.

-   **Verwenden Sie andernfalls die Schaltflächen Ja und Nein für Bestätigungsantworten.** Dies sorgt dafür, dass Benutzer der Bestätigung einige Gedanken machen, bevor sie antworten. Verwenden Sie niemals OK und Abbrechen für Bestätigungen.

**Richtig:**

![Screenshot von "Unterstützungsdateien deinstallieren möchten?" ](images/mess-confirm-image26.png)

In diesem Beispiel erzwingt die Verwendung der Schaltflächen Ja/Nein für Commits, dass Benutzer zumindest die Hauptanweisung lesen müssen.

**Falsch:**

![Screenshot von "Reservierung stornieren?" ](images/mess-confirm-image27.png)

In diesem Beispiel ist die Verwendung von OK/Abbrechen verwirrend.

-   **Um ein Programm zu schließen oder Windows neu zu starten, verwenden Sie bestimmte Antworten auf die main-Anweisung.** Verwenden Sie zu diesem Zweck nicht Schließen oder Ja/Nein, um Unglücken zu vermeiden.

**Richtig:**

![Screenshot der Schaltfläche "Windows jetzt neu starten"](images/mess-confirm-image28.png)

**Falsch:**

![Screenshot der Schaltfläche "Ja"](images/mess-confirm-image29.png)

Im falschen Beispiel wird Ja zum Neustarten von Windows.

### <a name="command-links"></a>Befehlslinks

-   **Für das Erläuterungsmuster sollten Sie Befehlslinks verwenden, um die Alternativen klar zu machen.**

**Annehmbar:**

![Screenshot von "Change one or all occurrences?" ](images/mess-confirm-image30.png)

**Besser:**

![Screenshot der gleichen Frage über Befehlslinks ](images/mess-confirm-image31.png)

Im besseren Beispiel machen Befehlslinks die Alternativen eindeutig.

-   **Stellen Sie zuerst die am häufigsten verwendeten Befehlslinks vor.** Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung folgen, aber auch einen logischen Fluss haben.
-   Wenn ein Befehlslink eine weitere Erläuterung erfordert, **geben Sie eine zusätzliche Erklärung an.** Ergänzende Erläuterungen beschreiben, warum Benutzer die Option auswählen möchten oder was geschieht, wenn die Option ausgewählt wird.

Weitere Richtlinien und Beispiele finden Sie unter [Befehlslinks.](ctrl-command-links.md)

### <a name="default-values"></a>Standardwerte

-   **Die Standardantwort für eine Bestätigung basiert auf dem Entwurfsmuster:**



    | Muster                                                 | Standardantwort                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Routinemäßige Bestätigungen <br/>                | Fortfahren. <br/>                                                            |
    | Bestätigungen riskanter Aktionen <br/>           | Fahren Sie nicht fort (oder die sichere Wahl). <br/>                                 |
    | Unbeabsichtigte Folgebestätigungen <br/> | Wenn die Folgen signifikant sind, fahren Sie nicht fort. Andernfalls fahren Sie fort. <br/> |
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

In diesem Beispiel bestätigt Windows Explorer in Windows XP jede schreibgeschützte Datei während einer Massendatei verschieben. Es ist besser, nur die schreibgeschützten Dateien zu kopieren, ohne sie zu fragen, oder die Verarbeitung dieser Dateien zu verschieben und die Bestätigung am Ende der Aufgabe zu präsentieren.

### <a name="progressive-disclosure&quot;></a>Schrittweise Offenlegung

-   **Wenn Sie erweiterte Informationen in eine Bestätigungsmeldung einschlussen müssen, zeigen Sie sie mithilfe von Schaltflächen für die progressive Offenlegung an (z. B. &quot;Details anzeigen").** Dadurch wird die Bestätigung für die typische Verwendung vereinfacht. Blenden Sie die benötigten Informationen nicht aus, da Benutzer sie möglicherweise nicht finden.
-   **Verwenden Sie nur dann "Details anzeigen", wenn es wirklich weitere Details gibt.** Erstellen Sie die vorhandenen Informationen nicht einfach in einem anderen Format.

Bezeichnungsrichtlinien finden Sie unter [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).

### <a name="user-account-control"></a>Benutzerkontensteuerung

-   **Verwenden Sie nicht die Benutzeroberfläche für die Benutzerkontensteuerung (User Account Control, UAC), um eine Bestätigung zu erhalten.** Wenn eine Aktion eine Bestätigung benötigt, verwenden Sie ein separates Dialogfeld. Während der [Benutzeroberfläche für Rechteerweiterungen](winenv-uac.md)müssen sich Benutzer darauf konzentrieren, ob sie die Aufgabe gestartet haben und ob das Programm vertrauenswürdig ist.
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

-   Obwohl es keine strengen Regeln für den Ausdruck gibt, haben diese **häufigen Bestätigungsaussätze die angegebene Konnotation:**



    | Satz                                                            | Konnotation                                                            |
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

    
| | | <strong>Muster</strong><br /> | <strong>Ergänzende Anweisung</strong><br /> | | Unbeabsichtigte Folgebestätigungen <br /> | Stellen Sie eine einzelne Frage, um zu bestimmen, ob der Benutzer fortfahren möchte. <br /> | | Alle anderen <br /> | Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte. Zu diesen Gründen gehören: <br /><ul><li>Potenzieller Verlust einer oder mehrere der folgenden Punkte:    <ul><li>Eine wertvolle Ressource, z. B. Datenverlust oder finanzieller Verlust.</li><li>Systemzugriff oder -integrität.</li><li>Datenschutz oder Kontrolle über vertrauliche Informationen.</li></ul></li><li>Aktionen, die nicht rückgängig gemacht werden können.</li></ul> | 


    

     

-   **Wiederholen Sie die Hauptanweisung nicht mit etwas anderen Formulierungen.** Lassen Sie stattdessen die zusätzliche Anweisung weg, wenn nicht mehr hinzugefügt werden muss.
-   **Ziehen Sie bei unbeabsichtigten** Folgebestätigungen in Betracht, den Begriff trotzdem zu verwenden, um präzise anzugeben, dass es einen Grund gibt, nicht fortzufahren, falls der Benutzer die Hauptanweisung übersehen hat. Weitere Informationen finden Sie unter Entwurfskonzepte.
-   Verwenden Sie vollständige Sätze, Groß- und Groß-/Endzeichen im Satzstil.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Bestätigungen:

-   Lesen Sie eine Bestätigung durch den Titel, wenn der Titel für die Bestätigung spezifisch ist (d. h. nicht den Programmnamen). andernfalls verweisen Sie mit der main-Anweisung darauf.
-   Bei Bedarf können Sie ein Bestätigungsdialogfeld als Meldung verwenden.
-   Verwenden Sie den genauen Text, einschließlich der Groß- und Groß-/A-
-   Formatieren Sie den Text nach Möglichkeit fett. Andernfalls setzen Sie den Text nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiel: Klicken Sie in **der Meldung Datei** kopieren auf die neuere Datei.


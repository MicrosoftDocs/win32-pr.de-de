---
title: Bestätigungen
description: Eine Bestätigung ist ein modales Dialogfeld, in dem Sie gefragt werden, ob der Benutzer eine Aktion fortsetzen möchte.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b979987daa4cf2c40308a0cda9c23b08b73f4795
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104559820"
---
# <a name="confirmations"></a>Bestätigungen

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Eine Bestätigung ist ein modales Dialogfeld, in dem Sie gefragt werden, ob der Benutzer eine Aktion fortsetzen möchte.

![Screenshot mit einem Notepad "möchten Sie die Änderungen speichern?" .](images/mess-confirm-image1.png)

Eine typische Bestätigung.

Bestätigungen haben folgende wesentliche Merkmale:

-   Sie werden als direktes Ergebnis einer vom Benutzer initiierten Aktion angezeigt.
-   Sie überprüfen, ob der Benutzer mit der Aktion fortfahren möchte.
-   Sie bestehen aus einer einfachen Frage und zwei oder mehr Antworten.

Bestätigungen sind besonders nützlich, wenn der Benutzer für die Aktion eine relevante und unterschiedliche Auswahl treffen muss, die später nicht getroffen werden kann. Diese Auswahl umfasst oft ein gewisses Risiko, das für den Benutzer nicht offensichtlich ist, aber das Risiko ist für Bestätigungen nicht entscheidend. Diese Elemente sind erforderlich, um die Unterbrechung der Reaktion auf ein modales Dialogfeld zu rechtfertigen.

Im Gegensatz dazu stellen [Warnmeldungen](mess-warn.md) eine Bedingung dar, die in der Zukunft ein Problem verursachen kann. Ihre grundlegende Besonderheit besteht darin, dass Sie Risiken beinhalten:

-   Sie beinhalten mögliche Verluste von einem oder mehreren der folgenden:
    -   Ein wertvolles Asset, z. b. Datenverlust oder finanzieller Verlust.
    -   System Zugriff oder-Integrität.
    -   Datenschutz oder Kontrolle über vertrauliche Informationen.
    -   Benutzer Zeit (eine beträchtliche Menge, z. b. 30 Sekunden oder mehr).
-   Sie haben unerwartete oder unbeabsichtigte Konsequenzen.
-   Sie benötigen jetzt eine korrekte Behandlung, da Fehler nicht einfach behoben werden können und möglicherweise sogar nicht rückgängig gemacht werden.

Wenn eine Bestätigung Risiken umfasst, kann dies auch als Warnung angesehen werden. Folglich gelten auch die Richtlinien für Warnmeldungen.

**Hinweis:** Richtlinien, die sich auf [Dialogfelder](win-dialog-box.md), [Fehlermeldungen](mess-error.md), [Layout](vis-layout.md)und [Warnmeldungen](mess-warn.md) beziehen, werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Wird der Benutzer zu einer Frage aufgefordert, um mit einer Aktion fortzufahren, die zwei oder mehr Antworten hat?** Andernfalls ist die Nachricht keine Bestätigung.
-   **Stellt die Benutzeroberfläche einen Fehler oder ein Problem dar, das aufgetreten ist?** Wenn dies der Fall ist, verwenden Sie stattdessen eine [Fehlermeldung](mess-error.md) .
-   **Erfordert das Fortsetzen der Aktion, dass der Benutzer eine Auswahl treffen muss, die keinen geeigneten Standard hat?** Wenn dies der Fall ist, ist möglicherweise eine Bestätigung angebracht.
-   **Gibt es einen alternativen Entwurf, der die Notwendigkeit der Bestätigung entfällt?** Der Bedarf an einer Bestätigung deutet manchmal auf einen Entwurfs Fehler hin. Häufig gibt es eine bessere Entwurfs Alternative, die keine Bestätigung benötigt.
-   **Ist der Benutzer im Begriff, eine riskante Aktion auszuführen?** Wenn dies der Fall ist, ist eine Bestätigung geeignet, wenn die Aktion bedeutende Konsequenzen hat oder nicht einfach rückgängig gemacht werden kann.
-   **Soll der Benutzer eine Aufgabe abbrechen?** Wenn dies der Fall ist, nicht bestätigen. Angenommen, die Benutzer verstehen die Konsequenzen, die das nicht abschließen einer Aufgabe hat.
-   **Hat die Aktion Konsequenzen, die Benutzer möglicherweise nicht kennen?** Wenn dies der Fall ist, ist möglicherweise eine Bestätigung angebracht.
-   **Gibt es bei dem aktuellen Kontext wahrscheinlich, dass Benutzer eine Aktion als fehlerhaft ausführen?** Wenn dies der Fall ist, ist möglicherweise eine Bestätigung angebracht.
-   **Können Benutzer die Aktion häufig ausführen?** Wenn dies der Fall ist, sollten Sie ein alternatives Design beachten Häufige Bestätigungen sind lästig und haben nur wenig Wert, da Benutzer lernen, ohne Gedanken zu reagieren.
-   **Hat die Aktion Auswirkungen auf die Sicherheit?** Wenn dies der Fall ist, ist möglicherweise eine Bestätigung erforderlich, auch wenn die vorherigen Tests auf andere Weise angeben.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="unnecessary-confirmations-are-annoying"></a>Unnötige Bestätigungen sind lästig

Die erste zuvor erstellte Windows-Bestätigung sieht zweifellos wie folgt aus:

![Screenshot von "sind Sie sicher?" Bestätigung ](images/mess-confirm-image2.png)

Die ursprüngliche lästige Bestätigung.

Dies war ein sehr guter Start. Wenn Sie möchten, dass Benutzer Ihr Programm hassen, sollten Sie einfach nur solche Bestätigungen überspringen. Um dies zu verstehen, sollten Sie die Sicht des Benutzers in Erwägung gezogen. Der Benutzer hat die Ausführung einer Aktion lediglich durch die Definition einer Bestätigung angefordert, sodass der Benutzer natürlich den Vorgang fortsetzen möchte, wenn der Benutzer nicht versehentlich darauf geklickt oder geklickt hat.

Nicht nur sind unnötige Bestätigungen lästig, aber Sie sind nicht wirksam, um den Benutzer vor Fehlern zu schützen. Benutzer können schnell feststellen, wann ein Programm unnötige Bestätigungen hat, und ihre natürliche Reaktion besteht darin, Sie so schnell wie möglich zu verwerfen, oft ohne Lesevorgänge. Folglich führen solche Bestätigungen nur wenig aus, als einen zusätzlichen Schritt zu diesen Aufgaben hinzuzufügen.

Verwenden Sie keine Bestätigungen, weil Benutzer möglicherweise einen Fehler machen. **Stattdessen sind Bestätigungen am effektivsten, wenn Sie zum Bestätigen von Aktionen verwendet werden, die bedeutende oder unbeabsichtigte Folgen haben.** Gute Bestätigungen werden nie offensichtlich. Sie sollten den Benutzern mitteilen, dass Sie einen guten Grund dafür benötigen, den Vorgang fortzusetzen. Diese werden nur verwendet, wenn Sie tatsächlich von einer Aktion benötigt werden, z. b. Wenn Benutzer aufgefordert werden, Änderungen nur dann zu speichern, wenn sich die Änderungen speichern. Dadurch wird die Aufmerksamkeit des Benutzers nur dann gefordert, wenn er wirklich gerechtfertigt ist.

Für andere Arten von Bestätigungen gibt es oftmals eine bessere Entwurfs Alternative als das Erzwingen einer Frage durch Benutzer.

### <a name="consider-the-design-alternatives"></a>Beachten Sie die Entwurfs Alternativen.

Im folgenden finden Sie einige Entwurfs Alternativen, die die Notwendigkeit von Routine Bestätigungen vermeiden:

-   **Verhindern von Fehlern.** Entwerfen Sie Aufgaben so, dass bedeutende Fehler versehentlich schwer zu erledigen sind. Beispielsweise können Sie zerstörerische Befehle physisch von anderen Befehlen trennen und mehrere Aktionen ausführen.
-   **Rückgängigmachen.** Bereitstellen der Möglichkeit zum Zurücksetzen von Aktionen. Beispielsweise ist für das Löschen einer Datei in Microsoft Windows in der Regel keine Bestätigung erforderlich, da gelöschte Dateien aus dem Papierkorb wieder hergestellt werden können. Beachten Sie, dass es möglicherweise ausreichend ist, wenn eine Aktion sehr einfach ausgeführt werden kann.
-   **Geben Sie uns Feedback.** Machen Sie unerwünschte Ergebnisse offensichtlich. Die Bereitstellung allein ist nicht ausreichend, wenn die Benutzer nicht erkennen, wenn Sie einen Fehler machen. Beispielsweise sollte die Auswirkung der direkten Bearbeitung (z. b. eines Drag & Drop-Vorgangs) immer offensichtlich sein.
-   **Nehmen Sie das wahrscheinliche Ergebnis an, machen Sie es jedoch leicht zu ändern.** Wenn Sie nicht sicher sind, was die Benutzer wünschen, aber eine wahrscheinliche, sichere und sichere Wahl ist, nehmen Sie die Auswahl vor, machen Sie fest, was passiert ist, und lassen Sie sich mithilfe eines Kontextmenüs ganz einfach ändern. Microsoft Word geht z. b. davon aus, dass Benutzer Wörter ordnungsgemäß schreiben möchten. Wenn ein falsch geschriebenes Wort erkannt wird und die wahrscheinliche Rechtschreibung bekannt ist, führt Word die Korrektur automatisch durch, aber die Benutzer können Sie wiederherstellen.
-   **Entfernen Sie die Auswahl vollständig.** Wenn die Auswahl nicht wichtig ist, ist es für Benutzer nicht relevant. Besser, um das Programm zu [vereinfachen](/previous-versions//dn742474(v=vs.85)) und die Auswahl zu eliminieren.

### <a name="make-confirmations-require-thought"></a>Bestätigungen müssen als gedacht angesehen werden

Damit eine Bestätigung den Wert hat, müssen die Benutzer verstehen, warum Sie nicht fortfahren müssen. Manchmal ist der Grund offensichtlich, als wenn Benutzer ein Dokument mit nicht gespeicherten Änderungen schließen:

![Screenshot mit der Abbildung "möchten Sie die Änderungen speichern?" ausgegeben wird.](images/mess-confirm-image3.png)

In diesem Beispiel ist der Grund für die Bestätigung offensichtlich.

In anderen Fällen ist der Grund möglicherweise nicht so offensichtlich.

Wenn Sie für Dialogfelder Commit-Schaltflächen Bezeichnungen auswählen, sind die [allgemeinen Richtlinien](win-dialog-box.md) für die Auswahl von Bezeichnungen, bei denen es sich um spezifische Antworten auf die Haupt Anweisung Dies führt zu einer effizienten Entscheidungsfindung, da Benutzer eine minimale Menge an Text lesen müssen, um den Vorgang fortzusetzen. Dieses effizienzziel kann jedoch für Bestätigungen kontraproduktiv sein. Betrachten Sie das folgende Beispiel:

**Falsch:**

![Screenshot der Bestätigung mit der Schaltfläche "deinstallieren" ](images/mess-confirm-image4.png)

In diesem Beispiel ist für die richtige Antwort eine Meinung erforderlich.

Wenn Sie diese Bestätigung sofort nach dem Deinstallations Befehl anzeigen, ist die Antwort des Benutzers wahrscheinlich "natürlich, ich möchte Sie deinstallieren!". Der Benutzer wird auf Deinstallieren klicken, ohne dass ein zweiter Gedanke angezeigt wird.

Für Bestätigungen möchten wir nicht, dass Benutzer über übereilte Entscheidungen treffen. Um Benutzern zu empfehlen, Ihre Antwort zu übernehmen, müssen wir eine kurze Geschwindigkeit bei der Entscheidungsfindung bereitstellen. Wenn dies praktikabel ist, ist es in der Regel besser, die Commit-Schaltflächen sorgfältig zu formulieren. Beispielsweise können wir zusätzliche Sprache verwenden, um anzugeben, dass es keinen Grund gibt, fortzufahren.

**Besserer**

![Screenshot der Schaltfläche "deinstallieren auf der gleichen Seite" ](images/mess-confirm-image5.png)

In diesem Beispiel wird "sowieso" der Bezeichnung für die Commit-Schaltfläche hinzugefügt, um anzugeben, dass die Bestätigung einen Grund für das Fortsetzen des Vorgangs angibt.

Wenn dieser Ansatz nicht praktikabel ist, können wir Ja/Nein-Commit-Schaltflächen verwenden.

**Außerdem besser:**

![Screenshot der Bestätigung mit Ja/Nein-Schaltflächen ](images/mess-confirm-image6.png)

In diesem Beispiel zwingt die Verwendung von Ja/Nein-Commit-Schaltflächen, dass Benutzer mindestens die main-Anweisung lesen.

### <a name="provide-all-the-information"></a>Alle Informationen bereitstellen

Wenn Sie eine Frage stellen möchten, müssen Sie genügend Informationen bereitstellen, damit Benutzer diese Frage Intelligent beantworten können. Sehen Sie sich das Dialogfeld "Datei Ersetzung bestätigen" von Windows XP an

![Screenshot des Dialog Felds "Datei Ersetzung bestätigen" ](images/mess-confirm-image7.png)

Das Dialogfeld "Datei Ersetzung bestätigen" von Windows XP.

Bietet diese Bestätigung alle Informationen, die Benutzer möglicherweise benötigen, um die Frage zu beantworten? Bevor Sie Antworten, berücksichtigen Sie die gängigsten Benutzer Szenarien:

-   Kopieren Sie die andere Datei, oder verschieben Sie Sie, und ersetzen Sie dabei die vorhandene Datei.
-   Behalten Sie die vorhandene Datei bei, ohne die andere Datei zu kopieren oder zu verschieben.
-   Behalten oder kopieren Sie die neuere Datei (Top-Szenario).
-   Behalten Sie entweder die vorhandene Datei bei, oder kopieren Sie die andere Datei, abhängig von den Kriterien wie Dateiinhalt und-Größe.
-   Behalten Sie die vorhandene Datei bei, und kopieren Sie die andere Datei mit einem anderen Namen.
-   Brechen Sie den Vorgang ab, wenn etwas falsch oder unerwartet ist.

Benutzer können Szenario 1 erreichen, indem Sie auf Ja und Szenario 2 klicken, indem Sie auf Nein klicken. Sie können Szenario 3 erzielen, indem Sie die Datei Datumsangaben vergleichen und auf die entsprechende Schaltfläche klicken. Beachten Sie jedoch, wie viel man zum Ermitteln der neueren Datei benötigt und wie Sie dann die entsprechende Schaltfläche ermitteln, insbesondere für das häufigste Szenario.

Die Szenarien 4, 5 und 6 sind ebenfalls überraschend schwierig. Die Dateigrößen werden abgerundet, sodass z. b. nicht bestimmt werden kann, ob diese Dateien dieselbe Größe aufweisen oder auch wenn Sie dieselbe Datei sind. Die Symbole sind für die Anwendung, die zum Öffnen der Datei verwendet wird, sodass Benutzer die Dateien öffnen müssen, um ihren Inhalt zu überprüfen und zu vergleichen. Das vorhanden sein von Miniaturansichten des Datei Inhalts wäre bei der Beantwortung der Frage weitaus nützlicher.

Die Bestätigung zum Kopieren von Dateien aus Windows Vista führt zu einer viel besseren Aufgabe der Verarbeitung dieser Szenarien, indem weitere Informationen bereitgestellt werden und die Option zum Beibehalten beider Dateien hinzugefügt wird:

![Screenshot des Dialog Felds "Datei kopieren" ](images/mess-confirm-image8.png)

Die Bestätigung der Windows Vista-Kopier Datei.

### <a name="provide-specific-useful-information"></a>Bereitstellen spezifischer, nützlicher Informationen

Wenn Sie eine Frage stellen möchten, stellen Sie sicher, dass die Benutzer die Frage und die Auswirkungen der alternativen Antworten verstehen. Beachten Sie diese Windows Internet Explorer-Sicherheits Bestätigung:

![Screenshot der Bestätigung mit einer vagen Frage ](images/mess-confirm-image9.png)

Eine vage Sicherheits Bestätigung.

Diese Bestätigung stellt eine Frage, die Benutzer möglicherweise nicht intelligent beantworten können. Der Benutzer hat angefordert, dass Windows Internet Explorer eine Seite anzeigt, und diese Meldung rät implizit durch den Text Text und durch Hervorheben von No als Standardauswahl ab.

Das Sicherheitsproblem, das die Seite darstellt, wird nicht ausreichend erläutert, sodass das Risiko der Fortsetzung nicht eindeutig ist. Welche Informationen in der Bestätigung bewirken, dass der Benutzer jemals auf Nein klickt? Aufgrund der Unbestimmtheit der Nachricht weist die Bestätigung wahrscheinlich nicht darauf hin, dass die Benutzer den Vorgang fortsetzen, Sie sind jedoch in diesem Fall schlecht.

Damit diese Bestätigung nützlich ist, muss Sie weitere Informationen enthalten, die den Benutzer möglicherweise dazu veranlassen, nicht fortzufahren. Im Allgemeinen sollten Sie für jede Antwort in einer Bestätigung die Szenarien beachten, in denen Sie erforderlich ist, und sicherstellen, dass die Benutzer über ausreichende Informationen verfügen, um Sie auszuwählen. Stellen Sie Optionen und keine dilemmtionen bereit.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Ermitteln, ob eine Bestätigung erforderlich ist

Wenn Sie die Szenarien durchdenken und die Wahrscheinlichkeit, jede Antwort auszuwählen, eine systematische Methode zum Ermitteln der Bestätigung finden. Wenn Benutzer wahrscheinlich alle Antworten auswählen, ist die Bestätigung erforderlich und hilfreich. Wenn jedoch nur eine Antwort wahrscheinlich ist (beispielsweise 98 Prozent der Zeit), ist die Bestätigung eindeutig unnötig und sollte entfernt werden. Beachten Sie, dass die Bestätigungen in Bezug auf Sicherheits-, rechtliche und Sicherheitsprobleme mögliche Ausnahmen sind.

![Screenshot von "möchten Sie Einstellungen ändern?" ](images/mess-confirm-image10.png)

Ist diese Bestätigung erforderlich? Werden Benutzer jemals Nein auswählen? Es ist zwar möglich, aber sehr unwahrscheinlich. Diese Bestätigung sollte entfernt werden.

**Wenn Sie nur drei Dinge tun...**

1. Stellen Sie sicher, dass Ihre Bestätigung wirklich erforderlich ist. Es sollte ein legitimer und eindeutiger Grund sein, nicht fortzufahren und die Wahrscheinlichkeit, dass Benutzer manchmal nicht.

2. Wenn der Grund für die Bestätigung nicht sofort offensichtlich ist, wählen Sie die Schaltflächen "Commit" aus, die Benutzer auffordern, sich über Ihre Antwort Dies erfolgt in der Regel durch formulieren der Bestätigung als Ja oder ohne Frage und Bereitstellung von vollständig selbsterklärenden oder Ja/Nein-antworten.

3. Beachten Sie alle Szenarien, und geben Sie die Informationen an, die zum intelligenten beantworten der Frage erforderlich sind.

## <a name="usage-patterns"></a>Verwendungsmuster

Bestätigungen weisen mehrere Verwendungs Muster auf:



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Routine Bestätigungen**<br/> Vergewissern Sie sich, dass der Benutzer mit einer Routineaktion mit geringem Risiko fortfahren möchte. <br/>                                              | Diese Bestätigungen werden normalerweise formuliert: "sind Sie sicher...?" und lassen Sie das Kontrollkästchen Diese Meldung nicht mehr anzeigen, um ihre Verärgerung zu minimieren. <br/> ![Screenshot von "Ordner in Papierkorb verschieben" ](images/mess-confirm-image11.png)<br/> ![Screenshot von "Meldung nicht mehr anzeigen" ](images/mess-confirm-image12.png)<br/> Beispiele für Routine Bestätigungen.<br/> **Hinweis:** Dieses Muster ist in der Regel unnötig und sollte vermieden werden.<br/>                                                                                                                                                                                                                                                                                        |
| **Bestätigungen von riskanten Aktionen**<br/> Vergewissern Sie sich, dass der Benutzer eine Aktion durchführen möchte, die ein gewisses Risiko aufweist und nicht einfach rückgängig gemacht werden kann. <br/>            | Da Sie Risiken aufweisen, haben diese Bestätigungen normalerweise ein Warnsymbol. <br/> ![Screenshot, der ein Beispiel für eine Bestätigung der volumeformatierung anzeigt.](images/mess-confirm-image13.png)<br/> ![Screenshot, der ein Beispiel für eine permanente Lösch Bestätigung zeigt.](images/mess-confirm-image14.png)<br/> Beispiele für riskante Aktions Bestätigungen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Unbeabsichtigte Folge Bestätigungen**<br/> Vergewissern Sie sich, dass der Benutzer mit einer Aktion fortfahren möchte, die unerwartete oder unbeabsichtigte Folgen hat. <br/> | Zusätzlich zum stellen einer Frage zeigen diese Bestätigungen die unbeabsichtigten Konsequenzen. Da Sie unbeabsichtigte Folgen haben, haben diese Bestätigungen normalerweise ein Warnsymbol. <br/> ![Screenshot von "alle Registerkarten schließen" bestätigt ](images/mess-confirm-image15.png)<br/> ![Screenshot der "Installation abbrechen" bestätigt ](images/mess-confirm-image16.png)<br/> Beispiele für unbeabsichtigte Folge Bestätigungen.<br/> Dieses Muster erfordert jedoch, dass die Folgen wirklich unbeabsichtigt sind. <br/> **Korre**<br/> ![Screenshot "Ausschalten der Schlüsselprotokollierung" bestätigt ](images/mess-confirm-image17.png)<br/> Die Konsequenzen sind hier vorgesehen, daher ist dies eine routinemäßige Bestätigung.<br/> |
| **Erläuterungen**<br/> Erläutern Sie, wie der Benutzer mit einer Aktion fortfahren möchte, die potenziell mehrdeutige oder unerwartete Folgen hat. <br/>             | Drag & amp; Drop-Vorgänge können zu einer Klärung führen, wenn die Auswirkung des Vorgangs falsch interpretiert werden kann. <br/> ![Screenshot von "nur dieses vorkommen ändern?"](images/mess-confirm-image18.png)<br/> ![Screenshot von "immer beim Beenden speichern" bestätigt ](images/mess-confirm-image19.png)<br/> Beispiele für Erläuterungen.<br/> **Hinweis:** Dieses Muster sollte vermieden werden, da es besser ist, Aktionen ohne mehrdeutige folgen zu entwerfen und das wahrscheinlichste gewünschte Ergebnis zu übernehmen. <br/>                                                                                                                                                                                                                                     |
| **Sicherheits Bestätigungen**<br/> Vergewissern Sie sich, dass der Benutzer mit einer Aktion mit Sicherheits Konsequenzen fortfahren möchte. <br/>                                   | ![Screenshot von "möchten Sie diese Software ausführen?" ](images/mess-confirm-image20.png)<br/> ![Screenshot von "Kennwort speichern" Bestätigung ](images/mess-confirm-image21.png)<br/> Beispiele für Sicherheits Bestätigungen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Bestätigung von Ulterior-Motiven**<br/> Geben Sie Informationen zu einer Aktion an, und stellen Sie Sie als Bestätigung dar. <br/>                                       | Diese Dialogfelder werden zwar als Bestätigungen angezeigt, das eigentliche Ziel ist jedoch die Benutzer Bildung oder Ankündigung von Features. <br/> ![Bildschirm Abbildung von möchten Sie diese Symbolleiste auf der Taskleiste? ](images/mess-confirm-image22.png)<br/> Ein Beispiel für eine bestätigungsbestätigung.<br/> **Hinweis:** Dieses Muster wird nicht empfohlen, da es in der Regel eine bessere und direktere Alternative gibt. [Animationen](vis-animations.md) sind z. b. eine bessere Möglichkeit, die Beziehung zwischen Ursache und Effekt anzuzeigen. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Verwenden Sie Bestätigungen für "Änderungen speichern" nur, wenn es bedeutende Änderungen gibt.** Bestätigen Sie keine Änderungen, die nicht direkt vom Benutzer vorgenommen wurden, z. b. automatische Neuformatierung von Dokumenten.

**Falsch:**

![Screenshot mit einem Microsoft Office Outlook "möchten Sie die Änderungen speichern?" .](images/mess-confirm-image23.png)

Dieses Beispiel ist falsch, wenn es für eine leere e-Mail oder ein Dokument verwendet wird, das nicht vom Benutzer geändert wurde.

### <a name="icons"></a>Symbole

-   Bei Bestätigungen werden keine Titelleisten Symbole verwendet.
-   **Das Inhalts Bereichs Symbol für eine Bestätigung basiert auf dem Entwurfsmuster:**



    | Muster                                                | Symbol                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Routine Bestätigungen <br/>                | Kein Symbol. <br/>                                                                                                                         |
    | Bestätigungen von riskanten Aktionen <br/>           | Warnsymbol. <br/>                                                                                                                    |
    | Unbeabsichtigte Folge Bestätigungen <br/> | Verwenden Sie ein Warnsymbol, wenn das Risiko besteht, falls verfügbar. Andernfalls kein Symbol. <br/>                                          |
    | Erläuterungen <br/>                       | Wenn die Bestätigung ein Dokument umfasst, verwenden Sie die Miniaturansicht des Dokuments. Andernfalls verwenden Sie das Feature-Symbol, falls verfügbar, oder kein Symbol. <br/> |
    | Sicherheits Bestätigungen <br/>               | Warnsymbol. <br/>                                                                                                                    |
    | Bestätigung von Ulterior-Motiven <br/>        | Kein Symbol. <br/>                                                                                                                         |



 

-   **Verwenden Sie keine Warn Symbole für Routine Fragen.** Dies ist gegen den ermutigenden [Ton von Fenstern](text-style-tone.md) und macht die Verwendung des Programms wie eine gefährliche Aktivität. Gehen Sie davon aus, dass Benutzer die Konsequenzen der Abbruch einer Aufgabe kennen, bevor Sie beendet wird.

**Falsch:**

![Screenshot von "möchten Sie das Tutorial beenden?" ](images/mess-confirm-image24.png)

In diesem Beispiel wird ein Warnsymbol verwendet, um eine Routine Frage zu stellen.

### <a name="commit-buttons"></a>Commit-Schaltflächen

-   **Verwenden Sie bestimmte Antworten auf die main-Anweisung, wenn der Grund für die Bestätigung offensichtlich ist oder selbsterklärend sein kann.**

![Screenshot von "möchten Sie die Änderungen speichern?" ](images/mess-confirm-image25.png)

In diesem Beispiel ist der Grund für die Bestätigung offensichtlich, also speichern und nicht gut speichern.

-   **Andernfalls verwenden Sie die Schaltflächen Ja und Nein für Bestätigungs Antworten.** Auf diese Weise können Benutzer die Bestätigung vor der Reaktion berücksichtigen. Verwenden Sie für Bestätigungen niemals OK und Abbrechen.

**Richtig:**

![Screenshot von "möchten Sie Unterstützungs Dateien deinstallieren?" ](images/mess-confirm-image26.png)

In diesem Beispiel zwingt die Verwendung von Ja/Nein-Commit-Schaltflächen, dass Benutzer mindestens die main-Anweisung lesen.

**Falsch:**

![Screenshot von "stornieren Ihrer Reservierung" ](images/mess-confirm-image27.png)

In diesem Beispiel ist die Verwendung von OK/Abbrechen verwirrend.

-   **Um ein Programm zu schließen oder Windows neu zu starten, verwenden Sie bestimmte Antworten auf die Haupt Anweisung.** Um Missverständnisse zu vermeiden, verwenden Sie für diesen Zweck nicht Close oder Yes/No.

**Richtig:**

![Screenshot der Schaltfläche "Windows jetzt neu starten"](images/mess-confirm-image28.png)

**Falsch:**

![Screenshot der Schaltfläche "Ja"](images/mess-confirm-image29.png)

Im falschen Beispiel wird ja verwendet, um Windows neu zu starten.

### <a name="command-links"></a>Befehls Verknüpfungen

-   **Verwenden Sie für das übereinstellungsmuster die Verwendung von Befehls Verknüpfungen, um die Alternativen zu löschen.**

**Annehmbar:**

![Screenshot von "Ändern eines oder aller Vorkommen?" ](images/mess-confirm-image30.png)

**Besserer**

![Screenshot der gleichen Frage mithilfe von Befehls Verknüpfungen ](images/mess-confirm-image31.png)

Im besseren Beispiel machen Befehls Verknüpfungen die alternativen eindeutig.

-   **Präsentieren Sie zuerst die am häufigsten verwendeten Befehls Verknüpfungen.** Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung, aber auch eines logischen Flows entsprechen.
-   Wenn für einen Befehls Link eine weitere Erläuterung erforderlich ist, sollten Sie **eine zusätzliche Erläuterung angeben.** Ergänzende Erläuterungen beschreiben, warum Benutzer die Option auswählen können oder was geschieht, wenn die Option ausgewählt wird.

Weitere Richtlinien und Beispiele finden Sie unter [Befehls Verknüpfungen](ctrl-command-links.md).

### <a name="default-values"></a>Standardwerte

-   **Die Standardantwort für eine Bestätigung basiert auf dem Entwurfsmuster:**



    | Muster                                                 | Standardantwort                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Routine Bestätigungen <br/>                | Zufahren. <br/>                                                            |
    | Bestätigungen von riskanten Aktionen <br/>           | Fahren Sie nicht fort (oder die sichere Auswahl). <br/>                                 |
    | Unbeabsichtigte Folge Bestätigungen <br/> | Wenn Konsequenzen wichtig sind, fahren Sie nicht fort. Andernfalls fahren Sie fort. <br/> |
    | Erläuterungen <br/>                       | Die wahrscheinlichste Antwort. <br/>                                           |
    | Sicherheits Bestätigungen <br/>               | Fahren Sie nicht fort. <br/>                                                      |
    | Bestätigung von Ulterior-Motiven <br/>        | Zufahren. <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a>Diese Meldung nicht mehr anzeigen

-   **Verwenden Sie diese Option nur für die Muster der Routine-und Ulterior-Motiv-Bestätigung.** Wenn die Informationen für die anderen Muster erforderlich sind, sollten Sie immer angezeigt werden.
-   **Geben Sie diese Option nicht an, um eine unnötige Bestätigung anzuzeigen.** Entfernen Sie einfach die Bestätigung.

**Falsch:**

![Screenshot von "diese Erinnerungen verwerfen?" ](images/mess-confirm-image32.png)

**Trotzdem falsch:**

![Screenshot von "Meldung nicht mehr anzeigen"](images/mess-confirm-image33.png)

In diesen Beispielen wird durch das Hinzufügen einer Option Diese Meldung nicht mehr anzeigen eine unnötige Bestätigung nicht behoben.

Weitere Richtlinien finden Sie unter [Dialog Felder](win-dialog-box.md).

### <a name="bulk-operations"></a>Massenvorgänge

-   Stellen Sie für Bestätigungen, die für Massen Vorgänge gelten, eine Option zum Anwenden der Bestätigung auf den gesamten Vorgang bereit.

![Screenshot von "do this for all Items?" Kontrollkästchen ](images/mess-confirm-image34.png)

Dieses Beispiel enthält eine Option für Massen Vorgänge.

-   Entfernen oder verschieben Sie Bestätigungen bei einem Massen Vorgang.

**Falsch:**

![Screenshot des Dialog Felds "Datei Löschen bestätigen" ](images/mess-confirm-image35.png)

In diesem Beispiel bestätigt Windows Explorer in Windows XP jede schreibgeschützte Datei während einer Massen Datei Verschiebung. Es empfiehlt sich, nur die schreibgeschützten Dateien zu kopieren, ohne Sie zu Fragen, oder die Verarbeitung dieser Dateien zu verschieben und die Bestätigung am Ende der Aufgabe zu präsentieren.

### <a name="progressive-disclosure&quot;></a>Schrittweise Offenlegung

-   **Wenn Sie erweiterte Informationen in eine Bestätigungsmeldung einschließen müssen, können Sie diese mithilfe der Schaltflächen für die Progressive Offenlegung anzeigen (z. b. &quot;Details anzeigen").** Dies vereinfacht die Bestätigung der typischen Verwendung. Blenden Sie erforderliche Informationen nicht aus, da Benutzer Sie möglicherweise nicht finden.
-   **Verwenden Sie "Details anzeigen" nicht, es sei denn, es gibt wirklich weitere Details.** Geben Sie die vorhandenen Informationen nicht nur in einem anderen Format zurück.

Informationen zu Bezeichnungs Richtlinien finden Sie unter [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md).

### <a name="user-account-control"></a>Benutzerkontensteuerung

-   **Verwenden Sie die Benutzerkontensteuerung (User Account Control, UAC) nicht als Ersatz für eine Bestätigung.** Wenn für eine Aktion eine Bestätigung erforderlich ist, verwenden Sie ein separates Dialogfeld. Während der Benutzer [Oberfläche](winenv-uac.md)für die Rechte Erweiterung müssen sich Benutzer darauf konzentrieren, ob Sie die Aufgabe gestartet haben und ob das Programm vertrauenswürdig ist.
-   **Anzeigen der Bestätigung vor der Benutzeroberfläche für die Rechte Erweiterung** Dadurch entfällt unnötige Erhöhung.

## <a name="text"></a>Text

### <a name="general"></a>Allgemein

-   **Entfernen Sie den redundanten Text.** Suchen Sie nach redundantem Text in Titeln, Haupt Anweisungen, ergänzenden Anweisungen, Inhalts Bereichen, Befehls Verknüpfungen und Commit-Schaltflächen. Im Allgemeinen sollten Sie voll Text in Anweisungen und interaktiven Steuerelementen belassen und Redundanz von den anderen Orten entfernen.
-   **Verwenden Sie im Text nicht "Warning" oder "Warning".** Wenn Benutzer mit Vorsicht fortfahren müssen, geben Sie dies stattdessen mithilfe eines Warn Symbols an.

**Falsch:**

![Screenshot der Volumen Formatierungs Bestätigung ](images/mess-confirm-image36.png)

In diesem Beispiel ist der Begriff "Warning" nicht erforderlich.

### <a name="titles"></a>Titel

-   **Verwenden Sie den Titel, um den Befehl oder das Feature zu identifizieren, von dem die Bestätigung stammt. Ausnahmen**
    -   Wenn eine Bestätigung durch viele verschiedene Befehle angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.
    -   Wenn der Titel mit der Main-Anweisung redundant oder verwirrend wäre, sollten Sie stattdessen den Programmnamen verwenden.

Wenn die Bestätigung jedoch von einer Aufgabe mit langer Ausführungszeit ausgeht und nach dem Starten der Aufgabe möglicherweise gut angezeigt wird, verwenden Sie immer den Befehl oder das Feature, um den Kontext eindeutig zu identifizieren.

-   **Verwenden Sie den Titel nicht, um zu erläutern, wie Sie im Dialog** Feld mit der Main-Anweisung vorgehen sollten.
-   Wenn Sie Klarheit hinzufügen, starten Sie den Titel mit dem Wort confirm.
-   **Für riskante Aktions Bestätigungen können Sie den Namen des betroffenen Objekts hinzufügen, um zusätzliche Akzente zu erhalten.**

![Screenshot des Dialogfeld Titels "f-Laufwerk formatieren" ](images/mess-confirm-image13.png)

In diesem Beispiel ist das zu formatierende Laufwerk im Titel enthalten.

-   Verwenden Sie die Groß-/Kleinschreibung im [Titel](glossary.md), ohne die Beendigung zu beenden

### <a name="main-instructions"></a>Haupt Anleitung

-   **Die Haupt Anweisung für eine Bestätigung basiert auf dem Entwurfsmuster:**



    | Muster                                                 | Main-Anweisung                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Unbeabsichtigte Folge Bestätigungen <br/> | State gibt die unbeabsichtigte Folge aus.<br/> **Ausnahme:** wenn eine Frage, die fragt, ob der Benutzer den Vorgang fortsetzen möchte, die unbeabsichtigte Folge impliziert, stellen Sie stattdessen die Frage. <br/> ![Screenshot von "alle Registerkarten schließen" bestätigt ](images/mess-confirm-image15.png)<br/> In diesem Beispiel werden die Folgen der Aktion durch den Benutzer aufgefordert, ausreichend fortzufahren.<br/> |
    | Alle anderen <br/>                           | Stellen Sie eine einzelne Frage, um zu bestimmen, ob der Benutzer den Vorgang fortsetzen möchte. <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   **Bei der präzisen Verwendung wird nur ein einzelner, kompletter Satz verwendet.** Entfernen Sie die Haupt Anweisung zu den wesentlichen Informationen. Wenn Sie etwas anderes erläutern müssen, verwenden Sie eine ergänzende Anweisung.
-   **Wenn Objekte beteiligt sind, geben Sie die vollständigen Namen an.**
-   **Verwenden Sie einen positiven Ausdruck.** Die positive Formulierung ist für Benutzer leichter zu verstehen.

**Richtig:**

Möchten Sie die Datei-und Druckerfreigabe aktivieren?

**Falsch:**

Möchten Sie die Datei-und Druckerfreigabe deaktivieren?

Der Ausdruck muss jedoch mit dem zugeordneten Befehl identisch sein, auch wenn der Befehl negativ formuliert ist. Verwenden Sie z. b. deaktivieren, um einen deaktivierte Befehl zu bestätigen.

-   Obwohl es keine strengen Regeln für das formulieren gibt, **verfügen diese allgemeinen Bestätigungs Ausdrücke über die folgende Meldung:**



    | Ausdruck                                                            | Konnotation                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | Möchten Sie \[ eine Aktion ausführen \] ? <br/> | Bestätigen des direkten Ergebnisses einer Benutzer Anforderung. <br/> |
    | Möchten Sie \[ eine Aktion ausführen \] ? <br/>           | Bestätigen eines neben Effekts einer Benutzer Anforderung. <br/>     |
    | Möchten Sie \[ ein Ergebnis auswählen \] ? <br/>          | Sie benötigen eine Erläuterung. <br/>                           |
    | \[Führen Sie eine Aktion aus \] ? <br/>                          | Keine-Anmerkung. <br/>                                 |



 

-   Verwenden Sie für Bestätigungen von riskanten Aktionen den Begriff permanent, um anzugeben, dass eine Aktion nicht rückgängig gemacht werden kann.

![Screenshot der Bestätigung des permanenten Löschvorgangs ](images/mess-confirm-image37.png)

In diesem Beispiel gibt "permanent" an, dass die Aktion nicht rückgängig gemacht werden kann.

-   Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.

### <a name="supplemental-instructions"></a>Ergänzende Anweisungen

-   **Die ergänzende Anweisung für eine Bestätigung basiert auf dem Entwurfsmuster:**

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
    <td>Unbeabsichtigte Folge Bestätigungen <br/></td>
    <td>Stellen Sie eine einzelne Frage, um zu bestimmen, ob der Benutzer den Vorgang fortsetzen möchte. <br/></td>
    </tr>
    <tr class="odd">
    <td>Alle anderen <br/></td>
    <td>Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte. Beispiele hierfür sind: <br/>
    <ul>
    <li>Möglicher Verlust von einem oder mehreren der folgenden: <ul>
    <li>Ein wertvolles Asset, z. b. Datenverlust oder finanzieller Verlust.</li>
    <li>System Zugriff oder-Integrität.</li>
    <li>Datenschutz oder Kontrolle über vertrauliche Informationen.</li>
    </ul></li>
    <li>Nicht rückgängig zu machende Aktionen.</li>
    </ul></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Wiederholen Sie die main-Anweisung nicht mit etwas anderen Formulierungen.** Lassen Sie stattdessen die ergänzende Anweisung Weg, wenn nicht mehr hinzugefügt werden muss.
-   **Für unbeabsichtigte Folge Bestätigungen sollten Sie den Begriff trotzdem verwenden, um anzugeben, dass es keinen Grund gibt** , den Vorgang fortzusetzen, wenn der Benutzer die Haupt Anweisung übersehen hat. Weitere Informationen finden Sie unter Entwurfskonzepte.
-   Verwenden Sie vollständige Sätze, die Groß-/Kleinschreibung und die endinterpunktions Zeichen.

## <a name="documentation"></a>Dokumentation

Beim Verweis auf Bestätigungen:

-   Wenn der Titel für die Bestätigung spezifisch ist (d. h. nicht der Programmname), lesen Sie seinen Titel in einer Bestätigung. Andernfalls können Sie über die Haupt Anweisung darauf verweisen.
-   Falls erforderlich, können Sie auf ein Bestätigungs Dialogfeld als Nachricht verweisen.
-   Verwenden Sie den genauen Text, einschließlich der Groß-und Kleinschreibung.
-   Formatieren Sie den Text nach Möglichkeit fett formatiert. Andernfalls sollten Sie den Text nur bei Bedarf in Anführungszeichen setzen, um Verwechslungen zu vermeiden.

Beispiel: Klicken Sie in der Meldung **Datei kopieren** auf die neuere Datei.


---
title: Benutzerkontensteuerung (Grundlagen des Designs)
description: Eine gut entworfene Benutzeroberfläche für die Benutzerkontensteuerung trägt dazu bei, unerwünschte systemweite Änderungen auf eine Weise zu verhindern, die vorhersagbar ist und nur minimalen Aufwand erfordert.
ms.assetid: c4b83537-c600-4b24-bda6-df7a82719ab1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b0330ee3ffbf608296bcb89abe3e02ef6969500356d0cca4f45db9d24d8ff73f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935947"
---
# <a name="user-account-control"></a>Benutzerkontensteuerung

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Eine gut entworfene Benutzeroberfläche für die Benutzerkontensteuerung trägt dazu bei, unerwünschte systemweite Änderungen auf eine Weise zu verhindern, die vorhersagbar ist und nur minimalen Aufwand erfordert.

Wenn die Benutzerkontensteuerung (User Account Control, UAC) vollständig aktiviert ist, werden interaktive Administratoren normalerweise mit den geringsten Benutzerberechtigungen ausgeführt. Sie können sich jedoch selbst erhöhen, um Administrative Aufgaben auszuführen, indem sie der Zustimmungsbenutzeroberfläche explizit zustimmen. Zu diesen administrativen Aufgaben gehören das Installieren von Software und Treibern, das Ändern systemweiter Einstellungen, das Anzeigen oder Ändern anderer Benutzerkonten und das Ausführen von Verwaltungstools.

In ihrem Zustand mit den geringsten Berechtigungen werden Administratoren als geschützte Administratoren bezeichnet. In ihrem Zustand mit erhöhten Rechten werden sie als Administratoren mit erhöhten Rechten bezeichnet. Im Gegensatz dazu können Standardbenutzer selbst keine Rechte erhöhen, aber sie können einen Administrator bitten, sie über die Benutzeroberfläche für Anmeldeinformationen zu erhöhen. Für das integrierte Administratorkonto sind keine Rechteerweiterungen erforderlich.

![Screenshot der Sicherheitsmeldung "Programm zulassen" ](images/winenv-uac-image1.png)

Die Zustimmungs-Benutzeroberfläche, die verwendet wird, um geschützte Administratoren auf Administratorrechte zu erhöhen.

![Screenshot der Meldung, in der nach kennwortgefragt wird ](images/winenv-uac-image2.png)

Die Benutzeroberfläche für Anmeldeinformationen, die zum Erhöhen von Standardbenutzern verwendet wird.

Die UAC bietet die folgenden Vorteile:

-   Dadurch wird die Anzahl von Programmen reduziert, die mit erhöhten Rechten ausgeführt werden. Dadurch wird verhindert, dass Benutzer versehentlich ihre Systemeinstellungen ändern, und "Schadsoftware" wird daran gehindert, systemweiten Zugriff zu erhalten. Wenn die Rechteerweiterung verweigert wird, kann Schadsoftware nur die Daten des aktuellen Benutzers beeinflussen. Ohne Erhöhte Rechte kann Schadsoftware keine systemweiten Änderungen vornehmen oder andere Benutzer beeinträchtigen.
-   Bei [verwalteten Umgebungen](glossary.md)ermöglichen gut entworfene UAC-Umgebungen es Benutzern, produktiver zu sein, wenn sie als Standardbenutzer ausgeführt werden, indem unnötige Einschränkungen entfernt werden.
-   Standardbenutzer erhalten die Möglichkeit, Administratoren aufzufordern, ihnen die Berechtigung zum Ausführen administrativer Aufgaben innerhalb ihrer aktuellen Sitzung zu erteilen.
-   Für Heimumgebungen ermöglicht es eine bessere Kontrolle der Eltern über systemweite Änderungen, einschließlich der installierten Software.

**Entwickler:** Informationen zur Implementierung finden Sie unter [Redesign Your UI for UAC Compatibility (Umgestalten der Benutzeroberfläche für UAC-Kompatibilität).](/previous-versions/bb756990(v=msdn.10))

In Windows Vista können geschützte Administratoren über alle Systemänderungen benachrichtigt werden. Die Standardeinstellung für die UAC besteht darin, alle Änderungen unabhängig vom Ursprung zu benachrichtigen. Wenn Sie benachrichtigt werden, ist Ihr Desktop abgeblendet, und Sie müssen die Anforderung im UAC-Dialogfeld entweder genehmigen oder ablehnen, bevor Sie auf Ihrem Computer weitere Möglichkeiten haben. Die Abgeblendung Ihres Desktops wird als [sicherer Desktop](glossary.md) bezeichnet, da andere Programme nicht ausgeführt werden können, während sie abgeblendet sind.

Windows 7 werden zwei UAC-Zwischeneinstellungen für geschützte Administratoren eingeführt, zusätzlich zu den beiden einstellungen von Windows Vista. Die erste besteht darin, Benutzer nur zu benachrichtigen, wenn ein Programm die Änderung vornimmt, sodass Administratoren automatisch erhöht werden, wenn sie selbst eine Änderung vornehmen. Dies ist die UAC-Standardeinstellung in Windows 7 und nutzt auch den sicheren Desktop.

Die zweite Zwischeneinstellung in Windows 7 ist mit der ersten identisch, mit der Ausnahme, dass der sichere Desktop nicht verwendet wird.

![Screenshot von vier UAC-Einstellungen in Windows 7 ](images/winenv-uac-image3.png)

Windows 7 werden zwei UAC-Zwischeneinstellungen eingeführt.

**Hinweis:** Richtlinien zum Schreiben von Code zur Unterstützung der [Benutzerkontensteuerung](/previous-versions/aa905330(v=msdn.10)) werden in einem separaten Artikel vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

**Ziele**

Eine gut entworfene Benutzeroberfläche für die Benutzerkontensteuerung hat die folgenden Ziele:

-   **Vermeiden Sie unnötige Rechteerweiterungen.** Benutzer sollten nur erhöht werden müssen, um Aufgaben auszuführen, die Administratorrechte erfordern. Alle anderen Aufgaben sollten so entworfen werden, dass keine Rechteerweiterung erforderlich ist. Ältere Software erfordert häufig unnötige Administratorrechte, indem sie in die Registrierungsabschnitte HKLM oder HKCR oder in die Ordner Programme oder Windows System schreibt.
-   **Vorhersagbar sein.** Standardbenutzer müssen wissen, welche Aufgaben ein Administrator ausführen muss oder in verwalteten Umgebungen überhaupt nicht ausgeführt werden kann. Administratoren müssen wissen, welche Aufgaben eine Erhöhung erfordern. Wenn sie den Bedarf an Erhöhungen nicht genau vorhersagen können, geben sie wahrscheinlich ihre Zustimmung für administrative Aufgaben, wenn sie dies nicht sollten.
-   **Minimaler Aufwand erforderlich.** Aufgaben, für die Administratorrechte erforderlich sind, sollten so entworfen werden, dass eine einzelne Erhöhung erforderlich ist. Aufgaben, die mehrere Rechteerweiterungen erfordern, werden schnell mühsam.
-   **Kehren Sie auf die geringsten Berechtigungen zurück.** Sobald eine Aufgabe, die Administratorrechte erfordert, abgeschlossen ist, sollte das Programm den Status der geringsten Rechte kehren.

**Aufgabenfluss für erhöhte Rechte**

Wenn für eine Aufgabe erhöhte Rechte erforderlich sind, sind die folgenden Schritte erforderlich:

1.  **Einstiegspunkt.** Aufgaben, für die eine sofortige Erhöhung erforderlich ist, wenn die UAC vollständig aktiviert ist, verfügen über Einstiegspunkte, die mit dem UAC-Shield markiert sind. In diesem Fall sollten Benutzer sofort nach dem Klicken auf solche Befehle eine Benutzeroberfläche für erhöhte Rechte sehen, und sie sollten besonders vorsichtig sein, wenn sie die Benutzeroberfläche für erhöhte Rechte von Aufgaben sehen, die keinen Schutz aufweisen.

    ![Screenshot von UAC-Shield-Symbolen und deren Bezeichnungen ](images/winenv-uac-image4.png)

    In diesem Beispiel erfordern die Elemente für die Jugendschutz- und Benutzerkontensteuerung erhöhte Rechte.

    Wenn UAC teilweise aktiviert oder vollständig deaktiviert ist, wird der UAC-Shield weiterhin angezeigt, um anzugeben, dass der Task Änderungen auf Systemebene umfasst und daher eine Erhöhung erfordert, auch wenn dem Benutzer die Benutzeroberfläche für erhöhte Rechte möglicherweise nicht angezeigt wird. Wenn Sie den UAC-Schutz immer für Aufgaben anzeigen, die erhöhte Rechte erfordern, bleibt die Benutzeroberfläche einfach und vorhersagbar.

2.  **Höhe.** Für geschützte Administratoren fordert der Task die Zustimmung über die Benutzeroberfläche für die Zustimmung an. Für Standardbenutzer fordert die Aufgabe Administratoranmeldeinformationen über die Benutzeroberfläche für Anmeldeinformationen an.

    ![Screenshot von zwei Arten von Rechteerweiterungen ](images/winenv-uac-image5.png)

    Diese Beispiele zeigen die Benutzeroberfläche für Anmeldeinformationen und die Benutzeroberfläche für die Zustimmung.

3.  **Separater Prozess mit erhöhten Rechten.** Intern wird ein neuer Prozess mit erhöhten Rechten erstellt, um die Aufgabe auszuführen.
4.  **Kehren Sie zu den geringsten Rechten zurück.** Kehren Sie bei Bedarf auf die geringsten Rechte zurück, um alle Schritte auszuführen, für die keine Erhöhung erforderlich ist.

Beachten Sie, dass Tasks keine erhöhten Zustände "merken". Wenn der Benutzer z. B. in einem Assistenten über einen Einstiegspunkt für erhöhte Rechte hin und her navigiert, muss der Benutzer jedes Mal erhöhte Rechte erhöhen.

## <a name="usage-patterns"></a>Verwendungsmuster

Die Benutzerkontensteuerung verfügt über mehrere Verwendungsmuster (in der Reihenfolge ihrer Präferenz):

1.  **Arbeiten für Standardbenutzer.** Entwerfen Sie das Feature für alle Benutzer, indem Sie seinen Bereich auf den aktuellen Benutzer beschränken. Indem Sie die Einstellungen auf den aktuellen Benutzer (im Gegensatz zu systemweit) beschränken, müssen Sie eine Benutzeroberfläche für erhöhte Rechte vollständig entfernen und Benutzern ermöglichen, die Aufgabe abzuschließen.

    **Falsch:**

    ![Screenshot der Meldung: Sie haben keine Berechtigung ](images/winenv-uac-image6.png)

    In diesem Beispiel mussten Windows XP-Benutzer über Administratorrechte verfügen, um die aktuelle Zeitzone anzuzeigen oder zu ändern.

    **Richtig:**

    ![Screenshot des Dialogfelds "Datum und Uhrzeit" ](images/winenv-uac-image7.png)

    In diesem Beispiel wurde das Zeitzonenfeature in Windows 7 umgestaltet und Windows Vista für alle Benutzer geeignet.

2.  **Sie verfügen über separate Benutzeroberflächenelemente für Standardbenutzer und -administratoren.** Trennen Sie Standardbenutzeraufgaben eindeutig von administrativen Aufgaben. Gewähren Sie allen Benutzern Zugriff auf nützliche schreibgeschützte Informationen. Identifizieren Sie administrative Aufgaben eindeutig mit dem UAC-Shield.

    ![Grafik des UAC-Shields mit erforderlicher Erhöhung ](images/winenv-uac-image8.png)

    In diesem Beispiel zeigt das Systemsteuerungselement seinen Zustand für alle Benutzer an, aber das Ändern der systemweiten Einstellungen erfordert erhöhte Rechte.

3.  **Standardbenutzer können versuchen, eine Aufgabe zu versuchen und bei einem Fehler erhöhte Rechte zu erhöhen.** Wenn Standardbenutzer die Informationen anzeigen können und einige Änderungen ohne Erhöhte Rechte vornehmen können, erlauben Sie ihnen den Zugriff auf die Benutzeroberfläche, und lassen Sie sie nur dann erhöhen, wenn die Aufgabe fehlschlägt. Dieser Ansatz eignet sich, wenn Standardbenutzer eingeschränkten Zugriff haben, z. B. mit Eigenschaften ihrer eigenen Dateien in Windows Explorer. Sie eignet sich auch für Einstellungen auf Systemsteuerung Hybrid Hub-Seiten.

    ![Screenshot: Meldung "Zugriff verweigert" ](images/winenv-uac-image9.png)

    In diesem Beispiel hat der Benutzer versucht, die Eigenschaften der Programmdatei zu ändern, verfügte aber nicht über ausreichende Berechtigungen. Der Benutzer kann die Rechte erhöhen und es erneut versuchen.

4.  **Arbeiten Sie nur für Administratoren.** Verwenden Sie diesen Ansatz nur für Administratorfeatures und -programme! Wenn ein Feature nur für Administratoren vorgesehen ist (und keine Navigationspfade oder nützliche schreibgeschützte Informationen für Standardbenutzer enthält), können Sie am Einstiegspunkt zur Eingabe von Administratoranmeldeinformationen auffordern, bevor Sie eine Benutzeroberfläche anzeigen. Verwenden Sie diesen Ansatz für lange Assistenten und [Seitenflows,](glossary.md) wenn für alle Pfade Administratorrechte erforderlich sind.

    Wenn das gesamte Programm nur für Administratoren vorgesehen ist, markieren Sie es, um zum Starten Administratoranmeldeinformationen einzufordern. Windows zeigt solche Programmsymbole mit der UAC-Shieldüberlagerung an.

    ![Screenshot: Windows-Logo und UAC-Shield-Überlagerung ](images/winenv-uac-image10.png)

    In diesem Beispiel benötigt das Programm Administratorrechte, um gestartet zu werden.

## <a name="guidelines"></a>Richtlinien

### <a name="uac-shield-icon"></a>UAC-Shield-Symbol

-   **Zeigen Sie Steuerelemente mit dem UAC-Shield an, um anzugeben, dass für den Task eine sofortige Erhöhung erforderlich ist, wenn die UAC vollständig aktiviert ist,** auch wenn die UAC derzeit nicht vollständig aktiviert ist. Wenn alle Pfade eines Assistenten und [Seitenflusses](glossary.md) erhöhte Rechte erfordern, zeigen Sie den UAC-Schutz am Einstiegspunkt des Tasks an. Durch die ordnungsgemäße Verwendung des UAC-Shields können Benutzer vorhersagen, wann erhöhte Rechte erforderlich sind.
-   **Wenn Ihr Programm mehrere Versionen von Windows unterstützt, zeigen Sie den UAC-Schutz an, wenn mindestens eine Version eine Erhöhung erfordert.** Da Windows XP nie erhöhte Rechte erfordert, sollten Sie erwägen, die UAC-Schirme für Windows XP zu entfernen, wenn Sie dies konsistent und ohne Beeinträchtigung der Leistung tun können.
-   **Zeigen Sie den UAC-Schutz nicht für Aufgaben an, für die in den meisten Kontexten keine Erhöhung erforderlich ist.** Da dieser Ansatz manchmal irreführend sein wird, ist es der bevorzugte Ansatz, stattdessen einen ordnungsgemäß abgeschirmten kontextbezogenen Befehl zu verwenden.

    ![Screenshot von Fotodateien im Windows-Explorer ](images/winenv-uac-image11.png)

    Da der Befehl Neuer Ordner nur erhöhte Rechte erfordert, wenn er in Systemordnern verwendet wird, wird er ohne UAC-Shield angezeigt.

-   Der UAC-Shield kann auf den folgenden Steuerelementen angezeigt werden:

    **Befehlsschaltflächen:**

    ![Screenshot der Befehlsschaltfläche mit UAC-Shield-Symbol ](images/winenv-uac-image12.png)

    Eine Befehlsschaltfläche, die eine sofortige Rechteerweiterung erfordert.

    **Befehlslinks:**

    ![Screenshot des Befehlslinks mit UAC-Shield-Symbol ](images/winenv-uac-image13.png)

    Ein Befehlslink, der eine sofortige Rechteerweiterung erfordert.

    **Links:**

    ![Screenshot: Ändern des Kontolinks mit uac shield ](images/winenv-uac-image14.png)

    Ein Link, der eine sofortige Rechteerweiterung erfordert.

    **Menüs:**

    ![Screenshot des Menüs mit UAC-Shield ](images/winenv-uac-image15.png)

    Ein Dropdownmenü, das sofortige Rechteerweiterungen erfordert.

-   Da Tasks sich nicht an erhöhte Zustände erinnern, **ändern Sie den UAC-Schutz nicht so, dass er den Zustand widerspiegelt.**
-   **Zeigen Sie den UAC-Schutz an, auch wenn die Benutzerkontensteuerung deaktiviert wurde oder der Benutzer das integrierte Administratorkonto verwendet.** Die konsistente Anzeige des UAC-Shields ist einfacher zu programmieren und stellt Benutzern Informationen über die Art der Aufgabe bereit.

### <a name="elevation"></a>Elevation

-   **Entwerfen Sie nach Möglichkeit Aufgaben, die von Standardbenutzern ohne Erhöhte Rechte ausgeführt werden sollen.** Gewähren Sie allen Benutzern Zugriff auf nützliche schreibgeschützte Informationen.
-   **Erhöhen Sie die Rechte pro Aufgabe, nicht pro Einstellung.** Kombinieren Sie Standardbenutzereinstellungen nicht mit Administratoreinstellungen auf einer einzelnen Seite oder einem Dialogfeld. Wenn Standardbenutzer beispielsweise einige, aber nicht alle Einstellungen ändern können, teilen Sie diese Einstellungen als separate Benutzeroberfläche auf.

    **Falsch:**

    ![Screenshot des Dialogfelds "Datums- und Uhrzeiteinstellungen" ](images/winenv-uac-image16.png)

    In diesem Beispiel werden Standardbenutzereinstellungen falsch mit Administratoreinstellungen gemischt.

    **Richtig:**

    ![Screenshot des gleichen Dialogfelds ohne UAC-Shields ](images/winenv-uac-image17.png)

    In diesem Beispiel befinden sich die Einstellungen zum Ändern von Datum und Uhrzeit in einem separaten Dialogfeld, das nur Administratoren zur Verfügung steht. Die Zeitzoneneinstellungen sind für Standardbenutzer verfügbar und werden nicht mit Administratoreinstellungen gemischt.

-   **Berücksichtigen Sie nicht die Notwendigkeit, die Rechte zu erhöhen, wenn Sie bestimmen, ob ein Steuerelement angezeigt oder deaktiviert werden soll.** Der Grund ist wie folgt:
    -   Gehen Sie in nicht verwalteten Umgebungen davon aus, dass Standardbenutzer die Rechte erhöhen können, indem sie einen Administrator bitten. Das Deaktivieren von Steuerelementen, die erhöhte Rechte erfordern, würde verhindern, dass Benutzer über Erhöhte Rechte von Administratoren verfügen.
    -   Gehen Sie in verwalteten Umgebungen davon aus, dass Standardbenutzer überhaupt keine Rechte erhöhen können. Das Entfernen von Steuerelementen, die erhöhte Rechte erfordern, würde verhindern, dass Benutzer wissen, wann sie nicht mehr suchen sollten.
-   **So vermeiden Sie unnötige Rechteerweiterungen:**
    -   **Wenn für eine Aufgabe erhöhte Rechte erforderlich sind, erhöhen Sie die Rechte so spät wie möglich.** Wenn eine Aufgabe eine [Bestätigung](mess-confirm.md)benötigt, zeigen Sie die Benutzeroberfläche für erhöhte Rechte erst an, nachdem der Benutzer dies bestätigt hat. Wenn für eine Aufgabe immer erhöhte Rechte erforderlich sind, erhöhen Sie die Rechte an ihrem Einstiegspunkt.
    -   **Bleiben Sie nach der Erhöhung erhöht, bis erhöhte Berechtigungen nicht mehr erforderlich sind.** Benutzer sollten nicht mehrmals erhöhen müssen, um eine einzelne Aufgabe auszuführen.
    -   **Wenn Benutzer die Rechte erhöhen müssen, um eine Änderung vorzunehmen, aber keine Änderungen vornehmen möchten, lassen Sie die Schaltflächen für positive Commits aktiviert, behandeln Sie den Commit jedoch als Abbruch.** Auf diese Weise müssen Benutzer keine Rechte erhöhen, nur um ein Fenster zu schließen.
    -   **Falsch:**
    -   ![Screenshot des Fensters mit nur einer aktiven Schaltfläche ](images/winenv-uac-image18.png)
    -   In diesem Beispiel ist die Schaltfläche Änderungen speichern deaktiviert, um unnötige Rechteerweiterungen zu vermeiden, wird jedoch aktiviert, wenn Benutzer die Auswahl ändern. Die deaktivierte Commitschaltfläche sieht jedoch so aus, als hätten Benutzer keine Auswahl.
-   **Es wird keine Fehlermeldung angezeigt, wenn Tasks fehlschlagen, da Benutzer keine Erhöhten Rechte ausgewählt haben.** Gehen Sie davon aus, dass Benutzer absichtlich nicht fortfahren möchten, sodass sie diese Situation nicht als Fehler betrachten.

    **Falsch:**

    ![Screenshot der Meldung: fabrikam restore can't run (Fabrikam-Wiederherstellung kann nicht ausgeführt werden) ](images/winenv-uac-image19.png)

    In diesem Beispiel wird bei der Fabrikam-Wiederherstellung fälschlicherweise eine Fehlermeldung angezeigt, wenn der Benutzer entscheidet, die Rechte nicht zu erhöhen.

-   **Zeigen Sie keine Warnungen an, um zu erklären, dass Benutzer möglicherweise ihre Berechtigungen zum Ausführen von Aufgaben erhöhen müssen.** Lassen Sie diese Tatsache von Benutzern selbst ermitteln.
-   **Zeigen Sie den UAC-Schutz und die Benutzeroberfläche für erhöhte Rechte basierend auf der folgenden Tabelle an:**

    | Object | Umstand | Wo der UAC-Shield ablegt | Zeitpunkt der Erhöhung der Rechte |
    |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | Programm<br/>    | Das gesamte Programm ist nur für Administratoren vorgesehen.<br/>                                                                                                            | ![Screenshot: Windows-Logo und UAC-Shield-Überlagerung ](images/winenv-uac-image10.png)<br/> UAC-Shieldüberlagerung auf Programmsymbol.<br/>                                                                       | Anzeigen der Benutzeroberfläche für erhöhte Rechte beim Start.<br/>                                                           |
    | Befehl<br/>    | Der gesamte Befehl ist nur für Administratoren vorgesehen.<br/>                                                                                                            | ![Screenshot: Ändern der Kontoverknüpfung und des UAC-Shields ](images/winenv-uac-image14.png)<br/> UAC-Shield auf Befehlsschaltfläche oder Link.<br/>                                                                      | Anzeigen der Benutzeroberfläche für erhöhte Rechte, wenn auf die Befehlsschaltfläche oder den Link geklickt wird, jedoch nach bestätigungserkenntnissen.<br/> |
    | Befehl<br/>    | Der Befehl zeigt nützliche schreibgeschützte Informationen an, die für alle Benutzer geeignet sind, änderungen erfordern jedoch Administratorrechte.<br/>                               | ![Screenshot des Links "Einstellungen ändern" und "uac shield" ](images/winenv-uac-image8.png)<br/> UAC-Shield auf Befehlsschaltfläche oder Link, um Änderungen vorzunehmen.<br/>                                                      | Anzeigen der Benutzeroberfläche für erhöhte Rechte, wenn auf die Befehlsschaltfläche geklickt wird, jedoch nach bestätigungserkenntnissen.<br/>         |
    | Befehl<br/>    | Standardbenutzer können die Informationen anzeigen und möglicherweise einige Änderungen ohne Erhöhte Rechte vornehmen. Standardbenutzern den Versuch zu ermöglichen und bei einem Fehler erhöhte Rechte zu erhöhen.<br/> | ![Screenshot des Fehlers mit dem UAC-Symbol auf der Wiederholungsschaltfläche ](images/winenv-uac-image9.png)<br/> Zeigen Sie den UAC-Schutz für den Befehl nicht an, sondern für den Einstiegspunkt für erhöhte Rechte, wenn der Befehl fehlschlägt.<br/> | Anzeige der Benutzeroberfläche für erhöhte Rechte, wenn der Benutzer den Befehl erneut anmeldet.<br/>                                       |
    | Taskschritt<br/>  | Alle nachfolgenden Schritte erfordern erhöhte Rechte.<br/>                                                                                                               | ![Screenshot der nächsten Befehlsschaltfläche mit uac shield ](images/winenv-uac-image20.png)<br/> UAC-Shield auf der Schaltfläche Weiter (oder gleichwertig).<br/>                                                                | Zeigen Sie die Benutzeroberfläche für erhöhte Rechte an, wenn auf die Schaltfläche Weiter oder ein anderer Commit geklickt wird.<br/>                         |
    | Taskschritt<br/>  | Einige Branches erfordern erhöhte Rechte.<br/>                                                                                                                      | ![Screenshot des Befehlslinks mit uac shield ](images/winenv-uac-image21.png)<br/> UAC-Shield für Befehlslinks, die eine Erhöhung erfordern.<br/>                                                              | Anzeigen der Benutzeroberfläche für erhöhte Rechte, wenn Befehlslinks mit UAC-Shield angeklickt werden.<br/>                      |

    

     

### <a name="elevation-ui"></a>Benutzeroberfläche für erhöhte Rechte

-   **Wenn der Benutzer ein Konto bereitstellt, das nicht gültig ist (Name oder Kennwort) oder nicht über Administratorrechte verfügt, zeigen Sie einfach die Benutzeroberfläche für Anmeldeinformationen erneut an.** Es wird keine Fehlermeldung angezeigt.
-   **Wenn der Benutzer die Anmeldeinformationsbenutzeroberfläche abbricht, kehren Sie den Benutzer zur ursprünglichen Benutzeroberfläche zurück.** Es wird keine Fehlermeldung angezeigt.
-   Wenn die Benutzerkontensteuerung deaktiviert wurde und ein Standardbenutzer versucht, eine Aufgabe auszuführen, die eine Erhöhung erfordert, geben Sie eine Fehlermeldung mit dem Hinweis an, dass für diese Aufgabe Administratorrechte erforderlich sind. Um diese Aufgabe auszuführen, müssen Sie sich mit einem Administratorkonto anmelden."

![Screenshot der Aufgabe erfordert Die Meldung "Berechtigungen" ](images/winenv-uac-image22.png)

In diesem Beispiel wurde die Benutzerkontensteuerung deaktiviert, sodass in einer Fehlermeldung erklärt wird, dass der Benutzer ein Administratorkonto verwenden muss.

### <a name="wizards"></a>Assistenten

-   **Erhöhen Sie die Rechte nicht mehrmals.** Sobald ein Assistent mit erhöhten Rechten ausgeführt wird, sollte er mit erhöhten Rechten bleiben.
-   Wenn die Aufgabe innerhalb des Assistenten ausgeführt wird, legen Sie einen UAC-Shield auf die Schaltfläche "Weiter" der Commit-Seite (die eine [spezifischere Bezeichnung](win-wizards.md)erhalten sollte). Beim Commit des Benutzers:
    -   Wenn die nächste Seite eine Seite Status ist, wechseln Sie zu dieser Seite, und zeigen Sie modal die Benutzeroberfläche für erhöhte Rechte an. Führen Sie nach erfolgreicher Erhöhung der Rechte die Aufgabe aus.
    -   Wenn die nächste Seite eine Vervollständigungsseite ist, wechseln Sie zu dieser Seite (ersetzen Sie den Inhalt jedoch vorübergehend durch "Warten auf Berechtigung..."), und zeigen Sie die Benutzeroberfläche für erhöhte Rechte modal an. Führen Sie nach erfolgreicher Erhöhung der Rechte die Aufgabe aus, und zeigen Sie dann den Inhalt der Seite Abschluss an.
    -   Wenn der Benutzer die Benutzeroberfläche für erhöhte Rechte abbricht, kehren Sie zur Seite Commit zurück. Auf diese Weise kann der Benutzer es erneut versuchen.
-   Wenn die Aufgabe nach Abschluss des Assistenten ausgeführt wird, legen Sie einen UAC-Shield auf der Schaltfläche "Fertig stellen" der Commit-Seite (die eine [spezifischere Bezeichnung](win-wizards.md)erhalten sollte). Beim Commit des Benutzers:
    -   Verbleiben Sie auf der Seite Commit, und zeigen Sie modal die Benutzeroberfläche für erhöhte Rechte an. Schließen Sie nach erfolgreicher Erhöhung den Assistenten.
    -   Wenn der Benutzer die Benutzeroberfläche für erhöhte Rechte abbricht, kehren Sie zur Seite Commit zurück. Auf diese Weise kann der Benutzer es erneut versuchen.
-   Für lange Assistenten, die nur für Administratoren vorgesehen sind, können Sie am Einstiegspunkt zur Eingabe von Administratoranmeldeinformationen auffordern, bevor Sie eine Benutzeroberfläche anzeigen.

## <a name="text"></a>Text

-   **Verwenden Sie keine Auslassungszeichen, nur weil für einen Befehl erhöhte Rechte erforderlich sind.** Die Notwendigkeit, die Rechte zu erhöhen, wird mit dem UAC-Shield angegeben.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Benutzerkontensteuerung:

-   Beziehen Sie sich auf das Feature als Benutzerkontensteuerung (bei erster Erwähnung) oder UAC (bei nachfolgender Erwähnung), nicht als Benutzerkonto mit geringsten Berechtigungen oder LUA.
-   Beziehen Sie sich auf Nichtadministratoren als Standardbenutzer.
-   Integrierte Computeradministratoren finden Sie unter Integrierte Administratoren.

In der Benutzerdokumentation:

-   Beziehen Sie sich auf das Erteilen der Zustimmung zum Ausführen einer administrativen Aufgabe als Erteilen der Berechtigung.

In der Programmierung und anderen technischen Dokumentationen:

-   Beziehen Sie sich auf das Erteilen der Zustimmung zum Ausführen einer Administrativen Aufgabe als Rechteerweiterung.
-   Beziehen Sie sich im Kontext der UAC auf Administratoren als geschützte Administratoren, wenn sie keine erhöhten Rechte haben, und Administratoren mit erhöhten Rechten nach erhöhten Rechten.
-   Weitere Informationen finden Sie in dem Dialogfeld, in dem Kennwörter als Anmeldeinformations-Benutzeroberfläche eingegeben werden. Verweisen Sie auf das Dialogfeld, das zum Erteilen der Zustimmung verwendet wird, als Zustimmungs-Benutzeroberfläche. Im Allgemeinen wird beides als Elevation UI (Erhöhte Benutzeroberfläche) bezeichnet.


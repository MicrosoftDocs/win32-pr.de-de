---
title: Benutzerkontensteuerung (Entwurfs Grundlagen)
description: Eine gut entworfene Benutzerkontensteuerung hilft, unerwünschte systemweite Änderungen auf eine Weise zu verhindern, die vorhersagbar ist und einen minimalen Aufwand erfordert.
ms.assetid: c4b83537-c600-4b24-bda6-df7a82719ab1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b346e5cb581ac83ad2ebffabe73c5fbed636d814
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104555410"
---
# <a name="user-account-control"></a>Benutzerkontensteuerung

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Eine gut entworfene Benutzerkontensteuerung hilft, unerwünschte systemweite Änderungen auf eine Weise zu verhindern, die vorhersagbar ist und einen minimalen Aufwand erfordert.

Wenn die Benutzerkontensteuerung (User Account Control, UAC) vollständig aktiviert ist, werden interaktive Administratoren normalerweise mit geringsten Benutzerrechten ausgeführt. Sie können sich jedoch selbst erhöhen, um administrative Aufgaben durchzuführen, indem Sie der Zustimmungs Benutzeroberfläche explizite Zustimmung erteilen. Zu diesen Verwaltungsaufgaben gehören das Installieren von Software und Treibern, das Ändern von systemweiten Einstellungen, das Anzeigen oder Ändern anderer Benutzerkonten und das Ausführen von Verwaltungs Tools.

Im Zustand mit den geringsten Rechten werden Administratoren als geschützte Administratoren bezeichnet. Im Zustand mit erhöhten Rechten werden Sie als erweiterte Administratoren bezeichnet. Im Gegensatz dazu können Standard Benutzer nicht selbst herauf Stufen, Sie können jedoch einen Administrator bitten, Sie mithilfe der Benutzeroberfläche für Anmelde Informationen zu erhöhen. Das integrierte Administrator Konto erfordert keine Erhöhung der Rechte.

![Screenshot der Sicherheits Meldung "Programm zulassen" ](images/winenv-uac-image1.png)

Die Zustimmungs Benutzeroberfläche, mit der geschützte Administratoren auf Administratorrechte erweitert werden.

![Screenshot der Meldung mit dem Kennwort ](images/winenv-uac-image2.png)

Die Benutzeroberfläche für Anmelde Informationen, die verwendet wird, um Standard Benutzer zu erhöhen.

UAC bietet die folgenden Vorteile:

-   Dadurch wird die Anzahl der Programme verringert, die mit erhöhten Rechten ausgeführt werden. Dadurch wird verhindert, dass Benutzer Ihre Systemeinstellungen versehentlich ändern können, und es wird verhindert, dass "Malware" systemweiten Zugriff erhält. Wenn die Rechte Erweiterung verweigert wird, kann Schadsoftware nur die Daten des aktuellen Benutzers beeinflussen. Ohne Erhöhung der Rechte können Schadsoftware keine systemweiten Änderungen vornehmen oder andere Benutzer beeinträchtigen.
-   Für [verwaltete Umgebungen](glossary.md)ermöglichen gut gestaltete UAC-Benutzeroberflächen, dass Benutzer produktiver arbeiten können, wenn Sie als Standard Benutzer ausgeführt werden, indem unnötige Einschränkungen entfernt werden.
-   Standard Benutzer haben die Möglichkeit, Administratoren aufzufordern, Ihnen die Berechtigung zum Ausführen administrativer Aufgaben innerhalb Ihrer aktuellen Sitzung zu erteilen.
-   In Heim Umgebungen ermöglicht es eine bessere Kontrolle über systemweite Änderungen, einschließlich der installierten Software.

**Entwickler:** Implementierungs Informationen finden Sie unter [Umgestalten der Benutzeroberfläche für die UAC-Kompatibilität](/previous-versions/bb756990(v=msdn.10)).

In Windows Vista können geschützte Administratoren über alle Systemänderungen oder keine benachrichtigt werden. Die UAC-Standardeinstellung besteht darin, über alle Änderungen zu informieren, unabhängig von ihrem Ursprung. Wenn Sie benachrichtigt werden, wird der Desktop Abgleich angezeigt, und Sie müssen die Anforderung im UAC-Dialogfeld genehmigen oder verweigern, bevor Sie auf dem Computer weitere Aktionen ausführen können. Das Dimmen Ihres Desktops wird als [sicherer Desktop](glossary.md) bezeichnet, da andere Programme nicht ausgeführt werden können.

Windows 7 führt neben den beiden von Windows Vista zwei zwischengeschaltete UAC-Einstellungen für geschützte Administratoren ein. Der erste besteht darin, Benutzer nur dann zu benachrichtigen, wenn ein Programm die Änderung vornimmt, sodass Administratoren automatisch erhöht werden, wenn Sie eine Änderung vornehmen. Dies ist die Standardeinstellung für die UAC in Windows 7 und nutzt auch den sicheren Desktop.

Die zweite zwischen Einstellung in Windows 7 ist die gleiche wie die erste, mit der Ausnahme, dass Sie nicht den sicheren Desktop verwendet.

![Screenshot der vier UAC-Einstellungen in Windows 7 ](images/winenv-uac-image3.png)

Mit Windows 7 werden zwei zwischengeschaltete UAC-Einstellungen eingeführt.

**Hinweis:** Richtlinien für das Schreiben [von Code zur Unterstützung der Benutzerkontensteuerung](/previous-versions/aa905330(v=msdn.10)) werden in einem separaten Artikel vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

**Ziele**

Eine gut entworfene Benutzerkontensteuerung hat die folgenden Ziele:

-   **Vermeiden Sie unnötige Rechte.** Benutzer müssen nur die Rechte erweitern, um Aufgaben auszuführen, für die Administratorrechte erforderlich sind. Alle anderen Aufgaben sollten so entworfen werden, dass die Notwendigkeit der Erhöhung der Rechte entfällt. Ältere Software benötigt häufig Administratorrechte, indem Sie in die Registrierungs Abschnitte "HKLM", "HKCR" oder "Programme" oder "Windows-System Ordner" schreiben.
-   **Ist vorhersagbar.** Standard Benutzer müssen wissen, welche Aufgaben ein Administrator in verwalteten Umgebungen ausführen muss oder nicht. Administratoren müssen wissen, welche Aufgaben eine Erhöhung der Rechte erfordern. Wenn Sie die Notwendigkeit der Erhöhung der Rechte nicht genau vorhersagen können, erhalten Sie mit höherer Wahrscheinlichkeit eine Zustimmung für administrative Aufgaben, wenn dies nicht der Fall sein sollte.
-   **Erfordert minimalen Aufwand.** Tasks, für die Administratorrechte erforderlich sind, sollten so entworfen werden, dass eine einzelne Erweiterung erforderlich ist Aufgaben, die mehrere herauf Stufen erfordern, werden schnell mühsam.
-   **Kehren Sie zu den geringsten Berechtigungen zurück.** Wenn eine Aufgabe, für die Administratorrechte erforderlich sind, fertiggestellt ist, sollte das Programm in den geringsten Berechtigungs Status zurückversetzt werden.

**Task Ablauf für erhöhte Rechte**

Wenn eine Aufgabe eine Erhöhung erfordert, werden die folgenden Schritte ausgeführt:

1.  **Einstiegspunkt.** Aufgaben, die eine sofortige Erhöhung erfordern, wenn UAC vollständig aktiviert ist, haben Einstiegspunkte, die mit dem UAC-Schild gekennzeichnet sind In diesem Fall sollten Benutzer sofort nach dem Klicken auf solche Befehle eine Benutzeroberfläche für die Rechte Erweiterung sehen, und Sie sollten besonders vorsichtig sein, wenn Sie die Benutzeroberfläche für Rechte Erweiterungen von Aufgaben sehen, für die kein Schild vorhanden ist.

    ![Screenshot der UAC-schildsymbole und deren Bezeichnungen ](images/winenv-uac-image4.png)

    In diesem Beispiel ist für die System Steuerungselemente "Jugendschutz" und "Benutzerkonten" eine Erhöhung erforderlich.

    Wenn die Benutzerkontensteuerung teilweise aktiviert oder ausgeschaltet ist, wird das UAC-Schild immer noch angezeigt, um anzugeben, dass die Aufgabe Änderungen auf Systemebene umfasst und daher auch dann eine Erhöhung erfordert, wenn dem Benutzer die Benutzeroberfläche für die Rechte Erweiterung möglicherweise nicht angezeigt wird. Wenn das UAC-Schild immer für Aufgaben angezeigt wird, für die eine Erhöhung erforderlich ist, wird die Benutzeroberfläche einfach und

2.  **Trie.** Für geschützte Administratoren fordert der Task die Zustimmung mithilfe der Zustimmungs Benutzeroberfläche an. Für Standard Benutzer fordert der Task Administrator Anmelde Informationen über die Benutzeroberfläche für Anmelde Informationen an.

    ![Screenshot von zwei Arten der Erhöhung ](images/winenv-uac-image5.png)

    Diese Beispiele zeigen die Benutzeroberfläche für Anmelde Informationen und die Zustimmungs Benutzeroberfläche.

3.  **Separater Prozess mit erhöhten Rechten.** Intern wird ein neuer erhöhter Prozess erstellt, um die Aufgabe auszuführen.
4.  **Kehren Sie zu den geringsten Berechtigungen zurück.** Stellen Sie bei Bedarf die geringste Berechtigung wieder her, um alle Schritte auszuführen, für die keine Rechte Erweiterung erforderlich ist.

Beachten Sie, dass sich Aufgaben nicht mit erhöhten Zuständen "merken". Wenn der Benutzer z. b. in einem Assistenten zu einem Erweiterungs Einstiegspunkt hin-und hernavigiert, muss der Benutzer jedes Mal eine Rechte Erweiterung durchgeführt werden.

## <a name="usage-patterns"></a>Verwendungsmuster

Die Benutzerkontensteuerung hat mehrere Verwendungs Muster (in der bevorzugten Reihenfolge):

1.  **Arbeiten Sie für Standard Benutzer.** Entwerfen Sie das Feature für alle Benutzer, indem Sie den Gültigkeitsbereich auf den aktuellen Benutzer beschränken. Durch das Einschränken von Einstellungen auf den aktuellen Benutzer (im Gegensatz zur systemweiten) entfällt die Notwendigkeit, eine Benutzeroberfläche für die Rechte Erweiterung vollständig zu benötigen, und ermöglicht es den Benutzern, die Aufgabe abzuschließen.

    **Falsch:**

    ![Screenshot der Meldung: Sie haben keine Berechtigung. ](images/winenv-uac-image6.png)

    In diesem Beispiel mussten Windows XP-Benutzer über Administratorrechte verfügen, um die aktuelle Zeitzone anzuzeigen oder zu ändern.

    **Richtig:**

    ![Screenshot des Dialog Felds "Datum und Uhrzeit" ](images/winenv-uac-image7.png)

    In diesem Beispiel wurde die Zeit Zonen Funktion in Windows 7 und Windows Vista umgestaltet, damit Sie für alle Benutzer funktioniert.

2.  **Sie verfügen über separate Benutzeroberflächen Elemente für Standard Benutzer und Administratoren.** Trennen Sie Standard Benutzer Aufgaben eindeutig von Verwaltungsaufgaben. Gibt allen Benutzern Zugriff auf nützliche schreibgeschützte Informationen. Identifizieren Sie administrative Aufgaben mit dem UAC-Schild eindeutig.

    ![Grafik zum UAC-Schild, das erhöhte Rechte anzeigt ](images/winenv-uac-image8.png)

    In diesem Beispiel zeigt das System System Steuerungselement seinen Zustand für alle Benutzer an. das Ändern der systemweiten Einstellungen erfordert jedoch eine Erhöhung der Rechte.

3.  **Ermöglicht Standard Benutzern das Ausführen von Aufgaben und das erhöhen bei Fehlern.** Wenn Standard Benutzer die Informationen anzeigen können und einige Änderungen ohne erhöhte Rechte vornehmen können, erlauben Sie Ihnen den Zugriff auf die Benutzeroberfläche, und lassen Sie Sie nur erhöhen, wenn die Aufgabe fehlschlägt. Diese Vorgehensweise eignet sich, wenn Standard Benutzer eingeschränkten Zugriff haben, z. b. die Eigenschaften ihrer eigenen Dateien in Windows-Explorer. Sie eignet sich auch für Einstellungen auf der Seite "hybridhub" der Systemsteuerung.

    ![Screenshot der Meldung "Zugriff verweigert" ](images/winenv-uac-image9.png)

    In diesem Beispiel hat der Benutzer versucht, die Eigenschaften der Programmdatei zu ändern, hatte aber keine ausreichenden Berechtigungen. Der Benutzer kann eine Erhöhung durchführen und den Vorgang wiederholen.

4.  **Nur für Administratoren arbeiten.** Verwenden Sie diesen Ansatz nur für Administrator Funktionen und-Programme! Wenn eine Funktion nur für Administratoren vorgesehen ist (ohne Navigationspfade oder hilfreiche schreibgeschützte Informationen für Standard Benutzer), können Sie am Einstiegspunkt zum Eingeben von Administrator Anmelde Informationen auffordern, bevor Sie eine Benutzeroberfläche angezeigt werden. Verwenden Sie diesen Ansatz für langwierige Assistenten und [Seiten Flüsse](glossary.md) , wenn alle Pfade Administratorrechte erfordern.

    Wenn das gesamte Programm nur für Administratoren vorgesehen ist, markieren Sie es als Eingabeaufforderung zum Eingeben von Administrator Anmelde Informationen, um zu starten. Windows zeigt diese Programmsymbole mit der UAC-Schild Überlagerung an.

    ![Screenshot von Windows-Logo und UAC-Schild Überlagerung ](images/winenv-uac-image10.png)

    In diesem Beispiel benötigt das Programm Administratorrechte, um gestartet werden zu können.

## <a name="guidelines"></a>Richtlinien

### <a name="uac-shield-icon"></a>UAC-Schild Symbol

-   **Zeigen Sie Steuerelemente mit dem UAC-Schild an, um anzugeben, dass der Task eine sofortige Erhöhung erfordert, wenn UAC vollständig aktiviert ist,** auch wenn die Benutzerkontensteuerung aktuell nicht vollständig Wenn alle Pfade eines Assistenten und [Seiten Flusses](glossary.md) eine Erhöhung erfordern, zeigen Sie das UAC-Schild am Einstiegspunkt der Aufgabe an. Durch die ordnungsgemäße Verwendung des UAC-Shield können Benutzer Vorhersagen, wann eine Erhöhung erforderlich ist.
-   **Wenn das Programm mehrere Versionen von Windows unterstützt, zeigen Sie das UAC-Schild an, wenn mindestens eine Version eine Erhöhung erfordert.** Da für Windows XP keine Rechte Erweiterung erforderlich ist, sollten Sie ggf. die UAC-Schilde für Windows XP entfernen, wenn dies durchgängig und ohne Beeinträchtigung der Leistung möglich ist
-   **Zeigen Sie das UAC-Schild nicht für Aufgaben an, die in den meisten Kontexten keine Rechte erfordern.** Da dieser Ansatz in manchen Fällen irreführend ist, besteht der bevorzugte Ansatz darin, stattdessen einen ordnungsgemäß abgeschirmten kontextbezogenen Befehl zu verwenden.

    ![Screenshot der Fotodateien in Windows-Explorer ](images/winenv-uac-image11.png)

    Da der neue Ordner Befehl nur bei Verwendung in Systemordnern eine Erhöhung erfordert, wird er ohne UAC-Schild angezeigt.

-   Der UAC-Schild kann in den folgenden Steuerelementen angezeigt werden:

    **Befehls Schaltflächen:**

    ![Screenshot der Befehls Schaltfläche mit UAC-Schild Symbol ](images/winenv-uac-image12.png)

    Eine Befehls Schaltfläche, die eine sofortige Erhöhung erfordert.

    **Befehls Verknüpfungen:**

    ![Screenshot des Befehls Links mit dem UAC-Schild Symbol ](images/winenv-uac-image13.png)

    Ein Befehls Link, der eine sofortige Erhöhung der Rechte erfordert.

    **Verweist**

    ![Screenshot der Verknüpfung "Konto ändern" mit dem UAC-Schild ](images/winenv-uac-image14.png)

    Ein Link, der eine sofortige Erhöhung der Rechte erfordert.

    **Kreiert**

    ![Screenshot des Menüs mit UAC-Schild ](images/winenv-uac-image15.png)

    Ein Dropdown Menü, das eine sofortige Erhöhung der Rechte erfordert.

-   Da sich die Zustände von Tasks nicht in erhöhten Zuständen befinden, **Ändern Sie den UAC-Schild nicht in den Zustand.**
-   **Zeigen Sie das UAC-Schild auch dann an, wenn die Benutzerkontensteuerung ausgeschaltet wurde oder der Benutzer das integrierte Administrator Konto verwendet.** Die konsistente Anzeige des UAC-Shield ist leichter zu programmieren und bietet Benutzern Informationen über die Art der Aufgabe.

### <a name="elevation"></a>Elevation

-   **Wenn möglich, entwerfen Sie Aufgaben, die von Standard Benutzern ohne Rechte Erweiterung ausgeführt werden.** Gibt allen Benutzern Zugriff auf nützliche schreibgeschützte Informationen.
-   **Erhöhen Sie die Rechte pro Aufgabe und nicht pro Einstellung.** Kombinieren Sie die Standard Benutzereinstellungen nicht mit den administrativen Einstellungen in einer einzelnen Seite oder in einem Dialogfeld. Wenn Standard Benutzer z. b. einige, aber nicht alle Einstellungen ändern können, teilen Sie diese Einstellungen als separate Oberfläche auf der Benutzeroberfläche auf.

    **Falsch:**

    ![Screenshot von Einstellungen für Datum und Uhrzeit (Dialogfeld) ](images/winenv-uac-image16.png)

    In diesem Beispiel werden die Standard Benutzereinstellungen fälschlicherweise mit den administrativen Einstellungen vermischt.

    **Richtig:**

    ![Screenshot desselben Dialog Felds ohne UAC-Schild ](images/winenv-uac-image17.png)

    In diesem Beispiel befinden sich die Einstellungen zum Ändern des Datums und der Uhrzeit in einem separaten Dialogfeld, das nur für Administratoren verfügbar ist. Die Zeitzoneneinstellungen stehen Standard Benutzern zur Verfügung und sind nicht mit den administrativen Einstellungen gemischt.

-   **Berücksichtigen Sie nicht die Notwendigkeit, eine Erhöhung durchzusetzen, wenn Sie bestimmen, ob ein Steuerelement angezeigt oder deaktiviert werden soll.** Der Grund ist wie folgt:
    -   Nehmen Sie in nicht verwalteten Umgebungen an, dass Standard Benutzer eine Erhöhung durch einen Administrator durchgeführt haben. Durch das Deaktivieren von Steuerelementen, die eine Rechte Erweiterung erfordern, wird verhindert, dass Benutzer über Administratoren verfügen.
    -   Nehmen Sie in verwalteten Umgebungen an, dass Standard Benutzer überhaupt keine Rechte erhöhen können. Das Entfernen von Steuerelementen, die eine Erhöhung erfordern, würde verhindern, dass Benutzer wissen, wann die Suche beendet
-   **So vermeiden Sie unnötige Rechte:**
    -   **Wenn eine Aufgabe eine Erhöhung der Rechte erfordern kann, erhöhen Sie so spät wie möglich.** Wenn für eine Aufgabe eine [Bestätigung](mess-confirm.md)erforderlich ist, sollten Sie die Benutzeroberfläche für die Rechte Erweiterung erst anzeigen, wenn der Benutzer die Wenn eine Aufgabe immer eine Erhöhung erfordert, erhöhen Sie an Ihrem Einstiegspunkt.
    -   **Bleiben Sie nach der Erhöhung der Rechte erhöht, bis erweiterte Berechtigungen nicht mehr benötigt werden.** Benutzer sollten sich nicht mehrmals erhöhen müssen, um eine einzelne Aufgabe auszuführen.
    -   **Wenn Benutzer erhöhen müssen, um eine Änderung vorzunehmen, aber keine Änderungen vornehmen möchten, lassen Sie die Schaltflächen für positives Commit aktiviert, und behandeln Sie den Commit als abbrechen.** Dadurch wird verhindert, dass Benutzer nur zum Schließen eines Fensters erweitert werden.
    -   **Falsch:**
    -   ![Screenshot des Fensters, in dem nur eine Schaltfläche aktiv ist ](images/winenv-uac-image18.png)
    -   In diesem Beispiel ist die Schaltfläche "Änderungen speichern" deaktiviert, um eine unnötige Erhöhung zu vermeiden, wird jedoch aktiviert, wenn Benutzer die Auswahl ändern. Die Schaltfläche "deaktivierte Commit" sieht jedoch so aus, als ob Benutzer wirklich keine Auswahl haben.
-   **Zeigt keine Fehlermeldung an, wenn Aufgaben fehlschlagen, da die Benutzer die Erhöhung nicht erhöhen.** Angenommen, die Benutzer haben sich bewusst entschieden, nicht fortzufahren, sodass Sie diese Situation nicht als Fehler betrachten.

    **Falsch:**

    ![Screenshot der Meldung: die Wiederherstellung von Fabrikam kann nicht ausgeführt werden. ](images/winenv-uac-image19.png)

    In diesem Beispiel gibt die Fabrikam-Wiederherstellung fälschlicherweise eine Fehlermeldung aus, wenn der Benutzer entscheidet, nicht zu erhöhen.

-   **Zeigen Sie keine Warnungen an, um zu erläutern, dass Benutzer möglicherweise Ihre Berechtigungen zum Ausführen von Aufgaben erhöhen müssen.** Ermöglichen Sie es Benutzern, diese Tatsache selbst zu erkennen.
-   **Zeigen Sie die Benutzeroberfläche für UAC-Schild und-Rechte auf Grundlage der folgenden Tabelle an:**

    |                       |                                                                                                                                                                  |                                                                                                                                                                                                                       |                                                                                                      |
    |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **Object**      | **Umfelds**                                                                                                                                                | **Speicherort für UAC-Schild**                                                                                                                                                                               | **Zeitpunkt der Erhöhung**                                                                            |
    | Program<br/>    | Das gesamte Programm ist nur für Administratoren vorgesehen.<br/>                                                                                                            | ![Screenshot von Windows-Logo und UAC-Schild Überlagerung ](images/winenv-uac-image10.png)<br/> UAC-Schild Überlagerung auf Programmsymbol.<br/>                                                                       | Anzeigen der Benutzeroberfläche für die Rechte Erweiterung beim Start<br/>                                                           |
    | Get-Help<br/>    | Der gesamte Befehl ist nur für Administratoren vorgesehen.<br/>                                                                                                            | ![Screenshot des Links zum Ändern des Kontos und des UAC-Shield ](images/winenv-uac-image14.png)<br/> UAC-Schild auf Befehls Schaltfläche oder Link.<br/>                                                                      | Zeigen Sie die Benutzeroberfläche für die Rechte Erweiterung an, wenn auf die Befehls Schaltfläche oder den Link geklickt wird,<br/> |
    | Get-Help<br/>    | Der Befehl zeigt nützliche schreibgeschützte Informationen an, die für alle Benutzer geeignet sind, für Änderungen sind jedoch Administratorrechte erforderlich.<br/>                               | ![Screenshot des Links "Einstellungen ändern" und "UAC-Schild" ](images/winenv-uac-image8.png)<br/> UAC-Schild auf Befehls Schaltfläche oder Verknüpfung, um Änderungen vorzunehmen.<br/>                                                      | Zeigt die Benutzeroberfläche für die Rechte Erweiterung an, wenn auf die Befehls Schaltfläche geklickt wird<br/>         |
    | Get-Help<br/>    | Standard Benutzer können die Informationen anzeigen und ggf. einige Änderungen ohne Erhöhung vornehmen. erlauben Sie Standard Benutzern, zu versuchen, und bei einem Fehler zu erhöhen.<br/> | ![Screenshot des Fehlers mit dem UAC-Symbol auf der Schaltfläche "Wiederholen" ](images/winenv-uac-image9.png)<br/> Zeigen Sie den UAC-Schild nicht für den Befehl an, sondern zeigen Sie ihn für den Einstiegspunkt für die Erhöhung an, wenn der Befehl fehlschlägt.<br/> | Benutzeroberfläche für Rechte Erweiterung anzeigen, wenn der Benutzer den Befehl erneut versucht.<br/>                                       |
    | Task Schritt<br/>  | Alle nachfolgenden Schritte erfordern eine Erhöhung der Rechte.<br/>                                                                                                               | ![Screenshot der nächsten Befehls Schaltfläche mit UAC-Schild ](images/winenv-uac-image20.png)<br/> UAC-Schild für die Schaltfläche "weiter" (oder Äquivalent).<br/>                                                                | Anzeige der Benutzeroberfläche für die Rechte Erweiterung anzeigen, wenn auf die Schaltfläche "weiter"<br/>                         |
    | Task Schritt<br/>  | Einige branches erfordern eine Erhöhung der Rechte.<br/>                                                                                                                      | ![Screenshot der Befehls Verknüpfung mit dem UAC-Schild ](images/winenv-uac-image21.png)<br/> UAC-Schild für Befehls Verknüpfungen, die eine Erhöhung erfordern.<br/>                                                              | Anzeige der Rechte Erweiterung anzeigen, wenn auf Befehls Verknüpfungen mit UAC-Schild geklickt wird.<br/>                      |

    

     

### <a name="elevation-ui"></a>Rechte Erweiterung

-   **Wenn der Benutzer ein ungültiges Konto (Name oder Kennwort) oder keine Administratorrechte bereitstellt, zeigen Sie einfach die Benutzeroberfläche für Anmelde Informationen erneut an.** Zeigt keine Fehlermeldung an.
-   **Wenn der Benutzer die Benutzeroberfläche für Anmelde Informationen abbricht, müssen Sie den Benutzer wieder an die ursprüngliche Benutzeroberfläche zurückgeben.** Zeigt keine Fehlermeldung an.
-   Wenn die Benutzerkontensteuerung ausgeschaltet wurde und ein Standard Benutzer versucht, eine Aufgabe auszuführen, für die erhöhte Rechte erforderlich sind, geben Sie eine Fehlermeldung mit dem Hinweis an, dass dieser Task Administratorrechte erfordert. Um diese Aufgabe auszuführen, müssen Sie sich mit einem Administrator Konto anmelden. "

![Screenshot der Aufgabe "erfordert eine Berechtigungs Meldung" ](images/winenv-uac-image22.png)

In diesem Beispiel wurde die Benutzerkontensteuerung deaktiviert, sodass in einer Fehlermeldung erläutert wird, dass der Benutzer ein Administrator Konto verwenden muss.

### <a name="wizards"></a>Assistenten

-   **Erhöhen Sie nicht mehrmals.** Sobald ein Assistent erhöht wird, sollte er erhöht werden.
-   Wenn die Aufgabe innerhalb des Assistenten ausgeführt wird, platzieren Sie ein UAC-Schild auf der Schaltfläche "weiter" der Commit-Seite (die eine spezifischere [Bezeichnung](win-wizards.md)erhalten sollte). Wenn der Benutzer einen Commit ausführt:
    -   Wenn die nächste Seite eine Statusseite ist, wechseln Sie zu dieser Seite, und zeigen Sie die Benutzeroberfläche für die Rechte Erweiterung modal an. Führen Sie nach erfolgreicher Erhöhung der Erweiterung die Aufgabe aus.
    -   Wenn die nächste Seite eine Vervollständigungs Seite ist, fahren Sie mit der Seite fort (ersetzen Sie den Inhalt vorübergehend durch "warten auf Berechtigungen..."), und zeigen Sie die Benutzeroberfläche für die Rechte Erweiterung modal an. Führen Sie nach erfolgreicher Erweiterung die Aufgabe aus, und zeigen Sie dann den Inhalt der Vervollständigungs Seite an.
    -   Wenn der Benutzer die Benutzeroberfläche für die Rechte Erweiterung abbricht, kehren Sie zur Seite Commit zurück. Auf diese Weise kann der Benutzer den Vorgang erneut versuchen.
-   Wenn die Aufgabe ausgeführt wird, nachdem der Assistent abgeschlossen ist, platzieren Sie ein UAC-Schild auf der Schaltfläche "Fertigstellen" der commitseite (die eine spezifischere [Bezeichnung](win-wizards.md)erhalten sollte). Wenn der Benutzer einen Commit ausführt:
    -   Bleiben Sie auf der Seite Commit, und zeigen Sie die Benutzeroberfläche für die Rechte Erweiterung modal an Schließen Sie den Assistenten nach der erfolgreichen Erhöhung der Rechte.
    -   Wenn der Benutzer die Benutzeroberfläche für die Rechte Erweiterung abbricht, kehren Sie zur Seite Commit zurück. Auf diese Weise kann der Benutzer den Vorgang erneut versuchen.
-   Für lange Assistenten, die nur für Administratoren vorgesehen sind, können Sie am Einstiegspunkt zum Eingeben von Administrator Anmelde Informationen auffordern, bevor Sie eine Benutzeroberfläche angezeigt werden.

## <a name="text"></a>Text

-   **Verwenden Sie nur dann ein Ellipsen, weil für einen Befehl eine Erhöhung erforderlich ist.** Die Notwendigkeit einer Erhöhung der Rechte wird durch das UAC-Schild angegeben.

## <a name="documentation"></a>Dokumentation

Beim Verweis auf die Benutzerkontensteuerung:

-   Weitere Informationen finden Sie unter Benutzerkontensteuerung (bei der ersten Erwähnung) oder UAC (bei späterer Erwähnung), nicht mit dem geringsten Benutzerkonto oder Lua.
-   Weitere Informationen finden Sie unter nicht-Administratoren als Standard Benutzer.
-   Weitere Informationen finden Sie unter integrierte Computer Administratoren als integrierte Administratoren.

In der Benutzerdokumentation:

-   Weitere Informationen finden Sie unter Erteilen der Zustimmung zum Ausführen einer administrativen Aufgabe als erteilen der Berechtigung.

In der Programmierung und in anderen technischen Dokumentationen:

-   Weitere Informationen finden Sie unter Erteilen der Zustimmung zum Ausführen einer administrativen Aufgabe als Erhöhung.
-   Im Zusammenhang mit der Benutzerkontensteuerung können Sie Administratoren als geschützte Administratoren bei nicht erhöhten Rechten und erhöhte Administratoren nach der Erhöhung der Rechte entnehmen.
-   Lesen Sie das Dialogfeld zum Eingeben von Kenn Wörtern als Anmelde Informationen-Benutzeroberfläche. Lesen Sie das Dialogfeld, das verwendet wird, um der Zustimmungs Benutzeroberfläche die Zustimmung zu erteilen. Im Allgemeinen wird die Benutzeroberfläche für die Rechte Erweiterung bezeichnet.


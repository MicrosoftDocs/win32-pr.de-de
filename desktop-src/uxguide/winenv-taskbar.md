---
title: Taskleiste
description: Die Taskleiste ist der Zugriffspunkt für Programme, die auf dem Desktop angezeigt werden. Mit den neuen Funktionen der Windows 7-Taskleiste können Benutzer Befehle bereitstellen, auf Ressourcen zugreifen und den Programmstatus direkt über die Taskleiste anzeigen.
ms.assetid: c00e558a-313f-4741-a4b2-7d738f4544fa
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f8b2bc21a75bc11c43df2cbdd37381165b89a793
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104551576"
---
# <a name="taskbar"></a>Taskleiste

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Die Taskleiste ist der Zugriffspunkt für Programme, die auf dem Desktop angezeigt werden. Mit den neuen Funktionen der Windows 7-Taskleiste können Benutzer Befehle bereitstellen, auf Ressourcen zugreifen und den Programmstatus direkt über die Taskleiste anzeigen.

Die Taskleiste ist der Zugriffspunkt für Programme, die auf dem Desktop angezeigt werden, selbst wenn das Programm minimiert ist. Solche Programme werden als Desktop Präsenz bezeichnet. Mithilfe der Taskleiste können Benutzer die geöffneten primären Fenster und bestimmte sekundäre Fenster auf dem Desktop anzeigen und schnell zwischen den Fenstern wechseln.

![Screenshot der Taskleiste mit den aufgerufenen Features ](images/winenv-taskbar-image1.png)

Die Microsoft Windows-Taskleiste.

Die Steuerelemente auf der Taskleiste werden als Task leisten Schaltflächen bezeichnet. Wenn ein Programm ein primäres Fenster (oder ein sekundäres Fenster mit bestimmten Merkmalen) erstellt, fügt Windows eine Task leisten Schaltfläche für dieses Fenster hinzu und entfernt diese, wenn dieses Fenster geschlossen wird.

Für Windows 7 entwickelte Programme können diese neuen Features der Task leisten-Schaltfläche nutzen:

-   Sprung Listen ermöglichen den schnellen Zugriff auf häufig verwendete Ziele (z. b. Dateien, Ordner und Verknüpfungen) und Befehle über ein Kontextmenü, auf das über die Task leisten Schaltfläche des Programms und das Startmenü Element zugegriffen werden kann, selbst wenn das Programm nicht ausgeführt wird.
-   Miniatur Ansichts Symbolleisten ermöglichen den schnellen Zugriff auf häufig verwendete Befehle für ein bestimmtes Fenster. Miniatur Ansichts Symbolleisten werden in der Miniaturansicht der Taskleiste angezeigt.
-   Überlagerungs Symbole zeigen die Statusänderung auf dem Symbolleisten Symbol der Taskleiste des Programms an.
-   Status leisten zeigen den Fortschritt für Aufgaben mit langer Ausführungszeit auf der Task leisten Schaltfläche des Programms an.
-   Mithilfe der Schaltflächen für die Taskleiste Unterfenster können Benutzer mithilfe von Schaltflächen Miniaturansichten auf der Taskleiste direkt zu Fenster Registerkarten, Projekt Fenstern, untergeordneten Fenstern von Multiple Document Interface (MDI) und sekundären Fenstern wechseln.
-   Mit angehefteten Task leisten Schaltflächen können Benutzerprogramm Schaltflächen an die Taskleiste anheften, um schnell auf Programme zuzugreifen, auch wenn Sie nicht ausgeführt werden.

Technisch gesehen umfasst die Taskleiste den gesamten Balken von der Start Schaltfläche bis zum Benachrichtigungsbereich. Üblicherweise verweist die Taskleiste auf den Bereich, der die Schaltflächen der Taskleiste enthält. Bei Konfigurationen mit mehreren Monitoren verfügt nur ein Monitor über eine Taskleiste, und dieser Monitor ist der Standard Monitor.

**Hinweis:** Die Richtlinien im Zusammenhang mit [Desktop](winenv-desktop.md), [Benachrichtigungsbereich](winenv-notification.md)und [Fensterverwaltung](win-window-mgt.md) werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Für Windows 7 entwickelte Programme können diese Funktionen der Task leisten-Schaltfläche nutzen. Stellen Sie sich die folgenden wichtigen Fragen, um zu bestimmen, ob Sie Sie verwenden möchten:

**Sprung Listen**

-   **Müssen Benutzer häufig neue Aufgaben mit Ihrem Programm starten?** Wenn dies der Fall ist, sollten Sie eine Sprung Liste bereitstellen. Sprung Listen können auch für andere Zwecke verwendet werden. in den meisten Szenarien ist jedoch das Starten einer neuen Aufgabe enthalten.
-   **Benötigen Benutzer häufig oder häufig verwendete Dateien, Ordner, Links oder andere Ressourcen?** Wenn dies der Fall ist, sollten Sie eine Sprung Liste angeben, um auf diese nützlichen Ressourcen zuzugreifen.

    ![Screenshot der Taskleiste mit der Sprung Liste von Internet Explorer ](images/winenv-taskbar-image2.png)

    In diesem Beispiel verwendet Windows Internet Explorer eine Sprung Liste, um häufig besuchte Seiten zu präsentieren.

-   **Benötigen Benutzer bei der Verwendung anderer Programme häufig schnellen Zugriff auf eine kleine Anzahl von Befehlen Ihres Programms, auch wenn das Programm nicht ausgeführt wird?** Wenn dies der Fall ist, sollten Sie eine Sprung Liste mit diesen häufig verwendeten Befehlen bereitstellen. Diese Befehle müssen auch dann funktionieren, wenn das Programm nicht ausgeführt wird und auf das gesamte Programm und nicht auf ein bestimmtes Fenster angewendet werden muss. Als Alternative empfiehlt es sich, eine Miniaturansicht für Befehle bereitzustellen, die auf ein bestimmtes Fenster angewendet werden.

    ![Screenshot der Taskleiste mit der Sprung Liste für kurz Notizen ](images/winenv-taskbar-image3.png)

    In diesem Beispiel können Benutzer mit dem Kurznotizen Zubehör einen neuen Hinweis schnell erstellen, während Sie andere Programme verwenden.

-   **Fördern Sie neue, einmalige Verwendung oder schwer zu suchende Features?** Wenn dies der Fall ist, verwenden Sie keine Sprung Listen, da Sie für diesen Zweck nicht vorgesehen sind. Stattdessen sollten Sie die Auffindbarkeit solcher Befehle direkt im Programm verbessern.

**Miniatur Ansichts Symbolleisten**

Gelten alle folgenden Bedingungen?

-   **Gelten die Befehle für ein bestimmtes Fenster?** Miniatur Ansichts Symbolleisten sind für Befehle, die für vorhandene Aufgaben gelten, während Sprung Listen Befehle zum Starten neuer Aufgaben dienen.
-   **Müssen Benutzer bei der Verwendung anderer Programme schnell mit einer laufenden Aufgabe interagieren?** Wenn dies der Fall ist, sind Miniatur Ansichts Symbolleisten eine gute Wahl. Miniatur Ansichts-Symbolleisten können maximal sieben Befehle enthalten, aber im Allgemeinen werden maximal fünf Befehle bevorzugt.
-   **Sind die Befehle sofort?** Das heißt, Sie benötigen keine zusätzlichen Eingaben? Miniatur Ansichts-Symbolleisten müssen über sofortige Befehle verfügen, um effizient zu sein, während Sprung Listen mit Befehlen, die zusätzliche Eingaben erfordern, besser funktionieren.

    **Falsch:**

    ![Screenshot der Taskleiste mit überlappenden Fenstern ](images/winenv-taskbar-image4.png)

    Befehle, die zusätzliche Eingaben erfordern, funktionieren nicht gut auf Miniatur Ansichts Symbolleisten.

-   **Sind die Befehle direkt?** Das heißt, können Benutzer mit Ihnen mit einem einzigen Mausklick interagieren? Symbolleisten müssen direkt Befehle aufweisen, damit Sie effizient sind.
-   **Werden die Befehle gut durch Symbole dargestellt?** Symbolleisten Befehle für Miniaturansichten werden mithilfe von Symbolen, nicht Text Bezeichnungen, angezeigt, während Sprung Listen Befehle durch Text Beschriftungen dargestellt werden.

    **Falsch:**

    ![Screenshot des Miniatur Ansichts Befehls mit dem Symbol ](images/winenv-taskbar-image5.png)

    In diesem Beispiel wird der Befehl nicht gut durch Symbole dargestellt.

**Überlagerungs Symbole**

-   **Hat das Programm "Desktop Präsenz"?** Wenn dies nicht der gibt, verwenden Sie stattdessen ein Benachrichtigungs Bereichs Symbol. Wenn dies der Fall ist, sollten Sie ein Überlagerungs Symbol verwenden, anstatt den Status im Info Bereichs Symbol für Programme für Windows 7 zu platzieren. Dadurch wird sichergestellt, dass das Symbol immer sichtbar ist (bei Verwendung von großen Symbolen), und das Programm wird mit seinem Status an einem Ort konsolidiert.
-   **Wird das Überlagerungs Symbol temporär angezeigt, um eine Statusänderung anzuzeigen?** Wenn dies der Fall ist, kann ein Überlagerungs Symbol geeignet sein, je nach den folgenden Faktoren:
    -   **Ist der Status hilfreich und relevant bei der Verwendung anderer Programme?** Wenn dies nicht der Wert ist, zeigen Sie die Informationen in den [Status leisten](ctrl-status-bars.md) des Programms oder in einem anderen Programmstatus an.

        ![Screenshot der Fenster Statusleiste von Internet Explorer ](images/winenv-taskbar-image7.png)

        In diesem Beispiel wird die Statusleiste verwendet, da der Status bei der Verwendung anderer Programme nicht hilfreich ist.

    -   **Wird der Status angezeigt?** Wenn dies der Fall ist, verwenden Sie stattdessen eine Statusleiste der Taskleiste.
    -   **Ist der Status kritisch? Ist eine sofortige Aktion erforderlich?** Wenn dies der Fall ist, zeigen Sie die Informationen so an, dass Sie beachtet werden und nicht einfach ignoriert werden können, z. b. ein [Dialogfeld](win-dialog-box.md).

**Status anzeigen**

-   **Ist das Fortschritts Feedback hilfreich und relevant bei der Verwendung anderer Programme?** Das heißt, Benutzer können den Fortschritt bei der Verwendung anderer Programme wahrscheinlich überwachen und ihr Verhalten als Ergebnis ändern? Dieser nützliche und relevante Status wird normalerweise im Dialogfeld "nicht modalstatus" oder auf einer dedizierten Statusseite angezeigt, jedoch nicht mit einem ausgelasteten Zeiger, Aktivitätsindikator oder Statusleiste auf einer Statusleiste. Wenn der Status bei der Verwendung anderer Programme nicht hilfreich ist, zeigen Sie einfach das Fortschritts Feedback direkt im Programm an.

    **Richtig:**

    ![Screenshot des Dialog Felds "Kopieren" mit Statusanzeige ](images/winenv-taskbar-image8.png)

    **Falsch:**

    ![Screenshot der Statusanzeige auf der Task leisten Schaltfläche ](images/winenv-taskbar-image9.png)

    Im falschen Beispiel ist die Statusleiste der Taskleiste nicht sehr nützlich.

-   **Ist die Aufgabe kontinuierlich?** Wenn die Aufgabe nie abgeschlossen wird, muss der Fortschritt nicht angezeigt werden. Beispiele für fortlaufende Aufgaben sind Antivirenscans, die nicht von Benutzern initiiert werden, und die Datei Indizierung.

    **Falsch:**

    ![Screenshot des Fortschritts Symbols einer kontinuierlichen Aufgabe ](images/winenv-taskbar-image10.png)

    In diesem Beispiel muss ein fortlaufender Task den Fortschritt nicht anzeigen.

**Unterfenster-Task leisten**

-   **Enthält Ihr Programm Registerkarten, Projektfenster, untergeordnete MDI-Fenster oder sekundäre Fenster, auf die Benutzer häufig direkt umsteigen möchten?** Wenn dies der Fall ist, können Sie für diese Windows-Schaltflächen Miniaturansichten geeignet sein.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="using-jump-lists-and-thumbnail-toolbars-effectively"></a>Effektive Verwendung von Sprung Listen und Miniatur Ansichts Symbolleisten

Sprung Listen und Miniaturansicht-Symbolleisten helfen Benutzern, auf Ressourcen zuzugreifen und Befehle effizienter auszuführen. Wenn Sie jedoch entwerfen, wie Ihr Programm diese Features unterstützt, nehmen Sie keine verbesserte Effizienz für die Gewährung vor. Wenn Benutzer nicht genau vorhersagen können, welches Feature den Befehl hat, den Sie benötigen, oder mehrere Orte überprüfen müssen, werden die Benutzer schließlich frustriert und können diese Features nicht mehr verwenden.

Sprung Listen und Miniatur Ansichts Symbolleisten arbeiten am effektivsten zusammen, wenn Sie Folgendes sind:

-   **Eindeutig differenziert.** Benutzer wissen, wann Sie in einer Sprung Liste nach einem Ziel oder Befehl Suchen und wann Sie in einer Miniaturansicht auf der Symbolleiste suchen müssen. Es gibt eine klare Aufgabe für jeden, sodass Benutzer den Inhalt der beiden selten verwechseln. Im Allgemeinen werden Sprung Listen zum Starten neuer Aufgaben verwendet, während bei der Verwendung anderer Programme Miniatur Ansichts-Symbolleisten verwendet werden, um mit laufenden Aufgaben zu interagieren.
-   **Lichem.** Die angebotenen Ziele und Befehle sind diejenigen, die von Benutzern benötigt werden. Wenn Benutzer wahrscheinlich nichts benötigen, ist Sie nicht enthalten. Verwenden Sie die maximale Anzahl von Elementen nicht, wenn Sie nicht benötigt werden.
-   **Vorhersagbare.** Die angebotenen Ziele und Befehle sind diejenigen, die von Benutzern erwartet werden. Benutzer müssen selten an mehr als einem Ort suchen.
-   **Gut organisiert.** Benutzer können schnell feststellen, was Sie suchen. Sie verwenden beschreibende, aber präzise Bezeichnungen und geeignete Symbole, um die Erkennung zu unterstützen.

Stellen Sie sicher, dass Sie eine Benutzer Recherche durchführen, um sicherzustellen, dass Sie richtig ist. Wenn Sie letztendlich feststellen, dass Sie keine Sprung Listen und Symbolleisten für die Miniaturansicht erstellen können, um diese Ziele zu erreichen, sollten Sie nur eine davon bereitstellen. Es ist besser, eine vorhersagbare Möglichkeit zu haben, Befehle als zwei verwirrende Befehle zu erhalten.

## <a name="guidelines"></a>Richtlinien

### <a name="taskbar-buttons"></a>Task leisten Schaltflächen

-   **Nehmen Sie die folgenden Fenstertypen auf der Taskleiste auf (für Windows 7, indem Sie eine Miniaturansicht der Taskleiste verwenden):**
    -   Primäre Fenster (einschließlich Dialogfeldern ohne Besitzer)
    -   Eigenschaftenblätter
    -   Dialogfelder mit nicht modalem Status
    -   Assistenten
-   **Verwenden Sie für Windows 7 die Schaltflächen Miniaturansichten der Taskleiste, um die folgenden Fenstertypen mit der Schaltfläche für das primäre Fenster der Taskleiste zu gruppieren, von der aus** Jedes Programm (insbesondere jedes Programm, das als separates Programm wahrgenommen wird) sollte über eine einzige Task leisten Schaltfläche verfügen.

    -   Sekundäre Fenster
    -   Arbeitsbereichs Registerkarten
    -   Projektfenster
    -   Untergeordnetes MDI-Fenster

    **Richtig:**

    ![Screenshot von Windows-Explorer und Statusanzeige ](images/winenv-taskbar-image11.png)

    In diesem Beispiel wird ein sekundäres Fenster mit der Task leisten Schaltfläche des primären Fensters gruppiert.

    **Falsch:**

    ![Screenshot von Windows-Explorer und der Systemsteuerung ](images/winenv-taskbar-image12.png)

    In diesem Beispiel ist die Systemsteuerung nicht ordnungsgemäß mit Windows-Explorer gruppiert. Benutzer nehmen diese als separate Programme an.

    **Falsch:**

    ![Screenshot des Programms, der Statusanzeige und einer Taskleiste ](images/winenv-taskbar-image13.png)

    In diesem Beispiel verwendet Windows Backup fälschlicherweise zwei Task leisten Schaltflächen für ein einzelnes Programm.

-   Beim **Wiederherstellen eines primären Fensters sollten auch alle zugehörigen sekundären Fenster wieder hergestellt werden,** selbst wenn diese sekundären Fenster über eigene Task leisten Schaltflächen verfügen. Platzieren Sie bei der Wiederherstellung sekundäre Fenster oberhalb des primären Fensters.
-   **Für Windows 7 können Programme, die normalerweise über Desktop Präsenz verfügen, vorübergehend eine Task leisten Schaltfläche anzeigen, um den Status anzuzeigen.** Dies ist nur möglich, wenn das Programm normalerweise auf dem Desktop angezeigt wird und Benutzer häufig mit dem Programm interagieren. Ein Programm, das normalerweise ohne Desktop Präsenz ausgeführt wird, sollte stattdessen sein Benachrichtigungs Bereichs Symbol verwenden, obwohl es möglicherweise nicht immer sichtbar ist.

    **Falsch:**

    ![Screenshot der Schaltfläche "Windows Sync Center-Taskleiste" ](images/winenv-taskbar-image14.png)

    In diesem Beispiel verwendet Windows Sync Center fälschlicherweise eine temporäre Task leisten Schaltfläche, um den Status anzuzeigen. Stattdessen sollte das Benachrichtigungs Bereichs Symbol verwendet werden.

### <a name="icons"></a>Symbole

-   **Entwerfen Sie das Programmsymbol so, dass es auf der Taskleiste hervorragend aussieht.** Stellen Sie sicher, dass Sie sinnvoll ist und ihre Funktion und Ihre Marke widerspiegelt. Machen Sie es eindeutig, machen Sie es speziell, und stellen Sie sicher, dass es in allen Symbolgrößen gut rendert. Nehmen Sie die Zeit, die Sie benötigen, um es zu korrigieren. Befolgen Sie die [Richtlinien für das Aero-Stilsymbol](vis-icons.md).
-   **Wenn das Programm Überlagerungs Symbole verwendet, entwerfen Sie das Basis Symbol Ihres Programms, um die Überlagerungen zu verarbeiten.** Die Überlagerungs Symbole werden in der unteren rechten Ecke angezeigt. entwerfen Sie also das Symbol, damit der Bereich verdeckt werden kann.

    ![Screenshot von Symbolen und mit niedrigerer Überlagerung ](images/winenv-taskbar-image15.png)

    In diesem Beispiel enthält das Symbol für die Taskleiste der Taskleiste des Programms keine wichtigen Informationen im unteren rechten Bereich.

-   **Verwenden Sie keine Überlagerungen im Basis Symbol Ihres Programms,** unabhängig davon, ob das Programm Überlagerungs Symbole verwendet oder nicht. Die Verwendung einer Überlagerung im Basis Symbol ist verwirrend, da die Benutzer herausfinden müssen, dass der Status nicht kommuniziert.

    **Falsch:**

    ![Screenshot des Basis Symbols mit Overlay ](images/winenv-taskbar-image16.png)

    In diesem Beispiel sieht das Basis Symbol des Programms so aus, als ob es den Status anzeigt.

Allgemeine Symbol Richtlinien und Beispiele finden Sie unter [Symbole](vis-icons.md).

### <a name="overlay-icons"></a>Überlagerungs Symbole

-   **Verwenden Sie Überlagerungs Symbole, um nur einen nützlichen und relevanten Status anzugeben.** Beachten Sie, dass ein Überlagerungs Symbol eine potenzielle Unterbrechung der Arbeit des Benutzers darstellen kann. Daher muss die Statusänderung wichtig genug sein, um eine mögliche Unterbrechung zu verdienen.

    **Falsch:**

    ![Screenshot von drei Überlagerungs Symbolen ](images/winenv-taskbar-image17.png)

    In diesen Beispielen ist das Überlagerungs Symbol nicht wichtig genug, um eine mögliche Unterbrechung zu verdienen.

-   **Verwenden Sie Überlagerungs Symbole für den temporären Status.** Die Überlagerungs Symbole verlieren ihren Wert, wenn Sie ständig angezeigt werden, sodass der normale Programmstatus kein Symbol anzeigen kann. Entfernen Sie das Überlagerungs Symbol, wenn das Symbol:

    -   **Liegt bei einem Problem:** Entfernen Sie das Symbol, sobald das Problem gelöst wurde.
    -   **Warnungen, dass etwas Neues ist:** Entfernen Sie das Symbol, sobald der Benutzer das Programm aktiviert hat.

    **Ausnahme:** Das Programm kann ständig ein Überlagerungs Symbol anzeigen, wenn Benutzer den Status immer kennen müssen.

    ![Screenshot von Live Messenger mit Überlagerungs Symbol ](images/winenv-taskbar-image18.png)

    In diesem Beispiel zeigt Windows Live Messenger immer ein Überlagerungs Symbol an, sodass Benutzer ihre gemeldete Anwesenheit immer überprüfen können.

-   **Zeigen Sie kein Symbol an, um anzugeben, dass ein Problem gelöst wurde.** Entfernen Sie stattdessen einfach alle vorherigen Symbole, die auf ein Problem hinweisen. Angenommen, die Benutzer erwarten, dass Ihr Programm ohne Probleme ausgeführt wird.
-   **Zeigen Sie entweder Überlagerungs Symbole oder Benachrichtigungs Bereichs Symbole an, aber nicht beides.** Das Programm kann beide Mechanismen aus Gründen der Abwärtskompatibilität unterstützen, aber wenn Ihr Programm den Status mithilfe von Überlagerungs Symbolen anzeigt, sollte es nicht auch Benachrichtigungs Bereichs Symbole für den Status verwenden.

    **Falsch:**

    ![Screenshot der Taskleiste, bei der das Symbol zweimal angezeigt wird ](images/winenv-taskbar-image19.png)

    In diesem Beispiel wird das Symbol für die neue e-Mail redundant angezeigt.

-   **Klicken Sie nicht auf die Schaltfläche "Taskleiste", um eine Statusänderung zu zeichnen.** Dies wäre zu ablenkend. Ermöglichen Sie Benutzern, über Lagerungs Symbole selbst zu erkennen.
-   **Standard-Überlagerungs Symbole bevorzugen, um Status-oder Statusänderungen anzugeben.** Verwenden Sie diese standardüberlagerungs Symbole: 

    |                                                                                                   |                                  |
    |---------------------------------------------------------------------------------------------------|----------------------------------|
    | **Überlagerung**<br/>                                                                            | **Status**<br/>            |
    | ![Screenshot des kleinen Warn Symbols ](images/winenv-taskbar-image20.png)<br/>               | Warnung<br/>               |
    | ![Screenshot des kleinen Fehler Symbols ](images/winenv-taskbar-image21.png)<br/>                 | Fehler<br/>                 |
    | ![Screenshot des kleinen deaktivierten/getrennten Symbols ](images/winenv-taskbar-image22.png)<br/> | Deaktiviert/getrennt<br/> |
    | ![Screenshot eines kleinen blockierten/Offline-Symbols ](images/winenv-taskbar-image23.png)<br/>       | Blockiert/offline<br/>       |

    

     

-   **Wählen Sie für benutzerdefinierte Überlagerungs Symbole einen leicht erkennbaren Entwurf aus.** Verwenden Sie hochwertige 16x16-Pixel-Symbole mit Vollfarben. Symbole mit besonderen Gliederungen über quadratische oder rechteckige förmige Symbole bevorzugen. Wenden Sie auch die anderen [Aero-Stil-Richtlinien](vis-icons.md) an.
-   **Lassen Sie das Design von benutzerdefinierten Überlagerungs Symbolen einfach.** Versuchen Sie nicht, komplexe, unbekannte oder abstrakte Ideen zu kommunizieren. Wenn Sie sich kein geeignetes benutzerdefiniertes Symbol vorstellen können, verwenden Sie stattdessen ein Standard symbolfehler-oder Warnsymbol. Diese Symbole können effektiv verwendet werden, um viele Arten von Status zu kommunizieren.
-   **Ändern Sie den Status nicht zu häufig.** Überlagerungs Symbole sollten nicht laut, instabil oder nach Bedarf angezeigt werden. Das Auge ist von den Änderungen im Peripherie Feld der Vision abhängig, sodass Statusänderungen gering sein müssen.
    -   **Ändern Sie das Symbol nicht schnell.** Wenn sich der zugrunde liegende Status schnell ändert, lassen Sie das Symbol den Status auf hoher Ebene widerspiegeln.

        **Falsch:**

        ![Screenshot des Überlagerungs Symbols in zwei Zuständen ](images/winenv-taskbar-image24.png)

        In diesem Beispiel erfordert das schnell veränderliche Überlagerungs Symbol Aufmerksamkeit.

    -   **Verwenden Sie keine Animationen.** Dies ist zu stark ablenkend.
    -   **Blinken Sie das Symbol nicht.** Dies ist zu stark ablenkend. Wenn ein Ereignis sofortige Aufmerksamkeit erfordert, verwenden Sie stattdessen ein Dialogfeld. Wenn das Ereignis anderweitig Eingreifen erfordert, verwenden Sie eine Benachrichtigung.

### <a name="taskbar-button-flashing"></a>Task leisten Schaltfläche blinkt

-   **Verwenden Sie die Symbolleisten Schaltfläche für die Taskleiste, um die sofortige Aufmerksamkeit des Benutzers auf die Ausführung einer laufenden Aufgabe zu fordern.** Es ist für die Benutzer schwierig, sich zu konzentrieren, während eine Task leisten Schaltfläche blinkt. gehen Sie also davon aus, dass Sie die Aktionen unterbrechen, die Sie durchführen. Das Blinken einer Task leisten Schaltfläche ist besser als das stehlen des Eingabefokus, aber blinkende Task leisten Schaltflächen sind weiterhin sehr eindringlich. Stellen Sie sicher, dass die Unterbrechung gerechtfertigt ist, z. b., um anzugeben, dass der Benutzer vor dem Schließen eines Fensters Daten speichern muss. Inaktive Programme sollten selten sofortige Aktionen erfordern. Klicken Sie nicht auf die Schaltfläche "Taskleiste", wenn der Benutzer nur das Programm aktivieren, eine Nachricht lesen oder eine Statusänderung sehen muss.
-   **Wenn sofortige Aktionen nicht erforderlich sind, sollten Sie diese alternativen beachten:**
    -   Verwenden Sie eine [Aktions Erfolgs Benachrichtigung](mess-notif.md) , um anzugeben, dass eine Aufgabe abgeschlossen wurde.
    -   Sie unternehmen nichts. Warten Sie, bis Benutzer an dem problemteil nehmen, wenn Sie das Programm das nächste Mal aktivieren. Dies ist oft die beste Wahl.
-   **Wenn ein inaktives Programm sofortige Aufmerksamkeit erfordert, können Sie die Task leisten Schaltfläche ablegen, um die Aufmerksamkeit zu zeichnen und diese hervorzuheben.** Führen Sie nichts anderes aus: Wiederherstellen oder aktivieren Sie das Fenster nicht, und spielen Sie keine Soundeffekte. Beachten Sie stattdessen die Fenster Zustands Auswahl des Benutzers, und lassen Sie den Benutzer das Fenster aktivieren, wenn Sie bereit sind.
-   **Bei sekundären Fenstern mit einer Task leisten Schaltfläche können Sie die zugehörige Schaltfläche anstelle der Task leisten Schaltfläche des primären Fensters blinken.** Auf diese Weise können Benutzer direkt am Fenster teilnehmen.
-   **Bei sekundären Fenstern, die nicht über eine Task leisten Schaltfläche verfügen, können Sie die Task leisten Schaltfläche des primären Fensters blinken und das sekundäre Fenster auf allen anderen Fenstern für dieses Programm aufrufen.** Sekundäre Fenster, für die eine Aufmerksamkeit erforderlich ist, müssen am meisten sein, um sicherzustellen, dass Sie von Benutzern
-   **Nur eine Task leisten Schaltfläche für ein Fenster gleichzeitig blinken.** Das Blinken von mehr als einer Schaltfläche ist unnötig und zu ablenkend.
-   **Entfernen Sie die Symbolleisten Schaltfläche, sobald das Programm aktiv wird.**
-   **Wenn das Programm aktiv wird, sollten Sie sicherstellen, dass es offensichtlich ist.** In der Regel wird dieses Ziel erreicht, indem ein Dialogfeld angezeigt wird, das eine Frage stellt oder eine Aktion initiiert.

### <a name="quick-launch-shortcuts"></a>Tastenkombinationen für Schnellstarts

-   **Legen Sie Programm Verknüpfungen nur dann im schnell Startbereich ab, wenn sich die Benutzer anmelden.** Da der Schnellstart von Windows 7 entfernt wurde, sollten Programme, die für Windows 7 entwickelt wurden, keine Programm Verknüpfungen zum Schnellstartbereich hinzufügen oder entsprechende Optionen bereitstellen.

### <a name="jump-lists"></a>Sprung Listen

**Design**

-   **Entwerfen Sie Sprung Listen, um die Ziele ihrer Benutzer für Ihre täglichen Aufgaben zu erfüllen.** Berücksichtigen Sie dabei Folgendes:
    -   **Der Zweck Ihres Programms.** Stellen Sie sich vor, was Benutzer wahrscheinlich als nächstes tun. Bei Dokumenten Erstellungs Programmen werden Benutzer wahrscheinlich zu kürzlich verwendeten Dokumenten zurückkehren. Für Programme, in denen vorhandener Inhalt angezeigt wird, möchten Benutzer möglicherweise auf häufig verwendete Ressourcen zugreifen. Bei anderen Programmen können Benutzer wahrscheinlich Aufgaben ausführen, die Sie zuvor noch nicht ausgeführt haben, z. b. neue Nachrichten lesen, neue Videos ansehen oder Ihre nächste Besprechung überprüfen.
    -   **Was die Benutzer interessieren.** Stellen Sie sich vor, warum Benutzer die Sprung Liste anstelle anderer Mittel verwenden würden. Beispielsweise ist es wahrscheinlicher, dass sich die Ziele, die Sie explizit als wichtig identifiziert haben (z. b. Webanwendungen, die Benutzer in ihrer Verknüpfungs Leiste oder in Favoriten abgelegt haben oder eingegeben haben). Es ist weniger wahrscheinlich, dass die indirekt oder mit geringem Aufwand (z. b. durch Umleitung oder durch Klicken auf Verknüpfungen besuchte Webadressen) nicht berücksichtigt werden.

        **Richtig:**

        ![Screenshot der Sprung Liste mit einem Link zu einem Ziel ](images/winenv-taskbar-image25.png)

        **Falsch:**

        ![Screenshot der Sprung Liste mit fünf Verknüpfungen zum Ziel ](images/winenv-taskbar-image26.png)

        Im falschen Beispiel enthält die Sprung Liste viele Ziele, die für Benutzer wahrscheinlich nicht relevant sind.

-   **Machen Sie Ziele nicht zu genau.** Wenn Sie Ziele zu eng und spezifisch machen, kann dies zu Redundanz führen, und es gibt mehrere Möglichkeiten, zum gleichen Ort zu wechseln. Wenn Sie z. b. keine einzelnen Webseiten auflisten, sollten Sie stattdessen die Startseiten der obersten Ebene auflisten. Listen Sie anstelle der Auflistung von Liedern Alben auf.

    **Richtig:**

    ![Screenshot der Sprung Liste nach Gruppen ](images/winenv-taskbar-image27.png)

    **Falsch:**

    ![Screenshot der Sprung Liste nach Liedern organisiert ](images/winenv-taskbar-image28.png)

    Im falschen Beispiel wird das Auflisten von Titeln in einer Sprung Liste mit einem einzigen Album gefüllt.

-   **Füllen Sie nicht alle verfügbaren Sprung Listen Slots aus, wenn Sie dies nicht benötigen.** Fokus Listen Inhalt der nützlichsten Elemente, wenn Ihr Programm nur drei nützliche Elemente enthält, geben Sie nur drei an. Umso mehr Elemente in einer Sprung Liste sind erforderlich, um ein bestimmtes Element zu finden.

    ![Screenshot der Sprung Liste mit einem Befehl ](images/winenv-taskbar-image29.png)

    In diesem Beispiel stellt das Kurznotizen Zubehör einen einzigen Sprung Listen Befehl bereit, da dies alles ist, was erforderlich ist.

-   **Geben Sie Quick Infos nur bei Bedarf ein, um Benutzern das Verständnis von Sprung Listenelementen zu erleichtern.** Vermeiden Sie redundante Quick Infos, da Sie unnötige Ablenkungen darstellen. Weitere QuickInfo-Richtlinien finden Sie unter Quick [Infos und infotips](ctrl-tooltips-and-infotips.md).

    **Falsch:**

    ![Screenshot der Sprung Liste mit redundanter QuickInfo ](images/winenv-taskbar-image30.png)

    In diesem Beispiel ist die QuickInfo der Sprung Liste redundant.

**Sprung Listen Features und Programm Features**

-   **Stellen Sie Ziele und Befehle nicht nur über Sprung Listen zur Verfügung.** Die gleichen Ziele und Befehle sollten direkt aus dem Programm selbst verfügbar sein.
-   **Verwenden Sie konsistente Namen für Ziele und Bezeichnungen für Befehle.** Sprung Listenelemente müssen mit den entsprechenden Elementen identisch sein, auf die direkt vom Programm zugegriffen wird.
-   **Aktivieren Sie das Programm, um Ziele und Befehle auch dann zu verarbeiten, wenn das Programm nicht ausgeführt wird.** Dies ist erforderlich, um eine konsistente, zuverlässige und bequeme Darstellung zu gewährleisten.

**Gruppierung**

-   **Geben Sie mindestens eine und höchstens drei Gruppen an.** Sprung Listenelemente werden immer gruppiert, um ihren Zweck zu bezeichnen. Wenn mehr als drei Gruppen vorhanden sind, sind Elemente schwerer zu finden.
-   **Verwenden Sie bei Bedarf Standard Gruppennamen.** Standard Gruppennamen sind Ihnen vertraut und können Benutzer leichter verstehen.

    Befehlen wird der Name der Aufgaben Gruppe zugewiesen, der von Windows zugewiesen wird und daher nicht geändert werden kann.

    **Richtig:**

    ![Screenshot der Sprung Liste mit dem aktuellen Gruppennamen ](images/winenv-taskbar-image31.png)

    **Falsch:**

    ![Screenshot der Sprung Liste mit dem Namen der Verlaufs Gruppe ](images/winenv-taskbar-image32.png)

    "Aktuell" ist der bessere Gruppenname, da er vertraut ist, und der feine Unterschied zwischen Verlauf und letzter ist nicht sinnvoll.

**Befehle**

-   **Stellen Sie einen festgelegten Satz von Befehlen bereit, unabhängig vom Status des Programms, das aktuelle Dokument oder den aktuellen Benutzer.** Die Befehle sollten auf das gesamte Programm, nicht auf ein bestimmtes Fenster oder Dokument angewendet werden. Dies ist erforderlich, um eine konsistente, zuverlässige und bequeme Darstellung zu gewährleisten. Befehle sollten nicht entfernt oder deaktiviert werden.

    **Ausnahmen:** In folgenden Aktionen können Sie Befehle ersetzen oder entfernen:

    -   Ein Satz von sich gegenseitig ausschließenden Befehlen hat einen einzelnen Befehls Slot gemeinsam, solange ein Befehl immer angewendet wird.
    -   Befehle werden erst angewendet, wenn bestimmte Features verwendet wurden, solange die Befehle andernfalls immer angewendet werden.

    **Falsch:**

    ![Screenshot der Sprung Liste mit Druck Aufgabe ](images/winenv-taskbar-image33.png)

    In diesem Beispiel ist "Print" kein guter Sprung Listen Befehl, da er vom aktuellen Dokument abhängig ist.

    **Richtig:**

    ![Screenshot der Sprung Liste mit der Anmeldung und Abmeldung ](images/winenv-taskbar-image34.png)

    In diesem Beispiel sind die Befehle "Anmelden" und "Abmelden" gegenseitig ausschließende Befehle. Außerdem werden Trennzeichen verwendet, um verwandte Befehle zu gruppieren.

-   **Verwenden Sie bei Bedarf die folgenden Standard Befehls Bezeichnungen.** Standard Befehls Bezeichnungen sind für Benutzer leichter zu verstehen.
-   **Stellen Sie die Befehle in einer logischen Reihenfolge dar.** Allgemeine Bestellungen umfassen die Nutzungshäufigkeit oder die Reihenfolge der Verwendung. Platzieren Sie sehr verwandte Befehle nebeneinander. Fügen Sie in der Gruppe Tasks nach Bedarf Trennzeichen zwischen Gruppen verwandter Befehle ein.
-   **Stellen Sie keine Befehle zum Öffnen oder Schließen des Programms bereit.** Diese Befehle sind in alle Sprung Listen integriert.

**Befehlssymbole**

-   **Geben Sie in der Gruppe Tasks nur dann ein Befehls Symbol an, wenn es Benutzern hilft, Befehle zu verstehen, zu erkennen oder zu unterscheiden,** insbesondere dann, wenn ein Symbol für den Befehl vorhanden ist, der innerhalb des Programms verwendet wird.

    -   **Ausnahme:** Wenn das Programm beide Ziele (die immer über Symbole verfügen) und Befehle verwendet, sollten Sie die Bereitstellung von Symbolen für alle Befehle in Erwägung gezogen, wenn dies nicht der Fall ist.

    **Falsch:**

    ![Screenshot der inkonsistenten Verwendung von Symbolen in der Sprung Liste ](images/winenv-taskbar-image35.png)

    In diesem Beispiel sollte Internet Explorer Symbole für alle Befehle bereitstellen, um ein unangenehmes aussehen zu vermeiden.

**Destinations**

-   **Stellen Sie einen dynamischen Satz von Zielen bereit, die für den aktuellen Benutzer spezifisch sind, aber unabhängig vom Programm, der den Status oder das aktuelle Dokument ausführen.** Wie bereits erwähnt, müssen Sie sicherstellen, dass Sie an den Zweck Ihres Programms angepasst werden, welche Benutzer sich am meisten interessieren und wie Sie die richtige Ebene aufweisen.
-   **Wenn geeignet, verwenden Sie eine "automatische" Zielliste.** Automatische Ziele werden von Windows verwaltet, aber das Programm steuert die spezifischen Ziele, die weitergegeben werden.
    -   Verwenden Sie "zuletzt verwendet" für Programme zur Dokument Erstellung, bei denen Benutzer wahrscheinlich zu den zuletzt verwendeten Zielen zurückkehren.

        ![Screenshot der Sprung Liste mit dem Gruppennamen "zuletzt" ](images/winenv-taskbar-image36.png)

        In diesem Beispiel verwendet Windows Notepad die letzten Ziele.

    -   Sie sollten häufig für Programme verwenden, die vorhandene Inhalte anzeigen, bei denen Benutzer wahrscheinlich zu häufig verwendeten Elementen zurückkehren. Häufige Ziele werden in der Reihenfolge der Häufigkeit sortiert, die am häufigsten zuerst auftritt.

        ![Screenshot der Sprung Liste mit dem häufigen Gruppennamen ](images/winenv-taskbar-image37.png)

        In diesem Beispiel verwendet Windows Explorer häufige Ziele.

    -   Verwenden Sie häufig, wenn die aktuelle zu vielen nutzlosen Zielen führen würde. Häufige Listen sind stabiler, und die bessere Wahl, wenn Benutzer zu vielen verschiedenen Zielen navigieren, aber wahrscheinlich nicht zu selten verwendeten Listen zurückkehren.

        **Falsch:**

        ![Screenshot der Sprung Liste mit mehreren zuletzt verwendeten Elementen ](images/winenv-taskbar-image38.png)

        Die Verwendung der aktuellen in Windows Internet Explorer führt zu vielen nutzlosen Zielen.

    -   Wenn "aktuell" oder "häufig" gleichermaßen geeignet ist, verwenden Sie "aktuell", da diese Vorgehensweise für Benutzer einfacher zu verstehen und besser vorhersagbar ist
    -   Wenn Sie "zuletzt verwendet" verwenden und das Programm im Menü "Datei" über eine Entsprechung verfügt, nehmen Sie an, dass die Listen denselben Inhalt in derselben Reihenfolge aufweisen. Den Benutzern sollten diese Listen angezeigt werden.

-   **Verwenden Sie ggf. eine benutzerdefinierte Zielliste.** Das Programm verfügt über eine umfassende Kontrolle über den Inhalt und die Sortierreihenfolge einer benutzerdefinierten Zielliste und kann daher die Liste auf beliebige Faktoren basieren.
    -   Erstellen Sie benutzerdefinierte Versionen von zuletzt oder häufig, wenn diese geeignet sind, aber die automatische Verwaltung funktioniert nicht gut für Ihr Programm. Beispielsweise muss das Programm möglicherweise eine Vielzahl von Faktoren über geöffnete Datei Befehle hinaus verfolgen. Verwenden Sie in diesem Fall denselben Namen (aktuell oder häufig) und die Sortierreihenfolge, da die Benutzer den Unterschied nicht kennen.
    -   Verwenden Sie andernfalls einen anderen Zieltyp, um die Ziele ihrer Benutzer besser zu erfüllen. Häufig helfen diese Listen Benutzern dabei, Aufgaben auszuführen, die Sie zuvor noch nicht ausgeführt haben, z. b. das Lesen neuer Nachrichten, das Ansehen neuer Videos oder das Überprüfen der nächsten Besprechung.

        ![Screenshot der Sprung Liste mit "New"-Gruppenname ](images/winenv-taskbar-image39.png)

        In diesem Beispiel listet Windows Media Center die kürzlich aufgezeichneten anzeigen auf, die der Benutzer noch nicht gesehen hat.

    -   Wählen Sie eine Sortierreihenfolge aus, die dem geistigen Modell der Liste des Benutzers entspricht. Beispielsweise würde eine to-do-Style-Liste zuerst die nächste Aufgabe haben. Wenn kein klares mentales Modell vorhanden ist, Sortieren Sie die Zielliste in alphabetischer Reihenfolge.

-   **Verwenden Sie nicht mehrere Ziellisten, die unterschiedliche Sichten derselben Daten bieten.** Vielmehr sollten mehrere Ziellisten größtenteils verschiedene Daten aufweisen, um die Differenz Szenarien zu unterstützen. Sie können z. b. eine aktuelle Liste oder eine häufig auftretende Liste, aber nicht beides bereitstellen. Dies ist verschwenderisch, wenn überlappende Elemente vorhanden sind, aber verwirrend sind, wenn überlappende Elemente entfernt werden.

    **Falsch:**

    ![Screenshot der Sprung Liste mit wiederholten Gruppenelementen ](images/winenv-taskbar-image40.png)

    In diesem Beispiel ist die Bereitstellung verschiedener Sichten der gleichen Ziele verschwenderisch.

    **Richtig:**

    ![Screenshot der Sprung Liste mit gut organisierten Aufgaben ](images/winenv-taskbar-image41.png)

    In diesem Beispiel verfügen die Ziellisten über unterschiedliche Daten für verschiedene Tasks.

-   **Wenn das Programm über einen Befehl zum Löschen von Daten für den Datenschutz verfügt, löschen Sie auch die Liste der Ziele.** Ziellisten können vertrauliche Daten enthalten.

### <a name="thumbnail-toolbars"></a>Miniatur Ansichts Symbolleisten

**Interaktion**

-   **Stellen Sie bis zu sieben der wichtigsten, häufig verwendeten Befehle bereit, die für das in der Miniaturansicht angezeigte Fenster gelten.** Sie sind nicht verpflichtet, so viele Befehle wie möglich bereitzustellen, wenn Ihr Programm nur drei wichtige, häufig verwendete Befehle enthält, geben Sie nur drei an.

    **Falsch:**

    ![Screenshot der Symbolleiste mit zu vielen Befehlen ](images/winenv-taskbar-image42.png)

    In diesem Beispiel enthält die Miniaturansicht-Symbolleiste Befehle, die nicht wichtig sind.

-   **Verwenden Sie direkte und unmittelbare Befehle.** Diese Befehle sollten sofort wirksam sein, wenn Sie auf den Befehl klicken, um weitere Eingaben anzuzeigen und kein Dropdown Menü oder Dialogfeld anzuzeigen.

    **Falsch:**

    ![Screenshot der Miniaturansicht mit dem Dropdown Menü ](images/winenv-taskbar-image43.png)

    Miniatur Ansichts-Symbolleisten Befehle müssen sofort wirksam werden.

-   **Deaktivieren Sie Befehle, die nicht auf den aktuellen Kontext angewendet werden oder direkt zu einem Fehler führen.** Blenden Sie solche Befehle nicht aus, da dadurch die Symbolleisten Präsentation instabil wird.
-   **Schließen Sie die Miniaturansicht nicht, wenn Benutzer auf einen Befehl klicken, wenn Sie die Ergebnisse wahrscheinlich überprüfen oder sofort auf einen anderen Befehl klicken.** Entfernen Sie die Miniaturansicht für Befehle, die angeben, dass der Benutzer vorerst fertig ist, z. b. mit Befehlen, die andere Fenster anzeigen.

    ![Screenshot der Media Player-Miniaturansicht mit dem Befehl ](images/winenv-taskbar-image44.png)

    Wenn Sie in diesem Beispiel in Windows Media Player auf Weiter klicken, wird die Miniaturansicht weiterhin angezeigt, da Benutzer möglicherweise andere Befehle übergeben möchten.

    ![Screenshot der Miniaturansicht mit Chat (Symbol) ](images/winenv-taskbar-image45.png)

    In diesem Beispiel wird durch Klicken auf chatten in Windows Live Messenger die Miniaturansicht verworfen, da Benutzer höchstwahrscheinlich eine Nachricht senden.

**Präsentation**

-   **Stellen Sie sicher, dass Miniaturansicht-Symbolleisten Symbole den Aero-Style-Symbol Richtlinien entsprechen.** Stellen Sie für jeden Befehl High-Quality-Symbole mit einer Breite von 16x16, 20 x 20 und 24 x 24 Pixel bereit. Die größeren Versionen werden im Modus mit hoher dpi-Anzeige verwendet.
-   **Stellen Sie sicher, dass die Symbole für die Symbolleisten-Hintergrundfarbe im normalen und im Hover-Zustand eindeutig sichtbar sind.** Wertet Symbole immer im Kontext und im Modus mit hohem Kontrast aus.
-   **Wählen Sie Befehls Symbol Entwürfe aus, die ihre Auswirkung eindeutig übermitteln.** Gut entworfene Befehls Symbole sind selbsterklärend, um Benutzern zu helfen, Befehle effizient zu finden und zu verstehen.
-   **Wählen Sie Symbole aus, die erkennbar und unterschieden werden können.** Stellen Sie sicher, dass die Symbole über unterschiedliche Formen und Farben verfügen. Auf diese Weise können Benutzer die Befehle schnell finden, auch wenn Sie das symbolsymbol nicht merken. Nach der anfänglichen Verwendung sollten sich Benutzer nicht mehr auf Quick Infos verlassen müssen, um zwischen den Befehlen zu unterscheiden.
-   **Geben Sie eine QuickInfo zum bezeichnen der einzelnen Befehle an.** Eine gute QuickInfo bezeichnet das nicht beschriftete Steuerelement, auf das verwiesen wird. Richtlinien und Beispiele finden Sie unter Quick [Infos und infotips](ctrl-tooltips-and-infotips.md).

### <a name="progress-bars"></a>Status anzeigen

-   **Befolgen Sie die allgemeinen Richtlinien für die Statusanzeige,** einschließlich nicht Neustart oder Sicherungs Status, und verwenden Sie eine rote Statusanzeige, um ein Problem anzuzeigen.
-   **Vermeiden Sie die Verwendung von unbestimmten Status leisten.** Unbeendete Status leisten zeigen Aktivität, nicht Fortschritt an. Reservieren Sie unbestimmt Status leisten in seltenen Fällen, in denen Benutzer keine Aktivitäten für die Gewährung durchführen.

Weitere Richtlinien finden Sie unter Status [leisten](progress-bars.md).

## <a name="text"></a>Text

### <a name="window-titles"></a>Fenstertitel

Beachten Sie beim Auswählen von Fenstertiteln die Darstellung des Titels auf der Taskleiste:

-   Optimieren Sie die Titel für die Anzeige auf der Taskleiste, indem Sie die Unterscheidungs Informationen an erster Stelle platzieren.
-   Fassen Sie den Fortschritt in den Dialogfeldern für den nicht modalem Status zusammen. Beispiel: "66% Complete".
-   Vermeiden Sie Fenstertitel, die über umständliche Abschneiden verfügen.

    **Falsch:**

    ![Screenshot des Titels, der den Programmnamen abschneidet ](images/winenv-taskbar-image48.png)

    In diesem Beispiel hat der Titel des abgeschnittene Fensters unglückliche Ergebnisse.

### <a name="jump-list-commands"></a>Befehle der Sprung Liste

-   **Starten Sie Befehle mit einem Verb.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

Weitere Richtlinien für die Befehls Bezeichnung finden Sie unter [Menüs](cmd-menus.md).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Taskleiste:

-   Verweisen Sie auf die gesamte Leiste als Taskleiste (ein einzelnes Verbund Wort in Kleinbuchstaben).
-   Verweisen Sie auf die Elemente auf der Taskleiste speziell auf ihre Bezeichnung oder im Allgemeinen auf die Schaltflächen der Taskleiste.
-   Formatieren Sie die Task leisten Bezeichnungen, wenn möglich, mit fett formatiertem Text. Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.
-   Weitere Informationen finden Sie unter über Lagerungs Symbole als Symbolleisten Symbole. Sie werden nicht als Benachrichtigungen bezeichnet, auch wenn der Zweck darin besteht, Benutzer zu benachrichtigen. Sie können jedoch sagen, dass diese Symbole Benutzer über bestimmte Ereignisse benachrichtigen.

Beispiel: das Schaltflächen Symbol "neue Mail-Taskleiste" benachrichtigt Sie, dass eine neue e-Mail-Nachricht eingetroffen ist.

 


---
title: Taskleiste
description: Die Taskleiste ist der Zugriffspunkt für Programme, die auf dem Desktop angezeigt werden. Mit den neuen Windows 7-Taskleistenfeatures können Benutzer Befehle erteilen, auf Ressourcen zugreifen und den Programmstatus direkt über die Taskleiste anzeigen.
ms.assetid: c00e558a-313f-4741-a4b2-7d738f4544fa
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c3e549e665f0200a448144ddf7202b258e88ff26
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443391"
---
# <a name="taskbar"></a>Taskleiste

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Die Taskleiste ist der Zugriffspunkt für Programme, die auf dem Desktop angezeigt werden. Mit den neuen Windows 7-Taskleistenfeatures können Benutzer Befehle erteilen, auf Ressourcen zugreifen und den Programmstatus direkt über die Taskleiste anzeigen.

Die Taskleiste ist der Zugriffspunkt für Programme, die auf dem Desktop angezeigt werden, auch wenn das Programm minimiert ist. Solche Programme werden als Desktopdarstellung bezeichnet. Über die Taskleiste können Benutzer die geöffneten primären Fenster und bestimmte sekundäre Fenster auf dem Desktop anzeigen und schnell zwischen ihnen wechseln.

![Screenshot der Taskleiste mit aufgerufenen Features ](images/winenv-taskbar-image1.png)

Die Microsoft Windows-Taskleiste.

Die Steuerelemente auf der Taskleiste werden als Taskleistenschaltflächen bezeichnet. Wenn ein Programm ein primäres Fenster (oder ein sekundäres Fenster mit bestimmten Merkmalen) erstellt, fügt Windows eine Taskleistenschaltfläche für dieses Fenster hinzu und entfernt es, wenn dieses Fenster geschlossen wird.

Programme, die für Windows 7 entwickelt wurden, können diese neuen Funktionen der Taskleistenschaltfläche nutzen:

-   Sprunglisten bieten schnellen Zugriff auf häufig verwendete Ziele (z. B. Dateien, Ordner und Links) und Befehle über ein Kontextmenü, auf das über die Taskleistenschaltfläche des Programms zugegriffen werden kann, und Startmenü Element, auch wenn das Programm derzeit nicht ausgeführt wird.
-   Miniaturansichtssymbolleisten bieten schnellen Zugriff auf häufig verwendete Befehle für ein bestimmtes Fenster. Miniaturansichtssymbolleisten werden in der Miniaturansicht der Taskleistenschaltfläche angezeigt.
-   Überlagerungssymbole zeigen die Statusänderung auf dem Symbol der Taskleistenschaltfläche des Programms an.
-   Statusleisten zeigen den Fortschritt für Aufgaben mit langer Ausführungslaufzeit auf der Taskleistenschaltfläche des Programms an.
-   Unterfenster-Taskleistenschaltflächen ermöglichen Benutzern die Verwendung von Miniaturansichten der Taskleistenschaltfläche, um direkt zu Fensterregisterkarten, Projektfenstern, untergeordneten MDI-Fenstern (Multiple Document Interface) und sekundären Fenstern zu wechseln.
-   Mit angehefteten Taskleistenschaltflächen können Benutzer Programmschaltflächen an die Taskleiste anheften, um schnellen Zugriff auf Programme auch dann zu ermöglichen, wenn sie nicht ausgeführt werden.

Technisch gesehen umfasst die Taskleiste den gesamten Balken vom Schaltfläche "Start" bis zum Benachrichtigungsbereich. In der Regel bezieht sich die Taskleiste jedoch nur auf den Bereich, der die Taskleistenschaltflächen enthält. Bei konfigurationen mit mehreren Monitoren verfügt nur ein Monitor über eine Taskleiste, und dieser Monitor ist der Standardmonitor.

**Hinweis:** Richtlinien zur [](winenv-desktop.md) [Desktop-,](win-window-mgt.md) [Benachrichtigungsbereichs-](winenv-notification.md)und Fensterverwaltung werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Programme, die für Windows 7 entwickelt wurden, können diese Funktionen der Taskleistenschaltfläche nutzen. Stellen Sie sich die folgenden wichtigen Fragen, um zu bestimmen, ob sie verwendet werden sollen:

**Sprunglisten**

-   **Müssen Benutzer häufig neue Aufgaben mit ihrem Programm starten?** Falls ja, sollten Sie eine Sprungliste bereitstellen. Sprunglisten können zwar für andere Zwecke verwendet werden, die meisten Szenarien umfassen jedoch das Starten einer neuen Aufgabe.
-   **Müssen Benutzer häufig auf zuletzt verwendete oder häufig verwendete Dateien, Ordner, Links oder andere Ressourcen zugreifen?** Falls ja, sollten Sie eine Sprungliste für den Zugriff auf diese nützlichen Ressourcen bereitstellen.

    ![Screenshot der Taskleiste mit Internet Explorer-Sprungliste ](images/winenv-taskbar-image2.png)

    In diesem Beispiel verwendet Windows Internet Explorer eine Sprungliste, um häufig besuchten Seiten darzustellen.

-   **Benötigen Benutzer häufig schnellen Zugriff auf eine kleine Anzahl von Befehlen Ihres Programms, während sie andere Programme verwenden, auch wenn Ihr Programm nicht ausgeführt wird?** Falls ja, sollten Sie eine Sprungliste mit diesen häufig verwendeten Befehlen bereitstellen. Diese Befehle müssen auch funktionieren, wenn ihr Programm nicht ausgeführt wird, und sie müssen für das gesamte Programm und nicht für ein bestimmtes Fenster gelten. Alternativ können Sie eine Miniaturansichtssymbolleiste für Befehle bereitstellen, die für ein bestimmtes Fenster gelten.

    ![Screenshot der Taskleiste mit Sprungliste mit stickigen Notizen ](images/winenv-taskbar-image3.png)

    In diesem Beispiel ermöglicht das Kurznotizen-Zubehör Benutzern, schnell eine neue Notiz zu erstellen, während sie andere Programme verwenden.

-   **Bewerben Sie neue, einmalige Verwendung oder schwer zu findende Features?** Verwenden Sie in diesem Falle keine Sprunglisten, da sie nicht für diesen Zweck vorgesehen sind. Verbessern Sie stattdessen die Auffindbarkeit solcher Befehle direkt im Programm.

**Miniaturansichtssymbolleisten**

Gelten alle folgenden Bedingungen?

-   **Gelten die Befehle für ein bestimmtes Fenster?** Miniaturansichtssymbolleisten sind für Befehle vorgesehen, die für vorhandene Aufgaben gelten, während Sprungliste Befehle zum Starten neuer Aufgaben dienen.
-   **Müssen Benutzer bei der Verwendung anderer Programme schnell mit einer ausgeführten Aufgabe interagieren?** Wenn ja, sind Miniaturansichtssymbolleisten eine gute Wahl. Miniaturansichtssymbolleisten können maximal sieben Befehle enthalten, aber maximal fünf Befehle werden im Allgemeinen bevorzugt.
-   **Sind die Befehle sofort?** Das heißt, sind keine zusätzlichen Eingaben erforderlich? Miniaturansichtssymbolleisten müssen über sofortige Befehle verfügen, um effizient zu sein, während Sprunglisten besser mit Befehlen funktionieren, die zusätzliche Eingaben erfordern.

    **Falsch:**

    ![Screenshot der Taskleiste mit überlappenden Fenstern ](images/winenv-taskbar-image4.png)

    Befehle, die zusätzliche Eingaben erfordern, funktionieren auf Miniaturansichtssymbolleisten nicht gut.

-   **Sind die Befehle direkt?** Das heißt, können Benutzer mit einem einzigen Klick mit ihnen interagieren? Symbolleisten müssen über direkte Befehle verfügen, um effizient zu sein.
-   **Werden die Befehle durch Symbole gut dargestellt?** Miniaturansichtssymbolleistenbefehle werden mit Symbolen und nicht mit Textbeschriftungen dargestellt, während Sprungliste Befehle durch Textbeschriftungen dargestellt werden.

    **Falsch:**

    ![Screenshot des Miniaturansichtsbefehls mit Symbol ](images/winenv-taskbar-image5.png)

    In diesem Beispiel wird der Befehl nicht gut durch Symbole dargestellt.

**Überlagerungssymbole**

-   **Verfügt das Programm über "Desktopdarstellung"?** Falls nicht, verwenden Sie stattdessen ein Symbol für den Benachrichtigungsbereich. Wenn ja, sollten Sie ein Überlagerungssymbol verwenden, anstatt den Status auf dem Symbol für den Benachrichtigungsbereich für Programme zu setzen, die für Windows 7 entwickelt wurden. Dadurch wird sichergestellt, dass das Symbol immer sichtbar ist (wenn große Symbole verwendet werden), und das Programm mit seinem Status an einem Ort konsolidiert.
-   **Wird das Überlagerungssymbol vorübergehend angezeigt, um eine Statusänderung anzuzeigen?** In diesem Falle kann je nach den folgenden Faktoren ein Überlagerungssymbol geeignet sein:
    -   **Ist der Status nützlich und relevant, wenn andere Programme verwendet werden?** Andernfalls werden die Informationen in den [Statusleisten](ctrl-status-bars.md) des Programms oder in einem anderen Programmstatusbereich angezeigt.

        ![Screenshot der Statusleiste des Internet Explorer-Fensters ](images/winenv-taskbar-image7.png)

        In diesem Beispiel wird die Statusleiste verwendet, da der Status bei Verwendung anderer Programme nicht nützlich ist.

    -   **Zeigt der Status den Fortschritt an?** Wenn ja, verwenden Sie stattdessen eine Statusleiste der Taskleistenschaltfläche.
    -   **Ist der Status kritisch? Ist sofortige Aktion erforderlich?** Wenn ja, zeigen Sie die Informationen auf eine Weise an, die Aufmerksamkeit erfordert und nicht einfach ignoriert werden kann, z. B. ein [Dialogfeld](win-dialog-box.md).

**Statusanzeigen**

-   **Ist das Fortschrittsfeedback nützlich und relevant bei der Verwendung anderer Programme?** Das heißt, werden Benutzer wahrscheinlich den Fortschritt überwachen, während sie andere Programme verwenden, und ihr Verhalten ändern? Ein solcher nützlicher und relevanter Status wird in der Regel über ein statusloses Dialogfeld oder eine dedizierte Statusseite angezeigt, jedoch nicht mit einem ausgelasteten Zeiger, Aktivitätsindikator oder Statusanzeige auf einer Statusleiste. Wenn der Status bei Verwendung anderer Programme nicht hilfreich ist, zeigen Sie einfach das Fortschrittsfeedback direkt im Programm selbst an.

    **Richtig:**

    ![Screenshot des Kopierdialogfelds mit Statusanzeige ](images/winenv-taskbar-image8.png)

    **Falsch:**

    ![Screenshot der Statusanzeige auf der Taskleistenschaltfläche ](images/winenv-taskbar-image9.png)

    Im falschen Beispiel ist die Statusleiste der Taskleistenschaltfläche nicht sehr nützlich.

-   **Ist die Aufgabe fortlaufend?** Wenn die Aufgabe nie abgeschlossen wird, muss der Fortschritt nicht angezeigt werden. Beispiele für kontinuierliche Aufgaben sind Antivirenscans, die nicht von Benutzern initiiert werden, und Dateiindizierung.

    **Falsch:**

    ![Screenshot des Statussymbols einer fortlaufenden Aufgabe ](images/winenv-taskbar-image10.png)

    In diesem Beispiel muss ein fortlaufender Task den Fortschritt nicht anzeigen.

**Taskleisten des Unterfensters**

-   **Enthält Ihr Programm Registerkarten, Projektfenster, untergeordnete MDI-Fenster oder sekundäre Fenster, zu denen Benutzer häufig direkt wechseln möchten?** Falls ja, kann es sinnvoll sein, diesen Fenstern eigene Miniaturansichten der Taskleistenschaltfläche zu geben.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="using-jump-lists-and-thumbnail-toolbars-effectively"></a>Effektives Verwenden von Sprunglisten und Miniaturansichtssymbolleisten

Sprunglisten und Miniaturansichtssymbolleisten helfen Benutzern, auf Ressourcen zu zugreifen und Befehle effizienter auszuführen. Wenn Sie jedoch entwerfen, wie Ihr Programm diese Features unterstützt, sollten Sie die effizienzsteigerung nicht selbstverständlicher gestalten. Wenn Benutzer nicht genau vorhersagen können, welches Feature über den benötigten Befehl verfügt, oder wenn sie mehrere Stellen überprüfen müssen, werden Benutzer letztendlich frustriert und können diese Features nicht mehr verwenden.

Sprunglisten und Miniaturansichtssymbolleisten funktionieren am effektivsten, wenn sie:

-   **Eindeutig differenziert.** Benutzer wissen, wann nach einem Ziel oder Befehl in einer Sprungliste und wann sie in einer Miniaturansichtssymbolleiste suchen sollten. Es gibt einen eindeutigen Zweck, sodass Benutzer den Inhalt der beiden nur selten verwechseln. Im Allgemeinen werden Sprunglisten verwendet, um neue Aufgaben zu starten, während Miniaturansichtssymbolleisten verwendet werden, um mit ausgeführten Aufgaben zu interagieren, während andere Programme verwendet werden.
-   **Nützlich.** Die von Benutzern benötigten Ziele und Befehle sind diejenigen, die sie benötigen. Wenn Benutzer wahrscheinlich etwas nicht benötigen, wird es nicht eingeschlossen. Verwenden Sie nicht die maximale Anzahl von Elementen, wenn sie nicht benötigt werden.
-   **Vorhersehbar.** Die angebotenen Ziele und Befehle sind die Ziele, die Benutzer erwarten. Benutzer müssen selten an mehr als einem Ort suchen.
-   **Gut organisiert.** Benutzer können schnell herausfinden, was sie suchen. Sie verwenden beschreibende, aber präzise Bezeichnungen und geeignete Symbole, um die Erkennung zu helfen.

Stellen Sie sicher, dass Sie nach Benutzerinformationen forschen, um sicherzustellen, dass Sie richtig sind. Wenn Sie letztendlich feststellen, dass Sie keine Sprunglisten und Miniaturansichtssymbolleisten zusammen entwerfen können, die diese Ziele erreichen, sollten Sie nur eine davon bereitstellen. Es ist besser, eine vorhersagbare Möglichkeit zu haben, Befehle zu geben, als zwei verwirrende.

## <a name="guidelines"></a>Richtlinien

### <a name="taskbar-buttons"></a>Taskleistenschaltflächen

-   **Lassen Sie die folgenden Fenstertypen auf der Taskleiste angezeigt (für Windows 7 mithilfe einer Miniaturansicht der Taskleistenschaltfläche):**
    -   Primäre Fenster (einschließlich Dialogfelder ohne Besitzer)
    -   Eigenschaftenblätter
    -   Dialogfelder für den statuslosen Status
    -   Assistenten
-   **Verwenden Sie für Windows 7 Miniaturansichten der Taskleistenschaltfläche, um die folgenden Fenstertypen mit der Taskleistenschaltfläche des primären Fensters zu gruppen, aus der sie gestartet wurde.** Jedes Programm (insbesondere jedes Programm, das als separates Programm wahrgenommen wird) sollte über eine einzelne Taskleistenschaltfläche verfügen.

    -   Sekundäre Fenster
    -   Registerkarten "Arbeitsbereich"
    -   Projektfenster
    -   Untergeordnetes MDI-Fenster

    **Richtig:**

    ![Screenshot des Windows-Explorers und der Statusleiste ](images/winenv-taskbar-image11.png)

    In diesem Beispiel wird ein sekundäres Fenster mit der Taskleistenschaltfläche des primären Fensters gruppiert.

    **Falsch:**

    ![Screenshot des Windows-Explorers und der Systemsteuerung ](images/winenv-taskbar-image12.png)

    In diesem Beispiel wird Systemsteuerung falsch mit einem Windows-Explorer. Benutzer betrachten diese als separate Programme.

    **Falsch:**

    ![Screenshot des Programms, der Statusleiste und einer Taskleiste ](images/winenv-taskbar-image13.png)

    In diesem Beispiel verwendet Windows-Sicherung fälschlicherweise zwei Taskleistenschaltflächen für ein einzelnes Programm.

-   **Beim Wiederherstellen eines primären Fensters sollten auch** alle sekundären Fenster wiederhergestellt werden, auch wenn diese sekundären Fenster über eigene Taskleistenschaltflächen verfügen. Platzieren Sie bei der Wiederherstellung sekundäre Fenster über dem primären Fenster.
-   **Unter Windows 7 können Programme, die normalerweise über Desktops verfügen, vorübergehend eine Taskleistenschaltfläche anzeigen, um den Status anzuzeigen.** Tun Sie dies nur, wenn Ihr Programm normalerweise auf dem Desktop angezeigt wird und Benutzer häufig damit interagieren. Ein Programm, das normalerweise ohne Desktop-Präsenz ausgeführt wird, sollte stattdessen das Benachrichtigungsbereichssymbol verwenden, obwohl es möglicherweise nicht immer sichtbar ist.

    **Falsch:**

    ![Screenshot der Taskleistenschaltfläche des Windows-Synchronisierungscenters ](images/winenv-taskbar-image14.png)

    In diesem Beispiel verwendet Windows Synchronisierungscenter fälschlicherweise eine temporäre Taskleistenschaltfläche, um den Status anzuzeigen. Stattdessen sollte das Benachrichtigungsbereichssymbol verwendet werden.

### <a name="icons"></a>Symbole

-   **Entwerfen Sie das Programmsymbol so, dass es auf der Taskleiste gut ausschaut.** Stellen Sie sicher, dass es sinnvoll ist und seine Funktion und Ihre Marke widerspiegelt. Machen Sie es eindeutig, machen Sie es speziell, und stellen Sie sicher, dass es in allen Symbolgrößen gut gerendert wird. Verbringen Sie die Zeit, die erforderlich ist, um es richtig zu machen. Befolgen Sie [die Richtlinien für Symbole im Stil von Stil.](vis-icons.md)
-   **Wenn Ihr Programm Überlagerungssymbole verwendet, entwerfen Sie das Basissymbol Ihres Programms, um Überlagerungen gut zu verarbeiten.** Überlagerungssymbole werden in der unteren rechten Ecke angezeigt. Entwerfen Sie daher das Symbol so, dass der Bereich verdeckt werden kann.

    ![Screenshot von Symbolen und mit unterer rechtem Overlay ](images/winenv-taskbar-image15.png)

    In diesem Beispiel enthält das Symbol für die Taskleistenschaltfläche des Programms im unteren rechten Bereich keine wichtigen Informationen.

-   **Verwenden Sie keine Überlagerungen im** Basissymbol Ihres Programms, unabhängig davon, ob das Programm Überlagerungssymbole verwendet oder nicht. Die Verwendung einer Überlagerung im Basissymbol ist verwirrend, da Benutzer herausfinden müssen, dass sie keinen Status kommunizieren.

    **Falsch:**

    ![Screenshot des Basissymbols mit Überlagerung ](images/winenv-taskbar-image16.png)

    In diesem Beispiel sieht das Basissymbol des Programms so aus, als würde es den Status anzeigen.

Allgemeine Symbolrichtlinien und Beispiele finden Sie unter [Symbole](vis-icons.md).

### <a name="overlay-icons"></a>Überlagerungssymbole

-   **Verwenden Sie Überlagerungssymbole, um nur den nützlichen und relevanten Status anzugeben.** Betrachten Sie die Anzeige eines Überlagerungssymbols als potenzielle Unterbrechung der Arbeit des Benutzers, sodass die Statusänderung wichtig genug sein muss, um eine potenzielle Unterbrechung zu bewerksparen.

    **Falsch:**

    ![Screenshot von drei Überlagerungssymbolen ](images/winenv-taskbar-image17.png)

    In diesen Beispielen ist das Überlagerungssymbol nicht wichtig genug, um eine potenzielle Unterbrechung zu ersparen.

-   **Verwenden Sie Überlagerungssymbole für den temporären Status.** Die Überlagerungssymbole verlieren ihren Wert, wenn sie ständig angezeigt werden, sodass der normale Programmstatus kein Symbol anzeigen sollte. Entfernen Sie das Überlagerungssymbol, wenn das Symbol:

    -   **Ist für ein Problem:** Entfernen Sie das Symbol, sobald das Problem behoben wurde.
    -   **Weist darauf hin, dass etwas neu ist:** Entfernen Sie das Symbol, nachdem der Benutzer das Programm aktiviert hat.

    **Ausnahme:** Ihr Programm kann ständig ein Überlagerungssymbol anzeigen, wenn Benutzer ihren Status immer kennen müssen.

    ![Screenshot von Live-Messenger mit Überlagerungssymbol ](images/winenv-taskbar-image18.png)

    In diesem Beispiel zeigt Windows Live Messenger immer ein Überlagerungssymbol an, damit Benutzer immer ihre gemeldete Präsenz überprüfen können.

-   **Zeigen Sie kein Symbol an, um anzugeben, dass ein Problem gelöst wurde.** Entfernen Sie stattdessen einfach alle vorherigen Symbole, die auf ein Problem hinweisen. Gehen Sie davon aus, dass Benutzer normalerweise erwarten, dass Ihr Programm problemlos ausgeführt wird.
-   **Zeigen Sie entweder Überlagerungssymbole oder Benachrichtigungsbereichssymbole an, aber nie beide.** Ihr Programm unterstützt möglicherweise beide Mechanismen zur Abwärtskompatibilität, aber wenn ihr Programm den Status mithilfe von Überlagerungssymbolen anzeigt, sollte es nicht auch Benachrichtigungsbereichssymbole für den Status verwenden.

    **Falsch:**

    ![Screenshot der Taskleiste mit zweimal angezeigten Symbolen ](images/winenv-taskbar-image19.png)

    In diesem Beispiel wird das neue E-Mail-Symbol redundant angezeigt.

-   **Drücken Sie nicht die Taskleistenschaltfläche, um auf eine Statusänderung aufmerksam zu machen.** Dies wäre zu störend. Benutzer können Überlagerungssymbole selbst entdecken.
-   **Standardüberlagerungssymbole werden bevorzugt, um Status- oder Statusänderungen anzuzeigen.** Verwenden Sie diese Standardüberlagerungssymbole: 

    | Überlagerung | Status |
    |---------------------------------------------------------------------------------------------------|----------------------------------|
    | ![Screenshot eines kleinen Warnsymbols ](images/winenv-taskbar-image20.png)<br/>               | Warnung<br/>               |
    | ![Screenshot des kleinen Fehlersymbols ](images/winenv-taskbar-image21.png)<br/>                 | Fehler<br/>                 |
    | ![Screenshot des Symbols "Klein deaktiviert/getrennt" ](images/winenv-taskbar-image22.png)<br/> | Deaktiviert/Getrennt<br/> |
    | ![Screenshot: kleines Symbol "Blockiert/Offline" ](images/winenv-taskbar-image23.png)<br/>       | Blockiert/Offline<br/>       |

    

     

-   **Wählen Sie für benutzerdefinierte Überlagerungssymbole ein leicht erkennbares Design aus.** Verwenden Sie hochwertige 16 x 16 Pixel umfassende Farbsymbole. Symbole mit unterschiedlichen Konturen gegenüber quadratischen oder rechteckigen Symbolen bevorzugen. Wenden Sie auch die anderen Richtlinien für [Symbole im Stil von Styles](vis-icons.md) an.
-   **Halten Sie den Entwurf benutzerdefinierter Überlagerungssymbole einfach.** Versuchen Sie nicht, komplexe, unbekannte oder abstrakte Ideen zu kommunizieren. Wenn Sie sich kein geeignetes benutzerdefiniertes Symbol vorstellen können, verwenden Sie bei Bedarf einen Standardsymbolfehler oder ein Warnsymbol. Diese Symbole können effektiv verwendet werden, um viele Statustypen zu kommunizieren.
-   **Ändern Sie den Status nicht zu häufig.** Überlagerungssymbole dürfen nicht laut, instabil oder Aufmerksamkeit erfordern. Das Auge reagiert empfindlich auf Änderungen im Peripheriebereich des Sehens, sodass Statusänderungen geringfügig sein müssen.
    -   **Ändern Sie das Symbol nicht schnell.** Wenn sich der zugrunde liegende Status schnell ändert, sollte das Symbol den Status auf hoher Ebene widerspiegeln.

        **Falsch:**

        ![Screenshot des Overlaysymbols in zwei Zuständen ](images/winenv-taskbar-image24.png)

        In diesem Beispiel erfordert das sich schnell ändernde Überlagerungssymbol Aufmerksamkeit.

    -   **Verwenden Sie keine Animationen.** Dies ist zu ablenkend.
    -   **Blinken Sie das Symbol nicht.** Dies ist zu ablenkend. Wenn ein Ereignis sofortige Aufmerksamkeit erfordert, verwenden Sie stattdessen ein Dialogfeld. Wenn das Ereignis andernfalls Aufmerksamkeit benötigt, verwenden Sie eine Benachrichtigung.

### <a name="taskbar-button-flashing"></a>Blinkende Taskleistenschaltfläche

-   **Verwenden Sie die Taskleistenschaltfläche, die nur selten blinkt, um die sofortige Aufmerksamkeit des Benutzers aufzufordern, damit eine laufende Aufgabe weiterhin ausgeführt wird.** Es ist schwierig für Benutzer, sich zu konzentrieren, während eine Taskleistenschaltfläche blinkt. Nehmen Sie daher an, dass sie unterbrechen, was sie tun, um sie zu beenden. Das Blinken einer Taskleistenschaltfläche ist zwar besser als das Stehlen des Eingabefokus, aber das Blinken von Taskleistenschaltflächen ist immer noch sehr aufdringlich. Stellen Sie sicher, dass die Unterbrechung gerechtfertigt ist, z. B. um anzugeben, dass der Benutzer Daten speichern muss, bevor ein Fenster geschlossen wird. Inaktive Programme sollten selten sofortige Aktionen erfordern. Flashen Sie die Taskleistenschaltfläche nicht, wenn der Benutzer nur das Programm aktivieren, eine Nachricht lesen oder eine Statusänderung sehen muss.
-   **Wenn keine sofortige Aktion erforderlich ist, sollten Sie die folgenden Alternativen in Betracht ziehen:**
    -   Verwenden Sie eine [Aktionserfolgsbenachrichtigung,](mess-notif.md) um anzugeben, dass eine Aufgabe abgeschlossen wurde.
    -   Sie unternehmen nichts. Warten Sie einfach, bis benutzer sich an dem Problem bei der nächsten Aktivierung des Programms teilnehmen. Dies ist häufig die beste Wahl.
-   **Wenn ein inaktives Programm sofortige Aufmerksamkeit erfordert, blinken Sie die Taskleistenschaltfläche, um die Aufmerksamkeit zu lenken und es hervorgehoben zu lassen.** Machen Sie nichts anderes: Stellen Sie das Fenster nicht wieder her, oder aktivieren Sie es nicht, und geben Sie keine Soundeffekte wieder. Berücksichtigen Sie stattdessen die Fensterzustandsauswahl des Benutzers, und lassen Sie den Benutzer das Fenster aktivieren, wenn er bereit ist.
-   **Für sekundäre Fenster, die über eine Taskleistenschaltfläche verfügen, flashen Sie die Schaltfläche anstelle der Taskleistenschaltfläche des primären Fensters.** Auf diese Weise können Benutzer direkt am Fenster teilnehmen.
-   **Für sekundäre Fenster, die keine Taskleistenschaltfläche haben, flashen Sie die Taskleistenschaltfläche des primären Fensters, und setzen Sie das sekundäre Fenster über alle anderen Fenster für dieses Programm.** Sekundäre Fenster, die Aufmerksamkeit erfordern, müssen ganz oben sein, um sicherzustellen, dass sie benutzern angezeigt werden.
-   **Blinken Sie jeweils nur eine Taskleistenschaltfläche für jeweils ein Fenster.** Das Blinken mehrerer Schaltflächen ist unnötig und zu ablenkend.
-   **Entfernen Sie die Hervorhebung der Taskleistenschaltfläche, sobald das Programm aktiv wird.**
-   **Wenn das Programm aktiv wird, stellen Sie sicher, dass etwas offensichtlich ist.** In der Regel wird dieses Ziel erreicht, indem ein Dialogfeld angezeigt wird, das eine Frage stellt oder eine Aktion initiiert.

### <a name="quick-launch-shortcuts"></a>Schnellstart Tastenkombinationen

-   **Setzen Sie Programmverknüpfungen nur dann in den bereich Schnellstart, wenn Benutzer sich dafür entscheiden.** Da Schnellstart aus Windows 7 entfernt wurde, sollten Programme, die für Windows 7 entwickelt wurden, keine Programmverknüpfungen zum Schnellstart Bereich hinzufügen oder entsprechende Optionen bereitstellen.

### <a name="jump-lists"></a>Sprunglisten

**Design**

-   **Entwerfen Sie Sprunglisten, um die Ziele Ihrer Benutzer für ihre alltäglichen Aufgaben zu erfüllen.** Berücksichtigen Sie dabei Folgendes:
    -   **Der Zweck Ihres Programms.** Überlegen Sie, welche Benutzer als Nächstes am wahrscheinlichsten vorgehen werden. Bei Programmen zur Dokumenterstellung kehren Benutzer wahrscheinlich zu kürzlich verwendeten Dokumenten zurück. Für Programme, die vorhandene Inhalte anzeigen, möchten Benutzer möglicherweise Zugriff auf Ressourcen, die sie häufig verwenden. Bei anderen Programmen können Benutzer möglicherweise Aufgaben ausführen, die sie noch nicht ausgeführt haben, z. B. neue Nachrichten lesen, neue Videos ansehen oder ihre nächste Besprechung überprüfen.
    -   **Was den Benutzern am meisten am Wichtigsten ist.** Überlegen Sie sich, warum Benutzer die Sprungliste anstelle anderer Mittel verwenden würden. Benutzer interessieren sich beispielsweise eher für Ziele, die sie explizit als wichtig identifiziert haben (z. B. Webadressenbenutzer, die auf ihrer Linkleiste oder in Favoriten platziert oder eingegeben werden). Es ist weniger wahrscheinlich, dass sie sich um diejenigen kümmern, die indirekt oder mit geringem Aufwand abgerufen werden (z. B. Webadressen, die durch Umleitung oder durch Klicken auf Links besucht werden).

        **Richtig:**

        ![Screenshot der Sprungliste mit einem Link zu einem Ziel ](images/winenv-taskbar-image25.png)

        **Falsch:**

        ![Screenshot der Sprungliste mit fünf Links zum Ziel ](images/winenv-taskbar-image26.png)

        Im falschen Beispiel enthält die Sprungliste viele Ziele, die Benutzern wahrscheinlich nicht wichtig sind.

-   **Machen Sie Ziele nicht zu präzise.** Wenn Ziele zu schmal und spezifisch sind, kann dies zu Redundanz führen, und es gibt mehrere Möglichkeiten, an denselben Ort zu gelangen. Anstatt beispielsweise einzelne Webseiten aufzulisten, listen Sie stattdessen Startseiten der obersten Ebene auf. Anstatt Titel aufzulisten, listen Sie Alben auf.

    **Richtig:**

    ![Screenshot der nach Gruppen organisierten Sprungliste ](images/winenv-taskbar-image27.png)

    **Falsch:**

    ![Screenshot der nach Titeln organisierten Sprungliste ](images/winenv-taskbar-image28.png)

    Im falschen Beispiel füllt das Auflisten von Titeln in einem Sprungliste es mit einem einzigen Album.

-   **Füllen Sie nicht alle verfügbaren Sprungliste Slots aus, wenn Sie dies nicht benötigen.** Konzentrieren Sie sich Sprungliste Inhalte auf die nützlichsten Elemente, wenn Ihr Programm nur drei nützliche Elemente enthält, stellen Sie nur drei bereit. Je mehr Elemente in einem Sprungliste, desto mehr Aufwand ist erforderlich, um ein bestimmtes Element zu finden.

    ![Screenshot der Sprungliste mit einem Befehl ](images/winenv-taskbar-image29.png)

    In diesem Beispiel stellt das Kurznotizen-Accessory einen einzelnen Sprungliste Befehl bereit, da dies alles erforderlich ist.

-   **Geben Sie QuickInfos nur bei Bedarf an, damit Benutzer Sprungliste Elemente besser verstehen können.** Vermeiden Sie redundante QuickInfos, da sie eine unnötige Ablenkung sind. Weitere QuickInfo-Richtlinien finden Sie unter [QuickInfos und Infotips.](ctrl-tooltips-and-infotips.md)

    **Falsch:**

    ![Screenshot der Sprungliste mit redundanter QuickInfo ](images/winenv-taskbar-image30.png)

    In diesem Beispiel ist die Sprungliste QuickInfo redundant.

**Sprungliste Features im Vergleich zu Programmfeatures**

-   **Stellen Sie Ziele und Befehle nicht nur über Sprunglisten zur Verfügung.** Die gleichen Ziele und Befehle sollten direkt über das Programm selbst verfügbar sein.
-   **Verwenden Sie konsistente Namen für Ziele und Bezeichnungen für Befehle.** Sprungliste Elemente sollten mit den entsprechenden Elementen beschriftet werden, auf die direkt aus dem Programm zugegriffen wird.
-   **Ermöglichen Sie es Ihrem Programm, Ziele und Befehle auch dann zu verarbeiten, wenn das Programm nicht ausgeführt wird.** Dies ist für eine konsistente, zuverlässige und praktische Erfahrung erforderlich.

**Gruppierung**

-   **Geben Sie mindestens eine und höchstens drei Gruppen an.** Sprungliste Elemente werden immer gruppiert, um ihren Zweck zu bezeichnen. Wenn Sie mehr als drei Gruppen haben, ist die Suche nach Elementen schwieriger.
-   **Verwenden Sie bei Bedarf Standardgruppennamen.** Standardgruppennamen sind für Benutzer vertraut und einfacher zu verstehen.

    Befehle erhalten den Gruppennamen Aufgaben, der von Windows zugewiesen wird und daher nicht geändert werden kann.

    **Richtig:**

    ![Screenshot der Sprungliste mit dem aktuellen Gruppennamen ](images/winenv-taskbar-image31.png)

    **Falsch:**

    ![Screenshot der Sprungliste mit Dem Namen der Verlaufsgruppe ](images/winenv-taskbar-image32.png)

    Aktuell ist der bessere Gruppenname, da er vertraut ist, und die dezente Unterscheidung zwischen Verlauf und neuer ist es nicht wert, dies zu machen.

**Befehle**

-   **Geben Sie einen festen Satz von Befehlen unabhängig vom Ausführungsstatus des Programms, dem aktuellen Dokument oder dem aktuellen Benutzer an.** Die Befehle sollten für das gesamte Programm und nicht für ein bestimmtes Fenster oder Dokument gelten. Dies ist für eine konsistente, zuverlässige und praktische Erfahrung erforderlich. Befehle sollten nicht entfernt oder deaktiviert werden.

    **Ausnahmen:** Sie können Befehle ersetzen oder entfernen, wenn:

    -   Eine Reihe von sich gegenseitig ausschließenden Befehlen verwendet einen einzelnen Befehlsslot, solange immer ein Befehl gilt.
    -   Befehle werden erst angewendet, wenn bestimmte Features verwendet wurden, solange die Befehle andernfalls immer angewendet werden.

    **Falsch:**

    ![Screenshot der Sprungliste mit Druckaufgabe ](images/winenv-taskbar-image33.png)

    In diesem Beispiel ist Drucken kein guter Sprungliste Befehl, da er vom aktuellen Dokument abhängt.

    **Richtig:**

    ![Screenshot der Sprungliste mit Anmeldung und Abanmeldung ](images/winenv-taskbar-image34.png)

    In diesem Beispiel schließen sich Die Befehle Anmelden und Abmelden gegenseitig aus. Außerdem werden Trennzeichen verwendet, um verwandte Befehle zu gruppieren.

-   **Verwenden Sie ggf. die folgenden Standardbefehlsbezeichnungen.** Standardbefehlsbezeichnungen sind für Benutzer einfacher zu verstehen.
-   **Stellen Sie die Befehle in einer logischen Reihenfolge dar.** Häufige Bestellungen sind nach Verwendungshäufigkeit oder Verwendungsreihenfolge. Platzieren Sie in hohem Maße verwandte Befehle nebeneinander. Legen Sie in der Gruppe Tasks nach Bedarf Trennzeichen zwischen Gruppen verwandter Befehle ein.
-   **Geben Sie keine Befehle zum Öffnen oder Schließen des Programms an.** Diese Befehle sind in alle Sprunglisten integriert.

**Befehlssymbole**

-   **Geben Sie in der Gruppe Aufgaben nur dann ein Befehlssymbol an, wenn es Benutzern hilft, Befehle zu verstehen, zu erkennen oder zu unterscheiden. Dies** gilt insbesondere, wenn ein symbol für den im Programm verwendeten Befehl vorhanden ist.

    -   **Ausnahme:** Wenn Ihr Programm sowohl Ziele (mit immer Symbolen) als auch Befehle verwendet, erwägen Sie die Bereitstellung von Symbolen für alle Befehle, wenn dies nicht umständlich aussieht.

    **Falsch:**

    ![Screenshot der inkonsistenten Verwendung von Symbolen in der Sprungliste ](images/winenv-taskbar-image35.png)

    In diesem Beispiel sollten Internet Explorer Symbole für alle Befehle bereitstellen, um eine umständliche Darstellung zu vermeiden.

**Destinations**

-   **Geben Sie einen dynamischen Satz von Zielen an, die für den aktuellen Benutzer spezifisch sind, aber unabhängig vom Ausführungsstatus des Programms oder dem aktuellen Dokument sind.** Wie bereits erwähnt, stellen Sie sicher, dass sie dem Zweck Ihres Programms entsprechen, den Benutzern am wichtigsten sind und über das richtige Maß an Spezifität verfügen.
-   **Verwenden Sie bei Bedarf eine "automatische" Zielliste.** Automatische Ziele werden von Windows verwaltet, aber Ihr Programm steuert die spezifischen Ziele, die übergeben werden.
    -   Erwägen Sie die Verwendung von Zuletzt verwendet für Programme zur Dokumenterstellung, bei denen Benutzer wahrscheinlich zu kürzlich verwendeten Zielen zurückkehren.

        ![Screenshot der Sprungliste mit dem Gruppennamen "zuletzt" ](images/winenv-taskbar-image36.png)

        In diesem Beispiel verwendet Windows Notepad zuletzt geöffnete Ziele.

    -   Erwägen Sie die Verwendung von Häufig für Programme, die vorhandene Inhalte anzeigen, bei denen Benutzer wahrscheinlich zu Elementen zurückkehren, die sie häufig verwenden. Häufige Ziele werden nach Häufigkeit sortiert, am häufigsten zuerst.

        ![Screenshot der Sprungliste mit häufigen Gruppennamen ](images/winenv-taskbar-image37.png)

        In diesem Beispiel verwendet Windows-Explorer häufige Ziele.

    -   Verwenden Sie Häufig, wenn Zuletzt verwendet zu vielen unnötigen Zielen führen würde. Häufige Listen sind stabiler und die bessere Wahl, wenn Benutzer zu vielen verschiedenen Zielen wechseln, aber wahrscheinlich nicht zu selten verwendeten Zielen zurückkehren.

        **Falsch:**

        ![Screenshot der Sprungliste mit mehreren aktuellen Elementen ](images/winenv-taskbar-image38.png)

        Die Verwendung von Recent in Windows Internet Explorer würde zu vielen unnötigen Zielen führen.

    -   Wenn Zuletzt verwendet oder Häufig gleich geeignete Optionen sind, verwenden Sie Zuletzt verwendet, da dieser Ansatz für Benutzer einfacher zu verstehen ist und besser vorhersagbar ist.
    -   Wenn Sie Zuletzt verwendet und das Programm im Menü Datei über eine Entsprechung verfügt, stellen Sie sicher, dass die Listen denselben Inhalt in der gleichen Reihenfolge aufweisen. Für Benutzer sollten diese listengleich sein.

-   **Verwenden Sie bei Bedarf eine benutzerdefinierte Zielliste.** Ihr Programm hat vollständige Kontrolle über den Inhalt und die Sortierreihenfolge einer benutzerdefinierten Zielliste und kann die Liste daher auf beliebigen Faktoren basieren.
    -   Erstellen Sie benutzerdefinierte Versionen von Zuletzt verwendet oder Häufig, wenn diese geeignet sind, aber die automatische Verwaltung für Ihr Programm nicht gut funktioniert. Beispielsweise muss Ihr Programm möglicherweise eine Vielzahl von Faktoren nachverfolgen, die über offene Dateibefehle hinausgehen. Verwenden Sie in diesem Fall den gleichen Namen (Zuletzt verwendet oder Häufig) und die Sortierreihenfolge, da Benutzer den Unterschied nicht kennen.
    -   Verwenden Sie andernfalls einen anderen Zieltyp, um die Ziele Ihres Benutzers besser zu erfüllen. Häufig helfen diese Listen Benutzern beim Ausführen von Aufgaben, die sie noch nicht ausgeführt haben, z. B. das Lesen neuer Nachrichten, das Ansehen neuer Videos oder das Überprüfen der nächsten Besprechung.

        ![Screenshot der Sprungliste mit dem Gruppennamen "new" ](images/winenv-taskbar-image39.png)

        In diesem Beispiel listet Windows Media Center die zuletzt aufgezeichneten Aufzählungen auf, die der Benutzer noch nicht gesehen hat.

    -   Wählen Sie eine Sortierreihenfolge aus, die dem mentalen Modell des Benutzers der Liste entspricht. Für eine To-Do-Stilliste wird beispielsweise zuerst das Nächste aufgeführt, was Sie tun müssen. Wenn kein klares mentales Modell vorhanden ist, sortieren Sie die Zielliste in alphabetischer Reihenfolge.

-   **Verwenden Sie nicht mehrere Ziellisten, die unterschiedliche Ansichten derselben Daten enthalten.** Stattdessen sollten mehrere Ziellisten größtenteils unterschiedliche Daten enthalten, um unterschiedliche Szenarien zu unterstützen. Sie können z. B. eine Liste Zuletzt vorhanden oder häufig angeben, aber nicht beides. Dies ist verschwendung, wenn überlappende Elemente vorhanden sind, aber verwirrend, wenn überlappende Elemente entfernt werden.

    **Falsch:**

    ![Screenshot der Sprungliste mit wiederholten Gruppenelementen ](images/winenv-taskbar-image40.png)

    In diesem Beispiel ist es verschwendung, verschiedene Ansichten derselben Ziele bereitzustellen.

    **Richtig:**

    ![Screenshot der Sprungliste mit gut organisierten Aufgaben ](images/winenv-taskbar-image41.png)

    In diesem Beispiel verfügen die Ziellisten über unterschiedliche Daten für verschiedene Aufgaben.

-   **Wenn Ihr Programm über einen Befehl zum Löschen von Daten für den Datenschutz verfügt, löschen Sie auch die Listen Ziele.** Ziellisten können vertrauliche Daten enthalten.

### <a name="thumbnail-toolbars"></a>Miniaturansichtssymbolleisten

**Interaktion**

-   **Stellen Sie bis zu sieben der wichtigsten, häufig verwendeten Befehle bereit, die für das in der Miniaturansicht angezeigte Fenster gelten.** Denken Sie nicht daran, so viele Befehle wie sie können bereitzustellen, wenn Ihr Programm nur über drei wichtige, häufig verwendete Befehle verfügt und nur drei bereitstellt.

    **Falsch:**

    ![Screenshot der Symbolleiste mit zu vielen Befehlen ](images/winenv-taskbar-image42.png)

    In diesem Beispiel enthält die Miniaturansichtssymbolleiste Befehle, die nicht wichtig sind.

-   **Verwenden Sie Befehle, die direkt und direkt sind.** Diese Befehle sollten sofortige Auswirkungen haben, wenn Sie auf den Befehl klicken, um kein Dropdownmenü oder Dialogfeld für weitere Eingaben anzuzeigen.

    **Falsch:**

    ![Screenshot der Miniaturansicht mit Dropdownmenü ](images/winenv-taskbar-image43.png)

    Befehle der Miniaturansichtssymbolleiste müssen sofort wirksam sein.

-   **Deaktivieren Sie Befehle, die nicht für den aktuellen Kontext gelten oder direkt zu einem Fehler führen würden.** Blenden Sie solche Befehle nicht aus, da dadurch die Darstellung der Symbolleiste instabil wird.
-   **Verkleinern Sie die Miniaturansicht nicht, wenn Benutzer auf einen Befehl klicken, wenn sie wahrscheinlich die Ergebnisse überprüfen oder sofort auf einen anderen Befehl klicken.** Entfernen Sie die Miniaturansicht für Befehle, die angeben, dass der Benutzer vorer zeit fertig ist, z. B. mit Befehlen, die andere Fenster anzeigen.

    ![Screenshot der Media Player-Miniaturansicht mit dem Befehl ](images/winenv-taskbar-image44.png)

    In diesem Beispiel wird beim Klicken auf Weiter in Windows Media Player weiterhin die Miniaturansicht angezeigt, da Benutzer möglicherweise andere Befehle geben möchten.

    ![Screenshot der Miniaturansicht mit Chatsymbol ](images/winenv-taskbar-image45.png)

    In diesem Beispiel wird durch Klicken auf Chat in Windows Live Messenger die Miniaturansicht verworfen, da Benutzer wahrscheinlich eine Nachricht senden.

**Präsentation**

-   **Stellen Sie sicher, dass Symbolleistensymbole für Miniaturansichten den Richtlinien für Symbole im Stil von Stilen entsprechen.** Stellen Sie für jeden Befehl hochwertige 16x16-, 20x20- und 24 x 24-Pixel-Vollfarbsymbole zur Verfügung. Die größeren Versionen werden in Anzeigemodi mit hohem DPI-Anteil verwendet.
-   **Stellen Sie sicher, dass die Symbole für die Hintergrundfarbe der Symbolleiste sowohl im normalen als auch im Hoverzustand deutlich sichtbar sind.** Werten Sie Symbole immer im Kontext und im Modus mit hohem Kontrast aus.
-   **Wählen Sie Befehlssymbolentwürfe aus, die ihre Wirkung deutlich kommunizieren.** Gut entworfene Befehlssymbole sind selbsterklärend, damit Benutzer Befehle effizient finden und verstehen können.
-   **Wählen Sie Symbole aus, die erkennbar und unterscheidbar sind.** Stellen Sie sicher, dass die Symbole über unterschiedliche Formen und Farben verfügen. Auf diese Weise können Benutzer die Befehle schnell finden, auch wenn sie sich nicht an das Symbolsymbol erinnern. Nach der ersten Verwendung sollten Sich Benutzer nicht auf QuickInfos verlassen müssen, um zwischen den Befehlen zu unterscheiden.
-   **Geben Sie eine QuickInfo an, um die einzelnen Befehle zu beschriften.** Eine gute QuickInfo bezeichnet das Steuerelement ohne Bezeichnung, auf das verwiesen wird. Richtlinien und Beispiele finden Sie unter [QuickInfos und Infotips.](ctrl-tooltips-and-infotips.md)

### <a name="progress-bars"></a>Statusleisten

-   **Befolgen Sie die allgemeinen Statusleistenrichtlinien,** z. B. das Nichtneustarten oder Sichern des Fortschritts, und verwenden Sie eine rote Statusleiste, um auf ein Problem hindeuten.
-   **Vermeiden Sie die Verwendung unbestimmter Statusleisten.** In unbestimmten Statusleisten wird die Aktivität und nicht der Fortschritt angezeigt. Reservieren Sie unbestimmte Statusleisten für die seltenen Situationen, in denen Benutzer keine Aktivität als selbstverständlich ein nehmen.

Weitere Richtlinien finden Sie unter [Statusleisten.](progress-bars.md)

## <a name="text"></a>Text

### <a name="window-titles"></a>Fenstertitel

Berücksichtigen Sie bei der Auswahl von Fenstertiteln die Darstellung des Titels auf der Taskleiste:

-   Optimieren Sie Titel für die Anzeige auf der Taskleiste, indem Sie die unterscheidenden Informationen präzise an erster Stelle platzieren.
-   Für Dialogfelder für den statuslosen Status fassen Sie zunächst den Fortschritt zusammen. Beispiel: "66 % abgeschlossen".
-   Vermeiden Sie Fenstertitel, die umkrüme Abgeschnitten haben.

    **Falsch:**

    ![Screenshot des Titels, der den Programmnamen ausschneidet ](images/winenv-taskbar-image48.png)

    In diesem Beispiel verfügt der abgeschnittene Fenstertitel über ergebnisschädigende Ergebnisse.

### <a name="jump-list-commands"></a>Sprungliste-Befehle

-   **Starten Sie Befehle mit einem Verb.**
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**

Weitere Richtlinien für Befehlsbezeichnungen finden Sie unter [Menüs](cmd-menus.md).

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf die Taskleiste:

-   Verweisen Sie auf die gesamte Leiste als Taskleiste (ein einzelnes zusammengesetztes Wort in Kleinbuchstaben).
-   Verweisen Sie auf Elemente auf der Taskleiste speziell nach ihrer Bezeichnung oder im Allgemeinen als Taskleistenschaltflächen.
-   Formatieren Sie die Taskleistenbezeichnungen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.
-   Überlagerungssymbole werden als Symbole für Taskleistenschaltfläche bezeichnet. Verweisen Sie nicht auf sie als Benachrichtigungen, auch wenn ihr Zweck die Benachrichtigung von Benutzern ist. Sie können jedoch sagen, dass diese Symbole Benutzer über bestimmte Ereignisse benachrichtigen.

Beispiel: Das Schaltflächensymbol Neue E-Mail-Taskleiste benachrichtigt Sie, dass eine neue E-Mail-Nachricht eingetroffen ist.

 


---
title: Infobereich
description: Der Infobereich enthält Benachrichtigungen und status. Gut entworfene Programme verwenden den Benachrichtigungsbereich entsprechend, ohne mäßig oder ablenkend zu sein.
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c580d80bd95684cc80dc24e59273553f4a08e11f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985453"
---
# <a name="notification-area"></a>Infobereich

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Der Infobereich enthält Benachrichtigungen und status. Gut entworfene Programme verwenden den Benachrichtigungsbereich entsprechend, ohne mäßig oder ablenkend zu sein.

Der Infobereich ist ein Teil der Taskleiste, der eine temporäre Quelle für Benachrichtigungen und Status bereitstellt. Es kann auch verwendet werden, um Symbole für System- und Programmfeatures anzuzeigen, die nicht auf dem Desktop vorhanden sind.

Elemente im Benachrichtigungsbereich werden als Benachrichtigungsbereichssymbole oder einfach Symbole bezeichnet, wenn der Kontext des Benachrichtigungsbereichs bereits eindeutig festgelegt ist.

![Screenshot von Benachrichtigungsbereich, Uhrzeit und Datum ](images/winenv-notification-image1.png)

Der Benachrichtigungsbereich.

Um Benutzern die Kontrolle über ihren Desktop in Windows 7 zu geben, werden nicht alle Symbole für den Benachrichtigungsbereich standardmäßig angezeigt. Stattdessen werden Symbole im Infobereichsüberlauf angezeigt, es sei denn, sie werden vom Benutzer in den Infobereich heraufgestuft.

![Screenshot: Benachrichtigungsbereich und Überlauf](images/winenv-notification-image2.png)

Der Benachrichtigungsbereichsüberlauf.

**Hinweis:** Richtlinien in Bezug auf die [Taskleiste,](winenv-taskbar.md) [Benachrichtigungen](mess-notif.md) und [Sprechblasen](ctrl-balloons.md) werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Muss ihr Programm eine Benachrichtigung anzeigen?** In diesem Falle müssen Sie ein Symbol für den Benachrichtigungsbereich verwenden.
-   **Wird das Symbol vorübergehend angezeigt, um eine Statusänderung anzuzeigen?** In diesem Falle kann je nach den folgenden Faktoren ein Symbol für den Benachrichtigungsbereich geeignet sein:

    -   **Ist der Status nützlich und relevant?** Das heißt, werden Benutzer das Symbol wahrscheinlich überwachen und ihr Verhalten aufgrund dieser Informationen ändern? Wenn nicht, zeigen Sie entweder den Status nicht an, oder speichern Sie ihn in einer Protokolldatei.

        **Falsch:**

        ![Screenshot des Infobereichs mit Laufwerksymbol ](images/winenv-notification-image3.png)

        In diesem Beispiel ist das Aktivitätssymbol des Datenträgerlaufwerks ungeeignet, da Benutzer ihr Verhalten wahrscheinlich nicht entsprechend ändern werden.

    -   **Ist der Status kritisch? Ist sofortige Aktion erforderlich?** Wenn ja, zeigen Sie die Informationen auf eine Weise an, die Aufmerksamkeit erfordert und nicht einfach ignoriert werden kann, z. B. ein [Dialogfeld](win-dialog-box.md).

    Programme, die für Windows 7 entwickelt wurden, können Überlagerungssymbole auf der Taskleistenschaltfläche des Programms verwenden, um Statusänderungen anzuzeigen, sowie Statusleisten der Taskleistenschaltfläche, um den Fortschritt von Zeittasks anzuzeigen.

-   **Verfügt das Feature bereits über "Desktopdarstellung"?** Wird das Feature bei der Ausführung also in einem Fenster auf dem Desktop angezeigt (möglicherweise minimiert)? Wenn ja, zeigen Sie den Status in der [Statusleiste](ctrl-status-bars.md)des Programms, in einem anderen Statusbereich oder für Windows 7 direkt auf der Taskleistenschaltfläche an. Wenn das Feature nicht auf dem Desktop vorhanden ist, können Sie ein Symbol für den Programmzugriff und zum Anzeigen des Status verwenden.
-   **Ist das Symbol in erster Linie dafür, ein Programm zu starten oder schnell auf seine Features oder Einstellungen zuzugreifen?** Verwenden Sie in diesem Falle die Startmenü, um stattdessen Programme zu starten. Der Benachrichtigungsbereich ist nicht für den schnellen Programm- oder Befehlszugriff vorgesehen.

    ![Screenshot der Schnellstartsymbolleiste ](images/winenv-notification-image4.png)

    In diesem Beispiel von Windows Vista aus wird Schnellstart verwendet, um Windows Explorer und Windows Internet Explorer schnell zu starten.

    Für Programme, die für Windows 7 entwickelt wurden, können Benutzer Taskleistenschaltflächen für den schnellen Programmzugriff anheften. Programme können eine Sprungliste- oder Miniaturansichtssymbolleiste verwenden, um direkt über die Symbolleistenschaltfläche eines Programms auf häufig verwendete Befehle zuzugreifen. Der bereich Schnellstart wird in Windows 7 standardmäßig nicht angezeigt.

    ![Screenshot der Taskleiste und Sprungliste mit Symbolen ](images/winenv-notification-image5.png)

    In diesem Beispiel wird ein Sprungliste für den schnellen Befehlszugriff verwendet.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="the-windows-desktop"></a>Der Windows Desktop

Der Windows Desktop verfügt über die folgenden Programmzugriffspunkte:

-   **Arbeitsbereich.** Der Bildschirmbereich, in dem Benutzer ihre Arbeit ausführen sowie Programme, Dokumente und ihre Verknüpfungen speichern können. Obwohl der Desktop technisch gesehen die Taskleiste enthält, bezieht er sich in den meisten Kontexten nur auf den Arbeitsbereich.
-   **Schaltfläche "Start".** Der Zugriffspunkt für alle Programme und speziellen Windows Orte (Dokumente, Bilder, Musik, Spiele, Computer, Systemsteuerung) mit Listen "Zuletzt verwendet" für den schnellen Zugriff auf zuletzt verwendete Programme und Dokumente.
-   **Schnellstart.** Ein direkter Zugriffspunkt für vom Benutzer ausgewählte Programme. Schnellstart wurde aus Windows 7 entfernt.
-   **Taskleiste.** Der Zugriffspunkt für ausgeführte Programme mit Desktopdarstellung. Obwohl die Taskleiste technisch gesehen den gesamten Balken vom Schaltfläche "Start" bis zum Benachrichtigungsbereich umfasst, bezieht sich die Taskleiste in den meisten Kontexten auf den Bereich dazwischen, der die Taskleistenschaltflächen enthält. Dieser Bereich wird manchmal auch als Taskband bezeichnet.
-   **Deskbands. Nicht empfohlen.**
-   **Benachrichtigungsbereich.** Eine kurzfristige Quelle für Benachrichtigungen und Status sowie ein Zugriffspunkt für system- und programmbezogene Features, die nicht auf dem Desktop vorhanden sind.

![Screenshot: Identifizieren von Desktopzugriffspunkten ](images/winenv-notification-image6.png)

Die Windows Desktopzugriffspunkte umfassen den Schaltfläche "Start", die Taskleiste und den Benachrichtigungsbereich. Beachten Sie die Miniaturansichtsfunktion der Taskleistenschaltfläche.

**Der Desktop ist eine eingeschränkte, freigegebene Ressource, die der Einstiegspunkt des Benutzers für Windows ist.** Lassen Sie Benutzer die Kontrolle. Sie sollten die Desktopbereiche wie vorgesehen verwenden. Jede andere Nutzung sollte als Missbrauch betrachtet werden. Beispielsweise können Sie Desktopbereiche niemals als Möglichkeiten zum Bewerben Ihres Programms oder seiner [Marke](exper-branding.md)anzeigen.

### <a name="using-the-notification-area-appropriately"></a>Geeignete Verwendung des Benachrichtigungsbereichs

Der Infobereich war ursprünglich als temporäre Quelle für Benachrichtigungen und Status vorgesehen. Seine Effizienz und Benutzerfreundlichkeit hat Entwicklern empfohlen, ihr andere Zwecke zu bieten, z. B. das Starten von Programmen und das Ausführen von Befehlen. Leider haben diese Ergänzungen den Benachrichtigungsbereich zu groß und laut gemacht und den Zweck mit den anderen Desktopzugriffspunkten verwechselt.

Windows XP hat das Skalierungsproblem behoben, indem der Bereich reduzierbar gemacht und die nicht verwendeten Symbole ausgeblendet wurden. Windows Vista hat das Rauschen behoben, indem unnötige, störungende Benachrichtigungen entfernt wurden. Windows 7 ist einen Schritt weiter gegangen, indem die Benachrichtigung auf ihren ursprünglichen Zweck als Benachrichtigungsquelle konzentriert wurde. **Die meisten Symbole werden standardmäßig in Windows 7 ausgeblendet, können jedoch manuell vom Benutzer in den Benachrichtigungsbereich heraufgestuft werden. Damit Benutzer die Kontrolle über ihre Desktops behalten, gibt es für Ihr Programm keine Möglichkeit, diese Heraufstufung automatisch durchzuführen.** Windows zeigt weiterhin Benachrichtigungen für ausgeblendete Symbole an, indem sie vorübergehend heraufstaufst.

![Screenshot des Infobereichs und des Überlaufs ](images/winenv-notification-image7.png)

In Windows 7 sind die meisten Symbole für den Benachrichtigungsbereich standardmäßig ausgeblendet.

Darüber hinaus unterstützt Windows 7 viele Funktionen direkt in den Taskleistenschaltflächen. Insbesondere können Sie Folgendes verwenden:

-   Sprunglisten und Miniaturansichtssymbolleisten, um schnell auf häufig verwendete Befehle zuzugreifen.
-   Überlagerungssymbole zum Anzeigen des Status für ausgeführte Programme.
-   Statusanzeigen der Taskleistenschaltfläche, um den Fortschritt für Aufgaben mit langer Ausführungslaufzeit anzuzeigen.

Kurz gesagt: Wenn Ihr Programm über Desktop-Präsenz verfügt, nutzen Sie für diese Zwecke die Funktionen der Windows 7 Taskleistenschaltfläche in vollem Umfang. **Behalten Sie die Symbole des Benachrichtigungsbereichs bei, um Benachrichtigungen und Status anzuzeigen.**

### <a name="keeping-users-in-control"></a>Behalten der Kontrolle über Benutzer

Die Kontrolle der Benutzer geht über die korrekte Verwendung des Benachrichtigungsbereichs hinaus. Abhängig von der Art Ihres Symbols können Sie benutzern folgende Schritte ermöglichen:

-   **Entfernen Sie das Symbol.** Ihr Symbol kann einen relevanten, nützlichen Status bereitstellen, aber trotzdem möchten Benutzer ihn möglicherweise nicht sehen. Windows ermöglicht Benutzern das Ausblenden von Symbolen, aber dieses Feature ist nicht leicht erkennbar. Um die Kontrolle über Benutzer zu behalten, geben Sie im Kontextmenü des Symbols die Option **Symbol im Benachrichtigungsbereich anzeigen** an. Beachten Sie, dass sich das Entfernen eines Symbols nicht auf das zugrunde liegende Programm, das zugrunde liegende Feature oder den zugrunde liegenden Prozess auswirken muss.
-   **Wählen Sie typen von Benachrichtigungen aus, die angezeigt werden sollen.** Ihre Benachrichtigung muss nützlich und relevant sein, aber es gibt möglicherweise Benachrichtigungen, die Benutzer nicht sehen möchten. Dies gilt insbesondere für [FYI-Benachrichtigungen.](mess-notif.md) Ermöglichen Sie Es Benutzern, die weniger wichtigen zu aktivieren.
-   **Optionale Features anhalten.** Symbole werden verwendet, um den Status für Features ohne Desktopdarstellung anzuzeigen. Solche Features sind in der Regel lang andauernde, optionale Hintergrundaufgaben, z. B. Drucken, Indizieren, Scannen oder Synchronisieren. Benutzer möchten diese Features möglicherweise anhalten, um die Systemleistung zu erhöhen, den Stromverbrauch zu reduzieren oder weil sie offline sind.
-   **Beenden Sie das Programm.** Stellen Sie die besser geeignete dieser Optionen bereit:
    -   **Programm vorübergehend beenden.** Das Programm wird beendet und neu gestartet, wenn Windows neu gestartet wird. Dieser Ansatz eignet sich für wichtige Systemprogramme wie Sicherheitsprogramme.
    -   **Programm dauerhaft beenden.** Das Programm wird beendet und nicht neu gestartet, wenn Windows neu gestartet wird (es sei denn, der Benutzer entscheidet sich für einen späteren Neustart). Entweder möchte der Benutzer das Programm nicht mehr ausführen oder das Programm bei Bedarf ausführen, um möglicherweise die Systemleistung zu verbessern.

Obwohl es eine gute Idee ist, die meisten dieser Einstellungen im Kontextmenü des Symbols bereitzustellen, sollte die Standarderfahrung des Programms für die meisten Benutzer geeignet sein. Aktivieren Sie nicht standardmäßig alles, und erwarten Sie, dass Benutzer Features deaktivieren. Aktivieren Sie stattdessen die wichtigen Features standardmäßig, und ermöglichen Sie es Benutzern, zusätzliche Features nach Bedarf zu aktivieren.

**Wenn Sie nur vier Dinge tun...**

1.  Missbrauchen Sie den Benachrichtigungsbereich nicht. Verwenden Sie es nur als Quelle für Benachrichtigungen und Status sowie für Features ohne Desktopdarstellung.
2.  Behalten Sie die Kontrolle über Benutzer. Stellen Sie geeignete Optionen bereit, um das Symbol, seine Benachrichtigungen und die zugrunde liegenden Features zu steuern.
3.  Stellen Sie eine Standarderfahrung dar, die für die meisten Benutzer geeignet ist. Ermöglichen Sie es Benutzern, gewünschte Features zu aktivieren, anstatt zu erwarten, dass sie unerwünschte Features deaktivieren.
4.  Nutzen Sie die Funktionen Windows 7 Taskleistenschaltflächen, um den Status anzuzeigen und die am häufigsten ausgeführten Aufgaben ihres Programms effizient zu gestalten.

## <a name="usage-patterns"></a>Verwendungsmuster

Symbole für den Benachrichtigungsbereich weisen mehrere Verwendungsmuster auf:




| Bezeichnung | Wert |
|--------|-------|
| <strong>Systemstatus und Zugriff</strong><br /> Wird fortlaufend angezeigt, um wichtige, aber nicht kritische Systemstatus anzuzeigen und den Zugriff auf relevante Features und Einstellungen zu ermöglichen. <br /> | Systemfeatures, die Benachrichtigungsbereichssymbole benötigen, weisen keine permanente Desktopdarstellung auf. Kann auch als Benachrichtigungsquelle verwendet werden. <br /><img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br /> In diesem Beispiel werden akku-, netzwerk- und volumesymbole nach Bedarf fortlaufend angezeigt.<br /> | 
| <strong>Status und Zugriff der Hintergrundaufgabe</strong><br /> Wird angezeigt, während eine Hintergrundaufgabe ausgeführt wird, um den Status anzuzeigen und Den Zugriff auf Features und Einstellungen zu ermöglichen. <br /> | Hintergrundprozesse benötigen Benachrichtigungsbereichssymbole, wenn sie nicht auf dem Desktop vorhanden sind. Kann auch als Benachrichtigungsquelle verwendet werden. <br /><img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br /> In diesem Beispiel können Benutzer mit dem Symbol "Action Center" ihren Status auch dann überprüfen, wenn kein Desktop vorhanden ist.<br /> | 
| <strong>Temporärer Ereignisstatus</strong><br /> Programme mit Desktopdarstellung können Symbole vorübergehend anzeigen, um wichtige Ereignisse oder Statusänderungen anzuzeigen. <br /> | <img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br /> In diesem Beispiel werden Symbole zum Drucken und Installieren von Updates vorübergehend angezeigt, um wichtige Ereignisse oder Statusänderungen anzuzeigen.<br /> | 
| <strong>Temporäre Benachrichtigungsquelle</strong><br /> Wird vorübergehend angezeigt, um eine Benachrichtigung anzuzeigen. Wird nach einem Timeout entfernt, oder wenn das zugrunde liegende Problem behoben oder eine Aufgabe ausgeführt wird. <br /> | Temporäre Symbole werden für reine Benachrichtigungsquellen bevorzugt. Zeigen Sie kein Symbol an, das keinen nützlichen, relevanten, dynamischen Status bietet, nur weil ein Feature in Zukunft möglicherweise eine Benachrichtigung anzeigen muss. <br /><img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br /> In diesem Beispiel wird das Plug & Play-Symbol angezeigt, während eine neue hardwareerkennungsbenachrichtigung angezeigt wird.<br /> | 
| <strong>Minimierte Einzelinstanzanwendung</strong><br /> Um die Aufgabenleistenübersicht zu reduzieren, kann eine Einzelinstanzanwendung mit langer Ausführungslaufzeit stattdessen auf ein Symbol für den Benachrichtigungsbereich minimiert werden. <br /> | <img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br /> In diesem Beispiel von Windows Vista sind Outlook und Windows Live Messenger Einzelinstanzanwendungen, die symbole für den Benachrichtigungsbereich minimieren.<br /> Erwägen Sie die Verwendung dieses Musters nur, wenn alle folgenden Punkte zutreffen: <br /><ul><li>Die Anwendung kann nur über eine einzelne -Instanz verfügen.</li><li>Die Anwendung wird über einen längeren Zeitraum ausgeführt.</li><li>Das Symbol zeigt den Status an.</li><li>Das Symbol kann eine Benachrichtigungsquelle sein.</li><li>Dies ist optional, und Benutzer müssen <a href="glossary.md">sich für entscheiden.</a></li></ul>Wenn alle diese Bedingungen erfüllt sind, werden durch die Minimierung auf ein Symbol zwei Zugriffspunkte entfernt, wenn nur einer erforderlich ist. <br /><strong>Hinweis:</strong> Dieses Symbolmuster wird für Windows 7 nicht mehr empfohlen. Verwenden Sie stattdessen reguläre Taskleistenschaltflächen, wenn Ihr Programm über Desktop-Präsenz verfügt.<br /><img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br /> In diesem Beispiel aus Windows 7 nimmt eine reguläre Taskleistenschaltfläche wenig Platz in Anspruch, profitiert aber von den Funktionen der Windows 7 Taskleistenschaltflächen, einschließlich Sprunglisten, Überlagerungssymbolen und umfangreichen Miniaturansichten.<br /> | 




 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Geben Sie pro Komponente nur ein Symbol für den Benachrichtigungsbereich an.**
-   **Verwenden Sie ein Symbol mit 16 x 16, 20 x 20 und 24 x 24 Pixeln.** Die größeren Versionen werden in Anzeigemodi mit hohen DPI-Daten verwendet.

### <a name="when-to-show"></a>Wann sollte angezeigt werden?

-   Für das Muster der temporären Benachrichtigungsquelle:
    -   Windows zeigt das Symbol an, wenn die Benachrichtigung angezeigt wird.
    -   Entfernen Sie das Symbol basierend auf seinem [Benachrichtigungsentwurfsmuster:](mess-notif.md)



    | Muster                                     | Zeitpunkt des Entfernens                                         |
    |--------------------------------------|------------------------------------------|
    | Aktion erfolgreich<br/>            | Wenn die Benachrichtigung entfernt wird.<br/> |
    | Aktionsfehler<br/>            | Wenn das Problem behoben ist.<br/>     |
    | Nicht kritisches Systemereignis<br/> | Wenn das Problem behoben ist.<br/>     |
    | Optionale Benutzeraufgabe<br/>        | Wenn die Aufgabe abgeschlossen ist.<br/>            |
    | FYI<br/>                       | Wenn die Benachrichtigung entfernt wird.<br/> |



 

-   **Zeigen Sie für das temporäre Ereignisstatusmuster das Symbol an, während das Ereignis stattfindet.**
-   Zeigen Sie für alle anderen Muster **das Symbol an, wenn das Programm, das Feature oder der Prozess ausgeführt wird und das Symbol relevant ist,** es sei denn, der Benutzer hat seine Option **Symbol im Benachrichtigungsbereich anzeigen** gelöscht (weitere Informationen finden Sie unter [Kontextmenüs](#context-menus)). Die meisten Symbole sind standardmäßig in Windows 7 ausgeblendet, können jedoch vom Benutzer in den Benachrichtigungsbereich heraufgestuft werden.
-   **Zeigen Sie keine Symbole an, die für Administratoren für Standardbenutzer vorgesehen sind.** Notieren Sie sich die Informationen im Windows Ereignisprotokoll.

### <a name="where-to-show"></a>Anzeigen des Orts

-   **Anzeigen von Fenstern, die über Symbole im Infobereich in der Nähe des Infobereichs gestartet werden.**

![Abbildung eines Fensters in der Nähe des Infobereichs ](images/winenv-notification-image14.png)

Windows, die über Benachrichtigungsbereichssymbole gestartet werden, werden in der Nähe des Infobereichs angezeigt.

### <a name="icons"></a>Symbole

-   **Wählen Sie das Symbol basierend auf seinem Entwurfsmuster aus:**

    | Muster                                                 | Symboltyp                                   |
    |--------------------------------------------------|------------------------------------|
    | Systemstatus und Zugriff<br/>              | Symbol für Systemfeatures<br/>     |
    | Status und Zugriff der Hintergrundaufgabe<br/>     | Programm- oder Featuresymbol<br/> |
    | Temporäre Benachrichtigungsquelle<br/>         | Symbol "Programm" oder "Feature"<br/> |
    | Temporärer Ereignisstatus<br/>                | Symbol "Programm" oder "Feature"<br/> |
    | Minimierte Einzelinstanzanwendung<br/> | Programmsymbol<br/>            |

    

     

    ![Screenshot des Benachrichtigungsbereichs und der Outlook-Symbole ](images/winenv-notification-image15.png)

    In diesem Beispiel verwendet Outlook ein E-Mail-Featuresymbol für eine temporäre Benachrichtigungsquelle und das Anwendungssymbol für die minimierte Anwendung.

-   **Wählen Sie ein leicht erkennbares Symboldesign aus.** Bevorzugen Sie Symbole mit eindeutigen Konturen gegenüber quadratischen oder rechteckigen, formten Symbolen. Halten Sie die Entwürfe einfach, und bevorzugen Sie Symbole gegenüber realistischen Bildern. Wenden Sie auch die anderen Richtlinien für Symbole [im Stil von Sollen](vis-icons.md) an.
-   **Verwenden Sie Symbolvarianten oder Überlagerungen, um Status- oder Statusänderungen anzuzeigen.** Verwenden Sie Symbolvarianten, um Änderungen an Mengen oder Stärken anzuzeigen. Verwenden Sie für andere Statustypen die folgenden Standardüberlagerungen. Verwenden Sie nur eine einzelne Überlagerung, und suchen Sie sie aus Konsistenz-Grund nach rechts unten. 

    | Überlagerung                                                                                                       | Status                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![Screenshot des Symbols für kleine Warnungen ](images/winenv-notification-image16.png)<br/>               | Warnung<br/>               |
    | ![Screenshot des kleinen Fehlersymbols ](images/winenv-notification-image17.png)<br/>                 | Fehler<br/>                 |
    | ![Screenshot des Symbols "Klein deaktiviert/getrennt" ](images/winenv-notification-image18.png)<br/> | Deaktiviert/Getrennt<br/> |
    | ![Screenshot des kleinen blockierten/offline-Symbols ](images/winenv-notification-image19.png)<br/>       | Blockiert/Offline<br/>       |

    

     

    ![Screenshot des Benachrichtigungsbereichs und zweier Symbole ](images/winenv-notification-image20.png)

    In diesem Beispiel zeigen die Drahtlos- und Akkusymbole Änderungen an Mengen oder Stärken an.

    ![Screenshot des Benachrichtigungsbereichs und zweier Überlagerungen ](images/winenv-notification-image21.png)

    In diesem Beispiel werden Überlagerungen verwendet, um Fehler- und Warnungszustände zu zeigen.

-   **Vermeiden Sie Swaths von reinen Roten, Gelben und Grünen in Ihren Basissymbolen.** Um Verwirrung zu vermeiden, reservieren Sie diese Farben, um den Status zu kommunizieren. Wenn Ihr [Branding diese](exper-branding.md) Farben verwendet, erwägen Sie die Verwendung von stummgeschalteten Tönen für Ihre Basissymbole für den Benachrichtigungsbereich.
-   Verwenden [Sie für die](mess-notif.md)progressive Eskalation Symbole mit einem progressiv emphatischen Aussehen, wenn die Situation **dringender wird.**

    ![Screenshot des Benachrichtigungsbereichs und fünf Symbole ](images/winenv-notification-image22.png)

    In diesen Beispielen wird das Aussehen des Akkusymbols mit zunehmender Dringendkeit deutlich.

-   **Ändern Sie den Status nicht zu häufig.** Benachrichtigungsbereichssymbole sollten nicht laut, instabil oder erfordern keine Aufmerksamkeit. Das Auge ist empfindlich auf Änderungen im Peripheriebereich des Sehens, daher müssen Statusänderungen dezent sein.
    -   **Ändern Sie das Symbol nicht schnell.** Wenn sich der zugrunde liegende Status schnell ändert, muss das Symbol den Status auf hoher Ebene widerspiegeln.

        **Falsch:**

        ![Screenshot des Benachrichtigungsbereichs und des Modemsymbols ](images/winenv-notification-image23.png)

        In diesem Beispiel zeigt das Modemsymbol Blinklichter an (wie ein Hardwaremodem), aber diese Zustandsänderungen sind für Benutzer nicht von Bedeutung.

    -   **Verwenden Sie keine Animationen mit langer Laufzeit, um kontinuierliche Aktivitäten zu zeigen.** Solche Animationen sind abgelenkt. Das Vorhandensein eines Symbols im Benachrichtigungsbereich zeigt eine kontinuierliche Aktivität ausreichend an.
    -   **Kurze, subtile Animationen sind akzeptabel, um den Fortschritt bei wichtigen temporären, transitiven Statusänderungen anzuzeigen.**

        ![Screenshot des Benachrichtigungsbereichs und des Drahtlossymbols ](images/winenv-notification-image24.png)

        In diesem Beispiel zeigt das Symbol Drahtlos einen Aktivitätsindikator an, um anzuzeigen, dass die Arbeit in Bearbeitung ist.

    -   **Blinken Sie nicht auf das Symbol.** Dies ist zu störend. Wenn ein Ereignis sofortige Aufmerksamkeit erfordert, verwenden Sie stattdessen ein Dialogfeld. Wenn das Ereignis andernfalls eine Aufmerksamkeit erfordert, verwenden Sie eine Benachrichtigung.

-   **Deaktivieren Sie keine Symbole für den Benachrichtigungsbereich.** Wenn das Symbol derzeit nicht angewendet wird, entfernen Sie es. Sie können jedoch ein aktiviertes Symbol mit einer deaktivierten Statusüberlagerung anzeigen, wenn Benutzer dies über das Symbol aktivieren können.

    ![Screenshot des Benachrichtigungsbereichs und des Volumeschiebereglers ](images/winenv-notification-image25.png)

    In diesem Beispiel können Benutzer die Soundausgabe über das Symbol aktivieren.

Allgemeine Symbolrichtlinien und Beispiele finden Sie unter [Symbole](vis-icons.md).

### <a name="interaction"></a>Interaktion

**Hinweis:** Die folgenden Klickereignisse sollten bei der Maus nach oben und nicht bei der Maus nach unten auftreten.

**Darauf zeigen (Hover)**

-   **Zeigt eine QuickInfo oder infotip an, die angibt, was das Symbol darstellt.**

    ![Screenshot des Benachrichtigungsbereichs und der QuickInfo ](images/winenv-notification-image26.png)

    In diesem Beispiel wird eine QuickInfo verwendet, um das Symbol beim Hovern zu beschreiben.

Richtlinien für Infotip-Text finden Sie im [Abschnitt Text](#context-menus) dieses Artikels.

**Linker Einzelklick**

-   **Zeigen Sie an, was Benutzer am wahrscheinlichsten sehen** möchten. Dies kann folgendes sein:

    -   Ein Flyoutfenster, Dialogfeld oder Programmfenster mit den nützlichsten Einstellungen und häufig ausgeführten Aufgaben. Präsentationsrichtlinien finden Sie unter [Flyouts für den Benachrichtigungsbereich.](#notification-area-flyouts)

        ![Screenshot des Benachrichtigungsbereichs und der Flyouts ](images/winenv-notification-image27.png)

        In diesen Beispielen werden beim Klicken mit der linken Maustaste Popupfenster mit den nützlichsten Einstellungen angezeigt.

    -   Ein Status-Flyout.

        ![Screenshot des Benachrichtigungsbereichs und des Status-Flyouts ](images/winenv-notification-image28.png)

        In diesem Beispiel wird beim Klicken mit der linken Maustaste das Status-Flyout angezeigt.

        -   Das zugehörige Systemsteuerungselement.
        -   Das Kontextmenü.

    Benutzer erwarten, dass mit nur einem Klick etwas angezeigt wird, sodass ein Benachrichtigungsbereichssymbol nicht reagiert, wenn nichts angezeigt wird.

-   **Zeigen Sie ein Kontextmenü nur an, wenn die anderen** Optionen nicht angewendet werden, und verwenden Sie dabei den Standardbefehl fett. Zeigen Sie in diesem Fall das gleiche Kontextmenü an, das beim Rechtsklick angezeigt wird, um Verwirrung zu vermeiden.
-   **Bevorzugen Sie die Verwendung eines Popupfensters gegenüber einem Dialogfeld,** um ein schlankeres Gefühl zu haben. Zeigen Sie nur die gängigsten Einstellungen an, und lassen Sie sie sofort wirksam werden, um eine einfachere Interaktion zu ermöglichen. Schließen Sie das Popupfenster, wenn der Benutzer auf eine beliebige Stelle außerhalb des Fensters klickt.
-   **Zeigen Sie kleine Fenster in der Nähe des zugeordneten Symbols an.** Große Fenster wie Systemsteuerungselemente können jedoch in der Mitte des Standardmonitors angezeigt werden.

**Doppelklick auf die linke Seite**

-   **Führen Sie den Standardbefehl im Kontextmenü aus.** In der Regel wird die primäre Benutzeroberfläche angezeigt, die dem Symbol zugeordnet ist, z. B. das zugeordnete Systemsteuerungselement, Eigenschaftenblatt oder Programmfenster.
-   **Wenn es keinen Standardbefehl gibt, führen Sie die gleiche Aktion wie ein linker Einzelklick aus.**

**Klicken Sie mit der rechten Maustaste auf**

-   **Zeigen Sie das Kontextmenü** mit dem Standardbefehl fett an.

### <a name="context-menus"></a>Kontextmenüs

-   **Zeigen Sie das Kontextmenü in der Nähe des zugehörigen Symbols an,** aber weg von der Taskleiste.
-   **Das Kontextmenü kann die folgenden Elemente** in der angegebenen Reihenfolge enthalten (genauer Text ist in Anführungszeichen angegeben):

Primäre Befehle

Öffnen (Standard, Liste zuerst, fett formatiert)

Ausführen

Sekundäre Befehle

< Trennzeichen>

Befehl zum Aktivieren/Deaktivieren von "Suspend/Resume" (Häkchen)

"Minimiert bis zum Benachrichtigungsbereich" (Häkchen)

Aktivieren von Benachrichtigungen (Häkchen)

"Symbol im Benachrichtigungsbereich anzeigen" (Häkchen)

< Trennzeichen>

"Optionen"

"Exit"

-   **Entfernen Sie kontextmenüelemente, die nicht gelten, anstatt sie zu deaktivieren.**
-   Geben Sie für die Befehle "Öffnen", "Ausführen" und "Aussetzen/Fortsetzen" genau an, was **geöffnet, ausgeführt,** angehalten und fortgesetzt wird.

![Screenshot: Benachrichtigungsbereich und Befehle](images/winenv-notification-image29.png)

In diesem Beispiel verfügt Windows Defender über spezifische Open- und Run-Befehle.

-   **Verwenden Sie Die Ausführung von Hintergrundaufgaben mit Suspend/Resume, aktivieren/deaktivieren Sie für alle anderen Aufgaben.**
-   **Verwenden Sie Häkungszeichen, um den Zustand anzugeben.** Listen Sie alle Zustände auf, aktivieren Sie sie, und platzieren Sie das Häkchen neben dem aktuellen Zustand. Deaktivieren Sie keine Optionen, oder ändern Sie die Optionsbezeichnungen nicht, um den aktuellen Zustand anzugeben.

**Richtig:**

![Screenshot eines Befehls mit Häkchen ](images/winenv-notification-image29.png)

**Falsch:**

![Screenshot eines Befehls ohne Häkchen ](images/winenv-notification-image30.png)

Im falschen Beispiel Windows Defender ein Häkchen verwenden, um den aktuellen Zustand anzugeben.

-   **Alle Hintergrundaufgaben müssen über den Befehl "Suspend/Resume" verfügen.** Wenn Sie den Befehl auswählen, sollte die Aufgabe vorübergehend angehalten werden. Möglicherweise möchten Benutzer Hintergrundaufgaben vorübergehend aussetzen, um die Systemleistung zu erhöhen oder den Energieverbrauch zu reduzieren. Angehaltene Hintergrundaufgaben werden neu gestartet, wenn sie vom Benutzer fortgesetzt oder Windows neu gestartet werden.
-   **Ermöglichen Sie es Benutzern, unterschiedliche** Benachrichtigungstypen zu aktivieren oder zu deaktivieren, wenn Ihr Programm Benachrichtigungen hat, die einige Benutzer möglicherweise nicht sehen möchten. Das [FYI-Benachrichtigungsmuster](mess-notif.md) erfordert, dass Benutzer sich dafür entscheiden, sodass diese Benachrichtigungen standardmäßig deaktiviert werden müssen.

![Screenshot des Benachrichtigungsbereichs und der Befehle ](images/winenv-notification-image31.png)

In diesem Beispiel Outlook Benutzer die Benachrichtigungen auswählen, die sie über das Symbol erhalten.

-   **Wenn Sie die Option "Symbol im Benachrichtigungsbereich anzeigen"** deaktivieren, wird das Symbol aus dem Benachrichtigungsbereich entfernt, wirkt sich jedoch nicht auf das zugrunde liegende Programm, feature oder process aus. Benutzer können das Symbol im Dialogfeld Optionen des Programms erneut anzeigen. Das Symbol wird nicht automatisch erneut angezeigt, wenn Windows neu gestartet wird.
-   **Mit dem Befehl Beenden wird das Programm für die aktuelle Windows beendet und das Symbol entfernt.** Verwenden Sie keinen Exit-Befehl, wenn das Programm nicht heruntergefahren werden kann. Das Programm wird neu gestartet, wenn Windows neu gestartet wird. Benutzer können das Programm dauerhaft über das Dialogfeld Optionen beenden.
-   **Verwenden Sie keinen About-Befehl.** Diese Informationen sollten über das Symbol, die Infoinfo und das Kontextmenü kommuniziert werden. Wenn Benutzer weitere Informationen wünschen, können sie die primäre Benutzeroberfläche anzeigen.
    -   **Ausnahme:** Sie können einen About-Befehl bereitstellen, wenn das Symbol für ein Programm ohne Desktop-Präsenz ist.

Allgemeine Kontextmenürichtlinien und Beispiele finden Sie unter [Menüs](cmd-menus.md).

### <a name="rich-tooltips"></a>Umfangreiche QuickInfos

-   **Verwenden Sie umfassende QuickInfos nur, um die Informationen leichter verständlich zu machen.** Verwenden Sie nicht nur umfangreiche QuickInfos, um das Feature zu verzieren. Wenn Sie die Informationen nicht mithilfe von RichNess besser verstehen können, verwenden Sie stattdessen eine einfache QuickInfo.

    **Falsch:**

    ![Screenshot: Benachrichtigungsbereich und umfassende QuickInfo ](images/winenv-notification-image32.png)

    **Richtig:**

    ![Screenshot des Benachrichtigungsbereichs und der einfachen QuickInfo ](images/winenv-notification-image33.png)

    Im falschen Beispiel erleichtert das Kalendersymbol das Verständnis des Datums nicht.

-   **Verwenden Sie eine präzise Darstellung.** Verwenden Sie präzisen Text und ein präzises Layout mit einem Symbol mit 32 x 32 Pixeln. Es besteht die Gefahr, dass QuickInfos abgelenkt werden, insbesondere wenn sie unbeabsichtigt angezeigt werden.
-   **Legen Sie keine Steuerelemente oder Elemente, die interaktiv erscheinen, in einer rich-QuickInfo ab.** QuickInfos sind nicht interaktiv und sollten daher nicht interaktiv erscheinen. Verwenden Sie keinen blauen oder unterstrichenen Text.

    **Richtig:**

    ![Screenshot: Rich-QuickInfo mit schwarzem Text ](images/winenv-notification-image34.png)

    **Falsch:**

    ![Screenshot: Umfangreiche QuickInfo mit blauem Text ](images/winenv-notification-image35.png)

    Im falschen Beispiel scheint der aktuelle Energieplan ein Link zu sein, aber es ist nicht möglich, darauf zu klicken.

### <a name="notification-area-flyouts"></a>Flyouts für Benachrichtigungsbereich

-   Stellen Sie gegebenenfalls Flyouts für den Benachrichtigungsbereich mit drei Abschnitten vor:
    -   **Zusammenfassung.** Zeigen Sie die gleichen Informationen an, die in der QuickInfo oder infotip des Symbols angezeigt werden, möglicherweise mit ausführlicheren Informationen. Verwenden Sie zur Konsistenz denselben Text und dieselben Symbole und im Allgemeinen dasselbe Layout (wenn Sie eine umfangreiche QuickInfo verwenden). Im Gegensatz zu den Infotips kann auf diese Informationen zugegriffen werden, wenn touch verwendet wird.
    -   **Allgemeine Aufgaben.** Stellen Sie die am häufigsten ausgeführten Aufgaben direkt im Flyout vor.
    -   **Verwandte Links.** Geben Sie mindestens einen der folgenden optionalen Links an:
        -   Ein Link zur am häufigsten ausgeführten Aufgabe in Systemsteuerung. Geben Sie an, ob eine häufig ausgeführte Aufgabe im Abschnitt allgemeine Aufgaben nicht dargestellt werden kann.
        -   Ein Link zum verknüpften Systemsteuerung Element. Dieses Systemsteuerung sollte Benutzern das Ausführen von Aufgaben ermöglichen, die im Abschnitt allgemeine Aufgaben nicht ausgeführt werden können.
        -   Ein Link zu einem bestimmten, relevanten Hilfethema. Befolgen Sie die [Standardrichtlinien für Hilfelinks.](winenv-help.md)

![Screenshot von Benachrichtigungsbereich und Flyout ](images/winenv-notification-image36.png)

Dieses Beispiel zeigt ein Flyout für den Benachrichtigungsbereich unter Verwendung der empfohlenen Präsentation.

### <a name="options-dialog-box"></a>Optionen (Dialogfeld)

-   Auf Optionen, auf die nicht direkt über das Kontextmenü zugegriffen werden kann, muss sich im Dialogfeld Optionen befindet. Dieser Dialog kann die Systemsteuerung des Features sein.
-   **Das Dialogfeld Optionen kann die folgenden Elemente enthalten** (genauer Text ist in Anführungszeichen angegeben):
    -   Featurename \[ aktivieren \] (Kontrollkästchen)
        -   Wenn Sie diese Option deaktivieren, wird das Programm dauerhaft beendet. Das Programm kann über das Systemsteuerungselement neu gestartet werden. Der Befehl Beenden im Kontextmenü beendet das Programm nur für die aktuelle Windows Sitzung.
    -   "Symbol im Benachrichtigungsbereich anzeigen" (Kontrollkästchen)
        -   Das Entfernen des Symbols aus dem Benachrichtigungsbereich wirkt sich nicht auf das zugrunde liegende Feature aus.
        -   Wenn Sie diese Option auswählen, kann der Benutzer das Symbol wiederherstellen. Dies ist natürlich nicht über das Symbol selbst möglich.
-   Deaktivieren Sie Features, die selten verwendet werden oder potenziell störend oder störend sind. Ermöglichen Sie [es Benutzern, sich für](glossary.md) solche Features zu entscheiden.

Allgemeine Richtlinien und Beispiele für Dialogfelder für Optionen finden Sie unter [Property Windows](win-property-win.md).

### <a name="minimizing-programs-to-the-notification-area"></a>Minimieren von Programmen im Benachrichtigungsbereich

**Hinweis: Die Minimierung von Programmfenstern auf den Benachrichtigungsbereich wird für Windows 7 nicht mehr empfohlen.** Verwenden Sie [stattdessen reguläre Taskleistenschaltflächen.](winenv-taskbar.md) Ihr Programm unterstützt möglicherweise beide Mechanismen zur Abwärtskompatibilität.

-   Um die Übersichtlichkeit der Taskleiste zu reduzieren, sollten Sie die Möglichkeit in Betracht ziehen, Programme nur dann für den Benachrichtigungsbereich zu minimieren, wenn alle der folgenden Punkte zu beachten sind:
    -   Das Programm kann nur eine einzelne Instanz haben.
    -   Das Programm wird für einen längeren Zeitraum ausgeführt.
    -   Das Symbol zeigt den Status an.
    -   Das Symbol kann eine Benachrichtigungsquelle sein.
    -   Dies ist optional, und Benutzer müssen [sich für entscheiden.](glossary.md)
-   Verwenden Sie die Schaltfläche Minimieren auf der Titelleiste der Anwendung, nicht die Schaltfläche Schließen.

## <a name="text"></a>Text

### <a name="infotips"></a>Infotips

-   Die Symbolinfoinfo sollte eines der folgenden Formate aufweisen (wobei der Unternehmensname optional ist):
    -   (Firmenname) Feature-, Programm- oder Gerätename
    -   ![Screenshot der Infotip mit Firmenname ](images/winenv-notification-image37.png)
    -   (Firmenname) Feature-, Programm- oder Gerätename: Statuszusammenfassung
    -   ![Screenshot der Infoinfo mit Statuszusammenfassung ](images/winenv-notification-image38.png)
    -   (Firmenname) Statusaufstellung für Feature, Programm oder Gerätename.
    -   ![Screenshot der Infotip zum Anzeigen der Status-Anweisung ](images/winenv-notification-image39.png)
    -   (Firmenname) Feature-, Programm- oder Gerätename
    -   Statusliste mit jedem Element in einer separaten Zeile
    -   ![Screenshot der Infotip zum Anzeigen der Statusliste ](images/winenv-notification-image40.png)

Infotip-Ausdrücke:

-   Konzentrieren Sie sich auf die nützlichsten Informationen. Zeigen Sie weitere Informationen im linken Einzelklick an.
-   Seien Sie präzise. Verwenden Sie Satzfragmente oder einfache Anweisungen.
-   Verwenden Sie keine endende Interpunktion, es sei denn, tip wird als vollständiger Satz formuliert.
-   Unnötige Wörter weglassen. Schließen Sie nicht die Softwareversion oder andere überflüssige Informationen ein.

    **Falsch:**

    ![Screenshot der Infotip mit unnötigen Informationen ](images/winenv-notification-image41.png)

    In diesem Beispiel enthält die Infoinfo überflüssige Informationen.

-   Erläutern Sie nicht, wie Sie mit dem Symbol interagieren.

    **Falsch:**

    ![Screenshot der Infotip mit Anweisungen zum Rechtsklick ](images/winenv-notification-image42.png)

    In diesem Beispiel enthält das Symbol Drahtlosnetzwerkverbindung Anweisungen zum Rechtsklick.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf den Benachrichtigungsbereich:

-   Verweisen Sie auf den Infobereich als Infobereich, nicht auf die Taskleiste.

Wenn Sie auf ein Symbol für den Benachrichtigungsbereich verweisen:

-   Verweisen Sie auf das Symbol, indem Sie den genauen Namen verwenden, der in der Infotip angegeben ist, einschließlich der Groß-/Großschreibung, gefolgt vom Symbol.
-   Die erste Referenz finden Sie auch im Infobereich.
-   Formatieren Sie den Überschriftentext nach Möglichkeit fett. Andernfalls setzen Sie die Überschrift nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

**Beispiel:** Um den Netzwerkstatus schnell zu überprüfen, klicken Sie im Infobereich auf das Symbol **Netzwerk.**

 


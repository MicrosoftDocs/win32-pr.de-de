---
title: Infobereich
description: Im Benachrichtigungsbereich werden Benachrichtigungen und Status bereitstellt. Gut entworfene Programme verwenden den Benachrichtigungsbereich entsprechend, ohne dass Sie lästig oder ablenkend sind.
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0293038dd155f12b96b22dd1c273a50f1c030ffa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961082"
---
# <a name="notification-area"></a>Infobereich

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Im Benachrichtigungsbereich werden Benachrichtigungen und Status bereitstellt. Gut entworfene Programme verwenden den Benachrichtigungsbereich entsprechend, ohne dass Sie lästig oder ablenkend sind.

Der Benachrichtigungsbereich ist ein Teil der Taskleiste, der eine temporäre Quelle für Benachrichtigungen und Status bereitstellt. Es kann auch verwendet werden, um Symbole für System-und Programm Features anzuzeigen, die auf dem Desktop nicht vorhanden sind.

Elemente im Benachrichtigungsbereich werden als Benachrichtigungs Bereichs Symbole oder einfach als Symbole bezeichnet, wenn der Kontext des Benachrichtigungs Bereichs bereits eindeutig festgelegt ist.

![Screenshot des Benachrichtigungs Bereichs, der Uhrzeit und des Datums ](images/winenv-notification-image1.png)

Der Benachrichtigungsbereich.

Um Benutzern die Kontrolle über den Desktop in Windows 7 zu verschaffen, werden standardmäßig nicht alle Symbole des Benachrichtigungs Bereichs angezeigt. Stattdessen werden Symbole im Benachrichtigungs Bereichs Überlauf angezeigt, es sei denn, Sie werden vom Benutzer in den Benachrichtigungsbereich herauf gestuft.

![Screenshot, der einen Benachrichtigungsbereich und einen Überlauf anzeigt.](images/winenv-notification-image2.png)

Der Überlauf des Benachrichtigungs Bereichs.

**Hinweis:** Richtlinien, die sich auf die [Taskleiste](winenv-taskbar.md), [Benachrichtigungen](mess-notif.md) und [Luftballons](ctrl-balloons.md) beziehen, werden in separaten Artikeln dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Muss Ihr Programm eine Benachrichtigung anzeigen?** Wenn dies der Fall ist, müssen Sie ein Benachrichtigungs Bereichs Symbol verwenden.
-   **Wird das Symbol temporär angezeigt, um eine Statusänderung anzuzeigen?** Wenn dies der Fall ist, kann ein Benachrichtigungs Bereichs Symbol geeignet sein, je nach den folgenden Faktoren:

    -   **Ist der Status hilfreich und relevant?** Das heißt, dass Benutzer das Symbol wahrscheinlich überwachen und ihr Verhalten aufgrund dieser Informationen ändern können? Wenn dies nicht der Fall ist, wird der Status entweder nicht angezeigt oder in eine Protokolldatei eingefügt.

        **Falsch:**

        ![Screenshot des Benachrichtigungs Bereichs mit Laufwerk (Symbol) ](images/winenv-notification-image3.png)

        In diesem Beispiel ist das Laufwerks Aktivitäts Symbol ungeeignet, da Benutzer ihr Verhalten wahrscheinlich nicht auf der Grundlage des Laufwerks ändern können.

    -   **Ist der Status kritisch? Ist eine sofortige Aktion erforderlich?** Wenn dies der Fall ist, zeigen Sie die Informationen so an, dass Sie beachtet werden und nicht einfach ignoriert werden können, z. b. ein [Dialogfeld](win-dialog-box.md).

    Für Windows 7 entwickelte Programme können über Lagerungs Symbole auf der Task leisten Schaltfläche des Programms verwendet werden, um Statusänderungen anzuzeigen, sowie Status leisten der Task leisten-Schaltfläche, um den Fortschritt von Aufgaben mit langer Ausführungsdauer anzuzeigen.

-   **Hat das Feature bereits "Desktop Präsenz"?** Das bedeutet, dass die Funktion bei der Laufzeit in einem Fenster auf dem Desktop angezeigt wird (möglicherweise minimiert)? Wenn dies der Fall ist, zeigen Sie den Status in der [Statusleiste](ctrl-status-bars.md)des Programms, in einem anderen Statusbereich oder für Windows 7 direkt auf der Task leisten Schaltfläche an. Wenn die Funktion keine Desktop Präsenz hat, können Sie ein Symbol für den Programm Zugriff verwenden und den Status anzeigen.
-   **Ist das Symbol primär das Starten eines Programms oder das schnelle zugreifen auf seine Features oder Einstellungen?** Wenn dies der Fall ist, verwenden Sie stattdessen das Startmenü, um Programme zu starten. Der Benachrichtigungsbereich ist nicht für schnelles Programm oder den Befehls Zugriff vorgesehen.

    ![Screenshot der Schnellstart-Symbolleiste ](images/winenv-notification-image4.png)

    In diesem Beispiel aus Windows Vista wird der Schnellstart verwendet, um Windows Explorer und Windows Internet Explorer schnell zu starten.

    Für für Windows 7 entwickelte Programme können Benutzer Task leisten Schaltflächen für den schnellen Programm Zugriff anheften. Programme können über eine Sprung Liste oder eine Miniaturansicht-Symbolleiste auf häufig verwendete Befehle direkt über die Symbolleisten Schaltfläche eines Programms zugreifen. Der Bereich Schnellstart wird in Windows 7 standardmäßig nicht angezeigt.

    ![Screenshot der Taskleiste und der Sprung Liste mit Symbolen ](images/winenv-notification-image5.png)

    In diesem Beispiel wird eine Sprung Liste für den schnellen Befehls Zugriff verwendet.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="the-windows-desktop"></a>Der Windows-Desktop

Der Windows-Desktop verfügt über die folgenden Programm Zugriffspunkte:

-   **Arbeitsbereich.** Der Bereich auf dem Bildschirm, in dem Benutzer ihre Arbeit ausführen und Programme, Dokumente und deren Verknüpfungen speichern können. Obwohl der Desktop technisch gesehen die Taskleiste enthält, bezieht er sich in den meisten Kontexten nur auf den Arbeitsbereich.
-   **Start Schaltfläche.** Der Zugriffspunkt für alle Programme und besonderen Windows-Speicherorte (Dokumente, Bilder, Musik, Spiele, Computer, Systemsteuerung) mit den Listen "zuletzt verwendet" für den schnellen Zugriff auf zuletzt verwendete Programme und Dokumente.
-   **Schnellstart:** Ein direkter Zugriffspunkt für Programme, die vom Benutzer ausgewählt wurden. Der Schnellstart wurde von Windows 7 entfernt.
-   **Taskleiste.** Der Zugriffspunkt für das Ausführen von Programmen, die über Desktop Präsenz verfügen. Technisch gesehen erstreckt sich die Taskleiste auf den gesamten Balken von der Start Schaltfläche bis zum Benachrichtigungsbereich. in den meisten Kontexten bezieht sich die Taskleiste auf den Bereich dazwischen, der die Schaltflächen der Taskleiste enthält. Dieser Bereich wird manchmal auch als TaskBand bezeichnet.
-   **Deskbands. Nicht empfohlen.**
-   **Benachrichtigungsbereich.** Eine kurzfristige Quelle für Benachrichtigungen und Status sowie einen Zugriffspunkt für System-und programmbezogene Features, die nicht auf dem Desktop vorhanden sind.

![Screenshot zur Identifizierung von Desktop Zugriffs Punkten ](images/winenv-notification-image6.png)

Zu den Windows-Desktop Zugriffs Punkten zählen die Start Schaltfläche, die Taskleiste und der Benachrichtigungsbereich. Beachten Sie die Miniaturansicht der Task leisten Schaltfläche.

**Der Desktop ist eine begrenzte, freigegebene Ressource, die der Einstiegspunkt des Benutzers auf Windows ist.** Belassen Sie die Benutzer in der Kontrolle. Sie sollten die Desktop Bereiche wie vorgesehen verwenden, damit andere Verwendungszwecke als Missbrauch angesehen werden. Zeigen Sie z. b. nie Desktop Bereiche als Möglichkeiten zum herauf Stufen Ihres Programms oder seiner [Marke](exper-branding.md)an.

### <a name="using-the-notification-area-appropriately"></a>Angemessene Verwendung des Benachrichtigungs Bereichs

Der Benachrichtigungsbereich war ursprünglich als temporäre Quelle für Benachrichtigungen und Status vorgesehen. Dank der Effizienz und der Umgebung wurden Entwickler dazu ermutigt, andere Zwecke zu unterstützen, z. b. Programme starten und Befehle ausführen. Leider haben diese Ergänzungen im Laufe der Zeit den Benachrichtigungsbereich zu groß und unabsichtlich und mit den anderen Desktop Zugriffs Punkten verwechselt.

Windows XP hat das Skalierungs Problem behoben, indem der Bereich reduziert und die nicht verwendeten Symbole ausgeblendet wurden. Windows Vista hat das Rauschen behoben, indem unnötige, lästige Benachrichtigungen entfernt wurden. Windows 7 hat einen Schritt weiter gehen, indem die Benachrichtigung auf den ursprünglichen Zweck einer Benachrichtigungs Quelle fokussiert wurde. **Die meisten Symbole werden standardmäßig in Windows 7 ausgeblendet, können jedoch vom Benutzer manuell in den Benachrichtigungsbereich herauf gestuft werden. Damit die Benutzer die Kontrolle über Ihre Desktops behalten können, gibt es keine Möglichkeit für Ihr Programm, diese herauf Stufung automatisch auszuführen.** In Windows werden weiterhin Benachrichtigungen für verborgene Symbole angezeigt, indem Sie vorübergehend herauf gestuft werden.

![Screenshot von Benachrichtigungsbereich und Überlauf ](images/winenv-notification-image7.png)

In Windows 7 sind die meisten Benachrichtigungs Bereichs Symbole standardmäßig ausgeblendet.

Darüber hinaus unterstützt Windows 7 viele Features direkt in den Schaltflächen der Taskleiste. Insbesondere können Sie Folgendes verwenden:

-   Sprung Listen und Miniatur Ansichts Symbolleisten für den schnellen Zugriff auf häufig verwendete Befehle.
-   Überlagerungs Symbole zum Anzeigen des Status für das Ausführen von Programmen.
-   Status leisten der Taskleiste, um den Fortschritt für Aufgaben mit langer Ausführungsdauer anzuzeigen.

Wenn Ihr Programm über Desktop Präsenz verfügt, können Sie die Features für die Windows 7-Taskleiste für diese Zwecke vollständig nutzen. **Behalten Sie die Benachrichtigungs Bereichs Symbole beim Anzeigen von Benachrichtigungen und Status bei.**

### <a name="keeping-users-in-control"></a>Behalten der Kontrolle durch Benutzer

Die Beibehaltung von Benutzern in der Kontrolle überschreitet den ordnungsgemäßen Einsatz des Benachrichtigungs Bereichs. Abhängig von der Art des Symbols sollten Sie Benutzern die folgenden Aktionen gestatten:

-   **Entfernen Sie das Symbol.** Ihr Symbol bietet möglicherweise einen relevanten, nützlichen Status, aber auch dies ist möglicherweise nicht möglich. Windows ermöglicht Benutzern das Ausblenden von Symbolen, aber dieses Feature ist nicht leicht erkennbar. Um Benutzern die Kontrolle zu behalten, geben Sie im Kontextmenü des Symbols ein **Anzeige Symbol in der Option Benachrichtigungsbereich** ein. Beachten Sie, dass sich das Entfernen eines Symbols nicht auf das zugrunde liegende Programm, Feature oder den zugrunde liegenden Prozess auswirken muss.
-   **Wählen Sie die anzuzeigenden Benachrichtigungs Typen aus.** Ihre Benachrichtigung muss hilfreich und relevant sein, aber es gibt möglicherweise Benachrichtigungen, die Benutzern nicht angezeigt werden sollen. Dies gilt insbesondere für- [Benachrichtigungen](mess-notif.md). Erlauben Sie Benutzern, die weniger wichtigen Optionen zu aktivieren.
-   **Unterbrechen Sie optionale Features.** Symbole werden verwendet, um den Status von Features ohne Desktop Präsenz anzuzeigen. Diese Features sind tendenziell mit langer Ausführungszeit, optionalen Hintergrundaufgaben wie z. b. Drucken, indizieren, Scannen oder synchronisieren. Benutzer möchten diese Features möglicherweise aussetzen, um die Systemleistung zu erhöhen, den Energieverbrauch zu reduzieren oder weil Sie offline sind.
-   **Beenden Sie das Programm.** Geben Sie die geeigneteren Optionen an:
    -   **Programm vorübergehend beenden.** Das Programm wird beendet und neu gestartet, wenn Windows neu gestartet wird. Diese Vorgehensweise eignet sich für wichtige System Dienstprogramme, wie z. b. Sicherheitsprogramme.
    -   **Programm dauerhaft beenden.** Das Programm wird beendet und nicht neu gestartet, wenn Windows neu gestartet wird (es sei denn, der Benutzer wählt den Neustart später aus). Der Benutzer möchte das Programm nicht mehr ausführen oder das Programm Bedarfs gesteuert ausführen, um die Systemleistung zu verbessern.

Obwohl es eine gute Idee ist, die meisten dieser Einstellungen im Kontextmenü des Symbols anzugeben, sollte die Standardumgebung des Programms für die meisten Benutzer geeignet sein. Aktivieren Sie alles nicht standardmäßig, und erwarten Sie, dass die Benutzer Funktionen deaktivieren. Aktivieren Sie stattdessen die wichtigen Features standardmäßig, und ermöglichen Sie es Benutzern, zusätzliche Features wie gewünscht zu aktivieren.

**Wenn Sie nur vier Dinge tun...**

1.  Missbrauchen Sie den Benachrichtigungsbereich nicht. Verwenden Sie es nur als Quelle für Benachrichtigungen und Status und für Features ohne Desktop Präsenz.
2.  Behalten Sie die Kontrolle über die Benutzer. Stellen Sie geeignete Optionen bereit, um das Symbol, seine Benachrichtigungen und die zugrunde liegenden Features zu steuern.
3.  Stellen Sie eine Standardeinstellung für die meisten Benutzer dar. Ermöglichen Sie Benutzern das Aktivieren gewünschter Features, anstatt zu erwarten, dass Sie nicht gewünschte Funktionen deaktivieren.
4.  Nutzen Sie die Funktionen der Windows 7-Task leisten Schaltfläche, um den Status anzuzeigen und die am häufigsten ausgeführten Aufgaben Ihres Programms zu optimieren.

## <a name="usage-patterns"></a>Verwendungsmuster

Benachrichtigungs Bereichs Symbole haben mehrere Verwendungs Muster:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>System Status und-Zugriff</strong><br/> Wird fortlaufend angezeigt, um einen wichtigen, aber nicht kritischen Systemstatus anzuzeigen und den Zugriff auf relevante Features und Einstellungen zu ermöglichen. <br/></td>
<td>System Funktionen, die Benachrichtigungs Bereichs Symbole benötigen, haben keine permanente Desktop Präsenz. Kann auch als Benachrichtigungs Quelle verwendet werden. <br/> <img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br/> In diesem Beispiel werden die Symbole "Akku", "Netzwerk" und "Volume" kontinuierlich angezeigt, falls zutreffend.<br/></td>
</tr>
<tr class="even">
<td><strong>Hintergrundaufgaben Status und-Zugriff</strong><br/> Wird angezeigt, während ein Hintergrund Task ausgeführt wird, um den Status anzuzeigen und Zugriff auf Funktionen und Einstellungen bereitzustellen. <br/></td>
<td>Hintergrundprozesse benötigen Benachrichtigungs Bereichs Symbole, wenn keine Desktop Präsenz vorhanden ist. Kann auch als Benachrichtigungs Quelle verwendet werden. <br/> <img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br/> In diesem Beispiel ermöglicht das Symbol "Aktions Center" Benutzern, ihren Status zu überprüfen, auch wenn keine Desktop Präsenz vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>Temporärer Ereignis Status</strong><br/> Programme mit Desktop Präsenz können Symbole temporär anzeigen, um wichtige Ereignisse oder Statusänderungen anzuzeigen. <br/></td>
<td><img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br/> In diesem Beispiel werden Symbole zum Drucken und Installieren von Updates temporär angezeigt, um wichtige Ereignisse oder Statusänderungen anzuzeigen.<br/></td>
</tr>
<tr class="even">
<td><strong>Temporäre Benachrichtigungs Quelle</strong><br/> Wird vorübergehend angezeigt, um eine Benachrichtigung anzuzeigen. Nach einem Timeout entfernt oder wenn das zugrunde liegende Problem behoben oder die Aufgabe ausgeführt wurde. <br/></td>
<td>Temporäre Symbole werden für reine Benachrichtigungs Quellen bevorzugt. Zeigen Sie kein Symbol an, das keinen nützlichen, relevanten und dynamischen Status bereitstellt, nur weil eine Funktion möglicherweise in der Zukunft eine Benachrichtigung anzeigen muss. <br/> <img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br/> In diesem Beispiel wird das Plug-and-Play-Symbol angezeigt, während eine neue Hardware erkannte Benachrichtigung angezeigt wird.<br/></td>
</tr>
<tr class="odd">
<td><strong>Minimierte Einzelinstanzanwendung</strong><br/> Um die Task leisten Übersichtlichkeit zu reduzieren, kann eine Anwendung mit langer Ausführungszeit auf ein Benachrichtigungs Bereichs Symbol minimiert werden. <br/></td>
<td><img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br/> In diesem Beispiel aus Windows Vista sind Outlook und Windows Live Messenger Einzelinstanzanwendungen, die die Symbole für Benachrichtigungs Bereiche minimieren.<br/> Verwenden Sie dieses Muster nur dann, wenn Folgendes zutrifft: <br/>
<ul>
<li>Die Anwendung kann nur über eine einzelne Instanz verfügen.</li>
<li>Die Anwendung wird für einen längeren Zeitraum ausgeführt.</li>
<li>Das Symbol zeigt den Status an.</li>
<li>Das Symbol kann eine Benachrichtigungs Quelle sein.</li>
<li>Dies ist optional, und die Benutzer müssen sich <a href="glossary.md">Anmelden</a>.</li>
</ul>
Wenn alle diese Bedingungen zutreffen, entfällt das Minimieren eines Symbols auf zwei Zugriffspunkte, wenn nur eine erforderlich ist. <br/> <strong>Hinweis:</strong> Dieses Symbol Muster wird für Windows 7 nicht mehr empfohlen. Verwenden Sie stattdessen reguläre Task leisten Schaltflächen, wenn Ihr Programm über eine Desktop Präsenz verfügt.<br/> <img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br/> In diesem Beispiel aus Windows 7 benötigt eine reguläre Task leisten Schaltfläche nur wenig Platz, bietet aber Vorteile von den Funktionen der Windows 7-Task leisten-Schaltfläche, einschließlich Sprung Listen, Überlagerungs Symbolen und umfangreichen Miniaturansichten.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Geben Sie nur ein Benachrichtigungs Bereichs Symbol pro Komponente an.**
-   **Verwenden Sie ein Symbol mit 16x16, 20 x 20 und 24 x 24 Pixel Versionen.** Die größeren Versionen werden im Modus mit hoher dpi-Anzeige verwendet.

### <a name="when-to-show"></a>Anzeige

-   Für das temporäre Benachrichtigungs Quell Muster:
    -   Windows zeigt das Symbol an, wenn die Benachrichtigung angezeigt wird.
    -   Entfernen Sie das Symbol auf der Grundlage des [Benachrichtigungs Entwurfs](mess-notif.md) Musters:



    | Muster                                     | Zeitpunkt der Entfernung                                         |
    |--------------------------------------|------------------------------------------|
    | Aktion erfolgreich<br/>            | Wenn die Benachrichtigung entfernt wird.<br/> |
    | Aktions Fehler<br/>            | Wenn das Problem behoben ist.<br/>     |
    | Nicht kritisches System Ereignis<br/> | Wenn das Problem behoben ist.<br/>     |
    | Optionale Benutzer Aufgabe<br/>        | Wenn die Aufgabe abgeschlossen ist.<br/>            |
    | Zur Kenntnisnahme<br/>                       | Wenn die Benachrichtigung entfernt wird.<br/> |



 

-   **Zeigen Sie für das Muster temporäres Ereignis Status das Symbol an, während das Ereignis auftritt.**
-   Zeigen Sie bei allen anderen Mustern **das Symbol an, wenn das Programm, die Funktion oder der Prozess ausgeführt wird und das Symbol relevant ist** , es sei denn, der Benutzer hat das **Anzeige Symbol in der Option Benachrichtigungsbereich** gelöscht (Weitere Informationen finden Sie unter [Kontextmenüs](#context-menus)). Die meisten Symbole werden standardmäßig in Windows 7 ausgeblendet, können aber vom Benutzer in den Benachrichtigungsbereich herauf gestuft werden.
-   **Zeigen Sie keine Symbole an, die für Administratoren für Standardbenutzer gedacht sind.** Notieren Sie die Informationen im Windows-Ereignisprotokoll.

### <a name="where-to-show"></a>Anzeige

-   **Zeigt Fenster an, die über das Benachrichtigungs Bereichs Symbol in der Nähe des Benachrichtigungs Bereichs**

![Abbildung eines Fensters in der Nähe des Benachrichtigungs Bereichs ](images/winenv-notification-image14.png)

Fenster, die über das Symbol für den Benachrichtigungsbereich gestartet werden, werden im Infobereich angezeigt

### <a name="icons"></a>Symbole

-   **Wählen Sie das Symbol basierend auf dem Entwurfsmuster aus:**

    | Muster                                                 | Symboltyp                                   |
    |--------------------------------------------------|------------------------------------|
    | System Status und-Zugriff<br/>              | Symbol "System Funktion"<br/>     |
    | Hintergrundaufgaben Status und-Zugriff<br/>     | Symbol "Programm oder Feature"<br/> |
    | Temporäre Benachrichtigungs Quelle<br/>         | Symbol "Programm oder Feature"<br/> |
    | Temporärer Ereignis Status<br/>                | Symbol "Programm oder Feature"<br/> |
    | Minimierte Einzelinstanzanwendung<br/> | Programmsymbol<br/>            |

    

     

    ![Screenshot des Benachrichtigungs Bereichs und der Outlook-Symbole ](images/winenv-notification-image15.png)

    In diesem Beispiel verwendet Outlook ein e-Mail-Funktions Symbol für eine temporäre Benachrichtigungs Quelle und das zugehörige Anwendungssymbol für die minimierte Anwendung.

-   **Wählen Sie ein leicht erkennbares Symbol Design aus.** Symbole mit eindeutigen Gliederungen über quadratische oder rechteckige förmige Symbole bevorzugen. Sorgen Sie dafür, dass die Entwürfe die Symbole für realistische Bilder bevorzugen. Wenden Sie auch die anderen [Aero-Stil-Richtlinien](vis-icons.md) an.
-   **Verwenden Sie Symbol Variationen oder Überlagerungen, um Status-oder Statusänderungen anzugeben.** Verwenden Sie Symbol Variationen, um Änderungen in Mengen oder stärken anzuzeigen. Verwenden Sie für andere Arten von Status die folgenden Standard Überlagerungen. Verwenden Sie nur eine einzelne Überlagerung, und suchen Sie Sie unten rechts auf Konsistenz. 

    | Überlagerung                                                                                                       | Status                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![Screenshot des kleinen Warn Symbols ](images/winenv-notification-image16.png)<br/>               | Warnung<br/>               |
    | ![Screenshot des kleinen Fehler Symbols ](images/winenv-notification-image17.png)<br/>                 | Fehler<br/>                 |
    | ![Screenshot des kleinen deaktivierten/getrennten Symbols ](images/winenv-notification-image18.png)<br/> | Deaktiviert/getrennt<br/> |
    | ![Screenshot eines kleinen blockierten/Offline-Symbols ](images/winenv-notification-image19.png)<br/>       | Blockiert/offline<br/>       |

    

     

    ![Screenshot des Benachrichtigungs Bereichs und der beiden Symbole ](images/winenv-notification-image20.png)

    In diesem Beispiel zeigen die drahtlos-und Akku Symbole Änderungen in Mengen oder stärken an.

    ![Screenshot des Benachrichtigungs Bereichs und der zwei Überlagerungen ](images/winenv-notification-image21.png)

    In diesem Beispiel werden Überlagerungen zum Anzeigen von Fehler-und Warn Zuständen verwendet.

-   **Vermeiden Sie, dass in ihren Basis Symbolen in den Basis Symbolen in den Basis Symbolen in den Basis Symbolen in der Farbe** Um Verwirrung zu vermeiden, reservieren Sie diese Farben, um den Status zu kommunizieren. Wenn Ihr [Branding](exper-branding.md) diese Farben verwendet, sollten Sie die Verwendung von gedämpften Tönen für Ihre Basis-Benachrichtigungs Bereichs Symbole in Erwägung
-   Verwenden Sie für die [Progressive Eskalation](mess-notif.md) **Symbole mit einer progressiveren Darstellung, da die Situation dringender wird.**

    ![Screenshot von Benachrichtigungsbereich und fünf Symbolen ](images/winenv-notification-image22.png)

    In diesen Beispielen wird die Darstellung des Akku Symbols deutlicher, wenn sich die Dringlichkeit vergrößert.

-   **Ändern Sie den Status nicht zu häufig.** Die Symbole des Benachrichtigungs Bereichs sollten nicht in der Nähe, instabil oder nach Bedarf angezeigt werden. Das Auge ist von den Änderungen im Peripherie Feld der Vision abhängig, sodass Statusänderungen gering sein müssen.
    -   **Ändern Sie das Symbol nicht schnell.** Wenn sich der zugrunde liegende Status schnell ändert, lassen Sie das Symbol den Status auf hoher Ebene widerspiegeln.

        **Falsch:**

        ![Screenshot des Benachrichtigungs Bereichs und Modem Symbols ](images/winenv-notification-image23.png)

        In diesem Beispiel zeigt das Modem Symbol blinkende Beleuchtung an (wie ein Hardware Modem), aber diese Zustandsänderungen sind für die Benutzer nicht signifikant.

    -   **Verwenden Sie keine Animationen mit langer Ausführungszeit, um fortlaufende Aktivitäten anzuzeigen.** Solche Animationen sind eine Ablenkungs Weise. Das vorhanden sein eines Symbols im Benachrichtigungsbereich deutet auf eine fortlaufende Aktivität hin.
    -   **Kurze, feine Animationen sind akzeptabel, um den Fortschritt während der wichtigen temporären, transitiven Statusänderungen anzuzeigen.**

        ![Screenshot des Benachrichtigungs Bereichs und des drahtlos Symbols ](images/winenv-notification-image24.png)

        In diesem Beispiel zeigt das drahtlos Symbol einen Aktivitätsindikator an, um anzuzeigen, dass die Arbeit ausgeführt wird.

    -   **Blinken Sie das Symbol nicht.** Dies ist zu stark ablenkend. Wenn ein Ereignis sofortige Aufmerksamkeit erfordert, verwenden Sie stattdessen ein Dialogfeld. Wenn das Ereignis anderweitig Eingreifen erfordert, verwenden Sie eine Benachrichtigung.

-   **Deaktivieren Sie keine Symbole für den Benachrichtigungsbereich.** Wenn das Symbol zurzeit nicht angewendet wird, entfernen Sie es. Sie können jedoch ein aktiviertes Symbol mit einem deaktivierten Status Überlagerung anzeigen, wenn Benutzer über das Symbol aktivieren können.

    ![Screenshot des Benachrichtigungs Bereichs und des Schiebereglers ](images/winenv-notification-image25.png)

    In diesem Beispiel können Benutzer die Soundausgabe über das Symbol aktivieren.

Allgemeine Symbol Richtlinien und Beispiele finden Sie unter [Symbole](vis-icons.md).

### <a name="interaction"></a>Interaktion

**Hinweis:** Die folgenden Click-Ereignisse sollten bei der Maus nach oben auftreten, nicht bei der Maustaste.

**Darauf zeigen (Hover)**

-   **Anzeigen einer QuickInfo oder eines Infotipps, der angibt, was das Symbol darstellt.**

    ![Screenshot des Benachrichtigungs Bereichs und der QuickInfo ](images/winenv-notification-image26.png)

    In diesem Beispiel wird eine QuickInfo verwendet, um das Symbol bei Hover zu beschreiben.

Informationen zu Infotipp-Text Richtlinien finden Sie im [Text](#context-menus) Abschnitt dieses Artikels.

**Links mit nur einem Mausklick**

-   **Zeigen Sie alle Benutzer an, die am wahrscheinlichsten** angezeigt werden sollen. Dies kann folgende sein:

    -   Ein Flyout-Fenster, Dialogfeld oder Programmfenster mit den nützlichsten Einstellungen und häufig ausgeführten Aufgaben. Präsentations Richtlinien finden Sie unter [Benachrichtigungs Bereichs Flyouts](#notification-area-flyouts).

        ![Screenshot des Benachrichtigungs Bereichs und der Flyouts ](images/winenv-notification-image27.png)

        In diesen Beispielen zeigt das Klicken mit der linken Maustaste Popup Fenster mit den nützlichsten Einstellungen an.

    -   Ein Status-Flyout.

        ![Screenshot des Benachrichtigungs Bereichs und des Status Flyout ](images/winenv-notification-image28.png)

        In diesem Beispiel wird mit der linken Maustaste das Status-Flyout angezeigt.

        -   Das zugehörige System Steuerungselement.
        -   Das Kontextmenü.

    Benutzer erwarten, dass ein Klick mit der linken Maustaste angezeigt wird. Wenn Sie also nichts anzeigen, wird ein Benachrichtigungs Bereichs Symbol nicht mehr angezeigt.

-   **Zeigen Sie ein Kontextmenü nur an, wenn die anderen Optionen nicht zutreffen** und der Standardbefehl fett formatiert ist. Zeigen Sie in diesem Fall das Kontextmenü an, das beim Klicken mit der rechten Maustaste angezeigt wird, um Verwechslungen zu vermeiden.
-   **Bevorzugen Sie ein Popup Fenster für ein Dialogfeld** , um ein einfacheres Gefühl zu haben. Zeigen Sie nur die gängigsten Einstellungen an, und lassen Sie Sie sich sofort auf eine einfachere Interaktion auswirken. Schließen Sie das Popup Fenster, wenn der Benutzer auf eine beliebige Stelle außerhalb des Fensters klickt.
-   **Zeigt kleine Fenster in der Nähe des zugeordneten Symbols an.** Große Fenster (z. b. System Steuerungselemente) können jedoch in der Mitte des Standard Monitors angezeigt werden.

**Doppelklick mit der linken Maustaste**

-   **Führen Sie den Standardbefehl im Kontextmenü aus.** Dadurch wird in der Regel die primäre Benutzeroberfläche angezeigt, die dem Symbol zugeordnet ist, z. b. das zugeordnete System Steuerungselement, das Eigenschaften Blatt oder das Programmfenster.
-   **Wenn kein Standardbefehl vorhanden ist, führen Sie dieselbe Aktion aus wie bei einem linken Mausklick.**

**Klicken Sie mit der rechten Maustaste auf**

-   **Zeigen Sie das Kontextmenü** an, wobei der Standardbefehl fett formatiert ist.

### <a name="context-menus"></a>Kontextmenüs

-   **Zeigen Sie das Kontextmenü neben dem zugehörigen Symbol** an, aber nicht in der Taskleiste.
-   **Das Kontextmenü kann ggf. die folgenden Elemente** in der aufgelisteten Reihenfolge enthalten (genauer Text in Anführungszeichen):

Primäre Befehle

Öffnen (Standard, Liste zuerst, Fett)

Ausführen

Sekundäre Befehle

< Trennzeichen>

Befehl zum Aktivieren/Deaktivieren von Suspend/Resume (Häkchen)

"In Benachrichtigungsbereich minimiert" (Häkchen)

Benachrichtigungen aktivieren (Häkchen)

"Anzeige Symbol im Benachrichtigungsbereich" (Häkchen)

< Trennzeichen>

Handlungs

Abstiegs

-   **Entfernen Sie keine Kontextmenü Elemente, die nicht angewendet werden, anstatt diese zu deaktivieren.**
-   Geben Sie für die Befehle öffnen, ausführen und aussetzen/fortsetzen **an, was geöffnet, ausgeführt,** angehalten und fortgesetzt wird.

![Screenshot, der einen Benachrichtigungsbereich und Befehle anzeigt.](images/winenv-notification-image29.png)

In diesem Beispiel verfügt Windows Defender über bestimmte Befehle zum Öffnen und ausführen.

-   **Verwenden Sie unterbrechen/fortsetzen ausführen Hintergrundaufgaben, aktivieren/deaktivieren für alles andere.**
-   **Verwenden Sie Häkchen, um den Status anzugeben.** Auflisten und aktivieren Sie alle Zustände, und platzieren Sie das Häkchen neben dem aktuellen Zustand. Deaktivieren Sie Optionen nicht, oder ändern Sie Options Bezeichnungen, um den aktuellen Zustand anzugeben.

**Richtig:**

![Screenshot eines Befehls mit einem Häkchen ](images/winenv-notification-image29.png)

**Falsch:**

![Screenshot eines Befehls ohne Häkchen ](images/winenv-notification-image30.png)

Im falschen Beispiel sollte in Windows Defender ein Häkchen verwendet werden, um den aktuellen Zustand anzugeben.

-   **Alle Hintergrundaufgaben müssen über einen Suspend/Resume-Befehl verfügen.** Wenn Sie den Befehl auswählen, sollte der Task vorübergehend angehalten werden. Möglicherweise möchten Sie Hintergrundaufgaben vorübergehend aussetzen, um die Systemleistung zu erhöhen oder den Energieverbrauch zu verringern. Angehaltene Hintergrundaufgaben werden neu gestartet, wenn Sie vom Benutzer wieder aufgenommen werden oder wenn Windows neu gestartet wird.
-   **Ermöglicht Benutzern das abonnieren oder Abmelden verschiedener Benachrichtigungs Typen** , wenn Ihr Programm Benachrichtigungen enthält, die möglicherweise nicht von einigen Benutzern angezeigt werden. Das [FYI](mess-notif.md) -Benachrichtigungs Muster erfordert, dass Benutzer sich entscheiden, sodass diese Benachrichtigungen standardmäßig deaktiviert werden müssen.

![Screenshot des Benachrichtigungs Bereichs und der Befehle ](images/winenv-notification-image31.png)

In diesem Beispiel können Benutzer mithilfe von Outlook die Benachrichtigungen auswählen, die Sie über das Symbol erhalten.

-   **Wenn Sie die Option "Anzeige Symbol in Benachrichtigungsbereich" löschen, wird das Symbol aus dem Benachrichtigungsbereich entfernt**, aber das zugrunde liegende Programm, Feature oder Prozess wird nicht beeinträchtigt. Benutzer können das Symbol im Dialogfeld Optionen des Programms erneut anzeigen. Das Symbol wird nicht automatisch erneut angezeigt, wenn Windows neu gestartet wird.
-   **Mit dem Exit-Befehl wird das Programm für die aktuelle Windows-Sitzung beendet, und das Symbol wird entfernt.** Es ist kein Exit-Befehl vorhanden, wenn das Programm nicht heruntergefahren werden kann. Das Programm wird neu gestartet, wenn Windows neu gestartet wird. Benutzer können das Programm im Dialogfeld Optionen dauerhaft beenden.
-   **Es ist kein about-Befehl vorhanden.** Diese Informationen sollten über das Symbol, den Infotipp und das Kontextmenü kommuniziert werden. Wenn Benutzer weitere Informationen wünschen, können Sie die primäre Benutzeroberfläche anzeigen.
    -   **Ausnahme:** Sie können einen Info-Befehl bereitstellen, wenn das Symbol für ein Programm ist, das keine Desktop Präsenz hat.

Allgemeine Richtlinien und Beispiele für das Kontextmenü finden Sie unter [Menüs](cmd-menus.md).

### <a name="rich-tooltips"></a>Umfangreiche QuickInfos

-   **Verwenden Sie Rich Quick Tips nur, um die Informationen verständlicher zu machen.** Verwenden Sie keine Rich Quick Tips, um das Feature zu ergänzen. Wenn Sie keine Fülle verwenden können, um die Informationen verständlicher zu machen, verwenden Sie stattdessen eine einfache QuickInfo.

    **Falsch:**

    ![Screenshot des Benachrichtigungs Bereichs und der umfangreichen QuickInfo ](images/winenv-notification-image32.png)

    **Richtig:**

    ![Screenshot des Benachrichtigungs Bereichs und der einfachen QuickInfo ](images/winenv-notification-image33.png)

    Im falschen Beispiel wird das Datum nicht durch das Kalendersymbol leichter verständlich.

-   **Verwenden Sie eine präzise Präsentation.** Verwenden Sie präzisen Text und ein präzisere Layout mit einem 32 x 32 Pixel-Symbol. Geräumige Quick Infos-Risiken sind ablenkend, insbesondere, wenn Sie unbeabsichtigt angezeigt werden.
-   **Fügen Sie Steuerelemente oder Elemente, die in einer umfassenden QuickInfo interaktiv erscheinen, nicht ein.** Quick Infos sind nicht interaktiv und sollten daher nicht interaktiv erscheinen. Verwenden Sie keinen blauen oder unterstrichenen Text.

    **Richtig:**

    ![Screenshot der Rich-QuickInfo mit schwarzem Text ](images/winenv-notification-image34.png)

    **Falsch:**

    ![Screenshot der Rich-QuickInfo mit blauem Text ](images/winenv-notification-image35.png)

    Im falschen Beispiel scheint der aktuelle Energie Sparplan ein Link zu sein, aber es ist nicht möglich, darauf zu klicken.

### <a name="notification-area-flyouts"></a>Benachrichtigungs Bereichs Flyouts

-   Stellen Sie ggf. Benachrichtigungs Bereichs-Flyouts mit drei Abschnitten dar:
    -   **Zusammenfassung.** Anzeigen der gleichen Informationen, die in der QuickInfo oder im infotip des Symbols angezeigt werden, möglicherweise mit ausführlicheren Details. Verwenden Sie aus Gründen der Konsistenz denselben Text und dieselben Symbole und im Allgemeinen das gleiche Layout (wenn Sie eine umfangreiche QuickInfo verwenden). Anders als bei den infotips sind diese Informationen bei der Verwendung von Touchscreen zugänglich.
    -   **Häufige Aufgaben.** Präsentieren Sie die am häufigsten ausgeführten Aufgaben direkt im Flyout.
    -   **Verwandte Links.** Geben Sie höchstens einen der folgenden optionalen Verknüpfungen an:
        -   Ein Link zur am häufigsten ausgeführten Aufgabe in der Systemsteuerung. Geben Sie an, ob eine häufig ausgeführte Aufgabe vorhanden ist, die im Abschnitt Allgemeine Aufgaben nicht angezeigt werden kann.
        -   Ein Link zum zugehörigen System Steuerungselement. Mit diesem System Steuerungselement können Benutzer alle Aufgaben ausführen, die im Abschnitt Allgemeine Aufgaben nicht ausgeführt werden können.
        -   Ein Link zu einem bestimmten, relevanten Hilfethema. Befolgen Sie die Standard [Leitlinien für Hilfe Links](winenv-help.md).

![Screenshot des Benachrichtigungs Bereichs und Flyout ](images/winenv-notification-image36.png)

Dieses Beispiel zeigt ein Flyout für Benachrichtigungs Bereiche, das die empfohlene Präsentation verwendet.

### <a name="options-dialog-box"></a>Optionen (Dialogfeld)

-   Optionen, die nicht direkt über das Kontextmenü zugänglich sind, müssen im Dialogfeld Optionen angezeigt werden. Dieses Dialogfeld kann die Systemsteuerung des Features sein.
-   Im **Dialogfeld Optionen können nach Bedarf die folgenden Elemente enthalten** sein (genauer Text in Anführungszeichen):
    -   \[Funktionsnamen aktivieren \] (Kontrollkästchen)
        -   Durch das Löschen dieser Option wird das Programm endgültig beendet. Das Programm kann über das System Steuerungselement neu gestartet werden. Mit dem Exit-Befehl im Kontextmenü wird das Programm nur für die aktuelle Windows-Sitzung beendet.
    -   "Anzeige Symbol im Benachrichtigungsbereich" (Kontrollkästchen)
        -   Das Entfernen des Symbols aus dem Benachrichtigungsbereich wirkt sich nicht auf das zugrunde liegende Feature aus.
        -   Wenn Sie diese Option auswählen, kann der Benutzer das Symbol wiederherstellen, was natürlich nicht über das Symbol selbst erfolgen kann.
-   Deaktivieren Sie Features, die selten verwendet werden oder potenziell lästig oder ablenkend sind. Ermöglichen Sie [Benutzern die](glossary.md) Aktivierung dieser Features.

Richtlinien und Beispiele für allgemeine Optionen finden Sie unter [Eigenschaften Fenster](win-property-win.md).

### <a name="minimizing-programs-to-the-notification-area"></a>Minimieren von Programmen in den Benachrichtigungsbereich

**Hinweis: das Minimieren von Programmfenstern in den Benachrichtigungsbereich wird für Windows 7 nicht mehr empfohlen.** Verwenden Sie stattdessen reguläre [Task](winenv-taskbar.md) leisten Schaltflächen. Das Programm unterstützt möglicherweise beide Mechanismen für die Abwärtskompatibilität.

-   Um die Task leisten Übersichtlichkeit zu verringern, sollten Sie die Möglichkeit zur Minimierung von Programmen auf den Benachrichtigungsbereich bereitstellen, wenn Folgendes zutrifft:
    -   Das Programm kann nur über eine einzelne Instanz verfügen.
    -   Das Programm wird für einen längeren Zeitraum ausgeführt.
    -   Das Symbol zeigt den Status an.
    -   Das Symbol kann eine Benachrichtigungs Quelle sein.
    -   Dies ist optional, und die Benutzer müssen sich [Anmelden](glossary.md).
-   Verwenden Sie die Schaltfläche Minimieren auf der Titelleiste der Anwendung und nicht auf der Schaltfläche Schließen.

## <a name="text"></a>Text

### <a name="infotips"></a>Infotipps

-   Das Infotipp-Symbol sollte eines der folgenden Formate aufweisen (wobei der Name des Unternehmens optional ist):
    -   (Firmenname) Funktions-, Programm-oder Gerätename
    -   ![Screenshot des InfoTipps mit dem Firmennamen ](images/winenv-notification-image37.png)
    -   (Firmenname) Funktions-, Programm-oder Gerätename: Status Zusammenfassung
    -   ![Screenshot der Infotipp mit Status Zusammenfassung ](images/winenv-notification-image38.png)
    -   (Firmenname) Die Status Anweisung für das Feature, das Programm oder den Gerätenamen.
    -   ![Screenshot der Infotipp-Anzeige der Status Anweisung ](images/winenv-notification-image39.png)
    -   (Firmenname) Funktions-, Programm-oder Gerätename
    -   Status Liste mit jedem Element in einer separaten Zeile
    -   ![Screenshot der Infotipp-Anzeige der Status Liste ](images/winenv-notification-image40.png)

Infotip-Ausdruck:

-   Konzentrieren Sie sich auf die nützlichsten Informationen. Zeigen Sie weitere Informationen an, indem Sie mit der linken Maustaste klicken.
-   Seien Sie präzise. Verwenden Sie Satzfragmente oder einfache Anweisungen.
-   Verwenden Sie keine endinterpunktions Zeichen, es sei denn, Tip wird als vollständiger Satz formuliert.
-   Lassen Sie unnötige Wörter aus. Schließen Sie die Softwareversion oder andere überflüssige Informationen nicht ein.

    **Falsch:**

    ![Screenshot von Infotipp mit unnötigen Informationen ](images/winenv-notification-image41.png)

    In diesem Beispiel enthält der Infotipp überflüssige Informationen.

-   Erläutern Sie nicht, wie Sie mit dem Symbol interagieren.

    **Falsch:**

    ![Screenshot von Infotipp mit Rechtsklick Anweisungen ](images/winenv-notification-image42.png)

    In diesem Beispiel enthält das Symbol für drahtlos Netzwerkverbindungen mit der rechten Maustaste auf Anweisungen.

## <a name="documentation"></a>Dokumentation

Wenn Sie auf den Benachrichtigungsbereich verweisen:

-   Informationen zum Benachrichtigungsbereich finden Sie im Benachrichtigungsbereich und nicht in der Taskleiste.

Wenn Sie auf ein Benachrichtigungs Bereichs Symbol verweisen:

-   Verweisen Sie auf das Symbol, und verwenden Sie dabei den exakten Namen in seinem infotip, einschließlich der Groß-/Kleinschreibung, gefolgt von Symbol.
-   Informationen zum ersten Verweis finden Sie auch im Benachrichtigungsbereich.
-   Formatieren Sie nach Möglichkeit den Text der Überschrift mit "Bold". Andernfalls sollten Sie die Überschrift nur bei Bedarf in Anführungszeichen setzen, um Verwechslungen zu vermeiden.

**Beispiel:** Klicken Sie im Benachrichtigungsbereich auf das Symbol **Netzwerk** , um den Netzwerkstatus schnell zu überprüfen.

 


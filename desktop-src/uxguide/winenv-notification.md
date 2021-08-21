---
title: Infobereich
description: Der Benachrichtigungsbereich enthält Benachrichtigungen und Status. Gut entworfene Programme verwenden den Benachrichtigungsbereich entsprechend, ohne störend oder störend zu sein.
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 21eeabfff67028df5485c63dd18a6362edda445f2282a0d739c45f6efec19c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119029321"
---
# <a name="notification-area"></a>Infobereich

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Der Benachrichtigungsbereich enthält Benachrichtigungen und Status. Gut entworfene Programme verwenden den Benachrichtigungsbereich entsprechend, ohne störend oder störend zu sein.

Der Benachrichtigungsbereich ist ein Teil der Taskleiste, der eine temporäre Quelle für Benachrichtigungen und den Status bietet. Es kann auch verwendet werden, um Symbole für System- und Programmfunktionen anzuzeigen, die nicht auf dem Desktop enthalten sind.

Elemente im Benachrichtigungsbereich werden als Benachrichtigungsbereichssymbole oder einfach symbole bezeichnet, wenn der Kontext des Benachrichtigungsbereichs bereits eindeutig festgelegt ist.

![Screenshot des Benachrichtigungsbereichs, der Uhrzeit und des Datums ](images/winenv-notification-image1.png)

Der Benachrichtigungsbereich.

Um Benutzern die Kontrolle über ihren Desktop in Windows 7 zu geben, werden standardmäßig nicht alle Symbole für den Benachrichtigungsbereich angezeigt. Stattdessen werden Symbole im Überlauf des Benachrichtigungsbereichs angezeigt, es sei denn, sie werden vom Benutzer auf den Benachrichtigungsbereich auf den Benachrichtigungsbereich um 2017 um 100:

![Screenshot: Benachrichtigungsbereich und Überlauf](images/winenv-notification-image2.png)

Der Überlauf des Benachrichtigungsbereichs.

**Hinweis:** Richtlinien für die [Taskleiste,](winenv-taskbar.md) [Benachrichtigungen](mess-notif.md) und [Balloons](ctrl-balloons.md) werden in separaten Artikeln vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

-   **Muss ihr Programm eine Benachrichtigung anzeigen?** Wenn ja, müssen Sie ein Symbol für den Benachrichtigungsbereich verwenden.
-   **Wird das Symbol vorübergehend angezeigt, um eine Statusänderung anzuzeigen?** In diesem Beispiel kann ein Symbol für den Benachrichtigungsbereich in Abhängigkeit von den folgenden Faktoren geeignet sein:

    -   **Ist der Status nützlich und relevant?** Das heißt, werden Benutzer wahrscheinlich das Symbol überwachen und ihr Verhalten als Folge dieser Informationen ändern? Falls nicht, zeigen Sie den Status entweder nicht an, oder speichern Sie ihn in einer Protokolldatei.

        **Falsch:**

        ![Screenshot des Benachrichtigungsbereichs mit Laufwerksymbol ](images/winenv-notification-image3.png)

        In diesem Beispiel ist das Laufwerkaktivitätssymbol nicht geeignet, da Benutzer ihr Verhalten wahrscheinlich nicht basierend darauf ändern.

    -   **Ist der Status kritisch? Ist sofortiges Handeln erforderlich?** Wenn ja, zeigen Sie die Informationen auf eine Weise an, die Aufmerksamkeit erfordert und nicht einfach ignoriert werden kann, z. B. [ein Dialogfeld](win-dialog-box.md).

    Programme, die für Windows 7 entwickelt wurden, können Überlagerungssymbole auf der Taskleistenschaltfläche des Programms verwenden, um Statusänderung anzuzeigen, sowie Statusleisten der Taskleiste, um den Fortschritt von Aufgaben mit langer Ausführung zu zeigen.

-   **Verfügt das Feature bereits über "Desktop presence"?** Wird das Feature bei der Ausführung in einem Fenster auf dem Desktop angezeigt (möglicherweise minimiert)? Falls ja, zeigen Sie den Status in der Statusleiste des [Programms,](ctrl-status-bars.md)in einem anderen Statusbereich oder Windows 7 direkt auf der Taskleistenschaltfläche an. Wenn das Feature nicht über Desktops verfügen, können Sie ein Symbol für den Programmzugriff und zum Anzeigen des Status verwenden.
-   **Soll das Symbol in erster Linie ein Programm starten oder schnell auf seine Features oder Einstellungen zugreifen?** Verwenden Sie in diesem Startmenü, um stattdessen Programme zu starten. Der Benachrichtigungsbereich ist nicht für den schnellen Programm- oder Befehlszugriff vorgesehen.

    ![Screenshot der Schnellstartsymbolleiste ](images/winenv-notification-image4.png)

    In diesem Beispiel von Windows Vista wird Schnellstart verwendet, um den Windows-Explorer zu starten und Windows Internet Explorer zu starten.

    Für Programme, die für Windows 7 entwickelt wurden, können Benutzer Taskleistenschaltflächen für den schnellen Programmzugriff anheften. Programme können eine Symbolleiste Sprungliste Miniaturansicht verwenden, um direkt über die Symbolleistenschaltfläche eines Programms auf häufig verwendete Befehle zu zugreifen. Der Schnellstart wird in 7 nicht Windows angezeigt.

    ![Screenshot der Taskleiste und Sprungliste mit Symbolen ](images/winenv-notification-image5.png)

    In diesem Beispiel wird ein Sprungliste für den schnellen Befehlszugriff verwendet.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="the-windows-desktop"></a>Der Windows Desktop

Der Windows Desktop verfügt über die folgenden Programmzugriffspunkte:

-   **Arbeitsbereich.** Der Bildschirmbereich, in dem Benutzer ihre Arbeit ausführen sowie Programme, Dokumente und ihre Verknüpfungen speichern können. Obwohl der Desktop technisch gesehen die Taskleiste enthält, bezieht er sich in den meisten Kontexten nur auf den Aufgabenbereich.
-   **Schaltfläche "Start".** Der Zugriffspunkt für alle Programme und speziellen Windows-Orte (Dokumente, Bilder, Musik, Spiele, Computer, Systemsteuerung) mit Listen "Zuletzt verwendet" für den schnellen Zugriff auf zuletzt verwendete Programme und Dokumente.
-   **Schnellstart.** Ein direkter Zugriffspunkt für vom Benutzer ausgewählte Programme. Schnellstart wurde aus Windows 7 entfernt.
-   **Taskleiste.** Der Zugriffspunkt zum Ausführen von Programmen, die über Desktops verfügen. Obwohl sich die Taskleiste technisch gesehen über die gesamte Leiste vom Schaltfläche "Start" bis zum Benachrichtigungsbereich erstreckt, bezieht sich die Taskleiste in den meisten Kontexten auf den Dazwischenbereich, der die Taskleistenschaltflächen enthält. Dieser Bereich wird manchmal als Taskband bezeichnet.
-   **Deskbands. Nicht empfohlen.**
-   **Benachrichtigungsbereich.** Eine kurzfristige Quelle für Benachrichtigungen und Status sowie ein Zugriffspunkt für system- und programmbezogene Features, die nicht auf dem Desktop verfügbar sind.

![Screenshot: Identifizieren von Desktopzugriffspunkten ](images/winenv-notification-image6.png)

Die Windows Desktopzugriffspunkte umfassen Schaltfläche "Start", Taskleiste und Benachrichtigungsbereich. Beachten Sie das Miniaturbildfeature der Taskleistenschaltfläche.

**Der Desktop ist eine eingeschränkte, freigegebene Ressource, die der Einstiegspunkt des Benutzers für Windows.** Lassen Sie Die Benutzer die Kontrolle. Sie sollten die Desktopbereiche wie vorgesehen verwenden, wenn jede andere Nutzung als Missbrauch angesehen werden sollte. Zeigen Sie Desktopbereiche z. B. nie als Möglichkeiten an, Ihr Programm oder dessen [Marke zu bewerben.](exper-branding.md)

### <a name="using-the-notification-area-appropriately"></a>Verwenden des Benachrichtigungsbereichs entsprechend

Der Benachrichtigungsbereich war ursprünglich als temporäre Quelle für Benachrichtigungen und den Status vorgesehen. Seine Effizienz und Benutzerfreundlichkeit hat Entwickler dazu aufgefordert, ihm andere Zwecke zu geben, z. B. das Starten von Programmen und das Ausführen von Befehlen. Leider haben diese Ergänzungen den Benachrichtigungsbereich im Laufe der Zeit zu groß und laut gemacht und seinen Zweck mit den anderen Desktopzugriffspunkten verwechselt.

Windows XP hat das Skalierungsproblem behoben, indem der Bereich reduzierbar gemacht und die nicht verwendeten Symbole verborgen wurden. Windows Vista hat das Rauschen behoben, indem unnötige, unerlässige Benachrichtigungen entfernt wurden. Windows 7 wurde ein Schritt weiter gehen, indem die Benachrichtigung auf ihren ursprünglichen Zweck als Benachrichtigungsquelle konzentriert wurde. **Die meisten Symbole werden standardmäßig in Windows 7 ausgeblendet, können jedoch manuell vom Benutzer zum Benachrichtigungsbereich promotet werden. Um Benutzer die Kontrolle über ihre Desktops zu behalten, gibt es keine Möglichkeit für Ihr Programm, diese Promotion automatisch durchzuführen.** Windows werden weiterhin Benachrichtigungen für ausgeblendete Symbole angezeigt, indem sie vorübergehend weiter benachrichtigungen werden.

![Screenshot: Benachrichtigungsbereich und Überlauf ](images/winenv-notification-image7.png)

In Windows 7 sind die meisten Benachrichtigungsbereichssymbole standardmäßig ausgeblendet.

Darüber hinaus unterstützt Windows 7 viele Features direkt in den Taskleistenschaltflächen. Insbesondere können Sie:

-   Sprunglisten und Miniaturansichtssymbolleisten, um schnell auf häufig verwendete Befehle zu zugreifen.
-   Überlagerungssymbole, um den Status für ausgeführte Programme anzuzeigen.
-   Statusleisten der Taskleistenschaltfläche, um den Fortschritt für Aufgaben mit langer Ausführungslauf zu zeigen.

Kurz gesagt: Wenn Ihr Programm desktop verfügbar ist, können Sie die Funktionen der Windows 7-Taskleistenschaltfläche für diese Zwecke voll nutzen. **Halten Sie die Symbole für den Benachrichtigungsbereich auf die Anzeige von Benachrichtigungen und Status ausgerichtet.**

### <a name="keeping-users-in-control"></a>Behalten der Kontrolle über Benutzer

Die Kontrolle der Benutzer reicht über die korrekte Verwendung des Benachrichtigungsbereichs hinaus. Abhängig von der Art Ihres Symbols können Sie es Benutzern ermöglichen, folgende Schritte zu unternehmen:

-   **Entfernen Sie das Symbol.** Ihr Symbol stellt möglicherweise einen relevanten, nützlichen Status zur Verfügung, aber dennoch möchten Benutzer es möglicherweise nicht sehen. Windows können Benutzer Symbole ausblenden, aber dieses Feature ist nicht leicht erkennbar. Um die Kontrolle über  Benutzer zu behalten, geben Sie im Kontextmenü des Symbols die Option Symbol anzeigen im Benachrichtigungsbereich an. Beachten Sie, dass das Entfernen eines Symbols keine Auswirkungen auf das zugrunde liegende Programm, Feature oder Denkprozess haben muss.
-   **Wählen Sie die anzuzeigenden Benachrichtigungstypen aus.** Ihre Benachrichtigung muss nützlich und relevant sein, aber es gibt möglicherweise Benachrichtigungen, die Benutzer nicht sehen möchten. Dies gilt insbesondere für [](mess-notif.md)FYI-Benachrichtigungen. Ermöglichen Sie es Benutzern, die weniger wichtigen zu aktivieren.
-   **Optionale Features werden angehalten.** Symbole werden verwendet, um den Status für Features ohne Desktopdarstellung anzuzeigen. Solche Features sind in der Regel lang ausgeführte, optionale Hintergrundaufgaben, z. B. Drucken, Indizieren, Scannen oder Synchronisieren. Benutzer möchten solche Features möglicherweise aussetzen, um die Systemleistung zu erhöhen, den Energieverbrauch zu reduzieren oder weil sie offline sind.
-   **Beenden Sie das Programm.** Geben Sie die geeignetere dieser Optionen an:
    -   **Programm vorübergehend beenden.** Das Programm wird beendet und neu gestartet, wenn Windows neu gestartet wird. Dieser Ansatz eignet sich für wichtige Systemprogramme wie Sicherheitsprogramme.
    -   **Programm dauerhaft beenden.** Das Programm wird beendet und nicht neu gestartet, Windows neu gestartet wird (es sei denn, der Benutzer entscheidet sich für einen späteren Neustart). Entweder möchte der Benutzer das Programm nicht mehr ausführen, oder er möchte das Programm bei Bedarf ausführen, um möglicherweise die Systemleistung zu verbessern.

Obwohl es eine gute Idee ist, die meisten dieser Einstellungen im Kontextmenü des Symbols zur Verfügung zu stellen, sollte die Standarderfahrung des Programms für die meisten Benutzer geeignet sein. Aktivieren Sie nicht standardmäßig alles, und erwarten Sie, dass Benutzer Features deaktivieren. Aktivieren Sie stattdessen die wichtigen Features standardmäßig, und ermöglichen Sie es Benutzern, zusätzliche Features wie gewünscht zu aktivieren.

**Wenn Sie nur vier Dinge tun...**

1.  Missbrauchen Sie den Benachrichtigungsbereich nicht. Verwenden Sie sie nur als Quelle für Benachrichtigungen und Status sowie für Features ohne Desktop-Präsenz.
2.  Behalten Sie die Kontrolle über Benutzer. Stellen Sie geeignete Optionen zum Steuern des Symbols, seiner Benachrichtigungen und der zugrunde liegenden Features zur Verfügung.
3.  Stellen Sie eine Standarderfahrung vor, die für die meisten Benutzer geeignet ist. Ermöglichen Sie es Benutzern, gewünschte Features zu aktivieren, anstatt zu erwarten, dass sie unerwünschte Features deaktivieren.
4.  Nutzen Sie die Funktionen der Windows 7-Taskleistenschaltfläche, um den Status anzuzeigen und die am häufigsten ausgeführten Aufgaben Ihres Programms effizient zu gestalten.

## <a name="usage-patterns"></a>Verwendungsmuster

Benachrichtigungsbereichssymbole haben mehrere Verwendungsmuster:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Systemstatus und Zugriff</strong><br/> Wird fortlaufend angezeigt, um den wichtigen, aber nicht kritischen Systemstatus anzuzeigen und zugriff auf relevante Features und Einstellungen zu ermöglichen. <br/></td>
<td>Systemfeatures, die Benachrichtigungsbereichssymbole benötigen, verfügen nicht über permanente Desktops. Kann auch als Benachrichtigungsquelle verwendet werden. <br/> <img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br/> In diesem Beispiel werden die Symbole "Akku", "Netzwerk" und "Volume" fortlaufend angezeigt, falls zutreffend.<br/></td>
</tr>
<tr class="even">
<td><strong>Status und Zugriff von Hintergrundaufgabe</strong><br/> Wird angezeigt, während eine Hintergrundaufgabe ausgeführt wird, um den Status anzuzeigen und Zugriff auf Features und Einstellungen zu ermöglichen. <br/></td>
<td>Hintergrundprozesse benötigen Benachrichtigungsbereichssymbole, wenn sie nicht auf dem Desktop verfügbar sind. Kann auch als Benachrichtigungsquelle verwendet werden. <br/> <img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br/> In diesem Beispiel können Benutzer mit dem Symbol "Aktionscenter" ihren Status auch dann überprüfen, wenn kein Desktop verfügbar ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>Temporärer Ereignisstatus</strong><br/> Programme mit Desktopdarstellung können Vorübergehend Symbole anzeigen, um wichtige Ereignisse oder Statusänderungen anzuzeigen. <br/></td>
<td><img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br/> In diesem Beispiel werden Symbole zum Drucken und Installieren von Updates vorübergehend angezeigt, um wichtige Ereignisse oder Statusänderungen anzuzeigen.<br/></td>
</tr>
<tr class="even">
<td><strong>Temporäre Benachrichtigungsquelle</strong><br/> Wird vorübergehend angezeigt, um eine Benachrichtigung anzuzeigen. Wird nach einem Timeout entfernt oder wenn das zugrunde liegende Problem behoben oder eine Aufgabe ausgeführt wird. <br/></td>
<td>Temporäre Symbole werden für reine Benachrichtigungsquellen bevorzugt. Zeigen Sie kein Symbol an, das keinen nützlichen, relevanten, dynamischen Status bietet, nur weil ein Feature in Zukunft möglicherweise eine Benachrichtigung anzeigen muss. <br/> <img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br/> In diesem Beispiel wird das Plug-and-Play-Symbol angezeigt, während eine neue Hardwarebenachrichtigung angezeigt wird.<br/></td>
</tr>
<tr class="odd">
<td><strong>Minimierte Einzelinstanzanwendung</strong><br/> Um die Übersichtlichkeit der Taskleiste zu reduzieren, kann eine Einzelinstanzanwendung mit langer Ausführung auf ein Benachrichtigungsbereichssymbol minimiert werden. <br/></td>
<td><img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br/> In diesem Beispiel von Windows Vista sind Outlook und Windows Live Messenger Einzelinstanzanwendungen, die symbole auf Benachrichtigungsbereiche minimieren.<br/> Erwägen Sie die Verwendung dieses Musters nur, wenn die folgenden Punkte zu berücksichtigen sind: <br/>
<ul>
<li>Die Anwendung kann nur eine einzelne Instanz haben.</li>
<li>Die Anwendung wird für einen längeren Zeitraum ausgeführt.</li>
<li>Das Symbol zeigt den Status an.</li>
<li>Das Symbol kann eine Benachrichtigungsquelle sein.</li>
<li>Dies ist optional, und Benutzer müssen <a href="glossary.md">sich für entscheiden.</a></li>
</ul>
Wenn alle diese Bedingungen erfüllt sind, werden durch die Minimierung auf ein Symbol keine zwei Zugriffspunkte mehr benötigt, wenn nur einer erforderlich ist. <br/> <strong>Hinweis:</strong> Dieses Symbolmuster wird nicht mehr für Windows 7 empfohlen. Verwenden Sie stattdessen reguläre Taskleistenschaltflächen, wenn Ihr Programm über Desktops verfügt.<br/> <img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br/> In diesem Beispiel von Windows 7 nimmt eine normale Taskleistenschaltfläche wenig Platz ein, profitiert jedoch von den Funktionen der Windows 7-Taskleistenschaltfläche, einschließlich Sprunglisten, Überlagerungssymbolen und rich thumbnails.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Geben Sie pro Komponente nur ein Benachrichtigungsbereichssymbol an.**
-   **Verwenden Sie ein Symbol mit versionen mit 16 x 16, 20 x 20 und 24 x 24 Pixeln.** Die größeren Versionen werden in Anzeigemodi mit hohem DPI-Anteil verwendet.

### <a name="when-to-show"></a>Anzeigen von

-   Für das Muster der temporären Benachrichtigungsquelle:
    -   Windows zeigt das Symbol an, wenn die Benachrichtigung angezeigt wird.
    -   Entfernen Sie das Symbol basierend auf seinem [Benachrichtigungsentwurfsmuster:](mess-notif.md)



    | Muster                                     | Wann muss entfernt werden?                                         |
    |--------------------------------------|------------------------------------------|
    | Aktion erfolgreich<br/>            | Wenn die Benachrichtigung entfernt wird.<br/> |
    | Aktionsfehler<br/>            | Wenn das Problem behoben ist.<br/>     |
    | Nicht kritisches Systemereignis<br/> | Wenn das Problem behoben ist.<br/>     |
    | Optionale Benutzeraufgabe<br/>        | Wenn die Aufgabe fertig ist.<br/>            |
    | Fyi<br/>                       | Wenn die Benachrichtigung entfernt wird.<br/> |



 

-   **Zeigen Sie für das Temporäre Ereignisstatusmuster das Symbol an, während das Ereignis stattfindet.**
-   Zeigen Sie für alle anderen Muster das Symbol an, wenn das **Programm,** das Feature  oder der Prozess ausgeführt wird, und das Symbol ist relevant, es sei denn, der Benutzer hat die Option Symbol im Benachrichtigungsbereich anzeigen deaktivieren (weitere Informationen finden Sie unter [Kontextmenüs).](#context-menus) Die meisten Symbole werden standardmäßig in Windows 7 ausgeblendet, können jedoch vom Benutzer zum Benachrichtigungsbereich promotet werden.
-   **Zeigen Sie keine Symbole an, die für Administratoren für Standardbenutzer bestimmt sind.** Zeichnen Sie die Informationen im Windows-Ereignisprotokoll auf.

### <a name="where-to-show"></a>Anzeigen des Orts

-   **Anzeigen von Fenstern, die über Benachrichtigungsbereichssymbole in der Nähe des Benachrichtigungsbereichs gestartet werden.**

![Abbildung eines Fensters in der Nähe des Benachrichtigungsbereichs ](images/winenv-notification-image14.png)

Windows Benachrichtigungsbereich gestartete Symbole werden in der Nähe des Benachrichtigungsbereichs angezeigt.

### <a name="icons"></a>Symbole

-   **Wählen Sie das Symbol basierend auf seinem Entwurfsmuster aus:**

    | Muster                                                 | Symboltyp                                   |
    |--------------------------------------------------|------------------------------------|
    | Systemstatus und Zugriff<br/>              | Symbol "Systemfeature"<br/>     |
    | Status und Zugriff von Hintergrundaufgabe<br/>     | Symbol "Programm" oder "Feature"<br/> |
    | Temporäre Benachrichtigungsquelle<br/>         | Symbol "Programm" oder "Feature"<br/> |
    | Temporärer Ereignisstatus<br/>                | Programm- oder Featuresymbol<br/> |
    | Minimierte Einzelinstanzanwendung<br/> | Programmsymbol<br/>            |

    

     

    ![Screenshot des Infobereichs und der Outlook-Symbole ](images/winenv-notification-image15.png)

    In diesem Beispiel verwendet Outlook ein E-Mail-Featuresymbol für eine temporäre Benachrichtigungsquelle und das zugehörige Anwendungssymbol für die minimierte Anwendung.

-   **Wählen Sie ein leicht erkennbares Symboldesign aus.** Symbole mit eindeutigen Konturen gegenüber quadratischen oder rechteckigen Symbolen bevorzugen. Lassen Sie die Entwürfe einfach symbole gegenüber realistischen Bildern bevorzugen. Wenden Sie auch die anderen Richtlinien für [Symbole im Stil von Style Style](vis-icons.md) an.
-   **Verwenden Sie Symbolvariationen oder Überlagerungen, um Status- oder Statusänderungen anzuzeigen.** Verwenden Sie Symbolvariationen, um Änderungen in Mengen oder Stärken anzuzeigen. Verwenden Sie für andere Statustypen die folgenden Standardüberlagerungen. Verwenden Sie nur eine einzige Überlagerung, und suchen Sie sie aus Konsistenzgründen unten rechts. 

    | Überlagerung                                                                                                       | Status                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![Screenshot eines kleinen Warnsymbols ](images/winenv-notification-image16.png)<br/>               | Warnung<br/>               |
    | ![Screenshot des kleinen Fehlersymbols ](images/winenv-notification-image17.png)<br/>                 | Fehler<br/>                 |
    | ![Screenshot des Symbols "Klein deaktiviert/getrennt" ](images/winenv-notification-image18.png)<br/> | Deaktiviert/Getrennt<br/> |
    | ![Screenshot: kleines Symbol "Blockiert/Offline" ](images/winenv-notification-image19.png)<br/>       | Blockiert/Offline<br/>       |

    

     

    ![Screenshot des Infobereichs und zweier Symbole ](images/winenv-notification-image20.png)

    In diesem Beispiel zeigen die Funk- und Akkusymbole Änderungen in Mengen oder Stärken an.

    ![Screenshot des Infobereichs und zweier Überlagerungen ](images/winenv-notification-image21.png)

    In diesem Beispiel werden Überlagerungen verwendet, um Fehler- und Warnungszustände anzuzeigen.

-   **Vermeiden Sie in Ihren Basissymbolen Reine Rot-, Gelb- und Grünstriche.** Um Verwirrung zu vermeiden, reservieren Sie diese Farben, um den Status zu kommunizieren. Wenn Ihr [Branding](exper-branding.md) diese Farben verwendet, sollten Sie mutierte Töne für Ihre Basissymbole für den Benachrichtigungsbereich verwenden.
-   Verwenden Sie für [die progressive Eskalation](mess-notif.md)Symbole mit einer zunehmend **emphatischen Darstellung, wenn die Situation dringender wird.**

    ![Screenshot des Infobereichs und fünf Symbole ](images/winenv-notification-image22.png)

    In diesen Beispielen wird die Darstellung des Akkusymbols mit zunehmender Dringlichkeit deutlicher.

-   **Ändern Sie den Status nicht zu häufig.** Benachrichtigungsbereichssymbole dürfen nicht laut, instabil oder aufmerksamkeitsfähig sein. Das Auge reagiert empfindlich auf Änderungen im Peripheriebereich des Sehens, sodass Statusänderungen geringfügig sein müssen.
    -   **Ändern Sie das Symbol nicht schnell.** Wenn sich der zugrunde liegende Status schnell ändert, sollte das Symbol den Status auf hoher Ebene widerspiegeln.

        **Falsch:**

        ![Screenshot des Infobereichs und des Modemsymbols ](images/winenv-notification-image23.png)

        In diesem Beispiel zeigt das Modemsymbol blinkende Lichtlichter an (wie es ein Hardwaremodem tut), aber diese Zustandsänderungen sind für Benutzer nicht von Bedeutung.

    -   **Verwenden Sie keine Animationen mit langer Laufzeit, um fortlaufende Aktivitäten anzuzeigen.** Solche Animationen sind ablenkend. Das Vorhandensein eines Symbols im Benachrichtigungsbereich weist ausreichend auf eine kontinuierliche Aktivität hin.
    -   **Kurze, dezente Animationen sind akzeptabel, um den Fortschritt während wichtiger temporärer, transitiver Statusänderungen anzuzeigen.**

        ![Screenshot des Infobereichs und des Funksymbols ](images/winenv-notification-image24.png)

        In diesem Beispiel zeigt das Funksymbol einen Aktivitätsindikator an, um anzuzeigen, dass die Arbeit ausgeführt wird.

    -   **Blinken Sie das Symbol nicht.** Dies ist zu ablenkend. Wenn ein Ereignis sofortige Aufmerksamkeit erfordert, verwenden Sie stattdessen ein Dialogfeld. Wenn das Ereignis andernfalls Aufmerksamkeit benötigt, verwenden Sie eine Benachrichtigung.

-   **Deaktivieren Sie keine Symbole für den Benachrichtigungsbereich.** Wenn das Symbol derzeit nicht zutrifft, entfernen Sie es. Sie können jedoch ein aktiviertes Symbol mit einer deaktivierten Statusüberlagerung anzeigen, wenn Benutzer über das Symbol aktivieren können.

    ![Screenshot des Benachrichtigungsbereichs und des Lautstärkereglers ](images/winenv-notification-image25.png)

    In diesem Beispiel können Benutzer die Soundausgabe über das Symbol aktivieren.

Allgemeine Richtlinien und Beispiele für Symbole finden Sie unter [Symbole.](vis-icons.md)

### <a name="interaction"></a>Interaktion

**Hinweis:** Die folgenden Klickereignisse sollten mit dem Mauszeiger nach oben und nicht mit der Maus nach unten auftreten.

**Darauf zeigen (Hover)**

-   **Zeigt eine QuickInfo oder Infoinfo an, die angibt, was das Symbol darstellt.**

    ![Screenshot des Infobereichs und der QuickInfo ](images/winenv-notification-image26.png)

    In diesem Beispiel wird eine QuickInfo verwendet, um das Symbol beim Zeigen zu beschreiben.

Informationen zu Textrichtlinien finden Sie im Abschnitt [Text](#context-menus) dieses Artikels.

**Linker Einzelklick**

-   **Zeigen Sie alle Benutzer an,** die am wahrscheinlichsten angezeigt werden sollen. Dies kann sein:

    -   Ein Flyoutfenster, Dialogfeld oder Programmfenster mit den nützlichsten Einstellungen und häufig ausgeführten Aufgaben. Präsentationsrichtlinien finden Sie unter [Infobereichs-Flyouts.](#notification-area-flyouts)

        ![Screenshot des Infobereichs und der Flyouts ](images/winenv-notification-image27.png)

        In diesen Beispielen werden durch Klicken mit der linken Maustaste Popupfenster mit den nützlichsten Einstellungen angezeigt.

    -   Ein Status-Flyout.

        ![Screenshot des Infobereichs und des Status-Flyouts ](images/winenv-notification-image28.png)

        In diesem Beispiel wird durch Klicken auf die linke Maustaste das Status-Flyout angezeigt.

        -   Das zugehörige Systemsteuerungselement.
        -   Das Kontextmenü.

    Benutzer erwarten, dass ein Linker mit nur einem Klick etwas anzeigt, sodass ein Symbol für den Benachrichtigungsbereich nicht mehr reagiert, wenn nichts angezeigt wird.

-   **Zeigen Sie ein Kontextmenü nur an, wenn die anderen Optionen nicht angewendet werden,** wobei der Standardbefehl fett formatiert ist. Zeigen Sie in diesem Fall das kontextbezogene Menü an, das beim Rechtsklick angezeigt wird, um Verwechslungen zu vermeiden.
-   Verwenden Sie für ein einfacheres Gefühl lieber **ein Popupfenster als ein Dialogfeld.** Zeigen Sie nur die gängigsten Einstellungen an, und lassen Sie sie sofort für eine einfachere Interaktion wirksam werden. Schließen Sie das Popupfenster, wenn der Benutzer auf eine beliebige Stelle außerhalb des Fensters klickt.
-   **Zeigt kleine Fenster in der Nähe des zugeordneten Symbols an.** Große Fenster wie Systemsteuerungselemente können jedoch in der Mitte des Standardmonitors angezeigt werden.

**Doppelklicken auf die linke Seite**

-   **Führen Sie den Standardbefehl im Kontextmenü aus.** In der Regel wird dadurch die primäre Benutzeroberfläche angezeigt, die dem Symbol zugeordnet ist, z. B. das zugeordnete Systemsteuerungselement, das Eigenschaftenblatt oder das Programmfenster.
-   **Wenn kein Standardbefehl vorhanden ist, führen Sie die gleiche Aktion wie ein linker Einzelklick aus.**

**Klicken Sie mit der rechten Maustaste auf**

-   **Zeigen Sie das Kontextmenü** mit dem Standardbefehl fett an.

### <a name="context-menus"></a>Kontextmenüs

-   **Zeigen Sie das Kontextmenü in der Nähe des zugehörigen Symbols** an, aber weg von der Taskleiste.
-   **Das Kontextmenü kann ggf. die folgenden Elemente** in der aufgeführten Reihenfolge enthalten (genauer Text ist in Anführungszeichen):

Primäre Befehle

Öffnen (Standard, Zuerst auflisten, fett formatiert)

Ausführen

Sekundäre Befehle

< Trennzeichen>

Befehl zum Anhalten/Fortsetzen aktivieren/deaktivieren (Häkchen)

"Auf Benachrichtigungsbereich minimiert" (Häkchen)

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

Im falschen Beispiel sollte Windows Defender ein Häkchen verwenden, um den aktuellen Zustand anzugeben.

-   **Alle Hintergrundaufgaben müssen über den Befehl "Suspend/Resume" verfügen.** Wenn Sie den Befehl auswählen, sollte die Aufgabe vorübergehend angehalten werden. Möglicherweise möchten Benutzer Hintergrundaufgaben vorübergehend aussetzen, um die Systemleistung zu erhöhen oder den Energieverbrauch zu reduzieren. Angehaltene Hintergrundaufgaben werden neu gestartet, wenn sie vom Benutzer fortgesetzt oder Windows neu gestartet werden.
-   **Ermöglichen Sie es Benutzern, unterschiedliche** Benachrichtigungstypen zu aktivieren oder zu deaktivieren, wenn Ihr Programm Benachrichtigungen hat, die einige Benutzer möglicherweise nicht sehen möchten. Das [FYI-Benachrichtigungsmuster](mess-notif.md) erfordert, dass Benutzer sich dafür entscheiden, sodass diese Benachrichtigungen standardmäßig deaktiviert werden müssen.

![Screenshot des Benachrichtigungsbereichs und der Befehle ](images/winenv-notification-image31.png)

In diesem Beispiel ermöglicht Outlook Benutzern die Auswahl der Benachrichtigungen, die sie über das Symbol erhalten.

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
-   Verwenden Sie die Schaltfläche Minimieren in der Titelleiste der Anwendung, nicht die Schaltfläche Schließen.

## <a name="text"></a>Text

### <a name="infotips"></a>Infotips

-   Die Symbolinfo sollte eines der folgenden Formate haben (wobei der Firmenname optional ist):
    -   (Firmenname) Feature-, Programm- oder Gerätename
    -   ![Screenshot der Infotips mit Firmenname ](images/winenv-notification-image37.png)
    -   (Firmenname) Feature-, Programm- oder Gerätename: Statuszusammenfassung
    -   ![Screenshot der Infotips mit Statuszusammenfassung ](images/winenv-notification-image38.png)
    -   (Firmenname) Status-Anweisung für Feature-, Programm- oder Gerätenamen.
    -   ![Screenshot der Infotip mit status-Anweisung ](images/winenv-notification-image39.png)
    -   (Firmenname) Feature-, Programm- oder Gerätename
    -   Statusliste mit jedem Element in einer separaten Zeile
    -   ![Screenshot der Infotip-Anzeige der Statusliste ](images/winenv-notification-image40.png)

Infotip-Ausdruck:

-   Konzentrieren Sie sich auf die nützlichsten Informationen. Zeigen Sie weitere Informationen auf der linken Seite mit nur einem Klick an.
-   Seien Sie präzise. Verwenden Sie Satzfragmente oder einfache Anweisungen.
-   Verwenden Sie keine endende Interpunktion, es sei denn, Trinkgeld wird als vollständiger Satz formuliert.
-   Lassen Sie unnötige Wörter weg. Schließen Sie nicht die Softwareversion oder andere informationen ein.

    **Falsch:**

    ![Screenshot der Infotips mit unnötigen Informationen ](images/winenv-notification-image41.png)

    In diesem Beispiel enthält die Infotip zusätzliche Informationen.

-   Erläutern Sie nicht, wie Sie mit dem Symbol interagieren.

    **Falsch:**

    ![Screenshot der Infotips mit Rechtsklickanweisungen ](images/winenv-notification-image42.png)

    In diesem Beispiel enthält das Symbol Drahtlosnetzwerkverbindung Anweisungen mit der rechten Maustaste.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf den Benachrichtigungsbereich:

-   Verweisen Sie auf den Benachrichtigungsbereich als Benachrichtigungsbereich, nicht auf die Taskleiste.

Beim Verweisen auf ein Symbol für einen Benachrichtigungsbereich:

-   Verweisen Sie auf das Symbol, indem Sie den genauen Namen verwenden, der in der Infotip angegeben ist, einschließlich der Groß-/A-n, gefolgt von einem Symbol.
-   Die erste Referenz finden Sie auch im Benachrichtigungsbereich.
-   Formatieren Sie den Überschriftentext nach Möglichkeit fett. Andernfalls setzen Sie die Überschrift nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

**Beispiel:** Um den Netzwerkstatus schnell zu überprüfen, klicken Sie **im** Benachrichtigungsbereich auf das Symbol Netzwerk.

 


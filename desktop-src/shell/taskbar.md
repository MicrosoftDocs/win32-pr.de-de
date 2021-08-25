---
description: Die Windows-Schnittstelle enthält eine spezielle Desktopsymbolleiste für Anwendungen, die als Taskleiste bezeichnet wird. Sie können die Taskleiste für Aufgaben wie das Wechseln zwischen geöffneten Fenstern und das Starten neuer Anwendungen verwenden.
ms.assetid: 14d520e7-7c15-441d-9662-24b972d208ac
title: Taskleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a4943c242b0b3f0993a4cf542c8625e19cf25c32b71cb01e4ef8581d12d64c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773720"
---
# <a name="the-taskbar"></a>Taskleiste

Die Windows-Schnittstelle enthält eine spezielle [Desktopsymbolleiste](application-desktop-toolbars.md) der Anwendung, die als *Taskleiste* bezeichnet wird. Sie können die Taskleiste für Aufgaben wie das Wechseln zwischen geöffneten Fenstern und das Starten neuer Anwendungen verwenden.

> [!Note]  
> Informationen zu Änderungen, die ab Windows 7 an der Taskleiste vorgenommen wurden, finden Sie unter [Taskleistenerweiterungen.](taskbar-extensions.md)

 

Dieses Thema enthält folgende Abschnitte:

-   [Informationen zur Taskleiste](#about-the-taskbar)
    -   [Optionen für die Taskleistenanzeige](#taskbar-display-options)
    -   [Hinzufügen von Verknüpfungen zum Startmenü](#adding-shortcuts-to-the-start-menu)
    -   [Verwalten von Taskleistenschaltflächen](#managing-taskbar-buttons)
    -   [Hinzufügen, Ändern und Löschen von Symbolen im Benachrichtigungsbereich](#adding-modifying-and-deleting-icons-in-the-notification-area)
    -   [Taskleistenerstellungsbenachrichtigung](#taskbar-creation-notification)
-   [Verwenden der Taskleiste](#using-the-taskbar)
    -   [Hinzufügen und Löschen von Taskleistensymbolen im Infobereich](#adding-and-deleting-taskbar-icons-in-the-notification-area)
    -   [Empfangen von Mausereignissen](#receiving-mouse-events)

## <a name="about-the-taskbar"></a>Informationen zur Taskleiste

Die Taskleiste enthält Folgendes:

-   **Startmenü**
-   Schnellstart -Leiste (nur Windows Vista und früher)
-   Schaltflächen auf der Taskleiste
-   Symbolleisten (optional)
-   Benachrichtigungsbereich

Das **Startmenü** enthält Befehle, die auf Programme, Dokumente und Einstellungen zugreifen können. Zu diesen Befehlen gehören **Alle Programme,** **Dokumente,** **Systemsteuerung,** **Spiele,** **Hilfe und Support,** **Herunterfahren** und **Suchen von Programmen und Dateien.**

Der **Start** in früheren Versionen von Windows enthalten Elemente wie **Suchen** und **Ausführen,** deren Funktionalität in **Suchprogrammen und Dateien** in Windows Vista und höher enthalten war.

Die Schnellstart-Leiste, die in Versionen von Windows vor Windows 7 verfügbar ist, enthält Verknüpfungen zu Anwendungen. Windows stellt Standardeinträge bereit, z. B. Windows Internet Explorer, und der Benutzer kann beliebige weitere Tastenkombinationen hinzufügen. Symbole in diesem Bereich reagieren auf einen einzelnen Klick. In Windows 7 und höher ist diese Funktionalität in den Taskleistenschaltflächen enthalten.

Die Shell platziert immer dann eine Schaltfläche auf der Taskleiste, wenn eine Anwendung ein fensterloses Fenster erstellt, d.amp;n.b. ein Fenster, das kein übergeordnetes Fenster besitzt und über die entsprechenden erweiterten Stilbits verfügt (siehe [Verwalten von Taskleistenschaltflächen](#managing-taskbar-buttons)weiter unten). Um zu einem Fenster zu wechseln, klickt der Benutzer auf die Fensterschaltfläche. Diese Funktionalität wurde ab Windows 7 erheblich erweitert. Weitere Informationen finden Sie unter [Taskleistenerweiterungen.](taskbar-extensions.md)

Anwendungen können Symbole in den Infobereich setzen, um den Status eines Vorgangs anzugeben oder den Benutzer über ein Ereignis zu benachrichtigen. Beispielsweise kann eine Anwendung ein Druckersymbol in den Infobereich setzen, um anzuzeigen, dass ein Druckauftrag gerade läuft. In Windows 7 und höher sollten einige der zuvor vom Benachrichtigungsbereich bereitgestellten Informationen jedoch über die Taskleistenschaltfläche einer Anwendung bereitgestellt werden. Der Infobereich befindet sich am rechten Rand der Taskleiste (wenn die Taskleiste horizontal ist) oder am unteren Rand (wenn die Taskleiste vertikal ist). Weitere Informationen finden Sie unter [Benachrichtigungen und im Infobereich](notification-area.md).

Im Benachrichtigungsbereich wird auch die aktuelle Uhrzeit angezeigt, wenn diese Option ausgewählt ist. Die Option wird wie die folgende gefunden:

-   **Windows 7 und höher:** Die Dropdownliste **Uhr** auf der Seite **Systemsymbole aktivieren oder deaktivieren** der Anwendung **Benachrichtigungsbereichssymbole** Systemsteuerung (auch über die Eigenschaften des Infobereichs zugänglich).
-   **Windows Vista:** Das **Kontrollkästchen Uhr** auf der Seite **Benachrichtigungsbereich** des Eigenschaftenfensters **Taskleiste und Startmenü.**
-   **Windows XP:** Das Kontrollkästchen **Uhr anzeigen** im Eigenschaftenfenster **Taskleiste und Startmenü.**

Der Benutzer kann mit der rechten Maustaste auf die Taskleiste klicken, um das Kontextmenü anzuzeigen. Das Kontextmenü enthält Befehle zum Kaskadierten von Fenstern, Stapelfenstern, nebeneinander angezeigten Fenstern, Anzeigen des Desktops, Starten Task-Manager und Festlegen von Taskleisteneigenschaften. Das Kontextmenü bietet auch die Option zum Hinzufügen oder Entfernen eines Satzes von Symbolleisten aus der Taskleiste. Sie können diesem Menü neue Symbolleisten hinzufügen, indem Sie sie in der Kategorie CATID \_ DeskBand registrieren. Weitere Informationen finden Sie unter [Implementieren von Bandobjekten.](band-objects.md) Beachten Sie, dass die Taskleiste und der Benachrichtigungsbereich ab Windows 7 über separate Kontextmenüs verfügen. Diese Kontextmenüs teilen sich einige Optionen, z. B. die Fensteranordnung, und fügen andere hinzu.

### <a name="taskbar-display-options"></a>Optionen für die Taskleistenanzeige

Die Taskleiste unterstützt zwei Anzeigeoptionen: Automatisches Ausblenden und nur in Windows Vista und früher Always On Top (die Taskleiste befindet sich in Windows 7 und höher immer in diesem Modus). Um diese Optionen festzulegen, muss der Benutzer das Kontextmenü der Taskleiste öffnen, auf **Eigenschaften** klicken und das Kontrollkästchen **Taskleiste** automatisch ausblenden aktivieren oder deaktivieren oder das Kontrollkästchen **Taskleiste über anderen Fenstern beibehalten** aktivieren oder deaktivieren. Verwenden Sie die [**ABM \_ GETSTATE-Meldung,**](abm-getstate.md) um den Status dieser Anzeigeoptionen abzurufen. Wenn Sie benachrichtigt werden möchten, wenn sich der Status dieser Anzeigeoptionen ändert, verarbeiten Sie die [**ABN STATECHANGE-Benachrichtigungsmeldung \_**](abn-statechange.md) in Ihrer Fensterprozedur. Um den Status dieser Anzeigeoptionen zu ändern, verwenden Sie die [**ABM \_ SETSTATE-Meldung.**](abm-setstate.md)

Der *Arbeitsbereich* ist der Teil des Bildschirms, der nicht von der Taskleiste verdeckt wird. Um die Größe des Arbeitsbereichs abzurufen, rufen Sie die [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) auf, wobei der **SPI \_ GETWORKAREA-Wert** festgelegt ist. Verwenden Sie die [**ABM \_ GETTASKBARPOS-Nachricht,**](abm-gettaskbarpos.md) um die Rechteckkoordinaten abzurufen, die die Position der Taskleiste beschreiben.

Sie können die Taskleiste abdecken, indem Sie die Größe des Fensterrechtecks explizit auf die Größe des Bildschirms mit [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)festlegen. Bei Windows 2000-Systemen oder höher muss dem Fenster entweder [**WS \_ CAPTION**](../winmsg/window-styles.md) oder [**WS \_ THICKFRAME**](../winmsg/window-styles.md)fehlen. Andernfalls muss die Größe des Fensters so angepasst sein, dass der Clientbereich den gesamten Bildschirm abdeckt. Auch für diese Systeme gilt: Wenn die Taskleiste auf Always On Top festgelegt ist, bleibt sie nur ausgeblendet, während es sich bei der Anwendung um die Vordergrundanwendung handelt.

### <a name="adding-shortcuts-to-the-start-menu"></a>Hinzufügen von Verknüpfungen zum Startmenü

Führen Sie die folgenden Schritte aus, um dem Untermenü **Programme** in Microsoft Windows NT 4.0, Windows 2000 und höher oder Windows 95 oder höher ein Element hinzuzufügen.

1.  Erstellen Sie einen [Shelllink](./links.md) mithilfe der [**IShellLink-Schnittstelle.**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)
2.  Rufen Sie die PIDL des Ordners Programme mithilfe von [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation)ab, und übergeben Sie [**dabei CSIDL \_ PROGRAMS**](csidl.md).
3.  Fügen Sie den Shell-Link zum Ordner Programme hinzu. Sie können auch einen Ordner im Ordner Programme erstellen und den Link zu diesem Ordner hinzufügen.

### <a name="managing-taskbar-buttons"></a>Verwalten von Taskleistenschaltflächen

Die Shell erstellt immer dann eine Schaltfläche auf der Taskleiste, wenn eine Anwendung ein Fenster erstellt, das sich nicht im Besitz von befindet. Um sicherzustellen, dass die Fensterschaltfläche auf der Taskleiste platziert wird, erstellen Sie ein fensterloses Fenster mit dem erweiterten [**WS \_ EX \_ APPWINDOW-Stil.**](../winmsg/extended-window-styles.md) Um zu verhindern, dass die Fensterschaltfläche auf der Taskleiste platziert wird, erstellen Sie das fensterlose Fenster mit dem erweiterten [**WS \_ EX \_ TOOLWINDOW-Stil.**](../winmsg/extended-window-styles.md) Alternativ können Sie ein ausgeblendetes Fenster erstellen und dieses ausgeblendete Fenster zum Besitzer ihres sichtbaren Fensters machen.

Die Shell entfernt die Schaltfläche eines Fensters nur dann aus der Taskleiste, wenn der Stil des Fensters sichtbare Taskleistenschaltflächen unterstützt. Wenn Sie den Stil eines Fensters dynamisch in einen Stil ändern möchten, der keine sichtbaren Taskleistenschaltflächen unterstützt, müssen Sie zuerst das Fenster ausblenden (indem [**Sie ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) mit **SW \_ HIDE** aufrufen), den Fensterstil ändern und dann das Fenster anzeigen.

Die Fensterschaltfläche enthält in der Regel das Anwendungssymbol und den Titel. Wenn die Anwendung jedoch kein Systemmenü enthält, wird die Fensterschaltfläche ohne das Symbol erstellt.

Wenn Sie möchten, dass Ihre Anwendung die Aufmerksamkeit des Benutzers erhält, wenn das Fenster nicht aktiv ist, verwenden Sie die [**FlashWindow-Funktion,**](/windows/win32/api/winuser/nf-winuser-flashwindow) um den Benutzer darüber zu informieren, dass eine Nachricht wartet. Diese Funktion blinkt auf die Fensterschaltfläche. Sobald der Benutzer auf die Fensterschaltfläche klickt, um das Fenster zu aktivieren, kann Ihre Anwendung die Meldung anzeigen.

### <a name="modifying-the-contents-of-the-taskbar"></a>Ändern des Inhalts der Taskleiste

[Version 4.71 und höher](versions.md) von Shell32.dll fügt die Funktion zum Ändern des Inhalts der Taskleiste hinzu. In einer Anwendung können Sie nun Schaltflächen auf der Taskleiste hinzufügen, entfernen und aktivieren. Wenn Sie das Element aktivieren, wird das Fenster nicht aktiviert. es zeigt das Element wie auf der Taskleiste gedrückt an.

Die Taskleistenänderungsfunktionen werden in einem Component Object Model (COM)-Objekt (CLSID \_ TaskbarList) implementiert, das die [**ITaskbarList-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) (IID \_ ITaskbarList) verfügbar macht. Sie müssen die [**ITaskbarList::HrInit-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-hrinit) aufrufen, um das Objekt zu initialisieren. Anschließend können Sie die Methoden der [**ITaskbarList-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) verwenden, um den Inhalt der Taskleiste zu ändern.

### <a name="adding-modifying-and-deleting-icons-in-the-notification-area"></a>Hinzufügen, Ändern und Löschen von Symbolen im Benachrichtigungsbereich

Verwenden Sie die [**\_ Funktion NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) der Shell, um Symbole im Benachrichtigungsbereich hinzuzufügen, zu ändern oder zu löschen. Der *dwMessage-Parameter* von **Shell \_ NotifyIcon** ist eine Meldung an die Taskleiste, die die zu ergreifende Aktion angibt. Der *pnid-Parameter* ist ein Zeiger auf eine [**NOTIFYICONDATA-Struktur,**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) die verwendet wird, um das Symbol zu identifizieren und alle zusätzlichen Informationen zu übergeben, die für die Verarbeitung der Nachricht durch das System erforderlich sind.

Sie können die folgenden Aktionen mit Symbolen für den Benachrichtigungsbereich ausführen.

-   Um dem Infobereich der Taskleiste ein Symbol hinzuzufügen, rufen [**Sie Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) auf, wobei der *dwMessage-Parameter* auf NIM ADD festgelegt \_ ist. Die [**NOTIFYICONDATA-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) wird verwendet, um das Handle und den Bezeichner des Symbols sowie jeglichen QuickInfo-Text anzugeben. Wenn der Benutzer das Kontrollkästchen **Uhr anzeigen** in den Taskleisteneigenschaften aktiviert hat, platziert das System das Symbol direkt links neben der Uhr. Andernfalls wird das Symbol auf der rechten Seite oder am unteren Rand der Taskleiste angezeigt. Alle vorhandenen Symbole werden nach links verschoben, um Platz für das neue Symbol zu schaffen.
-   Um die Informationen eines Symbols zu ändern, einschließlich Symbolhandle, QuickInfo-Text und Rückrufmeldungs-ID, rufen [**Sie Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) auf, wobei *dwMessage* auf NIM MODIFY festgelegt \_ ist.
-   Um ein Symbol aus dem Benachrichtigungsbereich zu löschen, rufen [**Sie Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) auf, wobei der *dwMessage-Parameter* auf NIM DELETE festgelegt \_ ist.

Wenn Sie einen Benutzeroberflächenvorgang abgeschlossen haben, kehren Sie den Fokus zum Benachrichtigungsbereich zurück, indem [**Sie Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufrufen, wobei *dwMessage* auf NIM SETFOCUS festgelegt \_ ist. Sie können dies beispielsweise tun, wenn ein Taskleistensymbol ein Kontextmenü anzeigt, der Benutzer es jedoch abbricht, indem er die ESCAPE-TASTE drückt.

### <a name="receiving-notification-area-callback-messages"></a>Empfangen von Rückrufmeldungen im Benachrichtigungsbereich

Anwendungen legen Symbole häufig im Infobereich der Taskleiste ab, um als Statusindikatoren zu dienen. Sie können zusätzliche Informationen angeben, wenn der Benutzer Mausaktionen ausführt, z. B. das Bewegen des Mauszeigers über das Symbol oder das Klicken auf das Symbol.

Das System benachrichtigt Sie über Maus- und Tastaturereignisse, indem es eine anwendungsdefinierte Rückrufmeldung sendet, die einem bestimmten Symbol zugeordnet ist. Auf diese Weise kann das System eine Anwendung benachrichtigen, wenn der Benutzer beispielsweise auf das Symbol klickt oder es durch Drücken einer Taste auswählt.

Sie definieren die Rückrufmeldung eines Symbols, wenn Sie das Symbol zur Taskleiste hinzufügen. Der Bezeichner der Rückrufmeldung wird im **uCallbackMessage-Member** der [**NOTIFYICONDATA-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) angegeben, die mit NIM ADD übergeben \_ wird. Wenn ein Ereignis auftritt, sendet das System die Rückrufmeldung an die Fensterprozedur des Vom **hWnd-Member** angegebenen Fensters. Der *wParam-Parameter* der Nachricht enthält den Bezeichner des Taskleistensymbols, in dem das Ereignis aufgetreten ist. Der *lParam-Parameter* enthält die Maus- oder Tastaturmeldung, die dem Ereignis zugeordnet ist. Wenn der Mauszeiger beispielsweise auf ein Taskleistensymbol bewegt wird, enthält *lParam* [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md).

Die Ergebnisse verschiedener Mausereignisse können wie folgt zusammengefasst werden:

-   Wenn der Benutzer den Mauszeiger über das Symbol bewegt, zeigt das System den QuickInfo-Text an, der in [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)angegeben wurde.
-   Wenn der Benutzer auf das Symbol klickt, erhält Ihre Anwendung eine [**\_ WM-LBUTTONDOWN-Benachrichtigung.**](../inputdev/wm-lbuttondown.md)
-   Wenn der Benutzer mit der rechten Maustaste auf das Symbol klickt, erhält Ihre Anwendung eine [**\_ WM-RBUTTONDOWN-Benachrichtigung.**](../inputdev/wm-rbuttondown.md)
-   Wenn der Benutzer auf das Symbol doppelklickt, erhält Ihre Anwendung eine [**\_ WM-Benachrichtigung LBUTTONDBLCLK.**](../inputdev/wm-lbuttondblclk.md)

Wenn Sie auf das Symbol klicken, zeigt die Anwendung in der Regel ein Fenster mit zusätzlichen Informationen an, durch Klicken mit der rechten Maustaste wird ein Kontextmenü angezeigt, und durch Doppelklicken wird der Standardbefehl für das Kontextmenü ausgeführt.

Ein Beispiel zum Ändern des QuickInfo-Texts, der einem Symbol für den Benachrichtigungsbereich zugeordnet ist, finden Sie unter [Balloon Tooltips for Status Bar Icons (QuickInfos für Statusleistensymbole).](../controls/tooltip-controls.md)

Die Versionen 5.0 und höher der Shell behandeln [**Shell \_ NotifyIcon-Maus-**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) und Tastaturereignisse auf andere Weise als frühere Shellversionen, die in Windows NT 4.0, Windows 95 und Windows 98 gefunden wurden. Es gibt die folgenden Unterschiede:

-   Wenn ein Benutzer das Kontextmenü eines Benachrichtigungssymbols mit der Tastatur anfordert, sendet die Version 5.0 Shell der zugeordneten Anwendung eine [**WM \_ CONTEXTMENU-Nachricht.**](../menurc/wm-contextmenu.md) Frühere Versionen senden [**WM \_ RBUTTONDOWN-**](../inputdev/wm-rbuttondown.md) und [**WM \_ RBUTTONUP-Nachrichten.**](../inputdev/wm-rbuttonup.md)
-   Wenn ein Benutzer ein Benachrichtigungssymbol mit der Tastatur auswählt und es mit der Leertaste oder EINGABETASTE aktiviert, sendet die Version 5.0 Shell der zugeordneten Anwendung eine **NIN \_ KEYSELECT-Benachrichtigung.** Frühere Versionen senden [**WM \_ RBUTTONDOWN-**](../inputdev/wm-rbuttondown.md) und [**WM \_ RBUTTONUP-Nachrichten.**](../inputdev/wm-rbuttonup.md)
-   Wenn ein Benutzer ein Benachrichtigungssymbol mit der Maus auswählt und es mit der EINGABETASTE aktiviert, sendet die Version 5.0 Shell der zugeordneten Anwendung eine **NIN \_ SELECT-Benachrichtigung.** Frühere Versionen senden [**WM \_ RBUTTONDOWN-**](../inputdev/wm-rbuttondown.md) und [**WM \_ RBUTTONUP-Nachrichten.**](../inputdev/wm-rbuttonup.md)
-   Wenn ein Benutzer den Mauszeiger über ein Symbol übergibt, dem eine Sprechblasen-QuickInfo zugeordnet ist, sendet die Shell der Version 6.0 (Windows XP) die folgenden Nachrichten.
    -   -   **NIN \_ BALLOONSHOW:** Wird gesendet, wenn die Sprechblase angezeigt wird (Sprechblasen werden in die Warteschlange eingereiht).
        -   **NIN \_ BALLOONHIDE:** Wird gesendet, wenn die Sprechblase nicht mehr angezeigt wird, z. B. wenn das Symbol gelöscht wird. Diese Meldung wird nicht gesendet, wenn die Sprechblase aufgrund eines Timeouts oder Eines Mausklicks verworfen wird.
        -   **NIN \_ BALLOONTIMEOUT:** Wird gesendet, wenn die Sprechblase aufgrund eines Timeouts verworfen wird.
        -   **NIN \_ BALLOONUSERCLICK:** Wird gesendet, wenn die Sprechblase aufgrund eines Mausklicks verworfen wird.

Sie können auswählen, wie sich die Shell verhalten soll, indem [**\_ Sie Shell NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufrufen, wobei *dwMessage* auf **NIM \_ SETVERSION** festgelegt ist. Legen Sie den **uVersion-Member** der [**NOTIFYICONDATA-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) fest, um anzugeben, ob Das Verhalten von Version 5.0 oder vor Version 5.0 angezeigt werden soll.

### <a name="taskbar-creation-notification"></a>Taskleistenerstellungsbenachrichtigung

Mit Microsoft Internet Explorer 4.0 und höher benachrichtigt die Shell Anwendungen, dass die Taskleiste erstellt wurde. Wenn die Taskleiste erstellt wird, registriert sie eine Nachricht mit der TaskbarCreated-Zeichenfolge und überträgt diese Nachricht dann an alle Fenster der obersten Ebene. Wenn Ihre Taskleistenanwendung diese Meldung empfängt, sollte davon ausgegangen werden, dass alle hinzugefügten Taskleistensymbole entfernt wurden, und sie erneut hinzufügen. Dieses Feature gilt im Allgemeinen nur für Dienste, die bereits ausgeführt werden, wenn die Shell gestartet wird. Das folgende Beispiel zeigt eine sehr vereinfachte Methode für die Behandlung dieses Falls.

Auf Windows 10 überträgt die Taskleiste diese Meldung auch, wenn sich der DPI der primären Anzeige ändert.

```
LRESULT CALLBACK WndProc(HWND hWnd, 
                         UINT uMessage, 
                         WPARAM wParam, 
                         LPARAM lParam)
{
    static UINT s_uTaskbarRestart;

    switch(uMessage)
    {
        case WM_CREATE:
            s_uTaskbarRestart = RegisterWindowMessage(TEXT("TaskbarCreated"));
            break;
        
        default:
            if(uMessage == s_uTaskbarRestart)
                AddTaskbarIcons();
            break;
    }

    return DefWindowProc(hWnd, uMessage, wParam, lParam);
}
```



## <a name="using-the-taskbar"></a>Verwenden der Taskleiste

Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie Dem Taskleistenbenachrichtigungsbereich Symbole hinzugefügt und Rückrufmeldungen für Taskleistensymbole verarbeitet werden.

### <a name="adding-and-deleting-taskbar-icons-in-the-notification-area"></a>Hinzufügen und Löschen von Taskleistensymbolen im Infobereich

Sie fügen dem Infobereich der Taskleiste ein Symbol hinzu, indem Sie eine [**NOTIFYICONDATA-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) ausfüllen und dann die Struktur an [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) übergeben, wobei *dwMessage* auf **NIM \_ ADD** festgelegt ist. Die Strukturmember müssen das Handle für das Fenster angeben, das das Symbol hinzufügt, sowie den Symbolbezeichner und das Symbolhandle. Sie können auch QuickInfo-Text für das Symbol angeben. Wenn Sie Mausnachrichten für das Symbol empfangen müssen, geben Sie den Bezeichner der Rückrufmeldung an, die das System verwenden soll, um die Nachricht an die Fensterprozedur zu senden.

Die Funktion im folgenden Beispiel veranschaulicht, wie sie der Taskleiste ein Symbol hinzufüge.


```
// MyTaskBarAddIcon - adds an icon to the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window to receive callback messages 
// uID - identifier of the icon 
// hicon - handle to the icon to add 
// lpszTip - tooltip text 

BOOL MyTaskBarAddIcon(HWND hwnd, UINT uID, HICON hicon, LPSTR lpszTip) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
    tnid.uFlags = NIF_MESSAGE | NIF_ICON | NIF_TIP; 
    tnid.uCallbackMessage = MYWM_NOTIFYICON; 
    tnid.hIcon = hicon; 
    if (lpszTip) 
        hr = StringCbCopyN(tnid.szTip, sizeof(tnid.szTip), lpszTip, 
                           sizeof(tnid.szTip));
        // TODO: Add error handling for the HRESULT.
    else 
        tnid.szTip[0] = (TCHAR)'\0'; 
 
    res = Shell_NotifyIcon(NIM_ADD, &tnid); 
 
    if (hicon) 
        DestroyIcon(hicon); 
 
    return res; 
}
```



Um ein Symbol aus dem Taskleistenbenachrichtigungsbereich zu löschen, füllen Sie eine [**NOTIFYICONDATA-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) aus, und rufen [**Sie Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) mit *dwMessage* auf, die auf **NIM \_ DELETE** festgelegt ist. Geben Sie beim Löschen eines Taskleistensymbols nur die Member **cbSize,** **hWnd** und **uID** der Struktur an. Beispiel:


```
// MyTaskBarDeleteIcon - deletes an icon from the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window that added the icon. 
// uID - identifier of the icon to delete. 

BOOL MyTaskBarDeleteIcon(HWND hwnd, UINT uID) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
         
    res = Shell_NotifyIcon(NIM_DELETE, &tnid); 
    return res; 
}
```



### <a name="receiving-mouse-events"></a>Empfangen von Mausereignissen

Wenn Sie eine Rückrufmeldung für ein Taskleistensymbol angeben, sendet das System die Nachricht immer dann an Ihre Anwendung, wenn ein Mausereignis im umschließenden Rechteck des Symbols auftritt. Der *wParam-Parameter* der Nachricht gibt den Bezeichner des Taskleistensymbols an, und der *lParam-Parameter* der Nachricht gibt die Nachricht an, die das System als Ergebnis des Mausereignisses generiert hat.

Die Funktion im folgenden Beispiel stammt aus einer Anwendung, die der Taskleiste sowohl Akku- als auch Druckersymbole hinzufügt. Die Anwendung ruft die Funktion auf, wenn sie eine Rückrufmeldung empfängt. Die -Funktion bestimmt, ob der Benutzer auf eines der Symbole geklickt hat, und ruft bei einem Klick eine anwendungsdefinierte Funktion auf, um Statusinformationen anzuzeigen.


```
// On_MYWM_NOTIFYICON - processes callback messages for taskbar icons. 
// wParam - first message parameter of the callback message. 
// lParam - second message parameter of the callback message. 

void On_MYWM_NOTIFYICON(WPARAM wParam, LPARAM lParam) 
{ 
    UINT uID; 
    UINT uMouseMsg; 
 
    uID = (UINT) wParam; 
    uMouseMsg = (UINT) lParam; 
 
    if (uMouseMsg == WM_LBUTTONDOWN) 
    { 
        switch (uID) 
        { 
            case IDI_MYBATTERYICON: 
 
                // The user clicked the battery icon. Display the 
                // battery status. 
                ShowBatteryStatus(); 
                break; 
 
            case IDI_MYPRINTERICON: 
 
                // The user clicked the printer icon. Display the 
                // status of the print job. 
                ShowJobStatus(); 
                break; 
 
            default: 
                break; 
        } 
     } 

     return; 
 }
```



 

 

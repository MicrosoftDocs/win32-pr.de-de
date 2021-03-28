---
description: Die Windows-Benutzeroberfläche enthält eine spezielle Anwendungs Desktop-Symbolleiste, die Taskleiste heißt. Sie können die Taskleiste für Aufgaben wie das Wechseln zwischen geöffneten Fenstern und das Starten neuer Anwendungen verwenden.
ms.assetid: 14d520e7-7c15-441d-9662-24b972d208ac
title: Die Taskleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce37991c6265f02ab92ece62dbae341031d272a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994967"
---
# <a name="the-taskbar"></a>Die Taskleiste

Die Windows-Benutzeroberfläche enthält eine spezielle [Anwendungs Desktop-Symbolleiste](application-desktop-toolbars.md) , die *Taskleiste* heißt. Sie können die Taskleiste für Aufgaben wie das Wechseln zwischen geöffneten Fenstern und das Starten neuer Anwendungen verwenden.

> [!Note]  
> Informationen zu Änderungen, die ab Windows 7 an der Taskleiste vorgenommen wurden, finden Sie unter [Task leisten Erweiterungen](taskbar-extensions.md).

 

Dieses Thema enthält folgende Abschnitte:

-   [Informationen zur Taskleiste](#about-the-taskbar)
    -   [Anzeigeoptionen in der Taskleiste](#taskbar-display-options)
    -   [Hinzufügen von Verknüpfungen zum Startmenü](#adding-shortcuts-to-the-start-menu)
    -   [Verwalten von Task leisten Schaltflächen](#managing-taskbar-buttons)
    -   [Hinzufügen, ändern und Löschen von Symbolen im Benachrichtigungsbereich](#adding-modifying-and-deleting-icons-in-the-notification-area)
    -   [Benachrichtigung zur Task leisten Erstellung](#taskbar-creation-notification)
-   [Verwenden der Taskleiste](#using-the-taskbar)
    -   [Hinzufügen und Löschen von Task leisten Symbolen im Benachrichtigungsbereich](#adding-and-deleting-taskbar-icons-in-the-notification-area)
    -   [Empfangen von Mausereignissen](#receiving-mouse-events)

## <a name="about-the-taskbar"></a>Informationen zur Taskleiste

Die Taskleiste umfasst Folgendes:

-   **Startmenü**
-   Schnellstartleiste (nur Windows Vista und frühere Versionen)
-   Task leisten Schaltflächen
-   Symbolleisten (optional)
-   Benachrichtigungsbereich

Das **Startmenü** enthält Befehle, die auf Programme, Dokumente und Einstellungen zugreifen können. Zu diesen Befehlen zählen **Alle Programme**, **Dokumente**, **Systemsteuerung**, **Spiele**, **Hilfe und Support**, **herunter** fahren und **Durchsuchen von Programmen und Dateien**.

Der **Start** in früheren Versionen von Windows enthielt **Elemente wie suchen und** **Ausführen**, die Funktionalität von, die in **Such Programmen und-Dateien** in Windows Vista und höher enthalten war.

Die Schnellstartleiste, die in früheren Windows-Versionen als Windows 7 verfügbar ist, enthält Verknüpfungen zu Anwendungen. Windows bietet Standardeinträge, z. b. Windows Internet Explorer, und der Benutzer kann alle weiteren Verknüpfungen hinzufügen, die Sie auswählen. Symbole in diesem Bereich Antworten auf einen einzigen Mausklick. In Windows 7 und höher ist diese Funktionalität in den Schaltflächen der Taskleiste enthalten.

Die Shell platziert eine Schaltfläche auf der Taskleiste, wenn eine Anwendung ein nicht eigenes Fenster erstellt – d. h. ein Fenster, das nicht über ein übergeordnetes Element verfügt und über die entsprechenden erweiterten stilbits verfügt (siehe [Verwalten von Task](#managing-taskbar-buttons)leisten Schaltflächen weiter unten). Um zu einem Fenster zu wechseln, klickt der Benutzer auf die Fenster Schaltfläche. Diese Funktionalität wurde seit Windows 7 stark erweitert. Weitere Informationen finden Sie unter [Task leisten Erweiterungen](taskbar-extensions.md).

Anwendungen können Symbole im Benachrichtigungsbereich platzieren, um den Status eines Vorgangs anzugeben oder um den Benutzer über ein Ereignis zu benachrichtigen. Beispielsweise kann eine Anwendung ein Druckersymbol im Benachrichtigungsbereich platzieren, um anzuzeigen, dass ein Druckauftrag unterläuft. In Windows 7 und höher sollten jedoch einige der zuvor über den Benachrichtigungsbereich bereitgestellten Informationen über die Task leisten Schaltfläche einer Anwendung bereitgestellt werden. Der Benachrichtigungsbereich befindet sich am rechten Rand der Taskleiste (wenn die Taskleiste horizontal ist) oder unten (wenn die Taskleiste vertikal ist). Weitere Informationen finden Sie unter [Benachrichtigungen und Benachrichtigungsbereich](notification-area.md).

Im Benachrichtigungsbereich wird auch die aktuelle Zeit angezeigt, wenn diese Option ausgewählt ist. Die Option wird wie folgt gefunden:

-   **Windows 7 und** höher: die Dropdown Liste " **Uhr** " auf der Seite " **System Symbole ein-oder ausschalten** " der System Steuerungsanwendung " **Benachrichtigungs Bereichs Symbole** " (auch über die Benachrichtigungs Bereichs Eigenschaften zugänglich).
-   **Windows Vista**: das Kontrollkästchen **Uhr** auf der Seite **Benachrichtigungsbereich** der **Taskleiste und** im Eigenschaften Fenster des Start Menüs.
-   **Windows XP**: das Kontrollkästchen **Uhr anzeigen** in der **Taskleiste und im Startmenü** Eigenschaften Fenster.

Der Benutzer kann mit der rechten Maustaste auf die Taskleiste klicken, um das Kontextmenü anzuzeigen. Das Kontextmenü enthält Befehle zum Kaskadieren von Fenstern, Stapel Fenstern, Fenster nebeneinander anzeigen, den Desktop anzeigen, Task-Manager starten und Eigenschaften der Taskleiste festlegen. Das Kontextmenü bietet auch die Option zum Hinzufügen oder Entfernen eines Satzes von Symbolleisten aus der Taskleiste. Sie können diesem Menü neue Symbolleisten hinzufügen, indem Sie Sie in der Kategorie CATID \_ Deskband registrieren. Weitere Informationen finden Sie unter [Implementieren von Band Objekten](band-objects.md). Beachten Sie, dass die Taskleiste und der Benachrichtigungsbereich ab Windows 7 separate Kontextmenüs enthalten. Diese Kontextmenüs haben einige Optionen, wie z. b. die Fensteranordnung, und fügen andere hinzu.

### <a name="taskbar-display-options"></a>Anzeigeoptionen in der Taskleiste

Die Taskleiste unterstützt zwei Anzeigeoptionen: automatisch ausblenden und in Windows Vista und früheren Versionen Always on oben (die Taskleiste befindet sich immer in diesem Modus in Windows 7 und höher). Um diese Optionen festzulegen, muss der Benutzer das Kontextmenü der Taskleiste öffnen, auf **Eigenschaften** klicken und das Kontrollkästchen das **automatische Ausblenden der Taskleiste** aktivieren bzw. deaktivieren oder die **Taskleiste oberhalb von anderen Fenstern belassen** aktivieren bzw. deaktivieren. Verwenden Sie zum Abrufen des Status dieser Anzeigeoptionen die [**ABM \_ GetState**](abm-getstate.md) -Nachricht. Wenn Sie benachrichtigt werden möchten, wenn sich der Status dieser Anzeigeoptionen ändert, verarbeiten Sie die [**ABN \_ StateChange**](abn-statechange.md) -Benachrichtigungs Meldung in der Fenster Prozedur. Um den Zustand dieser Anzeigeoptionen zu ändern, verwenden Sie die [**ABM \_ SetState**](abm-setstate.md) -Nachricht.

Der *Arbeitsbereich* ist der Teil des Bildschirms, der von der Taskleiste nicht verdeckt wird. Um die Größe des Arbeitsbereichs abzurufen, rufen Sie die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion mit dem festgelegten **SPI- \_ getworkarea** -Wert auf. Zum Abrufen der Rechteck Koordinaten, die den Speicherort der Taskleiste beschreiben, verwenden Sie die [**ABM \_ gettaskbarpos**](abm-gettaskbarpos.md) -Nachricht.

Es ist möglich, die Taskleiste abzudecken, indem die Größe des Fenster Rechtecks explizit auf die Größe des Bildschirms mit [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)festgelegt wird. Bei Windows 2000-Systemen oder höher muss das Fenster entweder über die [**WS- \_ Beschriftung**](../winmsg/window-styles.md) oder über einen [**WS- \_ dicken Rahmen**](../winmsg/window-styles.md)verfügen. andernfalls muss das Fenster so groß sein, dass der Client Bereich den gesamten Bildschirm abdeckt. Auch für diese Systeme gilt: Wenn die Taskleiste auf Always on oben festgelegt ist, bleibt Sie nur ausgeblendet, während die Anwendung die Vordergrund Anwendung ist.

### <a name="adding-shortcuts-to-the-start-menu"></a>Hinzufügen von Verknüpfungen zum Startmenü

Um dem Untermenü " **Programme** " unter Microsoft Windows NT 4,0, Windows 2000 und höher oder Windows 95 oder höher ein Element hinzuzufügen, führen Sie die folgenden Schritte aus.

1.  Erstellen Sie eine [Shellverknüpfung](./links.md) mithilfe der [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle.
2.  Rufen Sie die PIDL des Ordners "Programme" mithilfe von " [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation)" ab, und übergeben Sie [**CSIDL- \_ Programme**](csidl.md).
3.  Fügen Sie den shelllink zum Ordner Programme hinzu. Sie können auch einen Ordner im Ordner Programme erstellen und diesem Ordner den Link hinzufügen.

### <a name="managing-taskbar-buttons"></a>Verwalten von Task leisten Schaltflächen

Die Shell erstellt immer dann eine Schaltfläche auf der Taskleiste, wenn eine Anwendung ein Fenster erstellt, das nicht im Besitz von ist. Um sicherzustellen, dass die Fenster Schaltfläche auf der Taskleiste platziert wird, erstellen Sie ein Fenster ohne Besitzer mit dem erweiterten [**WS \_ Ex \_ appwindow**](../winmsg/extended-window-styles.md) -Stil. Um zu verhindern, dass die Fenster Schaltfläche auf der Taskleiste platziert wird, erstellen Sie das Fenster ohne Besitzer mit dem erweiterten [**WS \_ Ex- \_ ToolWindow**](../winmsg/extended-window-styles.md) -Stil. Als Alternative können Sie ein ausgeblendetes Fenster erstellen und dieses verborgene Fenster als Besitzer Ihres sichtbaren Fensters festlegen.

Die Shell entfernt die Schaltfläche eines Fensters nur dann von der Taskleiste, wenn der Stil des Fensters sichtbare Task leisten Schaltflächen unterstützt. Wenn Sie den Stil eines Fensters dynamisch in ein Fenster ändern möchten, das sichtbare Task leisten Schaltflächen nicht unterstützt, müssen Sie das Fenster zuerst ausblenden (durch Aufrufen von [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) mit **SW \_ Hide**), den Fenster Stil ändern und dann das Fenster anzeigen.

Die Fenster Schaltfläche enthält in der Regel das Anwendungssymbol und den Titel. Wenn die Anwendung jedoch kein Systemmenü enthält, wird die Fenster Schaltfläche ohne das Symbol erstellt.

Wenn Sie möchten, dass Ihre Anwendung die Aufmerksamkeit des Benutzers erhält, wenn das Fenster nicht aktiv ist, verwenden Sie die Funktion " [**Flash Window**](/windows/win32/api/winuser/nf-winuser-flashwindow) ", um dem Benutzer mitzuteilen, dass eine Nachricht wartet. Diese Funktion blinkt die Fenster Schaltfläche. Sobald der Benutzer auf die Fenster Schaltfläche klickt, um das Fenster zu aktivieren, kann die Anwendung die Meldung anzeigen.

### <a name="modifying-the-contents-of-the-taskbar"></a>Ändern des Inhalts der Taskleiste

In [Version 4,71 und](versions.md) höher von Shell32.dll wird die Funktion zum Ändern des Inhalts der Taskleiste hinzugefügt. In einer Anwendung können Sie nun Task leisten Schaltflächen hinzufügen, entfernen und aktivieren. Durch das Aktivieren des Elements wird das Fenster nicht aktiviert; das Element wird auf der Taskleiste als gedrückt angezeigt.

Die Funktionen der Task leisten Änderung werden in einem Component Object Model (com)-Objekt (CLSID \_ taskbarlist) implementiert, das die [**itaskbarlist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) -Schnittstelle (IID \_ itaskbarlist) verfügbar macht. Sie müssen die [**itaskbarlist:: HrInit**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-hrinit) -Methode zum Initialisieren des-Objekts aufzurufen. Sie können dann die Methoden der [**itaskbarlist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) -Schnittstelle verwenden, um den Inhalt der Taskleiste zu ändern.

### <a name="adding-modifying-and-deleting-icons-in-the-notification-area"></a>Hinzufügen, ändern und Löschen von Symbolen im Benachrichtigungsbereich

Verwenden Sie [**die \_ NotifyIcon-Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) -Funktion, um Symbole aus dem Benachrichtigungsbereich hinzuzufügen, zu ändern oder zu löschen. Der *dwmessage* -Parameter von **Shell \_ NotifyIcon** ist eine Meldung an die Taskleiste, die die auszuführende Aktion angibt. Der *pnid* -Parameter ist ein Zeiger auf eine [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur, die verwendet wird, um das Symbol zu identifizieren und alle zusätzlichen Informationen zu übergeben, die für das System zur Verarbeitung der Nachricht erforderlich sind.

Sie können die folgenden Aktionen mit Benachrichtigungs Bereichs Symbolen ausführen.

-   Um dem Benachrichtigungsbereich der Taskleiste ein Symbol hinzuzufügen, müssen Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufrufen, wobei der *dwmessage* -Parameter auf Nim Add festgelegt ist \_ . Die [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur wird verwendet, um das Handle und den Bezeichner des Symbols und den QuickInfo-Text anzugeben. Wenn der Benutzer das Kontrollkästchen **Uhr anzeigen** in den Eigenschaften der Taskleiste aktiviert hat, platziert das System das Symbol direkt links neben der Uhr. Andernfalls wird das Symbol auf der rechten Seite oder unten auf der Taskleiste angezeigt. Alle vorhandenen Symbole werden nach links verschoben, um Platz für das neue Symbol zu schaffen.
-   Zum Ändern der Informationen eines Symbols, einschließlich des Symbol Handles, des QuickInfo-Texts und des Rückruf Meldungs Bezeichners, rufen Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) auf, wobei *dwmessage* auf Nim Modify festgelegt ist \_ .
-   Wenn Sie ein Symbol aus dem Benachrichtigungsbereich löschen möchten, müssen Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufrufen, wobei der Parameter *dwmessage* auf Nim Delete festgelegt ist \_ .

Wenn Sie einen Benutzeroberflächen Vorgang abgeschlossen haben, setzen Sie den Fokus auf den Benachrichtigungsbereich, indem Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufrufen, wobei *dwmessage* auf Nim SetFocus festgelegt ist \_ . Dies kann z. b. der Fall sein, wenn ein Task leisten Symbol ein Kontextmenü anzeigt, der Benutzer es jedoch durch Drücken der Escapetaste abbricht.

### <a name="receiving-notification-area-callback-messages"></a>Empfangen von Benachrichtigungs Bereichs-Rückruf Meldungen

Anwendungen platzieren im Benachrichtigungsbereich der Taskleiste häufig Symbole, die als Status Indikatoren dienen. Sie können zusätzliche Informationen bereitstellen, wenn der Benutzer Mausaktionen ausführt, z. b. Wenn Sie den Mauszeiger über das Symbol bewegen oder auf das Symbol klicken.

Das System benachrichtigt Sie über Maus-und Tastatur Ereignisse, indem eine Anwendungs definierte Rückruf Meldung gesendet wird, die mit einem bestimmten Symbol verknüpft ist. Auf diese Weise kann das System eine Anwendung Benachrichtigen, wenn der Benutzer beispielsweise auf das Symbol klickt oder es durch Drücken einer Taste auswählt.

Sie definieren die Rückruf Meldung eines Symbols, wenn Sie der Taskleiste das Symbol hinzufügen. Der Bezeichner der Rückruf Meldung wird im **ucallbackmessage** -Member der [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur angegeben, die mit Nim Add übermittelt wurde \_ . Wenn ein Ereignis auftritt, sendet das System die Rückruf Meldung an die Fenster Prozedur des Fensters, das durch den **HWND** -Member angegeben wird. Der *wParam* -Parameter der Nachricht enthält den Bezeichner des Task leisten Symbols, in dem das Ereignis aufgetreten ist. Der *LPARAM* -Parameter enthält die Maus-oder Tastatur Meldung, die dem Ereignis zugeordnet ist. Wenn der Mauszeiger z. b. auf ein Task leisten Symbol wechselt, enthält *LPARAM* den Titel [**WM \_ MouseMove**](../inputdev/wm-mousemove.md).

Die Ergebnisse verschiedener Mausereignisse können wie folgt zusammengefasst werden:

-   When the user moves the mouse pointer over the icon, the system displays the tooltip text that was specified in [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa).
-   Wenn der Benutzer auf das Symbol klickt, empfängt die Anwendung eine [**WM- \_ lbuttondown**](../inputdev/wm-lbuttondown.md) -Benachrichtigung.
-   Wenn der Benutzer mit der rechten Maustaste auf das Symbol klickt, erhält die Anwendung eine [**\_ rbuttondown**](../inputdev/wm-rbuttondown.md) -Benachrichtigung.
-   Wenn der Benutzer auf das Symbol doppelklickt, empfängt die Anwendung eine [**WM- \_ lbuttondblclk**](../inputdev/wm-lbuttondblclk.md) -Benachrichtigung.

Wenn Sie auf das Symbol klicken, wird in der Regel ein Fenster mit zusätzlichen Informationen angezeigt, mit der rechten Maustaste klicken Sie auf ein Kontextmenü anzeigen, und doppelklicken Sie auf führt den Standardkontext Menübefehl aus.

Ein Beispiel für das Ändern des QuickInfo-Texts, der mit einem Benachrichtigungs Bereichs Symbol verknüpft ist, finden Sie unter Quick Infos für die Symbol [Leiste für Status leisten Symbole](../controls/tooltip-controls.md).

In den Versionen 5,0 und höher der Shell [**werden \_ shellereignisse**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) für Maus-und Tastatur Ereignisse auf unterschiedliche Weise angezeigt als frühere Shellversionen, die unter Windows NT 4,0, Windows 95 und Windows 98 gefunden wurden. Es gibt die folgenden Unterschiede:

-   Wenn ein Benutzer das Kontextmenü für das Benachrichtigungssymbol mit der Tastatur anfordert, sendet die Shell der Version 5,0 der zugeordneten Anwendung eine " [**\_ ContextMenu**](../menurc/wm-contextmenu.md) "-Meldung. In früheren Versionen werden [**WM \_ rbuttondown**](../inputdev/wm-rbuttondown.md) -und [**WM \_ rbuttonup**](../inputdev/wm-rbuttonup.md) -Meldungen gesendet.
-   Wenn ein Benutzer ein Benachrichtigungssymbol mit der Tastatur auswählt und ihn mit der Leertaste oder der EINGABETASTE aktiviert, sendet die Shell der Version 5,0 der zugeordneten Anwendung eine Meldung vom Typ " **Nin \_ keyselect** ". In früheren Versionen werden [**WM \_ rbuttondown**](../inputdev/wm-rbuttondown.md) -und [**WM \_ rbuttonup**](../inputdev/wm-rbuttonup.md) -Meldungen gesendet.
-   Wenn ein Benutzer mit der Maus ein Benachrichtigungssymbol auswählt und ihn mit der EINGABETASTE aktiviert, sendet die Shell der Version 5,0 die zugeordnete Anwendung an die Meldung " **Nin \_ Select** ". In früheren Versionen werden [**WM \_ rbuttondown**](../inputdev/wm-rbuttondown.md) -und [**WM \_ rbuttonup**](../inputdev/wm-rbuttonup.md) -Meldungen gesendet.
-   Wenn ein Benutzer den Mauszeiger über ein Symbol übergibt, dem eine QuickInfo-Sprechblase zugeordnet ist, sendet die Shell der Version 6,0 (Windows XP) die folgenden Meldungen.
    -   -   **Nin \_ Balloonshow** : wird gesendet, wenn die Sprechblase angezeigt wird (Luftballons werden in die Warteschlange gestellt).
        -   **Nin \_ Balloonhide** : wird gesendet, wenn die Sprechblase ausgeblendet wird – z. b. wenn das Symbol gelöscht wird. Diese Nachricht wird nicht gesendet, wenn die Sprechblase aufgrund eines Timeouts oder eines Mausklicks verworfen wird.
        -   **Nin \_ Balloontimeout** : wird gesendet, wenn die Sprechblase aufgrund eines Timeouts verworfen wird.
        -   **Nin \_ Balloonuserclick** : wird gesendet, wenn die Sprechblase aufgrund eines Mausklicks verworfen wird.

Sie können auswählen, wie sich die Shell Verhalten soll, indem Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) aufrufen, wobei *dwmessage* auf **nim \_ setVersion** festgelegt ist. Legen Sie den **uversion** -Member der [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur auf fest, um anzugeben, ob Sie das Verhalten von Version 5,0 oder vor Version 5,0 wünschen.

### <a name="taskbar-creation-notification"></a>Benachrichtigung zur Task leisten Erstellung

Mit Microsoft Internet Explorer 4,0 und höher benachrichtigt die Shell Anwendungen, dass die Taskleiste erstellt wurde. Wenn die Taskleiste erstellt wird, registriert Sie eine Meldung bei der taskbarcreated-Zeichenfolge und überträgt diese Nachricht dann an alle Fenster der obersten Ebene. Wenn Ihre Task leisten Anwendung diese Nachricht empfängt, sollte davon ausgegangen werden, dass alle hinzugefügten Task leisten Symbole entfernt wurden und Sie erneut hinzugefügt werden. Diese Funktion gilt im Allgemeinen nur für Dienste, die bereits ausgeführt werden, wenn die Shell gestartet wird. Das folgende Beispiel zeigt eine sehr vereinfachte Methode zum Behandeln dieses Falls.

Unter Windows 10 überträgt die Taskleiste diese Nachricht auch, wenn der dpi-Abschnitt der primären Anzeige geändert wird.

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

Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie Symbole zum Infobereich der Taskleiste hinzugefügt werden und wie Rückruf Meldungen für Task leisten Symbole verarbeitet werden.

### <a name="adding-and-deleting-taskbar-icons-in-the-notification-area"></a>Hinzufügen und Löschen von Task leisten Symbolen im Benachrichtigungsbereich

Fügen Sie dem Benachrichtigungsbereich der Taskleiste ein Symbol hinzu, indem Sie eine [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur ausfüllen und dann die Struktur an [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) übergeben, wobei *dwmessage* auf **nim \_ Add** festgelegt ist. Die Strukturmember müssen das Handle für das Fenster angeben, das das Symbol hinzufügt, sowie den Symbol Bezeichner und das Symbol handle. Sie können auch QuickInfo-Text für das Symbol angeben. Wenn Sie Maus Nachrichten für das Symbol empfangen müssen, geben Sie den Bezeichner der Rückruf Meldung an, den das System zum Senden der Nachricht an die Fenster Prozedur verwenden soll.

Die Funktion im folgenden Beispiel veranschaulicht, wie Sie der Taskleiste ein Symbol hinzufügen.


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



Wenn Sie ein Symbol aus dem Infobereich der Taskleiste löschen möchten, füllen Sie eine [**notifyiendata**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) -Struktur aus, und nennen Sie [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , wobei *dwmessage* auf **nim \_ Delete** festgelegt ist. Wenn Sie ein Symbol für die Taskleiste löschen, geben Sie nur die Member **CBSIZE**, **HWND** und **UID** der Struktur an. Beispiel:


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

Wenn Sie für ein Task leisten Symbol eine Rückruf Meldung angeben, sendet das System die Meldung an die Anwendung, wenn ein Maus Ereignis im umgebenden Rechteck des Symbols auftritt. Der *wParam* -Parameter der Meldung gibt den Bezeichner des Task leisten Symbols an, und der *LPARAM* -Parameter der Nachricht gibt die Meldung an, die das System als Ergebnis des Maus Ereignisses generiert hat.

Die Funktion im folgenden Beispiel wird von einer Anwendung abgeleitet, die der Taskleiste sowohl Akku-als auch Drucker Symbole hinzufügt. Die Anwendung ruft die-Funktion auf, wenn Sie eine Rückruf Meldung empfängt. Die Funktion bestimmt, ob der Benutzer auf eines der Symbole geklickt hat, und ruft, wenn ein Klick aufgetreten ist, eine Anwendungs definierte Funktion auf, um Statusinformationen anzuzeigen.


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



 

 

---
description: Eine Anwendungs Desktop-Symbolleiste (auch als appbar bezeichnet) ist ein Fenster, das der Windows-Taskleiste ähnelt.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Verwenden von Anwendungs Desktop-Symbolleisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128469"
---
# <a name="using-application-desktop-toolbars"></a>Verwenden von Anwendungs Desktop-Symbolleisten

Eine *Anwendungs Desktop-Symbolleiste* (auch als appbar bezeichnet) ist ein Fenster, das der Windows-Taskleiste ähnelt. Er ist an einem Bildschirmrand verankert und enthält in der Regel Schaltflächen, die dem Benutzer einen schnellen Zugriff auf andere Anwendungen und Windows ermöglicht. Das System verhindert, dass andere Anwendungen den von einer appbar verwendeten Desktop Bereich verwenden. Eine beliebige Anzahl von appbars kann zu einem beliebigen Zeitpunkt auf dem Desktop vorhanden sein.

Dieses Thema enthält folgende Abschnitte:

-   [Informationen zu Anwendungs Desktop-Symbolleisten](#about-application-desktop-toolbars)
    -   [Senden von Nachrichten](#sending-messages)
    -   [Registrierung](#registration)
    -   [Größe und Position von appbar](#appbar-size-and-position)
    -   [Anwendungs Desktop-Symbolleisten automatisch ausblenden](#autohide-application-desktop-toolbars)
    -   [Appbar-Benachrichtigungs Meldungen](#appbar-notification-messages)
-   [Registrieren einer Anwendungs Desktop-Symbolleiste](#registering-an-application-desktop-toolbar)
-   [Festlegen der Größe und Position der appbar](#setting-the-appbar-size-and-position)
-   [Verarbeiten von appbar-Benachrichtigungs Meldungen](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a>Informationen zu Anwendungs Desktop-Symbolleisten

Windows bietet eine API, mit der Sie die vom System bereitgestellten appbar-Dienste nutzen können. Mithilfe der-Dienste wird sichergestellt, dass Anwendungs definierte appbars problemlos miteinander und mit der Taskleiste funktionieren. Das System verwaltet Informationen zu den einzelnen appbars und sendet die appbars-Meldungen, um Sie über Ereignisse zu benachrichtigen, die ihre Größe, Position und Darstellung beeinflussen können.

### <a name="sending-messages"></a>Senden von Nachrichten

Eine Anwendung verwendet einen speziellen Satz von Nachrichten, die als appbar-Meldungen bezeichnet werden, um eine appbar hinzuzufügen oder zu entfernen, die Größe und Position einer appbar festzulegen und Informationen über Größe, Position und Zustand der Taskleiste abzurufen. Zum Senden einer appbar-Nachricht muss eine Anwendung die [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) -Funktion verwenden. Die Parameter der Funktion enthalten einen Nachrichten Bezeichner, z. b. " [**ABM \_ New**](abm-new.md)", und die Adresse einer [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur. Die Strukturmember enthalten Informationen, die das System benötigt, um die angegebene Nachricht zu verarbeiten.

Für jede angegebene appbar-Nachricht verwendet das System einige Member der [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur und ignoriert die anderen. Das System verwendet jedoch immer die Member **CBSIZE** und **HWND** , sodass eine Anwendung diese Member für jede appbar-Nachricht ausfüllen muss. Der **CBSIZE** -Member gibt die Größe der Struktur an, und der **HWND** -Member ist das Handle für das Fenster der appbar.

Einige appbar-Meldungen fordern Informationen vom System an. Bei der Verarbeitung dieser Nachrichten kopiert das System die angeforderten Informationen in die [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur.

### <a name="registration"></a>Registrierung

Das System behält eine interne Liste von appbars bei und verwaltet Informationen zu den einzelnen Balken in der Liste. Das System verwendet die Informationen, um appbars zu verwalten, Dienste für diese auszuführen und Benachrichtigungs Meldungen zu senden.

Eine Anwendung muss eine appbar registrieren (d. h., Sie wird der internen Liste hinzugefügt), bevor appbar-Dienste vom System empfangen werden können. Zum Registrieren einer appbar sendet eine Anwendung die [**\_ neue ABM**](abm-new.md) -Nachricht. Die zugehörige [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur enthält das Handle für das Fenster der appbar und einen Anwendungs definierten Nachrichten Bezeichner. Das System verwendet den Nachrichten Bezeichner, um Benachrichtigungs Meldungen an die Fenster Prozedur des appbar-Fensters zu senden. Weitere Informationen finden Sie unter appbar-Benachrichtigungs Meldungen.

Eine Anwendung hebt die Registrierung einer appbar auf, indem Sie die [**ABM- \_ Entfernungs**](abm-remove.md) Meldung sendet. Durch das Aufheben der Registrierung einer appbar wird diese aus der internen Liste der appbars des Systems entfernt. Das System sendet keine Benachrichtigungs Meldungen mehr an die appbar oder verhindert, dass andere Anwendungen den von der appbar verwendeten Bildschirmbereich verwenden. Eine Anwendung sollte vor dem zerstören einer appbar immer **ABM \_ Entfernen** senden.

### <a name="appbar-size-and-position"></a>Größe und Position von appbar

Eine Anwendung sollte die Größe und Position einer appbar so festlegen, dass Sie keine Auswirkung auf andere appbars oder die Taskleiste hat. Jede appbar muss an einer bestimmten Bildschirm Kante verankert werden, und mehrere appbars können an einer Kante verankert werden. Wenn eine appbar jedoch am gleichen Rand wie die Taskleiste verankert ist, stellt das System sicher, dass sich die Taskleiste immer am äußersten Rand befindet.

Zum Festlegen der Größe und Position einer appbar wird von einer Anwendung zunächst ein Bildschirmrand und ein Begrenzungs Rechteck für die appbar vorgeschlagen, indem die [**ABM- \_ querypos**](abm-querypos.md) -Nachricht gesendet wird. Das System bestimmt, ob ein Teil des Bildschirmbereichs innerhalb des vorgeschlagenen Rechtecks von der Taskleiste oder einer anderen appbar verwendet wird, das Rechteck (falls erforderlich) anpasst und das angepasste Rechteck an die Anwendung zurückgibt.

Anschließend sendet die Anwendung die [**ABM- \_ SetPos**](abm-setpos.md) -Nachricht, um das neue Begrenzungs Rechteck für die appbar festzulegen. Auch hier kann das System das Rechteck anpassen, bevor es an die Anwendung zurückgegeben wird. Aus diesem Grund sollte die Anwendung das angepasste Rechteck verwenden, das von **ABM- \_ SetPos** zurückgegeben wird, um die endgültige Größe und Position festzulegen. Die Anwendung kann die [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) -Funktion verwenden, um die appbar in die Position zu verschieben.

Durch die Verwendung eines zweistufigen Prozesses zum Festlegen der Größe und Position ermöglicht das System der Anwendung das Bereitstellen von zwischen Feedback für den Benutzer während des Verschiebungs Vorgangs. Wenn der Benutzer z. b. eine appbar zieht, zeigt die Anwendung möglicherweise ein schattiertes Rechteck an, das die neue Position anzeigt, bevor die appbar tatsächlich verschoben wird.

Eine Anwendung sollte die Größe und Position der appbar nach der Registrierung festlegen und immer dann, wenn die appbar die [**ABN \_ -Benachrichtigungs**](abn-poschanged.md) Meldung erhält. Eine appbar empfängt diese Benachrichtigungs Meldung immer dann, wenn eine Änderung in der Größe, Position oder Sichtbarkeit der Taskleiste auftritt und wenn die Größe einer anderen appbar auf der gleichen Seite des Bildschirms geändert, hinzugefügt oder entfernt wird.

Wenn eine appbar die WM- \_ Aktivierungs Nachricht empfängt, sollte Sie die [**ABM- \_ Aktivierungs**](abm-activate.md) Nachricht senden. Wenn eine appbar eine "WM \_ Windows Message Message"-Nachricht empfängt, muss Sie auch " [**ABM \_ windowposchge**](abm-windowposchanged.md)" aufgerufen werden. Wenn diese Nachrichten gesendet werden, wird sichergestellt, dass das System die z-Reihenfolge der automatisch Ausblend enden appbars am gleichen Rand ordnungsgemäß festlegt.

### <a name="autohide-application-desktop-toolbars"></a>Anwendungs Desktop-Symbolleisten automatisch ausblenden

Eine appbar zum automatischen Ausblenden ist eine, die normalerweise ausgeblendet ist, aber sichtbar wird, wenn der Benutzer den Mauszeiger auf den Bildschirmrand bewegt, dem die appbar zugeordnet ist. Die appbar verbirgt sich wieder, wenn der Benutzer den Mauszeiger aus dem umgebenden Rechteck des Balkens bewegt.

Obwohl das System eine Reihe von verschiedenen appbars zu einem beliebigen Zeitpunkt zulässt, lässt es jeweils nur eine automatische Ausblend-appbar für jeden Bildschirmrand zu. Das System behält automatisch die z-Reihenfolge einer automatischen Ausblend-appbar bei (nur in der z-Reihen folgen Gruppe).

Eine Anwendung verwendet die [**ABM \_ setaudehidebar**](abm-setautohidebar.md) -Nachricht, um eine automatisch Ausgeblend Bare appbar zu registrieren oder die Registrierung aufzuheben. Die Meldung gibt den Edge für die appbar und ein Flag an, das angibt, ob die appbar registriert oder die Registrierung aufgehoben werden soll. Die Meldung schlägt fehl, wenn eine APP-Leiste zum automatischen Ausblenden registriert wird, aber eine bereits mit dem angegebenen Edge verknüpft ist. Eine Anwendung kann das Handle für die automatisch Ausblend Ende appbar abrufen, die einem Edge zugeordnet ist, indem die [**ABM \_ getautohidebar**](abm-getautohidebar.md) -Nachricht gesendet wird.

Eine APP-Leiste zum automatischen Ausblenden muss nicht als normale appbar registriert werden. Dies bedeutet, dass Sie nicht durch Senden der [**\_ neuen ABM**](abm-new.md) -Nachricht registriert werden muss. Eine appbar, die nicht von **ABM \_ neu** registriert ist, überlappt alle an der gleichen Bildschirm Kante verankerten appbars.

### <a name="appbar-notification-messages"></a>Appbar-Benachrichtigungs Meldungen

Das System sendet Nachrichten, um eine appbar über Ereignisse zu benachrichtigen, die ihre Position und Darstellung beeinflussen können. Die Nachrichten werden im Kontext einer Anwendungs definierten Nachricht gesendet. Die Anwendung gibt den Bezeichner der Nachricht an, wenn Sie die [**\_ neue ABM**](abm-new.md) -Nachricht zum Registrieren der appbar sendet. Der Benachrichtigungs Code befindet sich im *wParam* -Parameter der von der Anwendung definierten Nachricht.

Eine appbar empfängt die [**ABN \_**](abn-poschanged.md) -Benachrichtigungs Meldung, wenn sich die Größe, Position oder Sichtbarkeit der Taskleiste ändert, wenn eine andere appbar zum gleichen Bildschirmrand hinzugefügt wird oder wenn die Größe einer anderen appbar am gleichen Bildschirmrand geändert oder entfernt wird. Eine appbar sollte auf diese Benachrichtigungs Meldung reagieren, indem [**ABM \_ querypos**](abm-querypos.md) und [**ABM- \_ SetPos**](abm-setpos.md) -Nachrichten gesendet werden. Wenn sich die Position einer appbar geändert hat, sollte Sie die [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) -Funktion zum Verschieben an die neue Position abrufen.

Das System sendet die [**ABN \_ StateChange**](abn-statechange.md) -Benachrichtigungs Meldung immer dann, wenn der Zustand "automatisch ausblenden" oder "Always on-Top" der Taskleiste geändert wurde – d. h. wenn der Benutzer das Kontrollkästchen " **Always on-Top** " oder " **automatisch ausblenden** " auf der Eigenschaften Seite der Taskleiste aktiviert oder deaktiviert. Eine appbar kann diese Benachrichtigungs Meldung verwenden, um den Status der Taskleiste, wenn gewünscht, auf die Konformität festzulegen.

Wenn eine Vollbildanwendung gestartet wird oder wenn die letzte Vollbildanwendung geschlossen wird, empfängt eine appbar die [**ABN \_ fullscreenapp**](abn-fullscreenapp.md) -Benachrichtigungs Meldung. Der *LPARAM* -Parameter gibt an, ob die Vollbildanwendung geöffnet oder geschlossen wird. Wenn Sie geöffnet wird, muss die appbar am Ende der z-Reihenfolge ablegen. Die appbar sollte die Position der z-Reihenfolge wiederherstellen, wenn die letzte Vollbildanwendung geschlossen wurde.

Eine appbar empfängt die [**ABN- \_ windowarrange**](abn-windowarrange.md) -Benachrichtigungs Meldung, wenn der Benutzer im Kontextmenü der Taskleiste den vertikal kaskadierten, nebeneinander-oder Kachel Befehl auswählt. Das System sendet die Nachricht zweimal – vor der Neuanordnung der Fenster (*LPARAM* ist **true**) und nach dem Anordnen der Fenster (*LPARAM* ist **false**).

Eine appbar kann [**ABN \_ windowarrange**](abn-windowarrange.md) -Nachrichten verwenden, um sich selbst vom kaskadierenden oder Kachel Vorgang auszuschließen. Um sich selbst auszuschließen, sollte die appbar ausgeblendet werden, wenn *LPARAM* den Wert **true** hat, und sich Selbstanzeigen, wenn *LPARAM* den Wert **false** hat. Wenn eine appbar als Reaktion auf diese Meldung ausgeblendet wird, ist es nicht erforderlich, die [**ABM- \_ querypos**](abm-querypos.md) -und [**ABM- \_ SetPos**](abm-setpos.md) -Nachrichten als Antwort auf den Cascade-oder Tile-Vorgang zu senden.

## <a name="registering-an-application-desktop-toolbar"></a>Registrieren einer Anwendungs Desktop-Symbolleiste

Eine Anwendung muss eine appbar registrieren, indem Sie die [**\_ neue ABM**](abm-new.md) -Nachricht sendet. Beim Registrieren einer appbar wird Sie der internen Liste des Systems hinzugefügt, und dem System wird eine Nachrichten-ID für das Senden von Benachrichtigungs Meldungen an die appbar bereitstellt. Bevor die Anwendung beendet wird, muss die Registrierung der appbar aufgehoben werden, indem die [**ABM- \_ Entfernungs**](abm-remove.md) Meldung gesendet wird. Durch das Aufheben der Registrierung wird die appbar aus der internen Liste des Systems entfernt und verhindert, dass der Balken appbar-Benachrichtigungs Meldungen empfängt.

Die Funktion im folgenden Beispiel registriert oder hebt die Registrierung einer appbar auf, abhängig vom Wert eines booleschen Flag-Parameters.


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a>Festlegen der Größe und Position der appbar

Eine Anwendung sollte die Größe und Position einer appbar nach dem Registrieren der appbar festlegen, nachdem der Benutzer die appbar bewegt oder mit der Größe losgt hat und wenn die APP-Leiste die [**ABN \_ -Benachrichtigungs**](abn-poschanged.md) Meldung erhält. Vor dem Festlegen der Größe und Position der appbar fragt die Anwendung das System nach einem genehmigten umgebenden Rechteck ab, indem die [**ABM \_ querypos**](abm-querypos.md) -Nachricht gesendet wird. Das System gibt ein umgebenden Rechteck zurück, das die Taskleiste oder andere appbar nicht beeinträchtigt. Das System passt das Rechteck ausschließlich durch die rechtesubtraktion an; Es wird nicht versucht, die anfängliche Größe des Rechtecks beizubehalten. Aus diesem Grund sollte die appbar nach dem Senden von **ABM- \_ querypos** das Rechteck nach Bedarf einlesen.

Als nächstes übergibt die Anwendung das umgebende Rechteck mithilfe der [**ABM- \_ SetPos**](abm-setpos.md) -Nachricht an das System zurück. Anschließend wird die Funktion [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) aufgerufen, um die appbar in die Position zu verschieben.

Im folgenden Beispiel wird gezeigt, wie Sie die Größe und Position einer appbar festlegen.


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a>Verarbeiten von appbar-Benachrichtigungs Meldungen

Eine appbar empfängt eine Benachrichtigungs Meldung, wenn sich der Zustand der Taskleiste ändert, wenn eine Vollbildanwendung gestartet wird (oder der letzte Vorgang geschlossen wird) oder wenn ein Ereignis auftritt, das die Größe und Position der appbar beeinflussen kann. Im folgenden Beispiel wird gezeigt, wie die verschiedenen Benachrichtigungs Meldungen verarbeitet werden.


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



Die folgende Funktion passt das umgebende Rechteck einer appbar an und ruft dann die Anwendungs definierte appbarquerysetpos-Funktion (im vorherigen Abschnitt enthalten) auf, um die Größe und Position der Leiste entsprechend festzulegen.


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 

---
description: Eine Desktopsymbolleiste einer Anwendung (auch als App-Leiste bezeichnet) ist ein Fenster, das der Windows Taskleiste ähnelt.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Verwenden von Anwendungsdesktopsymbolleisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c8604136040f5f3a1b4c1e9fcecb3b0c26b087724f477e592857ca4046d3a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351450"
---
# <a name="using-application-desktop-toolbars"></a>Verwenden von Anwendungsdesktopsymbolleisten

Eine *Desktopsymbolleiste* einer Anwendung (auch als App-Leiste bezeichnet) ist ein Fenster, das der Windows Taskleiste ähnelt. Sie ist an einem Rand des Bildschirms verankert und enthält in der Regel Schaltflächen, die dem Benutzer schnellen Zugriff auf andere Anwendungen und Fenster ermöglichen. Das System verhindert, dass andere Anwendungen den desktop-Bereich verwenden, der von einer Appbar verwendet wird. Auf dem Desktop kann jederzeit eine beliebige Anzahl von App-Leisten vorhanden sein.

Dieses Thema enthält folgende Abschnitte:

-   [Informationen zu Anwendungsdesktopsymbolleisten](#about-application-desktop-toolbars)
    -   [Senden von Nachrichten](#sending-messages)
    -   [Registrierung](#registration)
    -   [Appbar-Größe und -Position](#appbar-size-and-position)
    -   [AutomatischesHideen von Anwendungsdesktopsymbolleisten](#autohide-application-desktop-toolbars)
    -   [Appbar-Benachrichtigungsmeldungen](#appbar-notification-messages)
-   [Registrieren einer Anwendungsdesktopsymbolleiste](#registering-an-application-desktop-toolbar)
-   [Festlegen der Größe und Position der Appbar](#setting-the-appbar-size-and-position)
-   [Verarbeiten von Appbar-Benachrichtigungsmeldungen](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a>Informationen zu Anwendungsdesktopsymbolleisten

Windows bietet eine API, mit der Sie die vom System bereitgestellten AppBar-Dienste nutzen können. Die Dienste stellen sicher, dass anwendungsdefinierte AppBars reibungslos miteinander und mit der Taskleiste funktionieren. Das System verwaltet Informationen zu jeder Appbar und sendet die AppBars-Nachrichten, um sie über Ereignisse zu benachrichtigen, die sich auf ihre Größe, Position und Darstellung auswirken können.

### <a name="sending-messages"></a>Senden von Nachrichten

Eine Anwendung verwendet einen speziellen Satz von Nachrichten, die als AppBar-Nachrichten bezeichnet werden, um eine Appbar hinzuzufügen oder zu entfernen, die Größe und Position einer Appbar festzulegen und Informationen über Größe, Position und Status der Taskleiste abzurufen. Um eine AppBar-Nachricht zu senden, muss eine Anwendung die [**SHAppBarMessage-Funktion**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) verwenden. Die Parameter der Funktion enthalten einen Nachrichtenbezeichner, z. B. [**ABM \_ NEW,**](abm-new.md)und die Adresse einer [**APPBARDATA-Struktur.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Die Strukturmember enthalten Informationen, die das System zum Verarbeiten der angegebenen Nachricht benötigt.

Für jede appbar-Nachricht verwendet das System einige Member der [**APPBARDATA-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) und ignoriert die anderen. Das System verwendet jedoch immer die Member **cbSize** und **hWnd,** sodass eine Anwendung diese Member für jede Appbar-Nachricht ausfüllen muss. Der **cbSize-Member** gibt die Größe der -Struktur an, und der **hWnd-Member** ist das Handle für das Fenster der Appbar.

Einige AppBar-Nachrichten fordern Informationen vom System an. Beim Verarbeiten dieser Nachrichten kopiert das System die angeforderten Informationen in die [**APPBARDATA-Struktur.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)

### <a name="registration"></a>Registrierung

Das System behält eine interne Liste von AppBars bei und verwaltet Informationen zu den einzelnen Balken in der Liste. Das System verwendet die Informationen, um AppBars zu verwalten, Dienste für sie auszuführen und Benachrichtigungsmeldungen zu senden.

Eine Anwendung muss eine AppBar registrieren (d. h. sie der internen Liste hinzufügen), bevor sie AppBar-Dienste vom System empfangen kann. Um eine Appbar zu registrieren, sendet eine Anwendung die [**ABM \_ NEW-Nachricht.**](abm-new.md) Die zugehörige [**APPBARDATA-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) enthält das Handle für das Fenster der Appbar und eine anwendungsdefinierte Meldungs-ID. Das System verwendet den Nachrichtenbezeichner, um Benachrichtigungsmeldungen an die Fensterprozedur des AppBar-Fensters zu senden. Weitere Informationen finden Sie unter Appbar-Benachrichtigungsmeldungen.

Eine Anwendung hebt die Registrierung einer Appbar auf, indem sie die [**ABM \_ REMOVE-Nachricht**](abm-remove.md) sendet. Wenn Sie die Registrierung einer Appbar aufheben, wird sie aus der internen Liste der AppBars des Systems entfernt. Das System sendet keine Benachrichtigungen mehr an die App-Leiste oder verhindert, dass andere Anwendungen den von der Appbar verwendeten Bildschirmbereich verwenden. Eine Anwendung sollte immer **ABM \_ REMOVE** senden, bevor eine Appbar zerstört wird.

### <a name="appbar-size-and-position"></a>Appbar-Größe und -Position

Eine Anwendung sollte die Größe und Position einer Appbar so festlegen, dass sie keine anderen App-Leisten oder die Taskleiste beeinträchtigt. Jede App-Leiste muss an einem bestimmten Rand des Bildschirms verankert werden, und mehrere App-Leisten können an einem Rand verankert werden. Wenn eine Appbar jedoch am gleichen Rand wie die Taskleiste verankert ist, stellt das System sicher, dass sich die Taskleiste immer am äußersten Rand befindet.

Um die Größe und Position einer Appbar festzulegen, schlägt eine Anwendung zunächst einen Bildschirmrand und ein umschließendes Rechteck für die Appbar vor, indem sie die [**ABM \_ QUERYPOS-Nachricht**](abm-querypos.md) sendet. Das System bestimmt, ob ein Teil des Bildschirmbereichs innerhalb des vorgeschlagenen Rechtecks von der Taskleiste oder einer anderen Appbar verwendet wird, passt das Rechteck (falls erforderlich) an und gibt das angepasste Rechteck an die Anwendung zurück.

Als Nächstes sendet die Anwendung die [**ABM \_ SETPOS-Nachricht,**](abm-setpos.md) um das neue umschließende Rechteck für die Appbar festzulegen. Auch hier kann das System das Rechteck anpassen, bevor es an die Anwendung zurückgegeben wird. Aus diesem Grund sollte die Anwendung das angepasste Rechteck verwenden, das von **ABM \_ SETPOS** zurückgegeben wird, um die endgültige Größe und Position festzulegen. Die Anwendung kann die [**MoveWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-movewindow) verwenden, um die App-Leiste an die Position zu verschieben.

Durch die Verwendung eines zweistufigen Prozesses zum Festlegen von Größe und Position ermöglicht das System der Anwendung, dem Benutzer während des Verschiebevorgangs zwischengeschaltetes Feedback zu geben. Wenn der Benutzer beispielsweise eine AppBar zieht, zeigt die Anwendung möglicherweise ein schattiertes Rechteck an, das die neue Position angibt, bevor die Appbar tatsächlich verschoben wird.

Eine Anwendung sollte die Größe und Position ihrer Appbar festlegen, nachdem sie registriert wurde und wann immer die Appbar die [**ABN \_ POSCHANGED-Benachrichtigung**](abn-poschanged.md) empfängt. Eine Appbar empfängt diese Benachrichtigungsmeldung, wenn eine Änderung der Größe, Position oder Sichtbarkeit der Taskleiste auftritt und wenn eine andere Appbar auf der gleichen Seite des Bildschirms geändert, hinzugefügt oder entfernt wird.

Wenn eine Appbar die WM \_ ACTIVATE-Nachricht empfängt, sollte sie die [**ABM \_ ACTIVATE-Nachricht**](abm-activate.md) senden. Wenn eine Appbar eine WM \_ WINDOWPOSCHANGED-Nachricht empfängt, muss sie [**auch ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md)aufrufen. Durch das Senden dieser Nachrichten wird sichergestellt, dass das System die Z-Reihenfolge aller automatischen App-Leisten auf demselben Edge ordnungsgemäß festlegt.

### <a name="autohide-application-desktop-toolbars"></a>AutomatischesHideen von Anwendungsdesktopsymbolleisten

Eine Appbar mit automatischer Drosselung ist normalerweise ausgeblendet, wird aber sichtbar, wenn der Benutzer den Mauszeiger auf den Bildschirmrand bewegt, dem die Appbar zugeordnet ist. Die App-Leiste blendet sich erneut aus, wenn der Benutzer den Mauszeiger aus dem umschließenden Rechteck der Leiste bewegt.

Obwohl das System zu einem bestimmten Zeitpunkt eine Reihe verschiedener App-Leisten zulässt, lässt es für jeden Bildschirmrand jeweils nur eine appbar automatischhide auf einer ersten, zuerst bedienten Basis zu. Das System verwaltet automatisch die Z-Reihenfolge einer appbar für die automatische Drosselung (nur innerhalb der Z-Reihenfolge-Gruppe).

Eine Anwendung verwendet die [**ABM \_ SETAUTOHIDEBAR-Nachricht,**](abm-setautohidebar.md) um eine appbar für die automatische Benachrichtigung zu registrieren oder deren Registrierung zu aufheben. Die Meldung gibt den Rand für die Appbar und ein Flag an, das angibt, ob die Appbar registriert oder nicht registriert werden soll. Die Meldung schlägt fehl, wenn eine appbar für die automatische Benachrichtigung registriert wird, aber bereits eine appbar dem angegebenen Edge zugeordnet ist. Eine Anwendung kann das Handle zur automatischen Appbar abrufen, die einem Edge zugeordnet ist, indem sie die [**ABM \_ GETAUTOHIDEBAR-Nachricht**](abm-getautohidebar.md) sendet.

Eine appbar für automatischesHide muss nicht als normale AppBar registriert werden. Das heißt, sie muss nicht durch Senden der [**ABM \_ NEW-Nachricht**](abm-new.md) registriert werden. Eine Appbar, die nicht von **ABM \_ NEW** registriert wird, überschneidet sich mit allen App-Leisten, die am gleichen Bildschirmrand verankert sind.

### <a name="appbar-notification-messages"></a>Appbar-Benachrichtigungsmeldungen

Das System sendet Nachrichten, um eine Appbar über Ereignisse zu benachrichtigen, die sich auf die Position und Darstellung auswirken können. Die Nachrichten werden im Kontext einer anwendungsdefiniert Nachricht gesendet. Die Anwendung gibt den Bezeichner der Nachricht an, wenn sie die [**ABM \_ NEW-Nachricht**](abm-new.md) sendet, um die Appbar zu registrieren. Der Benachrichtigungscode befindet sich im *wParam-Parameter* der anwendungsdefinierte Nachricht.

Eine Appbar empfängt die [**ABN \_ POSCHANGED-Benachrichtigung,**](abn-poschanged.md) wenn sich die Größe, Position oder Sichtbarkeit der Taskleiste ändert, wenn eine andere Appbar am gleichen Bildschirmrand hinzugefügt wird oder wenn eine andere Appbar am gleichen Bildschirmrand geändert oder entfernt wird. Eine Appbar sollte auf diese Benachrichtigung reagieren, indem [**ABM \_ QUERYPOS-**](abm-querypos.md) und [**ABM \_ SETPOS-Nachrichten**](abm-setpos.md) gesendet werden. Wenn sich die Position einer Appbar geändert hat, sollte sie die [**MoveWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-movewindow) aufrufen, um sich selbst an die neue Position zu verschieben.

Das System sendet die [**ABN STATECHANGE-Benachrichtigungsmeldung \_**](abn-statechange.md) immer dann, wenn sich der automatische Oder always On-Top-Zustand der Taskleiste geändert hat, d. h., wenn der Benutzer das Kontrollkästchen **Always On top** oder Auto **hide** auf dem Eigenschaftenblatt der Taskleiste auswählt oder löscht. Eine Appbar kann diese Benachrichtigung verwenden, um bei Bedarf ihren Zustand so festzulegen, dass er dem Zustand der Taskleiste entspricht.

Wenn eine Vollbildanwendung gestartet oder die letzte Vollbildanwendung geschlossen wird, empfängt eine Appbar die [**ABN FULLSCREENAPP-Benachrichtigungsmeldung. \_**](abn-fullscreenapp.md) Der *lParam-Parameter* gibt an, ob die Vollbildanwendung geöffnet oder geschlossen wird. Wenn sie geöffnet wird, muss die Appbar am unteren Rand der Z-Reihenfolge liegen. Die Appbar sollte ihre Z-Reihenfolge wiederherstellen, wenn die letzte Vollbildanwendung geschlossen wurde.

Eine Appbar empfängt die [**Benachrichtigung ABN \_ WINDOWARRANGE,**](abn-windowarrange.md) wenn der Benutzer im Kontextmenü der Taskleiste den Befehl Cascade, Tile Horizontally oder Tile Vertically auswählt. Das System sendet die Nachricht zweimal – vor dem Neuanordnen der Fenster (*lParam* ist **TRUE**) und nach dem Anordnen der Fenster (*lParam* ist **FALSE**).

Eine Appbar kann [**ABN \_ WINDOWARRANGE-Nachrichten**](abn-windowarrange.md) verwenden, um sich selbst vom Kaskadieren oder Kachelvorgang auszuschließen. Um sich selbst auszuschließen, sollte sich die App-Leiste selbst ausblenden, wenn *lParam* **TRUE** ist, und sich selbst anzeigen, wenn *lParam* **FALSE** ist. Wenn sich eine Appbar als Reaktion auf diese Nachricht ausblendet, muss sie die [**ABM \_ QUERYPOS-**](abm-querypos.md) und [**ABM \_ SETPOS-Nachrichten**](abm-setpos.md) nicht als Reaktion auf den Kaskadieren- oder Kachelvorgang senden.

## <a name="registering-an-application-desktop-toolbar"></a>Registrieren einer Anwendungsdesktopsymbolleiste

Eine Anwendung muss eine AppBar registrieren, indem sie die [**\_ ABM NEW-Nachricht**](abm-new.md) sendet. Durch das Registrieren einer AppBar wird sie der internen Liste des Systems hinzugefügt, und dem System wird ein Nachrichtenbezeichner zum Senden von Benachrichtigungsmeldungen an die App-Leiste angezeigt. Vor dem Beenden muss eine Anwendung die Registrierung der Appbar aufheben, indem die [**ABM \_ REMOVE-Nachricht**](abm-remove.md) gesendet wird. Durch die Aufhebung der Registrierung wird die AppBar aus der internen Liste des Systems entfernt, und die Leiste kann keine AppBar-Benachrichtigungen empfangen.

Die Funktion im folgenden Beispiel registriert eine Appbar, abhängig vom Wert eines booleschen Flagparameters, oder aufheben die Registrierung.


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



## <a name="setting-the-appbar-size-and-position"></a>Festlegen der Größe und Position der Appbar

Eine Anwendung sollte die Größe und Position einer Appbar festlegen, nachdem die Appbar registriert wurde, nachdem der Benutzer die Appbar verschoben oder dimensioniert hat und wenn die Appbar die [**ABN \_ POSCHANGED-Benachrichtigung**](abn-poschanged.md) empfängt. Vor dem Festlegen der Größe und Position der Appbar fragt die Anwendung das System nach einem genehmigten umschließenden Rechteck ab, indem die [**ABM \_ QUERYPOS-Nachricht**](abm-querypos.md) gesendet wird. Das System gibt ein umschließendes Rechteck zurück, das die Taskleiste oder eine andere Appbar nicht beeinträchtigt. Das System passt das Rechteck ausschließlich durch Rechtecksubtraktion an. es ist nicht erforderlich, die Anfangsgröße des Rechtecks zu erhalten. Aus diesem Grund sollte die App-Leiste das Rechteck nach Dem Senden von **ABM QUERYPOS nach Bedarf \_ neu justieren.**

Als Nächstes übergibt die Anwendung das umgebundene Rechteck mithilfe der [**ABM \_ SETPOS-Meldung**](abm-setpos.md) zurück an das System. Anschließend wird die [**MoveWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-movewindow) aufrufen, um die App-Leiste an die Position zu verschieben.

Das folgende Beispiel zeigt, wie Sie die Größe und Position einer App-Leiste festlegen.


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



## <a name="processing-appbar-notification-messages"></a>Verarbeiten von Appbar-Benachrichtigungsmeldungen

Eine App-Leiste empfängt eine Benachrichtigungsmeldung, wenn sich der Status der Taskleiste ändert, wenn eine Vollbildanwendung gestartet wird (oder die letzte anwendung geschlossen wird) oder wenn ein Ereignis auftritt, das sich auf die Größe und Position der Appbar auswirken kann. Das folgende Beispiel zeigt, wie die verschiedenen Benachrichtigungsmeldungen verarbeiten.


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



Die folgende Funktion passt das umgebundene Rechteck einer Appbar an und ruft dann die anwendungsdefinierte AppBarQuerySetPos-Funktion (im vorherigen Abschnitt enthalten) auf, um die Größe und Position des Balkens entsprechend festzulegen.


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



 

 

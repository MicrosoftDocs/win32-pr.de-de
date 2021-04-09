---
title: Implementieren von Quick Infos für die Nachverfolgung
description: Die nach Verfolgungs Quick Infos bleiben sichtbar, bis Sie explizit von der Anwendung geschlossen werden, und können die Position auf dem Bildschirm dynamisch ändern. Sie werden von Version 4,70 und höher der allgemeinen Steuerelemente unterstützt.
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036532"
---
# <a name="how-to-implement-tracking-tooltips"></a>Implementieren von Quick Infos für die Nachverfolgung

Die nach Verfolgungs Quick Infos bleiben sichtbar, bis Sie explizit von der Anwendung geschlossen werden, und können die Position auf dem Bildschirm dynamisch ändern. Sie werden von [Version 4,70](common-control-versions.md) und höher der allgemeinen Steuerelemente unterstützt.

Fügen Sie zum Erstellen einer nach Verfolgungs-QuickInfo das "ttf Track"- \_ Flag im **uFlags** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur ein, wenn Sie die [**TTM \_ AddTool**](ttm-addtool.md) -Nachricht senden.

Die Anwendung muss eine nach Verfolgungs-QuickInfo manuell aktivieren (anzeigen) und deaktivieren (ausblenden), indem eine [**TTM- \_ trackaktivierungs**](ttm-trackactivate.md) Meldung gesendet wird. Während eine nach Verfolgungs-QuickInfo aktiv ist, muss die Anwendung den Speicherort der QuickInfo angeben, indem [**TTM \_ trackposition**](ttm-trackposition.md) -Meldungen an das QuickInfo-Steuerelement gesendet werden. Da die Anwendung Aufgaben wie z. b. das Positionieren der QuickInfo behandelt, wird bei der Nachverfolgung von Quick Infos nicht das Steuer Flag " **ttf \_ subclass** " oder " [**TTM \_ relayevent**](ttm-relayevent.md) "

Die [**TTM \_ trackposition**](ttm-trackposition.md) -Meldung bewirkt, dass das QuickInfo-Steuerelement das Fenster mit einem von zwei Platzierungs Stilen anzeigt:

-   Standardmäßig wird die QuickInfo neben dem entsprechenden Tool an einer Position angezeigt, die das Steuerelement auswählt. Der ausgewählte Standort ist relativ zu den Koordinaten, die Sie mithilfe dieser Nachricht bereitstellen.
-   Wenn Sie den **\_ absoluten** Wert von ttf in den Member der toolinfo-Struktur einschließen, wird die [**QuickInfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) an der in der Meldung angegebenen Pixelposition angezeigt. In diesem Fall versucht das Steuerelement nicht, den Speicherort des QuickInfo-Fensters von den von Ihnen bereitgestellten Koordinaten zu ändern.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="implement-in-place-tooltips"></a>Implementieren von In-Place Quick Infos

Der **uFlags** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die im Beispiel verwendet wird, enthält das " **ttf \_ absolute** "-Flag. Ohne dieses Flag wählt das QuickInfo-Steuerelement aus, wo die QuickInfo angezeigt werden soll, und seine Position relativ zum Dialogfeld kann sich plötzlich ändern, wenn der Mauszeiger bewegt wird.

> [!Note]  
> `g_toolItem` ist eine globale [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur.

 

Im folgenden Beispiel wird veranschaulicht, wie ein ToolTip-Steuerelement für die Überwachung erstellt wird. Im Beispiel wird der gesamte Client Bereich des Hauptfensters als Tool angegeben.


```C++
HWND CreateTrackingToolTip(int toolID, HWND hDlg, WCHAR* pText)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hDlg, NULL, g_hInst,NULL);

    if (!hwndTT)
    {
      return NULL;
    }

    // Set up the tool information. In this case, the "tool" is the entire parent window.
    
    g_toolItem.cbSize   = sizeof(TOOLINFO);
    g_toolItem.uFlags   = TTF_IDISHWND | TTF_TRACK | TTF_ABSOLUTE;
    g_toolItem.hwnd     = hDlg;
    g_toolItem.hinst    = g_hInst;
    g_toolItem.lpszText = pText;
    g_toolItem.uId      = (UINT_PTR)hDlg;
    
    GetClientRect (hDlg, &g_toolItem.rect);

    // Associate the tooltip with the tool window.
    
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &g_toolItem); 
    
    return hwndTT;
}
            
```



### <a name="window-procedure-implementation"></a>Implementierung der Fenster Prozedur

Wenn sich der Mauszeiger im Client Bereich befindet, ist die QuickInfo aktiv und zeigt die Cursor Koordinaten an, wie in der folgenden Abbildung dargestellt.

![Screenshot eines Dialog Felds in einer QuickInfo werden die x-und y-Koordinaten des Mauszeigers angezeigt.](images/tt-tracking.png)

Der folgende Beispielcode wird aus der Fenster Prozedur für ein Dialogfeld angezeigt, in dem die im vorherigen Beispiel erstellte nach Verfolgungs-QuickInfo angezeigt wird. Die globale boolesche Variable *g \_ trackingmouse* wird verwendet, um zu bestimmen, ob es erforderlich ist, die QuickInfo zu reaktivieren und die Maus Nachverfolgung zurückzusetzen, damit die Anwendung benachrichtigt wird, wenn der Mauszeiger den Client Bereich des Dialog Felds verlässt.


```
//g_hwndTrackingTT is a global HWND variable

case WM_INITDIALOG:

        InitCommonControls();
        g_hwndTrackingTT = CreateTrackingToolTip(IDC_BUTTON1, hDlg, L"");
        return TRUE;

case WM_MOUSELEAVE: // The mouse pointer has left our window. Deactivate the tooltip.
    
    SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)FALSE, (LPARAM)&g_toolItem);
    g_TrackingMouse = FALSE;
    return FALSE;

case WM_MOUSEMOVE:

    static int oldX, oldY;
    int newX, newY;

    if (!g_TrackingMouse)   // The mouse has just entered the window.
    {                       // Request notification when the mouse leaves.
    
        TRACKMOUSEEVENT tme = { sizeof(TRACKMOUSEEVENT) };
        tme.hwndTrack       = hDlg;
        tme.dwFlags         = TME_LEAVE;
        
        TrackMouseEvent(&tme);

        // Activate the tooltip.
        SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)TRUE, (LPARAM)&g_toolItem);
        
        g_TrackingMouse = TRUE;
    }

    newX = GET_X_LPARAM(lParam);
    newY = GET_Y_LPARAM(lParam);

    // Make sure the mouse has actually moved. The presence of the tooltip 
    // causes Windows to send the message continuously.
    
    if ((newX != oldX) || (newY != oldY))
    {
        oldX = newX;
        oldY = newY;
            
        // Update the text.
        WCHAR coords[12];
        swprintf_s(coords, ARRAYSIZE(coords), L"%d, %d", newX, newY);
        
        g_toolItem.lpszText = coords;
        SendMessage(g_hwndTrackingTT, TTM_SETTOOLINFO, 0, (LPARAM)&g_toolItem);

        // Position the tooltip. The coordinates are adjusted so that the tooltip does not overlap the mouse pointer.
        
        POINT pt = { newX, newY }; 
        ClientToScreen(hDlg, &pt);
        SendMessage(g_hwndTrackingTT, TTM_TRACKPOSITION, 0, (LPARAM)MAKELONG(pt.x + 10, pt.y - 20));
    }
    return FALSE;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Quick Infos](using-tooltip-contro.md)
</dt> </dl>

 

 





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
# <a name="how-to-implement-tracking-tooltips"></a><span data-ttu-id="cdf0b-104">Implementieren von Quick Infos für die Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="cdf0b-104">How to Implement Tracking Tooltips</span></span>

<span data-ttu-id="cdf0b-105">Die nach Verfolgungs Quick Infos bleiben sichtbar, bis Sie explizit von der Anwendung geschlossen werden, und können die Position auf dem Bildschirm dynamisch ändern.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-105">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="cdf0b-106">Sie werden von [Version 4,70](common-control-versions.md) und höher der allgemeinen Steuerelemente unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-106">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span>

<span data-ttu-id="cdf0b-107">Fügen Sie zum Erstellen einer nach Verfolgungs-QuickInfo das "ttf Track"- \_ Flag im **uFlags** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur ein, wenn Sie die [**TTM \_ AddTool**](ttm-addtool.md) -Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-107">To create a tracking tooltip, include the TTF\_TRACK flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when sending the [**TTM\_ADDTOOL**](ttm-addtool.md) message.</span></span>

<span data-ttu-id="cdf0b-108">Die Anwendung muss eine nach Verfolgungs-QuickInfo manuell aktivieren (anzeigen) und deaktivieren (ausblenden), indem eine [**TTM- \_ trackaktivierungs**](ttm-trackactivate.md) Meldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-108">Your application must manually activate (show) and deactivate (hide) a tracking tooltip by sending a [**TTM\_TRACKACTIVATE**](ttm-trackactivate.md) message.</span></span> <span data-ttu-id="cdf0b-109">Während eine nach Verfolgungs-QuickInfo aktiv ist, muss die Anwendung den Speicherort der QuickInfo angeben, indem [**TTM \_ trackposition**](ttm-trackposition.md) -Meldungen an das QuickInfo-Steuerelement gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-109">While a tracking tooltip is active, your application must specify the location of the tooltip by sending [**TTM\_TRACKPOSITION**](ttm-trackposition.md) messages to the tooltip control.</span></span> <span data-ttu-id="cdf0b-110">Da die Anwendung Aufgaben wie z. b. das Positionieren der QuickInfo behandelt, wird bei der Nachverfolgung von Quick Infos nicht das Steuer Flag " **ttf \_ subclass** " oder " [**TTM \_ relayevent**](ttm-relayevent.md) "</span><span class="sxs-lookup"><span data-stu-id="cdf0b-110">Because the application handles tasks such as positioning the tooltip, tracking tooltips do not use the **TTF\_SUBCLASS** flag or the [**TTM\_RELAYEVENT**](ttm-relayevent.md) message.</span></span>

<span data-ttu-id="cdf0b-111">Die [**TTM \_ trackposition**](ttm-trackposition.md) -Meldung bewirkt, dass das QuickInfo-Steuerelement das Fenster mit einem von zwei Platzierungs Stilen anzeigt:</span><span class="sxs-lookup"><span data-stu-id="cdf0b-111">The [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message causes the tooltip control to display the window using one of two placement styles:</span></span>

-   <span data-ttu-id="cdf0b-112">Standardmäßig wird die QuickInfo neben dem entsprechenden Tool an einer Position angezeigt, die das Steuerelement auswählt.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-112">By default, the tooltip is displayed next to the corresponding tool in a position that the control chooses.</span></span> <span data-ttu-id="cdf0b-113">Der ausgewählte Standort ist relativ zu den Koordinaten, die Sie mithilfe dieser Nachricht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-113">The location chosen is relative to the coordinates that you provide by using this message.</span></span>
-   <span data-ttu-id="cdf0b-114">Wenn Sie den **\_ absoluten** Wert von ttf in den Member der toolinfo-Struktur einschließen, wird die [**QuickInfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) an der in der Meldung angegebenen Pixelposition angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-114">If you include the **TTF\_ABSOLUTE** value in the member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, the tooltip is displayed at the pixel location specified in the message.</span></span> <span data-ttu-id="cdf0b-115">In diesem Fall versucht das Steuerelement nicht, den Speicherort des QuickInfo-Fensters von den von Ihnen bereitgestellten Koordinaten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-115">In this case, the control does not attempt to change the tooltip window's location from the coordinates you provide.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cdf0b-116">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="cdf0b-116">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cdf0b-117">Technologien</span><span class="sxs-lookup"><span data-stu-id="cdf0b-117">Technologies</span></span>

-   [<span data-ttu-id="cdf0b-118">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="cdf0b-118">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cdf0b-119">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="cdf0b-119">Prerequisites</span></span>

-   <span data-ttu-id="cdf0b-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="cdf0b-120">C/C++</span></span>
-   <span data-ttu-id="cdf0b-121">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="cdf0b-121">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cdf0b-122">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="cdf0b-122">Instructions</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="cdf0b-123">Implementieren von In-Place Quick Infos</span><span class="sxs-lookup"><span data-stu-id="cdf0b-123">Implement In-Place Tooltips</span></span>

<span data-ttu-id="cdf0b-124">Der **uFlags** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die im Beispiel verwendet wird, enthält das " **ttf \_ absolute** "-Flag.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-124">The **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that is used in the example includes the **TTF\_ABSOLUTE** flag.</span></span> <span data-ttu-id="cdf0b-125">Ohne dieses Flag wählt das QuickInfo-Steuerelement aus, wo die QuickInfo angezeigt werden soll, und seine Position relativ zum Dialogfeld kann sich plötzlich ändern, wenn der Mauszeiger bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-125">Without this flag, the tooltip control chooses where to display the tooltip, and its position relative to the dialog box may change suddenly as the mouse pointer moves.</span></span>

> [!Note]  
> <span data-ttu-id="cdf0b-126">`g_toolItem` ist eine globale [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-126">`g_toolItem` is a global [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

 

<span data-ttu-id="cdf0b-127">Im folgenden Beispiel wird veranschaulicht, wie ein ToolTip-Steuerelement für die Überwachung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-127">The following example demonstrates how to create a tracking tooltip control.</span></span> <span data-ttu-id="cdf0b-128">Im Beispiel wird der gesamte Client Bereich des Hauptfensters als Tool angegeben.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-128">The example specifies the main window's entire client area as the tool.</span></span>


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



### <a name="window-procedure-implementation"></a><span data-ttu-id="cdf0b-129">Implementierung der Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="cdf0b-129">Window Procedure Implementation</span></span>

<span data-ttu-id="cdf0b-130">Wenn sich der Mauszeiger im Client Bereich befindet, ist die QuickInfo aktiv und zeigt die Cursor Koordinaten an, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-130">When the mouse pointer is within the client area, the tooltip is active and displays the cursor coordinates, as shown in the following illustration.</span></span>

![Screenshot eines Dialog Felds in einer QuickInfo werden die x-und y-Koordinaten des Mauszeigers angezeigt.](images/tt-tracking.png)

<span data-ttu-id="cdf0b-132">Der folgende Beispielcode wird aus der Fenster Prozedur für ein Dialogfeld angezeigt, in dem die im vorherigen Beispiel erstellte nach Verfolgungs-QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-132">The following example code is from the window procedure for a dialog box that displays the tracking tooltip created in the preceding example.</span></span> <span data-ttu-id="cdf0b-133">Die globale boolesche Variable *g \_ trackingmouse* wird verwendet, um zu bestimmen, ob es erforderlich ist, die QuickInfo zu reaktivieren und die Maus Nachverfolgung zurückzusetzen, damit die Anwendung benachrichtigt wird, wenn der Mauszeiger den Client Bereich des Dialog Felds verlässt.</span><span class="sxs-lookup"><span data-stu-id="cdf0b-133">The global Boolean variable *g\_TrackingMouse* is used to determine whether it is necessary to reactivate the tooltip and reset mouse tracking so that the application is notified when the mouse pointer leaves the client area of the dialog box.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cdf0b-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cdf0b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdf0b-135">Verwenden von Quick Infos</span><span class="sxs-lookup"><span data-stu-id="cdf0b-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 





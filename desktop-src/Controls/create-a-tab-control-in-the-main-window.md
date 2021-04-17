---
title: Erstellen eines Registerkarten-Steuer Elements im Hauptfenster
description: Das Beispiel in diesem Abschnitt veranschaulicht, wie ein Registerkarten-Steuerelement erstellt und im Client Bereich des Hauptfensters der Anwendung angezeigt wird.
ms.assetid: 24157B8B-177B-471C-9DA0-548D09EA5F89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686a9a4fe4f6be95ccdcf3bbcb597c2c48ff3b2d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474365"
---
# <a name="how-to-create-a-tab-control-in-the-main-window"></a><span data-ttu-id="45a1b-103">Erstellen eines Registerkarten-Steuer Elements im Hauptfenster</span><span class="sxs-lookup"><span data-stu-id="45a1b-103">How to Create a Tab Control in the Main Window</span></span>

<span data-ttu-id="45a1b-104">Das Beispiel in diesem Abschnitt veranschaulicht, wie ein Registerkarten-Steuerelement erstellt und im Client Bereich des Hauptfensters der Anwendung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="45a1b-104">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="45a1b-105">Die Anwendung zeigt ein drittes Fenster (ein statisches Steuerelement) im Anzeigebereich des Registerkarten-Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="45a1b-105">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="45a1b-106">Das übergeordnete Fenster positioniert und passt das Registerkarten-Steuerelement und das statische Steuerelement, wenn es die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="45a1b-106">The parent window positions and sizes the tab control and static control when it processes the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

<span data-ttu-id="45a1b-107">In diesem Beispiel gibt es sieben Registerkarten, eine für jeden Tag der Woche.</span><span class="sxs-lookup"><span data-stu-id="45a1b-107">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="45a1b-108">Wenn der Benutzer eine Registerkarte auswählt, zeigt die Anwendung den Namen des entsprechenden Tags im statischen Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="45a1b-108">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="45a1b-109">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="45a1b-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="45a1b-110">Technologien</span><span class="sxs-lookup"><span data-stu-id="45a1b-110">Technologies</span></span>

-   [<span data-ttu-id="45a1b-111">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="45a1b-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="45a1b-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="45a1b-112">Prerequisites</span></span>

-   <span data-ttu-id="45a1b-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="45a1b-113">C/C++</span></span>
-   <span data-ttu-id="45a1b-114">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="45a1b-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="45a1b-115">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="45a1b-115">Instructions</span></span>

### <a name="create-a-tab-control-in-the-main-window"></a><span data-ttu-id="45a1b-116">Erstellen eines Registerkarten-Steuer Elements im Hauptfenster</span><span class="sxs-lookup"><span data-stu-id="45a1b-116">Create a Tab Control in the Main Window</span></span>

<span data-ttu-id="45a1b-117">Mit der folgenden Funktion wird das Registerkarten-Steuerelement erstellt und für jeden Wochentag eine Registerkarte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="45a1b-117">The following function creates the tab control and adds a tab for each day of the week.</span></span> <span data-ttu-id="45a1b-118">Die Namen der Tage werden als Zeichen folgen Ressourcen definiert, beginnend mit IDs \_ Sunday (definiert in der Ressourcen Header Datei der Anwendung).</span><span class="sxs-lookup"><span data-stu-id="45a1b-118">The names of the days are defined as string resources, consecutively numbered starting with IDS\_SUNDAY (defined in the application's resource header file).</span></span> <span data-ttu-id="45a1b-119">Sowohl das übergeordnete als auch das Registerkarten-Steuerelement müssen den Fenster Stil " [**WS \_ clipparent**](/windows/desktop/winmsg/window-styles) " aufweisen.</span><span class="sxs-lookup"><span data-stu-id="45a1b-119">Both the parent window and the tab control must have the [**WS\_CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles) window style.</span></span> <span data-ttu-id="45a1b-120">Die Initialisierungsfunktion der Anwendung ruft diese Funktion nach dem Erstellen des Hauptfensters auf.</span><span class="sxs-lookup"><span data-stu-id="45a1b-120">The application's initialization function calls this function after creating the main window.</span></span>


```C++
#define DAYS_IN_WEEK 7

// Creates a tab control, sized to fit the specified parent window's client
//   area, and adds some tabs. 
// Returns the handle to the tab control. 
// hwndParent - parent window (the application's main window). 
// 
HWND DoCreateTabControl(HWND hwndParent) 
{ 
    RECT rcClient; 
    INITCOMMONCONTROLSEX icex;
    HWND hwndTab; 
    TCITEM tie; 
    int i; 
    TCHAR achTemp[256];  // Temporary buffer for strings.
 
    // Initialize common controls.
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&icex);
    
    // Get the dimensions of the parent window's client area, and 
    // create a tab control child window of that size. Note that g_hInst
    // is the global instance handle.
    GetClientRect(hwndParent, &rcClient); 
    hwndTab = CreateWindow(WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, rcClient.right, rcClient.bottom, 
        hwndParent, NULL, g_hInst, NULL); 
    if (hwndTab == NULL)
    { 
        return NULL; 
    }
 
    // Add tabs for each day of the week. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = achTemp; 
 
    for (i = 0; i < DAYS_IN_WEEK; i++) 
    { 
        // Load the day string from the string resources. Note that
        // g_hInst is the global instance handle.
        LoadString(g_hInst, IDS_SUNDAY + i, 
                achTemp, sizeof(achTemp) / sizeof(achTemp[0])); 
        if (TabCtrl_InsertItem(hwndTab, i, &tie) == -1) 
        { 
            DestroyWindow(hwndTab); 
            return NULL; 
        } 
    } 
    return hwndTab; 
} 
```



<span data-ttu-id="45a1b-121">Die folgende Funktion erstellt das statische Steuerelement, das sich im Anzeigebereich des Registerkarten-Steuer Elements befindet.</span><span class="sxs-lookup"><span data-stu-id="45a1b-121">The following function creates the static control that resides in the tab control's display area.</span></span> <span data-ttu-id="45a1b-122">Die Initialisierungsfunktion der Anwendung ruft diese Funktion nach dem Erstellen des Hauptfensters und des Registerkarten-Steuer Elements auf.</span><span class="sxs-lookup"><span data-stu-id="45a1b-122">The application's initialization function calls this function after creating the main window and the tab control.</span></span>


```C++
// Creates a child window (a static control) to occupy the tab control's 
//   display area. 
// Returns the handle to the static control. 
// hwndTab - handle of the tab control. 
// 
HWND DoCreateDisplayWindow(HWND hwndTab) 
{ 
    HWND hwndStatic = CreateWindow(WC_STATIC, L"", 
        WS_CHILD | WS_VISIBLE | WS_BORDER, 
        100, 100, 100, 100,        // Position and dimensions; example only.
        hwndTab, NULL, g_hInst,    // g_hInst is the global instance handle
        NULL); 
    return hwndStatic; 
}
```



<span data-ttu-id="45a1b-123">Die folgenden Beispiel Funktionen werden aus der Fenster Prozedur der Anwendung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="45a1b-123">The following example functions are called from the application's window procedure.</span></span> <span data-ttu-id="45a1b-124">Die Anwendung ruft die- `OnSize` Funktion auf, wenn die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht verarbeitet und die Größe des Registerkarten-Steuer Elements an den Client Bereich des Hauptfensters angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="45a1b-124">The application calls the `OnSize` function when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to position and size the tab control to fit the main window's client area.</span></span>

<span data-ttu-id="45a1b-125">Wenn eine Registerkarte ausgewählt ist, sendet das Registerkarten-Steuerelement eine WM-Benachrichtigungs Meldung, die den [TCN \_ selChange](tcn-selchange.md) -Benachrichtigungs Code angibt. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="45a1b-125">When a tab is selected, the tab control sends a [**WM\_NOTIFY**](wm-notify.md) message, specifying the [TCN\_SELCHANGE](tcn-selchange.md) notification code.</span></span> <span data-ttu-id="45a1b-126">Die Funktion der Anwendung `OnNotify` verarbeitet diesen Benachrichtigungs Code, indem der Text des statischen Steuer Elements festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="45a1b-126">The application's `OnNotify` function processes this notification code by setting the text of the static control.</span></span>


```C++
// Handles the WM_SIZE message for the main window by resizing the 
//   tab control. 
// hwndTab - handle of the tab control.
// lParam - the lParam parameter of the WM_SIZE message.
//
HRESULT OnSize(HWND hwndTab, LPARAM lParam)
{
    RECT rc; 

    if (hwndTab == NULL)
        return E_INVALIDARG;

    // Resize the tab control to fit the client are of main window.
     if (!SetWindowPos(hwndTab, HWND_TOP, 0, 0, GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), SWP_SHOWWINDOW))
        return E_FAIL;

    return S_OK;
}

// Handles notifications from the tab control, as follows: 
//   TCN_SELCHANGING - always returns FALSE to allow the user to select a 
//     different tab.  
//   TCN_SELCHANGE - loads a string resource and displays it in a static 
//     control on the selected tab.
// hwndTab - handle of the tab control.
// hwndDisplay - handle of the static control. 
// lParam - the lParam parameter of the WM_NOTIFY message.
//
BOOL OnNotify(HWND hwndTab, HWND hwndDisplay, LPARAM lParam)
{
    TCHAR achTemp[256]; // temporary buffer for strings

    switch (((LPNMHDR)lParam)->code)
        {
            case TCN_SELCHANGING:
                {
                    // Return FALSE to allow the selection to change.
                    return FALSE;
                }

            case TCN_SELCHANGE:
                { 
                    int iPage = TabCtrl_GetCurSel(hwndTab); 

                    // Note that g_hInst is the global instance handle.
                    LoadString(g_hInst, IDS_SUNDAY + iPage, achTemp,
                        sizeof(achTemp) / sizeof(achTemp[0])); 
                    LRESULT result = SendMessage(hwndDisplay, WM_SETTEXT, 0,
                        (LPARAM) achTemp); 
                    break;
                } 
        }
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="45a1b-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45a1b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45a1b-128">Verwenden von Register Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="45a1b-128">Using Tab Controls</span></span>](using-tab-controls.md)
</dt> <dt>

<span data-ttu-id="45a1b-129">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="45a1b-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 
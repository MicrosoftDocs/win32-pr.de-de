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
# <a name="how-to-create-a-tab-control-in-the-main-window"></a>Erstellen eines Registerkarten-Steuer Elements im Hauptfenster

Das Beispiel in diesem Abschnitt veranschaulicht, wie ein Registerkarten-Steuerelement erstellt und im Client Bereich des Hauptfensters der Anwendung angezeigt wird. Die Anwendung zeigt ein drittes Fenster (ein statisches Steuerelement) im Anzeigebereich des Registerkarten-Steuer Elements an. Das übergeordnete Fenster positioniert und passt das Registerkarten-Steuerelement und das statische Steuerelement, wenn es die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht verarbeitet.

In diesem Beispiel gibt es sieben Registerkarten, eine für jeden Tag der Woche. Wenn der Benutzer eine Registerkarte auswählt, zeigt die Anwendung den Namen des entsprechenden Tags im statischen Steuerelement an.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-tab-control-in-the-main-window"></a>Erstellen eines Registerkarten-Steuer Elements im Hauptfenster

Mit der folgenden Funktion wird das Registerkarten-Steuerelement erstellt und für jeden Wochentag eine Registerkarte hinzugefügt. Die Namen der Tage werden als Zeichen folgen Ressourcen definiert, beginnend mit IDs \_ Sunday (definiert in der Ressourcen Header Datei der Anwendung). Sowohl das übergeordnete als auch das Registerkarten-Steuerelement müssen den Fenster Stil " [**WS \_ clipparent**](/windows/desktop/winmsg/window-styles) " aufweisen. Die Initialisierungsfunktion der Anwendung ruft diese Funktion nach dem Erstellen des Hauptfensters auf.


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



Die folgende Funktion erstellt das statische Steuerelement, das sich im Anzeigebereich des Registerkarten-Steuer Elements befindet. Die Initialisierungsfunktion der Anwendung ruft diese Funktion nach dem Erstellen des Hauptfensters und des Registerkarten-Steuer Elements auf.


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



Die folgenden Beispiel Funktionen werden aus der Fenster Prozedur der Anwendung aufgerufen. Die Anwendung ruft die- `OnSize` Funktion auf, wenn die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht verarbeitet und die Größe des Registerkarten-Steuer Elements an den Client Bereich des Hauptfensters angepasst wird.

Wenn eine Registerkarte ausgewählt ist, sendet das Registerkarten-Steuerelement eine WM-Benachrichtigungs Meldung, die den [TCN \_ selChange](tcn-selchange.md) -Benachrichtigungs Code angibt. [**\_**](wm-notify.md) Die Funktion der Anwendung `OnNotify` verarbeitet diesen Benachrichtigungs Code, indem der Text des statischen Steuer Elements festgelegt wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Register Steuerelementen](using-tab-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
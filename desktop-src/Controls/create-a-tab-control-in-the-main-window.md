---
title: Erstellen eines Registerkarten-Steuerelements im Hauptfenster
description: Im Beispiel in diesem Abschnitt wird veranschaulicht, wie Sie ein Registerkarten-Steuerelement erstellen und es im Clientbereich des Hauptfensters der Anwendung anzeigen.
ms.assetid: 24157B8B-177B-471C-9DA0-548D09EA5F89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b7d945b01c1e6409cf795d7f42f29999830ed1272bb661a9bb13e52cd1e293
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320010"
---
# <a name="how-to-create-a-tab-control-in-the-main-window"></a>Erstellen eines Registerkarten-Steuerelements im Hauptfenster

Im Beispiel in diesem Abschnitt wird veranschaulicht, wie Sie ein Registerkarten-Steuerelement erstellen und es im Clientbereich des Hauptfensters der Anwendung anzeigen. Die Anwendung zeigt ein drittes Fenster (ein statisches Steuerelement) im Anzeigebereich des Registerkarten-Steuerelements an. Das übergeordnete Fenster positioniert und singt das Registerkarten-Steuerelement und das statische Steuerelement, wenn es die [**WM \_ SIZE-Meldung**](/windows/desktop/winmsg/wm-size) verarbeitet.

In diesem Beispiel gibt es sieben Registerkarten, eine für jeden Tag der Woche. Wenn der Benutzer eine Registerkarte auswählt, zeigt die Anwendung den Namen des entsprechenden Tages im statischen Steuerelement an.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-tab-control-in-the-main-window"></a>Erstellen eines Registerkarten-Steuerelements im Hauptfenster

Die folgende Funktion erstellt das Registerkarten-Steuerelement und fügt eine Registerkarte für jeden Wochentag hinzu. Die Namen der Tage werden als Zeichenfolgenressourcen definiert, beginnend mit IDS SUNDAY (definiert in der Ressourcenheaderdatei \_ der Anwendung). Sowohl das übergeordnete Fenster als auch das Registerkarten-Steuerelement müssen das [**Fensterformat WS \_ CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles) haben. Die Initialisierungsfunktion der Anwendung ruft diese Funktion nach dem Erstellen des Hauptfensters auf.


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



Die folgende Funktion erstellt das statische Steuerelement, das sich im Anzeigebereich des Registerkarten-Steuerelements befindet. Die Initialisierungsfunktion der Anwendung ruft diese Funktion auf, nachdem das Hauptfenster und das Registerkarten-Steuerelement erstellt wurden.


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



Die folgenden Beispielfunktionen werden über die Fensterprozedur der Anwendung aufgerufen. Die Anwendung ruft die -Funktion auf, wenn die WM SIZE-Nachricht verarbeitet wird, um das Registerkarten-Steuerelement so zu positionieren und zu formatieren, dass es dem Clientbereich `OnSize` des Hauptfensters [**\_**](/windows/desktop/winmsg/wm-size) passt.

Wenn eine Registerkarte ausgewählt ist, sendet das Registerkarten-Steuerelement eine [**WM \_ NOTIFY-Nachricht**](wm-notify.md) und gibt den [TCN \_ SELCHANGE-Benachrichtigungscode](tcn-selchange.md) an. Die -Funktion der `OnNotify` Anwendung verarbeitet diesen Benachrichtigungscode durch Festlegen des Texts des statischen Steuerelements.


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

[Verwenden von Registerkartensteuerelementen](using-tab-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
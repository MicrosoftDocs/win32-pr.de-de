---
title: Unterstufen eines Kombinationsfelds
description: In diesem Thema wird veranschaulicht, wie Kombinationsfelder untergliedert werden.
ms.assetid: 9897EA94-1BF7-4711-AED6-5E9C863C287A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea674cfecf3c84ce4a1fa2abb1f23f8f208a8b8fd220736bbcec61bea7880b34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078444"
---
# <a name="how-to-subclass-a-combo-box"></a>Unterstufen eines Kombinationsfelds

In diesem Thema wird veranschaulicht, wie Kombinationsfelder untergliedert werden. Die C++-Beispielanwendung erstellt ein Symbolleistenfenster, das zwei Kombinationsfelder enthält. Durch Unterklassen der Bearbeitungssteuerelemente in den Kombinationsfeldern fängt das Symbolleistenfenster TAB-, EINGABE- und ESC-Schlüssel ab, die andernfalls ignoriert würden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="process-the-wm_create-message"></a>Verarbeiten der WM \_ CREATE-Nachricht

Die Anwendung verarbeitet die [**WM \_ CREATE-Nachricht,**](/windows/desktop/winmsg/wm-create) um zwei Kombinationsfeldsteuerelemente als untergeordnete Fenster zu erstellen.


```C++
//  Create two combo box child windows. 
dwBaseUnits = GetDialogBaseUnits(); 
 
hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (6 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, NULL, NULL);  
 
hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (112 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, hInst, NULL); 
```



Die Anwendung untergliedert dann die Bearbeitungssteuerelemente (Auswahlfelder) in jedem Kombinationsfeld, da sie die Zeicheneingabe für einfache und Dropdown-Kombinationsfelder erhalten. Schließlich wird die [**ChildWindowFromPoint-Funktion**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) aufgerufen, um das Handle für jedes Bearbeitungssteuerelement abzurufen.

Um die Bearbeitungssteuerelemente zu untergliedern, ruft die Anwendung die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) auf und ersetzt den Zeiger auf die Klassenfensterprozedur durch einen Zeiger auf die anwendungsdefinierte **SubClassProc-Funktion.** Der Zeiger auf die ursprüngliche Fensterprozedur wird in der globalen Variablen *lpfnEditWndProc* gespeichert.

**SubClassProc** fängt TAB-, EINGABE- und ESC-Schlüssel ab und benachrichtigt das Symbolleistenfenster durch Senden von anwendungsdefinierten Nachrichten (WM \_ TAB, WM \_ ESC und WM \_ ENTER). **SubClassProc** verwendet die [**CallWindowProc-Funktion,**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) um die meisten Nachrichten an die ursprüngliche Fensterprozedur *lpfnEditWndProc* zu übergeben.


```C++
//  Get the edit window handle to each combo box. 
pt.x = 1; 
pt.y = 1; 
hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
//  Change the window procedure for both edit windows 
//  to the subclass procedure. 
lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
    GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
```



### <a name="process-the-wm_setfocus-message"></a>Verarbeiten der WM \_ SETFOCUS-Nachricht

Wenn das Symbolleistenfenster den Eingabefokus erhält, wird der Fokus sofort auf das erste Kombinationsfeld in der Symbolleiste festgelegt. Zu diesem Zweck ruft das Beispiel die [**SetFocus-Funktion**](/windows/desktop/api/winuser/nf-winuser-setfocus) als Reaktion auf die [**WM \_ SETFOCUS-Nachricht**](/windows/desktop/inputdev/wm-setfocus) auf.


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a>Verarbeiten Application-Defined Nachrichten

Die **SubClassProc-Funktion** sendet anwendungsdefinierte Nachrichten an das Symbolleistenfenster, wenn der Benutzer die TAB-, EINGABE- oder ESC-TASTE in einem Kombinationsfeld drückt. Die **\_ WM-TAB-Nachricht** wird für die TAB-TASTE, die **WM \_ ESC-Nachricht** für die ESC-Taste und die **\_ WM-EINGABE-Meldung** für die EINGABETASTE gesendet.

Im Beispiel wird die **\_ WM-TAB-Meldung** verarbeitet, indem der Fokus auf das nächste Kombinationsfeld in der Symbolleiste festgelegt wird. Die **WM \_ ESC-Nachricht** wird verarbeitet, indem der Fokus auf das Hauptanwendungsfenster festgelegt wird.


```C++
  case WM_TAB: 
      if (GetFocus() == hwndEdit1) 
          SetFocus(hwndCombo2); 
      else 
          SetFocus(hwndCombo1); 
      break; 
 
  case WM_ESC: 
       hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
       // Clear the current selection. 
       SendMessage(hwndCombo, CB_SETCURSEL, 
          (WPARAM) (-1), 0); 
 
      //  Set the focus to the main window. 
      SetFocus(hwndMain); 
      break;
```



Als Reaktion auf die **\_ WM-EINGABEMELDUNG** stellt das Beispiel sicher, dass die aktuelle Auswahl für das Kombinationsfeld gültig ist, und legt dann den Fokus auf das Hauptanwendungsfenster fest. Wenn das Kombinationsfeld keine aktuelle Auswahl enthält, wird im Beispiel die [**CB \_ FINDSTRINGEXACT-Nachricht**](cb-findstringexact.md) verwendet, um nach einem Listenelement zu suchen, das dem Inhalt des Auswahlfelds entspricht. Wenn eine Übereinstimmung vorhanden ist, wird im Beispiel die aktuelle Auswahl festgelegt. Andernfalls wird ein neues Listenelement hinzugefügt.


```C++
case WM_ENTER: 
    hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
    SetFocus(hwndMain); 
 
    //  If there is no current selection, set one. 
    if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
            == CB_ERR) 
    { 
        if (SendMessage(hwndCombo, WM_GETTEXT, 
                sizeof(achTemp), (LPARAM) achTemp) == 0) 
            break;      //  Empty selection field 
        dwIndex = SendMessage(hwndCombo, 
            CB_FINDSTRINGEXACT, (WPARAM) (-1), 
            (LPARAM) achTemp); 
 
        //  Add the string, if necessary, and select it. 
        if (dwIndex == CB_ERR) 
            dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                0, (LPARAM) achTemp); 
        if (dwIndex != CB_ERR) 
            SendMessage(hwndCombo, CB_SETCURSEL, 
                dwIndex, 0); 
    } 
    break; 
       
    // . 
    // .  Process additional messages. 
    // . 
 
default: 
    return DefWindowProc(hwnd, msg, wParam, lParam); 
```



## <a name="complete-example"></a>Vollständiges Beispiel

Im Folgenden sind die Fensterprozedur für die Symbolleiste und die Unterklassenprozedur für die beiden Kombinationsfelder aufgeführt.


```C++
#define WM_TAB (WM_USER) 
#define WM_ESC (WM_USER + 1) 
#define WM_ENTER (WM_USER + 2) 

//  Global variables
HWND    hwndMain; 
WNDPROC lpfnEditWndProc; //  Original wndproc for the combo box 

//  Prototypes
LRESULT CALLBACK SubClassProc( HWND, UINT, WPARAM, LPARAM );
 
/******************************************************** 
 
    FUNCTION:   ToolbarWindowProc 
 
    PURPOSE:    Window procedure for the toolbar window 
 
*********************************************************/ 
 
LRESULT CALLBACK ToolbarWindowProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    static HWND   hwndEdit1; 
    static HWND   hwndEdit2; 
    static HWND   hwndCombo1; 
    static HWND   hwndCombo2; 
    POINT       pt; 
    DWORD       dwBaseUnits; 
    HWND        hwndCombo; 
    DWORD       dwIndex; 
    char achTemp[256];       //  Temporary buffer 
 
    switch (msg) 
    { 
        case WM_CREATE: 
            //  Create two combo box child windows. 
            dwBaseUnits = GetDialogBaseUnits(); 
 
            hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (6 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, NULL, NULL);  
 
            hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (112 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, hInst, NULL); 
            
            //  Get the edit window handle to each combo box. 
            pt.x = 1; 
            pt.y = 1; 
            hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
            hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
            //  Change the window procedure for both edit windows 
            //  to the subclass procedure. 
            lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
                GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
            SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 

            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndCombo1); 
            break; 

        case WM_TAB: 
            if (GetFocus() == hwndEdit1) 
                SetFocus(hwndCombo2); 
            else 
                SetFocus(hwndCombo1); 
            break; 
 
        case WM_ESC: 
             hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
             // Clear the current selection. 
             SendMessage(hwndCombo, CB_SETCURSEL, 
                (WPARAM) (-1), 0); 
 
            //  Set the focus to the main window. 
            SetFocus(hwndMain); 
            break;

        case WM_ENTER: 
            hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
            SetFocus(hwndMain); 
 
            //  If there is no current selection, set one. 
            if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
                    == CB_ERR) 
            { 
                if (SendMessage(hwndCombo, WM_GETTEXT, 
                        sizeof(achTemp), (LPARAM) achTemp) == 0) 
                    break;      //  Empty selection field 
                dwIndex = SendMessage(hwndCombo, 
                    CB_FINDSTRINGEXACT, (WPARAM) (-1), 
                    (LPARAM) achTemp); 
 
                //  Add the string, if necessary, and select it. 
                if (dwIndex == CB_ERR) 
                    dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                        0, (LPARAM) achTemp); 
                if (dwIndex != CB_ERR) 
                    SendMessage(hwndCombo, CB_SETCURSEL, 
                        dwIndex, 0); 
            } 
            break; 
       
            // . 
            // .  Process additional messages. 
            // . 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
/******************************************************** 
 
    FUNCTION:   SubClassProc 
 
    PURPOSE:    Process TAB and ESCAPE keys, and pass all 
                other messages to the class window 
                procedure. 
 
*********************************************************/ 
LRESULT CALLBACK SubClassProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (msg) 
    { 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_TAB: 
                    SendMessage(hwndMain, WM_TAB, 0, 0); 
                    return 0; 
                case VK_ESCAPE: 
                    SendMessage(hwndMain, WM_ESC, 0, 0); 
                    return 0; 
                case VK_RETURN: 
                    SendMessage(hwndMain, WM_ENTER, 0, 0); 
                    return 0; 
            } 
            break; 
 
        case WM_KEYUP: 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case VK_TAB: 
                case VK_ESCAPE: 
                case VK_RETURN: 
                    return 0; 
            } 
    } 
 
    //  Call the original window procedure for default processing. 
     return CallWindowProc(lpfnEditWndProc, hwnd, msg, wParam, lParam); 
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Kombinationsfeldern](about-combo-boxes.md)
</dt> <dt>

[ComboBox-Steuerelementreferenz](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[Verwenden von Kombinationsfeldern](using-combo-boxes.md)
</dt> <dt>

[ComboBox](combo-boxes.md)
</dt> </dl>

 

 
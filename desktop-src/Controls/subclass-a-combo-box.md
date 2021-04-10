---
title: Vorgehensweise bei der Unterklasse eines Kombinations Felds
description: In diesem Thema wird die Unterklasse von Kombinations Feldern veranschaulicht.
ms.assetid: 9897EA94-1BF7-4711-AED6-5E9C863C287A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b48301309597c53f02ca87d1d1748ab1fe05139
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039707"
---
# <a name="how-to-subclass-a-combo-box"></a>Vorgehensweise bei der Unterklasse eines Kombinations Felds

In diesem Thema wird die Unterklasse von Kombinations Feldern veranschaulicht. Die C++-Beispielanwendung erstellt ein Symbolleisten Fenster, das zwei Kombinations Felder enthält. Durch die Unterklassen der Bearbeitungs Steuerelemente innerhalb der Kombinations Felder fängt das Symbolleisten Fenster die Tab-Taste, die EINGABETASTE und die ESC-Taste ab, die andernfalls ignoriert werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="process-the-wm_create-message"></a>Verarbeiten der "WM Create"- \_ Nachricht

Die Anwendung verarbeitet die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht, um zwei Kombinations Feld-Steuerelemente als untergeordnete Fenster zu erstellen.


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



Die Anwendung unterteilt dann die Bearbeitungs Steuerelemente (Auswahlfelder) in jedem Kombinations Feld, da Sie die Zeicheneingabe für einfaches und Dropdown-Kombinations Feld erhalten. Zum Schluss ruft Sie die [**childwindowfrompoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) -Funktion auf, um das Handle für jedes Bearbeitungs Steuerelement abzurufen.

Um die Bearbeitungs Steuerelemente zu unterteilen, ruft die Anwendung die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion auf und ersetzt den Zeiger auf die Klassen Fenster Prozedur durch einen Zeiger auf die Anwendungs definierte **subclassproc** -Funktion. Der Zeiger auf die ursprüngliche Fenster Prozedur wird in der globalen Variablen *lpfnditwndproc* gespeichert.

**Subclassproc** fängt die Tab-Taste, die EINGABETASTE und die ESC-Taste ein und benachrichtigt das Symbolleisten Fenster, indem Anwendungs definierte Meldungen ( \_ Registerkarte WM, WM \_ ESC und WM \_ Enter) gesendet werden. **Subclassproc** verwendet die [**callwindowproc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) -Funktion, um die meisten Nachrichten an die ursprüngliche Fenster Prozedur *lpfnditwndproc* zu übergeben.


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



### <a name="process-the-wm_setfocus-message"></a>Verarbeiten der WM- \_ SetFocus-Nachricht

Wenn das Symbolleisten Fenster den Eingabefokus erhält, wird der Fokus sofort auf das erste Kombinations Feld auf der Symbolleiste festgelegt. Zu diesem Zweck wird im Beispiel die [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion als Reaktion auf die [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) -Nachricht aufgerufen.


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a>Verarbeiten von Application-Defined Meldungen

Die **subclassproc** -Funktion sendet Anwendungs definierte Meldungen an das Symbolleisten Fenster, wenn der Benutzer die Tab-Taste, die EINGABETASTE oder die ESC-Taste in einem Kombinations Feld drückt. Die **\_ Registerkarte "WM** " wird für die Tab-Taste, die **WM- \_ ESC** -Nachricht für die ESC-Taste und die **WM- \_ Eingabe** Nachricht für die EINGABETASTE gesendet.

Im Beispiel wird die **WM- \_ Register** Karten Nachricht verarbeitet, indem der Fokus auf das nächste Kombinations Feld auf der Symbolleiste festgelegt wird. Die WM- **\_ ESC** -Nachricht wird verarbeitet, indem der Fokus auf das Hauptanwendungsfenster festgelegt wird.


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



Als Antwort auf die **WM \_ Enter** -Nachricht stellt das Beispiel sicher, dass die aktuelle Auswahl für das Kombinations Feld gültig ist, und legt dann den Fokus auf das Hauptanwendungsfenster fest. Wenn das Kombinations Feld keine aktuelle Auswahl enthält, wird im Beispiel die [**CB \_ FindStringExact**](cb-findstringexact.md) -Nachricht verwendet, um nach einem Listenelement zu suchen, das mit dem Inhalt des Auswahl Felds übereinstimmt. Wenn eine Entsprechung vorhanden ist, wird im Beispiel die aktuelle Auswahl festgelegt. Andernfalls wird ein neues Listenelement hinzugefügt.


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

Im folgenden finden Sie die Fenster Prozedur für die Symbolleiste und die Unterklassen Prozedur für die beiden Kombinations Felder.


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

[Informationen zu Kombinations Feldern](about-combo-boxes.md)
</dt> <dt>

[Referenz für ComboBox-Steuerelement](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[Verwenden von Kombinations Feldern](using-combo-boxes.md)
</dt> <dt>

[ComboBox](combo-boxes.md)
</dt> </dl>

 

 
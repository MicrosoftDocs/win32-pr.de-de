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
# <a name="how-to-subclass-a-combo-box"></a><span data-ttu-id="65ea2-103">Vorgehensweise bei der Unterklasse eines Kombinations Felds</span><span class="sxs-lookup"><span data-stu-id="65ea2-103">How to Subclass a Combo Box</span></span>

<span data-ttu-id="65ea2-104">In diesem Thema wird die Unterklasse von Kombinations Feldern veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="65ea2-104">This topic demonstrates how to subclass combo boxes.</span></span> <span data-ttu-id="65ea2-105">Die C++-Beispielanwendung erstellt ein Symbolleisten Fenster, das zwei Kombinations Felder enthält.</span><span class="sxs-lookup"><span data-stu-id="65ea2-105">The C++ example application creates a toolbar window that contains two combo boxes.</span></span> <span data-ttu-id="65ea2-106">Durch die Unterklassen der Bearbeitungs Steuerelemente innerhalb der Kombinations Felder fängt das Symbolleisten Fenster die Tab-Taste, die EINGABETASTE und die ESC-Taste ab, die andernfalls ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="65ea2-106">By subclassing the edit controls within the combo boxes, the toolbar window intercepts TAB, ENTER, and ESC keys that would otherwise be ignored.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="65ea2-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="65ea2-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="65ea2-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="65ea2-108">Technologies</span></span>

-   [<span data-ttu-id="65ea2-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="65ea2-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="65ea2-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="65ea2-110">Prerequisites</span></span>

-   <span data-ttu-id="65ea2-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="65ea2-111">C/C++</span></span>
-   <span data-ttu-id="65ea2-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="65ea2-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="65ea2-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="65ea2-113">Instructions</span></span>

### <a name="process-the-wm_create-message"></a><span data-ttu-id="65ea2-114">Verarbeiten der "WM Create"- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="65ea2-114">Process the WM\_CREATE Message</span></span>

<span data-ttu-id="65ea2-115">Die Anwendung verarbeitet die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht, um zwei Kombinations Feld-Steuerelemente als untergeordnete Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="65ea2-115">The application processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to create two combo box controls as child windows.</span></span>


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



<span data-ttu-id="65ea2-116">Die Anwendung unterteilt dann die Bearbeitungs Steuerelemente (Auswahlfelder) in jedem Kombinations Feld, da Sie die Zeicheneingabe für einfaches und Dropdown-Kombinations Feld erhalten.</span><span class="sxs-lookup"><span data-stu-id="65ea2-116">The application then subclasses the edit controls (selection fields) in each combo box, because they receive the character input for simple and drop-down combo box.</span></span> <span data-ttu-id="65ea2-117">Zum Schluss ruft Sie die [**childwindowfrompoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) -Funktion auf, um das Handle für jedes Bearbeitungs Steuerelement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="65ea2-117">Finally, it calls the [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) function to retrieve the handle to each edit control.</span></span>

<span data-ttu-id="65ea2-118">Um die Bearbeitungs Steuerelemente zu unterteilen, ruft die Anwendung die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion auf und ersetzt den Zeiger auf die Klassen Fenster Prozedur durch einen Zeiger auf die Anwendungs definierte **subclassproc** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="65ea2-118">To subclass the edit controls, the application calls the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function, replacing the pointer to the class window procedure with a pointer to the application-defined **SubClassProc** function.</span></span> <span data-ttu-id="65ea2-119">Der Zeiger auf die ursprüngliche Fenster Prozedur wird in der globalen Variablen *lpfnditwndproc* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="65ea2-119">The pointer to the original window procedure is saved in the global variable *lpfnEditWndProc*.</span></span>

<span data-ttu-id="65ea2-120">**Subclassproc** fängt die Tab-Taste, die EINGABETASTE und die ESC-Taste ein und benachrichtigt das Symbolleisten Fenster, indem Anwendungs definierte Meldungen ( \_ Registerkarte WM, WM \_ ESC und WM \_ Enter) gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="65ea2-120">**SubClassProc** intercepts TAB, ENTER, and ESC keys and notifies the toolbar window by sending application-defined messages (WM\_TAB, WM\_ESC, and WM\_ENTER).</span></span> <span data-ttu-id="65ea2-121">**Subclassproc** verwendet die [**callwindowproc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) -Funktion, um die meisten Nachrichten an die ursprüngliche Fenster Prozedur *lpfnditwndproc* zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="65ea2-121">**SubClassProc** uses the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function to pass most messages to the original window procedure, *lpfnEditWndProc*.</span></span>


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



### <a name="process-the-wm_setfocus-message"></a><span data-ttu-id="65ea2-122">Verarbeiten der WM- \_ SetFocus-Nachricht</span><span class="sxs-lookup"><span data-stu-id="65ea2-122">Process the WM\_SETFOCUS Message</span></span>

<span data-ttu-id="65ea2-123">Wenn das Symbolleisten Fenster den Eingabefokus erhält, wird der Fokus sofort auf das erste Kombinations Feld auf der Symbolleiste festgelegt.</span><span class="sxs-lookup"><span data-stu-id="65ea2-123">When the toolbar window receives the input focus, it immediately sets the focus to the first combo box in the toolbar.</span></span> <span data-ttu-id="65ea2-124">Zu diesem Zweck wird im Beispiel die [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion als Reaktion auf die [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) -Nachricht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="65ea2-124">To do this, the example calls the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function in response to the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span>


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a><span data-ttu-id="65ea2-125">Verarbeiten von Application-Defined Meldungen</span><span class="sxs-lookup"><span data-stu-id="65ea2-125">Process Application-Defined Messages</span></span>

<span data-ttu-id="65ea2-126">Die **subclassproc** -Funktion sendet Anwendungs definierte Meldungen an das Symbolleisten Fenster, wenn der Benutzer die Tab-Taste, die EINGABETASTE oder die ESC-Taste in einem Kombinations Feld drückt.</span><span class="sxs-lookup"><span data-stu-id="65ea2-126">The **SubClassProc** function sends application-defined messages to the toolbar window when the user presses the TAB, ENTER, or ESC key in a combo box.</span></span> <span data-ttu-id="65ea2-127">Die **\_ Registerkarte "WM** " wird für die Tab-Taste, die **WM- \_ ESC** -Nachricht für die ESC-Taste und die **WM- \_ Eingabe** Nachricht für die EINGABETASTE gesendet.</span><span class="sxs-lookup"><span data-stu-id="65ea2-127">The **WM\_TAB** message is sent for the TAB key, the **WM\_ESC** message for the ESC key, and the **WM\_ENTER** message for the ENTER key.</span></span>

<span data-ttu-id="65ea2-128">Im Beispiel wird die **WM- \_ Register** Karten Nachricht verarbeitet, indem der Fokus auf das nächste Kombinations Feld auf der Symbolleiste festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="65ea2-128">The example processes the **WM\_TAB** message by setting the focus to the next combo box in the toolbar.</span></span> <span data-ttu-id="65ea2-129">Die WM- **\_ ESC** -Nachricht wird verarbeitet, indem der Fokus auf das Hauptanwendungsfenster festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="65ea2-129">It processes the **WM\_ESC** message by setting the focus to the main application window.</span></span>


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



<span data-ttu-id="65ea2-130">Als Antwort auf die **WM \_ Enter** -Nachricht stellt das Beispiel sicher, dass die aktuelle Auswahl für das Kombinations Feld gültig ist, und legt dann den Fokus auf das Hauptanwendungsfenster fest.</span><span class="sxs-lookup"><span data-stu-id="65ea2-130">In response to the **WM\_ENTER** message, the example ensures that the current selection for the combo box is valid and then sets the focus to the main application window.</span></span> <span data-ttu-id="65ea2-131">Wenn das Kombinations Feld keine aktuelle Auswahl enthält, wird im Beispiel die [**CB \_ FindStringExact**](cb-findstringexact.md) -Nachricht verwendet, um nach einem Listenelement zu suchen, das mit dem Inhalt des Auswahl Felds übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="65ea2-131">If the combo box contains no current selection, the example uses the [**CB\_FINDSTRINGEXACT**](cb-findstringexact.md) message to search for a list item that matches the contents of the selection field.</span></span> <span data-ttu-id="65ea2-132">Wenn eine Entsprechung vorhanden ist, wird im Beispiel die aktuelle Auswahl festgelegt. Andernfalls wird ein neues Listenelement hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="65ea2-132">If there is a match, the example sets the current selection; otherwise, it adds a new list item.</span></span>


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



## <a name="complete-example"></a><span data-ttu-id="65ea2-133">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="65ea2-133">Complete example</span></span>

<span data-ttu-id="65ea2-134">Im folgenden finden Sie die Fenster Prozedur für die Symbolleiste und die Unterklassen Prozedur für die beiden Kombinations Felder.</span><span class="sxs-lookup"><span data-stu-id="65ea2-134">Following are the window procedure for the toolbar and the subclass procedure for the two combo boxes.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="65ea2-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="65ea2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65ea2-136">Informationen zu Kombinations Feldern</span><span class="sxs-lookup"><span data-stu-id="65ea2-136">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="65ea2-137">Referenz für ComboBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="65ea2-137">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="65ea2-138">Verwenden von Kombinations Feldern</span><span class="sxs-lookup"><span data-stu-id="65ea2-138">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="65ea2-139">ComboBox</span><span class="sxs-lookup"><span data-stu-id="65ea2-139">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 
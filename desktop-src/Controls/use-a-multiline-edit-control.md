---
title: Erstellen eines mehrzeiligen Bearbeitungssteuerelements
description: In diesem Thema wird veranschaulicht, wie ein einfacher Textprozessor implementiert wird, indem dem Clientbereich eines Fensters ein mehrzeiliges Bearbeitungssteuerelement hinzugefügt wird.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11100d4d6f82c7a352d4ddacaa7fc05694b4d54125febc766a6d3f1c68376e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829071"
---
# <a name="how-to-create-a-multiline-edit-control"></a>Erstellen eines mehrzeiligen Bearbeitungssteuerelements

In diesem Thema wird veranschaulicht, wie ein einfacher Textprozessor implementiert wird, indem dem Clientbereich eines Fensters ein mehrzeiliges Bearbeitungssteuerelement hinzugefügt wird. Mithilfe des mehrzeiligen Bearbeitungssteuerelements kann der Benutzer In einem Menü Befehle bearbeiten auswählen. Mit diesen Befehlen kann der Benutzer einfache Bearbeitungsvorgänge ausführen, z. B. vorherige Aktionen rückgängig machen, Auswahlen in die Zwischenablage ausschneiden oder kopieren, Text aus der Zwischenablage einfügen und die aktuelle Auswahl löschen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Ihre Anwendung muss Code enthalten, um eine Instanz von zu erstellen, ein mehrzeiliges Bearbeitungssteuerelement zu initialisieren und dann Benutzerbearbeitungsbefehle zu verarbeiten.

Im folgenden C++-Codebeispiel wird ein Großteil der Funktionalität eines einfachen Textprozessors implementiert, indem dem Clientbereich eines Fensters ein mehrzeiliges Bearbeitungssteuerelement hinzugefügt wird. Das System führt automatisch Wordwrap-Vorgänge für das Bearbeitungssteuerelement aus und verarbeitet auch die Verarbeitung für die vertikale Scrollleiste (erstellt durch Angabe von [**ES \_ AUTOVSCROLL**](edit-control-styles.md) im Aufruf der [**CreateWindow-Funktion).**](/windows/desktop/api/winuser/nf-winuser-createwindowa)

Benutzerbearbeitungsbefehle werden über [**WM \_ COMMAND-Benachrichtigungsmeldungen**](/windows/desktop/menurc/wm-command) an den Fensterprozess gesendet.

> [!Note]  
> Wenn das Fenster das Windows Menüband enthält, muss die Größe des Bearbeitungssteuerelements angepasst werden, um die Höhe des Menübands aufzunehmen. Weitere Informationen finden Sie unter [Windows Menübandframework.](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry)

 



```C++
#define ID_EDITCHILD 100
 
LRESULT CALLBACK MainWndProc(HWND hwnd,      // window handle 
                             UINT message,   // type of message 
                             WPARAM wParam,  // additional information 
                             LPARAM lParam)  // additional information 
{ 
    static HWND hwndEdit; 
 
    TCHAR lpszLatin[] =  L"Lorem ipsum dolor sit amet, consectetur "
                         L"adipisicing elit, sed do eiusmod tempor " 
                         L"incididunt ut labore et dolore magna " 
                         L"aliqua. Ut enim ad minim veniam, quis " 
                         L"nostrud exercitation ullamco laboris nisi " 
                         L"ut aliquip ex ea commodo consequat. Duis " 
                         L"aute irure dolor in reprehenderit in " 
                         L"voluptate velit esse cillum dolore eu " 
                         L"fugiat nulla pariatur. Excepteur sint " 
                         L"occaecat cupidatat non proident, sunt " 
                         L"in culpa qui officia deserunt mollit " 
                         L"anim id est laborum."; 
 
    switch (message) 
    { 
        case WM_CREATE: 
            hwndEdit = CreateWindowEx(
                                0, L"EDIT",   // predefined class 
                                NULL,         // no window title 
                                WS_CHILD | WS_VISIBLE | WS_VSCROLL | 
                                ES_LEFT | ES_MULTILINE | ES_AUTOVSCROLL, 
                                0, 0, 0, 0,   // set size in WM_SIZE message 
                                hwnd,         // parent window 
                                (HMENU) ID_EDITCHILD,   // edit control ID 
                                (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE), 
                                NULL);        // pointer not needed 
 
            // Add text to the window. 
            SendMessage(hwndEdit, WM_SETTEXT, 0, (LPARAM) lpszLatin); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (wParam) 
            { 
                case IDM_EDUNDO: 
                    // Send WM_UNDO only if there is something to be undone. 
 
                    if (SendMessage(hwndEdit, EM_CANUNDO, 0, 0)) 
                        SendMessage(hwndEdit, WM_UNDO, 0, 0); 
                    else 
                    {
                        MessageBox(hwndEdit, 
                                   L"Nothing to undo.", 
                                   L"Undo notification", 
                                   MB_OK); 
                    }
                    break; 
 
                case IDM_EDCUT: 
                    SendMessage(hwndEdit, WM_CUT, 0, 0); 
                    break; 
 
                case IDM_EDCOPY: 
                    SendMessage(hwndEdit, WM_COPY, 0, 0); 
                    break; 
 
                case IDM_EDPASTE: 
                    SendMessage(hwndEdit, WM_PASTE, 0, 0); 
                    break; 
 
                case IDM_EDDEL: 
                    SendMessage(hwndEdit, WM_CLEAR, 0, 0); 
                    break; 

                case IDM_ABOUT: 
                    DialogBox(hInst,                // current instance 
                              L"AboutBox",           // resource to use 
                              hwnd,                 // parent handle 
                              (DLGPROC) About); 
                    break; 

                default: 
                    return DefWindowProc(hwnd, message, wParam, lParam); 
            } 
            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndEdit); 
            return 0; 

        case WM_SIZE: 
            // Make the edit control the size of the window's client area. 

            MoveWindow(hwndEdit, 
                       0, 0,                  // starting x- and y-coordinates 
                       LOWORD(lParam),        // width of client area 
                       HIWORD(lParam),        // height of client area 
                       TRUE);                 // repaint window 
            return 0; 

        case WM_DESTROY: 
            PostQuitMessage(0); 
            return 0; 

        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Bearbeiten von Steuerelementen](about-edit-controls.md)
</dt> <dt>

[Steuerelementverweis bearbeiten](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Verwenden von Bearbeitungssteuerelementen](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Steuerelement bearbeiten](edit-controls.md)
</dt> </dl>

 

 
---
title: Erstellen eines Header Steuer Elements
description: In diesem Thema wird veranschaulicht, wie ein Header Steuerelement erstellt und im Client Bereich des übergeordneten Fensters positioniert wird.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9bf9d7b117f5f61766ca326b91b0d19a2c903
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039869"
---
# <a name="how-to-create-a-header-control"></a>Erstellen eines Header Steuer Elements

In diesem Thema wird veranschaulicht, wie ein Header Steuerelement erstellt und im Client Bereich des übergeordneten Fensters positioniert wird. Sie können ein Header Steuerelement erstellen, indem Sie die Funktion " [**roatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden und die Fenster Klasse " [**WC- \_ Header**](common-control-window-classes.md) " und die entsprechenden [Header Steuerelement Stile](header-control-styles.md)angeben. Diese Fenster Klasse wird beim Laden der allgemeinen Steuerelement-DLL registriert. Um sicherzustellen, dass diese DLL geladen wird, verwenden Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Im folgenden C++-Codebeispiel wird zuerst die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufgerufen, um die allgemeine Steuerelement-DLL zu laden. Anschließend wird die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " aufgerufen, um ein Header Steuerelement zu erstellen. Das-Steuerelement ist anfänglich ausgeblendet. Die [**HDM- \_ layoutnachricht**](hdm-layout.md) wird zum Berechnen der Größe und Position des Steuer Elements im übergeordneten Fenster verwendet. Das Steuerelement wird dann neu positioniert und sichtbar gemacht.



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über Header Steuerelemente](header-controls.md)
</dt> <dt>

[Header Steuerelement Verweis](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Verwenden von Header Steuerelementen](using-header-controls.md)
</dt> </dl>

 

 
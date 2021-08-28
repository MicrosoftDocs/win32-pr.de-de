---
title: Erstellen eines Header-Steuerelements
description: In diesem Thema wird veranschaulicht, wie ein Headersteuersatz erstellt und im Clientbereich des übergeordneten Fensters positioniert wird.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae5bb3ae9c323d30384f5d058a61393bf6425c2a27dfe67faa9cbedd4b3289e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063200"
---
# <a name="how-to-create-a-header-control"></a>Erstellen eines Header-Steuerelements

In diesem Thema wird veranschaulicht, wie ein Headersteuersatz erstellt und im Clientbereich des übergeordneten Fensters positioniert wird. Sie können ein Header-Steuerelement erstellen, indem Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden und die [**WC \_ HEADER-Fensterklasse**](common-control-window-classes.md) und die entsprechenden [Headersteuerstile angeben.](header-control-styles.md) Diese Fensterklasse wird registriert, wenn die allgemeine Steuerelement-DLL geladen wird. Um sicherzustellen, dass diese DLL geladen wird, verwenden Sie die [**InitCommonControlsEx-Funktion.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Im folgenden C++-Codebeispiel wird zuerst die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) zum Laden der allgemeinen Steuerelement-DLL aufruft. Anschließend wird die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) zum Erstellen eines Header-Steuerelements aufruft. Das Steuerelement ist anfänglich ausgeblendet. Die [**HDM \_ LAYOUT-Meldung**](hdm-layout.md) wird verwendet, um die Größe und Position des Steuerelements im übergeordneten Fenster zu berechnen. Das Steuerelement wird dann neu positioniert und sichtbar gemacht.



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

[Informationen zu Headersteuerelementen](header-controls.md)
</dt> <dt>

[Header-Steuerelementreferenz](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Verwenden von Headersteuerelementen](using-header-controls.md)
</dt> </dl>

 

 
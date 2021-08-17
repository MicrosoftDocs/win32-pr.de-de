---
title: Erstellen von Statusleisten
description: Sie können eine Statusleiste erstellen, indem Sie die CreateStatusWindow-Funktion oder die CreateWindowEx-Funktion verwenden und die STATUSCLASSNAME-Fensterklasse angeben.
ms.assetid: 4ED4BFD3-904D-4198-8152-5DD13CA7C189
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7075c8d8896d59a5711d5ee80be4af90948ee4ee99a441fbbf1140cd7452c4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413188"
---
# <a name="how-to-create-status-bars"></a>Erstellen von Statusleisten

Sie können eine Statusleiste erstellen, indem Sie die [**CreateStatusWindow-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa) oder die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden und die [**STATUSCLASSNAME-Fensterklasse**](common-control-window-classes.md) angeben.

Nachdem Sie die Statusleiste erstellt haben, können Sie sie in Teile unterteilen, den Text für die einzelnen Teile festlegen und die Darstellung des Fensters mithilfe von Statusleistenmeldungen steuern.

> [!Note]  
> Um sicherzustellen, dass die allgemeine Steuerelement-DLL geladen wird, verwenden Sie zuerst die [**InitCommonControls-Funktion.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)

 

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-status-bar"></a>Erstellen einer Statusleiste

Im folgenden Beispiel wird veranschaulicht, wie Sie eine Statusleiste erstellen, die über einen Größenziehstrich verfügt, und das Fenster basierend auf der Breite des Clientbereichs des übergeordneten Fensters in vier gleiche Teile unterteilen.


```C++
// Description: 
//   Creates a status bar and divides it into the specified number of parts.
// Parameters:
//   hwndParent - parent window for the status bar.
//   idStatus - child window identifier of the status bar.
//   hinst - handle to the application instance.
//   cParts - number of parts into which to divide the status bar.
// Returns:
//   The handle to the status bar.
//
HWND DoCreateStatusBar(HWND hwndParent, int idStatus, HINSTANCE
                      hinst, int cParts)
{
    HWND hwndStatus;
    RECT rcClient;
    HLOCAL hloc;
    PINT paParts;
    int i, nWidth;

    // Ensure that the common control DLL is loaded.
    InitCommonControls();

    // Create the status bar.
    hwndStatus = CreateWindowEx(
        0,                       // no extended styles
        STATUSCLASSNAME,         // name of status bar class
        (PCTSTR) NULL,           // no text when first created
        SBARS_SIZEGRIP |         // includes a sizing grip
        WS_CHILD | WS_VISIBLE,   // creates a visible child window
        0, 0, 0, 0,              // ignores size and position
        hwndParent,              // handle to parent window
        (HMENU) idStatus,       // child window identifier
        hinst,                   // handle to application instance
        NULL);                   // no window creation data

    // Get the coordinates of the parent window's client area.
    GetClientRect(hwndParent, &rcClient);

    // Allocate an array for holding the right edge coordinates.
    hloc = LocalAlloc(LHND, sizeof(int) * cParts);
    paParts = (PINT) LocalLock(hloc);

    // Calculate the right edge coordinate for each part, and
    // copy the coordinates to the array.
    nWidth = rcClient.right / cParts;
    int rightEdge = nWidth;
    for (i = 0; i < cParts; i++) { 
       paParts[i] = rightEdge;
       rightEdge += nWidth;
    }

    // Tell the status bar to create the window parts.
    SendMessage(hwndStatus, SB_SETPARTS, (WPARAM) cParts, (LPARAM)
               paParts);

    // Free the array, and return.
    LocalUnlock(hloc);
    LocalFree(hloc);
    return hwndStatus;
}  
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Statusleisten](using-status-bars.md)
</dt> <dt>

[Demo zu Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
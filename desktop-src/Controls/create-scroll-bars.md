---
title: Erstellen von Scrollleisten
description: Beim Erstellen eines überlappenden, Popup-oder untergeordneten Fensters können Sie Standard Scrollleisten hinzufügen, indem Sie die Funktion "kreatewindowex" verwenden und "WS \_ HScroll", "WS \_ VScroll" oder beide Stile angeben.
ms.assetid: 58353030-DCF5-4368-9658-BB282B8B5EF0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b27e3e6d9495492f46567633cc53b0f3f7c5bd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474429"
---
# <a name="how-to-create-scroll-bars"></a>Erstellen von Scrollleisten

Beim Erstellen eines überlappenden, Popup-oder untergeordneten Fensters können Sie Standard Scrollleisten hinzufügen, indem Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden und "WS \_ HScroll", "WS \_ VScroll" oder beide Stile angeben.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-scroll-bar"></a>Bild Lauf Leiste erstellen

Im folgenden Beispiel wird ein Fenster mit standardmäßigen horizontalen und vertikalen Schiebe leisten erstellt.


```C++
    hwnd = CreateWindowEx( 
        0,                     // no extended styles 
        g_szWindowClass,       // global string containing name of window class
        g_szTitle,             // global string containing title bar text 
        WS_OVERLAPPEDWINDOW |  
            WS_HSCROLL | WS_VSCROLL, // window styles 
        CW_USEDEFAULT,         // default horizontal position 
        CW_USEDEFAULT,         // default vertical position 
        CW_USEDEFAULT,         // default width 
        CW_USEDEFAULT,         // default height 
        (HWND) NULL,           // no parent for overlapped windows 
        (HMENU) NULL,          // use the window class menu 
        g_hInst,               // global instance handle  
        (PVOID) NULL           // pointer not needed 
    ); 
```



Um Bild Lauf leisten Meldungen für diese Schiebe leisten zu verarbeiten, müssen Sie den entsprechenden Code in die Hauptfenster Prozedur einschließen.

Sie können [**die Funktion "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion" verwenden, um eine Bild Lauf Leiste zu erstellen, indem Sie die ScrollBar-Fenster Klasse angeben. Dadurch wird eine horizontale oder vertikale Schiebe Leiste erstellt, abhängig davon, ob [**SSB \_ Horz**](scroll-bar-control-styles.md) oder [**SSB \_ Vert**](scroll-bar-control-styles.md) als Fenster Stil angegeben wird. Die Bild Lauf leisten Größe und ihre Position relativ zum übergeordneten Fenster können ebenfalls angegeben werden.

Im folgenden Beispiel wird eine horizontale Schiebe Leiste erstellt, die am unteren Rand des Client Bereichs des übergeordneten Fensters positioniert ist.


```C++
// Description:
//   Creates a horizontal scroll bar along the bottom of the parent 
//   window's area.
// Parameters:
//   hwndParent - handle to the parent window.
//   sbHeight - height, in pixels, of the scroll bar.
// Returns:
//   The handle to the scroll bar.
HWND CreateAHorizontalScrollBar(HWND hwndParent, int sbHeight)
{
    RECT rect;

    // Get the dimensions of the parent window's client area;
    if (!GetClientRect(hwndParent, &rect))
        return NULL;

    // Create the scroll bar.
    return (CreateWindowEx( 
            0,                      // no extended styles 
            L"SCROLLBAR",           // scroll bar control class 
            (PTSTR) NULL,           // no window text 
            WS_CHILD | WS_VISIBLE   // window styles  
                | SBS_HORZ,         // horizontal scroll bar style 
            rect.left,              // horizontal position 
            rect.bottom - sbHeight, // vertical position 
            rect.right,             // width of the scroll bar 
            sbHeight,               // height of the scroll bar
            hwndParent,             // handle to main window 
            (HMENU) NULL,           // no menu 
            g_hInst,                // instance owning this window 
            (PVOID) NULL            // pointer not needed 
        )); 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Scrollleisten](using-scroll-bars.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
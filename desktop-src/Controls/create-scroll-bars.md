---
title: Erstellen von Bildlaufleisten
description: Beim Erstellen eines überlappenden, Popup- oder untergeordneten Fensters können Sie Standardscrollleisten hinzufügen, indem Sie die CreateWindowEx-Funktion verwenden und WS \_ HSCROLL, WS VSCROLL oder beide Stile \_ angeben.
ms.assetid: 58353030-DCF5-4368-9658-BB282B8B5EF0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec76c49d9f97e21626546a760d0e42a44b04c70db5790e0b80c08fcdee34412
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831752"
---
# <a name="how-to-create-scroll-bars"></a>Erstellen von Bildlaufleisten

Beim Erstellen eines überlappenden, Popup- oder untergeordneten Fensters können Sie Standardscrollleisten hinzufügen, indem Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden und WS \_ HSCROLL, WS VSCROLL oder beide Stile \_ angeben.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-scroll-bar"></a>Erstellen einer Scrollleiste

Im folgenden Beispiel wird ein Fenster mit horizontalen und vertikalen Standardscrollleisten erstellt.


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



Um Bildlaufleistenmeldungen für diese Bildlaufleisten zu verarbeiten, müssen Sie den entsprechenden Code in die Hauptfensterprozedur eingeben.

Sie können die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwenden, um eine Scrollleiste zu erstellen, indem Sie die SCROLLBAR-Fensterklasse angeben. Dadurch wird eine horizontale oder vertikale Scrollleiste erstellt, je nachdem, ob [**SBS \_ HORZ**](scroll-bar-control-styles.md) oder [**SBS \_ VERT**](scroll-bar-control-styles.md) als Fensterformat angegeben ist. Die Bildlaufleistengröße und ihre Position relativ zum übergeordneten Fenster können ebenfalls angegeben werden.

Im folgenden Beispiel wird eine horizontale Scrollleiste erstellt, die am unteren Rand des Clientbereichs des übergeordneten Fensters positioniert ist.


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

[Verwenden von Bildlaufleisten](using-scroll-bars.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
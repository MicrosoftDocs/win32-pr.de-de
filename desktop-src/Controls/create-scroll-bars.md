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
# <a name="how-to-create-scroll-bars"></a><span data-ttu-id="aec63-103">Erstellen von Scrollleisten</span><span class="sxs-lookup"><span data-stu-id="aec63-103">How to Create Scroll Bars</span></span>

<span data-ttu-id="aec63-104">Beim Erstellen eines überlappenden, Popup-oder untergeordneten Fensters können Sie Standard Scrollleisten hinzufügen, indem Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden und "WS \_ HScroll", "WS \_ VScroll" oder beide Stile angeben.</span><span class="sxs-lookup"><span data-stu-id="aec63-104">When creating an overlapped, pop-up, or child window, you can add standard scroll bars by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying WS\_HSCROLL, WS\_VSCROLL, or both styles.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="aec63-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="aec63-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="aec63-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="aec63-106">Technologies</span></span>

-   [<span data-ttu-id="aec63-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="aec63-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="aec63-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="aec63-108">Prerequisites</span></span>

-   <span data-ttu-id="aec63-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="aec63-109">C/C++</span></span>
-   <span data-ttu-id="aec63-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="aec63-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="aec63-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="aec63-111">Instructions</span></span>

### <a name="create-a-scroll-bar"></a><span data-ttu-id="aec63-112">Bild Lauf Leiste erstellen</span><span class="sxs-lookup"><span data-stu-id="aec63-112">Create a Scroll Bar</span></span>

<span data-ttu-id="aec63-113">Im folgenden Beispiel wird ein Fenster mit standardmäßigen horizontalen und vertikalen Schiebe leisten erstellt.</span><span class="sxs-lookup"><span data-stu-id="aec63-113">The following example creates a window with standard horizontal and vertical scroll bars.</span></span>


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



<span data-ttu-id="aec63-114">Um Bild Lauf leisten Meldungen für diese Schiebe leisten zu verarbeiten, müssen Sie den entsprechenden Code in die Hauptfenster Prozedur einschließen.</span><span class="sxs-lookup"><span data-stu-id="aec63-114">To process scroll bar messages for these scroll bars, you must include appropriate code in the main window procedure.</span></span>

<span data-ttu-id="aec63-115">Sie können [**die Funktion "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion" verwenden, um eine Bild Lauf Leiste zu erstellen, indem Sie die ScrollBar-Fenster Klasse angeben.</span><span class="sxs-lookup"><span data-stu-id="aec63-115">You can use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a scroll bar by specifying the SCROLLBAR window class.</span></span> <span data-ttu-id="aec63-116">Dadurch wird eine horizontale oder vertikale Schiebe Leiste erstellt, abhängig davon, ob [**SSB \_ Horz**](scroll-bar-control-styles.md) oder [**SSB \_ Vert**](scroll-bar-control-styles.md) als Fenster Stil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aec63-116">This creates a horizontal or vertical scroll bar, depending on whether [**SBS\_HORZ**](scroll-bar-control-styles.md) or [**SBS\_VERT**](scroll-bar-control-styles.md) is specified as the window style.</span></span> <span data-ttu-id="aec63-117">Die Bild Lauf leisten Größe und ihre Position relativ zum übergeordneten Fenster können ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aec63-117">The scroll bar size and its position relative to its parent window can also be specified.</span></span>

<span data-ttu-id="aec63-118">Im folgenden Beispiel wird eine horizontale Schiebe Leiste erstellt, die am unteren Rand des Client Bereichs des übergeordneten Fensters positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="aec63-118">The following example creates a horizontal scroll bar that is positioned along the bottom of the parent window's client area.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="aec63-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aec63-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec63-120">Verwenden von Scrollleisten</span><span class="sxs-lookup"><span data-stu-id="aec63-120">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="aec63-121">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="aec63-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 
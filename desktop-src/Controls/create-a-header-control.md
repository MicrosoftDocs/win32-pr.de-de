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
# <a name="how-to-create-a-header-control"></a><span data-ttu-id="b073d-103">Erstellen eines Header Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="b073d-103">How to Create a Header Control</span></span>

<span data-ttu-id="b073d-104">In diesem Thema wird veranschaulicht, wie ein Header Steuerelement erstellt und im Client Bereich des übergeordneten Fensters positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="b073d-104">This topic demonstrates how to create a header control and position it within the parent window's client area.</span></span> <span data-ttu-id="b073d-105">Sie können ein Header Steuerelement erstellen, indem Sie die Funktion " [**roatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwenden und die Fenster Klasse " [**WC- \_ Header**](common-control-window-classes.md) " und die entsprechenden [Header Steuerelement Stile](header-control-styles.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="b073d-105">You can create a header control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying the [**WC\_HEADER**](common-control-window-classes.md) window class and the appropriate [header control styles](header-control-styles.md).</span></span> <span data-ttu-id="b073d-106">Diese Fenster Klasse wird beim Laden der allgemeinen Steuerelement-DLL registriert.</span><span class="sxs-lookup"><span data-stu-id="b073d-106">This window class is registered when the common control DLL is loaded.</span></span> <span data-ttu-id="b073d-107">Um sicherzustellen, dass diese DLL geladen wird, verwenden Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b073d-107">To ensure that this DLL is loaded, use the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b073d-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="b073d-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b073d-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="b073d-109">Technologies</span></span>

-   [<span data-ttu-id="b073d-110">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b073d-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b073d-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="b073d-111">Prerequisites</span></span>

-   <span data-ttu-id="b073d-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="b073d-112">C/C++</span></span>
-   <span data-ttu-id="b073d-113">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="b073d-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b073d-114">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="b073d-114">Instructions</span></span>


<span data-ttu-id="b073d-115">Im folgenden C++-Codebeispiel wird zuerst die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufgerufen, um die allgemeine Steuerelement-DLL zu laden.</span><span class="sxs-lookup"><span data-stu-id="b073d-115">The following C++ code example first calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="b073d-116">Anschließend wird die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " aufgerufen, um ein Header Steuerelement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b073d-116">It then calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a header control.</span></span> <span data-ttu-id="b073d-117">Das-Steuerelement ist anfänglich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="b073d-117">The control is initially hidden.</span></span> <span data-ttu-id="b073d-118">Die [**HDM- \_ layoutnachricht**](hdm-layout.md) wird zum Berechnen der Größe und Position des Steuer Elements im übergeordneten Fenster verwendet.</span><span class="sxs-lookup"><span data-stu-id="b073d-118">The [**HDM\_LAYOUT**](hdm-layout.md) message is used to calculate the size and position of the control within the parent window.</span></span> <span data-ttu-id="b073d-119">Das Steuerelement wird dann neu positioniert und sichtbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="b073d-119">The control is then repositioned and made visible.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="b073d-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b073d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b073d-121">Informationen über Header Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b073d-121">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="b073d-122">Header Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="b073d-122">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b073d-123">Verwenden von Header Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="b073d-123">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 
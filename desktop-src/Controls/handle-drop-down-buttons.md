---
title: Behandeln von Dropdown-Schaltflächen
description: Eine Dropdown-Schaltfläche kann Benutzern eine Liste von Optionen zur Verfügung stellen.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724273"
---
# <a name="how-to-handle-drop-down-buttons"></a><span data-ttu-id="60901-103">Behandeln von Dropdown-Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="60901-103">How to Handle Drop-down Buttons</span></span>

<span data-ttu-id="60901-104">Eine Dropdown-Schaltfläche kann Benutzern eine Liste von Optionen zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="60901-104">A drop-down button can present users with a list of options.</span></span> <span data-ttu-id="60901-105">Um diese Art von Schaltfläche zu erstellen, geben Sie den [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil (auch als [**tbstyle- \_ Dropdown**](toolbar-control-and-button-styles.md) bezeichnet) für die Kompatibilität mit früheren Versionen der allgemeinen Steuerelemente an.</span><span class="sxs-lookup"><span data-stu-id="60901-105">To create this style of button, specify the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style (also called [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) for compatibility with previous versions of the common controls).</span></span> <span data-ttu-id="60901-106">Um eine Dropdown-Schaltfläche mit einem Pfeil anzuzeigen, müssen Sie auch den Symbolleisten Stil [**tbstyle \_ Ex \_ drawddarrows**](toolbar-extended-styles.md) festlegen, indem Sie eine [**TB- \_ SetExtendedStyle**](tb-setextendedstyle.md) -Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="60901-106">To show a drop-down button with an arrow, you must also set the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) toolbar style by sending a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span>

<span data-ttu-id="60901-107">Die folgende Abbildung zeigt eine Dropdown-Schaltfläche "Öffnen", bei der das Kontextmenü geöffnet ist und eine Liste von Dateien anzeigt.</span><span class="sxs-lookup"><span data-stu-id="60901-107">The following illustration shows a drop-down "Open" button with the context menu open and showing a list of files.</span></span> <span data-ttu-id="60901-108">In diesem Beispiel hat die Symbolleiste den Stil [**tbstyle \_ Ex \_ drawddarrows**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="60901-108">In this example, the toolbar has the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![Screenshot eines Dialog Felds mit drei Symbolleisten Elementen, die durch Symbole dargestellt werden. eine verfügt über einen erweiterten Dropdown Pfeil und ein Kontextmenü mit drei Elementen.](images/tb-dropdown.png)

<span data-ttu-id="60901-110">In der folgenden Abbildung wird die gleiche Symbolleiste angezeigt, diesmal ohne den Stil " [**tbstyle \_ Ex \_ drawddarrows**](toolbar-extended-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="60901-110">The following illustration shows the same toolbar, this time without the [**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style.</span></span>

![Screenshot eines vorherigen Dialog Felds, aber das Symbol mit dem Kontextmenü enthält keinen Dropdown Pfeil.](images/tb-dropdown2.png)

<span data-ttu-id="60901-112">Wenn Benutzer auf eine Symbolleisten Schaltfläche klicken, die den [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil verwendet, sendet das Symbolleisten-Steuerelement das übergeordnete Fenster mit dem [ \_ Dropdown](tbn-dropdown.md) -Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="60901-112">When users click a toolbar button that uses the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style, the toolbar control sends its parent window a [TBN\_DROPDOWN](tbn-dropdown.md) notification code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="60901-113">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="60901-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="60901-114">Technologien</span><span class="sxs-lookup"><span data-stu-id="60901-114">Technologies</span></span>

-   [<span data-ttu-id="60901-115">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="60901-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="60901-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="60901-116">Prerequisites</span></span>

-   <span data-ttu-id="60901-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="60901-117">C/C++</span></span>
-   <span data-ttu-id="60901-118">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="60901-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="60901-119">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="60901-119">Instructions</span></span>

### <a name="handle-a-drop-down-button"></a><span data-ttu-id="60901-120">Behandeln einer Dropdown Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="60901-120">Handle a Drop-down Button</span></span>

<span data-ttu-id="60901-121">Im folgenden Codebeispiel wird veranschaulicht, wie eine Anwendung eine Dropdown-Schaltfläche in einem Symbolleisten-Steuerelement unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="60901-121">The following code example demonstrates how an application can support a drop-down button in a toolbar control.</span></span>


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="60901-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60901-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60901-123">Verwenden von Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="60901-123">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="60901-124">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="60901-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





---
title: Behandeln von BCN_DROPDOWN Benachrichtigungen von splitbuttons
description: In diesem Thema wird beschrieben, wie Sie \_ in einem Dialogfeld Prozeduren auf die BCN-Dropdown Benachrichtigung reagieren können.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102443"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a><span data-ttu-id="77e71-103">Behandeln der BCN- \_ Dropdown Benachrichtigung über eine unterteilte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="77e71-103">How to Handle the BCN\_DROPDOWN Notification from a Split Button</span></span>

<span data-ttu-id="77e71-104">In diesem Thema wird beschrieben, wie Sie in einem Dialogfeld Prozeduren auf die [BCN- \_ Dropdown](bcn-dropdown.md) Benachrichtigung reagieren können.</span><span class="sxs-lookup"><span data-stu-id="77e71-104">This topic describes one possible way of responding to the [BCN\_DROPDOWN](bcn-dropdown.md) notification in a dialog procedure.</span></span>

<span data-ttu-id="77e71-105">Die C++-Anwendung ruft die Client Koordinaten der Schaltfläche aus dem Benachrichtigungs Header ab und konvertiert sie in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="77e71-105">The C++ application retrieves the client coordinates of the button from the notification header and converts them to screen coordinates.</span></span> <span data-ttu-id="77e71-106">Anschließend wird ein Popupmenü erstellt und am unteren Rand der Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77e71-106">It then creates a popup menu and displays it at the bottom of the button.</span></span> <span data-ttu-id="77e71-107">Um das Beispiel einfach zu halten, sind keine Tastenkombinationen für das Menü implementiert.</span><span class="sxs-lookup"><span data-stu-id="77e71-107">To keep the example simple, keyboard shortcuts are not implemented for the menu.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="77e71-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="77e71-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="77e71-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="77e71-109">Technologies</span></span>

-   [<span data-ttu-id="77e71-110">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="77e71-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="77e71-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="77e71-111">Prerequisites</span></span>

-   <span data-ttu-id="77e71-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="77e71-112">C/C++</span></span>
-   <span data-ttu-id="77e71-113">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="77e71-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="77e71-114">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="77e71-114">Instructions</span></span>

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a><span data-ttu-id="77e71-115">Schritt 1: warten auf die *BCN- \_ Dropdown* Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="77e71-115">Step 1: Wait for the *BCN\_DROPDOWN* notification.</span></span>


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a><span data-ttu-id="77e71-116">Schritt 2: Sie erhalten die Bildschirm Koordinaten der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="77e71-116">Step 2: Get the screen coordinates of the button.</span></span>

<span data-ttu-id="77e71-117">Verwenden Sie die [**clientdescreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) -Funktion, um die Fenster Koordinaten der unteren linken Kante der Schaltfläche in Bildschirm Koordinaten zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="77e71-117">Use the [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) function to convert the window coordinates of the button's lower left edge to screen coordinates.</span></span>


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a><span data-ttu-id="77e71-118">Schritt 3: Erstellen Sie ein Menü, und fügen Sie Elemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="77e71-118">Step 3: Create a menu and add items.</span></span>

<span data-ttu-id="77e71-119">Verwenden Sie die Funktion " [**kreatepopupmenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) ", um ein Menü zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77e71-119">Use the [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) function to create a menu.</span></span> <span data-ttu-id="77e71-120">Verwenden Sie die [**AppendMenu**](/windows/desktop/menurc/u) -Funktion, um dem Menü Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="77e71-120">Use the [**AppendMenu**](/windows/desktop/menurc/u) function to add items to the menu.</span></span> <span data-ttu-id="77e71-121">IDC \_ MENUCOMMAND1 und IDC \_ MENUCOMMAND2 sind Anwendungs definierte Konstanten für Menübefehle.</span><span class="sxs-lookup"><span data-stu-id="77e71-121">IDC\_MENUCOMMAND1 and IDC\_MENUCOMMAND2 are application-defined constants for menu commands.</span></span>


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a><span data-ttu-id="77e71-122">Schritt 4: zeigen Sie das Menü an.</span><span class="sxs-lookup"><span data-stu-id="77e71-122">Step 4: Display the menu.</span></span>

<span data-ttu-id="77e71-123">Die [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) -Funktion zeigt ein Kontextmenü an der angegebenen Position an und verfolgt die Auswahl der Elemente im Menü.</span><span class="sxs-lookup"><span data-stu-id="77e71-123">The [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) function displays a shortcut menu at the specified location and tracks the selection of items on the menu.</span></span>


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a><span data-ttu-id="77e71-124">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="77e71-124">Complete example</span></span>


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="77e71-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77e71-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77e71-126">BCN- \_ Dropdown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="77e71-126">BCN\_DROPDOWN Notification Code</span></span>](bcn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="77e71-127">Informationen zu Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="77e71-127">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="77e71-128">Button-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="77e71-128">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="77e71-129">Verwenden von Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="77e71-129">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="77e71-130">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="77e71-130">Button</span></span>](buttons.md)
</dt> </dl>

 

 
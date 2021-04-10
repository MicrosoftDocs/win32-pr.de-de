---
title: Erstellen eines Tree-View-Steuer Elements
description: Um ein Strukturansicht-Steuerelement zu erstellen, verwenden Sie die Funktion "kreatewindowex", die den WC- \_ TreeView-Wert für die Fenster Klasse angibt.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102431"
---
# <a name="how-to-create-a-tree-view-control"></a><span data-ttu-id="d954f-103">Erstellen eines Tree-View-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="d954f-103">How to Create a Tree-View Control</span></span>

<span data-ttu-id="d954f-104">Um ein Strukturansicht-Steuerelement zu erstellen, verwenden Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", die den [**WC- \_ TreeView**](common-control-window-classes.md) -Wert für die Fenster Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="d954f-104">To create a tree-view control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_TREEVIEW**](common-control-window-classes.md) value for the window class.</span></span> <span data-ttu-id="d954f-105">Die Strukturansicht-Fenster Klasse wird beim Laden der allgemeinen Steuerelement-DLL im Adressraum der Anwendung registriert.</span><span class="sxs-lookup"><span data-stu-id="d954f-105">The tree-view window class is registered in the application's address space when the common control DLL is loaded.</span></span> <span data-ttu-id="d954f-106">Um sicherzustellen, dass die dll geladen wird, verwenden Sie die Funktion [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .</span><span class="sxs-lookup"><span data-stu-id="d954f-106">To ensure that the DLL is loaded, use the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d954f-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="d954f-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d954f-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="d954f-108">Technologies</span></span>

-   [<span data-ttu-id="d954f-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d954f-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d954f-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d954f-110">Prerequisites</span></span>

-   <span data-ttu-id="d954f-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d954f-111">C/C++</span></span>
-   <span data-ttu-id="d954f-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d954f-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d954f-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d954f-113">Instructions</span></span>

### <a name="create-an-instance-of-a-tree-view-control"></a><span data-ttu-id="d954f-114">Erstellen einer Instanz eines Tree-View-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="d954f-114">Create an Instance of a Tree-View Control</span></span>

<span data-ttu-id="d954f-115">Im folgenden Beispiel wird ein Strukturansicht-Steuerelement erstellt, dessen Größenanpassung an den Client Bereich des übergeordneten Fensters erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d954f-115">The following example creates a tree-view control that is sized to fit the client area of the parent window.</span></span> <span data-ttu-id="d954f-116">Außerdem werden Anwendungs definierte Funktionen verwendet, um dem Steuerelement eine Bildliste zuzuordnen und dem Steuerelement Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d954f-116">It also uses application-defined functions to associate an image list with the control and add items to the control.</span></span>


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a><span data-ttu-id="d954f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d954f-117">Remarks</span></span>

<span data-ttu-id="d954f-118">Wenn Sie ein Strukturansicht-Steuerelement erstellen, können Sie ihm auch eine [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont) -Nachricht senden, um die Schriftart festzulegen, die für den Text verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d954f-118">When you create a tree-view control, you can also send it a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to set the font to be used for the text.</span></span> <span data-ttu-id="d954f-119">Sie sollten diese Nachricht vor dem Einfügen von Elementen senden.</span><span class="sxs-lookup"><span data-stu-id="d954f-119">You should send this message before inserting any items.</span></span> <span data-ttu-id="d954f-120">Standardmäßig wird in einer Strukturansicht die Symbol Titel Schriftart verwendet.</span><span class="sxs-lookup"><span data-stu-id="d954f-120">By default, a tree view uses the icon title font.</span></span> <span data-ttu-id="d954f-121">Obwohl Sie die Schriftart pro Element mithilfe von [benutzerdefiniertem zeichnen](custom-draw.md)anpassen können, verwendet das Strukturansicht-Steuerelement die Dimensionen der Schriftart, die von der **WM- \_ setFont** -Nachricht angegeben werden, um den Abstand und das Layout zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d954f-121">Although you can customize the font per-item by using [Custom Draw](custom-draw.md), the tree-view control uses the dimensions of the font specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d954f-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d954f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d954f-123">Verwenden von Tree-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d954f-123">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="d954f-124">Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d954f-124">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 
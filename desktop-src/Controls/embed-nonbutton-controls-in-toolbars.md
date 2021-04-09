---
title: Einbetten von nicht-Schaltflächen-Steuerelementen in Symbolleisten
description: Symbolleisten unterstützen nur Schaltflächen. Daher müssen Sie, wenn Ihre Anwendung eine andere Art von Kontrolle erfordert, ein untergeordnetes Fenster erstellen. Die folgende Abbildung zeigt eine Symbolleiste mit einem eingebetteten Bearbeitungs Steuerelement.
ms.assetid: 7B4DACEF-96BB-447E-AE8F-F55401C665E9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ae2189350b9ea2f4aaa0c3ea0b49727bd3415
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103858102"
---
# <a name="how-to-embed-nonbutton-controls-in-toolbars"></a><span data-ttu-id="67efe-104">Einbetten von nicht-Schaltflächen-Steuerelementen in Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="67efe-104">How to Embed Nonbutton Controls in Toolbars</span></span>

<span data-ttu-id="67efe-105">Symbolleisten unterstützen nur Schaltflächen. Daher müssen Sie, wenn Ihre Anwendung eine andere Art von Kontrolle erfordert, ein untergeordnetes Fenster erstellen.</span><span class="sxs-lookup"><span data-stu-id="67efe-105">Toolbars support only buttons; therefore, if your application requires a different kind of control, you must create a child window.</span></span> <span data-ttu-id="67efe-106">Die folgende Abbildung zeigt eine Symbolleiste mit einem eingebetteten Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="67efe-106">The following illustration shows a toolbar with an embedded edit control.</span></span>

![Screenshot eines Dialog Felds mit einem Bearbeitungs Steuerelement auf der Symbolleiste, vorangehenden drei Symbolleisten Symbolen](images/tb-withedit.png)

> [!Note]  
> <span data-ttu-id="67efe-108">Erwägen Sie die Verwendung von Grund leisten-Steuer [Elementen](rebar-controls.md) anstelle von Steuerelementen in Symbolleisten.</span><span class="sxs-lookup"><span data-stu-id="67efe-108">Consider using [Rebar Controls](rebar-controls.md) instead of placing controls in toolbars.</span></span>

 

<span data-ttu-id="67efe-109">Jeder Fenstertyp kann auf einer Symbolleiste platziert werden.</span><span class="sxs-lookup"><span data-stu-id="67efe-109">Any type of window can be placed on a toolbar.</span></span> <span data-ttu-id="67efe-110">Im folgenden Beispielcode wird ein Bearbeitungs Steuerelement als untergeordnetes Element des Fensters Symbolleisten-Steuerelement hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="67efe-110">The following example code adds an edit control as a child of the toolbar control window.</span></span> <span data-ttu-id="67efe-111">Da die Symbolleiste erstellt und dann das Bearbeitungs Steuerelement hinzugefügt wurde, müssen Sie Platz für das Bearbeitungs Steuerelement bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="67efe-111">Because the toolbar is created and then the edit control added, you must provide space for the edit control.</span></span> <span data-ttu-id="67efe-112">Eine Möglichkeit besteht darin, ein Trennzeichen als Platzhalter in der Symbolleiste hinzuzufügen und die Breite des Trenn Zeichens auf die Anzahl der Pixel festzulegen, die Sie reservieren möchten.</span><span class="sxs-lookup"><span data-stu-id="67efe-112">One way to do this is to add a separator as a placeholder in the toolbar, setting the width of the separator to the number of pixels you want to reserve.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="67efe-113">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="67efe-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="67efe-114">Technologien</span><span class="sxs-lookup"><span data-stu-id="67efe-114">Technologies</span></span>

-   [<span data-ttu-id="67efe-115">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="67efe-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="67efe-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="67efe-116">Prerequisites</span></span>

-   <span data-ttu-id="67efe-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="67efe-117">C/C++</span></span>
-   <span data-ttu-id="67efe-118">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="67efe-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="67efe-119">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="67efe-119">Instructions</span></span>

### <a name="embed-a-nonbutton-control-in-a-toolbar"></a><span data-ttu-id="67efe-120">Einbetten eines nonbutton-Steuer Elements in einer Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="67efe-120">Embed a Nonbutton Control in a Toolbar</span></span>

<span data-ttu-id="67efe-121">Der folgende Code Ausschnitt erstellt die Symbolleiste in der obigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="67efe-121">The following code snippet creates the toolbar in the preceding illustration.</span></span>


```C++
// IDM_NEW, IDM_OPEN, and IDM_SAVE are application-defined command constants.

HIMAGELIST g_hImageList = NULL;

HWND CreateToolbarWithEdit(HWND hWndParent)
{
    const int ImageListID = 0;    // Define some constants.
    const int bitmapSize  = 16;
    
    const int cx_edit = 100;      // Dimensions of edit control.
    const int cy_edit = 35;  

    TBBUTTON tbButtons[] =        // Toolbar buttons.
    {
        // The separator is set to the width of the edit control. 
        
        {cx_edit, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, -1},
        {STD_FILENEW, IDM_NEW, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILEOPEN, IDM_OPEN, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {STD_FILESAVE, IDM_SAVE, TBSTATE_ENABLED, BTNS_BUTTON, {0}, 0, 0},
        {0, 0, TBSTATE_ENABLED, BTNS_SEP, {0}, 0, 0},
    };

    // Create the toolbar.
    HWND hWndToolbar = CreateWindowEx(0, TOOLBARCLASSNAME, L"Toolbar", 
                                      WS_CHILD | WS_VISIBLE | WS_BORDER, 
                                      0, 0, 0, 0,
                                      hWndParent, NULL, HINST_COMMCTRL, NULL);

    if (!hWndToolbar)
        return NULL;
    
    int numButtons = sizeof(tbButtons) / sizeof(TBBUTTON);

    // Create the image list.
    g_hImageList = ImageList_Create(bitmapSize, bitmapSize, // Dimensions of individual bitmaps.
                                    0,                      // Flags.
                                    numButtons, 0);

    // Set the image list.
    SendMessage(hWndToolbar, TB_SETIMAGELIST, (WPARAM)ImageListID, (LPARAM)g_hImageList);

    // Load the button images.
    SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);

    // Add buttons.
    SendMessage(hWndToolbar, TB_BUTTONSTRUCTSIZE, (WPARAM)sizeof(TBBUTTON), 0);
    SendMessage(hWndToolbar, TB_ADDBUTTONS,       (WPARAM)numButtons,       (LPARAM)&tbButtons);

    // Create the edit control child window.    
    HWND hWndEdit = CreateWindowEx(0L, L"Edit", NULL, 
                                   WS_CHILD | WS_BORDER | WS_VISIBLE | ES_LEFT | ES_AUTOVSCROLL | ES_MULTILINE, 
                                   0, 0, cx_edit, cy_edit, 
                                   hWndToolbar, (HMENU) IDM_EDIT, g_hInst, 0 );
    
    if (!hWndEdit)
    {
        DestroyWindow(hWndToolbar);
        ImageList_Destroy(g_hImageList);
        
        return NULL;
    }
    
    return hWndToolbar;    // Return the toolbar with the embedded edit control.
}
```



<span data-ttu-id="67efe-122">In diesem Beispiel werden die Dimensionen des untergeordneten Fensters hart codiert. Wenn Sie jedoch eine stabilere Anwendung erstellen möchten, ermitteln Sie die Größe der Symbolleiste, und legen Sie das Bearbeitungs Steuerelement Fenster an.</span><span class="sxs-lookup"><span data-stu-id="67efe-122">This example hard-codes the dimensions of the child window; however, to make a more robust application, determine the size of the toolbar and make the edit control window to fit.</span></span>

<span data-ttu-id="67efe-123">Möglicherweise möchten Sie, dass die Bearbeitungs Steuerelement-Benachrichtigungen zu einem anderen Fenster, z. b. dem übergeordneten Symbol der Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="67efe-123">You might want the edit control notifications to go to another window, such as the toolbar's parent.</span></span> <span data-ttu-id="67efe-124">Erstellen Sie hierzu das Bearbeitungs Steuerelement als untergeordnetes Element des übergeordneten Fensters der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="67efe-124">To do this, create the edit control as a child of the toolbar's parent window.</span></span> <span data-ttu-id="67efe-125">Ändern Sie dann das übergeordnete Element des Bearbeitungs Steuer Elements wie folgt in die Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="67efe-125">Then change the parent of the edit control to the toolbar as follows.</span></span>


```
SetParent (hWndEdit, hWndToolbar);
```



<span data-ttu-id="67efe-126">Benachrichtigungen gelangen zum ursprünglichen übergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="67efe-126">Notifications go to the original parent.</span></span> <span data-ttu-id="67efe-127">Aus diesem Grund werden die Bearbeitungs Steuerelement Meldungen an das übergeordnete Element der Symbolleiste gesendet, auch wenn sich das Bearbeitungsfenster im Symbolleisten Fenster befindet.</span><span class="sxs-lookup"><span data-stu-id="67efe-127">Therefore, the edit control messages go to the parent of the toolbar even though the edit window resides in the toolbar window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67efe-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67efe-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67efe-129">Verwenden von Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="67efe-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="67efe-130">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="67efe-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





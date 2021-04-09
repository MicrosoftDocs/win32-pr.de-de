---
title: Verwenden von Hot-Tracking mit Symbolleisten
description: Wenn ein Mauszeiger über ein Element bewegt wird, wird das Element in den heiß. Wenn die Hot-Tracking-Funktion aktiviert ist, wird das heiße Element hervorgehoben. Eine Symbolleiste, die mit dem flachen Stil tbstyle erstellt wird \_ , oder eine Symbolleiste, die visuelle Stile verwendet, unterstützt standardmäßig Hot-Tracking.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104038708"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a><span data-ttu-id="447a4-105">Verwenden von Hot-Tracking mit Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="447a4-105">How to Use Hot-Tracking with Toolbars</span></span>

<span data-ttu-id="447a4-106">Wenn ein Mauszeiger über ein Element bewegt wird, wird das Element in den heiß.</span><span class="sxs-lookup"><span data-stu-id="447a4-106">When a mouse pointer hovers over an item, the item becomes hot.</span></span> <span data-ttu-id="447a4-107">Wenn die Hot-Tracking-Funktion aktiviert ist, wird das heiße Element hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="447a4-107">If hot-tracking is enabled, the hot item is highlighted.</span></span> <span data-ttu-id="447a4-108">Eine Symbolleiste, die mit dem [**\_ flachen Stil tbstyle**](toolbar-control-and-button-styles.md) erstellt wird, oder eine Symbolleiste, die [visuelle Stile](themes-overview.md)verwendet, unterstützt standardmäßig Hot-Tracking.</span><span class="sxs-lookup"><span data-stu-id="447a4-108">A toolbar that is created with the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style, or one that uses [Visual Styles](themes-overview.md), supports hot-tracking by default.</span></span>

<span data-ttu-id="447a4-109">Die Hot-Tracking erfordert, dass Sie Bildlisten erstellen; Daher können Sie Ihre Symbolleiste nicht mithilfe der [**TB- \_ AddBitmap**](tb-addbitmap.md) -Nachricht oder [**der Funktion "**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) -Funktion" in der Funktion "Anordnen" erstellen.</span><span class="sxs-lookup"><span data-stu-id="447a4-109">Hot-tracking requires that you create image lists; therefore, you cannot use the [**TB\_ADDBITMAP**](tb-addbitmap.md) message or the [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function to create your toolbar.</span></span>

<span data-ttu-id="447a4-110">Wenn die Maus über eine Symbolleisten Schaltfläche bewegt wird, wird die Schaltfläche so dargestellt, dass Sie hervorgehoben wird</span><span class="sxs-lookup"><span data-stu-id="447a4-110">When the mouse hovers over a toolbar button, the button is outlined to highlight it.</span></span> <span data-ttu-id="447a4-111">In der folgenden Abbildung ist eine Symbolleiste mit aktivierter Hot-Tracking-Funktion dargestellt. der Mauszeiger befand sich auf die Schaltfläche "Speichern", als der Screenshot erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="447a4-111">The following illustration shows a toolbar with hot-tracking enabled; the mouse pointer was hovering on the Save button when the screen shot was taken.</span></span>

![Screenshot eines Dialog Felds mit einer drei-Element-Symbolleiste das ausgewählte Symbol wird angezeigt.](images/tb-withstyles.png)

<span data-ttu-id="447a4-113">Wenn Sie möchten, dass sich die Bitmap einer Symbolleisten-Schaltfläche ändert, wenn sich der Zustand des Steuer Elements ändert, speichern Sie die verschiedenen Bilder in [Bildlisten](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="447a4-113">If you want a toolbar button bitmap to change when the state of the control changes, store the different images in [image lists](image-lists.md).</span></span> <span data-ttu-id="447a4-114">Beispielsweise verfügen einige Anwendungen über schwarze und weiße Symbolleisten Schaltflächen, die bei der Auswahl angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="447a4-114">For example, some applications have black and white toolbar buttons that become colored when they are selected.</span></span> <span data-ttu-id="447a4-115">Die beiden unterschiedlichen Bilder werden in Bildlisten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="447a4-115">The two different images are stored in image lists.</span></span> <span data-ttu-id="447a4-116">Symbolleisten unterstützen die Verwendung von bis zu drei Bildlisten.</span><span class="sxs-lookup"><span data-stu-id="447a4-116">Toolbars support using up to three image lists.</span></span> <span data-ttu-id="447a4-117">In der Regel verfügt eine Anwendung über eine standardmäßige, deaktivierte und nach Verfolgungs Liste von Bildern.</span><span class="sxs-lookup"><span data-stu-id="447a4-117">Typically an application has a default, disabled, and hot-tracking list of images.</span></span> <span data-ttu-id="447a4-118">Um Bildlisten für heiße Symbolleisten Schaltflächen festzulegen und abzurufen, verwenden Sie die TB-Meldungen [**\_ SetHotImageList**](tb-sethotimagelist.md) und [**TB \_ gethotimagelist**](tb-gethotimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="447a4-118">To set and retrieve image lists for hot toolbar buttons, use the [**TB\_SETHOTIMAGELIST**](tb-sethotimagelist.md) and [**TB\_GETHOTIMAGELIST**](tb-gethotimagelist.md) messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="447a4-119">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="447a4-119">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="447a4-120">Technologien</span><span class="sxs-lookup"><span data-stu-id="447a4-120">Technologies</span></span>

-   [<span data-ttu-id="447a4-121">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="447a4-121">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="447a4-122">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="447a4-122">Prerequisites</span></span>

-   <span data-ttu-id="447a4-123">C/C++</span><span class="sxs-lookup"><span data-stu-id="447a4-123">C/C++</span></span>
-   <span data-ttu-id="447a4-124">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="447a4-124">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="447a4-125">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="447a4-125">Instructions</span></span>

### <a name="use-hot-tracking-with-a-toolbar"></a><span data-ttu-id="447a4-126">Verwenden von Hot-Tracking mit einer Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="447a4-126">Use Hot-Tracking with a Toolbar</span></span>

<span data-ttu-id="447a4-127">Im folgenden Codebeispiel wird eine Bildliste für Hot Buttons erstellt, ausgefüllt und zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="447a4-127">The following code example creates, fills, and assigns an image list for hot buttons.</span></span>


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a><span data-ttu-id="447a4-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="447a4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="447a4-129">Verwenden von Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="447a4-129">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="447a4-130">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="447a4-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





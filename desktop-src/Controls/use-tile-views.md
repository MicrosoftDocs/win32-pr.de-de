---
title: Verwenden von Kachel Ansichten
description: In diesem Thema wird veranschaulicht, wie die Kachel Ansicht für ein Listenansicht-Steuerelement festgelegt wird.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949230"
---
# <a name="how-to-use-tile-views"></a><span data-ttu-id="3d8d8-103">Verwenden von Kachel Ansichten</span><span class="sxs-lookup"><span data-stu-id="3d8d8-103">How to Use Tile Views</span></span>

<span data-ttu-id="3d8d8-104">In diesem Thema wird veranschaulicht, wie die Kachel Ansicht für ein Listenansicht-Steuerelement festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-104">This topic demonstrates how to set the tile view for a list-view control.</span></span> <span data-ttu-id="3d8d8-105">In der Kachel Ansicht wird jedes Element durch ein großes Symbol mit einer oder mehreren Zeilen mit begleitenden Text dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-105">In tile view, each item is represented by a large icon with one or more lines of accompanying text.</span></span> <span data-ttu-id="3d8d8-106">Eine Abbildung finden Sie unter [Informationen zu List-View](list-view-controls-overview.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-106">For an illustration, see [About List-View Controls](list-view-controls-overview.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3d8d8-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="3d8d8-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3d8d8-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="3d8d8-108">Technologies</span></span>

-   [<span data-ttu-id="3d8d8-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3d8d8-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3d8d8-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3d8d8-110">Prerequisites</span></span>

-   <span data-ttu-id="3d8d8-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="3d8d8-111">C/C++</span></span>
-   <span data-ttu-id="3d8d8-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="3d8d8-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3d8d8-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="3d8d8-113">Instructions</span></span>


<span data-ttu-id="3d8d8-114">Legen Sie die allgemeinen Anzeige Parameter für die Kachel Ansicht fest, indem Sie das [**ListView \_ settileviewinfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-114">Set the general display parameters for tile view by using the [**ListView\_SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) macro.</span></span> <span data-ttu-id="3d8d8-115">Verwenden Sie die an dieses Makro weiter gegebene " [**lvtileviewinfo**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) "-Struktur, um die Position des Texts in Bezug auf das Symbol, die Größe der einzelnen Kacheln (einschließlich begleitenden Texts) und die maximale Anzahl von Textzeilen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-115">Use the [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) structure that is passed to this macro to specify the position of the text in relation to the icon, the size of each tile (including accompanying text), and the maximum number of lines of text.</span></span>

<span data-ttu-id="3d8d8-116">Wenn die Größe der Kacheln nicht automatisch skaliert werden soll, müssen Sie im **dwFlags** -Member und im [**dwtileviewinfo**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) **-Member** **die Größe von \_** " **lvtvif \_ FixedSize** " festlegen und die Dimensionen im **sizetile** -Member bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-116">If you do not want tiles to be automatically sized, you must set **LVTVIF\_FIXEDSIZE** in the **dwFlags** member and **LVTVIM\_TILESIZE** in the **dwMask** member of [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), as well as providing the dimensions in the **sizeTile** member.</span></span>

<span data-ttu-id="3d8d8-117">Im folgenden C++-Codebeispiel werden die Kachel Ansichts Informationen für ein Listenansicht-Steuerelement festgelegt, sodass für jedes Element maximal zwei unter Elemente angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-117">The following C++ code example sets the tile view info for a list-view control so that a maximum of two subitems are displayed for each item.</span></span> <span data-ttu-id="3d8d8-118">Außerdem wird die Größe der einzelnen Kacheln festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-118">It also sets the size of each tile.</span></span>


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



<span data-ttu-id="3d8d8-119">Für jedes Element in der Liste können Sie weitere Parameter festlegen, wenn das Element in die Liste eingefügt wird, oder später.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-119">For each item in the list, you can set further parameters when the item is inserted in the list, or later.</span></span> <span data-ttu-id="3d8d8-120">Die [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die mit [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) verwendet wird, enthält Elemente, die angeben, welche Datenspalten unterhalb des Elements angezeigt werden sollen, und deren Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-120">The [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that is used with [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contains members that specify which columns of data to display below the item, and their alignment.</span></span> <span data-ttu-id="3d8d8-121">Diese gleichen Anzeige Parameter finden Sie auch in der mit [**ListView \_ settileinfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo)verwendeten Struktur " [**lvtileinfo**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) ".</span><span class="sxs-lookup"><span data-stu-id="3d8d8-121">These same display parameters are also found in the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure used with [**ListView\_SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span></span>

> [!Note]  
> <span data-ttu-id="3d8d8-122">"Columns" bezieht sich hier nicht auf das Anzeigen von Spalten in der Kachel Ansicht, sondern auf unter Elemente, die in den Spalten in der Detailansicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3d8d8-122">"Columns" here refers not to display columns in tile view but rather to subitems, which are displayed in columns in details view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3d8d8-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d8d8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d8d8-124">Listenansicht-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="3d8d8-124">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3d8d8-125">Informationen zu List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="3d8d8-125">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="3d8d8-126">Verwenden von List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="3d8d8-126">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





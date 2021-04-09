---
title: Verwenden List-View Arbeitsbereichen
description: In diesem Thema wird die Arbeit mit Arbeitsbereichen in der Listenansicht veranschaulicht. Arbeitsbereiche sind rechteckige virtuelle Bereiche, die zum Anordnen von Elementen in einem List-VEW-Steuerelement verwendet werden können.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036794"
---
# <a name="how-to-use-list-view-working-areas"></a><span data-ttu-id="55556-104">Verwenden List-View Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="55556-104">How to Use List-View Working Areas</span></span>

<span data-ttu-id="55556-105">In diesem Thema wird die Arbeit mit Arbeitsbereichen in der Listenansicht veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="55556-105">This topic demonstrates how to work with list-view working areas.</span></span> <span data-ttu-id="55556-106">Arbeitsbereiche sind rechteckige virtuelle Bereiche, die zum Anordnen von Elementen in einem List-VEW-Steuerelement verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="55556-106">Working areas are rectangular virtual areas that can be used to arrange items in a list-vew control.</span></span> <span data-ttu-id="55556-107">Ein Arbeitsbereich ist kein Fenster und kann keinen sichtbaren Rahmen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="55556-107">A working area is not a window and cannot have a visible border.</span></span> <span data-ttu-id="55556-108">Standardmäßig weist das Listenansicht-Steuerelement keine Arbeitsbereiche auf.</span><span class="sxs-lookup"><span data-stu-id="55556-108">By default, the list-view control has no working areas.</span></span> <span data-ttu-id="55556-109">Wenn Sie einen Arbeitsbereich erstellen, können Sie Links, oben oder rechts von den Elementen einen leeren Rahmen erstellen oder eine horizontale Schiebe Leiste anzeigen, wenn es normalerweise keine wäre.</span><span class="sxs-lookup"><span data-stu-id="55556-109">By creating a working area, you can create an empty border on the left, top, or right of the items or cause a horizontal scroll bar to be displayed when there normally would not be one.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="55556-110">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="55556-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="55556-111">Technologien</span><span class="sxs-lookup"><span data-stu-id="55556-111">Technologies</span></span>

-   [<span data-ttu-id="55556-112">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="55556-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="55556-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="55556-113">Prerequisites</span></span>

-   <span data-ttu-id="55556-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="55556-114">C/C++</span></span>
-   <span data-ttu-id="55556-115">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="55556-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="55556-116">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="55556-116">Instructions</span></span>

### <a name="create-a-working-area"></a><span data-ttu-id="55556-117">Erstellen eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="55556-117">Create a Working Area</span></span>

<span data-ttu-id="55556-118">Im folgenden C++-Codebeispiel wird veranschaulicht, wie ein Arbeitsbereich mit einem leeren 25-Pixel-Rahmen auf der oberen, linken und rechten Seite erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="55556-118">The following C++ code example demonstrates how to create a working area with a 25-pixel empty border on its top, left, and right sides.</span></span>


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a><span data-ttu-id="55556-119">Erstellen mehrerer Arbeitsbereiche</span><span class="sxs-lookup"><span data-stu-id="55556-119">Create Multiple Working Areas</span></span>

<span data-ttu-id="55556-120">Im folgenden C++-Codebeispiel wird veranschaulicht, wie zwei Arbeitsbereiche in einem-Steuerelement erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="55556-120">The following C++ code example demonstrates how to create two working areas in a control.</span></span> <span data-ttu-id="55556-121">Jeder Arbeitsbereich verwendet ungefähr die Hälfte des Client Bereichs und ist von einem leeren 25-Pixel-Rahmen umgeben.</span><span class="sxs-lookup"><span data-stu-id="55556-121">Each working area uses about half of the client area, and is surrounded by a 25-pixel empty border.</span></span>


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a><span data-ttu-id="55556-122">Bestimmen Sie den Arbeitsbereich, zu dem ein Element gehört.</span><span class="sxs-lookup"><span data-stu-id="55556-122">Determine the Working Area to Which an Item Belongs</span></span>

<span data-ttu-id="55556-123">Eine Möglichkeit, zu bestimmen, zu welchem Arbeitsbereich ein Element gehört, besteht darin, die folgenden Aufgaben durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="55556-123">One way to determine which working area an item belongs is to do the following:</span></span>

-   <span data-ttu-id="55556-124">Rufen Sie die Liste der Koordinaten aller Arbeitsbereiche im Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="55556-124">Retrieve the list of coordinates of all of the working areas in the list-view control.</span></span>
-   <span data-ttu-id="55556-125">Ruft die Koordinaten des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="55556-125">Retrieve the coordinates of the item.</span></span>
-   <span data-ttu-id="55556-126">Bestimmen Sie, ob die Element Koordinaten innerhalb der Koordinaten eines der Arbeitsbereiche liegen.</span><span class="sxs-lookup"><span data-stu-id="55556-126">Determine whether the item coordinates lie within the coordinates of one of the working areas.</span></span>

<span data-ttu-id="55556-127">Die Anwendungs definierte Funktion im folgenden C++-Codebeispiel gibt den Index des Arbeitsbereichs zurück, zu dem das Element gehört.</span><span class="sxs-lookup"><span data-stu-id="55556-127">The application-defined function in the following C++ code example returns the index of the working area to which the item belongs.</span></span> <span data-ttu-id="55556-128">Wenn die Funktion fehlschlägt, wird – 1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="55556-128">If the function fails, it returns –1.</span></span> <span data-ttu-id="55556-129">Wenn die Funktion erfolgreich ausgeführt wird, das Element aber nicht in einem der Arbeitsbereiche vorhanden ist, gibt die Funktion 0 zurück, da alle Elemente, die sich nicht in einem Arbeitsbereich befinden, automatisch zu einem Member des Arbeitsbereichs NULL werden.</span><span class="sxs-lookup"><span data-stu-id="55556-129">If the function succeeds, but the item is not inside any of the working areas, the function returns 0, because all items that are not inside a working area automatically become a member of working area zero.</span></span>


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a><span data-ttu-id="55556-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55556-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55556-131">Listenansicht-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="55556-131">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="55556-132">Informationen zu List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="55556-132">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="55556-133">Verwenden von List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="55556-133">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





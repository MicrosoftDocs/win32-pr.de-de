---
title: Vorgehensweise beim Verwenden von Gruppen in einer List-View
description: In diesem Thema wird beschrieben, wie eine Instanz einer Gruppe erstellt und einem Listenansicht-Steuerelement hinzugefügt wird.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858557"
---
# <a name="how-to-use-groups-in-a-list-view"></a><span data-ttu-id="ec7d3-103">Vorgehensweise beim Verwenden von Gruppen in einer List-View</span><span class="sxs-lookup"><span data-stu-id="ec7d3-103">How to Use Groups in a List-View</span></span>

<span data-ttu-id="ec7d3-104">In diesem Thema wird beschrieben, wie eine Instanz einer Gruppe erstellt und einem Listenansicht-Steuerelement hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ec7d3-104">This topic describes how to create an instance of a group and add it to a list-view control.</span></span> <span data-ttu-id="ec7d3-105">Mithilfe von Gruppierungen kann ein Benutzer Listen in Gruppen von Elementen anordnen, die mithilfe eines horizontalen unter Teilers und eines Gruppen Titels visuell auf der Seite aufgeteilt sind.</span><span class="sxs-lookup"><span data-stu-id="ec7d3-105">Grouping allows a user to arrange lists into groups of items that are visually divided on the page, using a horizontal divider and a group title.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ec7d3-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="ec7d3-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ec7d3-107">Technologien</span><span class="sxs-lookup"><span data-stu-id="ec7d3-107">Technologies</span></span>

-   [<span data-ttu-id="ec7d3-108">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="ec7d3-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ec7d3-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ec7d3-109">Prerequisites</span></span>

-   <span data-ttu-id="ec7d3-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="ec7d3-110">C/C++</span></span>
-   <span data-ttu-id="ec7d3-111">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="ec7d3-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ec7d3-112">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="ec7d3-112">Instructions</span></span>


<span data-ttu-id="ec7d3-113">Um Gruppen in einem Listenansicht-Steuerelement zu verwenden, stellen Sie sicher, dass das Steuerelement den [**LVS \_ AlignTop**](list-view-window-styles.md) -Fenster Stil enthält.</span><span class="sxs-lookup"><span data-stu-id="ec7d3-113">To use groups in a list-view control, ensure that the control includes the [**LVS\_ALIGNTOP**](list-view-window-styles.md) window style.</span></span>

<span data-ttu-id="ec7d3-114">Wenn Sie der Liste ein Element hinzufügen, weisen Sie es einer Gruppe zu, indem Sie den **igroupid** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur des Elements auf den Wert des **igroupid** -Members der Struktur der [**Gruppe "LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="ec7d3-114">When you add an item to the list, you assign it to a group by setting the **iGroupId** member of the item's [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the value of the **iGroupId** member of the groups's [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure.</span></span> <span data-ttu-id="ec7d3-115">Ein Element, das keiner Gruppe zugewiesen ist, wird nicht in der Liste angezeigt, wenn die Gruppenansicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ec7d3-115">An item that is not assigned to a group does not appear in the list when group view is enabled.</span></span> <span data-ttu-id="ec7d3-116">Verwenden Sie das [**ListView \_ enablegroupview**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) -Makro, um die Gruppenansicht zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ec7d3-116">To enable or disable group view, use the [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) macro.</span></span>

<span data-ttu-id="ec7d3-117">Im folgenden Beispiel wird gezeigt, wie eine Gruppe mit einem Header erstellt und einem Listenansicht-Steuerelement hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ec7d3-117">The following example shows how to create a group with a header and add it to a list-view control.</span></span>


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a><span data-ttu-id="ec7d3-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec7d3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec7d3-119">Listenansicht-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="ec7d3-119">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ec7d3-120">Informationen zu List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="ec7d3-120">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="ec7d3-121">Verwenden von List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="ec7d3-121">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





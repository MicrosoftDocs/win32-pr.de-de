---
title: StatusBar-Steuer Element (MSAA UI-Element Referenz)
description: In Status leisten werden Statusinformationen in einem horizontalen Fenster am unteren Rand eines Anwendungsfensters angezeigt.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311202"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a><span data-ttu-id="a7012-103">StatusBar-Steuer Element (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="a7012-103">Status Bar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="a7012-104">In diesem Thema werden **StatusBar-Steuer** Element Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a7012-104">This topic describes **Status Bar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="a7012-105">Das Erstellen von **StatusBar-Steuer** Element Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a7012-105">How to create **Status Bar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="a7012-106">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="a7012-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="a7012-107">In Status leisten werden Statusinformationen in einem horizontalen Fenster am unteren Rand eines Anwendungsfensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a7012-107">Status bars display status information in a horizontal window at the bottom of an application window.</span></span> <span data-ttu-id="a7012-108">Status leisten sind häufig in Teile unterteilt, die als Bereiche bezeichnet werden, und in jedem Bereich werden andere Statusinformationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a7012-108">Status bars are often divided into parts, called panes, and each pane displays different status information.</span></span> <span data-ttu-id="a7012-109">Außerdem können Status leisten Objekte unterschiedlicher Typen enthalten, einschließlich Schaltflächen und Status leisten.</span><span class="sxs-lookup"><span data-stu-id="a7012-109">Additionally, status bars can contain objects of different types, including buttons and progress bars.</span></span> <span data-ttu-id="a7012-110">Der Fenster Klassenname für ein StatusBar-Steuerelement ist statusclassname, das in der Datei "kommctrl. h" als "msctls \_ statusbar32" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a7012-110">The window class name for a status bar control is STATUSCLASSNAME, which is defined as "msctls\_statusbar32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="a7012-111">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="a7012-111">IAccessible Methods</span></span>

<span data-ttu-id="a7012-112">Status leisten unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="a7012-112">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="a7012-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="a7012-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="a7012-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="a7012-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="a7012-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="a7012-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="a7012-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="a7012-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="a7012-117">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7012-117">IAccessible Properties</span></span>

<span data-ttu-id="a7012-118">Status leisten unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a7012-118">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="a7012-119">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a7012-119">Property</span></span>                                                                 | <span data-ttu-id="a7012-120">Kommentare</span><span class="sxs-lookup"><span data-stu-id="a7012-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7012-121">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="a7012-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="a7012-122">Die **childCount** -Eigenschaft ist die Anzahl der Bereiche in der Statusleiste.</span><span class="sxs-lookup"><span data-stu-id="a7012-122">The **ChildCount** property is the number of panes in the status bar.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a7012-123">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="a7012-123">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a7012-124">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="a7012-124">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="a7012-125">Das StatusBar-Objekt selbst hat keine **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a7012-125">The status bar object itself does not have a **Name** property.</span></span> <span data-ttu-id="a7012-126">Die **Name** -Eigenschaft jedes Bereichs in der Statusleiste ist mit dem angezeigten Text identisch.</span><span class="sxs-lookup"><span data-stu-id="a7012-126">The **Name** property of each pane in the status bar is the same as the displayed text.</span></span>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="a7012-127">**\_accParent erhalten**</span><span class="sxs-lookup"><span data-stu-id="a7012-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="a7012-128">Die **Parent** -Eigenschaft des StatusBar-Objekts ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und denselben Fenster Klassennamen wie das Steuerelement aufweist.</span><span class="sxs-lookup"><span data-stu-id="a7012-128">The **Parent** property of the status bar object is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span> <span data-ttu-id="a7012-129">Die über **geordnete** Eigenschaft der Bereiche in der Statusleiste ist das StatusBar-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a7012-129">The **Parent** property of the panes in the status bar is the status bar object.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="a7012-130">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="a7012-130">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="a7012-131">Die **Role** -Eigenschaft für das StatusBar-Objekt selbst ist [**role \_ System \_ StatusBar**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a7012-131">The **Role** property for the status bar object itself is [**ROLE\_SYSTEM\_STATUSBAR**](object-roles.md).</span></span> <span data-ttu-id="a7012-132">Der in einer Statusleiste angezeigte Text verfügt über das [**role \_ System \_ StaticText**](object-roles.md) als seine **Role** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a7012-132">The text displayed in a status bar has [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md) as its **Role** property.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="a7012-133">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="a7012-133">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="a7012-134">Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a7012-134">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="a7012-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7012-135">Notes</span></span>

<span data-ttu-id="a7012-136">Da Tastenkombinationen für StatusBar-Steuerelemente oder Textbereiche in Status leisten nicht unterstützt werden, wird " [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) " nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a7012-136">Because keyboard shortcuts are not supported for status bar controls or text areas on status bars, [**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) is not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7012-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a7012-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7012-138">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a7012-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 






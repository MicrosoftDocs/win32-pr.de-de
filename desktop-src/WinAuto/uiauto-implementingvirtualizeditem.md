---
title: VirtualizedItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IVirtualizedItemProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des VirtualizedItem-Steuerelement Musters
- UI-Automatisierung, VirtualizedItem-Steuerelement Muster
- UI-Automatisierung, IVirtualizedItemProvider
- IVirtualizedItemProvider
- Implementieren von VirtualizedItem-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- VirtualizedItem-Steuerelement Muster
- Steuerelement Muster, IVirtualizedItemProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-VirtualizedItem
- Steuerelement Muster, VirtualizedItem
- Schnittstellen, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207426"
---
# <a name="virtualizeditem-control-pattern"></a><span data-ttu-id="abd34-113">VirtualizedItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="abd34-113">VirtualizedItem Control Pattern</span></span>

<span data-ttu-id="abd34-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="abd34-114">Describes guidelines and conventions for implementing [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), including information about properties and methods.</span></span> <span data-ttu-id="abd34-115">Das **VirtualizedItem** -Steuerelement Muster wird zur Unterstützung von virtualisierten Elementen verwendet, bei denen es sich um Elemente handelt, die durch Platzhalter-Automatisierungselemente in der Microsoft UI Automation-Struktur dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="abd34-115">The **VirtualizedItem** control pattern is used to support virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.</span></span>

<span data-ttu-id="abd34-116">Virtualisierte Elemente können Elemente enthalten, die von einem Steuerelement abgerufen werden, das das [ItemContainer](uiauto-implementingitemcontainer.md) -Steuerelement Muster unterstützt, oder ein virtualisiertes eingebettetes Objekt, das von einem Steuerelement abgerufen wird, das das [Text](uiauto-implementingtextandtextrange.md) -</span><span class="sxs-lookup"><span data-stu-id="abd34-116">Virtualized items can include items retrieved from a control that supports the [ItemContainer](uiauto-implementingitemcontainer.md) control pattern, or a virtualized embedded object retrieved from a control that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span> <span data-ttu-id="abd34-117">Der Platzhalter für ein virtualisiertes Element hat möglicherweise keine Daten für alle Benutzeroberflächenautomatisierungs-Eigenschaften geladen und gibt [**ggf. UIA \_ E \_ elementnotavailable**](uiauto-error-codes.md) als Reaktion auf Abfragen von Eigenschaften zurück, die nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="abd34-117">The placeholder for a virtualized item might not have loaded data for all UI Automation properties, and may return [**UIA\_E\_ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) in response to queries for properties that are not available.</span></span> <span data-ttu-id="abd34-118">Das **VirtualizedItem** -Steuerelement Muster bietet eine Methode zum Erkennen eines virtuellen Elements, sodass vollständige Informationen für das Element verfügbar gemacht werden und ein vollständiges Automation-Element für das Element in der Benutzeroberflächenautomatisierungs-Struktur erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="abd34-118">The **VirtualizedItem** control pattern provides a method for realizing a virtual item so that full information is made available for the item, and a full automation element can be created for the item in the UI Automation tree.</span></span>

<span data-ttu-id="abd34-119">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="abd34-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="abd34-120">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="abd34-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="abd34-121">Erforderliche Member für **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="abd34-121">Required Members for **IVirtualizedItemProvider**</span></span>](#required-members-for-ivirtualizeditemprovider)
-   [<span data-ttu-id="abd34-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="abd34-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="abd34-123">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="abd34-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="abd34-124">Beachten Sie beim Implementieren des **VirtualizedItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="abd34-124">When implementing the **VirtualizedItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="abd34-125">Alle Benutzeroberflächen-Automatisierungs Platzhalter Elemente, die virtualisiert werden können, müssen das **VirtualizedItem** -Steuerelement Muster unterstützen, indem die [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) -Schnittstelle verfügbar gemacht wird</span><span class="sxs-lookup"><span data-stu-id="abd34-125">Any UI Automation placeholder element that can be virtualized must support the **VirtualizedItem** control pattern by exposing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>
-   <span data-ttu-id="abd34-126">Wenn [**IVirtualizedItemProvider:: merkt**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) aufgerufen wird, muss das Platzhalter Objekt mit vollständigen Implementierungen seiner Eigenschaften und Steuerelement Muster aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="abd34-126">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the placeholder object must be updated with full implementations of its properties and control patterns.</span></span>
-   <span data-ttu-id="abd34-127">Wenn [**IVirtualizedItemProvider:: merkt**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) aufgerufen wird, kann der Anbieter den Viewport so ändern, dass das virtualisierte Element in der Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abd34-127">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the provider can change the viewport so that the virtualized item comes into view.</span></span> <span data-ttu-id="abd34-128">Das Element in die Ansicht zu bringen, ist nicht erforderlich. nicht virtualisierte Elemente, die auf dem Bildschirm angezeigt werden, sollten jedoch die [**IScrollItemProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) -Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="abd34-128">Bringing the item into view is not required; however, off-screen, non-virtualized items should support the [**IScrollItemProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) method.</span></span>

## <a name="required-members-for-ivirtualizeditemprovider"></a><span data-ttu-id="abd34-129">Erforderliche Member für **IVirtualizedItemProvider**</span><span class="sxs-lookup"><span data-stu-id="abd34-129">Required Members for **IVirtualizedItemProvider**</span></span>

<span data-ttu-id="abd34-130">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abd34-130">The following properties and methods are required for implementing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>



| <span data-ttu-id="abd34-131">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="abd34-131">Required members</span></span>                                           | <span data-ttu-id="abd34-132">Memberart</span><span class="sxs-lookup"><span data-stu-id="abd34-132">Member type</span></span> | <span data-ttu-id="abd34-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="abd34-133">Notes</span></span> |
|------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="abd34-134">**Erkannten**</span><span class="sxs-lookup"><span data-stu-id="abd34-134">**Realize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | <span data-ttu-id="abd34-135">Methode</span><span class="sxs-lookup"><span data-stu-id="abd34-135">Method</span></span>      | <span data-ttu-id="abd34-136">Keine</span><span class="sxs-lookup"><span data-stu-id="abd34-136">None</span></span>  |



 

<span data-ttu-id="abd34-137">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="abd34-137">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abd34-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="abd34-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abd34-139">Implementieren des ItemContainer-Steuerelement Musters der Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="abd34-139">Implementing the UI Automation ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
</dt> <dt>

[<span data-ttu-id="abd34-140">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="abd34-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="abd34-141">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="abd34-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="abd34-142">Arbeiten mit virtualisierten Elementen</span><span class="sxs-lookup"><span data-stu-id="abd34-142">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 





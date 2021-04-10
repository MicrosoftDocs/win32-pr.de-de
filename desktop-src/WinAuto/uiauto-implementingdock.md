---
title: Dock-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IDockProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Dock-Steuerelement Muster wird verwendet, um die Andock Eigenschaften eines Steuer Elements in einem Docking Container verfügbar zu machen.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Benutzeroberflächenautomatisierung, Implementieren des Dock-Steuerelement Musters
- Benutzeroberflächenautomatisierungs, Dock-Steuerelement Muster
- UI-Automatisierung, IDockProvider
- IDockProvider
- Implementieren von Dock-Steuerungs Mustern für Benutzeroberflächen Automatisierung
- Dock-Steuerelement Muster
- Steuerelement Muster, IDockProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Dock
- Steuerelement Muster, Andocken
- Schnittstellen, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855991"
---
# <a name="dock-control-pattern"></a><span data-ttu-id="18eca-114">Dock-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="18eca-114">Dock Control Pattern</span></span>

<span data-ttu-id="18eca-115">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="18eca-115">Describes guidelines and conventions for implementing [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), including information about properties and methods.</span></span> <span data-ttu-id="18eca-116">Das **Dock** -Steuerelement Muster wird verwendet, um die Andock Eigenschaften eines Steuer Elements in einem Docking Container verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="18eca-116">The **Dock** control pattern is used to expose the dock properties of a control within a docking container.</span></span>

<span data-ttu-id="18eca-117">Ein Dockingcontainer ist ein Steuerelement, mit dem untergeordnete Elemente horizontal oder vertikal zueinander ausgerichtet werden können.</span><span class="sxs-lookup"><span data-stu-id="18eca-117">A docking container is a control that allows you to arrange child elements horizontally and vertically, relative to each other.</span></span> <span data-ttu-id="18eca-118">Die folgende Abbildung zeigt einen Docking Container mit zwei untergeordneten Elementen.</span><span class="sxs-lookup"><span data-stu-id="18eca-118">The following image shows a docking container with two child elements.</span></span> <span data-ttu-id="18eca-119">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="18eca-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![Screenshot des Docking Containers mit zwei angedockten untergeordneten Elementen](images/dockxmpl.jpg)

<span data-ttu-id="18eca-121">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="18eca-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="18eca-122">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="18eca-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="18eca-123">Erforderliche Member für **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="18eca-123">Required Members for **IDockProvider**</span></span>](#required-members-for-idockprovider)
-   [<span data-ttu-id="18eca-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18eca-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="18eca-125">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="18eca-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="18eca-126">Beachten Sie beim Implementieren des **Dock** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="18eca-126">When implementing the **Dock** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="18eca-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) macht keine Eigenschaften des Docking Containers oder Eigenschaften von Steuerelementen verfügbar, die neben dem aktuellen Steuerelement im Docking Container angedockt sind.</span><span class="sxs-lookup"><span data-stu-id="18eca-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) does not expose any properties of the docking container or any properties of controls that are docked adjacent to the current control within the docking container.</span></span>
-   <span data-ttu-id="18eca-128">Steuerelemente werden relativ zueinander entsprechend ihrer aktuellen z-Reihenfolge angeordnet. Je höher ihre z-Reihenfolgenposition ist, desto weiter entfernt vom angegebenen Rand des Dockingcontainers werden sie platziert.</span><span class="sxs-lookup"><span data-stu-id="18eca-128">Controls are docked relative to each other based on their current z-order; the higher their z-order placement, the farther they are placed from the specified edge of the docking container.</span></span>
-   <span data-ttu-id="18eca-129">Wenn die Größe des Dockingcontainers geändert wird, werden alle angedockten Steuerelemente im Container bündig zu derselben Kante neu positioniert, an der sie ursprünglich angedockt waren.</span><span class="sxs-lookup"><span data-stu-id="18eca-129">If the docking container is resized, any docked controls within the container will be repositioned flush to the same edge to which they were originally docked.</span></span> <span data-ttu-id="18eca-130">Die Größe der angedockten Steuerelemente wird ebenfalls geändert, um den Platz innerhalb des Containers entsprechend dem Andock Verhalten Ihrer [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) -Eigenschaft auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="18eca-130">The docked controls will also resize to fill any space within the container according to the docking behavior of their [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) property.</span></span> <span data-ttu-id="18eca-131">Wenn z. b. **DockPosition \_ Top** angegeben ist, werden die linke und die Rechte Seite des Steuer Elements erweitert, um den verfügbaren Platz auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="18eca-131">For example, if **DockPosition\_Top** is specified, the left and right sides of the control will expand to fill any available space.</span></span> <span data-ttu-id="18eca-132">Wenn **DockPosition \_ Fill** angegeben ist, werden alle vier Seiten des Steuer Elements erweitert, um den verfügbaren Platz auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="18eca-132">If **DockPosition\_Fill** is specified, all four sides of the control will expand to fill any available space.</span></span>
-   <span data-ttu-id="18eca-133">Auf einem System mit mehreren Bildschirmen sollten Steuerelemente auf der linken oder rechten Seite des aktuellen Bildschirms andocken.</span><span class="sxs-lookup"><span data-stu-id="18eca-133">On a multi-monitor system, controls should dock to the left or right side of the current monitor.</span></span> <span data-ttu-id="18eca-134">Ist dies nicht möglich, sollten sie auf der linken Seite des am weitesten links stehenden Bildschirms bzw. auf der rechten Seite des am weitesten rechts stehenden Bildschirms angedockt werden.</span><span class="sxs-lookup"><span data-stu-id="18eca-134">If that is not possible, they should dock to the left side of the leftmost monitor or the right side of the rightmost monitor.</span></span>

## <a name="required-members-for-idockprovider"></a><span data-ttu-id="18eca-135">Erforderliche Member für **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="18eca-135">Required Members for **IDockProvider**</span></span>

<span data-ttu-id="18eca-136">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="18eca-136">The following properties and methods are required for implementing the [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) interface.</span></span>



| <span data-ttu-id="18eca-137">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="18eca-137">Required members</span></span>                                                | <span data-ttu-id="18eca-138">Memberart</span><span class="sxs-lookup"><span data-stu-id="18eca-138">Member type</span></span> | <span data-ttu-id="18eca-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18eca-139">Notes</span></span> |
|-----------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="18eca-140">**Dock Position**</span><span class="sxs-lookup"><span data-stu-id="18eca-140">**DockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | <span data-ttu-id="18eca-141">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="18eca-141">Property</span></span>    | <span data-ttu-id="18eca-142">Keine</span><span class="sxs-lookup"><span data-stu-id="18eca-142">None</span></span>  |
| [<span data-ttu-id="18eca-143">**SetDockPosition**</span><span class="sxs-lookup"><span data-stu-id="18eca-143">**SetDockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | <span data-ttu-id="18eca-144">Methode</span><span class="sxs-lookup"><span data-stu-id="18eca-144">Method</span></span>      | <span data-ttu-id="18eca-145">Keine</span><span class="sxs-lookup"><span data-stu-id="18eca-145">None</span></span>  |



 

<span data-ttu-id="18eca-146">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="18eca-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18eca-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18eca-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18eca-148">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="18eca-148">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="18eca-149">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="18eca-149">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="18eca-150">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="18eca-150">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 





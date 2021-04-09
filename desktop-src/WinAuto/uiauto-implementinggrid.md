---
title: Raster-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IGridProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Raster-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von untergeordneten Elementen fungieren.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Raster Steuerelement Musters
- UI-Automatisierung, Raster-Steuerelement Muster
- UI-Automatisierung, IGridProvider
- IGridProvider
- Implementieren von Raster Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Raster Steuerelement Muster
- Steuerelement Muster, IGridProvider
- Steuerelement Muster, Implementieren des UI-Automatisierungs Rasters
- Steuerelement Muster, Raster
- Schnittstellen, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036725"
---
# <a name="grid-control-pattern"></a><span data-ttu-id="07cf8-114">Raster-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="07cf8-114">Grid Control Pattern</span></span>

<span data-ttu-id="07cf8-115">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="07cf8-115">Describes guidelines and conventions for implementing [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), including information about properties and methods.</span></span> <span data-ttu-id="07cf8-116">Das **Raster** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von untergeordneten Elementen fungieren.</span><span class="sxs-lookup"><span data-stu-id="07cf8-116">The **Grid** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="07cf8-117">Die untergeordneten Elemente dieses Elements müssen [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) implementieren und in einem zweidimensionalen logischen Koordinatensystem angeordnet sein, das Zeilen-und spaltenweise durchlaufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="07cf8-117">The children of this element must implement [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="07cf8-118">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="07cf8-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="07cf8-119">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="07cf8-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="07cf8-120">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="07cf8-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="07cf8-121">Erforderliche Member für **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="07cf8-121">Required Members for **IGridProvider**</span></span>](#required-members-for-igridprovider)
-   [<span data-ttu-id="07cf8-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07cf8-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="07cf8-123">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="07cf8-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="07cf8-124">Beachten Sie beim Implementieren des **Grid** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="07cf8-124">When implementing the **Grid** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="07cf8-125">Raster Koordinaten sind NULL basiert, wobei die obere linke Zelle (oder die obere rechte Zelle, je nach Gebiets Schema) die Koordinaten (0,0) aufweist.</span><span class="sxs-lookup"><span data-stu-id="07cf8-125">Grid coordinates are zero-based with the upper left (or upper right cell depending on locale) having coordinates (0,0).</span></span>
-   <span data-ttu-id="07cf8-126">Wenn eine Zelle leer ist, muss ein Microsoft UI Automation-Element zurückgegeben werden, um die [**IGridItemProvider:: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) -Eigenschaft für diese Zelle zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="07cf8-126">If a cell is empty, a Microsoft UI Automation element must still be returned in order to support the [**IGridItemProvider::ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) property for that cell.</span></span> <span data-ttu-id="07cf8-127">Dies ist möglich, wenn das Layout von untergeordneten Elementen im Raster dem eines unregelmäßigen Arrays entspricht (siehe folgendes Beispiel).</span><span class="sxs-lookup"><span data-stu-id="07cf8-127">This is possible when the layout of child elements in the grid is similar to a ragged array (see example below).</span></span>

    ![Beispiel für ein Grid-Steuerelement mit leeren Koordinaten](images/grid.png)

-   <span data-ttu-id="07cf8-129">Ein Raster mit einem einzelnen Element ist nach wie vor erforderlich, um [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) zu implementieren, wenn es logisch als Raster angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="07cf8-129">A grid with a single item is still required to implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) if it is logically considered to be a grid.</span></span> <span data-ttu-id="07cf8-130">Die Anzahl untergeordneter Elemente im Raster ist unwesentlich.</span><span class="sxs-lookup"><span data-stu-id="07cf8-130">The number of child items in the grid is immaterial.</span></span>
-   <span data-ttu-id="07cf8-131">Ausgeblendete Zeilen und Spalten können abhängig von der Implementierung des Anbieters in der Benutzeroberflächenautomatisierungs-Struktur geladen werden und werden daher in den Eigenschaften [**IGridProvider:: ROWCOUNT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) und [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="07cf8-131">Hidden rows and columns, depending on the provider implementation, may be loaded in the UI Automation tree and will therefore be reflected in the [**IGridProvider::RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) and [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) properties.</span></span> <span data-ttu-id="07cf8-132">Wenn die ausgeblendeten Zeilen und Spalten noch nicht geladen wurden, sollten sie nicht gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="07cf8-132">If the hidden rows and columns have not yet been loaded, they should not be counted.</span></span>
-   <span data-ttu-id="07cf8-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) ermöglicht keine aktive Bearbeitung eines Rasters. [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) muss implementiert werden, um diese Funktionalität zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="07cf8-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not enable active manipulation of a grid; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) must be implemented to enable this functionality.</span></span>
-   <span data-ttu-id="07cf8-134">Verwenden Sie einen [**iuiautomationstructurechangedebug-thandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) zum lauschen auf Struktur-oder Layoutänderungen am Raster, z. b. Zellen, die hinzugefügt, entfernt oder zusammengeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="07cf8-134">Use a [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) to listen for structural or layout changes to the grid such as cells that have been added, removed, or merged.</span></span>
-   <span data-ttu-id="07cf8-135">Verwenden Sie einen [**iuiautomationfocuschangedebug-thandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) , um den Durchlauf durch die Elemente oder Zellen eines Rasters zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="07cf8-135">Use a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) to track traversal through the items or cells of a grid.</span></span>

## <a name="required-members-for-igridprovider"></a><span data-ttu-id="07cf8-136">Erforderliche Member für **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="07cf8-136">Required Members for **IGridProvider**</span></span>

<span data-ttu-id="07cf8-137">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="07cf8-137">The following properties and methods are required for implementing the [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) interface.</span></span>



| <span data-ttu-id="07cf8-138">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="07cf8-138">Required members</span></span>                                        | <span data-ttu-id="07cf8-139">Memberart</span><span class="sxs-lookup"><span data-stu-id="07cf8-139">Member type</span></span> | <span data-ttu-id="07cf8-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="07cf8-140">Notes</span></span> |
|---------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="07cf8-141">**RowCount**</span><span class="sxs-lookup"><span data-stu-id="07cf8-141">**RowCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | <span data-ttu-id="07cf8-142">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07cf8-142">Property</span></span>    | <span data-ttu-id="07cf8-143">Keine</span><span class="sxs-lookup"><span data-stu-id="07cf8-143">None</span></span>  |
| [<span data-ttu-id="07cf8-144">**ColumnCount**</span><span class="sxs-lookup"><span data-stu-id="07cf8-144">**ColumnCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | <span data-ttu-id="07cf8-145">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="07cf8-145">Property</span></span>    | <span data-ttu-id="07cf8-146">Keine</span><span class="sxs-lookup"><span data-stu-id="07cf8-146">None</span></span>  |
| [<span data-ttu-id="07cf8-147">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="07cf8-147">**GetItem**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | <span data-ttu-id="07cf8-148">Methode</span><span class="sxs-lookup"><span data-stu-id="07cf8-148">Method</span></span>      | <span data-ttu-id="07cf8-149">Keine</span><span class="sxs-lookup"><span data-stu-id="07cf8-149">None</span></span>  |



 

<span data-ttu-id="07cf8-150">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="07cf8-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07cf8-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07cf8-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07cf8-152">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="07cf8-152">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="07cf8-153">GridItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="07cf8-153">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
</dt> <dt>

[<span data-ttu-id="07cf8-154">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="07cf8-154">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="07cf8-155">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="07cf8-155">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 





---
title: GridItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IGridItemProvider, einschließlich Informationen zu Eigenschaften. Das GridItem-Steuerelement Muster wird verwendet, um einzelne untergeordnete Steuerelemente von Containern zu unterstützen, die IGridProvider implementieren.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des GridItem-Steuerelement Musters
- UI-Automatisierung, GridItem-Steuerelement Muster
- UI-Automatisierung, IGridItemProvider
- IGridItemProvider
- Implementieren von GridItem-Steuerelement Mustern für Benutzeroberflächen
- GridItem-Steuerelement Muster
- Steuerelement Muster, IGridItemProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-GridItem
- Steuerelement Muster, GridItem
- Schnittstellen, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709695"
---
# <a name="griditem-control-pattern"></a><span data-ttu-id="50367-114">GridItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="50367-114">GridItem Control Pattern</span></span>

<span data-ttu-id="50367-115">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), einschließlich Informationen zu Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="50367-115">Describes guidelines and conventions for implementing [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), including information about properties.</span></span> <span data-ttu-id="50367-116">Das **GridItem** -Steuerelement Muster wird verwendet, um einzelne untergeordnete Steuerelemente von Containern zu unterstützen, die [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)implementieren.</span><span class="sxs-lookup"><span data-stu-id="50367-116">The **GridItem** control pattern is used to support individual child controls of containers that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>

<span data-ttu-id="50367-117">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="50367-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="50367-118">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="50367-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="50367-119">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="50367-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="50367-120">Erforderliche Member für **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="50367-120">Required Members for **IGridItemProvider**</span></span>](#required-members-for-igriditemprovider)
-   [<span data-ttu-id="50367-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50367-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="50367-122">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="50367-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="50367-123">Beachten Sie beim Implementieren des **GridItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="50367-123">When implementing the **GridItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="50367-124">Rasterkoordinaten (Grid-Koordinaten) sind nullbasiert, wobei die obere linke Zelle die Koordinaten (0, 0) hat.</span><span class="sxs-lookup"><span data-stu-id="50367-124">Grid coordinates are zero-based with the upper left cell having coordinates (0, 0).</span></span>
-   <span data-ttu-id="50367-125">Zusammengeführte Zellen melden ihre [**Zeilen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) -und [**Spalten**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) Eigenschaften basierend auf Ihrer zugrunde liegenden Anker Zelle, wie vom Microsoft UI Automation Provider definiert.</span><span class="sxs-lookup"><span data-stu-id="50367-125">Merged cells will report their [**Row**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) and [**Column**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) properties based on their underlying anchor cell as defined by the Microsoft UI Automation provider.</span></span> <span data-ttu-id="50367-126">In der Regel sind dies die oberste Zeile und die am weitesten links liegende Spalte.</span><span class="sxs-lookup"><span data-stu-id="50367-126">Typically, it will be the topmost and leftmost row or column.</span></span>
-   <span data-ttu-id="50367-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) bietet keine aktive Bearbeitung des Rasters, wie z. b. das Zusammenführen oder aufteilen von Zellen.</span><span class="sxs-lookup"><span data-stu-id="50367-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not provide for active manipulation of the grid such as merging or splitting cells.</span></span>
-   <span data-ttu-id="50367-128">Steuerelemente, die [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) implementieren, können in der Regel mithilfe der Tastatur durchlaufen werden (d. h., ein Benutzeroberflächenautomatisierungs-Client kann zu benachbarten Steuerelementen wechseln).</span><span class="sxs-lookup"><span data-stu-id="50367-128">Controls that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) can typically be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.</span></span>

## <a name="required-members-for-igriditemprovider"></a><span data-ttu-id="50367-129">Erforderliche Member für **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="50367-129">Required Members for **IGridItemProvider**</span></span>

<span data-ttu-id="50367-130">Die folgenden Eigenschaften sind erforderlich, um die [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) -Schnittstelle zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="50367-130">The following properties are required for implementing the [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) interface.</span></span>



| <span data-ttu-id="50367-131">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="50367-131">Required members</span></span>                                                  | <span data-ttu-id="50367-132">Memberart</span><span class="sxs-lookup"><span data-stu-id="50367-132">Member type</span></span> | <span data-ttu-id="50367-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50367-133">Notes</span></span> |
|-------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="50367-134">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="50367-134">**Row**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | <span data-ttu-id="50367-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50367-135">Property</span></span>    | <span data-ttu-id="50367-136">Keine</span><span class="sxs-lookup"><span data-stu-id="50367-136">None</span></span>  |
| [<span data-ttu-id="50367-137">**Column**</span><span class="sxs-lookup"><span data-stu-id="50367-137">**Column**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | <span data-ttu-id="50367-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50367-138">Property</span></span>    | <span data-ttu-id="50367-139">Keine</span><span class="sxs-lookup"><span data-stu-id="50367-139">None</span></span>  |
| [<span data-ttu-id="50367-140">**RowSpan**</span><span class="sxs-lookup"><span data-stu-id="50367-140">**RowSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | <span data-ttu-id="50367-141">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50367-141">Property</span></span>    | <span data-ttu-id="50367-142">Keine</span><span class="sxs-lookup"><span data-stu-id="50367-142">None</span></span>  |
| [<span data-ttu-id="50367-143">**ColumnSpan**</span><span class="sxs-lookup"><span data-stu-id="50367-143">**ColumnSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | <span data-ttu-id="50367-144">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50367-144">Property</span></span>    | <span data-ttu-id="50367-145">Keine</span><span class="sxs-lookup"><span data-stu-id="50367-145">None</span></span>  |
| [<span data-ttu-id="50367-146">**ContainingGrid**</span><span class="sxs-lookup"><span data-stu-id="50367-146">**ContainingGrid**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | <span data-ttu-id="50367-147">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50367-147">Property</span></span>    | <span data-ttu-id="50367-148">Keine</span><span class="sxs-lookup"><span data-stu-id="50367-148">None</span></span>  |



 

<span data-ttu-id="50367-149">Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="50367-149">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50367-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50367-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50367-151">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="50367-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="50367-152">Raster-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="50367-152">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
</dt> <dt>

[<span data-ttu-id="50367-153">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="50367-153">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="50367-154">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="50367-154">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 





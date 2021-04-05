---
title: TableItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ITableItemProvider, einschließlich Informationen zu-Methoden. Das TableItem-Steuerelement Muster wird verwendet, um untergeordnete Steuerelemente von Containern zu unterstützen, die ITableProvider implementieren.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des TableItem-Steuerelement Musters
- UI-Automatisierung, TableItem-Steuerelement Muster
- UI-Automatisierung, ITableItemProvider
- ITableItemProvider
- Implementieren von TableItem-Steuerelement Mustern für Benutzeroberflächen
- TableItem-Steuerelement Muster
- Steuerelement Muster, ITableItemProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-TableItem
- Steuerelement Muster, TableItem
- Schnittstellen, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709276"
---
# <a name="tableitem-control-pattern"></a><span data-ttu-id="279ef-114">TableItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="279ef-114">TableItem Control Pattern</span></span>

<span data-ttu-id="279ef-115">Beschreibt Richtlinien und Konventionen für das Implementieren von [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), einschließlich Informationen zu-Methoden.</span><span class="sxs-lookup"><span data-stu-id="279ef-115">Describes guidelines and conventions for implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), including information about methods.</span></span> <span data-ttu-id="279ef-116">Das **TableItem** -Steuerelement Muster wird verwendet, um untergeordnete Steuerelemente von Containern zu unterstützen, die [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)implementieren.</span><span class="sxs-lookup"><span data-stu-id="279ef-116">The **TableItem** control pattern is used to support child controls of containers that implement [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span></span>

<span data-ttu-id="279ef-117">Der Zugriff auf die Funktionalität einzelner Zellen wird von der erforderlichen, gleichzeitigen Implementierung von [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="279ef-117">Access to individual cell functionality is provided by the required, concurrent implementation of [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span></span> <span data-ttu-id="279ef-118">Dieses Steuerelement Muster ist analog zu **IGridItemProvider** , wobei jedes Steuerelement, das [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) implementiert, die Beziehung zwischen der einzelnen Zelle und den zugehörigen Zeilen-und Spalten Informationen Programm gesteuert verfügbar machen muss.</span><span class="sxs-lookup"><span data-stu-id="279ef-118">This control pattern is analogous to **IGridItemProvider** with the distinction that any control implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) must programmatically expose the relationship between the individual cell and its row and column information.</span></span> <span data-ttu-id="279ef-119">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="279ef-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="279ef-120">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="279ef-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="279ef-121">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="279ef-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="279ef-122">Erforderliche Member für " **ITableItemProvider** "</span><span class="sxs-lookup"><span data-stu-id="279ef-122">Required Members for **ITableItemProvider**</span></span>](#required-members-for-itableitemprovider)
-   [<span data-ttu-id="279ef-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="279ef-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="279ef-124">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="279ef-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="279ef-125">Beachten Sie beim Implementieren des **TableItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="279ef-125">When implementing the **TableItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="279ef-126">Weitere Informationen zu verwandten Raster Elementen finden Sie unter [GridItem-Steuerelement Muster](uiauto-implementinggriditem.md).</span><span class="sxs-lookup"><span data-stu-id="279ef-126">For related grid item functionality, see [GridItem Control Pattern](uiauto-implementinggriditem.md).</span></span>

## <a name="required-members-for-itableitemprovider"></a><span data-ttu-id="279ef-127">Erforderliche Member für " **ITableItemProvider** "</span><span class="sxs-lookup"><span data-stu-id="279ef-127">Required Members for **ITableItemProvider**</span></span>

<span data-ttu-id="279ef-128">Die folgenden Methoden sind erforderlich, um die [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) -Schnittstelle zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="279ef-128">The following methods are required for implementing the [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) interface.</span></span>



| <span data-ttu-id="279ef-129">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="279ef-129">Required members</span></span>                                                               | <span data-ttu-id="279ef-130">Memberart</span><span class="sxs-lookup"><span data-stu-id="279ef-130">Member type</span></span> | <span data-ttu-id="279ef-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="279ef-131">Notes</span></span> |
|--------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="279ef-132">**GetColumnHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="279ef-132">**GetColumnHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | <span data-ttu-id="279ef-133">Methode</span><span class="sxs-lookup"><span data-stu-id="279ef-133">Method</span></span>      | <span data-ttu-id="279ef-134">Keine</span><span class="sxs-lookup"><span data-stu-id="279ef-134">None</span></span>  |
| [<span data-ttu-id="279ef-135">**GetRowHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="279ef-135">**GetRowHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | <span data-ttu-id="279ef-136">Methode</span><span class="sxs-lookup"><span data-stu-id="279ef-136">Method</span></span>      | <span data-ttu-id="279ef-137">Keine</span><span class="sxs-lookup"><span data-stu-id="279ef-137">None</span></span>  |



 

<span data-ttu-id="279ef-138">Diesem Steuerelementmuster sind keine Eigenschaften oder Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="279ef-138">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="279ef-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="279ef-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="279ef-140">**Licher**</span><span class="sxs-lookup"><span data-stu-id="279ef-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="279ef-141">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="279ef-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="279ef-142">Table-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="279ef-142">Table Control Pattern</span></span>](uiauto-implementingtable.md)
</dt> <dt>

[<span data-ttu-id="279ef-143">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="279ef-143">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="279ef-144">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="279ef-144">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 





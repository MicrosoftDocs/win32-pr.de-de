---
title: Table-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ITableProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Table-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von untergeordneten Elementen fungieren.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Tabellen Steuerungs Musters
- UI-Automatisierung, Table-Steuerelement Muster
- UI-Automatisierung, ITableProvider
- ITableProvider
- Implementieren von Tabellen Steuerungs Mustern für Benutzeroberflächen Automatisierung
- Tabellen Steuerelement-Muster
- Steuerelement Muster, ITableProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Tabelle
- Steuerelement Muster, Tabelle
- Schnittstellen, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104562573"
---
# <a name="table-control-pattern"></a><span data-ttu-id="01ddc-114">Table-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="01ddc-114">Table Control Pattern</span></span>

<span data-ttu-id="01ddc-115">Beschreibt Richtlinien und Konventionen für das Implementieren von [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="01ddc-115">Describes guidelines and conventions for implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), including information about properties and methods.</span></span> <span data-ttu-id="01ddc-116">Das **Table** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von untergeordneten Elementen fungieren.</span><span class="sxs-lookup"><span data-stu-id="01ddc-116">The **Table** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="01ddc-117">Die untergeordneten Elemente des Container-Elements müssen [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) implementieren und in einem zweidimensionalen logischen Koordinatensystem angeordnet sein, das nach Zeilen und Spalten durchlaufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="01ddc-117">The children of the container element must implement [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="01ddc-118">Dieses Steuerelement Muster entspricht [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , wobei jedes Steuerelement, das [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) implementiert, auch für jedes untergeordnete Element eine Spalten-und/oder Zeilen Header Beziehung verfügbar machen muss.</span><span class="sxs-lookup"><span data-stu-id="01ddc-118">This control pattern is analogous to [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) with the distinction that any control implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) must also expose a column and/or row header relationship for each child element.</span></span> <span data-ttu-id="01ddc-119">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="01ddc-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="01ddc-120">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="01ddc-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="01ddc-121">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="01ddc-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="01ddc-122">Erforderliche Member für **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="01ddc-122">Required Members for **ITableProvider**</span></span>](#required-members-for-itableprovider)
-   [<span data-ttu-id="01ddc-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01ddc-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="01ddc-124">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="01ddc-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="01ddc-125">Beachten Sie beim Implementieren des **Table** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="01ddc-125">When implementing the **Table** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="01ddc-126">Der Zugriff auf den Inhalt einzelner Zellen erfolgt über ein zweidimensionales logisches Koordinatensystem oder ein Array, das von der erforderlichen, gleichzeitigen Implementierung von [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="01ddc-126">Access to the content of individual cells is through a two-dimensional logical coordinate system or array provided by the required, concurrent implementation of [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>
-   <span data-ttu-id="01ddc-127">Eine Spalten- oder Zeilenüberschrift kann in einem Tabellenobjekt enthalten sein oder ein separates Headerobjekt darstellen, das einem Tabellenobjekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="01ddc-127">A column or row header can be contained within a table object or be a separate header object that is associated with a table object.</span></span>
-   <span data-ttu-id="01ddc-128">Spalten- und Zeilenüberschriften können sowohl eine primäre als auch beliebige unterstützende Überschriften enthalten.</span><span class="sxs-lookup"><span data-stu-id="01ddc-128">Column and row headers may include both a primary header as well as any supporting headers.</span></span>
    > [!Note]  
    > <span data-ttu-id="01ddc-129">Dieses Konzept wird in einem Microsoft Excel-Arbeitsblatt ersichtlich, in dem ein Benutzer eine **Vorname** -Spalte definiert hat.</span><span class="sxs-lookup"><span data-stu-id="01ddc-129">This concept becomes evident in a Microsoft Excel spreadsheet where a user has defined a **First name** column.</span></span> <span data-ttu-id="01ddc-130">Diese Spalte verfügt jetzt über zwei Header, einschließlich des vom benutzerdefinierten **Vornamen** Headers und der alphanumerischen Bezeichnung für diese Spalte, die von der Anwendung zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="01ddc-130">This column now has two headers, including the **First name** header defined by the user, and the alphanumeric designation for that column assigned by the application.</span></span>

     

-   <span data-ttu-id="01ddc-131">Weitere Informationen finden Sie unter [Raster Steuerelement Muster](uiauto-implementinggrid.md) für Verwandte Raster Funktionen.</span><span class="sxs-lookup"><span data-stu-id="01ddc-131">See [Grid Control Pattern](uiauto-implementinggrid.md) for related grid functionality.</span></span>

    <span data-ttu-id="01ddc-132">Die folgende Abbildung zeigt eine Tabelle mit komplexen Spalten Headern.</span><span class="sxs-lookup"><span data-stu-id="01ddc-132">The following image shows a table with complex column headers.</span></span>

    ![Tabelle mit komplexen Spaltenüberschriften](images/uia-valuepattern-colorpicker.jpg)

    <span data-ttu-id="01ddc-134">Die folgende Abbildung zeigt eine Tabelle mit einer mehrdeutigen [**ITableProvider:: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="01ddc-134">The following image shows a table with an ambiguous [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) property.</span></span>

    ![Tabelle mit mehrdeutiger RowOrColumnMajor-Eigenschaft](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a><span data-ttu-id="01ddc-136">Erforderliche Member für **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="01ddc-136">Required Members for **ITableProvider**</span></span>

<span data-ttu-id="01ddc-137">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="01ddc-137">The following properties and methods are required for implementing the [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) interface.</span></span>



| <span data-ttu-id="01ddc-138">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="01ddc-138">Required members</span></span>                                                   | <span data-ttu-id="01ddc-139">Memberart</span><span class="sxs-lookup"><span data-stu-id="01ddc-139">Member type</span></span> | <span data-ttu-id="01ddc-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01ddc-140">Notes</span></span> |
|--------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="01ddc-141">**RowOrColumnMajor**</span><span class="sxs-lookup"><span data-stu-id="01ddc-141">**RowOrColumnMajor**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | <span data-ttu-id="01ddc-142">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="01ddc-142">Property</span></span>    | <span data-ttu-id="01ddc-143">Keine</span><span class="sxs-lookup"><span data-stu-id="01ddc-143">None</span></span>  |
| [<span data-ttu-id="01ddc-144">**GetColumnHeaders**</span><span class="sxs-lookup"><span data-stu-id="01ddc-144">**GetColumnHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | <span data-ttu-id="01ddc-145">Methode</span><span class="sxs-lookup"><span data-stu-id="01ddc-145">Method</span></span>      | <span data-ttu-id="01ddc-146">Keine</span><span class="sxs-lookup"><span data-stu-id="01ddc-146">None</span></span>  |
| [<span data-ttu-id="01ddc-147">**GetRowHeaders**</span><span class="sxs-lookup"><span data-stu-id="01ddc-147">**GetRowHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | <span data-ttu-id="01ddc-148">Methode</span><span class="sxs-lookup"><span data-stu-id="01ddc-148">Method</span></span>      | <span data-ttu-id="01ddc-149">Keine</span><span class="sxs-lookup"><span data-stu-id="01ddc-149">None</span></span>  |



 

<span data-ttu-id="01ddc-150">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="01ddc-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01ddc-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01ddc-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="01ddc-152">**Licher**</span><span class="sxs-lookup"><span data-stu-id="01ddc-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="01ddc-153">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="01ddc-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="01ddc-154">TableItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="01ddc-154">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
</dt> <dt>

[<span data-ttu-id="01ddc-155">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="01ddc-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="01ddc-156">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="01ddc-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 





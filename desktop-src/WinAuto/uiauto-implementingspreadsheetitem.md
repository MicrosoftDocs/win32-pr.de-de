---
title: Spreadsheetitem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ispreadsheetitemprovider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Benutzeroberflächenautomatisierung, Implementieren des spreadsheetitem-Steuerelement Musters
- UI-Automatisierung, spreadsheetitem-Steuerelement Muster
- UI-Automatisierung, ispreadsheetitemprovider
- ISpreadsheetItemProvider
- Implementieren des spreadsheetitem-Steuerelement Musters der Benutzeroberflächen Automatisierung
- Spreadsheetitem-Steuerelement Muster
- Steuerelement Muster, ispreadsheetitemprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Tabellen kalerischen Elemente
- Steuerelement Muster, spreadsheetitem
- Schnittstellen, ispreadsheetitemprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039478"
---
# <a name="spreadsheetitem-control-pattern"></a><span data-ttu-id="2b249-113">Spreadsheetitem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="2b249-113">SpreadsheetItem Control Pattern</span></span>

<span data-ttu-id="2b249-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**ispreadsheetitemprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="2b249-114">Describes guidelines and conventions for implementing [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), including information about properties and methods.</span></span> <span data-ttu-id="2b249-115">Das **spreadsheetitem** -Steuerelement Muster wird verwendet, um die Eigenschaften einer Zelle in einer Kalkulations Tabelle oder einem anderen Raster basierten Dokument verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2b249-115">The **SpreadsheetItem** control pattern is used to expose the properties of a cell in a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="2b249-116">Das **spreadsheetitem** -Steuerelement Muster ist eng mit dem [GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster verknüpft. Steuerelemente, die das **spreadsheetitem** -Steuerelement Muster implementieren, sollten auch das GridItem-Steuerelement Muster implementieren.</span><span class="sxs-lookup"><span data-stu-id="2b249-116">The **SpreadsheetItem** control pattern is closely related to the [GridItem](uiauto-implementinggriditem.md) control pattern; controls that implement the **SpreadsheetItem** control pattern should also implement the GridItem control pattern.</span></span> <span data-ttu-id="2b249-117">Steuerelemente können ggf. auch das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster implementieren.</span><span class="sxs-lookup"><span data-stu-id="2b249-117">Controls can also implement the [TableItem](uiauto-implementingtableitem.md) control pattern, if appropriate.</span></span> <span data-ttu-id="2b249-118">Beispiele für Steuerelemente, die diese Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="2b249-118">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="2b249-119">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="2b249-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2b249-120">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="2b249-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="2b249-121">Erforderliche Member für **ispreadsheetitemprovider**</span><span class="sxs-lookup"><span data-stu-id="2b249-121">Required Members for **ISpreadsheetItemProvider**</span></span>](#required-members-for-ispreadsheetitemprovider)
-   [<span data-ttu-id="2b249-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b249-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="2b249-123">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="2b249-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="2b249-124">Beachten Sie beim Implementieren des **spreadsheetitem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="2b249-124">When implementing the **SpreadsheetItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="2b249-125">Informationen zum Implementieren der [**ispreadsheetitemprovider:: getannotationobjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) -Methode und der [**ispreadsheetitemprovider:: getannotationtypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) -Methode finden Sie in der [**iannotationprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2b249-125">When implementing the [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) and [**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) methods, please refer to the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) documentation.</span></span> <span data-ttu-id="2b249-126">Diese Methoden geben Arrays zurück, damit Anbieter mehrere Anmerkungen in einer einzelnen Zelle unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="2b249-126">These methods both return arrays to enable providers to support multiple annotations on a single cell.</span></span>
-   <span data-ttu-id="2b249-127">Einige Arten von Anmerkungen erfordern keine vollständige Implementierung der [**iannotationprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2b249-127">Some kinds of annotations do not require a full implementation of the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) interface.</span></span> <span data-ttu-id="2b249-128">Ein einfacher Rechtschreibfehler Indikator könnte z. b. dargestellt werden, wenn [**getannotationtypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) einen Text Attribut Bezeichner von [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)zurückgibt und [**getannotationobjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) einen NULL-Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2b249-128">For example, a simple spelling-error indicator could be represented by having [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) return a text attribute identifier of [**AnnotationType\_SpellingError**](uiauto-annotation-type-identifiers.md), and having [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) return a null value.</span></span>

## <a name="required-members-for-ispreadsheetitemprovider"></a><span data-ttu-id="2b249-129">Erforderliche Member für **ispreadsheetitemprovider**</span><span class="sxs-lookup"><span data-stu-id="2b249-129">Required Members for **ISpreadsheetItemProvider**</span></span>

<span data-ttu-id="2b249-130">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ispreadsheetitemprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2b249-130">The following properties and methods are required for implementing the [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>



| <span data-ttu-id="2b249-131">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="2b249-131">Required members</span></span>                                                                         | <span data-ttu-id="2b249-132">Memberart</span><span class="sxs-lookup"><span data-stu-id="2b249-132">Member type</span></span> | <span data-ttu-id="2b249-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b249-133">Notes</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b249-134">**Formel**</span><span class="sxs-lookup"><span data-stu-id="2b249-134">**Formula**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | <span data-ttu-id="2b249-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2b249-135">Property</span></span>    | <span data-ttu-id="2b249-136">Das Implementieren einer separaten [**Formel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) Eigenschaft ist erforderlich, da die [value](value-property.md) -Eigenschaft einer Zelle in der Regel den berechneten Wert der Zelle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2b249-136">Implementing a separate [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) property is necessary because a cell’s [Value](value-property.md) property typically returns the computed value of the cell.</span></span> <span data-ttu-id="2b249-137">Die **Formel** Eigenschaft sollte **null** sein, wenn keine Formel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2b249-137">The **Formula** property should be **NULL** if no formula is set.</span></span> |
| [<span data-ttu-id="2b249-138">**Getannotationobjects**</span><span class="sxs-lookup"><span data-stu-id="2b249-138">**GetAnnotationObjects**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | <span data-ttu-id="2b249-139">Methode</span><span class="sxs-lookup"><span data-stu-id="2b249-139">Method</span></span>      | <span data-ttu-id="2b249-140">Gibt ein Array von Element Anbietern zurück, die auf die Anmerkungen verweisen, die mit dieser Zelle verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="2b249-140">Returns an array of element providers that refer to the annotations linked to this cell.</span></span> <span data-ttu-id="2b249-141">Zeiger innerhalb des Arrays können NULL sein, wenn eine Anmerkung keinen verknüpften Anbieter hat.</span><span class="sxs-lookup"><span data-stu-id="2b249-141">Pointers within the array can be null if an annotation does not have a linked provider.</span></span>                                                                                                       |
| [<span data-ttu-id="2b249-142">**Getannotationtypes**</span><span class="sxs-lookup"><span data-stu-id="2b249-142">**GetAnnotationTypes**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | <span data-ttu-id="2b249-143">Methode</span><span class="sxs-lookup"><span data-stu-id="2b249-143">Method</span></span>      | <span data-ttu-id="2b249-144">Gibt ein Array von Anmerkung-typbezeichaten zurück, die die Anmerkungen in dieser Zelle beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2b249-144">Returns an array of annotation type identifiers that describe the annotations on this cell.</span></span> <span data-ttu-id="2b249-145">Das Array muss dieselbe Größe aufweisen wie das Array, das von [**getannotationobjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2b249-145">The array must be the same size as the array returned by [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span></span>                                         |



 

<span data-ttu-id="2b249-146">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2b249-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b249-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b249-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2b249-148">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2b249-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2b249-149">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="2b249-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="2b249-150">Tabellen Steuerungs Muster</span><span class="sxs-lookup"><span data-stu-id="2b249-150">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
</dt> <dt>

[<span data-ttu-id="2b249-151">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="2b249-151">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="2b249-152">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="2b249-152">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 
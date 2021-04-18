---
title: RangeValue-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IRangeValueProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das RangeValue-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die auf einen Wert innerhalb eines Bereichs festgelegt werden können.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des RangeValue-Steuerelement Musters
- UI-Automatisierung, RangeValue-Steuerelement Muster
- Benutzeroberflächenautomatisierung, IRangeValueProvider
- IRangeValueProvider
- Implementieren von RangeValue-Steuerelement Mustern für Benutzeroberflächen
- RangeValue-Steuerelement Muster
- Steuerelement Muster, IRangeValueProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-RangeValue
- Steuerelement Muster, RangeValue
- Schnittstellen, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339214"
---
# <a name="rangevalue-control-pattern"></a><span data-ttu-id="7da15-114">RangeValue-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="7da15-114">RangeValue Control Pattern</span></span>

<span data-ttu-id="7da15-115">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="7da15-115">Describes guidelines and conventions for implementing [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="7da15-116">Das **RangeValue** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die auf einen Wert innerhalb eines Bereichs festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="7da15-116">The **RangeValue** control pattern is used to support controls that can be set to a value within a range.</span></span>

<span data-ttu-id="7da15-117">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="7da15-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="7da15-118">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="7da15-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7da15-119">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="7da15-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="7da15-120">Erforderliche Member für " **IRangeValueProvider** "</span><span class="sxs-lookup"><span data-stu-id="7da15-120">Required Members for **IRangeValueProvider**</span></span>](#required-members-for-irangevalueprovider)
-   [<span data-ttu-id="7da15-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7da15-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="7da15-122">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="7da15-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="7da15-123">Beachten Sie beim Implementieren des **RangeValue** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="7da15-123">When implementing the **RangeValue** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="7da15-124">Steuerelemente lassen eine erneute Kalibrierung der unterstützten Eigenschaften auf Grundlage des Gebietsschemas oder einer Benutzereinstellung zu.</span><span class="sxs-lookup"><span data-stu-id="7da15-124">Controls allow recalibration of their supported properties based upon locale or user preference.</span></span> <span data-ttu-id="7da15-125">Ein Beispiel hierfür ist ein Thermometersteuerelement, das so festgelegt werden kann, dass die Temperatur in Fahrenheit oder Celsius angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7da15-125">An example of this is a thermometer control that can be set to display the temperature in Fahrenheit or Celsius.</span></span>
-   <span data-ttu-id="7da15-126">Für Steuerelemente, die über mehrdeutige Bereichswerte verfügen, z. B. Statusanzeigen oder Schieberegler, sollten diese Werte normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7da15-126">Controls that have ambiguous range values, such as progress bars or sliders, should have those values normalized.</span></span>

## <a name="required-members-for-irangevalueprovider"></a><span data-ttu-id="7da15-127">Erforderliche Member für " **IRangeValueProvider** "</span><span class="sxs-lookup"><span data-stu-id="7da15-127">Required Members for **IRangeValueProvider**</span></span>

<span data-ttu-id="7da15-128">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7da15-128">The following properties and methods are required for implementing the [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface.</span></span>



| <span data-ttu-id="7da15-129">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="7da15-129">Required members</span></span>                                              | <span data-ttu-id="7da15-130">Memberart</span><span class="sxs-lookup"><span data-stu-id="7da15-130">Member type</span></span> | <span data-ttu-id="7da15-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7da15-131">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="7da15-132">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="7da15-132">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | <span data-ttu-id="7da15-133">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7da15-133">Property</span></span>    | <span data-ttu-id="7da15-134">Keine</span><span class="sxs-lookup"><span data-stu-id="7da15-134">None</span></span>  |
| [<span data-ttu-id="7da15-135">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7da15-135">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | <span data-ttu-id="7da15-136">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7da15-136">Property</span></span>    | <span data-ttu-id="7da15-137">Keine</span><span class="sxs-lookup"><span data-stu-id="7da15-137">None</span></span>  |
| [<span data-ttu-id="7da15-138">**LargeChange**</span><span class="sxs-lookup"><span data-stu-id="7da15-138">**LargeChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | <span data-ttu-id="7da15-139">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7da15-139">Property</span></span>    | <span data-ttu-id="7da15-140">Keine</span><span class="sxs-lookup"><span data-stu-id="7da15-140">None</span></span>  |
| [<span data-ttu-id="7da15-141">**SmallChange**</span><span class="sxs-lookup"><span data-stu-id="7da15-141">**SmallChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | <span data-ttu-id="7da15-142">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7da15-142">Property</span></span>    | <span data-ttu-id="7da15-143">Keine</span><span class="sxs-lookup"><span data-stu-id="7da15-143">None</span></span>  |
| [<span data-ttu-id="7da15-144">**Maximum**</span><span class="sxs-lookup"><span data-stu-id="7da15-144">**Maximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | <span data-ttu-id="7da15-145">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7da15-145">Property</span></span>    | <span data-ttu-id="7da15-146">Keine</span><span class="sxs-lookup"><span data-stu-id="7da15-146">None</span></span>  |
| [<span data-ttu-id="7da15-147">**Minimum**</span><span class="sxs-lookup"><span data-stu-id="7da15-147">**Minimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | <span data-ttu-id="7da15-148">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7da15-148">Property</span></span>    | <span data-ttu-id="7da15-149">Keine</span><span class="sxs-lookup"><span data-stu-id="7da15-149">None</span></span>  |
| [<span data-ttu-id="7da15-150">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="7da15-150">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | <span data-ttu-id="7da15-151">Methode</span><span class="sxs-lookup"><span data-stu-id="7da15-151">Method</span></span>      | <span data-ttu-id="7da15-152">Keine</span><span class="sxs-lookup"><span data-stu-id="7da15-152">None</span></span>  |



 

<span data-ttu-id="7da15-153">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7da15-153">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7da15-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7da15-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7da15-155">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="7da15-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="7da15-156">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="7da15-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="7da15-157">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="7da15-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 





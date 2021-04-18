---
title: Transform-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ITransformProvider und ITransformProvider2, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Transformations Steuerelement Musters
- Benutzeroberflächenautomatisierungs, Transformations Steuerelement-Muster
- UI-Automatisierung, ITransformProvider
- ITransformProvider
- Implementieren von Transformations Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Transformations Steuerelement-Muster
- Steuerelement Muster, ITransformProvider
- Steuerelement Muster, Implementieren der Transformation für die Benutzeroberflächen Automatisierung
- Steuerelement Muster, Transformieren
- Schnittstellen, ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516958"
---
# <a name="transform-control-pattern"></a><span data-ttu-id="9886e-113">Transform-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="9886e-113">Transform Control Pattern</span></span>

<span data-ttu-id="9886e-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) und [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="9886e-114">Describes guidelines and conventions for implementing [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) and [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), including information about properties and methods.</span></span> <span data-ttu-id="9886e-115">Das Transform-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die in einem zweidimensionalen Raum verschoben, verkleinert, geändert oder gedreht werden können.</span><span class="sxs-lookup"><span data-stu-id="9886e-115">The Transform control pattern is used to support controls that can be moved, resized, or rotated within a two-dimensional space.</span></span>

<span data-ttu-id="9886e-116">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="9886e-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="9886e-117">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9886e-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9886e-118">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="9886e-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="9886e-119">Erforderliche Member für **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="9886e-119">Required Members for **ITransformProvider**</span></span>](#required-members-for-itransformprovider)
-   [<span data-ttu-id="9886e-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9886e-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="9886e-121">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="9886e-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="9886e-122">Beachten Sie beim Implementieren des **Transform** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="9886e-122">When implementing the **Transform** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="9886e-123">Die Unterstützung für dieses Steuerelementmuster ist nicht auf Objekte auf dem Desktop beschränkt.</span><span class="sxs-lookup"><span data-stu-id="9886e-123">Support for this control pattern is not limited to objects on the desktop.</span></span> <span data-ttu-id="9886e-124">Dieses Steuerelementmuster muss auch von den untergeordneten Elementen eines Containerobjekts unterstützt werden, wenn die untergeordneten Elemente verschoben, vergrößert, verkleinert oder innerhalb der Grenzen des Containers frei gedreht werden können.</span><span class="sxs-lookup"><span data-stu-id="9886e-124">This control pattern must also be supported by the children of a container object if the children can be moved, resized, or rotated freely within the boundaries of the container.</span></span>
-   <span data-ttu-id="9886e-125">Ein Objekt kann nicht so verschoben, vergrößert, verkleinert oder gedreht werden, dass seine resultierende Bildschirmposition vollständig außerhalb der Koordinaten des Containers liegt und daher nicht über die Tastatur oder Maus zugänglich ist (wenn z. B. ein Fenster auf oberster Ebene außerhalb des Bildschirms oder ein untergeordnetes Objekt außerhalb der Viewportgrenzen des Containers verschoben wird).</span><span class="sxs-lookup"><span data-stu-id="9886e-125">An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and therefore inaccessible to the keyboard or mouse (for example, when a top-level window is moved off-screen or a child object is moved outside the boundaries of the container's viewport).</span></span> <span data-ttu-id="9886e-126">In diesen Fällen wird das Objekt so nahe wie möglich bei den angeforderten Bildschirmkoordinaten platziert, wobei die oberen oder linken Koordinaten außer Kraft gesetzt werden, damit sich die Koordinaten innerhalb der Containergrenzen befinden.</span><span class="sxs-lookup"><span data-stu-id="9886e-126">In these cases, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.</span></span>
-   <span data-ttu-id="9886e-127">Für Systeme mit mehreren Monitoren wird ein Objekt so nahe wie möglich bei den angeforderten Koordinaten auf dem primären Monitor platziert, wenn das Objekt vollständig außerhalb der Bildschirmkoordinaten des kombinierten Desktops verschoben, vergrößert, verkleinert oder gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="9886e-127">For multi-monitor systems, if an object is moved, resized, or rotated completely outside the combined desktop screen coordinates, the object is placed on the primary monitor as close to the requested coordinates as possible.</span></span>
-   <span data-ttu-id="9886e-128">Alle Parameter und Eigenschaftswerte sind absolute Angaben und unabhängig vom Gebietsschema.</span><span class="sxs-lookup"><span data-stu-id="9886e-128">All parameters and property values are absolute and independent of locale.</span></span>

## <a name="required-members-for-itransformprovider"></a><span data-ttu-id="9886e-129">Erforderliche Member für **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="9886e-129">Required Members for **ITransformProvider**</span></span>

<span data-ttu-id="9886e-130">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9886e-130">The following properties and methods are required for implementing the [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="9886e-131">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="9886e-131">Required members</span></span>                                         | <span data-ttu-id="9886e-132">Memberart</span><span class="sxs-lookup"><span data-stu-id="9886e-132">Member type</span></span> | <span data-ttu-id="9886e-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9886e-133">Notes</span></span> |
|----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="9886e-134">**CanMove**</span><span class="sxs-lookup"><span data-stu-id="9886e-134">**CanMove**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | <span data-ttu-id="9886e-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9886e-135">Property</span></span>    | <span data-ttu-id="9886e-136">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-136">None</span></span>  |
| [<span data-ttu-id="9886e-137">**CanResize**</span><span class="sxs-lookup"><span data-stu-id="9886e-137">**CanResize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | <span data-ttu-id="9886e-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9886e-138">Property</span></span>    | <span data-ttu-id="9886e-139">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-139">None</span></span>  |
| [<span data-ttu-id="9886e-140">**Canrotation**</span><span class="sxs-lookup"><span data-stu-id="9886e-140">**CanRotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | <span data-ttu-id="9886e-141">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9886e-141">Property</span></span>    | <span data-ttu-id="9886e-142">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-142">None</span></span>  |
| [<span data-ttu-id="9886e-143">**Move**</span><span class="sxs-lookup"><span data-stu-id="9886e-143">**Move**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | <span data-ttu-id="9886e-144">Methode</span><span class="sxs-lookup"><span data-stu-id="9886e-144">Method</span></span>      | <span data-ttu-id="9886e-145">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-145">None</span></span>  |
| [<span data-ttu-id="9886e-146">**Größe ändern**</span><span class="sxs-lookup"><span data-stu-id="9886e-146">**Resize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | <span data-ttu-id="9886e-147">Methode</span><span class="sxs-lookup"><span data-stu-id="9886e-147">Method</span></span>      | <span data-ttu-id="9886e-148">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-148">None</span></span>  |
| [<span data-ttu-id="9886e-149">**Drehen**</span><span class="sxs-lookup"><span data-stu-id="9886e-149">**Rotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | <span data-ttu-id="9886e-150">Methode</span><span class="sxs-lookup"><span data-stu-id="9886e-150">Method</span></span>      | <span data-ttu-id="9886e-151">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-151">None</span></span>  |



 

<span data-ttu-id="9886e-152">Die folgenden zusätzlichen Eigenschaften und Methoden sind für die Implementierung der [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9886e-152">The following additional properties and methods are required for implementing the [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="9886e-153">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="9886e-153">Required members</span></span>                                              | <span data-ttu-id="9886e-154">Memberart</span><span class="sxs-lookup"><span data-stu-id="9886e-154">Member type</span></span> | <span data-ttu-id="9886e-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9886e-155">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="9886e-156">**Kanzoom**</span><span class="sxs-lookup"><span data-stu-id="9886e-156">**CanZoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | <span data-ttu-id="9886e-157">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9886e-157">Property</span></span>    | <span data-ttu-id="9886e-158">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-158">None</span></span>  |
| [<span data-ttu-id="9886e-159">**Zoom**</span><span class="sxs-lookup"><span data-stu-id="9886e-159">**Zoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | <span data-ttu-id="9886e-160">Methode</span><span class="sxs-lookup"><span data-stu-id="9886e-160">Method</span></span>      | <span data-ttu-id="9886e-161">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-161">None</span></span>  |
| [<span data-ttu-id="9886e-162">**Zoombyunit**</span><span class="sxs-lookup"><span data-stu-id="9886e-162">**ZoomByUnit**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | <span data-ttu-id="9886e-163">Methode</span><span class="sxs-lookup"><span data-stu-id="9886e-163">Method</span></span>      | <span data-ttu-id="9886e-164">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-164">None</span></span>  |
| [<span data-ttu-id="9886e-165">**ZoomLevel**</span><span class="sxs-lookup"><span data-stu-id="9886e-165">**ZoomLevel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | <span data-ttu-id="9886e-166">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9886e-166">Property</span></span>    | <span data-ttu-id="9886e-167">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-167">None</span></span>  |
| [<span data-ttu-id="9886e-168">**Zoommaximum**</span><span class="sxs-lookup"><span data-stu-id="9886e-168">**ZoomMaximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | <span data-ttu-id="9886e-169">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9886e-169">Property</span></span>    | <span data-ttu-id="9886e-170">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-170">None</span></span>  |
| [<span data-ttu-id="9886e-171">**Zoomminimal**</span><span class="sxs-lookup"><span data-stu-id="9886e-171">**ZoomMinimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | <span data-ttu-id="9886e-172">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9886e-172">Property</span></span>    | <span data-ttu-id="9886e-173">Keine</span><span class="sxs-lookup"><span data-stu-id="9886e-173">None</span></span>  |



 

<span data-ttu-id="9886e-174">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9886e-174">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9886e-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9886e-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9886e-176">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="9886e-176">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="9886e-177">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="9886e-177">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="9886e-178">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="9886e-178">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 
---
title: Window-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IWindowProvider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen. Das Window-Steuerelement Muster unterstützt Steuerelemente, die grundlegende fensterbasierte Funktionen in einer herkömmlichen GUI bereitstellen.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Fenster Steuerelement Musters
- UI-Automatisierung, Window-Steuerelement Muster
- UI-Automatisierung, IWindowProvider
- IWindowProvider
- Implementieren von Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Window-Steuerelement Muster
- Steuerelement Muster, IWindowProvider
- Steuerelement Muster, Implementieren des Benutzeroberflächenautomatisierungs-Fensters
- Steuerelement Muster, Fenster
- Schnittstellen, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311345"
---
# <a name="window-control-pattern"></a><span data-ttu-id="32812-114">Window-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="32812-114">Window Control Pattern</span></span>

<span data-ttu-id="32812-115">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="32812-115">Describes guidelines and conventions for implementing [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="32812-116">Das **Window** -Steuerelement Muster unterstützt Steuerelemente, die grundlegende fensterbasierte Funktionen in einer herkömmlichen GUI bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="32812-116">The **Window** control pattern supports controls that provide fundamental window-based functionality within a traditional GUI.</span></span>

<span data-ttu-id="32812-117">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren müssen, sind u. a. Anwendungsfenster der obersten Ebene, untergeordnete MDI-Fenster (Multiple Document Interface), in der Größe umsetzbare Steuerelemente für geteilte Bereiche, Modale Dialoge und</span><span class="sxs-lookup"><span data-stu-id="32812-117">Examples of controls that must implement this control pattern include top-level application windows, multiple-document interface (MDI) child windows, resizable split pane controls, modal dialogs and balloon help windows.</span></span> <span data-ttu-id="32812-118">Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="32812-118">For examples of controls that implement this control pattern, see [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="32812-119">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="32812-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="32812-120">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="32812-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="32812-121">Erforderliche Member für **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="32812-121">Required Members for **IWindowProvider**</span></span>](#required-members-for-iwindowprovider)
-   [<span data-ttu-id="32812-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32812-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="32812-123">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="32812-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="32812-124">Beachten Sie beim Implementieren des **Window** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="32812-124">When implementing the **Window** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="32812-125">Um die Möglichkeit zum Ändern der Fenstergröße und Bildschirmposition mithilfe der Microsoft-Benutzeroberflächen Automatisierung zu unterstützen, muss ein Steuerelement zusätzlich zu [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) implementieren.</span><span class="sxs-lookup"><span data-stu-id="32812-125">To support the ability to modify both window size and screen position using Microsoft UI Automation, a control must implement [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) in addition to [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="32812-126">Steuerelemente, die Titelleisten und Titelleisten Elemente enthalten, mit denen das Steuerelement verschoben, verkleinert, minimiert oder geschlossen werden kann, sind in der Regel für die Implementierung von [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32812-126">Controls that contain title bars, and title bar elements that enable the control to be moved, resized, maximized, minimized, or closed, are typically required to implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="32812-127">Steuerelemente wie QuickInfo-Popups und Kombinations Feld-oder Menü-Dropdown-Elemente implementieren i. d. d. [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)nicht.</span><span class="sxs-lookup"><span data-stu-id="32812-127">Controls such as tooltip pop-ups and combo-box or menu drop-downs do not typically implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="32812-128">Die Hilfefenster der Sprechblase unterscheiden sich von einfachen QuickInfo-Popups durch die Bereitstellung einer Fenster ähnlichen Schaltfläche " **Schließen** ".</span><span class="sxs-lookup"><span data-stu-id="32812-128">Balloon help windows are differentiated from basic tooltip pop-ups by the provision of a window-like **Close** button.</span></span>
-   <span data-ttu-id="32812-129">Der Vollbildmodus wird von [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) nicht unterstützt, da er featurespezifisch für eine Anwendung ist und kein typisches Fenster Verhalten ist.</span><span class="sxs-lookup"><span data-stu-id="32812-129">Full-screen mode is not supported by [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) as it is feature-specific to an application and is not typical window behavior.</span></span>

## <a name="required-members-for-iwindowprovider"></a><span data-ttu-id="32812-130">Erforderliche Member für **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="32812-130">Required Members for **IWindowProvider**</span></span>

<span data-ttu-id="32812-131">Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32812-131">The following properties, methods, and events are required for implementing the [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) interface.</span></span>



| <span data-ttu-id="32812-132">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="32812-132">Required members</span></span>                                                                            | <span data-ttu-id="32812-133">Memberart</span><span class="sxs-lookup"><span data-stu-id="32812-133">Member type</span></span> | <span data-ttu-id="32812-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="32812-134">Notes</span></span>                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="32812-135">**Windowinteraktionstate**</span><span class="sxs-lookup"><span data-stu-id="32812-135">**WindowInteractionState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | <span data-ttu-id="32812-136">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32812-136">Property</span></span>    | <span data-ttu-id="32812-137">Es ist nicht garantiert, dass " **windowinteraktionstate" " \_ synchyforuserinteraction** " ist.</span><span class="sxs-lookup"><span data-stu-id="32812-137">Is not guaranteed to be **WindowInteractionState\_ReadyForUserInteraction**</span></span> |
| [<span data-ttu-id="32812-138">**IsModal**</span><span class="sxs-lookup"><span data-stu-id="32812-138">**IsModal**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | <span data-ttu-id="32812-139">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32812-139">Property</span></span>    | <span data-ttu-id="32812-140">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-140">None</span></span>                                                                        |
| [<span data-ttu-id="32812-141">**IsTopmost**</span><span class="sxs-lookup"><span data-stu-id="32812-141">**IsTopmost**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | <span data-ttu-id="32812-142">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32812-142">Property</span></span>    | <span data-ttu-id="32812-143">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-143">None</span></span>                                                                        |
| [<span data-ttu-id="32812-144">**Canmaximi**</span><span class="sxs-lookup"><span data-stu-id="32812-144">**CanMaximize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | <span data-ttu-id="32812-145">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32812-145">Property</span></span>    | <span data-ttu-id="32812-146">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-146">None</span></span>                                                                        |
| [<span data-ttu-id="32812-147">**Canmini mieren**</span><span class="sxs-lookup"><span data-stu-id="32812-147">**CanMinimize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | <span data-ttu-id="32812-148">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32812-148">Property</span></span>    | <span data-ttu-id="32812-149">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-149">None</span></span>                                                                        |
| [<span data-ttu-id="32812-150">**WindowVisualState**</span><span class="sxs-lookup"><span data-stu-id="32812-150">**WindowVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | <span data-ttu-id="32812-151">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32812-151">Property</span></span>    | <span data-ttu-id="32812-152">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-152">None</span></span>                                                                        |
| [<span data-ttu-id="32812-153">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="32812-153">**Close**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | <span data-ttu-id="32812-154">Methode</span><span class="sxs-lookup"><span data-stu-id="32812-154">Method</span></span>      | <span data-ttu-id="32812-155">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-155">None</span></span>                                                                        |
| [<span data-ttu-id="32812-156">**SetVisualState**</span><span class="sxs-lookup"><span data-stu-id="32812-156">**SetVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | <span data-ttu-id="32812-157">Methode</span><span class="sxs-lookup"><span data-stu-id="32812-157">Method</span></span>      | <span data-ttu-id="32812-158">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-158">None</span></span>                                                                        |
| [<span data-ttu-id="32812-159">**WaitForInputIdle**</span><span class="sxs-lookup"><span data-stu-id="32812-159">**WaitForInputIdle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | <span data-ttu-id="32812-160">Methode</span><span class="sxs-lookup"><span data-stu-id="32812-160">Method</span></span>      | <span data-ttu-id="32812-161">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-161">None</span></span>                                                                        |
| [<span data-ttu-id="32812-162">**UIA \_ \_ -Fenster windowclosedeventid**</span><span class="sxs-lookup"><span data-stu-id="32812-162">**UIA\_Window\_WindowClosedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="32812-163">Ereignis</span><span class="sxs-lookup"><span data-stu-id="32812-163">Event</span></span>       | <span data-ttu-id="32812-164">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-164">None</span></span>                                                                        |
| [<span data-ttu-id="32812-165">**UIA \_ \_ -Fenster windowopenedeventid**</span><span class="sxs-lookup"><span data-stu-id="32812-165">**UIA\_Window\_WindowOpenedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="32812-166">Ereignis</span><span class="sxs-lookup"><span data-stu-id="32812-166">Event</span></span>       | <span data-ttu-id="32812-167">Keine</span><span class="sxs-lookup"><span data-stu-id="32812-167">None</span></span>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="32812-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32812-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="32812-169">**Licher**</span><span class="sxs-lookup"><span data-stu-id="32812-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="32812-170">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="32812-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="32812-171">Zuordnen von Steuerelementmustern für Benutzeroberflächenautomatisierungs-Clients</span><span class="sxs-lookup"><span data-stu-id="32812-171">Control Pattern Mapping for UI Automation Clients</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="32812-172">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="32812-172">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 





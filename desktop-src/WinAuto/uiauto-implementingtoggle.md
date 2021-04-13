---
title: Toggle-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ideggleprovider, einschließlich Informationen zu Eigenschaften und Methoden. Das Toggle-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die eine Reihe von Zuständen durchlaufen und einen Zustand nach dem Festlegen beibehalten können.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- UI-Automatisierung, Implementieren eines Toggle-Steuerelement Musters
- UI-Automatisierung, Toggle-Steuerelement Muster
- UI-Automatisierung, iabggleprovider
- IToggleProvider
- Implementieren von Steuerelement Mustern zum Umschalten der Benutzeroberflächen Automatisierung
- Steuerelement Muster umschalten
- Steuerelement Muster, iesggleprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächen Automatisierung umschalten
- Steuerelement Muster, Umschalten
- Schnittstellen, ideggleprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388122"
---
# <a name="toggle-control-pattern"></a><span data-ttu-id="a9e83-114">Toggle-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="a9e83-114">Toggle Control Pattern</span></span>

<span data-ttu-id="a9e83-115">Beschreibt Richtlinien und Konventionen für das Implementieren von [**ideggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="a9e83-115">Describes guidelines and conventions for implementing [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), including information about properties and methods.</span></span> <span data-ttu-id="a9e83-116">Das **Toggle** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die eine Reihe von Zuständen durchlaufen und einen Zustand nach dem Festlegen beibehalten können.</span><span class="sxs-lookup"><span data-stu-id="a9e83-116">The **Toggle** control pattern is used to support controls that can cycle through a set of states and maintain a state once set.</span></span>

<span data-ttu-id="a9e83-117">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="a9e83-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="a9e83-118">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="a9e83-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a9e83-119">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="a9e83-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="a9e83-120">Erforderliche Member für **iesggleprovider**</span><span class="sxs-lookup"><span data-stu-id="a9e83-120">Required Members for **IToggleProvider**</span></span>](#required-members-for-itoggleprovider)
-   [<span data-ttu-id="a9e83-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9e83-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a9e83-122">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="a9e83-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a9e83-123">Beachten Sie beim Implementieren des **Toggle** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="a9e83-123">When implementing the **Toggle** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a9e83-124">Steuerelemente, die den Zustand bei Aktivierung nicht beibehalten, z. b. Schaltflächen, Symbolleisten Schaltflächen und Links, müssen stattdessen [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) implementieren.</span><span class="sxs-lookup"><span data-stu-id="a9e83-124">Controls that do not maintain state when activated, such as buttons, toolbar buttons, and hyperlinks, must implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) instead.</span></span>
-   <span data-ttu-id="a9e83-125">Ein Steuerelement muss seine UMSCHALT Zustände ("[**degglestate**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)") in der folgenden Reihenfolge durchlaufen: " **degglestate \_ on**", " **degglestate \_ Off** " und ", falls unterstützt", " **degglestate" \_ unbestimmt**.</span><span class="sxs-lookup"><span data-stu-id="a9e83-125">A control must cycle through its toggle states ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) in the following order: **ToggleState\_On**, **ToggleState\_Off** and, if supported, **ToggleState\_Indeterminate**.</span></span>
-   <span data-ttu-id="a9e83-126">Ein-und **ausschalten bietet keine** Set-State-Methode aufgrund von Problemen im Zusammenhang mit der direkten Einstellung eines Kontrollkästchens mit drei Zuständen ohne durchlaufen der entsprechenden " [**degglestate**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) "-Sequenz.</span><span class="sxs-lookup"><span data-stu-id="a9e83-126">**Toggle** does not provide a set-state method because of issues surrounding the direct setting of a three-state check box without cycling through its appropriate [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) sequence.</span></span>
-   <span data-ttu-id="a9e83-127">Das Optionsfeld-Steuerelement implementiert [**iumggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)nicht, da es nicht in der Lage ist, seine gültigen Zustände zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a9e83-127">The radio button control does not implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), because it is not capable of cycling through its valid states.</span></span>

## <a name="required-members-for-itoggleprovider"></a><span data-ttu-id="a9e83-128">Erforderliche Member für **iesggleprovider**</span><span class="sxs-lookup"><span data-stu-id="a9e83-128">Required Members for **IToggleProvider**</span></span>

<span data-ttu-id="a9e83-129">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ideggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9e83-129">The following properties and methods are required for implementing the [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) interface.</span></span>



| <span data-ttu-id="a9e83-130">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="a9e83-130">Required members</span></span>                                          | <span data-ttu-id="a9e83-131">Memberart</span><span class="sxs-lookup"><span data-stu-id="a9e83-131">Member type</span></span> | <span data-ttu-id="a9e83-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9e83-132">Notes</span></span> |
|-----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="a9e83-133">**Ein-/Ausschalten**</span><span class="sxs-lookup"><span data-stu-id="a9e83-133">**Toggle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | <span data-ttu-id="a9e83-134">Methode</span><span class="sxs-lookup"><span data-stu-id="a9e83-134">Method</span></span>      | <span data-ttu-id="a9e83-135">Keine</span><span class="sxs-lookup"><span data-stu-id="a9e83-135">None</span></span>  |
| [<span data-ttu-id="a9e83-136">**Objektstatus**</span><span class="sxs-lookup"><span data-stu-id="a9e83-136">**ToggleState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | <span data-ttu-id="a9e83-137">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a9e83-137">Property</span></span>    | <span data-ttu-id="a9e83-138">Keine</span><span class="sxs-lookup"><span data-stu-id="a9e83-138">None</span></span>  |



 

<span data-ttu-id="a9e83-139">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a9e83-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9e83-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9e83-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9e83-141">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="a9e83-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="a9e83-142">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="a9e83-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="a9e83-143">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="a9e83-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 





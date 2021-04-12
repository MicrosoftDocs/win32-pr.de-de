---
title: DropTarget-Steuerelement Muster
description: Stellt Richtlinien und Konventionen für das Implementieren des DropTarget-Steuerelement Musters mithilfe von idroptargetprovider bereit, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines DropTarget-Steuerelement Musters
- UI-Automatisierung, DropTarget-Steuerelement Muster
- UI-Automatisierung, idroptargetprovider
- IDropTargetProvider
- Implementieren von DropTarget-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- DropTarget-Steuerelement Muster
- Steuerelement Muster, idroptargetprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs DropTarget
- Steuerelement Muster, DropTarget
- Schnittstellen, idroptargetprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315669"
---
# <a name="droptarget-control-pattern"></a><span data-ttu-id="2fd7f-113">DropTarget-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="2fd7f-113">DropTarget Control Pattern</span></span>

<span data-ttu-id="2fd7f-114">Stellt Richtlinien und Konventionen für das Implementieren des **DropTarget** -Steuerelement Musters mithilfe von [**idroptargetprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider)bereit, einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="2fd7f-114">Provides guidelines and conventions for implementing the **DropTarget** control pattern by using [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), including information about properties and methods.</span></span> <span data-ttu-id="2fd7f-115">Das **DropTarget** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Ziel eines Drag & Drop-Vorgangs verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="2fd7f-115">The **DropTarget** control pattern is used to support controls that can be the target of a drag-and-drop operation.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="2fd7f-116">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="2fd7f-116">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="2fd7f-117">Wenn Sie das **DropTarget** -Steuerelement Muster implementieren, verwenden Sie die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="2fd7f-117">When implementing the **DropTarget** control pattern, use the following guidelines and conventions:</span></span>

-   <span data-ttu-id="2fd7f-118">Das **DropTarget** -Muster muss unterstützt werden, während ein Zieh Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fd7f-118">The **DropTarget** pattern must be supported while a drag operation is in progress.</span></span> <span data-ttu-id="2fd7f-119">Sie kann auch dann unterstützt werden, wenn kein Zieh Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fd7f-119">It can be supported even when a drag operation is not in progress.</span></span>
-   <span data-ttu-id="2fd7f-120">Die [**idroptargetprovider::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) -Eigenschaft ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2fd7f-120">The [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property is required.</span></span>
-   <span data-ttu-id="2fd7f-121">Die [**idroptargetprovider::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) -Eigenschaft ist erforderlich, wenn mehrere mögliche Ablage Effekte für das Ziel vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2fd7f-121">The [**IDropTargetProvider::DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) property is required when there is more than one possible drop effect for the target.</span></span>
-   <span data-ttu-id="2fd7f-122">Das-Element muss geänderte Ereignis Eigenschaften für die Eigenschaften **droptargeteffect** ([**UIA \_ droptargetdroptargeteffectpropertyid**](uiauto-control-pattern-propids.md)) und **droptargeteffects** ([**UIA \_ droptargetdroptargeteffectspropertyid**](uiauto-control-pattern-propids.md)) bei Änderungen angeben.</span><span class="sxs-lookup"><span data-stu-id="2fd7f-122">The element must raise property changed events for the **DropTargetEffect** ([**UIA\_DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) and **DropTargetEffects** ([**UIA\_DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) properties when they change.</span></span>

## <a name="required-members-for-idroptargetprovider"></a><span data-ttu-id="2fd7f-123">Erforderliche Member für **idroptargetprovider**</span><span class="sxs-lookup"><span data-stu-id="2fd7f-123">Required Members for **IDropTargetProvider**</span></span>

<span data-ttu-id="2fd7f-124">Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**idroptargetprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2fd7f-124">The following properties and methods are required for implementing the [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) interface.</span></span>



| <span data-ttu-id="2fd7f-125">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="2fd7f-125">Required members</span></span>                                                                              | <span data-ttu-id="2fd7f-126">Memberart</span><span class="sxs-lookup"><span data-stu-id="2fd7f-126">Member type</span></span> | <span data-ttu-id="2fd7f-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2fd7f-127">Notes</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="2fd7f-128">**Droptargeteffect**</span><span class="sxs-lookup"><span data-stu-id="2fd7f-128">**DropTargetEffect**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | <span data-ttu-id="2fd7f-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2fd7f-129">Property</span></span>    | <span data-ttu-id="2fd7f-130">Keine</span><span class="sxs-lookup"><span data-stu-id="2fd7f-130">None</span></span>                                                                     |
| [<span data-ttu-id="2fd7f-131">**Droptargeteffects**</span><span class="sxs-lookup"><span data-stu-id="2fd7f-131">**DropTargetEffects**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | <span data-ttu-id="2fd7f-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2fd7f-132">Property</span></span>    | <span data-ttu-id="2fd7f-133">Erforderlich, wenn das Ablage Ziel mehr als einen möglichen Ablage Effekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2fd7f-133">Required if the drop target supports more than one possible drop effect.</span></span> |
| [<span data-ttu-id="2fd7f-134">**UIA \_ DropTarget \_ dragentereventid**</span><span class="sxs-lookup"><span data-stu-id="2fd7f-134">**UIA\_DropTarget\_DragEnterEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="2fd7f-135">Ereignis</span><span class="sxs-lookup"><span data-stu-id="2fd7f-135">Event</span></span>       | <span data-ttu-id="2fd7f-136">Keine</span><span class="sxs-lookup"><span data-stu-id="2fd7f-136">None</span></span>                                                                     |
| [<span data-ttu-id="2fd7f-137">**UIA \_ DropTarget \_ dragleaveeventid**</span><span class="sxs-lookup"><span data-stu-id="2fd7f-137">**UIA\_DropTarget\_DragLeaveEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="2fd7f-138">Ereignis</span><span class="sxs-lookup"><span data-stu-id="2fd7f-138">Event</span></span>       | <span data-ttu-id="2fd7f-139">Keine</span><span class="sxs-lookup"><span data-stu-id="2fd7f-139">None</span></span>                                                                     |
| [<span data-ttu-id="2fd7f-140">**\_Droppedeventid für UIA DropTarget \_**</span><span class="sxs-lookup"><span data-stu-id="2fd7f-140">**UIA\_DropTarget\_DroppedEventId**</span></span>](uiauto-event-ids.md)     | <span data-ttu-id="2fd7f-141">Ereignis</span><span class="sxs-lookup"><span data-stu-id="2fd7f-141">Event</span></span>       | <span data-ttu-id="2fd7f-142">Keine</span><span class="sxs-lookup"><span data-stu-id="2fd7f-142">None</span></span>                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="2fd7f-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2fd7f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fd7f-144">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="2fd7f-144">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="2fd7f-145">Steuerelement Muster ziehen</span><span class="sxs-lookup"><span data-stu-id="2fd7f-145">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[<span data-ttu-id="2fd7f-146">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="2fd7f-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="2fd7f-147">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="2fd7f-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="2fd7f-148">Benutzeroberflächenautomatisierungs-Unterstützung für Drag & Drop</span><span class="sxs-lookup"><span data-stu-id="2fd7f-148">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 
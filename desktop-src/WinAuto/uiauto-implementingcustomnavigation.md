---
title: Customnavigation-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren der icustomnavigationprovider-Schnittstelle, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206706"
---
# <a name="customnavigation-control-pattern"></a><span data-ttu-id="bf541-103">Customnavigation-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="bf541-103">CustomNavigation Control Pattern</span></span>

<span data-ttu-id="bf541-104">Beschreibt Richtlinien und Konventionen für das Implementieren der **icustomnavigationprovider** -Schnittstelle, einschließlich Informationen zu Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="bf541-104">Describes guidelines and conventions for implementing the **ICustomNavigationProvider** interface, including information about properties and methods.</span></span> <span data-ttu-id="bf541-105">Das **customnavigation** -Steuerelement Muster wird verwendet, um die benutzerdefinierte Navigation zwischen Steuerelementen in Hierarchie ähnlichen Strukturen zu ermöglichen, z. b. Listenelemente, aufzählige Listen, nummerierte Listen</span><span class="sxs-lookup"><span data-stu-id="bf541-105">The **CustomNavigation** control pattern is used to enable custom navigation between controls in hierarchy-like structures such as list items, bulleted lists, numbered lists and headings.</span></span> <span data-ttu-id="bf541-106">Dies ermöglicht es Anbietern, Strukturen zu beschreiben oder die navigierbaren Beziehungen mit dem Element allein und nicht nur mit dem enthaltenden Steuerelement zu definieren.</span><span class="sxs-lookup"><span data-stu-id="bf541-106">This enables providers to describe structures or define the navigable relationships using the element alone and not just the containing control.</span></span>

<span data-ttu-id="bf541-107">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="bf541-107">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="bf541-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="bf541-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="bf541-109">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="bf541-109">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="bf541-110">Erforderliche Member für **icustomnavigationprovider**</span><span class="sxs-lookup"><span data-stu-id="bf541-110">Required Members for **ICustomNavigationProvider**</span></span>](#required-members-for-icustomnavigationprovider)
-   [<span data-ttu-id="bf541-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf541-111">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="bf541-112">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="bf541-112">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="bf541-113">Beachten Sie beim Implementieren des **customnavigation** -Anbieters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="bf541-113">When implementing the **CustomNavigation** provider, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="bf541-114">Eigenschaftswerte für **positioninset**, **sizeofset** und Level sind 1-basierte ganzzahlige Werte. </span><span class="sxs-lookup"><span data-stu-id="bf541-114">Property values for **PositionInSet**, **SizeOfSet**, and **Level** are one-based integer values.</span></span>
-   <span data-ttu-id="bf541-115">**Icustomnavigationprovider** bietet keine aktive Bearbeitung des Steuer Elements, z. b. das Verschieben von Positionen, das Hinzufügen und Entfernen von Elementen oder das herauf Stufen und Herabstufen von Ebenen.</span><span class="sxs-lookup"><span data-stu-id="bf541-115">**ICustomNavigationProvider** does not provide for active manipulation of the control such as moving positions, adding and removing items, or promoting and demoting levels.</span></span>
-   <span data-ttu-id="bf541-116">Steuerelemente, die **icustomnavigationprovider** implementieren, verfügen in der Regel über eine hierarchische Struktur, können jedoch Ebenen mithilfe der **Navigate** -Methode überspringen.</span><span class="sxs-lookup"><span data-stu-id="bf541-116">Controls that implement **ICustomNavigationProvider** typically have a hierarchical structure, but can skip levels by using the **Navigate** method.</span></span> <span data-ttu-id="bf541-117">Die Eigenschaften **positioninset**, **sizeofset** und **Level** sind für das Muster erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf541-117">The properties **PositionInSet**, **SizeOfSet**, and **Level** are required on the pattern.</span></span>

## <a name="required-members-for-icustomnavigationprovider"></a><span data-ttu-id="bf541-118">Erforderliche Member für **icustomnavigationprovider**</span><span class="sxs-lookup"><span data-stu-id="bf541-118">Required Members for **ICustomNavigationProvider**</span></span>

<span data-ttu-id="bf541-119">Die folgenden Eigenschaften sind erforderlich, um die **icustomnavigationprovider** -Schnittstelle zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="bf541-119">The following properties are required for implementing the **ICustomNavigationProvider** interface.</span></span>



| <span data-ttu-id="bf541-120">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="bf541-120">Required members</span></span>                                                                  | <span data-ttu-id="bf541-121">Memberart</span><span class="sxs-lookup"><span data-stu-id="bf541-121">Member type</span></span> | <span data-ttu-id="bf541-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bf541-122">Notes</span></span>                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf541-123">**Cachedlevel**</span><span class="sxs-lookup"><span data-stu-id="bf541-123">**CachedLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | <span data-ttu-id="bf541-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf541-124">Property</span></span>    | <span data-ttu-id="bf541-125">In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bf541-125">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="bf541-126">**Cachedpositioninset**</span><span class="sxs-lookup"><span data-stu-id="bf541-126">**CachedPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | <span data-ttu-id="bf541-127">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf541-127">Property</span></span>    | <span data-ttu-id="bf541-128">In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bf541-128">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="bf541-129">**Cachedsizeofset**</span><span class="sxs-lookup"><span data-stu-id="bf541-129">**CachedSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | <span data-ttu-id="bf541-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf541-130">Property</span></span>    | <span data-ttu-id="bf541-131">In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bf541-131">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="bf541-132">**Currentlevel**</span><span class="sxs-lookup"><span data-stu-id="bf541-132">**CurrentLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | <span data-ttu-id="bf541-133">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf541-133">Property</span></span>    | <span data-ttu-id="bf541-134">In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bf541-134">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="bf541-135">**Currentpositioninset**</span><span class="sxs-lookup"><span data-stu-id="bf541-135">**CurrentPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | <span data-ttu-id="bf541-136">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf541-136">Property</span></span>    | <span data-ttu-id="bf541-137">In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bf541-137">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="bf541-138">**Currentsizeofset**</span><span class="sxs-lookup"><span data-stu-id="bf541-138">**CurrentSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | <span data-ttu-id="bf541-139">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bf541-139">Property</span></span>    | <span data-ttu-id="bf541-140">In der [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bf541-140">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="bf541-141">**Navigieren**</span><span class="sxs-lookup"><span data-stu-id="bf541-141">**Navigate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | <span data-ttu-id="bf541-142">Methode</span><span class="sxs-lookup"><span data-stu-id="bf541-142">Method</span></span>      | <span data-ttu-id="bf541-143">Keine</span><span class="sxs-lookup"><span data-stu-id="bf541-143">None</span></span>                                                                                |



 

<span data-ttu-id="bf541-144">Diesem Steuerelementmuster sind keine Methoden oder Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="bf541-144">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf541-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf541-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf541-146">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="bf541-146">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="bf541-147">ListItem-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="bf541-147">ListItem Control</span></span>](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="bf541-148">HeaderItem-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="bf541-148">HeaderItem Control</span></span>](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="bf541-149">DataItem-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="bf541-149">DataItem Control</span></span>](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="bf541-150">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="bf541-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





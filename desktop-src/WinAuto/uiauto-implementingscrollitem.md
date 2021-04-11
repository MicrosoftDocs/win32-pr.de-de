---
title: ScrollItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IScrollItemProvider, einschließlich Informationen zu-Methoden.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des ScrollItem-Steuerelement Musters
- UI-Automatisierung, ScrollItem-Steuerelement Muster
- UI-Automatisierung, IScrollItemProvider
- IScrollItemProvider
- Implementieren von ScrollItem-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- ScrollItem-Steuerelement Muster
- Steuerelement Muster, IScrollItemProvider
- Steuerelement Muster, Implementieren von Benutzeroberflächen Automatisierung (ScrollItem)
- Steuerelement Muster, ScrollItem
- Schnittstellen, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206897"
---
# <a name="scrollitem-control-pattern"></a><span data-ttu-id="f4ab2-113">ScrollItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="f4ab2-113">ScrollItem Control Pattern</span></span>

<span data-ttu-id="f4ab2-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), einschließlich Informationen zu-Methoden.</span><span class="sxs-lookup"><span data-stu-id="f4ab2-114">Describes guidelines and conventions for implementing [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), including information about methods.</span></span> <span data-ttu-id="f4ab2-115">Das **ScrollItem** -Steuerelement Muster wird verwendet, um einzelne untergeordnete Steuerelemente von Containern zu unterstützen, die [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)implementieren.</span><span class="sxs-lookup"><span data-stu-id="f4ab2-115">The **ScrollItem** control pattern is used to support individual child controls of containers that implement [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span></span> <span data-ttu-id="f4ab2-116">Das vorhanden sein des **ScrollItem** -Steuerelement Musters in einem-Steuerelement impliziert nicht, dass sein Container oder ein Vorgänger das **Scroll** -Steuerelement Muster implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="f4ab2-116">The existence of the **ScrollItem** control pattern on a control does not imply that its container or any ancestor must implement the **Scroll** control pattern.</span></span>

<span data-ttu-id="f4ab2-117">Wenn der Container das **Scroll** -Steuerelement Muster implementiert, fungiert das **ScrollItem** -Steuerelement Muster als Kommunikationskanal zwischen einem untergeordneten Steuerelement und seinem Container, um sicherzustellen, dass der Container den aktuell sichtbaren Inhalt (oder die Region) innerhalb des Viewports ändern kann, um das untergeordnete Steuerelement anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f4ab2-117">When the container does implement the **Scroll** control pattern, the **ScrollItem** control pattern acts as a communication channel between a child control and its container to ensure that the container can change the currently visible content (or region) within its viewport to display the child control.</span></span> <span data-ttu-id="f4ab2-118">Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="f4ab2-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="f4ab2-119">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="f4ab2-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f4ab2-120">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="f4ab2-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="f4ab2-121">Erforderliche Member für **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="f4ab2-121">Required Members for **IScrollItemProvider**</span></span>](#required-members-for-iscrollitemprovider)
-   [<span data-ttu-id="f4ab2-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4ab2-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="f4ab2-123">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="f4ab2-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="f4ab2-124">Beachten Sie beim Implementieren des **ScrollItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="f4ab2-124">When implementing the **ScrollItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="f4ab2-125">Elemente, die in einem [Fenster](uiauto-supportwindowcontroltype.md) -oder **Canvas** -Steuerelement enthalten sind, müssen nicht die [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="f4ab2-125">Items contained within a [Window](uiauto-supportwindowcontroltype.md) or **Canvas** control are not required to implement the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span> <span data-ttu-id="f4ab2-126">Als Alternative müssen Sie jedoch einen gültigen Speicherort für die Eigenschaft [**iuiautomationelement:: currentboundingrechteck**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (oder [**cachedboundingrechteck**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="f4ab2-126">As an alternative, however, they must expose a valid location for the [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (or [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) property.</span></span> <span data-ttu-id="f4ab2-127">Dadurch kann eine Microsoft UI Automation-Client Anwendung die [**iuiautomationscrollpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) -Steuerelement Muster-Methoden für den Container verwenden, um das untergeordnete Element anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f4ab2-127">This will allow a Microsoft UI Automation client application to use the [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) control pattern methods on the container to display the child item.</span></span>

## <a name="required-members-for-iscrollitemprovider"></a><span data-ttu-id="f4ab2-128">Erforderliche Member für **IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="f4ab2-128">Required Members for **IScrollItemProvider**</span></span>

<span data-ttu-id="f4ab2-129">Die folgende Methode ist für die Implementierung der [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f4ab2-129">The following method is required for implementing the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span>



| <span data-ttu-id="f4ab2-130">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="f4ab2-130">Required members</span></span>                                                    | <span data-ttu-id="f4ab2-131">Memberart</span><span class="sxs-lookup"><span data-stu-id="f4ab2-131">Member type</span></span> | <span data-ttu-id="f4ab2-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4ab2-132">Notes</span></span> |
|---------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="f4ab2-133">**ScrollIntoView**</span><span class="sxs-lookup"><span data-stu-id="f4ab2-133">**ScrollIntoView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | <span data-ttu-id="f4ab2-134">Methode</span><span class="sxs-lookup"><span data-stu-id="f4ab2-134">Method</span></span>      | <span data-ttu-id="f4ab2-135">Keine</span><span class="sxs-lookup"><span data-stu-id="f4ab2-135">None</span></span>  |



 

<span data-ttu-id="f4ab2-136">Diesem Steuerelementmuster sind keine Eigenschaften oder Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f4ab2-136">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4ab2-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4ab2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4ab2-138">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="f4ab2-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="f4ab2-139">Auswahl Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="f4ab2-139">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
</dt> <dt>

[<span data-ttu-id="f4ab2-140">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="f4ab2-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="f4ab2-141">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="f4ab2-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 





---
title: ObjectModel-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von iobjectmodelprovider, einschließlich Informationen zu-Methoden. Das ObjectModel-Steuerelement Muster wird verwendet, um einen Zeiger auf das zugrunde liegende Objektmodell eines Dokuments verfügbar zu machen.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des ObjectModel-Steuerelement Musters
- UI-Automatisierung, ObjectModel-Steuerelement Muster
- UI-Automatisierung, iobjectmodelprovider
- IObjectModelProvider
- Implementieren eines ObjectModel-Steuerelement Musters
- ObjectModel-Steuerelement Muster
- Steuerelement Muster, iobjectmodelprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-ObjectModel
- Steuerelement Muster, ObjectModel
- Schnittstellen, iobjectmodelprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315782"
---
# <a name="objectmodel-control-pattern"></a><span data-ttu-id="6ce49-114">ObjectModel-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="6ce49-114">ObjectModel Control Pattern</span></span>

<span data-ttu-id="6ce49-115">Beschreibt Richtlinien und Konventionen für das Implementieren von [**iobjectmodelprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), einschließlich Informationen zu-Methoden.</span><span class="sxs-lookup"><span data-stu-id="6ce49-115">Describes guidelines and conventions for implementing [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), including information about methods.</span></span> <span data-ttu-id="6ce49-116">Das **ObjectModel** -Steuerelement Muster wird verwendet, um einen Zeiger auf das zugrunde liegende Objektmodell eines Dokuments verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="6ce49-116">The **ObjectModel** control pattern is used to expose a pointer to the underlying object model of a document.</span></span>

<span data-ttu-id="6ce49-117">Viele Anwendungen implementieren umfassende Objekt Modelle, die über die von der Microsoft-Benutzeroberflächen Automatisierung bereitgestellte Werte hinaus erhöhen.</span><span class="sxs-lookup"><span data-stu-id="6ce49-117">Many applications implement rich object models that add value beyond what Microsoft UI Automation provides.</span></span> <span data-ttu-id="6ce49-118">Dieses Steuerelement Muster ermöglicht einem Client, von einem Benutzeroberflächenautomatisierungs-Element in das zugrunde liegende-Objektmodell zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="6ce49-118">This control pattern allows a client to navigate from a UI Automation element into the underlying object model.</span></span>

<span data-ttu-id="6ce49-119">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6ce49-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6ce49-120">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="6ce49-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="6ce49-121">Erforderliche Member für **iobjectmodelprovider**</span><span class="sxs-lookup"><span data-stu-id="6ce49-121">Required Members for **IObjectModelProvider**</span></span>](#required-members-for-iobjectmodelprovider)
-   [<span data-ttu-id="6ce49-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ce49-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="6ce49-123">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="6ce49-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="6ce49-124">Beachten Sie beim Implementieren des **ObjectModel** -Steuerelement Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="6ce49-124">When implementing the **ObjectModel** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="6ce49-125">Die [**iobjectmodelprovider:: getunderlyingobjectmodel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) -Methode sollte einen Zeiger auf das Objekt zurückgeben, das so nah wie möglich an das Quell-UI-Element ist.</span><span class="sxs-lookup"><span data-stu-id="6ce49-125">The [**IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) method should return a pointer to the object that is as close as possible to the source UI element.</span></span> <span data-ttu-id="6ce49-126">Beispielsweise sollte ein Benutzeroberflächenautomatisierungs-Anbieter für ein einzelnes Element in einem Webbrowser einen Objektmodell Zeiger für das Element zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6ce49-126">For example, in a web browser, a UI Automation provider for a single element should return an object model pointer for the element.</span></span> <span data-ttu-id="6ce49-127">Das Zurückgeben eines Objektmodell Zeigers für den Dokument Stamm wäre weitaus weniger nützlich.</span><span class="sxs-lookup"><span data-stu-id="6ce49-127">Returning an object model pointer for the document root would be far less useful.</span></span>
-   <span data-ttu-id="6ce49-128">Es wird erwartet, dass der Client des **ObjectModel** -Steuerelement Musters über die IID für die Schnittstelle verfügt, die Sie suchen. aus diesem Grund genügt es, einen einfachen [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="6ce49-128">The client of the **ObjectModel** control pattern is expected to have the IID for the interface they are seeking, which is why it is enough to return a simple [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="6ce49-129">Da die Benutzeroberflächen Automatisierung den Zeiger auf den Client Prozess Marshalls, sollte der Anbieter den Zugriff auf das Objektmodell unter Verwendung von Standard-Component Object Model-Methoden (com) erwarten.</span><span class="sxs-lookup"><span data-stu-id="6ce49-129">Because UI Automation marshals the pointer to the client process, the provider should expect the client to access the object model using standard Component Object Model (COM) practices.</span></span>

## <a name="required-members-for-iobjectmodelprovider"></a><span data-ttu-id="6ce49-130">Erforderliche Member für **iobjectmodelprovider**</span><span class="sxs-lookup"><span data-stu-id="6ce49-130">Required Members for **IObjectModelProvider**</span></span>

<span data-ttu-id="6ce49-131">Zum Implementieren der [**iobjectmodelprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) -Schnittstelle ist die folgende Methode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6ce49-131">The following method is required for implementing the [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) interface.</span></span>



| <span data-ttu-id="6ce49-132">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="6ce49-132">Required members</span></span>                                                                             | <span data-ttu-id="6ce49-133">Memberart</span><span class="sxs-lookup"><span data-stu-id="6ce49-133">Member type</span></span> | <span data-ttu-id="6ce49-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ce49-134">Notes</span></span>                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ce49-135">**Getunderlyingobjectmodel**</span><span class="sxs-lookup"><span data-stu-id="6ce49-135">**GetUnderlyingObjectModel**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | <span data-ttu-id="6ce49-136">Methode</span><span class="sxs-lookup"><span data-stu-id="6ce49-136">Method</span></span>      | <span data-ttu-id="6ce49-137">Gibt einen com-Zeiger auf das zugrunde liegende Objektmodell zurück.</span><span class="sxs-lookup"><span data-stu-id="6ce49-137">Returns a COM pointer to the underlying object model.</span></span> <span data-ttu-id="6ce49-138">Der Client wird erwartet, dass die [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode aufgerufen wird, um bestimmte Objektmodell Zeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ce49-138">The client is expected to call the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to retrieve specific object model pointers.</span></span> |



 

<span data-ttu-id="6ce49-139">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6ce49-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ce49-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ce49-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ce49-141">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="6ce49-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="6ce49-142">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="6ce49-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="6ce49-143">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="6ce49-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 
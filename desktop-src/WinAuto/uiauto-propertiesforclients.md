---
title: Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen
description: Eigenschaften für iuiautomationelement-Objekte enthalten Informationen über Benutzeroberflächen Elemente, in der Regel Steuerelemente.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- Clients, Abrufen von Benutzeroberflächenautomatisierungs-Elementen
- Clients, Benutzeroberflächenautomatisierungs-Elemente
- Clients, Eigenschaften
- Clients, Abrufen von Eigenschaften
- Clients, Benutzeroberflächenautomatisierungs-Eigenschaften
- Benutzeroberflächen Automatisierung, Abrufen von Elementen
- Benutzeroberflächen Automatisierung, Elemente
- Benutzeroberflächen Automatisierung, Eigenschaften
- Benutzeroberflächen Automatisierung, Abrufen von Eigenschaften
- Abrufen von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337863"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a><span data-ttu-id="92e73-113">Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen</span><span class="sxs-lookup"><span data-stu-id="92e73-113">Retrieving Properties from UI Automation Elements</span></span>

<span data-ttu-id="92e73-114">Eigenschaften für [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Objekte enthalten Informationen über Benutzeroberflächen Elemente, in der Regel Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="92e73-114">Properties on [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) objects contain information about UI elements, usually controls.</span></span> <span data-ttu-id="92e73-115">Die Eigenschaften eines Elements sind generisch. Das heißt, nicht spezifisch für einen Steuer ungstyp.</span><span class="sxs-lookup"><span data-stu-id="92e73-115">The properties of an element are generic; that is, not specific to a control type.</span></span> <span data-ttu-id="92e73-116">Steuerelement spezifische Eigenschaften eines Elements werden von seinen Steuerelement Muster-Schnittstellen verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="92e73-116">Control-specific properties of an element are exposed by its control pattern interfaces.</span></span>

<span data-ttu-id="92e73-117">Microsoft UI Automation-Eigenschaften sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="92e73-117">Microsoft UI Automation properties are read-only.</span></span> <span data-ttu-id="92e73-118">Um Eigenschaften eines Steuerelements festzulegen, müssen Sie die Methoden des entsprechenden Steuerelementmusters verwenden.</span><span class="sxs-lookup"><span data-stu-id="92e73-118">To set properties of a control, you must use the methods of the appropriate control pattern.</span></span> <span data-ttu-id="92e73-119">Verwenden Sie z. b. [**iuiautomationscrollpattern:: Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) , um die Positionswerte eines scrollfensters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="92e73-119">For example, use [**IUIAutomationScrollPattern::Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) to change the position values of a scrolling window.</span></span>

<span data-ttu-id="92e73-120">Um die Leistung zu verbessern, können Eigenschaftswerte von Steuerelementen und Steuerelement Mustern zwischengespeichert werden, wenn Elemente abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92e73-120">To improve performance, property values of controls and control patterns can be cached when elements are retrieved.</span></span> <span data-ttu-id="92e73-121">Weitere Informationen finden Sie unter zwischen [Speichern von Eigenschaften der Benutzeroberflächen Automatisierung und Steuerelement Mustern](uiauto-cachingforclients.md).</span><span class="sxs-lookup"><span data-stu-id="92e73-121">For more information, see [Caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).</span></span>

<span data-ttu-id="92e73-122">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="92e73-122">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="92e73-123">Eigenschaften-IDs</span><span class="sxs-lookup"><span data-stu-id="92e73-123">Property IDs</span></span>](#property-ids)
-   [<span data-ttu-id="92e73-124">Eigenschaftsbedingungen</span><span class="sxs-lookup"><span data-stu-id="92e73-124">Property Conditions</span></span>](#property-conditions)
-   [<span data-ttu-id="92e73-125">Abrufen von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92e73-125">Retrieving Properties</span></span>](#retrieving-properties)
-   [<span data-ttu-id="92e73-126">Standardeigenschaftswerte</span><span class="sxs-lookup"><span data-stu-id="92e73-126">Default Property Values</span></span>](#default-property-values)
-   [<span data-ttu-id="92e73-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92e73-127">Related topics</span></span>](#related-topics)

## <a name="property-ids"></a><span data-ttu-id="92e73-128">Eigenschaften-IDs</span><span class="sxs-lookup"><span data-stu-id="92e73-128">Property IDs</span></span>

<span data-ttu-id="92e73-129">Eigenschafts Bezeichner werden in "UIAutomationClient. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="92e73-129">Property identifiers are defined in Uiautomationclient.h.</span></span> <span data-ttu-id="92e73-130">Sie werden verwendet, um Eigenschaften anzugeben, wenn Sie Eigenschaften geänderte Ereignisse abonnieren, Eigenschaftswerte abrufen und Eigenschafts Bedingungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="92e73-130">They are used to specify properties when you subscribe to property-changed events, retrieve property values, and construct property conditions.</span></span> <span data-ttu-id="92e73-131">Eigenschafts Bezeichner identifizieren auch die Eigenschaft, die sich geändert hat, wenn [**iuiautomationpropertychangedebug:: shandpropertychangedebug**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="92e73-131">Property identifiers also identify the property that has changed when [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) is called.</span></span>

<span data-ttu-id="92e73-132">Eine Liste der Benutzeroberflächenautomatisierungs-Eigenschaften Bezeichner finden Sie unter [Property Identifiers](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="92e73-132">For a list of UI Automation property identifiers, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-conditions"></a><span data-ttu-id="92e73-133">Eigenschaftsbedingungen</span><span class="sxs-lookup"><span data-stu-id="92e73-133">Property Conditions</span></span>

<span data-ttu-id="92e73-134">Die Eigenschaften-IDs werden zum Erstellen von [**iuiautomationpropertycondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) -Objekten verwendet, die für die Suche nach Benutzeroberflächenautomatisierungs-Elementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92e73-134">The property IDs are used in constructing [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) objects that are used to find UI Automation elements.</span></span> <span data-ttu-id="92e73-135">Angenommen, Sie möchten ein Element mit einem bestimmten Namen oder alle aktivierten Steuerelemente suchen.</span><span class="sxs-lookup"><span data-stu-id="92e73-135">For example, you might want to find an element that has a certain name, or all controls that are enabled.</span></span> <span data-ttu-id="92e73-136">Jede Eigenschafts Bedingung gibt einen Eigenschafts Bezeichner und den Wert an, dem die Eigenschaft entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="92e73-136">Each property condition specifies a property identifier and the value that the property must match.</span></span>

<span data-ttu-id="92e73-137">Weitere Informationen finden Sie unter den folgenden Referenzthemen:</span><span class="sxs-lookup"><span data-stu-id="92e73-137">For more information, see the following reference topics:</span></span>

-   [<span data-ttu-id="92e73-138">**Iuiautomation:: kreatepropertycondition**</span><span class="sxs-lookup"><span data-stu-id="92e73-138">**IUIAutomation::CreatePropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [<span data-ttu-id="92e73-139">**Iuiautomation:: kreatepropertyconditionex**</span><span class="sxs-lookup"><span data-stu-id="92e73-139">**IUIAutomation::CreatePropertyConditionEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [<span data-ttu-id="92e73-140">**Iuiautomationelement:: FindFirst**</span><span class="sxs-lookup"><span data-stu-id="92e73-140">**IUIAutomationElement::FindFirst**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [<span data-ttu-id="92e73-141">**Iuiautomationelement:: FindAll**</span><span class="sxs-lookup"><span data-stu-id="92e73-141">**IUIAutomationElement::FindAll**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a><span data-ttu-id="92e73-142">Abrufen von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92e73-142">Retrieving Properties</span></span>

<span data-ttu-id="92e73-143">Einige generische Eigenschaften und alle Steuerelement Muster Eigenschaften sind als Eigenschaften in der [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -oder Steuerelement Muster-Schnittstelle verfügbar und können mithilfe eines Accessors, wie z. b. [**iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) oder [**cacheddockposition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition), abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="92e73-143">Some generic properties, and all control pattern properties, are available as properties on the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) or control pattern interface and can be retrieved by using an accessor, such as [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) or [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span></span>

<span data-ttu-id="92e73-144">Darüber hinaus können alle aktuellen oder zwischengespeicherten Eigenschaften (mit Ausnahme der Eigenschaften von Steuerelement Mustern) mithilfe einer der folgenden Methoden abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="92e73-144">In addition, any current or cached property (other than control pattern properties) can be retrieved by using one of the following methods:</span></span>

-   [<span data-ttu-id="92e73-145">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="92e73-145">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [<span data-ttu-id="92e73-146">**Getcurrentpropertyvalueex**</span><span class="sxs-lookup"><span data-stu-id="92e73-146">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [<span data-ttu-id="92e73-147">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="92e73-147">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [<span data-ttu-id="92e73-148">**Getcachedpropertyvalueex**</span><span class="sxs-lookup"><span data-stu-id="92e73-148">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

<span data-ttu-id="92e73-149">Diese Methoden bieten eine etwas bessere Leistung und Zugriff auf den vollständigen Bereich von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92e73-149">These methods offer slightly better performance and access to the full range of properties.</span></span> <span data-ttu-id="92e73-150">Werte werden jedoch in [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Strukturen zurückgegeben, während die einzelnen Eigenschaftenaccessoren den Wert in den entsprechenden Typ umwandeln.</span><span class="sxs-lookup"><span data-stu-id="92e73-150">However, values are returned in [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structures, whereas the individual property accessors cast the value to the appropriate type.</span></span>

## <a name="default-property-values"></a><span data-ttu-id="92e73-151">Standardeigenschaftswerte</span><span class="sxs-lookup"><span data-stu-id="92e73-151">Default Property Values</span></span>

<span data-ttu-id="92e73-152">Wenn ein Benutzeroberflächenautomatisierungs-Anbieter eine Eigenschaft nicht implementiert, kann die Benutzeroberflächen Automatisierung einen Standardwert bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="92e73-152">If a UI Automation provider does not implement a property, UI Automation can supply a default value.</span></span> <span data-ttu-id="92e73-153">Wenn z. b. der Anbieter für ein Steuerelement die von [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)identifizierte Eigenschaft nicht unterstützt, gibt die Benutzeroberflächen Automatisierung eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="92e73-153">For example, if the provider for a control does not support the property identified by [**UIA\_HelpTextPropertyId**](uiauto-automation-element-propids.md), UI Automation returns an empty string.</span></span> <span data-ttu-id="92e73-154">Wenn der Anbieter die durch [**UIA \_ isdockpatternavailablepropertyid**](uiauto-control-pattern-availability-propids.md)identifizierte Eigenschaft nicht unterstützt, gibt die Benutzeroberflächen Automatisierung auf ähnliche Weise **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="92e73-154">Similarly, if the provider does not support the property identified by [**UIA\_IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), UI Automation returns **FALSE**.</span></span>

<span data-ttu-id="92e73-155">Der Unterschied zwischen [**iuiautomationelement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) und [**getcurrentpropertyvalueex**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (und zwischen ähnlichen Methoden Paaren) besteht darin, dass die "ex"-Methode angeben kann, dass kein Standardwert zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="92e73-155">The difference between [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) and [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (and between similar pairs of methods) is that the "Ex" method can specify that no default value is to be returned.</span></span> <span data-ttu-id="92e73-156">In diesem Fall ist der Rückgabewert eine besondere eindeutige Konstante, die angibt, dass die Eigenschaft nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="92e73-156">In this case, the return value is a special unique constant, indicating that the property is not supported.</span></span> <span data-ttu-id="92e73-157">Beim Empfang dieses Werts kann die Anwendung einen eigenen Wert bereitstellen oder die-Eigenschaft einfach ignorieren.</span><span class="sxs-lookup"><span data-stu-id="92e73-157">On receiving this value, the application can supply its own value or simply ignore the property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92e73-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92e73-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="92e73-159">**Licher**</span><span class="sxs-lookup"><span data-stu-id="92e73-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="92e73-160">Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92e73-160">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="92e73-161">Eigenschaftsbezeichner</span><span class="sxs-lookup"><span data-stu-id="92e73-161">Property Identifiers</span></span>](uiauto-entry-propids.md)
</dt> </dl>

 

 
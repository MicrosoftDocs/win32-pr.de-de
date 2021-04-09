---
title: Hinzufügen von Funktionen für die Benutzeroberflächen Automatisierung zu Active Accessibility Servern
description: Steuerelemente, die nicht über einen Microsoft-Benutzeroberflächenautomatisierungs-Anbieter verfügen, aber IAccessible implementieren, können problemlos aktualisiert werden, um einige Funktionen zur Automatisierung der Benutzeroberfläche bereitzustellen
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Benutzeroberflächen Automatisierung, Active Accessibility Server
- Benutzeroberflächen Automatisierung, Microsoft Active Accessibility-Server
- Benutzeroberflächen Automatisierung, IAccessible
- UI-Automatisierung, iaccessibleex
- Benutzeroberflächen Automatisierung, verfügbar machen von iaccessibleex
- Benutzeroberflächen Automatisierung, Implementieren von iaccessibleex
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- verfügbar machen von iaccessibleex
- Implementieren von iaccessibleex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948797"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a><span data-ttu-id="08cfb-115">Hinzufügen von Funktionen für die Benutzeroberflächen Automatisierung zu Active Accessibility Servern</span><span class="sxs-lookup"><span data-stu-id="08cfb-115">Adding UI Automation Functionality to Active Accessibility Servers</span></span>

<span data-ttu-id="08cfb-116">Steuerelemente, die nicht über einen Microsoft-Benutzeroberflächenautomatisierungs-Anbieter verfügen, aber [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren, können problemlos aktualisiert werden, um einige Funktionen zur [**Automatisierung der Benutzeroberfläche bereit**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) zustellen</span><span class="sxs-lookup"><span data-stu-id="08cfb-116">Controls that do not have a Microsoft UI Automation provider but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) can easily be upgraded to provide some UI Automation functionality, by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="08cfb-117">Diese Schnittstelle ermöglicht es dem Steuerelement, Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster verfügbar zu machen, ohne dass eine vollständige Implementierung von Schnittstellen für Benutzeroberflächenautomatisierungs-Anbieter wie [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)</span><span class="sxs-lookup"><span data-stu-id="08cfb-117">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="08cfb-118">Zum Implementieren von **iaccessibleex** muss die grundlegende Microsoft Active Accessibility-Objekthierarchie keine Fehler oder Inkonsistenzen enthalten (z. b. ein untergeordnetes Objekt, dessen übergeordnetes Objekt Sie nicht als untergeordnetes Element aufführt) und kein Konflikt mit Benutzeroberflächenautomatisierungs-Spezifikationen</span><span class="sxs-lookup"><span data-stu-id="08cfb-118">To implement **IAccessibleEx**, the baseline Microsoft Active Accessibility object hierarchy must contain no errors or inconsistencies (such as a child object whose parent object does not list it as a child), and must not conflict with UI Automation specifications.</span></span> <span data-ttu-id="08cfb-119">Wenn die Microsoft Active Accessibility-Objekthierarchie diese Anforderungen erfüllt, ist Sie ein guter Kandidat für das Hinzufügen von Funktionen mithilfe von **iaccessibleex**. Andernfalls müssen Sie die Benutzeroberflächen Automatisierung allein oder zusammen mit der Microsoft Active Accessibility-Implementierung implementieren.</span><span class="sxs-lookup"><span data-stu-id="08cfb-119">If the Microsoft Active Accessibility object hierarchy meets these requirements, it is a good candidate for adding functionality by using **IAccessibleEx**; otherwise, you must implement UI Automation alone or alongside the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="08cfb-120">Nehmen Sie den Fall eines benutzerdefinierten Steuer Elements, das über einen Bereichs Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="08cfb-120">Take the case of a custom control that has a range value.</span></span> <span data-ttu-id="08cfb-121">Der Microsoft Active Accessibility Server für das Steuerelement definiert seine Rolle und kann seinen aktuellen Wert zurückgeben. es fehlen jedoch die Möglichkeit, den minimalen und maximalen Wert des Steuer Elements zurückzugeben, da diese Eigenschaften nicht in Microsoft Active Accessibility definiert sind.</span><span class="sxs-lookup"><span data-stu-id="08cfb-121">The Microsoft Active Accessibility server for the control defines its role, and is able to return its current value, but lacks the means to return the minimum and maximum values of the control, because these properties are not defined in Microsoft Active Accessibility.</span></span> <span data-ttu-id="08cfb-122">Ein Benutzeroberflächenautomatisierungs-Client kann die Rolle, den aktuellen Wert und andere Eigenschaften von Microsoft Active Accessibility abrufen, da der Benutzeroberflächenautomatisierungs-Kern diese über [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="08cfb-122">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="08cfb-123">Ohne Zugriff auf eine [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) -Schnittstelle für das Objekt kann die Benutzeroberflächen Automatisierung jedoch auch nicht die maximalen und minimalen Werte abrufen.</span><span class="sxs-lookup"><span data-stu-id="08cfb-123">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="08cfb-124">Der Steuerelement Entwickler könnte einen kompletten Benutzeroberflächenautomatisierungs-Anbieter für das Steuerelement bereitstellen. Dies würde jedoch bedeuten, dass ein Großteil der vorhandenen Funktionen der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung duplizieren würde, z. b. Navigation und allgemeine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08cfb-124">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="08cfb-125">Stattdessen kann sich der Entwickler weiterhin auf **IAccessible** verlassen, um diese Funktionalität bereitzustellen, und gleichzeitig Unterstützung für Steuerelement spezifische Eigenschaften durch [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="08cfb-125">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

<span data-ttu-id="08cfb-126">Zum Aktualisieren des benutzerdefinierten Steuer Elements sind die folgenden Hauptschritte erforderlich:</span><span class="sxs-lookup"><span data-stu-id="08cfb-126">Updating the custom control requires these main steps:</span></span>

-   <span data-ttu-id="08cfb-127">Implementieren Sie [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) für das barrierefreie Objekt, sodass die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle für dieses oder ein separates Objekt gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="08cfb-127">Implement [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="08cfb-128">Implementieren Sie [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für das barrierefreie Objekt.</span><span class="sxs-lookup"><span data-stu-id="08cfb-128">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="08cfb-129">Erstellen Sie unterschiedliche barrierefreie Objekte für alle untergeordneten Elemente von Microsoft Active Accessibility, die in Microsoft Active Accessibility möglicherweise durch die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das übergeordnete Objekt (z. b. Listenelemente) repräsentiert wurden.</span><span class="sxs-lookup"><span data-stu-id="08cfb-129">Create distinct accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility might have been represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="08cfb-130">Implementieren Sie [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für diese Objekte.</span><span class="sxs-lookup"><span data-stu-id="08cfb-130">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="08cfb-131">Implementieren Sie [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) für alle zugänglichen Objekte.</span><span class="sxs-lookup"><span data-stu-id="08cfb-131">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="08cfb-132">Implementieren Sie die entsprechenden Steuerelement Muster-Schnittstellen für die barrierefreien Objekte.</span><span class="sxs-lookup"><span data-stu-id="08cfb-132">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

<span data-ttu-id="08cfb-133">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="08cfb-133">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="08cfb-134">Verfügbar machen von iaccessibleex</span><span class="sxs-lookup"><span data-stu-id="08cfb-134">Exposing IAccessibleEx</span></span>](#exposing-iaccessibleex)
-   [<span data-ttu-id="08cfb-135">Implementieren von iaccessibleex</span><span class="sxs-lookup"><span data-stu-id="08cfb-135">Implementing IAccessibleEx</span></span>](#implementing-iaccessibleex)
-   [<span data-ttu-id="08cfb-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08cfb-136">Related topics</span></span>](#related-topics)

## <a name="exposing-iaccessibleex"></a><span data-ttu-id="08cfb-137">Verfügbar machen von iaccessibleex</span><span class="sxs-lookup"><span data-stu-id="08cfb-137">Exposing IAccessibleEx</span></span>

<span data-ttu-id="08cfb-138">Da sich die Implementierung von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für ein Steuerelement in einem separaten Objekt befinden kann, können Client Anwendungen nicht auf [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) zurückgreifen, um diese Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="08cfb-138">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="08cfb-139">Stattdessen wird von Clients erwartet, dass [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="08cfb-139">Instead, clients are expected to call [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span></span> <span data-ttu-id="08cfb-140">In der folgenden Beispiel Implementierung dieser Methode wird davon ausgegangen, dass **iaccessibleex** nicht in einem separaten Objekt implementiert ist. Daher ruft die Methode einfach über **QueryInterface** auf.</span><span class="sxs-lookup"><span data-stu-id="08cfb-140">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a><span data-ttu-id="08cfb-141">Implementieren von iaccessibleex</span><span class="sxs-lookup"><span data-stu-id="08cfb-141">Implementing IAccessibleEx</span></span>

<span data-ttu-id="08cfb-142">Die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Methode, die von Interesse ist, ist [**getobjectforchild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span><span class="sxs-lookup"><span data-stu-id="08cfb-142">The method of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) that is of most interest is [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span></span> <span data-ttu-id="08cfb-143">Diese Methode ermöglicht es dem Microsoft Active Accessibility-Server, ein Barrierefreies Objekt (eines, das mindestens **iaccessibleex** verfügbar macht) für ein untergeordnetes Element zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08cfb-143">This method gives the Microsoft Active Accessibility server an opportunity to create an accessible object (one that exposes, at a minimum, **IAccessibleEx**) for a child item.</span></span> <span data-ttu-id="08cfb-144">In Microsoft Active Accessibility werden untergeordnete Elemente in der Regel nicht als barrierefreie Objekte, sondern als untergeordnete Elemente eines barrierefreien Objekts dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08cfb-144">In Microsoft Active Accessibility, child items typically are not represented as accessible objects but as children of an accessible object.</span></span> <span data-ttu-id="08cfb-145">Da die Benutzeroberflächen Automatisierung jedoch erfordert, dass jedes Element durch ein separates Barrierefreies Objekt dargestellt wird, muss **getobjectforchild** bei Bedarf ein separates Objekt für jedes untergeordnete Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="08cfb-145">However, because UI Automation requires that each element be represented by a separate accessible object, **GetObjectForChild** must create a separate object for each child on demand.</span></span>

<span data-ttu-id="08cfb-146">Die folgende Beispiel Implementierung gibt ein Barrierefreies Objekt für ein Element in einer benutzerdefinierten Listenansicht zurück.</span><span class="sxs-lookup"><span data-stu-id="08cfb-146">The following example implementation returns an accessible object for an item in a custom list view.</span></span>


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



<span data-ttu-id="08cfb-147">Eine vollständige Beispiel Implementierung finden [Sie unter Erstellen von benutzerdefinierten Steuerelementen, Teil 5: Verwenden von iaccessibleex zum Hinzufügen von Benutzeroberflächenautomatisierungs-Unterstützung zu einem benutzerdefinierten Steuer](/previous-versions/msdn10/cc307850(v=msdn.10)) Element auf MSDN</span><span class="sxs-lookup"><span data-stu-id="08cfb-147">For a complete sample implementation, see [Making Custom Controls Accessible, Part 5: Using IAccessibleEx to Add UI Automation Support to a Custom Control](/previous-versions/msdn10/cc307850(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08cfb-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08cfb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08cfb-149">Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="08cfb-149">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 
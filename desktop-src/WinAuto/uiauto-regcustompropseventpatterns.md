---
title: Registrieren von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelement Mustern
description: Bevor eine benutzerdefinierte Eigenschaft, ein Ereignis oder ein Steuerelement Muster verwendet werden kann, müssen sowohl der Anbieter als auch der Client die Eigenschaft, das Ereignis oder das Steuerelement Muster zur Laufzeit registrieren.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Benutzeroberflächen Automatisierung, benutzerdefinierte Eigenschaften
- UI-Automatisierung, Übersicht über Ereignisse
- UI-Automatisierung, Übersicht über Steuerelement Muster
- Benutzeroberflächen Automatisierung, registrieren benutzerdefinierter Eigenschaften
- Benutzeroberflächen Automatisierung, Registrieren von Ereignissen
- Benutzeroberflächen Automatisierung, Registrieren von Steuerelement Mustern
- benutzerdefinierte Eigenschaften, registrieren
- Ereignisse, registrieren
- Steuerelement Muster, registrieren
- registrieren, benutzerdefinierte Eigenschaften
- registrieren, Ereignisse
- registrieren, Steuerelement Muster
- Steuerelement Muster, Benutzer definiert
- Steuerelement Muster, Implementieren von benutzerdefinierten
- Implementieren von benutzerdefinierten Steuerelement Mustern
- benutzerdefinierte Steuerelement Muster
- Client-Wrapper
- Muster Handler
- Implementieren von Muster Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039430"
---
# <a name="register-custom-properties-events-and-control-patterns"></a><span data-ttu-id="6f1fb-122">Registrieren von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelement Mustern</span><span class="sxs-lookup"><span data-stu-id="6f1fb-122">Register custom properties, events, and control patterns</span></span>

<span data-ttu-id="6f1fb-123">Bevor eine benutzerdefinierte Eigenschaft, ein Ereignis oder ein Steuerelement Muster verwendet werden kann, müssen sowohl der Anbieter als auch der Client die Eigenschaft, das Ereignis oder das Steuerelement Muster zur Laufzeit registrieren.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-123">Before a custom property, event, or control pattern can be used, both the provider and the client must register the property, event, or control pattern at run time.</span></span> <span data-ttu-id="6f1fb-124">Die Registrierung wird global innerhalb eines Anwendungsprozesses wirksam und bleibt wirksam, bis der Prozess beendet oder das letzte Microsoft UI Automation-Element Objekt ([**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) oder [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) innerhalb des Prozesses freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-124">The registration is effective globally within an application process, and remains effective until the process closes or the last Microsoft UI Automation element object ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) or [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) is released within the process.</span></span>

<span data-ttu-id="6f1fb-125">Die Registrierung umfasst die Übergabe einer GUID an die Benutzeroberflächen Automatisierung sowie ausführliche Informationen über die benutzerdefinierte Eigenschaft, das Ereignis oder das Steuerelement Muster.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-125">Registation involves passing a GUID to UI Automation, along with detailed information about the custom property, event, or control pattern.</span></span> <span data-ttu-id="6f1fb-126">Der Versuch, dieselbe GUID ein zweites Mal mit denselben Informationen zu registrieren, ist erfolgreich, aber der Versuch, dieselbe GUID ein zweites Mal zu registrieren, aber mit unterschiedlichen Informationen (z. b. eine benutzerdefinierte Eigenschaft eines anderen Typs) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-126">Attempting to register the same GUID a second time with the same information will succeed, but attempting to register the same GUID a second time but with different information (for example, a custom property of a different type) will fail.</span></span> <span data-ttu-id="6f1fb-127">Wenn die benutzerdefinierte Spezifikation in Zukunft akzeptiert und in den Benutzeroberflächenautomatisierungs-Kern integriert wird, werden die benutzerdefinierten Registrierungsinformationen von der Benutzeroberflächen Automatisierung überprüft und der bereits registrierte Code anstelle der "offiziellen" Frameworkimplementierung verwendet, wodurch Anwendungs Kompatibilitätsprobleme minimiert werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-127">In the future, if the custom specification is accepted and integrated into the UI Automation core, UI Automation will validate the custom registration information and use the already registered code instead of the "official" framework implementation, thereby minimizing application compatibility issues.</span></span> <span data-ttu-id="6f1fb-128">Eigenschaften, Ereignisse oder Steuerelement Muster, die bereits registriert sind, können nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-128">You cannot remove properties, events, or control patterns that are already registered.</span></span>

<span data-ttu-id="6f1fb-129">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6f1fb-129">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="6f1fb-130">Registrieren von benutzerdefinierten Eigenschaften und Ereignissen</span><span class="sxs-lookup"><span data-stu-id="6f1fb-130">Registering Custom Properties and Events</span></span>](#registering-custom-properties-and-events)
-   [<span data-ttu-id="6f1fb-131">Implementieren von benutzerdefinierten Steuerelement Mustern</span><span class="sxs-lookup"><span data-stu-id="6f1fb-131">Implementing Custom Control Patterns</span></span>](#implementing-custom-control-patterns)
    -   [<span data-ttu-id="6f1fb-132">Der Client-Wrapper und der Muster Handler</span><span class="sxs-lookup"><span data-stu-id="6f1fb-132">The Client Wrapper and the Pattern Handler</span></span>](#the-client-wrapper-and-the-pattern-handler)
    -   [<span data-ttu-id="6f1fb-133">Implementieren des Client Wrappers</span><span class="sxs-lookup"><span data-stu-id="6f1fb-133">Implementing the Client Wrapper</span></span>](#implementing-the-client-wrapper)
    -   [<span data-ttu-id="6f1fb-134">Implementieren des Muster Handlers</span><span class="sxs-lookup"><span data-stu-id="6f1fb-134">Implementing the Pattern Handler</span></span>](#implementing-the-pattern-handler)
    -   [<span data-ttu-id="6f1fb-135">Registrieren eines benutzerdefinierten Steuerelement Musters</span><span class="sxs-lookup"><span data-stu-id="6f1fb-135">Registering a Custom Control Pattern</span></span>](#registering-a-custom-control-pattern)
    -   [<span data-ttu-id="6f1fb-136">Beispiel Implementierung eines benutzerdefinierten Steuerelement Musters</span><span class="sxs-lookup"><span data-stu-id="6f1fb-136">Example Implementation of a Custom Control Pattern</span></span>](#example-implementation-of-a-custom-control-pattern)
-   [<span data-ttu-id="6f1fb-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f1fb-137">Related topics</span></span>](#related-topics)

## <a name="registering-custom-properties-and-events"></a><span data-ttu-id="6f1fb-138">Registrieren von benutzerdefinierten Eigenschaften und Ereignissen</span><span class="sxs-lookup"><span data-stu-id="6f1fb-138">Registering Custom Properties and Events</span></span>

<span data-ttu-id="6f1fb-139">Wenn Sie eine benutzerdefinierte Eigenschaft oder ein Ereignis registrieren, können der Anbieter und der Client eine ID für die Eigenschaft oder das Ereignis abrufen, die dann an verschiedene API-Methoden weitergegeben werden kann, die IDs als Parameter annehmen.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-139">Registering a custom property or event enables the provider and client to obtain an ID for the property or event, which can then be passed to various API methods that take IDs as parameters.</span></span>

<span data-ttu-id="6f1fb-140">So registrieren Sie eine Eigenschaft oder ein Ereignis:</span><span class="sxs-lookup"><span data-stu-id="6f1fb-140">To register a property or event:</span></span>

1.  <span data-ttu-id="6f1fb-141">Definieren Sie eine GUID für die benutzerdefinierte Eigenschaft oder das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-141">Define a GUID for the custom property or event.</span></span>
2.  <span data-ttu-id="6f1fb-142">Füllen Sie eine [**uiautomationpropertyinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) -oder [**uiautomationeventinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) -Struktur mit Informationen über die Eigenschaft oder das Ereignis aus, einschließlich der GUID und einer nicht lokalisierbaren Zeichenfolge, die den Namen der benutzerdefinierten Eigenschaft oder des Ereignisses enthält.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-142">Fill a [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) or a [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure with information about the property or event, including the GUID and a nonlocalizable string that contains the name of the custom property or event.</span></span> <span data-ttu-id="6f1fb-143">Benutzerdefinierte Eigenschaften erfordern außerdem, dass der Datentyp der Eigenschaft angegeben wird, z. b. ob die Eigenschaft eine ganze Zahl oder eine Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-143">Custom properties also require the data type of the property to be specified, for example, whether the property holds an integer or a string.</span></span> <span data-ttu-id="6f1fb-144">Der Datentyp muss einer der folgenden Typen sein, die durch die [**uiautomationtype**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) -Enumeration angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-144">The data type must be one of the following types specified by the [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) enumeration.</span></span> <span data-ttu-id="6f1fb-145">Für benutzerdefinierte Eigenschaften werden keine anderen Datentypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-145">No other data types are supported for custom properties.</span></span>
    -   <span data-ttu-id="6f1fb-146">**Uiautomationtype \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-146">**UIAutomationType\_Bool**</span></span>
    -   <span data-ttu-id="6f1fb-147">**Uiautomationtype \_ Double**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-147">**UIAutomationType\_Double**</span></span>
    -   <span data-ttu-id="6f1fb-148">**Uiautomationtype- \_ Element**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-148">**UIAutomationType\_Element**</span></span>
    -   <span data-ttu-id="6f1fb-149">**Uiautomationtype \_ int**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-149">**UIAutomationType\_Int**</span></span>
    -   <span data-ttu-id="6f1fb-150">**Uiautomationtype- \_ Punkt**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-150">**UIAutomationType\_Point**</span></span>
    -   <span data-ttu-id="6f1fb-151">**Uiautomationtype- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-151">**UIAutomationType\_String**</span></span>
3.  <span data-ttu-id="6f1fb-152">Verwenden Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion, um eine Instanz des [**cuiautomationregistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) -Objekts zu erstellen und einen Zeiger auf die [**iuiautomationregistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) -Schnittstelle des Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-152">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
4.  <span data-ttu-id="6f1fb-153">Aufrufen der [**iuiautomationregistrar:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) -Methode oder der [**registerevent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) -Methode und übergeben der Adresse der [**uiautomationpropertyinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) -Struktur oder der [**uiautomationeventinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-153">Call the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method and pass the address of the [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structure or the [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure.</span></span>

<span data-ttu-id="6f1fb-154">Die [**iuiautomationregistrar:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) -Methode oder die [**registerevent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) -Methode gibt eine eigen schafts-ID oder Ereignis-ID zurück, die von einer Anwendung an eine beliebige Benutzeroberflächenautomatisierungs-Methode übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-154">The [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method returns a property ID or event ID that an application can pass to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="6f1fb-155">Beispielsweise können Sie eine registrierte eigen schafts-ID an die [**iuiautomationelement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) -Methode oder an die [**iuiautomation:: deatepropertycondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-155">For example, you can pass a registered property ID to the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method or to the [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) method.</span></span>

<span data-ttu-id="6f1fb-156">Im folgenden Beispiel wird veranschaulicht, wie eine benutzerdefinierte Eigenschaft registriert wird.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-156">The following example demonstrates how to register a custom property.</span></span>


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



<span data-ttu-id="6f1fb-157">Die von den Methoden [**iuiautomationregistrar:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) und [**registerevent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) abgerufenen Eigenschaften-und Ereignis Bezeichner sind nur im Kontext der Anwendung gültig, von der Sie abgerufen werden, und nur für die Dauer der Anwendungs Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-157">The property and event identifiers retrieved by the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) and [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) methods are valid only in the context of the application that retrieves them, and only for the duration of the application's lifetime.</span></span> <span data-ttu-id="6f1fb-158">Die Registrierungsmethoden können andere ganzzahlige Werte für dieselbe GUID zurückgeben, wenn Sie über verschiedene Lauf Zeit Instanzen derselben Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-158">The registration methods can return different integer values for the same GUID when it is called over different runtime instances of the same application.</span></span>

<span data-ttu-id="6f1fb-159">Es gibt keine Methode, die die Registrierung einer benutzerdefinierten Eigenschaft oder eines Ereignisses abhebt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-159">There is no method that unregisters a custom property or event.</span></span> <span data-ttu-id="6f1fb-160">Stattdessen wird die Registrierung implizit aufgehoben, wenn das letzte Benutzeroberflächenautomatisierungs-Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-160">Instead, they are implicitly unregistered when the last UI Automation object is released.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f1fb-161">Wenn es sich bei dem Code um einen MSAA-Client (Microsoft Active Accessibility) handelt, müssen Sie die [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) -Funktion aufzurufen, wenn Sie den Wert einer benutzerdefinierten Eigenschaft ändern.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-161">If your code is a Microsoft Active Accessibility (MSAA) client, you must call the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function when you change the value of a custom property.</span></span>

 

## <a name="implementing-custom-control-patterns"></a><span data-ttu-id="6f1fb-162">Implementieren von benutzerdefinierten Steuerelement Mustern</span><span class="sxs-lookup"><span data-stu-id="6f1fb-162">Implementing Custom Control Patterns</span></span>

<span data-ttu-id="6f1fb-163">Ein benutzerdefiniertes Steuerelement Muster ist nicht in der Benutzeroberflächenautomatisierungs-API enthalten, wird jedoch von einem Drittanbieter zur Laufzeit bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-163">A custom control pattern is not included in the UI Automation API, but is provided by a third party at run time.</span></span> <span data-ttu-id="6f1fb-164">Entwickler von Client-und Anbieter Anwendungen müssen zusammenarbeiten, um ein benutzerdefiniertes Steuerelement Muster zu definieren, einschließlich der Methoden, Eigenschaften und Ereignisse, die vom Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-164">Developers of client and provider applications must work together to define a custom control pattern, including the methods, properties, and events that the control pattern will support.</span></span> <span data-ttu-id="6f1fb-165">Nachdem Sie das-Steuerelement Muster definiert haben, müssen sowohl der Client als auch der Anbieter unterstützende Component Object Model (com)-Objekte zusammen mit Code implementieren, um das Steuerelement Muster zur Laufzeit zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-165">After defining the control pattern, both the client and the provider must implement supporting Component Object Model (COM) objects, along with code to register the control pattern at run time.</span></span> <span data-ttu-id="6f1fb-166">Ein benutzerdefiniertes Steuerelement Muster erfordert die Implementierung von zwei COM-Objekten: einen Client-Wrapper und einen Muster Handler.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-166">A custom control pattern requires the implementation of two COM objects: a client wrapper and a pattern handler.</span></span>

> [!Note]  
> <span data-ttu-id="6f1fb-167">In den Beispielen in den folgenden Themen wird veranschaulicht, wie Sie ein benutzerdefiniertes Steuerelement Muster implementieren, das die Funktionalität des vorhandenen [value](uiauto-implementingvalue.md) -Steuerelement Musters dupliziert.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-167">The examples in the following topics illustrate how to implement a custom control pattern that duplicates the functionality of the existing [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="6f1fb-168">Diese Beispiele sind nur für Lehrzwecke vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-168">These examples are for instructional purposes only.</span></span> <span data-ttu-id="6f1fb-169">Ein tatsächliches benutzerdefiniertes Steuerelement Muster sollte Funktionen bereitstellen, die nicht über die standardmäßigen Benutzeroberflächenautomatisierungs-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="6f1fb-169">An actual custom control pattern should provide functionality that is not available from the standard UI Automation control patterns.</span></span>

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a><span data-ttu-id="6f1fb-170">Der Client-Wrapper und der Muster Handler</span><span class="sxs-lookup"><span data-stu-id="6f1fb-170">The Client Wrapper and the Pattern Handler</span></span>

<span data-ttu-id="6f1fb-171">Der Client Wrapper implementiert die API, die vom Client verwendet wird, um Eigenschaften abzurufen und Methoden aufzurufen, die durch das benutzerdefinierte Steuerelement Muster verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-171">The client wrapper implements the API that is used by the client to retrieve properties and call methods exposed by the custom control pattern.</span></span> <span data-ttu-id="6f1fb-172">Die API wird als COM-Schnittstelle implementiert, die alle Eigenschafts Anforderungen und Methodenaufrufe an den Benutzeroberflächenautomatisierungs-Kern übergibt, der dann die Anforderungen und Aufrufe an den Anbieter marshallst.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-172">The API is implemented as a COM interface that passes all property requests and method calls to the UI Automation core, which then marshals the requests and calls to the provider.</span></span>

<span data-ttu-id="6f1fb-173">Der Code, der ein benutzerdefiniertes Steuerelement Muster registriert, muss eine Klassenfactory bereitstellen, mit der die Benutzeroberflächen Automatisierung Instanzen des Client Wrapper Objekts erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-173">The code that registers a custom control pattern must supply a class factory that UI Automation can use to create instances of the client wrapper object.</span></span> <span data-ttu-id="6f1fb-174">Wenn ein benutzerdefiniertes Steuerelement Muster erfolgreich registriert wird, gibt die Benutzeroberflächen Automatisierung einen [**iuiautomationpatterninstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) -Schnittstellen Zeiger zurück, der vom Client verwendet wird, um Eigenschaften Anforderungen und Methodenaufrufe an den Benutzeroberflächenautomatisierungs-Kern weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-174">When a custom control pattern is successfully registered, UI Automation returns an [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface pointer that is used by the client to forward property requests and methods calls to the UI Automation core.</span></span>

<span data-ttu-id="6f1fb-175">Auf der Anbieterseite nimmt der Benutzeroberflächenautomatisierungs-Kern die Eigenschaften Anforderungen und Methodenaufrufe vom Client an und übergibt sie an das musterhandlerobjekt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-175">On the provider side, the UI Automation core takes the property requests and method calls from the client and passes them to the pattern handler object.</span></span> <span data-ttu-id="6f1fb-176">Der Muster Handler ruft dann die entsprechenden Methoden auf der Anbieter Schnittstelle für das benutzerdefinierte Steuerelement Muster auf.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-176">The pattern handler then calls the appropriate methods on the provider interface for the custom control pattern.</span></span>

<span data-ttu-id="6f1fb-177">Der Code, der ein benutzerdefiniertes Steuerelement Muster registriert, erstellt das musterhandlerobjekt und stellt beim Registrieren des Steuerelement Musters eine Benutzeroberflächen Automatisierung mit einem Zeiger auf die [**iuiautomationpatternhandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) -Schnittstelle des Objekts bereit.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-177">The code that registers a custom control pattern creates the pattern handler object and, when registering the control pattern, provides UI Automation with a pointer to the object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span>

<span data-ttu-id="6f1fb-178">Das folgende Diagramm zeigt, wie ein Client Eigenschafts Anforderungs-oder-Methodenaufrufe vom Client-Wrapper über die Benutzeroberflächenautomatisierungs-Kernkomponenten an den Muster Handler und dann an die Anbieter Schnittstelle fließt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-178">The following diagram shows how a client property request or method call flows from the client wrapper, through the UI Automation core components to the pattern handler, and then to the provider interface.</span></span>

![Diagramm, das den Flow vom Client-Wrapper zum Muster Handler und-Anbieter anzeigt](images/custompatternsupport.jpg)

<span data-ttu-id="6f1fb-180&quot;>Die Objekte, die die Client Wrapper-und musterhandlerschnittstellen implementieren, müssen freigegeben sein.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6f1fb-180&quot;>The objects that implement the client wrapper and pattern handler interfaces must be free-threaded.</span></span> <span data-ttu-id=&quot;6f1fb-181&quot;>Außerdem muss der Benutzeroberflächenautomatisierungs-Kern in der Lage sein, die Objekte direkt ohne zwischenmarshallingcode aufzurufen.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6f1fb-181&quot;>Also, the UI Automation core must be able to call the objects directly without any intermediate marshaling code.</span></span>

### <a name=&quot;implementing-the-client-wrapper&quot;></a><span data-ttu-id=&quot;6f1fb-182&quot;>Implementieren des Client Wrappers</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6f1fb-182&quot;>Implementing the Client Wrapper</span></span>

<span data-ttu-id=&quot;6f1fb-183&quot;>Der Client Wrapper ist ein Objekt, das eine ixxxpattern-Schnittstelle verfügbar macht, mit der der Client Eigenschaften anfordert und Methoden aufruft, die vom benutzerdefinierten Steuerelement Muster unterstützt werden.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6f1fb-183&quot;>The client wrapper is an object that exposes an IXxxPattern interface that the client uses to request properties and call methods supported by the custom control pattern.</span></span> <span data-ttu-id=&quot;6f1fb-184&quot;>Die Schnittstelle besteht aus einem Paar von &quot;Getter&quot;-Methoden für jede unterstützte Eigenschaft (&quot;get \_ currentxxx&quot; und &quot;get \_ cachedxxx Method") und einer "Caller"-Methode für jede unterstützte Methode.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-184">The interface consists of a pair of "getter" methods for each supported property (get\_CurrentXxx and get\_CachedXxx method), and a "caller" method for each supported method.</span></span> <span data-ttu-id="6f1fb-185">Wenn das Objekt instanziiert wird, empfängt der Objektkonstruktor einen Zeiger auf die [**iuiautomationpatterninstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) -Schnittstelle, die vom Benutzeroberflächenautomatisierungs-Kern implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-185">When the object is instantiated, the object constructor receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface, which is implemented by the UI Automation core.</span></span> <span data-ttu-id="6f1fb-186">Die Methoden der ixxxpattern-Schnittstelle verwenden die [**iuiautomationpatterninstance:: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) -Methode und die [**CALLMETHOD-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) , um Eigenschafts Anforderungen und Methodenaufrufe an den Benutzeroberflächenautomatisierungs-Kern weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-186">The methods of the IXxxPattern interface use the [**IUIAutomationPatternInstance::GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) and [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) methods to forward property requests and method calls to the UI Automation core.</span></span>

<span data-ttu-id="6f1fb-187">Im folgenden Beispiel wird gezeigt, wie ein Client Wrapper Objekt für ein einfaches benutzerdefiniertes Steuerelement Muster implementiert wird, das eine einzelne Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-187">The following example shows how to implement a client wrapper object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="6f1fb-188">Ein komplexeres Beispiel finden Sie unter [Beispiel Implementierung eines benutzerdefinierten Steuerelement Musters](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="6f1fb-188">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a><span data-ttu-id="6f1fb-189">Implementieren des Muster Handlers</span><span class="sxs-lookup"><span data-stu-id="6f1fb-189">Implementing the Pattern Handler</span></span>

<span data-ttu-id="6f1fb-190">Der Muster Handler ist ein Objekt, das die [**iuiautomationpatternhandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-190">The pattern handler is an object that implements the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span> <span data-ttu-id="6f1fb-191">Diese Schnittstelle verfügt über zwei Methoden: [**iuiautomationpatternhandler:: kreateclientwrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) und [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span><span class="sxs-lookup"><span data-stu-id="6f1fb-191">This interface has two methods: [**IUIAutomationPatternHandler::CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) and [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span></span> <span data-ttu-id="6f1fb-192">Die Methode " **kreateclientwrapper** " wird vom Benutzeroberflächenautomatisierungs-Kern aufgerufen und empfängt einen Zeiger auf die [**iuiautomationpatterninstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-192">The **CreateClientWrapper** method is called by the UI Automation core and receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface.</span></span> <span data-ttu-id="6f1fb-193">" **Anateclientwrapper** " antwortet, indem das Client Wrapper Objekt instanziiert und der **iuiautomationpatterninstance** -Schnittstellen Zeiger an den clientwrapper-Konstruktor übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-193">**CreateClientWrapper** responds by instantiating the client wrapper object and passing the **IUIAutomationPatternInstance** interface pointer to the client wrapper constructor.</span></span>

<span data-ttu-id="6f1fb-194">Die [**dispatchmethode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) wird vom Benutzeroberflächenautomatisierungs-Kern verwendet, um Eigenschafts Anforderungen und Methodenaufrufe an die Anbieter Schnittstelle für das benutzerdefinierte Steuerelement Muster zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-194">The [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) method is used by the UI Automation core to pass property requests and method calls to the provider interface for the custom control pattern.</span></span> <span data-ttu-id="6f1fb-195">Parameter enthalten einen Zeiger auf die Anbieter Schnittstelle, den NULL basierten Index des aufzurufenden Eigenschaften Getters oder der aufzurufenden Methode und ein Array von [**uiautomationparameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) -Strukturen, die die Parameter enthalten, die an den Anbieter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-195">Parameters include a pointer to the provider interface, the zero-based index of the property getter or method being called, and an array of [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) structures that contain the parameters to pass to the provider.</span></span> <span data-ttu-id="6f1fb-196">Der Muster Handler antwortet, indem er den Index-Parameter prüft, um zu bestimmen, welche Anbieter Methode aufgerufen werden soll. Anschließend ruft er die Anbieter Schnittstelle auf und übergibt die in den **uiautomationparameter** -Strukturen enthaltenen Parameter.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-196">The pattern handler responds by checking the index parameter to determine which provider method to call, and then calls that provider interface, passing the parameters contained in the **UIAutomationParameter** structures.</span></span>

<span data-ttu-id="6f1fb-197">Das musterhandlerobjekt wird durch denselben Code instanziiert, der das benutzerdefinierte Steuerelement Muster registriert, bevor das Steuerelement Muster registriert wird.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-197">The pattern handler object is instantiated by the same code that registers the custom control pattern, before the control pattern is registered.</span></span> <span data-ttu-id="6f1fb-198">Der Code muss den [**iuiautomationpatternhandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) -Schnittstellen Zeiger des musterhandlerobjekts zum Zeitpunkt der Registrierung an den Benutzeroberflächenautomatisierungs-Kern übergeben.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-198">The code must pass the pattern handler object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface pointer to the UI Automation core at registration time.</span></span>

<span data-ttu-id="6f1fb-199">Im folgenden Beispiel wird gezeigt, wie ein musterhandlerobjekt für ein einfaches benutzerdefiniertes Steuerelement Muster implementiert wird, das eine einzelne Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-199">The following example shows how to implement a pattern handler object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="6f1fb-200">Ein komplexeres Beispiel finden Sie unter [Beispiel Implementierung eines benutzerdefinierten Steuerelement Musters](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="6f1fb-200">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a><span data-ttu-id="6f1fb-201">Registrieren eines benutzerdefinierten Steuerelement Musters</span><span class="sxs-lookup"><span data-stu-id="6f1fb-201">Registering a Custom Control Pattern</span></span>

<span data-ttu-id="6f1fb-202">Bevor Sie verwendet werden kann, muss ein benutzerdefiniertes Steuerelement Muster sowohl vom Anbieter als auch vom Client registriert werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-202">Before it can be used, a custom control pattern must be registered by both the provider and the client.</span></span> <span data-ttu-id="6f1fb-203">Die Registrierung stellt dem Benutzeroberflächenautomatisierungs-Kern ausführliche Informationen über das-Steuerelement Muster bereit und stellt dem Anbieter oder Client die Steuerelement Muster-ID und IDs für die Eigenschaften und Ereignisse bereit, die vom-Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-203">Registering provides the UI Automation core with detailed information about the control pattern, and supplies the provider or client with the control pattern ID, and IDs for the properties and events that are supported by the control pattern.</span></span> <span data-ttu-id="6f1fb-204">Auf der Anbieterseite muss das benutzerdefinierte Steuerelement Muster registriert werden, bevor das zugeordnete Steuerelement die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht oder zur gleichen Zeit behandelt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-204">On the provider side, the custom control pattern must be registered before the associated control handles the [**WM\_GETOBJECT**](wm-getobject.md) message, or at the same time.</span></span>

<span data-ttu-id="6f1fb-205">Wenn Sie ein benutzerdefiniertes Steuerelement Muster registrieren, liefert der Anbieter oder Client die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="6f1fb-205">When registering a custom control pattern, the provider or client supplies the following information:</span></span>

-   <span data-ttu-id="6f1fb-206">Der GUID des benutzerdefinierten Steuerelement Musters.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-206">The GUID of the custom control pattern.</span></span>
-   <span data-ttu-id="6f1fb-207">Eine nicht lokalisierbare Zeichenfolge, die den Namen des benutzerdefinierten Steuerelement Musters enthält.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-207">A nonlocalizable string containing the name of the custom control pattern.</span></span>
-   <span data-ttu-id="6f1fb-208">Der GUID der Anbieter Schnittstelle, die das benutzerdefinierte Steuerelement Muster unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-208">The GUID of the provider interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="6f1fb-209">Der GUID der Client Schnittstelle, die das benutzerdefinierte Steuerelement Muster unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-209">The GUID of the client interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="6f1fb-210">Ein Array von [**uiautomationpropertyinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) -Strukturen, die die Eigenschaften beschreiben, die vom benutzerdefinierten Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-210">An array of [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structures that describe the properties supported by the custom control pattern.</span></span> <span data-ttu-id="6f1fb-211">Für jede Eigenschaft müssen die GUID, der Eigenschaftsname und der Datentyp angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-211">For each property, the GUID, property name, and data type must be specified.</span></span>
-   <span data-ttu-id="6f1fb-212">Ein Array von [**uiautomationmethodinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) -Strukturen, die die Methoden beschreiben, die vom benutzerdefinierten Steuerelement Muster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-212">An array of [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) structures that describe the methods supported by the custom control pattern.</span></span> <span data-ttu-id="6f1fb-213">Für jede Methode enthält die-Struktur die folgenden Informationen: den Methodennamen, eine Anzahl von Parametern, eine Liste von Parameter Datentypen und eine Liste der Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-213">For each method, the structure includes the following information: the method name, a count of parameters, a list of parameter data types, and a list of the parameter names.</span></span>
-   <span data-ttu-id="6f1fb-214">Ein Array von [**uiautomationeventinfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) -Strukturen, die die Ereignisse beschreiben, die vom benutzerdefinierten Steuerelement Muster ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-214">An array of [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structures that describe the events raised by the custom control pattern.</span></span> <span data-ttu-id="6f1fb-215">Für jedes Ereignis müssen die GUID und der Ereignis Name angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-215">For each event, the GUID and event name must be specified.</span></span>
-   <span data-ttu-id="6f1fb-216">Die Adresse der [**iuiautomationpatternhandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) -Schnittstelle des musterhandlerobjekts, das das benutzerdefinierte Steuerelement Muster für Clients verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-216">The address of the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface of the pattern handler object that makes the custom control pattern available to clients.</span></span>

<span data-ttu-id="6f1fb-217">Um das benutzerdefinierte Steuerelement Muster zu registrieren, muss der Anbieter oder Client Code die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="6f1fb-217">To register the custom control pattern, the provider or client code must perform the following steps:</span></span>

1.  <span data-ttu-id="6f1fb-218">Füllen Sie eine [**uiautomationpatterninfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) -Struktur mit den vorangehenden Informationen aus.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-218">Fill a [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure with the preceding information.</span></span>
2.  <span data-ttu-id="6f1fb-219">Verwenden Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion, um eine Instanz des [**cuiautomationregistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) -Objekts zu erstellen und einen Zeiger auf die [**iuiautomationregistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) -Schnittstelle des Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-219">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
3.  <span data-ttu-id="6f1fb-220">Aufrufen der [**iuiautomationregistrar:: registerpattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) -Methode, wobei die Adresse der [**uiautomationpatterninfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) -Struktur übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-220">Call the [**IUIAutomationRegistrar::RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method, passing the address of the [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure.</span></span>

<span data-ttu-id="6f1fb-221">Die [**registerpattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) -Methode gibt eine Steuerelement Muster-ID zusammen mit einer Liste von Eigenschaften-IDs und Ereignis-IDs zurück.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-221">The [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method returns a control pattern ID, along with a list of property IDs and event IDs.</span></span> <span data-ttu-id="6f1fb-222">Eine Anwendung kann diese IDs an jede Benutzeroberflächen-Automatisierungs Methode übergeben, die einen solchen Bezeichner als Parameter annimmt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-222">An application can pass these IDs to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="6f1fb-223">Beispielsweise können Sie eine registrierte Muster-ID an die [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) -Methode übergeben, um einen Zeiger auf die Anbieter Schnittstelle für das Steuerelement Muster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-223">For example, you can pass a registered pattern ID to the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method to retrieve a pointer to the provider interface for the control pattern.</span></span>

<span data-ttu-id="6f1fb-224">Es gibt keine Methode, die die Registrierung eines benutzerdefinierten Steuerelement Musters abhebt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-224">There is no method that unregisters a custom control pattern.</span></span> <span data-ttu-id="6f1fb-225">Stattdessen wird die Registrierung implizit aufgehoben, wenn das letzte Benutzeroberflächenautomatisierungs-Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-225">Instead, it is implicitly unregistered when the last UI Automation object is released.</span></span>

<span data-ttu-id="6f1fb-226">Ein Beispiel, das zeigt, wie ein benutzerdefiniertes Steuerelement Muster registriert wird, finden Sie im folgenden Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-226">For an example that shows how to register a custom control pattern, see the following section.</span></span>

### <a name="example-implementation-of-a-custom-control-pattern"></a><span data-ttu-id="6f1fb-227">Beispiel Implementierung eines benutzerdefinierten Steuerelement Musters</span><span class="sxs-lookup"><span data-stu-id="6f1fb-227">Example Implementation of a Custom Control Pattern</span></span>

<span data-ttu-id="6f1fb-228">Dieser Abschnitt enthält Beispielcode, der veranschaulicht, wie die clientwrapper-und musterhandlerobjekte für ein benutzerdefiniertes Steuerelement Muster implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-228">This section contains example code that demonstrates how to implement the client wrapper and pattern handler objects for a custom control pattern.</span></span> <span data-ttu-id="6f1fb-229">Im Beispiel wird ein benutzerdefiniertes Steuerelement Muster implementiert, das auf dem [value](uiauto-implementingvalue.md) -Steuerelement Muster basiert.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-229">The example implements a custom control pattern that is based on the [Value](uiauto-implementingvalue.md) control pattern.</span></span>


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6f1fb-230">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f1fb-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6f1fb-231">**Licher**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6f1fb-232">Entwerfen von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelement Mustern</span><span class="sxs-lookup"><span data-stu-id="6f1fb-232">Designing Custom Properties, Events, and Control Patterns</span></span>](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[<span data-ttu-id="6f1fb-233">Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6f1fb-233">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="6f1fb-234">Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6f1fb-234">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="6f1fb-235">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="6f1fb-235">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 
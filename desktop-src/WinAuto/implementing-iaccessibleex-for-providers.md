---
title: Implementieren von iaccessibleex für Anbieter
description: In diesem Abschnitt wird erläutert, wie Sie Microsoft Benutzeroberflächenautomatisierungs-Anbieter Funktionen zu einem Microsoft Active Accessibility Server hinzufügen, indem Sie die iaccessibleex-Schnittstelle
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338668"
---
# <a name="implementing-iaccessibleex-for-providers"></a><span data-ttu-id="f0e03-103">Implementieren von iaccessibleex für Anbieter</span><span class="sxs-lookup"><span data-stu-id="f0e03-103">Implementing IAccessibleEx for Providers</span></span>

<span data-ttu-id="f0e03-104">In diesem Abschnitt wird erläutert, wie Sie Microsoft Benutzeroberflächenautomatisierungs-Anbieter Funktionen zu einem Microsoft Active Accessibility Server hinzufügen, indem Sie die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f0e03-104">This section explains how to add Microsoft UI Automation provider capabilities to a Microsoft Active Accessibility server by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>

<span data-ttu-id="f0e03-105">Berücksichtigen Sie vor der Implementierung von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)die folgenden Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="f0e03-105">Before implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), consider the following requirements:</span></span>

-   <span data-ttu-id="f0e03-106">Die grundlegende Microsoft Active Accessibility barrierefreie Objekthierarchie muss bereinigt werden.</span><span class="sxs-lookup"><span data-stu-id="f0e03-106">The baseline Microsoft Active Accessibility accessible object hierarchy must be clean.</span></span> <span data-ttu-id="f0e03-107">[**Iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) kann Probleme mit vorhandenen zugänglichen Objekt Hierarchien nicht beheben.</span><span class="sxs-lookup"><span data-stu-id="f0e03-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) cannot correct problems with existing accessible object hierarchies.</span></span> <span data-ttu-id="f0e03-108">Alle Probleme mit der Objektmodell Struktur müssen in der Microsoft Active Accessibility-Implementierung korrigiert werden, bevor **iaccessibleex** implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="f0e03-108">Any problems with the object model structure must be corrected in the Microsoft Active Accessibility implementation before implementing **IAccessibleEx**.</span></span>
-   <span data-ttu-id="f0e03-109">Die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung muss sowohl der Microsoft Active Accessibility Spezifikation als auch der Benutzeroberflächenautomatisierungs-Spezifikation entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f0e03-109">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation must comply with both the Microsoft Active Accessibility specification and the UI Automation specification.</span></span> <span data-ttu-id="f0e03-110">Tools sind verfügbar, um die Konformität unter beiden Spezifikationen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f0e03-110">Tools are available to validate compliance under both specifications.</span></span> <span data-ttu-id="f0e03-111">Weitere Informationen finden Sie unter Test [Tools](testing-tools.md) und [UI Automation Verify (UIA Verify) Test Automation Framework](https://www.codeplex.com/UIAutomationVerify/).</span><span class="sxs-lookup"><span data-stu-id="f0e03-111">For more information, see [Testing Tools](testing-tools.md) and [UI Automation Verify (UIA Verify) Test Automation Framework](https://www.codeplex.com/UIAutomationVerify/).</span></span>

<span data-ttu-id="f0e03-112">Die Implementierung von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) erfordert die folgenden Hauptschritte:</span><span class="sxs-lookup"><span data-stu-id="f0e03-112">Implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requires these main steps:</span></span>

-   <span data-ttu-id="f0e03-113">Implementieren Sie **IServiceProvider** für das barrierefreie Objekt, sodass die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle für dieses oder ein separates Objekt gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0e03-113">Implement **IServiceProvider** on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="f0e03-114">Implementieren Sie [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für das barrierefreie Objekt.</span><span class="sxs-lookup"><span data-stu-id="f0e03-114">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="f0e03-115">Erstellen Sie barrierefreie Objekte für alle untergeordneten Elemente von Microsoft Active Accessibility, die in Microsoft Active Accessibility durch die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das übergeordnete Objekt (z. b. Listenelemente) repräsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="f0e03-115">Create accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility are represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="f0e03-116">Implementieren Sie [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für diese Objekte.</span><span class="sxs-lookup"><span data-stu-id="f0e03-116">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="f0e03-117">Implementieren Sie [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) für alle zugänglichen Objekte.</span><span class="sxs-lookup"><span data-stu-id="f0e03-117">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="f0e03-118">Implementieren Sie die entsprechenden Steuerelement Muster-Schnittstellen für die barrierefreien Objekte.</span><span class="sxs-lookup"><span data-stu-id="f0e03-118">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

### <a name="implementing-the-iserviceprovider-interface"></a><span data-ttu-id="f0e03-119">Implementieren der IServiceProvider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f0e03-119">Implementing the IServiceProvider Interface</span></span>

<span data-ttu-id="f0e03-120">Da sich die Implementierung von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für ein Steuerelement in einem separaten Objekt befinden kann, können Client Anwendungen nicht auf [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) zurückgreifen, um diese Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0e03-120">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="f0e03-121">Stattdessen wird von Clients erwartet, dass **IServiceProvider:: QueryService** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f0e03-121">Instead, clients are expected to call **IServiceProvider::QueryService**.</span></span> <span data-ttu-id="f0e03-122">In der folgenden Beispiel Implementierung dieser Methode wird davon ausgegangen, dass **iaccessibleex** nicht in einem separaten Objekt implementiert ist. Daher ruft die Methode einfach über **QueryInterface** auf.</span><span class="sxs-lookup"><span data-stu-id="f0e03-122">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
           
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (ppvObject == NULL)
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
        return E_NOINTERFACE;
    }
};      
```



### <a name="implementing-the-iaccessibleex-interface"></a><span data-ttu-id="f0e03-123">Implementieren der iaccessibleex-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f0e03-123">Implementing the IAccessibleEx Interface</span></span>

<span data-ttu-id="f0e03-124">In Microsoft Active Accessibility wird ein UI-Element immer durch eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle und eine untergeordnete ID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f0e03-124">In Microsoft Active Accessibility, a UI element is always identified by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and a child ID.</span></span> <span data-ttu-id="f0e03-125">Eine einzelne Instanz von **IAccessible** kann mehrere Benutzeroberflächen Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="f0e03-125">A single instance of **IAccessible** can represent multiple UI elements.</span></span>

<span data-ttu-id="f0e03-126">Da jede [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Instanz nur ein einzelnes UI-Element darstellt, muss jedes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -und untergeordnete ID-Paar einer einzelnen **iaccessibleex** -Instanz zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f0e03-126">Because each [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance represents only a single UI element, each [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair must be mapped to a single **IAccessibleEx** instance.</span></span> <span data-ttu-id="f0e03-127">**Iaccessibleex** enthält zwei Methoden, um diese Zuordnung zu behandeln:</span><span class="sxs-lookup"><span data-stu-id="f0e03-127">**IAccessibleEx** includes two methods to handle this mapping:</span></span>

-   <span data-ttu-id="f0e03-128">[**Getobjectforchild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)– Ruft die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle für das angegebene untergeordnete Element ab.</span><span class="sxs-lookup"><span data-stu-id="f0e03-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)—Retrieves the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface for the specified child.</span></span> <span data-ttu-id="f0e03-129">Diese Methode gibt **null** zurück, wenn die **iaccessibleex** -Implementierung die angegebene untergeordnete ID nicht erkennt, keine **iaccessibleex** für das angegebene untergeordnete Element aufweist oder ein untergeordnetes Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0e03-129">This method returns **NULL** if the **IAccessibleEx** implementation does not recognize the specified child ID, does not have an **IAccessibleEx** for the specified child, or represents a child element.</span></span>
-   <span data-ttu-id="f0e03-130">[**Getiaccessiblepair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)– Ruft die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle und die untergeordnete ID für das [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Element ab.</span><span class="sxs-lookup"><span data-stu-id="f0e03-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)—Retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and child ID for the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) element.</span></span> <span data-ttu-id="f0e03-131">Bei **IAccessible** -Implementierungen, die keine untergeordnete ID verwenden, ruft diese Methode das entsprechende Objekt mit **IAccessible** und childID \_ selbst ab.</span><span class="sxs-lookup"><span data-stu-id="f0e03-131">For **IAccessible** implementations that do not use a child ID, this method retrieves the corresponding **IAccessible** object and CHILDID\_SELF.</span></span>

<span data-ttu-id="f0e03-132">Das folgende Beispiel zeigt die Implementierung der Methoden [**getobjectforchild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) und [**getiaccessiblepair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) für ein Element in einer benutzerdefinierten Listenansicht.</span><span class="sxs-lookup"><span data-stu-id="f0e03-132">The following example shows the implementation of the [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) and [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) methods for an item in a custom list view.</span></span> <span data-ttu-id="f0e03-133">Die-Methoden ermöglichen der Benutzeroberflächen Automatisierung, das [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -paar und das untergeordnete ID-Paar einer entsprechenden [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Instanz zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f0e03-133">The methods enable UI Automation to map the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair to a corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance.</span></span>


```C++
           
HRESULT CListboxAccessibleObject::GetObjectForChild(
    long idChild, IAccessibleEx **ppRetVal)
{ 
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;
    HRESULT hr = ValidateChildId(vChild);
    if (FAILED(hr))
    {
        return E_INVALIDARG;
    }
    // List item accessible objects are stored as an array of
    // pointers; for the purpose of this example it is assumed that 
    // the list contents will not change. Accessible objects are
    // created only when needed.
    if (itemProviders[idChild - 1] == NULL)
    {
        // Create an object that supports UI Automation and
        // IAccessibleEx for the item.
        itemProviders[idChild - 1] = 
          new CListItemAccessibleObject(idChild, 
          g_pListboxControl);
        if (itemProviders[idChild - 1] == NULL)
        {
            return E_OUTOFMEMORY;
        }
    }
    IAccessibleEx* pAccEx = static_cast<IAccessibleEx*>
      (itemProviders[idChild - 1]);
    if (pAccEx != NULL)
    {
      pAccEx->AddRef();
    }
    *ppRetVal = pAccEx;
    return S_OK; 
}

HRESULT CListItemAccessibleObject::GetIAccessiblePair(
    IAccessible **ppAcc, long *pidChild)
{ 
    if (ppAcc == NULL || pidChild == NULL)
    {
        return E_INVALIDARG;   
    }

                CListboxAccessibleObject* pParent = 
        m_control->GetAccessibleObject();

    HRESULT hr = pParent->QueryInterface( 
        __uuidof(IAccessible), (void**)ppAcc);
    if (FAILED(hr))
    {
        *pidChild = 0;
        return E_NOINTERFACE;
    }
    *pidChild = m_childID; 
    return S_OK; 
}
}
```



<span data-ttu-id="f0e03-134">Wenn eine barrierefreie Objekt Implementierung keine untergeordnete ID verwendet, können die Methoden dennoch implementiert werden, wie im folgenden Code Ausschnitt gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0e03-134">If an accessible object implementation does not use a child ID, the methods can still be implemented as shown in the following code snippet.</span></span>


```C++
           

    // This sample implements IAccessibleEx on the same object; it could use a tear-off
    // or inner object instead.
    class MyAccessibleImpl: public IAccessible,
                        public IAccessibleEx,
                        public IRawElementProviderSimple
    {
    public:
    ...
   HRESULT STDMETHODCALLTYPE GetObjectForChild( long idChild, IAccessibleEx **ppRetVal )
    {
        // This implementation does not support child IDs.
        *ppRetVal = NULL;
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE GetIAccessiblePair( IAccessible ** ppAcc, long * pidChild )
    {
        // This implementation assumes that IAccessibleEx is implemented on same object as
        // IAccessible.
        *ppAcc = static_cast<IAccessible *>(this);
        (*ppAcc)->AddRef();
        *pidChild = CHILDID_SELF;
        return S_OK;
    }
```



### <a name="implement-the-irawelementprovidersimple-interface"></a><span data-ttu-id="f0e03-135">Implementieren der IRawElementProviderSimple-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f0e03-135">Implement the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="f0e03-136">Server verwenden " [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) ", um Informationen über Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster verfügbar zu machen</span><span class="sxs-lookup"><span data-stu-id="f0e03-136">Servers use [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) to expose information about UI Automation properties and control patterns.</span></span> <span data-ttu-id="f0e03-137">**IRawElementProviderSimple** umfasst die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="f0e03-137">**IRawElementProviderSimple** includes the following methods:</span></span>

-   <span data-ttu-id="f0e03-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)– diese Methode wird verwendet, um Steuerelement Muster-Schnittstellen verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="f0e03-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)—This method is used to expose control pattern interfaces.</span></span> <span data-ttu-id="f0e03-139">Es gibt ein Objekt zurück, das das angegebene Steuerelement Muster unterstützt, oder **null** , wenn das Steuerelement Muster nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f0e03-139">It returns an object that supports the specified control pattern, or **NULL** if the control pattern is not supported.</span></span>
-   <span data-ttu-id="f0e03-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)– diese Methode wird verwendet, um Eigenschaftswerte für die Benutzeroberflächen Automatisierung verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="f0e03-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)—This method is used to expose UI Automation property values.</span></span>
-   <span data-ttu-id="f0e03-141">" [**Hustrawelementprovider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)" – Diese Methode wird nicht mit [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0e03-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>
-   <span data-ttu-id="f0e03-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)– diese Methode wird nicht mit [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0e03-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>

<span data-ttu-id="f0e03-143">Ein [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Server macht Steuerelement Muster durch Implementieren von [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0e03-143">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server exposes control patterns by implementing [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span></span> <span data-ttu-id="f0e03-144">Diese Methode nimmt einen ganzzahligen Parameter an, der das-Steuerelement Muster angibt.</span><span class="sxs-lookup"><span data-stu-id="f0e03-144">This method takes an integer parameter that specifies the control pattern.</span></span> <span data-ttu-id="f0e03-145">Der Server gibt **null** zurück, wenn das Muster nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f0e03-145">The server returns **NULL** if the pattern is not supported.</span></span> <span data-ttu-id="f0e03-146">Wenn die Steuerelement Muster Schnittstelle unterstützt wird, geben Server einen [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Wert zurück, und der Client ruft dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um das entsprechende Steuerelement Muster zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0e03-146">If the control pattern interface is supported, servers return an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) and the client then calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the appropriate control pattern.</span></span>

<span data-ttu-id="f0e03-147">Ein [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Server kann Benutzeroberflächenautomatisierungs-Eigenschaften (z. b. LabeledBy und isrequirements dforform) unterstützen, indem er [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) implementiert und eine ganzzahlige PropertyId bereitstellt, die die Eigenschaft als Parameter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f0e03-147">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server can support UI Automation properties (such as LabeledBy, and IsRequiredForForm) by implementing [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) and supplying an integer PROPERTYID identifying the property as a parameter.</span></span> <span data-ttu-id="f0e03-148">Dieses Verfahren gilt nur für Benutzeroberflächenautomatisierungs-Eigenschaften, die nicht in einer Steuerelement Muster-Schnittstelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f0e03-148">This technique applies only to UI Automation properties that are not included in a control pattern interface.</span></span> <span data-ttu-id="f0e03-149">Eigenschaften, die einer Steuerelement Muster Schnittstelle zugeordnet sind, werden über die Steuerelement Muster-Schnittstellen Methode verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="f0e03-149">Properties associated with a control pattern interface are exposed through the control pattern interface method.</span></span> <span data-ttu-id="f0e03-150">Beispielsweise würde die issgewählt-Eigenschaft des [SelectionItem](uiauto-implementingselectionitem.md) -Steuerelement Musters mit [**ISelectionItemProvider:: get \_ issgewählt**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="f0e03-150">For example, the IsSelected property from the [SelectionItem](uiauto-implementingselectionitem.md) control pattern would be exposed with [**ISelectionItemProvider::get\_IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span></span>

 

 
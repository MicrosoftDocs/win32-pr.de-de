---
title: Verwenden von iaccessibleex von einem Client
description: In diesem Thema wird erläutert, wie Clients auf die iaccessibleex-Implementierung eines Servers zugreifen und diese zum Abrufen von Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Mustern für Benutzeroberflächen Elemente verwenden.
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b14b935bd7ed432ea4d378034763635309213f
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104391210"
---
# <a name="using-iaccessibleex-from-a-client"></a><span data-ttu-id="50b7d-103">Verwenden von iaccessibleex von einem Client</span><span class="sxs-lookup"><span data-stu-id="50b7d-103">Using IAccessibleEx from a Client</span></span>

<span data-ttu-id="50b7d-104">In diesem Thema wird erläutert, wie Clients auf die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung eines Servers zugreifen und diese zum Abrufen von Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Mustern für Benutzeroberflächen Elemente verwenden.</span><span class="sxs-lookup"><span data-stu-id="50b7d-104">This topic explains how clients access the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation of a server and use it to get UI Automation properties and control patterns for UI elements.</span></span>

<span data-ttu-id="50b7d-105">Bei den Prozeduren und Beispielen in diesem Abschnitt wird davon ausgegangen, dass es sich um einen bereits in Bearbeitung [**baren Client handelt und um einen vorhandenen**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Microsoft Active Accessibility-Server.</span><span class="sxs-lookup"><span data-stu-id="50b7d-105">The procedures and examples in this section assume an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) client that is already in-process, and an existing Microsoft Active Accessibility server.</span></span> <span data-ttu-id="50b7d-106">Außerdem wird davon ausgegangen, dass der Client bereits ein **IAccessible** -Objekt mit einer der frameworkframeworkfunktionen wie [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="50b7d-106">They also assume that the client has already obtained an **IAccessible** object by using one of the accessibility framework functions such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a><span data-ttu-id="50b7d-107">Abrufen einer iaccessibleex-Schnittstelle von der IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="50b7d-107">Obtaining an IAccessibleEx Interface from the IAccessible Interface</span></span>

<span data-ttu-id="50b7d-108">Ein Client, der über eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für ein Barrierefreies Objekt verfügt, kann es mithilfe der folgenden Schritte zum Abrufen der entsprechenden [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle verwenden:</span><span class="sxs-lookup"><span data-stu-id="50b7d-108">A client that has an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for an accessible object can use it to obtain the corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface by following these steps:</span></span>

-   <span data-ttu-id="50b7d-109">Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das ursprüngliche [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt mit der IID \_ \_ uuidof (IServiceProvider).</span><span class="sxs-lookup"><span data-stu-id="50b7d-109">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with an IID of \_\_uuidof(IServiceProvider).</span></span>
-   <span data-ttu-id="50b7d-110">Aufrufen von **IServiceProvider:: QueryService** zum Abrufen von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).</span><span class="sxs-lookup"><span data-stu-id="50b7d-110">Call **IServiceProvider::QueryService** to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).</span></span>

### <a name="handling-the-child-id"></a><span data-ttu-id="50b7d-111">Behandeln der untergeordneten ID</span><span class="sxs-lookup"><span data-stu-id="50b7d-111">Handling the Child ID</span></span>

<span data-ttu-id="50b7d-112">Clients müssen auf Server mit einer anderen untergeordneten ID als childID Self vorbereitet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="50b7d-112">Clients must be prepared for servers with a child ID other than CHILDID\_SELF.</span></span> <span data-ttu-id="50b7d-113">Nachdem eine [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle von einer [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)-Schnittstelle erhalten hat, muss der Client [**iaccessibleex:: getobjectforchild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) aufrufen, wenn die untergeordnete ID nicht childID \_ Self ist (was ein übergeordnetes Objekt anzeigt).</span><span class="sxs-lookup"><span data-stu-id="50b7d-113">After obtaining an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface from an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), clients must call [**IAccessibleEx::GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) if the child ID is not CHILDID\_SELF (indicating a parent object).</span></span>

<span data-ttu-id="50b7d-114">Im folgenden Beispiel wird gezeigt, wie ein [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Objekt für ein bestimmtes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt und eine untergeordnete ID erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="50b7d-114">The following example shows how to get an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a particular [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span>


```C++
   
HRESULT GetIAccessibleExFromIAccessible(IAccessible * pAcc, long idChild, 
                                           IAccessibleEx ** ppaex)
{
    *ppaex = NULL;

    // First, get IServiceProvider from the IAccessible.
    IServiceProvider * pSp = NULL;
    HRESULT hr = pAcc->QueryInterface(IID_IServiceProvider, (void **) & pSp);
    if(FAILED(hr))
        return hr;
    if(pSp == NULL)
        return E_NOINTERFACE;

    // Next, get the IAccessibleEx for the parent object.
    IAccessibleEx * paex = NULL;
    hr = pSp->QueryService(__uuidof(IAccessibleEx), __uuidof(IAccessibleEx),
                                                                 (void **)&paex);
    pSp->Release();
    if(FAILED(hr))
        return hr;
    if(paex == NULL)
        return E_NOINTERFACE;

    // If this is for CHILDID_SELF, we're done. Otherwise, we have a child ID and 
    // can request the object for child.
    if(idChild == CHILDID_SELF)
    {
        *ppaex = paex;
        return S_OK;
    }
    else
    {
        // Get the IAccessibleEx for the specified child.
        IAccessibleEx * paexChild = NULL;
        hr = paex->GetObjectForChild(idChild, &paexChild);
        paex->Release();
        if(FAILED(hr))
            return hr;
        if(paexChild == NULL)
            return E_NOINTERFACE;
        *ppaex = paexChild;
        return S_OK;
    }
}
```



### <a name="obtaining-the-irawelementprovidersimple-interface"></a><span data-ttu-id="50b7d-115">Abrufen der "IRawElementProviderSimple"-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="50b7d-115">Obtaining the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="50b7d-116">Wenn ein Client über eine [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle verfügt, kann er QueryInterface verwenden, um zur [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle zu gelangen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="50b7d-116">If a client has an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, it can use QueryInterface to get to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, as the following example shows.</span></span>


```C++
HRESULT GetIRawElementProviderFromIAccessible(IAccessible * pAcc, long idChild,
                                                 IRawElementProviderSimple ** ppEl)
{
    * ppEl = NULL;

    // First, get the IAccessibleEx for the IAccessible and child ID pair.
    IAccessibleEx * paex;
    HRESULT hr = GetIAccessibleExFromIAccessible( pAcc, idChild, &paex );
    if(FAILED(hr))
        return hr;

    // Next, use QueryInterface.
    hr = paex->QueryInterface(__uuidof(IRawElementProviderSimple), (void **)ppEl);
    paex->Release();
    return hr;
}
```



### <a name="retrieving-control-patterns"></a><span data-ttu-id="50b7d-117">Abrufen von Steuerelement Mustern</span><span class="sxs-lookup"><span data-stu-id="50b7d-117">Retrieving Control Patterns</span></span>

<span data-ttu-id="50b7d-118">Wenn ein Client auf die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle zugreifen kann, kann er Steuerelement Muster-Schnittstellen abrufen, die von Anbietern implementiert wurden, und dann Methoden für diese Schnittstellen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50b7d-118">If a client has access to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, it can retrieve control pattern interfaces that have been implemented by providers, and can then call methods on those interfaces.</span></span> <span data-ttu-id="50b7d-119">Das folgende Beispiel zeigt die erforderliche Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="50b7d-119">The following example shows how to do this.</span></span>


```C++
// Helper function to get a pattern interface from an IAccessible and child ID 
// pair. Gets the IAccessibleEx, then calls GetPatternObject and QueryInterface.
HRESULT GetPatternFromIAccessible(IAccessible * pAcc, long idChild,
                                     PATTERNID patternId, REFIID iid, void ** ppv)
{
    // First, get the IAccesibleEx for this IAccessible and child ID pair.
    IRawElementProviderSimple * pel;
    HRESULT hr = GetIRawElementProviderSimpleFromIAccessible(pAcc, idChild, &pel);
    if(FAILED(hr))
        return hr;
    if(pel == NULL)
        return E_NOINTERFACE;

    // Now get the pattern object.
    IUnknown * pPatternObject = NULL;
    hr = pel->GetPatternProvider(patternId, &pPatternObject);
    pel->Release();
    if(FAILED(hr))
        return hr;
    if(pPatternObject == NULL)
        return E_NOINTERFACE;

    // Finally, use QueryInterface to get the correct interface type.
    hr = pPatternObject->QueryInterface(iid, ppv);
    pPatternObject->Release();
    if(*ppv == NULL)
        return E_NOINTERFACE;
    return hr;
}

HRESULT CallInvokePatternMethod(IAccessible * pAcc, long idChild)
{
    IInvokeProvider * pPattern;
    HRESULT hr = GetPatternFromIAccessible(pAcc, varChild,
                                  UIA_InvokePatternId, __uuidof(IInvokeProvider),
                                  (void **)&pPattern);
    if(FAILED(hr))
        return hr;

    hr = pPattern->Invoke();
    pPattern->Release();
    return hr;
}
```



### <a name="retrieving-property-values"></a><span data-ttu-id="50b7d-120">Abrufen von Eigenschafts Werten</span><span class="sxs-lookup"><span data-stu-id="50b7d-120">Retrieving Property Values</span></span>

<span data-ttu-id="50b7d-121">Wenn ein Client Zugriff auf [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)hat, kann er Eigenschaftswerte abrufen.</span><span class="sxs-lookup"><span data-stu-id="50b7d-121">If a client has access to [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), it can retrieve property values.</span></span> <span data-ttu-id="50b7d-122">Das folgende Beispiel zeigt, wie Sie Werte für die Eigenschaften AutomationId und LabeledBy Microsoft UI Automation erhalten.</span><span class="sxs-lookup"><span data-stu-id="50b7d-122">The following example shows how to get values for the AutomationId and LabeledBy Microsoft UI Automation properties.</span></span>


```C++
#include <initguid.h>
#include <uiautomationcoreapi.h> // Includes the UI Automation property GUID definitions.
#include <uiautomationcoreids.h> // Includes definitions of pattern/property IDs.

// Assume we already have a IRawElementProviderSimple * pEl.

VARIANT varValue;

// Get AutomationId property:
varValue.vt = VT_EMPTY;
HRESULT hr = pEl->GetPropertyValue(UIA_AutomationIdPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_BSTR)
    {
        // AutomationId is varValue.bstrVal.
    }
    VariantClear(&varValue);
}


// Get LabeledBy property:
varValue.vt = VT_EMPTY;
hr = pEl->GetPropertyValue(UIA_LabeledByPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_UNKNOWN || varValue.punkVal != NULL)
    {
        // Use QueryInterface to get IRawElementProviderSimple.
        IRawElementProviderSimple * pElLabel = NULL;
        hr = varValue.punkVal->QueryInterface(__uuidof(IRawElementProviderSimple),
                                              (void**)& pElLabel);
        if (SUCCEEDED(hr))
        {
            if(pElLabel != NULL)
            {
            // Use the pElLabel pointer here.
            pElLabel ->Release();
            }
        }
    }
    VariantClear(&varValue);
}
```



<span data-ttu-id="50b7d-123">Das vorherige Beispiel gilt für Eigenschaften, die keinem Steuerelement Muster zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="50b7d-123">The preceding example applies to properties that are not associated with a control pattern.</span></span> <span data-ttu-id="50b7d-124">Um auf die Eigenschaften von Steuerelement Mustern zuzugreifen, muss ein Client eine Steuerelement Muster-Schnittstelle abrufen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="50b7d-124">To access control pattern properties, a client must obtain and use a control pattern interface.</span></span>

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a><span data-ttu-id="50b7d-125">Abrufen einer IAccessible-Schnittstelle von einer IRawElementProviderSimple-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="50b7d-125">Retrieving an IAccessible Interface from an IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="50b7d-126">Wenn ein Client die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle für ein UI-Element erhält, kann der Client diese Schnittstelle verwenden, um eine entsprechende [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das Element zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="50b7d-126">If a client obtains the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface for a UI element, the client can use that interface to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="50b7d-127">Dies ist hilfreich, wenn der Client auf die Microsoft Active Accessibility-Eigenschaften für das-Element zugreifen muss.</span><span class="sxs-lookup"><span data-stu-id="50b7d-127">This is useful if the client needs to access the Microsoft Active Accessibility properties for the element.</span></span>

<span data-ttu-id="50b7d-128">Ein Client kann die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle als Eigenschafts Wert abrufen (z. b. durch Aufrufen von [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) mit UIA \_ labeledbypropertyid) oder als Element, das von einer Methode abgerufen wurde (z. b. durch Aufrufen von [**ISelectionProvider:: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) zum Abrufen eines Arrays von " **IRawElementProviderSimple** "-Schnittstellen ausgewählter Elemente).</span><span class="sxs-lookup"><span data-stu-id="50b7d-128">A client can obtain the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface as a property value (for example, by calling [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) with UIA\_LabeledByPropertyId), or as an item retrieved by a method (for example, by calling [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) to retrieve an array of **IRawElementProviderSimple** interfaces of selected elements).</span></span> <span data-ttu-id="50b7d-129">Nachdem die Schnittstelle " **IRawElementProviderSimple** " abgerufen wurde, kann Sie mithilfe der folgenden Schritte zum Abrufen eines entsprechenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="50b7d-129">After obtaining the **IRawElementProviderSimple** interface, a client can use it to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) by following these steps:</span></span>

-   <span data-ttu-id="50b7d-130">Versuchen Sie, QueryInterface zum Abrufen der [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="50b7d-130">Attempt to use QueryInterface to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>
-   <span data-ttu-id="50b7d-131">Wenn QueryInterface fehlschlägt, nennen Sie [**iaccessibleex::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) Configuration Manager für die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Instanz, aus der die Eigenschaft ursprünglich abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="50b7d-131">If QueryInterface fails, call [**IAccessibleEx::ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) on the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance from which the property was originally obtained.</span></span>
-   <span data-ttu-id="50b7d-132">Rufen Sie die [**getiaccessiblepair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) -Methode für die neue [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Instanz auf, um eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -interfae und eine untergeordnete ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="50b7d-132">Call the [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) method on the new [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfae and child ID.</span></span>

<span data-ttu-id="50b7d-133">Der folgende Code Ausschnitt veranschaulicht, wie Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle von einer zuvor abzurufenden [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="50b7d-133">The following code snippet demonstrates how to obtain the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface from a previously-obtained [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface.</span></span>


```C++
// IRawElementProviderSimple * pVal - an element returned by a property or method
// from another IRawElementProviderSimple.

IAccessible * pAcc = NULL;
long idChild;

// First, try to use QueryInterface to get the IAccessibleEx interface.
IAccessibleEx * pAccEx;
HRESULT hr = pVal->QueryInterface(__uuidof(IAccessibleEx), (void**)&pAccEx);
if (SUCCEEDED(hr)
{
    if (!pAccEx)
    {
        // If QueryInterface fails, and the IRawElementProviderSimple was 
              // obtained as a property or return value from another 
              // IRawElementProviderSimple, pass it to the 
              // IAccessibleEx::ConvertReturnedValue method of the
        // originating element.

        pAccExOrig->ConvertReturnedElement(pVal, &pAccEx);
    }

    if (pAccEx)
    {
        // Call GetIAccessiblePair to get an IAccessible interface and 
              // child ID.
        pAccEx->GetIAccessiblePair(&pAcc, &idChild);
    }

    // Finally, use the IAccessible interface and child ID.
    if (pAcc)
    {
        // Use IAccessible methods to get further information about this UI
              // element, or pass it to existing code that works in terms of 
              // IAccessible.
        ...
    }
}    
```



 

 
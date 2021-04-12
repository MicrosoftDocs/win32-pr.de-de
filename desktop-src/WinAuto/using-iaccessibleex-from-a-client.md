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
# <a name="using-iaccessibleex-from-a-client"></a>Verwenden von iaccessibleex von einem Client

In diesem Thema wird erläutert, wie Clients auf die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung eines Servers zugreifen und diese zum Abrufen von Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Mustern für Benutzeroberflächen Elemente verwenden.

Bei den Prozeduren und Beispielen in diesem Abschnitt wird davon ausgegangen, dass es sich um einen bereits in Bearbeitung [**baren Client handelt und um einen vorhandenen**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Microsoft Active Accessibility-Server. Außerdem wird davon ausgegangen, dass der Client bereits ein **IAccessible** -Objekt mit einer der frameworkframeworkfunktionen wie [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)abgerufen hat.

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a>Abrufen einer iaccessibleex-Schnittstelle von der IAccessible-Schnittstelle

Ein Client, der über eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für ein Barrierefreies Objekt verfügt, kann es mithilfe der folgenden Schritte zum Abrufen der entsprechenden [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle verwenden:

-   Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das ursprüngliche [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt mit der IID \_ \_ uuidof (IServiceProvider).
-   Aufrufen von **IServiceProvider:: QueryService** zum Abrufen von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).

### <a name="handling-the-child-id"></a>Behandeln der untergeordneten ID

Clients müssen auf Server mit einer anderen untergeordneten ID als childID Self vorbereitet werden \_ . Nachdem eine [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle von einer [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)-Schnittstelle erhalten hat, muss der Client [**iaccessibleex:: getobjectforchild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) aufrufen, wenn die untergeordnete ID nicht childID \_ Self ist (was ein übergeordnetes Objekt anzeigt).

Im folgenden Beispiel wird gezeigt, wie ein [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Objekt für ein bestimmtes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt und eine untergeordnete ID erhalten wird.


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



### <a name="obtaining-the-irawelementprovidersimple-interface"></a>Abrufen der "IRawElementProviderSimple"-Schnittstelle

Wenn ein Client über eine [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle verfügt, kann er QueryInterface verwenden, um zur [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle zu gelangen, wie im folgenden Beispiel gezeigt.


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



### <a name="retrieving-control-patterns"></a>Abrufen von Steuerelement Mustern

Wenn ein Client auf die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle zugreifen kann, kann er Steuerelement Muster-Schnittstellen abrufen, die von Anbietern implementiert wurden, und dann Methoden für diese Schnittstellen aufrufen. Das folgende Beispiel zeigt die erforderliche Vorgehensweise.


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



### <a name="retrieving-property-values"></a>Abrufen von Eigenschafts Werten

Wenn ein Client Zugriff auf [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)hat, kann er Eigenschaftswerte abrufen. Das folgende Beispiel zeigt, wie Sie Werte für die Eigenschaften AutomationId und LabeledBy Microsoft UI Automation erhalten.


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



Das vorherige Beispiel gilt für Eigenschaften, die keinem Steuerelement Muster zugeordnet sind. Um auf die Eigenschaften von Steuerelement Mustern zuzugreifen, muss ein Client eine Steuerelement Muster-Schnittstelle abrufen und verwenden.

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a>Abrufen einer IAccessible-Schnittstelle von einer IRawElementProviderSimple-Schnittstelle

Wenn ein Client die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle für ein UI-Element erhält, kann der Client diese Schnittstelle verwenden, um eine entsprechende [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle für das Element zu erhalten. Dies ist hilfreich, wenn der Client auf die Microsoft Active Accessibility-Eigenschaften für das-Element zugreifen muss.

Ein Client kann die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle als Eigenschafts Wert abrufen (z. b. durch Aufrufen von [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) mit UIA \_ labeledbypropertyid) oder als Element, das von einer Methode abgerufen wurde (z. b. durch Aufrufen von [**ISelectionProvider:: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) zum Abrufen eines Arrays von " **IRawElementProviderSimple** "-Schnittstellen ausgewählter Elemente). Nachdem die Schnittstelle " **IRawElementProviderSimple** " abgerufen wurde, kann Sie mithilfe der folgenden Schritte zum Abrufen eines entsprechenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) verwendet werden:

-   Versuchen Sie, QueryInterface zum Abrufen der [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle zu verwenden.
-   Wenn QueryInterface fehlschlägt, nennen Sie [**iaccessibleex::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) Configuration Manager für die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Instanz, aus der die Eigenschaft ursprünglich abgerufen wurde.
-   Rufen Sie die [**getiaccessiblepair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) -Methode für die neue [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Instanz auf, um eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -interfae und eine untergeordnete ID zu erhalten.

Der folgende Code Ausschnitt veranschaulicht, wie Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle von einer zuvor abzurufenden [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle abrufen.


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



 

 
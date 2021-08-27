---
title: Verwenden von IAccessibleEx über einen Client
description: In diesem Thema wird erläutert, wie Clients auf die IAccessibleEx-Implementierung eines Servers zugreifen und diese verwenden, Benutzeroberflächenautomatisierung Eigenschaften und Steuerelementmuster für Benutzeroberflächenelemente zu erhalten.
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f03bd58ec80a29f13e0428de4655aa7200144122b1a1889259844db078aa9dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098100"
---
# <a name="using-iaccessibleex-from-a-client"></a>Verwenden von IAccessibleEx über einen Client

In diesem Thema wird erläutert, wie Clients auf die [**IAccessibleEx-Implementierung**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) eines Servers zugreifen und diese zum Benutzeroberflächenautomatisierung eigenschaften und Steuerelementmuster für Benutzeroberflächenelemente verwenden.

Bei den Prozeduren und Beispielen in diesem Abschnitt wird davon ausgegangen, dass ein bereits ausgeführter [**IAccessible-Client**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und ein vorhandener Microsoft Active Accessibility sind. Außerdem wird davon ausgegangen, dass der Client bereits ein **IAccessible-Objekt** mithilfe einer der Frameworkfunktionen für die Barrierefreiheit wie [**AccessibleObjectFromEvent,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**AccessibleObjectFromWindow erhalten hat.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a>Abrufen einer IAccessibleEx-Schnittstelle von der IAccessible-Schnittstelle

Ein Client, der über eine [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für ein barrierefreies Objekt verfügt, kann es verwenden, um die entsprechende [**IAccessibleEx-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) mithilfe der folgenden Schritte zu erhalten:

-   Rufen [**Sie QueryInterface für**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) das ursprüngliche [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) mit einer IID von \_ \_ uuidof(IServiceProvider) auf.
-   Rufen **Sie IServiceProvider::QueryService auf,** um [**IAccessibleEx zu erhalten.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)

### <a name="handling-the-child-id"></a>Behandeln der untergeordneten ID

Clients müssen für Server mit einer anderen untergeordneten ID als CHILDID SELF vorbereitet \_ werden. Nach dem Abrufen einer [**IAccessibleEx-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) von einem [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)müssen Clients [**IAccessibleEx::GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) aufrufen, wenn die untergeordnete ID nicht CHILDID SELF ist (was ein übergeordnetes Objekt \_ angibt).

Das folgende Beispiel zeigt, wie [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) für ein bestimmtes [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und eine untergeordnete ID erhalten wird.


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



### <a name="obtaining-the-irawelementprovidersimple-interface"></a>Abrufen der IRawElementProviderSimple-Schnittstelle

Wenn ein Client über eine [**IAccessibleEx-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) verfügt, kann er QueryInterface verwenden, um zur [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) zu kommen, wie im folgenden Beispiel gezeigt.


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



### <a name="retrieving-control-patterns"></a>Abrufen von Steuerelementmustern

Wenn ein Client Zugriff auf die [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) hat, kann er Steuerelementmusterschnittstellen abrufen, die von Anbietern implementiert wurden, und dann Methoden für diese Schnittstellen aufrufen. Das folgende Beispiel zeigt die erforderliche Vorgehensweise.


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



### <a name="retrieving-property-values"></a>Abrufen von Eigenschaftswerten

Wenn ein Client Zugriff auf [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)hat, kann er Eigenschaftswerte abrufen. Das folgende Beispiel zeigt, wie Werte für die Eigenschaften AutomationId und LabeledBy Microsoft Benutzeroberflächenautomatisierung werden.


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



Das vorherige Beispiel gilt für Eigenschaften, die nicht einem Steuerelementmuster zugeordnet sind. Für den Zugriff auf Steuerelementmustereigenschaften muss ein Client eine Steuerelementmusterschnittstelle abrufen und verwenden.

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a>Abrufen einer IAccessible-Schnittstelle von einer IRawElementProviderSimple-Schnittstelle

Wenn ein Client die [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) für ein Benutzeroberflächenelement erhält, kann der Client diese Schnittstelle verwenden, um eine entsprechende [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für das Element zu erhalten. Dies ist nützlich, wenn der Client auf die eigenschaften Microsoft Active Accessibility für das Element zugreifen muss.

Ein Client kann die [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) als Eigenschaftswert abrufen (z. B. durch Aufrufen von [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) mit UIA LabeledByPropertyId) oder als Element, das von einer Methode abgerufen wird (z. B. durch Aufrufen von \_ [**ISelectionProvider::GetSelection,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) um ein Array von **IRawElementProviderSimple-Schnittstellen** ausgewählter Elemente abzurufen). Nach dem Abrufen der **IRawElementProviderSimple-Schnittstelle** kann ein Client sie verwenden, um eine entsprechende [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zu erhalten, indem sie die folgenden Schritte ausführen:

-   Versuchen Sie, QueryInterface zu verwenden, um die [**IAccessibleEx-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) zu erhalten.
-   Wenn QueryInterface fehlschlägt, rufen [**Sie IAccessibleEx::ConvertReturnedElement für**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) die [**IAccessibleEx-Instanz**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) auf, von der die Eigenschaft ursprünglich erhalten wurde.
-   Rufen Sie die [**GetIAccessiblePair-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) für die neue [**IAccessibleEx-Instanz**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) auf, um eine [**IAccessible-Interfae**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und eine untergeordnete ID zu erhalten.

Der folgende Codeausschnitt veranschaulicht, wie sie die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) von einer zuvor erhaltenen [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) abrufen.


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



 

 
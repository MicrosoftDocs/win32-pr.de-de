---
title: Verwenden der Benutzeroberflächen Automatisierung zum Zugreifen auf ein fensterloses ActiveX-Steuerelement
description: Beschreibt die Verwendung von Microsoft UI Automation \ 32; API, um sicherzustellen, dass das fensterlose Microsoft-ActiveX-Steuerelement für Hilfstechnologien (at)-Client Anwendungen zugänglich ist.
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Fensterlose ActiveX-Steuerelement, Barrierefreiheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ada1d26463b0654c1808f6e4fd43f571687d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728417"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a>Verwenden der Benutzeroberflächen Automatisierung zum Zugreifen auf ein fensterloses ActiveX-Steuerelement

Beschreibt die Verwendung der Microsoft UI Automation API, um sicherzustellen, dass das fensterlose Microsoft-ActiveX-Steuerelement für Hilfstechnologien (at)-Client Anwendungen zugänglich ist.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [ActiveX-Steuerelemente](/windows/desktop/com/activex-controls)
-   [Benutzeroberflächenautomatisierung](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmierung von Microsoft Win32 und Component Object Model (com)
-   Fensterlose ActiveX-Steuerelemente
-   Benutzeroberflächen-Automatisierungsanbieter

## <a name="instructions"></a>Anweisungen

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a>Schritt 1: Implementieren der Schnittstellen für Benutzeroberflächenautomatisierungs-Anbieter.

Damit die Anwendung zugänglich ist, müssen Sie die Schnittstellen für Benutzeroberflächenautomatisierungs-Anbieter für Ihr fensterloses ActiveX-Steuerelement implementieren, einschließlich [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)und [**irawelementprovideradviseevents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents). Sie sollten diese Schnittstellen genauso wie für ein Fenster basiertes Steuerelement implementieren, es sei denn, dies wird in den folgenden Schritten beschrieben. Weitere Informationen zum Implementieren von UIA-Anbieter Schnittstellen finden Sie [im Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-providerportal.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Schritt 2: Implementieren Sie die IServiceProvider-Schnittstelle.

Wenn ein Client Barrierefreiheits Informationen über das fensterlose Steuerelement benötigt, ruft der Steuerelement Container die **IServiceProvider:: QueryService** -Methode Ihres Steuer Elements auf, um den [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstellen Zeiger für das Steuerelement abzurufen.

Im folgenden Beispiel wird gezeigt, wie die **QueryService** -Methode implementiert wird.


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a>Schritt 3: Implementieren der IRawElementProviderFragment:: Navigate-Methode.

Wenn die [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) -Methode Ihres fensterlosen Steuer Elements aufgerufen wird, um zum übergeordneten Element oder zu einem gleich geordneten Element des Stamm Anbieters des fensterlosen Steuer Elements zu navigieren, sollte Ihre **Navigate** -Methode an die [**irawelementproviderwindowlesssite:: getereigentfragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) -Methode des Steuerelement Containers delegiert werden.

Im folgenden Beispiel wird die Implementierung der [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) -Methode veranschaulicht.


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a>Schritt 4: Implementieren Sie die Methode IRawElementProviderFragment:: GetRuntimeId.

Wenn das fensterlose Steuerelement einen Aufrufen der Methode [**IRawElementProviderFragment:: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) empfängt, muss das Steuerelement folgende Aktionen ausführen:

1.  Rufen Sie ein Lauf Zeit-ID-Präfix ab, indem Sie die [**irawelementproviderwindowlesssite:: getruntimeidprefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) -Methode der Steuerelement Website aufrufen.
2.  Erstellen Sie eine eindeutige Lauf Zeit-ID für das Steuerelement, indem Sie eine ganze Zahl an das Präfix der Laufzeit-ID Anhängen
3.  Gibt die Runtime-ID an den Aufrufer zurück.

Im folgenden Beispiel wird gezeigt, wie die [**GetRuntimeId-**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) Methode implementiert wird.


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MSAA zum Zugreifen auf ein fensterloses ActiveX-Steuerelement](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Barrierefreiheit für das fensterlose ActiveX-Steuerelement](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 
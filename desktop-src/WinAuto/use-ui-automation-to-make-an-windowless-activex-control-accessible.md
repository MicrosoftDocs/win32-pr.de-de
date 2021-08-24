---
title: So verwenden Sie Benutzeroberflächenautomatisierung, um ein fensterloses ActiveX-Steuerelement zugänglich zu machen
description: Beschreibt die Verwendung des Microsoft Benutzeroberflächenautomatisierung \ 32; API, um sicherzustellen, dass Ihre fensterlose Microsoft ActiveX-Steuerung für AT-Clientanwendungen (Assistive Technology) zugänglich ist.
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Fensterloses ActiveX-Steuerelement, Barrierefreiheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ef56d5f3a06bbfa21502c791163f2251506a10fda7da9d07ee04941ad39de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570360"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a>So verwenden Sie Benutzeroberflächenautomatisierung, um ein fensterloses ActiveX-Steuerelement zugänglich zu machen

Beschreibt die Verwendung der Microsoft Benutzeroberflächenautomatisierung-API, um sicherzustellen, dass Ihr fensterloses Microsoft ActiveX-Steuerelement für At-Clientanwendungen (Assistive Technology) zugänglich ist.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [ActiveX-Steuerelemente](/windows/desktop/com/activex-controls)
-   [Benutzeroberflächenautomatisierung](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Microsoft Win32- und Component Object Model-Programmierung (COM)
-   Fensterlose ActiveX-Steuerelemente
-   Benutzeroberflächenautomatisierung-Anbieter

## <a name="instructions"></a>Anweisungen

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a>Schritt 1: Implementieren Sie die Benutzeroberflächenautomatisierung-Anbieterschnittstellen.

Damit Ihre Anwendung zugänglich ist, müssen Sie die Benutzeroberflächenautomatisierung-Anbieterschnittstellen für Ihr fensterloses ActiveX-Steuerelement implementieren, einschließlich [**IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) [**IRawElementProviderFragment,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)und [**IRawElementProviderAdviseEvents.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) Sie sollten diese Schnittstellen genauso implementieren wie für ein fensterbasiertes Steuerelement, außer wie in den folgenden Schritten beschrieben. Weitere Informationen zum Implementieren von UIA-Anbieterschnittstellen finden Sie im [Benutzeroberflächenautomatisierung Anbieterprogrammiererhandbuch.](uiauto-providerportal.md)

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Schritt 2: Implementieren sie die IServiceProvider-Schnittstelle.

Wenn ein Client Barrierefreiheitsinformationen zu Ihrem fensterlosen Steuerelement benötigt, ruft der Steuerelementcontainer die **IServiceProvider::QueryService-Methode** Ihres Steuerelements auf, um den [**IRawElementProviderSimple-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) für das Steuerelement abzurufen.

Das folgende Beispiel zeigt, wie die **QueryService-Methode** implementiert wird.


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



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a>Schritt 3: Implementieren Sie die IRawElementProviderFragment::Navigate-Methode.

Wenn die [**IRawElementProviderFragment::Navigate-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) Ihres fensterlosen Steuerelements aufgerufen wird, um zum übergeordneten oder nebengeordneten Element des Stammanbieters des fensterlosen Steuerelements zu navigieren, sollte Ihre **Navigate-Methode** an die [**IRawElementProviderWindowlessSite::GetAdjacentFragment-Methode**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) des Steuerelementcontainers delegieren.

Das folgende Beispiel zeigt, wie die [**Navigate-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) implementiert wird.


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



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a>Schritt 4: Implementieren Sie die IRawElementProviderFragment::GetRuntimeId-Methode.

Wenn ihr fensterloses Steuerelement einen Aufruf der [**IRawElementProviderFragment::GetRuntimeId-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) empfängt, muss das Steuerelement folgende Schritte ausführen:

1.  Rufen Sie ein Laufzeit-ID-Präfix ab, indem Sie die [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix-Methode**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) der Steuerelementsite aufrufen.
2.  Erstellen Sie eine eindeutige Laufzeit-ID für das Steuerelement, indem Sie eine ganze Zahl an das Laufzeit-ID-Präfix anfügen.
3.  Gibt die Laufzeit-ID an den Aufrufer zurück.

Das folgende Beispiel zeigt, wie die [**GetRuntimeId-Methode**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) implementiert wird.


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

[Verwenden von MSAA, um ein fensterloses ActiveX-Steuerelement zugänglich zu machen](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Fensterlose ActiveX Steuern der Barrierefreiheit](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 
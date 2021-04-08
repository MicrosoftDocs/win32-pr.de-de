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
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="7cfb7-104">Verwenden der Benutzeroberflächen Automatisierung zum Zugreifen auf ein fensterloses ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7cfb7-104">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>

<span data-ttu-id="7cfb7-105">Beschreibt die Verwendung der Microsoft UI Automation API, um sicherzustellen, dass das fensterlose Microsoft-ActiveX-Steuerelement für Hilfstechnologien (at)-Client Anwendungen zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-105">Describes how to use the Microsoft UI Automation API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7cfb7-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="7cfb7-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7cfb7-107">Technologien</span><span class="sxs-lookup"><span data-stu-id="7cfb7-107">Technologies</span></span>

-   [<span data-ttu-id="7cfb7-108">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7cfb7-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="7cfb7-109">Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="7cfb7-109">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="7cfb7-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7cfb7-110">Prerequisites</span></span>

-   <span data-ttu-id="7cfb7-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="7cfb7-111">C/C++</span></span>
-   <span data-ttu-id="7cfb7-112">Programmierung von Microsoft Win32 und Component Object Model (com)</span><span class="sxs-lookup"><span data-stu-id="7cfb7-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="7cfb7-113">Fensterlose ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7cfb7-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="7cfb7-114">Benutzeroberflächen-Automatisierungsanbieter</span><span class="sxs-lookup"><span data-stu-id="7cfb7-114">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="7cfb7-115">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="7cfb7-115">Instructions</span></span>

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a><span data-ttu-id="7cfb7-116">Schritt 1: Implementieren der Schnittstellen für Benutzeroberflächenautomatisierungs-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-116">Step 1: Implement the UI Automation provider interfaces.</span></span>

<span data-ttu-id="7cfb7-117">Damit die Anwendung zugänglich ist, müssen Sie die Schnittstellen für Benutzeroberflächenautomatisierungs-Anbieter für Ihr fensterloses ActiveX-Steuerelement implementieren, einschließlich [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)und [**irawelementprovideradviseevents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span><span class="sxs-lookup"><span data-stu-id="7cfb7-117">To make your application accessible, you must implement the UI Automation provider interfaces for your windowless ActiveX control, including [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), and [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span></span> <span data-ttu-id="7cfb7-118">Sie sollten diese Schnittstellen genauso wie für ein Fenster basiertes Steuerelement implementieren, es sei denn, dies wird in den folgenden Schritten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-118">You should implement these interfaces just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="7cfb7-119">Weitere Informationen zum Implementieren von UIA-Anbieter Schnittstellen finden Sie [im Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="7cfb7-119">For more information about implementing UIA provider interfaces, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="7cfb7-120">Schritt 2: Implementieren Sie die IServiceProvider-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-120">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="7cfb7-121">Wenn ein Client Barrierefreiheits Informationen über das fensterlose Steuerelement benötigt, ruft der Steuerelement Container die **IServiceProvider:: QueryService** -Methode Ihres Steuer Elements auf, um den [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstellen Zeiger für das Steuerelement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-121">When a client needs accessibility information about your windowless control, the control container calls your control's **IServiceProvider::QueryService** method to retrieve the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface pointer for your control.</span></span>

<span data-ttu-id="7cfb7-122">Im folgenden Beispiel wird gezeigt, wie die **QueryService** -Methode implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-122">The following example shows how to implement the **QueryService** method.</span></span>


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



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a><span data-ttu-id="7cfb7-123">Schritt 3: Implementieren der IRawElementProviderFragment:: Navigate-Methode.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-123">Step 3: Implement the IRawElementProviderFragment::Navigate method.</span></span>

<span data-ttu-id="7cfb7-124">Wenn die [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) -Methode Ihres fensterlosen Steuer Elements aufgerufen wird, um zum übergeordneten Element oder zu einem gleich geordneten Element des Stamm Anbieters des fensterlosen Steuer Elements zu navigieren, sollte Ihre **Navigate** -Methode an die [**irawelementproviderwindowlesssite:: getereigentfragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) -Methode des Steuerelement Containers delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-124">When your windowless control’s [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method is called to navigate to the parent or a sibling of the windowless control's root provider, your **Navigate** method should delegate to the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method of the control container.</span></span>

<span data-ttu-id="7cfb7-125">Im folgenden Beispiel wird die Implementierung der [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) -Methode veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-125">The following example shows how to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span>


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



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a><span data-ttu-id="7cfb7-126">Schritt 4: Implementieren Sie die Methode IRawElementProviderFragment:: GetRuntimeId.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-126">Step 4: Implement the IRawElementProviderFragment::GetRuntimeId method.</span></span>

<span data-ttu-id="7cfb7-127">Wenn das fensterlose Steuerelement einen Aufrufen der Methode [**IRawElementProviderFragment:: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) empfängt, muss das Steuerelement folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="7cfb7-127">When your windowless control receives a call to its [**IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) method, the control must do the following:</span></span>

1.  <span data-ttu-id="7cfb7-128">Rufen Sie ein Lauf Zeit-ID-Präfix ab, indem Sie die [**irawelementproviderwindowlesssite:: getruntimeidprefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) -Methode der Steuerelement Website aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-128">Retrieve a runtime ID prefix by calling the control site's [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>
2.  <span data-ttu-id="7cfb7-129">Erstellen Sie eine eindeutige Lauf Zeit-ID für das Steuerelement, indem Sie eine ganze Zahl an das Präfix der Laufzeit-ID Anhängen</span><span class="sxs-lookup"><span data-stu-id="7cfb7-129">Create a unique runtime ID for the control by appending an integer to the runtime ID prefix.</span></span>
3.  <span data-ttu-id="7cfb7-130">Gibt die Runtime-ID an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-130">Return the runtime ID to the caller.</span></span>

<span data-ttu-id="7cfb7-131">Im folgenden Beispiel wird gezeigt, wie die [**GetRuntimeId-**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) Methode implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="7cfb7-131">The following example shows how to implement the [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7cfb7-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7cfb7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cfb7-133">Verwenden von MSAA zum Zugreifen auf ein fensterloses ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7cfb7-133">Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="7cfb7-134">Barrierefreiheit für das fensterlose ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7cfb7-134">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 
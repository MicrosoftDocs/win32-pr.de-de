---
title: Verwenden von MSAA zum Zugreifen auf ein fensterloses ActiveX-Steuerelement
description: Beschreibt die Verwendung des Microsoft Active Accessibility \ 32; API, um sicherzustellen, dass das fensterlose Microsoft-ActiveX-Steuerelement für Hilfstechnologien (at)-Client Anwendungen zugänglich ist.
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- ActiveX-Steuerelement, Barrierefreiheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337243"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="0b829-104">Verwenden von MSAA zum Zugreifen auf ein fensterloses ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="0b829-104">Use MSAA to make a windowless ActiveX control accessible</span></span>

<span data-ttu-id="0b829-105">Beschreibt, wie die Microsoft Active Accessibility-API verwendet wird, um sicherzustellen, dass das fensterlose Microsoft-ActiveX-Steuerelement für Hilfstechnologien (at)-Client Anwendungen zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="0b829-105">Describes how to use the Microsoft Active Accessibility API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0b829-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="0b829-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0b829-107">Technologien</span><span class="sxs-lookup"><span data-stu-id="0b829-107">Technologies</span></span>

-   [<span data-ttu-id="0b829-108">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="0b829-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="0b829-109">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="0b829-109">Microsoft Active Accessibility</span></span>](microsoft-active-accessibility.md)

### <a name="prerequisites"></a><span data-ttu-id="0b829-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0b829-110">Prerequisites</span></span>

-   <span data-ttu-id="0b829-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="0b829-111">C/C++</span></span>
-   <span data-ttu-id="0b829-112">Programmierung von Microsoft Win32 und Component Object Model (com)</span><span class="sxs-lookup"><span data-stu-id="0b829-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="0b829-113">Fensterlose ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="0b829-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="0b829-114">Microsoft Active Accessibility-Server</span><span class="sxs-lookup"><span data-stu-id="0b829-114">Microsoft Active Accessibility servers</span></span>

## <a name="instructions"></a><span data-ttu-id="0b829-115">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="0b829-115">Instructions</span></span>

### <a name="step-1-implement-the-iaccessible-interface"></a><span data-ttu-id="0b829-116">Schritt 1: Implementieren Sie die IAccessible-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0b829-116">Step 1: Implement the IAccessible interface.</span></span>

<span data-ttu-id="0b829-117">Um das fensterlose ActiveX-Steuerelement zugänglich zu machen, müssen Sie die Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren, genauso wie für ein Fenster basiertes Steuerelement, es sei denn, dies wird in den folgenden Schritten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0b829-117">To make your windowless ActiveX control accessible, you must implement the Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="0b829-118">Weitere Informationen zum Implementieren von **IAccessible** finden Sie [im Entwicklerhandbuch für Active Accessibility-Server](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="0b829-118">For more information about implementing **IAccessible**, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="0b829-119">Schritt 2: Implementieren Sie die IServiceProvider-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0b829-119">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="0b829-120">Wenn ein Client Barrierefreiheits Informationen über das fensterlose Steuerelement anfordert, ruft der Container die [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) -Methode Ihres Steuer Elements auf, um den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0b829-120">When a client requests accessibility information about your windowless control, the container calls your control's [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method to retrieve the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="0b829-121">Dieses Beispiel zeigt, wie die [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) -Methode implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="0b829-121">This example shows how to implement the [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a><span data-ttu-id="0b829-122">Schritt 3: Delegieren von IAccessible:: get \_ accParent-Methoden aufrufen an die iaccessiblewindowlesssite:: getsamentaccessible-Methode der Steuerelement Website.</span><span class="sxs-lookup"><span data-stu-id="0b829-122">Step 3: Delegate IAccessible::get\_accParent method calls to the control site's IAccessibleWindowlessSite::GetParentAccessible method.</span></span>

<span data-ttu-id="0b829-123">Wenn ein Client das übergeordnete Objekt des fensterlosen Steuer Elements anfordert, ruft der Container die [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) -Methode Ihres Steuer Elements auf.</span><span class="sxs-lookup"><span data-stu-id="0b829-123">When a client requests the parent object of your windowless control, the container calls your control's [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span> <span data-ttu-id="0b829-124">Die **get \_ accParent** -Implementierung sollte an die [**iaccessiblewindowlesssite:: getparameentaccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) -Methode des Containers delegieren.</span><span class="sxs-lookup"><span data-stu-id="0b829-124">Your **get\_accParent** implementation should delegate to the [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) method of the container.</span></span>

<span data-ttu-id="0b829-125">In diesem Beispiel wird gezeigt, wie die [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) -Methode implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="0b829-125">This example shows how to implement the [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span>


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a><span data-ttu-id="0b829-126">Schritt 4: beschaffen eines Bereichs von Objekt-IDs, die den Ereignis Quellen in Ihrem fensterlosen Steuerelement zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0b829-126">Step 4: Acquire a range of object IDs to assign to the event sources in your windowless control.</span></span>

<span data-ttu-id="0b829-127">Wie fensterbasierte Steuerelemente Ruft ein fensterloses ActiveX-Steuerelement die [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) -Funktion auf, um Clients über wichtige Ereignisse zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="0b829-127">Like window-based controls, a windowless ActiveX control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function to notify clients of important events.</span></span> <span data-ttu-id="0b829-128">Die Funktionsparameter enthalten die Objekt-ID des Elements, das das Ereignis aufhebt.</span><span class="sxs-lookup"><span data-stu-id="0b829-128">The function parameters include the object ID of the item that is raising the event.</span></span> <span data-ttu-id="0b829-129">Das fensterlose Steuerelement muss Objekt-IDs mithilfe eines Werts aus einem Bereich zuweisen, der durch Aufrufen der [**iaccessiblewindowlesssite:: acquireobjectidrange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) -Methode der Steuerelement Website abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0b829-129">Your windowless control must assign object IDs by using a value from a range acquired by calling the control site’s [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) method.</span></span>

<span data-ttu-id="0b829-130">Dieses Beispiel zeigt, wie Sie einen Bereich von Objekt-ID-Werten aus dem Steuerelement Container abrufen.</span><span class="sxs-lookup"><span data-stu-id="0b829-130">This example shows how to acquire a range of object ID values from the control container.</span></span>


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a><span data-ttu-id="0b829-131">Schritt 5: Implementieren Sie die IAccessibleHandler-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0b829-131">Step 5: Implement the IAccessibleHandler interface.</span></span>

<span data-ttu-id="0b829-132">Wenn ein fensterloses Steuerelement die [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) -Funktion aufruft, gibt das Steuerelement die Objekt-ID des Benutzeroberflächen Elements an, das das Ereignis aufhebt, und gibt den Steuerelement Container als das Fenster an, das auf die [**WM- \_ GetObject**](wm-getobject.md) -Nachrichten im Namen des Steuer Elements antwortet.</span><span class="sxs-lookup"><span data-stu-id="0b829-132">When a windowless control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function, the control specifies the object ID of the UI item that is raising the event, and specifies the control container as the window that will respond to [**WM\_GETOBJECT**](wm-getobject.md) messages on behalf of the control.</span></span>

<span data-ttu-id="0b829-133">Wenn eine Client Anwendung auf das-Ereignis reagiert, empfängt der Steuerelement Container eine [**WM \_ GetObject**](wm-getobject.md) -Nachricht, die die Objekt-ID des UI-Elements enthält, das das Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="0b829-133">If a client application responds to the event, the control container receives a [**WM\_GETOBJECT**](wm-getobject.md) message that includes the object ID of the UI item that raised the event.</span></span> <span data-ttu-id="0b829-134">Der Steuerelement Container antwortet, indem er das fensterlose Steuerelement sucht, das die Objekt-ID besitzt, und dann die [**iaccessibleobjectfromid**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) -Methode dieses Steuer Elements aufruft.</span><span class="sxs-lookup"><span data-stu-id="0b829-134">The control container responds by looking up the windowless control that "owns" the object ID, and then calling that control's [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) method.</span></span> <span data-ttu-id="0b829-135">Die **AccessibleObjectFromID** -Methode gibt den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger für das UI-Element zurück, und der Steuerelement Container leitet den Zeiger an die Client Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="0b829-135">The **AccessibleObjectFromID** method returns the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the UI item, and the control container forwards the pointer to the client application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b829-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b829-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b829-137">Verwenden der Benutzeroberflächen Automatisierung, um ein fensterloses ActiveX-Steuerelement zugänglich zu machen</span><span class="sxs-lookup"><span data-stu-id="0b829-137">Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="0b829-138">Barrierefreiheit für das fensterlose ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="0b829-138">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 
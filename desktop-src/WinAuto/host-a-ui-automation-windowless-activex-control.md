---
title: Hosten eines fensterlosen ActiveX-Steuer Elements für die Benutzeroberflächen Automatisierung
description: Erfahren Sie, wie Sie einen Steuerelement Container erstellen, der fensterlose Microsoft-ActiveX-Steuerelemente hosten kann, die Microsoft UI Automation implementieren.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- UI-Automatisierung, fensterloses ActiveX-Steuerelement
- Fensterlose ActiveX-Steuerelement, UI-Automatisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315290"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a><span data-ttu-id="23db7-105">Hosten eines fensterlosen ActiveX-Steuer Elements für die Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="23db7-105">Host a UI Automation Windowless ActiveX Control</span></span>

<span data-ttu-id="23db7-106">Erfahren Sie, wie Sie einen Steuerelement Container erstellen, der fensterlose Microsoft-ActiveX-Steuerelemente hosten kann, die Microsoft UI Automation implementieren.</span><span class="sxs-lookup"><span data-stu-id="23db7-106">Learn how to create a control container that can host windowless Microsoft ActiveX controls that implement Microsoft UI Automation.</span></span> <span data-ttu-id="23db7-107">Mithilfe der hier beschriebenen Schritte können Sie sicherstellen, dass Benutzeroberflächen Automatisierung fensterlose Steuerelemente, die in Ihrem Steuerelement Container gehostet werden, von Hilfstechnologien (bei) Client Anwendungen zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="23db7-107">By using the steps described here, you can ensure that any UI Automation windowless controls that are hosted in your control container are accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="23db7-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="23db7-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="23db7-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="23db7-109">Technologies</span></span>

-   [<span data-ttu-id="23db7-110">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23db7-110">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="23db7-111">Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="23db7-111">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="23db7-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="23db7-112">Prerequisites</span></span>

-   <span data-ttu-id="23db7-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="23db7-113">C/C++</span></span>
-   <span data-ttu-id="23db7-114">Programmierung von Microsoft Win32 und Component Object Model (com)</span><span class="sxs-lookup"><span data-stu-id="23db7-114">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="23db7-115">Fensterlose ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="23db7-115">Windowless ActiveX controls</span></span>
-   <span data-ttu-id="23db7-116">Benutzeroberflächen-Automatisierungsanbieter</span><span class="sxs-lookup"><span data-stu-id="23db7-116">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="23db7-117">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="23db7-117">Instructions</span></span>

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a><span data-ttu-id="23db7-118">Schritt 1: Geben Sie die IRawElementProviderSimple-Schnittstelle für das fensterlose Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="23db7-118">Step 1: Provide the IRawElementProviderSimple interface on behalf of the windowless control.</span></span>

<span data-ttu-id="23db7-119">Wenn das System den " [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) "-Zeiger für den Stamm eines fensterlosen Steuer Elements benötigt, fragt das System den Steuerelement Container ab.</span><span class="sxs-lookup"><span data-stu-id="23db7-119">Whenever the system needs the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer for the root of a windowless control, the system queries the control container.</span></span> <span data-ttu-id="23db7-120">Zum Abrufen des Zeigers ruft der Container die Implementierung der [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) -Methode des fensterlosen Steuer Elements auf.</span><span class="sxs-lookup"><span data-stu-id="23db7-120">To retrieve the pointer, the container calls the windowless control's implementation of the [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>

<span data-ttu-id="23db7-121">Wenn der Steuerelement Container über eine Benutzeroberflächenautomatisierungs-Implementierung verfügt, kann er den [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Zeiger des fensterlosen Steuer Elements auf das System zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="23db7-121">If the control container has a UI Automation implementation, it can return the windowless control's [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer to the system.</span></span>

<span data-ttu-id="23db7-122">Wenn der Steuerelement Container eine Microsoft Active Accessibility-Implementierung aufweist, rufen Sie die [**uiaiaccessiblefromprovider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) -Funktion auf, um einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger zu erhalten, der das Steuerelement darstellt, und geben Sie dann den **IAccessible** -Schnittstellen Zeiger auf das System zurück.</span><span class="sxs-lookup"><span data-stu-id="23db7-122">If the control container has a Microsoft Active Accessibility implementation, call the [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) function to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer that represents the control, and then return the **IAccessible** interface pointer to the system.</span></span>

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a><span data-ttu-id="23db7-123">Schritt 2: Implementieren Sie die "irawelementproviderwindowlesssite"-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="23db7-123">Step 2: Implement the IRawElementProviderWindowlessSite interface.</span></span>

<span data-ttu-id="23db7-124">Ein Steuerelement Container implementiert die [**irawelementproviderwindowlesssite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) -Schnittstelle und ermöglicht ein fensterloses Steuerelement, das auf der Benutzeroberflächen Automatisierung basiert, um seine Barrierefreiheits Informationen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="23db7-124">A control container implements the [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) interface enable a windowless control that is based on UI Automation to communicate its accessibility information.</span></span>

1.  <span data-ttu-id="23db7-125">Implementieren Sie [**irawelementproviderwindowlesssite:: getruntimeidprefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span><span class="sxs-lookup"><span data-stu-id="23db7-125">Implement [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span></span>

    <span data-ttu-id="23db7-126">Ein fensterloses Steuerelement Fragment muss eine eindeutige Lauf Zeit-ID für sich selbst erstellen.</span><span class="sxs-lookup"><span data-stu-id="23db7-126">A windowless control fragment must create a unique runtime ID for itself.</span></span> <span data-ttu-id="23db7-127">Um die Lauf Zeit-ID zu erstellen, Ruft ein fensterloses Steuerelement Fragment einen Präfix Wert durch Aufrufen der [**getruntimeidprefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) -Methode der Steuerungs Website ab und fügt dann an das Präfix einen ganzzahligen Wert an, der relativ zu allen anderen Fragmenten im fensterlosen Steuerelement eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="23db7-127">To create its runtime ID, a windowless control fragment retrieves a prefix value by calling the control site's [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method, and then appends to the prefix an integer value that is unique relative to all other fragments in the windowless control.</span></span>

    <span data-ttu-id="23db7-128">Die Steuerungs Site für ein fensterloses Steuerelement sollte die [**getruntimeidprefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) -Methode implementieren, indem ein **SAFEARRAY** gebildet wird, das die Konstante **uiaappendruntimeid** enthält, gefolgt von einem ganzzahligen Wert, der für die Website eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="23db7-128">The control site for a windowless control should implement the [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method by forming a **SAFEARRAY** that contains the constant **UiaAppendRuntimeId**, followed by an integer value that is unique to the site.</span></span>

    <span data-ttu-id="23db7-129">Dieses Beispiel zeigt, wie ein Lauf Zeit-ID-Präfix für ein fensterloses Steuerelement zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="23db7-129">This example shows how to return a runtime ID prefix for a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  <span data-ttu-id="23db7-130">Implementieren Sie die Methode [**irawelementproviderwindowlesssite:: getaccessentfragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .</span><span class="sxs-lookup"><span data-stu-id="23db7-130">Implement the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method.</span></span>

    <span data-ttu-id="23db7-131">Ein Steuerelement, das die Benutzeroberflächen Automatisierung implementiert, muss einen Zeiger auf den übergeordneten Fragmentanbieter des-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="23db7-131">A control that implements UI Automation must return a pointer to the control's parent fragment provider.</span></span>

    <span data-ttu-id="23db7-132">Um das übergeordnete Element des Fragments zurückzugeben, muss ein Objekt, das die [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) -Schnittstelle implementiert, in der Lage sein, die [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) -Methode zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="23db7-132">To return the parent of the fragment, an object that implements the [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) interface must be able to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span> <span data-ttu-id="23db7-133">Das Implementieren von **Navigate** ist für ein fensterloses Steuerelement schwierig, da das Steuerelement seine Position in der zugänglichen Struktur des übergeordneten Objekts möglicherweise nicht ermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="23db7-133">Implementing **Navigate** is difficult for a windowless control because the control might be unable to determine its location in the accessible tree of the parent object.</span></span> <span data-ttu-id="23db7-134">Die Methode [**irawelementproviderwindowlesssite:: getereigentfragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) ermöglicht dem fensterlosen Steuerelement, seine Website nach dem angrenzenden Fragment abzufragen und dieses Fragment dann an den Client zurückzugeben, der **Navigate** aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="23db7-134">The [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method enables the windowless control to query its site for the adjacent fragment, and then return that fragment to the client that called **Navigate**.</span></span>

    <span data-ttu-id="23db7-135">Dieses Beispiel zeigt, wie ein Steuerelement Container das übergeordnete Fragment eines fensterlosen Steuer Elements abruft.</span><span class="sxs-lookup"><span data-stu-id="23db7-135">This example shows how a control container retrieves the parent fragment of a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a><span data-ttu-id="23db7-136">Schritt 3: optional: Implementieren Sie die irawelementproviderhostingaccessibles-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="23db7-136">Step 3: Optional: Implement the IRawElementProviderHostingAccessibles interface.</span></span>

<span data-ttu-id="23db7-137">Implementieren Sie die-Schnittstelle [**irawelementproviderhostingaccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) , wenn Ihr Steuerelement Container über eine Benutzeroberflächenautomatisierungs-Anbieter Implementierung verfügt, die der Stamm einer Barrierefreiheits Struktur ist, die fensterlose ActiveX-Steuerelemente enthält, die Microsoft Active Accessibility unterstützen</span><span class="sxs-lookup"><span data-stu-id="23db7-137">Implement the [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) interface if your control container has a UI Automation provider implementation that is the root of an accessibility tree that includes windowless ActiveX controls that support Microsoft Active Accessibility.</span></span> <span data-ttu-id="23db7-138">Die " **irawelementproviderhostingaccessibles** "-Schnittstelle verfügt über eine einzelne Methode, " [**getembeddedaccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles)", die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger von allen Microsoft Active Accessibility basierten, fensterlosen ActiveX-Steuerelementen abruft, die von Ihrem Steuerelement Container gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="23db7-138">The **IRawElementProviderHostingAccessibles** interface has a single method, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), which retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers of all Microsoft Active Accessibility-based windowless ActiveX controls that are hosted by your control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23db7-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23db7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23db7-140">Hosten eines Windows-losen ActiveX-Steuer Elements mit MSAA</span><span class="sxs-lookup"><span data-stu-id="23db7-140">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[<span data-ttu-id="23db7-141">Barrierefreiheit für das fensterlose ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="23db7-141">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 
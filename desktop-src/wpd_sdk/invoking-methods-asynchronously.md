---
description: Asynchrones Aufrufen von Dienstmethoden
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Asynchrones Aufrufen von Dienstmethoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef4f0eb2e75b977b53300bed6eab4c909fa7796
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423850"
---
# <a name="invoking-service-methods-asynchronously"></a><span data-ttu-id="ed6a4-103">Asynchrones Aufrufen von Dienstmethoden</span><span class="sxs-lookup"><span data-stu-id="ed6a4-103">Invoking Service Methods Asynchronously</span></span>

<span data-ttu-id="ed6a4-104">Die WpdServiceApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die Dienstmethoden asynchron aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-104">The WpdServiceApiSample application includes code that demonstrates how an application can invoke the service methods asynchronously.</span></span> <span data-ttu-id="ed6a4-105">In diesem Beispiel werden die folgenden Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-105">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="ed6a4-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ed6a4-106">Interface</span></span>    | <span data-ttu-id="ed6a4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed6a4-107">Description</span></span>          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed6a4-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="ed6a4-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | <span data-ttu-id="ed6a4-109">Wird verwendet, um die **IPortableDeviceServiceMethods-Schnittstelle** abzurufen, um Methoden für einen bestimmten Dienst aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="ed6a4-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="ed6a4-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | <span data-ttu-id="ed6a4-111">Wird zum Aufrufen einer Dienstmethode verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="ed6a4-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="ed6a4-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                                  | <span data-ttu-id="ed6a4-113">Wird verwendet, um die ausgehenden Methodenparameter und die eingehenden Methodenergebnisse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="ed6a4-114">Dies kann **NULL** sein, wenn die Methode keine Parameter erfordert oder Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |
| [<span data-ttu-id="ed6a4-115">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="ed6a4-115">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | <span data-ttu-id="ed6a4-116">Wird von der Anwendung implementiert, um die Methodenergebnisse zu empfangen, wenn eine Methode abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-116">Implemented by the application to receive the method results when a method has completed.</span></span>                                                                               |



 

<span data-ttu-id="ed6a4-117">Wenn der Benutzer die Option "10" in der Befehlszeile auswählt, ruft die Anwendung die **InvokeMethodsAsync-Methode** auf, die sich im Modul ServiceMethods.cpp befindet.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-117">When the user chooses option "10" at the command line, the application invokes the **InvokeMethodsAsync** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="ed6a4-118">Beachten Sie, dass die Beispielanwendung vor dem Aufrufen der Methoden einen Contacts-Dienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-118">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="ed6a4-119">Dienstmethoden kapseln Funktionen, die jeder Dienst definiert und implementiert.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-119">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="ed6a4-120">Sie sind für jeden Diensttyp eindeutig und werden durch eine GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-120">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="ed6a4-121">Beispielsweise definiert der Contacts-Dienst eine **BeginSync-Methode,** die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Contact-Objekten vorzubereiten, und eine **EndSync-Methode,** um das Gerät über den Abschluss der Synchronisierung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-121">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="ed6a4-122">Anwendungen führen eine portable Gerätedienstmethode aus, indem [**sie IPortableDeviceServiceMethods::Invoke aufrufen.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)</span><span class="sxs-lookup"><span data-stu-id="ed6a4-122">Applications execute a portable device service method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="ed6a4-123">Dienstmethoden sollten nicht mit WPD-Befehlen verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-123">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="ed6a4-124">WPD-Befehle sind Teil der standardmäßigen WPD Device Driver Interface (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-124">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="ed6a4-125">Befehle sind vordefiniert, nach Kategorien (z. B. **WPD \_ CATEGORY \_ COMMON)** unterteilt und werden durch eine **PROPERTYKEY-Struktur** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-125">Commands are predefined, grouped by categories (for example, **WPD\_CATEGORY\_COMMON**), and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="ed6a4-126">Eine Anwendung sendet Befehle an den Gerätetreiber, indem [**sie IPortableDeviceService::SendCommand aufruft.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)</span><span class="sxs-lookup"><span data-stu-id="ed6a4-126">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="ed6a4-127">Weitere Informationen finden Sie im Thema Befehle.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-127">For more information, see the Commands topic.</span></span>

<span data-ttu-id="ed6a4-128">Die **InvokeMethodsAsync-Methode** ruft [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**IPortableDeviceServiceMethods-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-128">The **InvokeMethodsAsync** method invokes [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="ed6a4-129">Über diese Schnittstelle wird die **InvokeMethodAsync-Hilfsfunktion** zweimal aufgerufen. einmal für die **BeginSync-Methode** und einmal für die **EndSync-Methode.**</span><span class="sxs-lookup"><span data-stu-id="ed6a4-129">Using this interface, it invokes the **InvokeMethodAsync** helper function twice; once for the **BeginSync** method and once for the **EndSync** method.</span></span> <span data-ttu-id="ed6a4-130">In diesem Beispiel wartet **InvokeMethodAsync** unbegrenzt darauf, dass ein globales Ereignis signalisiert wird, wenn [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-130">In this example, , **InvokeMethodAsync** waits indefinitely for a global event to be signaled when [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) is called.</span></span>

<span data-ttu-id="ed6a4-131">Im folgenden Code wird die **InvokeMethodsAsync-Methode** verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-131">The following code uses the **InvokeMethodsAsync** method.</span></span>


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



<span data-ttu-id="ed6a4-132">Die **InvokeMethodAsync-Hilfsfunktion** führt für jede aufgerufene Methode Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="ed6a4-132">The **InvokeMethodAsync** helper function does the following for each method that it invokes:</span></span>

-   <span data-ttu-id="ed6a4-133">Erstellt ein globales Ereignishand handle, das überwacht wird, um den Methodenabschluss zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-133">Creates a global event handle that it monitors to determine method completion.</span></span>
-   <span data-ttu-id="ed6a4-134">Erstellt ein **CMethodCallback-Objekt,** das als Argument für [**IPortableDeviceServiceMethods:InvokeAsync bereitgestellt wird.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync)</span><span class="sxs-lookup"><span data-stu-id="ed6a4-134">Creates a **CMethodCallback** object that is supplied as an argument to [**IPortableDeviceServiceMethods:InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span></span>
-   <span data-ttu-id="ed6a4-135">Ruft die **IPortableDeviceServiceMethods::InvokeAsync-Methode** auf, um die gegebene Methode auf aufruft.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-135">Calls the **IPortableDeviceServiceMethods::InvokeAsync** method to invoke the given method.</span></span>
-   <span data-ttu-id="ed6a4-136">Überwacht das globale Ereignishand handle auf Abschluss.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-136">Monitors the global event handle for completion.</span></span>
-   <span data-ttu-id="ed6a4-137">Führt eine Bereinigung durch.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-137">Performs cleanup.</span></span>

<span data-ttu-id="ed6a4-138">Die **CMethodCallback-Klasse** veranschaulicht, wie eine Anwendung [**IPortableDeviceServiceMethodCallback implementieren kann.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)</span><span class="sxs-lookup"><span data-stu-id="ed6a4-138">The **CMethodCallback** class demonstrates how an application can implement [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span></span> <span data-ttu-id="ed6a4-139">Die Implementierung von **OnComplete** in dieser Klasse signalisiert ein Ereignis, um die Anwendung zu benachrichtigen, dass die Dienstmethode abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-139">The implementation of **OnComplete** in this class signals an event to notify the application that the service method has completed.</span></span> <span data-ttu-id="ed6a4-140">Zusätzlich zur **OnComplete-Methode** implementiert diese Klasse **AddRef,** **QueryInterface** und **Release,** die verwendet werden, um den Verweiszähler des Objekts und die schnittstellen zu verwalten, die es implementiert.</span><span class="sxs-lookup"><span data-stu-id="ed6a4-140">In addition to the **OnComplete** method, this class implements **AddRef**, **QueryInterface**, and **Release**, which are used to maintain the object's reference count and the interfaces that it implements.</span></span>


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a><span data-ttu-id="ed6a4-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed6a4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed6a4-142">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="ed6a4-142">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="ed6a4-143">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="ed6a4-143">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[<span data-ttu-id="ed6a4-144">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="ed6a4-144">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="ed6a4-145">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="ed6a4-145">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 

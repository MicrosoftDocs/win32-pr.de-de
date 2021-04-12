---
description: Asynchrones Aufrufen von Dienst Methoden
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Asynchrones Aufrufen von Dienst Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d312cc76cf8cb737136629c1e2c8135d1b7bd1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216956"
---
# <a name="invoking-service-methods-asynchronously"></a><span data-ttu-id="28049-103">Asynchrones Aufrufen von Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="28049-103">Invoking Service Methods Asynchronously</span></span>

<span data-ttu-id="28049-104">Die Anwendung wpdserviceapisample enthält Code, der veranschaulicht, wie eine Anwendung die Dienst Methoden asynchron aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="28049-104">The WpdServiceApiSample application includes code that demonstrates how an application can invoke the service methods asynchronously.</span></span> <span data-ttu-id="28049-105">In diesem Beispiel werden die folgenden Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="28049-105">This sample uses the following interfaces.</span></span>



|                                                                                         |                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28049-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="28049-106">Interface</span></span>                                                                               | <span data-ttu-id="28049-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28049-107">Description</span></span>                                                                                                                                                             |
| [<span data-ttu-id="28049-108">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="28049-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | <span data-ttu-id="28049-109">Wird zum Abrufen der **iportabledeviceservicemethods** -Schnittstelle verwendet, um Methoden für einen bestimmten Dienst aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="28049-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="28049-110">**Iportabledeviceservicemethods**</span><span class="sxs-lookup"><span data-stu-id="28049-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | <span data-ttu-id="28049-111">Wird verwendet, um eine Dienst Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="28049-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="28049-112">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="28049-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                                  | <span data-ttu-id="28049-113">Wird verwendet, um die Parameter für die ausgehende Methode und die Ergebnisse der eingehenden Methode aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="28049-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="28049-114">Dieser Wert kann **null** sein, wenn die Methode keine Parameter erfordert oder keine Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="28049-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |
| [<span data-ttu-id="28049-115">**Iportablede viceservicemethodcallback**</span><span class="sxs-lookup"><span data-stu-id="28049-115">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | <span data-ttu-id="28049-116">Wird von der Anwendung implementiert, um die Methoden Ergebnisse zu empfangen, wenn eine Methode abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="28049-116">Implemented by the application to receive the method results when a method has completed.</span></span>                                                                               |



 

<span data-ttu-id="28049-117">Wenn der Benutzer die Option "10" in der Befehlszeile auswählt, ruft die Anwendung die **invokemethodsasync** -Methode auf, die im Modul "servicemethods. cpp" zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="28049-117">When the user chooses option "10" at the command line, the application invokes the **InvokeMethodsAsync** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="28049-118">Beachten Sie, dass die Beispielanwendung vor dem Aufrufen der Methoden einen Contacts-Dienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="28049-118">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="28049-119">Dienst Methoden Kapseln Funktionen, die von den einzelnen Diensten definiert und implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="28049-119">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="28049-120">Sie sind für jeden Diensttyp eindeutig und werden durch eine GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="28049-120">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="28049-121">Der Kontakt Dienst definiert z. b. eine **BeginSync** -Methode, die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Kontakt Objekten vorzubereiten, und eine **EndSync** -Methode, um das Gerät zu benachrichtigen, dass die Synchronisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="28049-121">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="28049-122">Anwendungen führen eine Dienst Methode für tragbare Geräte durch Aufrufen von [**iportabledeviceservicemethods::**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)Call aus.</span><span class="sxs-lookup"><span data-stu-id="28049-122">Applications execute a portable device service method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="28049-123">Dienst Methoden sollten nicht mit WPD-Befehlen verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="28049-123">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="28049-124">WPD-Befehle sind Teil der standardmäßigen WPD-Gerätetreiber Schnittstelle (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar.</span><span class="sxs-lookup"><span data-stu-id="28049-124">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="28049-125">Befehle sind vordefiniert, nach Kategorien gruppiert (z. b. **WPD- \_ Kategorie \_ Common**) und werden durch eine **PropertyKey** -Struktur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="28049-125">Commands are predefined, grouped by categories (for example, **WPD\_CATEGORY\_COMMON**), and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="28049-126">Eine Anwendung sendet durch Aufrufen von [**iportabledeviceservice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)Befehle an den Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="28049-126">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="28049-127">Weitere Informationen finden Sie im Thema "Befehle".</span><span class="sxs-lookup"><span data-stu-id="28049-127">For more information, see the Commands topic.</span></span>

<span data-ttu-id="28049-128">Die **invokemethodsasync** -Methode ruft [**iportabledeviceservice:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**iportabledeviceservicemethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="28049-128">The **InvokeMethodsAsync** method invokes [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="28049-129">Mithilfe dieser Schnittstelle ruft Sie die **invokemethodasync** -Hilfsfunktion zweimal auf. einmal für die **BeginSync** -Methode und einmal für die **EndSync** -Methode.</span><span class="sxs-lookup"><span data-stu-id="28049-129">Using this interface, it invokes the **InvokeMethodAsync** helper function twice; once for the **BeginSync** method and once for the **EndSync** method.</span></span> <span data-ttu-id="28049-130">In diesem Beispiel wartet **invokemethodasync** unbegrenzt darauf, dass ein globales Ereignis signalisiert wird, wenn [**iportablede viceservicemethodcallback:: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="28049-130">In this example, , **InvokeMethodAsync** waits indefinitely for a global event to be signaled when [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) is called.</span></span>

<span data-ttu-id="28049-131">Im folgenden Code wird die **invokemethodsasync** -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="28049-131">The following code uses the **InvokeMethodsAsync** method.</span></span>


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



<span data-ttu-id="28049-132">Die Hilfsfunktion **invokemethodasync** führt für jede aufgerufenen Methode Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="28049-132">The **InvokeMethodAsync** helper function does the following for each method that it invokes:</span></span>

-   <span data-ttu-id="28049-133">Erstellt einen globalen Ereignis handle, den es überwacht, um den Abschluss der Methode zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="28049-133">Creates a global event handle that it monitors to determine method completion.</span></span>
-   <span data-ttu-id="28049-134">Erstellt ein **cmethodcallback** -Objekt, das als Argument für [**iportabledeviceservicemethods: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync)bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="28049-134">Creates a **CMethodCallback** object that is supplied as an argument to [**IPortableDeviceServiceMethods:InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span></span>
-   <span data-ttu-id="28049-135">Ruft die **iportabledeviceservicemethods:: InvokeAsync** -Methode auf, um die angegebene Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="28049-135">Calls the **IPortableDeviceServiceMethods::InvokeAsync** method to invoke the given method.</span></span>
-   <span data-ttu-id="28049-136">Überwacht den globalen Ereignis Handle auf den Abschluss.</span><span class="sxs-lookup"><span data-stu-id="28049-136">Monitors the global event handle for completion.</span></span>
-   <span data-ttu-id="28049-137">Führt eine Bereinigung durch.</span><span class="sxs-lookup"><span data-stu-id="28049-137">Performs cleanup.</span></span>

<span data-ttu-id="28049-138">Die **cmethodcallback** -Klasse veranschaulicht, wie eine Anwendung [**iportabledeviceservicemethodcallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="28049-138">The **CMethodCallback** class demonstrates how an application can implement [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span></span> <span data-ttu-id="28049-139">Die Implementierung von **OnComplete** in dieser Klasse signalisiert einem Ereignis, dass die Anwendung benachrichtigt wird, dass die Dienst Methode abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="28049-139">The implementation of **OnComplete** in this class signals an event to notify the application that the service method has completed.</span></span> <span data-ttu-id="28049-140">Zusätzlich zur **OnComplete** -Methode implementiert diese Klasse " **adressf**", " **QueryInterface**" und " **Release**", die zum Verwalten des Verweis Zählers des Objekts und der von ihm implementierten Schnittstellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28049-140">In addition to the **OnComplete** method, this class implements **AddRef**, **QueryInterface**, and **Release**, which are used to maintain the object's reference count and the interfaces that it implements.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="28049-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28049-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28049-142">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="28049-142">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="28049-143">**Iportablede viceservicemethodcallback**</span><span class="sxs-lookup"><span data-stu-id="28049-143">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[<span data-ttu-id="28049-144">**Iportabledeviceservicemethods**</span><span class="sxs-lookup"><span data-stu-id="28049-144">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="28049-145">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="28049-145">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 

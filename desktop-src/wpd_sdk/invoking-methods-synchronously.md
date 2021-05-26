---
description: Aufrufen von Dienstmethoden
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Aufrufen von Dienstmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b9540cf7378e13d56af2611d6216897c6750f6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424200"
---
# <a name="invoking-service-methods"></a><span data-ttu-id="4217e-103">Aufrufen von Dienstmethoden</span><span class="sxs-lookup"><span data-stu-id="4217e-103">Invoking Service Methods</span></span>

<span data-ttu-id="4217e-104">Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Contacts-Dienst unterstützten Methoden synchron aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="4217e-104">The WpdServicesApiSample application includes code that demonstrates how an application can invoke the methods supported by a given Contacts service synchronously..</span></span> <span data-ttu-id="4217e-105">In diesem Beispiel werden die folgenden Schnittstellen verwendet:</span><span class="sxs-lookup"><span data-stu-id="4217e-105">This sample uses the following interfaces</span></span>



| <span data-ttu-id="4217e-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4217e-106">Interface</span></span>    | <span data-ttu-id="4217e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4217e-107">Description</span></span>    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4217e-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="4217e-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="4217e-109">Wird verwendet, um die **IPortableDeviceServiceMethods-Schnittstelle** abzurufen, um Methoden für einen bestimmten Dienst aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4217e-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="4217e-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="4217e-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | <span data-ttu-id="4217e-111">Wird zum Aufrufen einer Dienstmethode verwendet.</span><span class="sxs-lookup"><span data-stu-id="4217e-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="4217e-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="4217e-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="4217e-113">Wird verwendet, um die ausgehenden Methodenparameter und die eingehenden Methodenergebnisse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4217e-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="4217e-114">Dies kann **NULL** sein, wenn die Methode keine Parameter erfordert oder Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4217e-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |



 

<span data-ttu-id="4217e-115">Wenn der Benutzer die Option "9" in der Befehlszeile auswählt, ruft die Anwendung die **InvokeMethods-Methode** auf, die sich im ServiceMethods.cpp-Modul befindet.</span><span class="sxs-lookup"><span data-stu-id="4217e-115">When the user chooses option "9" at the command line, the application invokes the **InvokeMethods** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="4217e-116">Beachten Sie, dass die Beispielanwendung vor dem Aufrufen der Methoden einen Contacts-Dienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="4217e-116">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="4217e-117">Dienstmethoden kapseln Funktionen, die jeder Dienst definiert und implementiert.</span><span class="sxs-lookup"><span data-stu-id="4217e-117">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="4217e-118">Sie sind für jeden Diensttyp eindeutig und werden durch eine GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4217e-118">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="4217e-119">Beispielsweise definiert der Contacts-Dienst eine **BeginSync-Methode,** die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Contact-Objekten vorzubereiten, und eine **EndSync-Methode,** um das Gerät über den Abschluss der Synchronisierung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="4217e-119">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="4217e-120">Anwendungen führen eine Methode aus, indem [**sie IPortableDeviceServiceMethods::Invoke aufrufen.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)</span><span class="sxs-lookup"><span data-stu-id="4217e-120">Applications execute a method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="4217e-121">Dienstmethoden dürfen nicht mit WPD-Befehlen verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="4217e-121">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="4217e-122">WPD-Befehle sind Teil der standardmäßigen WPD-Gerätetreiberschnittstelle (DDI) und der Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber.</span><span class="sxs-lookup"><span data-stu-id="4217e-122">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="4217e-123">Befehle sind vordefiniert, nach Kategorien gruppiert, z. B. **WPD \_ CATEGORY \_ COMMON**, und werden durch eine **PROPERTYKEY-Struktur** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4217e-123">Commands are predefined, grouped by categories, for example, **WPD\_CATEGORY\_COMMON**, and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="4217e-124">Eine Anwendung sendet Befehle an den Gerätetreiber, indem [**sie IPortableDeviceService::SendCommand aufruft.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)</span><span class="sxs-lookup"><span data-stu-id="4217e-124">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="4217e-125">Weitere Informationen finden Sie im Thema Befehle.</span><span class="sxs-lookup"><span data-stu-id="4217e-125">For more information, see the Commands topic.</span></span>

<span data-ttu-id="4217e-126">Die **InvokeMethods-Methode** ruft die [**IPortableDeviceService::Methods-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**IPortableDeviceServiceMethods-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4217e-126">The **InvokeMethods** method invokes the [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="4217e-127">Über diese Schnittstelle werden die **Methoden BeginSync** und **EndSync** aufgerufen, indem die [**IPortableDeviceServiceMethods::Invoke-Methode aufgerufen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) wird.</span><span class="sxs-lookup"><span data-stu-id="4217e-127">Using this interface, it invokes the **BeginSync** and **EndSync** methods by calling the [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="4217e-128">Bei jedem Aufruf **von Invoke** stellt die Anwendung die REFGUID für die aufgerufene Methode zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4217e-128">Each time it calls **Invoke**, the application supplies the REFGUID for the method that is invoked.</span></span>

<span data-ttu-id="4217e-129">Im folgenden Code wird die **InvokeMethods-Methode** verwendet.</span><span class="sxs-lookup"><span data-stu-id="4217e-129">The following code uses the **InvokeMethods** method.</span></span>


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
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

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="4217e-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4217e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4217e-131">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="4217e-131">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="4217e-132">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="4217e-132">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="4217e-133">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="4217e-133">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




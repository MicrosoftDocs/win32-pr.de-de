---
description: Aufrufen von Dienstmethoden
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Aufrufen von Dienstmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b568ea169d0f3c6465d9879eb9eb01c0b46b526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359418"
---
# <a name="invoking-service-methods"></a><span data-ttu-id="e3a4b-103">Aufrufen von Dienstmethoden</span><span class="sxs-lookup"><span data-stu-id="e3a4b-103">Invoking Service Methods</span></span>

<span data-ttu-id="e3a4b-104">Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung die Methoden aufrufen kann, die von einem bestimmten Kontakt Dienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-104">The WpdServicesApiSample application includes code that demonstrates how an application can invoke the methods supported by a given Contacts service synchronously..</span></span> <span data-ttu-id="e3a4b-105">In diesem Beispiel werden die folgenden Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-105">This sample uses the following interfaces</span></span>



|                                                                        |                                                                                                                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a4b-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e3a4b-106">Interface</span></span>                                                              | <span data-ttu-id="e3a4b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3a4b-107">Description</span></span>                                                                                                                                                             |
| [<span data-ttu-id="e3a4b-108">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="e3a4b-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="e3a4b-109">Wird zum Abrufen der **iportabledeviceservicemethods** -Schnittstelle verwendet, um Methoden für einen bestimmten Dienst aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="e3a4b-110">**Iportabledeviceservicemethods**</span><span class="sxs-lookup"><span data-stu-id="e3a4b-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | <span data-ttu-id="e3a4b-111">Wird verwendet, um eine Dienst Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="e3a4b-112">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="e3a4b-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="e3a4b-113">Wird verwendet, um die Parameter für die ausgehende Methode und die Ergebnisse der eingehenden Methode aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="e3a4b-114">Dieser Wert kann **null** sein, wenn die Methode keine Parameter erfordert oder keine Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |



 

<span data-ttu-id="e3a4b-115">Wenn der Benutzer die Option "9" in der Befehlszeile auswählt, ruft die Anwendung die **invokemethods** -Methode auf, die im Modul "servicemethods. cpp" zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-115">When the user chooses option "9" at the command line, the application invokes the **InvokeMethods** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="e3a4b-116">Beachten Sie, dass die Beispielanwendung vor dem Aufrufen der Methoden einen Contacts-Dienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-116">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="e3a4b-117">Dienst Methoden Kapseln Funktionen, die von den einzelnen Diensten definiert und implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-117">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="e3a4b-118">Sie sind für jeden Diensttyp eindeutig und werden durch eine GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-118">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="e3a4b-119">Der Kontakt Dienst definiert z. b. eine **BeginSync** -Methode, die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Kontakt Objekten vorzubereiten, und eine **EndSync** -Methode, um das Gerät zu benachrichtigen, dass die Synchronisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-119">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="e3a4b-120">Anwendungen führen eine Methode aus, indem Sie [**iportabledeviceservicemethods::**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke)Call aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-120">Applications execute a method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="e3a4b-121">Dienst Methoden sollten nicht mit WPD-Befehlen verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-121">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="e3a4b-122">WPD-Befehle sind Teil der standardmäßigen WPD-Gerätetreiber Schnittstelle (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-122">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="e3a4b-123">Befehle sind vordefiniert, gruppiert nach Kategorien, z. b. die **WPD- \_ Kategorie \_ Common**, und werden durch eine **PropertyKey** -Struktur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-123">Commands are predefined, grouped by categories, for example, **WPD\_CATEGORY\_COMMON**, and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="e3a4b-124">Eine Anwendung sendet durch Aufrufen von [**iportabledeviceservice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)Befehle an den Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-124">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="e3a4b-125">Weitere Informationen finden Sie im Thema "Befehle".</span><span class="sxs-lookup"><span data-stu-id="e3a4b-125">For more information, see the Commands topic.</span></span>

<span data-ttu-id="e3a4b-126">Die **invokemethods** -Methode ruft die [**iportabledeviceservice:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) -Methode auf, um eine [**iportabledeviceservicemethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-126">The **InvokeMethods** method invokes the [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="e3a4b-127">Mithilfe dieser Schnittstelle ruft Sie die **BeginSync** -Methode und die **EndSync** -Methode auf, indem Sie die [**iportabledeviceservicemethods::**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) Call-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-127">Using this interface, it invokes the **BeginSync** and **EndSync** methods by calling the [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="e3a4b-128">Jedes **Mal, wenn der Aufruf aufgerufen** wird, gibt die Anwendung die refguid für die aufgerufene Methode an.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-128">Each time it calls **Invoke**, the application supplies the REFGUID for the method that is invoked.</span></span>

<span data-ttu-id="e3a4b-129">Im folgenden Code wird die **invokemethods** -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3a4b-129">The following code uses the **InvokeMethods** method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e3a4b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3a4b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3a4b-131">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="e3a4b-131">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="e3a4b-132">**Iportabledeviceservicemethods**</span><span class="sxs-lookup"><span data-stu-id="e3a4b-132">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="e3a4b-133">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="e3a4b-133">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




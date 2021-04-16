---
description: Abrufen der von einem Gerät unterstützten Ereignisse
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Abrufen der von einem Gerät unterstützten Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530251"
---
# <a name="retrieving-the-events-supported-by-a-device"></a><span data-ttu-id="dfe8a-103">Abrufen der von einem Gerät unterstützten Ereignisse</span><span class="sxs-lookup"><span data-stu-id="dfe8a-103">Retrieving the Events Supported by a Device</span></span>

<span data-ttu-id="dfe8a-104">Einige WPD-Treiber unterstützen die Ereignis Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-104">Some WPD drivers support event notification.</span></span> <span data-ttu-id="dfe8a-105">Dies bedeutet, dass eine Anwendung beim Treiber registriert werden kann, um eine Benachrichtigung zu erhalten, wenn eine bestimmte Aktion erfolgt.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-105">This means that an application can register with the driver to receive a notification when a specific action occurs.</span></span> <span data-ttu-id="dfe8a-106">Beispielsweise kann eine Anwendung registrieren, um eine Benachrichtigung zu erhalten, wenn ein Objekt hinzugefügt oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-106">For example, an application can register to receive a notification when an object is added or removed.</span></span>

<span data-ttu-id="dfe8a-107">Es gibt zehn vordefinierte Ereignisse, die eine Anwendung überwachen kann.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-107">There are ten predefined events that an application can monitor.</span></span> <span data-ttu-id="dfe8a-108">Diese werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-108">They are described in the following table.</span></span>



| <span data-ttu-id="dfe8a-109">Ereignis</span><span class="sxs-lookup"><span data-stu-id="dfe8a-109">Event</span></span>                       | <span data-ttu-id="dfe8a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfe8a-110">Description</span></span>                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe8a-111">Gerätefunktionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="dfe8a-111">Device capabilities updated</span></span> | <span data-ttu-id="dfe8a-112">Tritt auf, wenn sich die Gerätefunktionen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-112">Occurs when the device capabilities have changed.</span></span>                                                                                      |
| <span data-ttu-id="dfe8a-113">Gerät entfernt</span><span class="sxs-lookup"><span data-stu-id="dfe8a-113">Device removed</span></span>              | <span data-ttu-id="dfe8a-114">Tritt auf, wenn das Gerät getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-114">Occurs when the device is unplugged.</span></span>                                                                                                   |
| <span data-ttu-id="dfe8a-115">Gerät zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="dfe8a-115">Device reset</span></span>                | <span data-ttu-id="dfe8a-116">Tritt auf, wenn das Gerät zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-116">Occurs when the device has been reset.</span></span>                                                                                                 |
| <span data-ttu-id="dfe8a-117">Objekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="dfe8a-117">Object added</span></span>                | <span data-ttu-id="dfe8a-118">Tritt auf, nachdem ein neues-Objekt auf dem Gerät verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-118">Occurs after a new object becomes available on the device.</span></span>                                                                             |
| <span data-ttu-id="dfe8a-119">Objekt entfernt</span><span class="sxs-lookup"><span data-stu-id="dfe8a-119">Object removed</span></span>              | <span data-ttu-id="dfe8a-120">Tritt auf, nachdem ein Objekt vom Gerät entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-120">Occurs after an object has been removed from the device.</span></span>                                                                               |
| <span data-ttu-id="dfe8a-121">Objekt Übertragung angefordert</span><span class="sxs-lookup"><span data-stu-id="dfe8a-121">Object transfer requested</span></span>   | <span data-ttu-id="dfe8a-122">Gibt an, dass für die Übertragung eines Objekts eine Anforderung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-122">Indicates that a request has been made to transfer an object.</span></span>                                                                          |
| <span data-ttu-id="dfe8a-123">Objekt aktualisiert</span><span class="sxs-lookup"><span data-stu-id="dfe8a-123">Object updated</span></span>              | <span data-ttu-id="dfe8a-124">Tritt auf, nachdem entweder ein-Objekt oder seine untergeordneten Elemente aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-124">Occurs after either an object or its children has been updated.</span></span> <span data-ttu-id="dfe8a-125">(Verbundene Clients sollten dann Ihre Ansicht des angegebenen Objekts aktualisieren.)</span><span class="sxs-lookup"><span data-stu-id="dfe8a-125">(Connected clients should then update their view of the given object.)</span></span> |
| <span data-ttu-id="dfe8a-126">Speicherformat wird ausgeführt</span><span class="sxs-lookup"><span data-stu-id="dfe8a-126">Storage format in progress</span></span>  | <span data-ttu-id="dfe8a-127">Tritt auf, wenn der Gerätespeicher formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-127">Occurs when the device storage is being formatted.</span></span>                                                                                     |



 

<span data-ttu-id="dfe8a-128">Eine Liste der Konstanten, die diesen Ereignissen zugeordnet sind, finden Sie im Thema [Ereignis Konstanten](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe8a-128">For a list of the constants associated with these events, see the [Event Constants](event-constants.md) topic.</span></span>

<span data-ttu-id="dfe8a-129">Die "listsupportedevents"-Funktion im Modul "devicecapabili. cpp" veranschaulicht das Abrufen von Ereignissen, die von einem bestimmten Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-129">The ListSupportedEvents function in the DeviceCapabilities.cpp module demonstrates the retrieval of events supported by a given device.</span></span>

<span data-ttu-id="dfe8a-130">Die Anwendung kann die Bezeichner für Ereignisse abrufen, die von einem Gerät unterstützt werden, und zwar mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-130">Your application can retrieve the identifiers for events supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="dfe8a-131">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dfe8a-131">Interface</span></span>                                                                                      | <span data-ttu-id="dfe8a-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfe8a-132">Description</span></span>                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="dfe8a-133">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dfe8a-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="dfe8a-134">Bietet Zugriff auf die unterstützten Ereignis Abruf Methoden.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-134">Provides access to the supported-event retrieval methods.</span></span> |
| [<span data-ttu-id="dfe8a-135">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dfe8a-135">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="dfe8a-136">Wird zum Auflisten und Speichern von funktionalen Kategorieinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-136">Used to enumerate and store functional-category data.</span></span>     |



 

<span data-ttu-id="dfe8a-137">Die erste Aufgabe, die von der Beispielanwendung durchgeführt wird, ist das Abrufen eines [**iportabledevicecapabili-**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) Objekts, das verwendet wird, um die vom jeweiligen Gerät unterstützten Ereignisse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-137">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the events supported by the given device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="dfe8a-138">Die unterstützten Ereignisse werden durch Aufrufen der [**iportabledevicecapabili:: getsupportedevents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-138">The supported events are retrieved by calling the [**IPortableDeviceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="dfe8a-139">Diese Methode ruft eine Auflistung der Ereignis Bezeichner für das angegebene Gerät ab und speichert Sie in einem [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt, auf das durch das Peer Vents-Argument verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-139">This method retrieves a collection of event identifiers for the given device and stores them in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object pointed to by the pEvents argument.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="dfe8a-140">Der nächste Schritt besteht darin, die Anzahl der unterstützten Ereignisse abzurufen, sodass die Anwendung das [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt durchlaufen und den Bezeichner für jede abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="dfe8a-140">The next step is to retrieve the count of supported events so that the application can iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object and retrieve the identifier for each.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="dfe8a-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dfe8a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfe8a-142">**Ereignis Konstanten**</span><span class="sxs-lookup"><span data-stu-id="dfe8a-142">**Event Constants**</span></span>](event-constants.md)
</dt> <dt>

[<span data-ttu-id="dfe8a-143">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dfe8a-143">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="dfe8a-144">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dfe8a-144">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="dfe8a-145">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dfe8a-145">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="dfe8a-146">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="dfe8a-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




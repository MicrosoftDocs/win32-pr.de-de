---
description: Abrufen unterstützter Dienst Ereignisse
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Abrufen unterstützter Dienst Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515b65b8ed062c346777224a64539f5229a704a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352671"
---
# <a name="retrieving-supported-service-events"></a><span data-ttu-id="d972e-103">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="d972e-103">Retrieving Supported Service Events</span></span>

<span data-ttu-id="d972e-104">Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung die Ereignisse abrufen kann, die von einem bestimmten Kontakt Dienst unterstützt werden, indem Methoden für die folgenden Schnittstellen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d972e-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the events supported by a given Contacts service by calling methods on the following interfaces.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d972e-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d972e-105">Interface</span></span>                                                                            | <span data-ttu-id="d972e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d972e-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="d972e-107">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="d972e-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="d972e-108">Wird zum Abrufen der **iportabledeviceservicecapabili-** Schnittstelle verwendet, um auf die unterstützten Ereignisse zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d972e-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="d972e-109">**Iportablede viceservicecapabili**</span><span class="sxs-lookup"><span data-stu-id="d972e-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="d972e-110">Bietet Zugriff auf die unterstützten Ereignisse und Ereignis Attribute.</span><span class="sxs-lookup"><span data-stu-id="d972e-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="d972e-111">**Iportabledevicepropvariantcollection**</span><span class="sxs-lookup"><span data-stu-id="d972e-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="d972e-112">Enthält die Liste der unterstützten Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="d972e-112">Contains the list of supported events.</span></span>                                                                |
| [<span data-ttu-id="d972e-113">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="d972e-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="d972e-114">Enthält die Attribute für ein bestimmtes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d972e-114">Contains the attributes for a given event.</span></span>                                                            |



 

<span data-ttu-id="d972e-115">Wenn der Benutzer die Option "4" in der Befehlszeile auswählt, ruft die Anwendung die **listsupportedevents** -Methode auf, die im Modul "servicecapabili. cpp" zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="d972e-115">When the user chooses option "4" at the command line, the application invokes the **ListSupportedEvents** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="d972e-116">Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontakt Dienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="d972e-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="d972e-117">In WPD wird ein Ereignis anhand des Namens, der Optionen und der Parameter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d972e-117">In WPD, an event is described by its name, options, and parameters.</span></span> <span data-ttu-id="d972e-118">Der Ereignis Name ist eine Skript freundliche Zeichenfolge, z. b. "mycustomevent".</span><span class="sxs-lookup"><span data-stu-id="d972e-118">The event name is a script-friendly string, for example, "MyCustomEvent".</span></span> <span data-ttu-id="d972e-119">Die Ereignis Optionen geben an, ob ein bestimmtes Ereignis an alle Clients gesendet wird und ob dieses Ereignis die automatische Wiedergabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d972e-119">The event options indicate whether a given event is broadcast to all clients and whether that event supports autoplay.</span></span> <span data-ttu-id="d972e-120">Die Attribute des Ereignis Parameters enthalten den PropertyKey und den VarType eines angegebenen Parameters.</span><span class="sxs-lookup"><span data-stu-id="d972e-120">The event parameter attributes includes a given parameter's PROPERTYKEY and VARTYPE.</span></span>

<span data-ttu-id="d972e-121">Vier Methoden im servicecapabili. cpp-Modul unterstützen das Abrufen von unterstützten Ereignissen für den jeweiligen Contacts-Dienst: **listsupportedevents**, **Display Event**, **displayeventoptions** und **displayeventparameters**.</span><span class="sxs-lookup"><span data-stu-id="d972e-121">Four methods in the ServiceCapabilities.cpp module support the retrieval of supported events for the given Contacts service: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions**, and **DisplayEventParameters**.</span></span> <span data-ttu-id="d972e-122">Die **listsupportedevents** -Methode ruft die Anzahl unterstützter Ereignisse und den GUID-Bezeichner für jedes Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="d972e-122">The **ListSupportedEvents** method retrieves a count of supported events and the GUID identifier for each event.</span></span> <span data-ttu-id="d972e-123">Die **displayevent** -Methode zeigt den Ereignis Namen oder die GUID an und ruft dann **displayeventoptions** und **displayeventparameters** auf, um die ereignisbezogenen Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d972e-123">The **DisplayEvent** method displays the event name or GUID, and then calls **DisplayEventOptions** and **DisplayEventParameters** to display the event-related data.</span></span>

<span data-ttu-id="d972e-124">Die **listsupportedevents** -Methode ruft die [**iportabledeviceservice:: Funktionen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) -Methode auf, um eine [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d972e-124">The **ListSupportedEvents** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="d972e-125">Mithilfe dieser Schnittstelle werden die unterstützten Ereignisse abgerufen, indem die [**iportabledeviceservicecapabili:: getsupportedevents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d972e-125">Using this interface, it retrieves the supported events by calling the [**IPortableDeviceServiceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="d972e-126">Die **getsupportedevents** -Methode ruft die GUIDs für jedes Ereignis ab, das vom Dienst unterstützt wird, und kopiert diese GUIDs in ein [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d972e-126">The **GetSupportedEvents** method retrieves the GUIDs for each event supported by the service and copies those GUIDs into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="d972e-127">Der folgende Code veranschaulicht das Abrufen unterstützter Dienst Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="d972e-127">The following code illustrates retrieving supported service events.</span></span>


```C++
// List all supported events on the service
void ListSupportedEvents(
    IPortableDeviceService* pService)
{
    HRESULT hr          = S_OK;
    DWORD   dwNumEvents = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pEvents;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all events supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedEvents(&pEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get supported events from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported events found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pEvents->GetCount(&dwNumEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Events Found on the service\n\n", dwNumEvents);

    // Loop through each event and display it
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
                    DisplayEvent(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="d972e-128">Nachdem die **listsupportedevents** -Methode die GUIDs abgerufen hat, die die einzelnen Ereignisse darstellen, die vom angegebenen Dienst unterstützt werden, ruft Sie die **displayevent** -Methode auf, um ereignisspezifische Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d972e-128">After the **ListSupportedEvents** method retrieves the GUIDs representing each event supported by the given service, it invokes the **DisplayEvent** method to retrieve event-specific data.</span></span> <span data-ttu-id="d972e-129">Zu diesen Daten gehören der Ereignis Name, seine Optionen (Broadcast oder AutoPlay), Parameter-GUIDs, Parametertypen usw.</span><span class="sxs-lookup"><span data-stu-id="d972e-129">This data includes the event name, its options (broadcast or autoplay), parameter GUIDs, parameter types, and so on.</span></span>

<span data-ttu-id="d972e-130">Die **displayevent** -Methode ruft die [**iportabledeviceservicecapabili:: geteventattributemethode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) auf, um eine Auflistung von Attributen für das angegebene Ereignis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d972e-130">The **DisplayEvent** method invokes the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method to retrieve a collection of attributes for the given event.</span></span> <span data-ttu-id="d972e-131">Anschließend wird die [**iportabledevicevalues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) -Methode aufgerufen, und es wird angefordert, dass der Treiber einen benutzerfreundlichen Namen für das angegebene Ereignis zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d972e-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a user-friendly name for the given event.</span></span> <span data-ttu-id="d972e-132">Als Nächstes ruft **Display Vent** [**iportabledevicevalues:: getiportabledevicevaluesvalue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) auf, um die Ereignis Optionen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d972e-132">Next, **DisplayEvent** calls the [**IPortableDeviceValues::GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) to retrieve the event options.</span></span> <span data-ttu-id="d972e-133">Zum Schluss ruft displayevent [**iportabledevicevalues:: getiportabledevicekeycollectionvalue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) auf, um die Liste der Ereignis Parameter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d972e-133">Finally, DisplayEvent calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the list of event parameters.</span></span> <span data-ttu-id="d972e-134">Sie übergibt die von diesen Methoden zurückgegebenen Daten an die Hilfsfunktionen " **displayeventoptions** " und " **displayeventparameters** ", die die Optionen und Parameterinformationen für das jeweilige Ereignis darstellen.</span><span class="sxs-lookup"><span data-stu-id="d972e-134">It passes the data returned by these methods to the **DisplayEventOptions** and the **DisplayEventParameters** helper functions, which render the options and parameter information for the given event.</span></span>

<span data-ttu-id="d972e-135">Im folgenden Code wird die **displayevent** -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="d972e-135">The following code uses the **DisplayEvent** method.</span></span>


```C++
// Display basic information about an event
void DisplayEvent(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Event)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the event attributes which describe the event
    HRESULT hr = pCapabilities->GetEventAttributes(Event, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the event attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the event if it is available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_EVENT_ATTRIBUTE_NAME, &pszFormatName);
        if (SUCCEEDED(hr))
        {
            printf("%ws\n", pszFormatName);
        }
        else
        {
            printf("%ws\n", (PWSTR)CGuidToString(Event));
        }       

        // Display the event options
        hr = pAttributes->GetIPortableDeviceValuesValue(WPD_EVENT_ATTRIBUTE_OPTIONS, &pOptions);
        if (SUCCEEDED(hr))
        {
            DisplayEventOptions(pOptions);
        }
        else
        {
            printf("! Failed to get the event options, hr = 0x%lx\n", hr);
        }       

        // Display the event parameters
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_EVENT_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayEventParameters(pCapabilities, Event, pParameters);
        }
        else
        {
            printf("! Failed to get the event parameters, hr = 0x%lx\n", hr);
        }       
        
        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



<span data-ttu-id="d972e-136">Die Hilfsfunktion **displayeventoptions** empfängt ein [**iportabledevicevalues**](iportabledevicevalues.md) -Objekt, das die Options Daten des Ereignisses enthält.</span><span class="sxs-lookup"><span data-stu-id="d972e-136">The **DisplayEventOptions** helper function receives an [**IPortableDeviceValues**](iportabledevicevalues.md) object which contains the event's option data.</span></span> <span data-ttu-id="d972e-137">Anschließend wird die [**iportabledevicevalues:: GetBoolValue**](iportabledevicevalues-getboolvalue.md) -Methode aufgerufen, um die Options Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d972e-137">It then calls the [**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) method to retrieve the options data.</span></span> <span data-ttu-id="d972e-138">Mithilfe dieser Daten wird eine Zeichenfolge gerendert, die angibt, ob die Optionen Broadcast und automatische Wiedergabe unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d972e-138">Using this data, it renders a string indicating whether the broadcast and autoplay options are supported.</span></span>


```C++
// Display the basic event options.
void DisplayEventOptions(
    IPortableDeviceValues* pOptions)
{
    printf("\tEvent Options:\n");
    // Read the WPD_EVENT_OPTION_IS_BROADCAST_EVENT value to see if the event is
    // a broadcast event. If the read fails, assume FALSE
    BOOL  bIsBroadcastEvent = FALSE;
    pOptions->GetBoolValue(WPD_EVENT_OPTION_IS_BROADCAST_EVENT, &bIsBroadcastEvent);
    printf("\tWPD_EVENT_OPTION_IS_BROADCAST_EVENT = %ws\n",bIsBroadcastEvent ? L"TRUE" : L"FALSE");
}
```



## <a name="related-topics"></a><span data-ttu-id="d972e-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d972e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d972e-140">**Iportabledevicekeycollection**</span><span class="sxs-lookup"><span data-stu-id="d972e-140">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="d972e-141">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="d972e-141">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="d972e-142">**Iportablede viceservicecapabili**</span><span class="sxs-lookup"><span data-stu-id="d972e-142">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="d972e-143">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="d972e-143">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d972e-144">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="d972e-144">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




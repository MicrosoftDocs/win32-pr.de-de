---
description: Abrufen von unterstützten Dienstereignissen
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Abrufen von unterstützten Dienstereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc1df4c8255a4dc2a1297ae99216437ac3b4c9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423470"
---
# <a name="retrieving-supported-service-events"></a><span data-ttu-id="b29f5-103">Abrufen von unterstützten Dienstereignissen</span><span class="sxs-lookup"><span data-stu-id="b29f5-103">Retrieving Supported Service Events</span></span>

<span data-ttu-id="b29f5-104">Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Contacts-Dienst unterstützten Ereignisse abrufen kann, indem Methoden für die folgenden Schnittstellen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b29f5-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the events supported by a given Contacts service by calling methods on the following interfaces.</span></span>



| <span data-ttu-id="b29f5-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b29f5-105">Interface</span></span>                | <span data-ttu-id="b29f5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b29f5-106">Description</span></span>    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b29f5-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="b29f5-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="b29f5-108">Wird verwendet, um die **IPortableDeviceServiceCapabilities-Schnittstelle** abzurufen, um auf die unterstützten Ereignisse zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b29f5-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="b29f5-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b29f5-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="b29f5-110">Ermöglicht den Zugriff auf die unterstützten Ereignisse und Ereignisattribute.</span><span class="sxs-lookup"><span data-stu-id="b29f5-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="b29f5-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="b29f5-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="b29f5-112">Enthält die Liste der unterstützten Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b29f5-112">Contains the list of supported events.</span></span>                                                                |
| [<span data-ttu-id="b29f5-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b29f5-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="b29f5-114">Enthält die Attribute für ein bestimmtes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b29f5-114">Contains the attributes for a given event.</span></span>                                                            |



 

<span data-ttu-id="b29f5-115">Wenn der Benutzer die Option "4" in der Befehlszeile auswählt, ruft die Anwendung die **ListSupportedEvents-Methode** auf, die sich im Modul ServiceCapabilities.cpp befindet.</span><span class="sxs-lookup"><span data-stu-id="b29f5-115">When the user chooses option "4" at the command line, the application invokes the **ListSupportedEvents** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="b29f5-116">Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontaktdienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="b29f5-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="b29f5-117">In WPD wird ein Ereignis anhand seines Namens, seiner Optionen und seiner Parameter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b29f5-117">In WPD, an event is described by its name, options, and parameters.</span></span> <span data-ttu-id="b29f5-118">Der Ereignisname ist eine skriptfreundliche Zeichenfolge, z.B. "MyCustomEvent".</span><span class="sxs-lookup"><span data-stu-id="b29f5-118">The event name is a script-friendly string, for example, "MyCustomEvent".</span></span> <span data-ttu-id="b29f5-119">Die Ereignisoptionen geben an, ob ein bestimmtes Ereignis an alle Clients übertragen wird und ob dieses Ereignis die automatische Wiedergabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b29f5-119">The event options indicate whether a given event is broadcast to all clients and whether that event supports autoplay.</span></span> <span data-ttu-id="b29f5-120">Die Ereignisparameterattribute enthalten propertykey und VARTYPE eines bestimmten Parameters.</span><span class="sxs-lookup"><span data-stu-id="b29f5-120">The event parameter attributes includes a given parameter's PROPERTYKEY and VARTYPE.</span></span>

<span data-ttu-id="b29f5-121">Vier Methoden im ServiceCapabilities.cpp-Modul unterstützen das Abrufen unterstützter Ereignisse für den angegebenen Contacts-Dienst: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions** und **DisplayEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="b29f5-121">Four methods in the ServiceCapabilities.cpp module support the retrieval of supported events for the given Contacts service: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions**, and **DisplayEventParameters**.</span></span> <span data-ttu-id="b29f5-122">Die **ListSupportedEvents-Methode** ruft die Anzahl der unterstützten Ereignisse und den GUID-Bezeichner für jedes Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="b29f5-122">The **ListSupportedEvents** method retrieves a count of supported events and the GUID identifier for each event.</span></span> <span data-ttu-id="b29f5-123">Die **DisplayEvent-Methode** zeigt den Ereignisnamen oder die GUID an und ruft **dann DisplayEventOptions** und **DisplayEventParameters** auf, um die ereignisbezogenen Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b29f5-123">The **DisplayEvent** method displays the event name or GUID, and then calls **DisplayEventOptions** and **DisplayEventParameters** to display the event-related data.</span></span>

<span data-ttu-id="b29f5-124">Die **ListSupportedEvents-Methode** ruft die [**IPortableDeviceService::Capabilities-Methode auf,**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) um eine [**IPortableDeviceServiceCapabilities-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b29f5-124">The **ListSupportedEvents** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="b29f5-125">Über diese Schnittstelle werden die unterstützten Ereignisse abgerufen, indem die [**IPortableDeviceServiceCapabilities::GetSupportedEvents-Methode aufgerufen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) wird.</span><span class="sxs-lookup"><span data-stu-id="b29f5-125">Using this interface, it retrieves the supported events by calling the [**IPortableDeviceServiceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="b29f5-126">Die **GetSupportedEvents-Methode** ruft die GUIDs für jedes vom Dienst unterstützte Ereignis ab und kopiert diese GUIDs in ein [**IPortableDevicePropVariantCollection-Objekt.**](iportabledevicepropvariantcollection.md)</span><span class="sxs-lookup"><span data-stu-id="b29f5-126">The **GetSupportedEvents** method retrieves the GUIDs for each event supported by the service and copies those GUIDs into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="b29f5-127">Der folgende Code veranschaulicht das Abrufen unterstützter Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="b29f5-127">The following code illustrates retrieving supported service events.</span></span>


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



<span data-ttu-id="b29f5-128">Nachdem die **ListSupportedEvents-Methode** die GUIDs abgerufen hat, die jedes vom angegebenen Dienst unterstützte Ereignis darstellen, ruft sie die **DisplayEvent-Methode** auf, um ereignisspezifische Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b29f5-128">After the **ListSupportedEvents** method retrieves the GUIDs representing each event supported by the given service, it invokes the **DisplayEvent** method to retrieve event-specific data.</span></span> <span data-ttu-id="b29f5-129">Diese Daten umfassen den Ereignisnamen, seine Optionen (Broadcast oder automatische Wiedergabe), Parameter-GUIDs, Parametertypen und so weiter.</span><span class="sxs-lookup"><span data-stu-id="b29f5-129">This data includes the event name, its options (broadcast or autoplay), parameter GUIDs, parameter types, and so on.</span></span>

<span data-ttu-id="b29f5-130">Die **DisplayEvent-Methode** ruft die [**IPortableDeviceServiceCapabilities::GetEventAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) auf, um eine Auflistung von Attributen für das gegebene Ereignis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b29f5-130">The **DisplayEvent** method invokes the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method to retrieve a collection of attributes for the given event.</span></span> <span data-ttu-id="b29f5-131">Anschließend ruft sie die [**IPortableDeviceValues::GetStringValue-Methode**](iportabledevicevalues-getstringvalue.md) auf und fordert an, dass der Treiber einen benutzerfreundlichen Namen für das gegebene Ereignis zurücksendet.</span><span class="sxs-lookup"><span data-stu-id="b29f5-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a user-friendly name for the given event.</span></span> <span data-ttu-id="b29f5-132">Als Nächstes **ruft DisplayEvent** [**IPortableDeviceValues::GetIPortableDeviceValuesValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) auf, um die Ereignisoptionen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b29f5-132">Next, **DisplayEvent** calls the [**IPortableDeviceValues::GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) to retrieve the event options.</span></span> <span data-ttu-id="b29f5-133">Schließlich ruft DisplayEvent den [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) auf, um die Liste der Ereignisparameter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b29f5-133">Finally, DisplayEvent calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the list of event parameters.</span></span> <span data-ttu-id="b29f5-134">Die von diesen Methoden zurückgegebenen Daten werden an die **Hilfsfunktionen DisplayEventOptions** und **DisplayEventParameters** übergeben, die die Optionen und Parameterinformationen für das gegebene Ereignis rendern.</span><span class="sxs-lookup"><span data-stu-id="b29f5-134">It passes the data returned by these methods to the **DisplayEventOptions** and the **DisplayEventParameters** helper functions, which render the options and parameter information for the given event.</span></span>

<span data-ttu-id="b29f5-135">Im folgenden Code wird die **DisplayEvent-Methode** verwendet.</span><span class="sxs-lookup"><span data-stu-id="b29f5-135">The following code uses the **DisplayEvent** method.</span></span>


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



<span data-ttu-id="b29f5-136">Die **DisplayEventOptions-Hilfsfunktion** empfängt ein [**IPortableDeviceValues-Objekt,**](iportabledevicevalues.md) das die Optionsdaten des Ereignisses enthält.</span><span class="sxs-lookup"><span data-stu-id="b29f5-136">The **DisplayEventOptions** helper function receives an [**IPortableDeviceValues**](iportabledevicevalues.md) object which contains the event's option data.</span></span> <span data-ttu-id="b29f5-137">Anschließend wird die [**IPortableDeviceValues::GetBoolValue-Methode**](iportabledevicevalues-getboolvalue.md) aufgerufen, um die Optionsdaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b29f5-137">It then calls the [**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) method to retrieve the options data.</span></span> <span data-ttu-id="b29f5-138">Mithilfe dieser Daten wird eine Zeichenfolge gerendert, die angibt, ob die Broadcast- und Autoplay-Optionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b29f5-138">Using this data, it renders a string indicating whether the broadcast and autoplay options are supported.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b29f5-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b29f5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b29f5-140">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="b29f5-140">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="b29f5-141">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="b29f5-141">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="b29f5-142">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b29f5-142">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="b29f5-143">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b29f5-143">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b29f5-144">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="b29f5-144">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




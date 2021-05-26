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
# <a name="retrieving-supported-service-events"></a>Abrufen von unterstützten Dienstereignissen

Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Contacts-Dienst unterstützten Ereignisse abrufen kann, indem Methoden für die folgenden Schnittstellen aufgerufen werden.



| Schnittstelle                | BESCHREIBUNG    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Wird verwendet, um die **IPortableDeviceServiceCapabilities-Schnittstelle** abzurufen, um auf die unterstützten Ereignisse zuzugreifen. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Ermöglicht den Zugriff auf die unterstützten Ereignisse und Ereignisattribute.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Enthält die Liste der unterstützten Ereignisse.                                                                |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Enthält die Attribute für ein bestimmtes Ereignis.                                                            |



 

Wenn der Benutzer die Option "4" in der Befehlszeile auswählt, ruft die Anwendung die **ListSupportedEvents-Methode** auf, die sich im Modul ServiceCapabilities.cpp befindet.

Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontaktdienst auf einem verbundenen Gerät öffnet.

In WPD wird ein Ereignis anhand seines Namens, seiner Optionen und seiner Parameter beschrieben. Der Ereignisname ist eine skriptfreundliche Zeichenfolge, z.B. "MyCustomEvent". Die Ereignisoptionen geben an, ob ein bestimmtes Ereignis an alle Clients übertragen wird und ob dieses Ereignis die automatische Wiedergabe unterstützt. Die Ereignisparameterattribute enthalten propertykey und VARTYPE eines bestimmten Parameters.

Vier Methoden im ServiceCapabilities.cpp-Modul unterstützen das Abrufen unterstützter Ereignisse für den angegebenen Contacts-Dienst: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions** und **DisplayEventParameters**. Die **ListSupportedEvents-Methode** ruft die Anzahl der unterstützten Ereignisse und den GUID-Bezeichner für jedes Ereignis ab. Die **DisplayEvent-Methode** zeigt den Ereignisnamen oder die GUID an und ruft **dann DisplayEventOptions** und **DisplayEventParameters** auf, um die ereignisbezogenen Daten anzuzeigen.

Die **ListSupportedEvents-Methode** ruft die [**IPortableDeviceService::Capabilities-Methode auf,**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) um eine [**IPortableDeviceServiceCapabilities-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen. Über diese Schnittstelle werden die unterstützten Ereignisse abgerufen, indem die [**IPortableDeviceServiceCapabilities::GetSupportedEvents-Methode aufgerufen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) wird. Die **GetSupportedEvents-Methode** ruft die GUIDs für jedes vom Dienst unterstützte Ereignis ab und kopiert diese GUIDs in ein [**IPortableDevicePropVariantCollection-Objekt.**](iportabledevicepropvariantcollection.md)

Der folgende Code veranschaulicht das Abrufen unterstützter Dienstereignisse.


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



Nachdem die **ListSupportedEvents-Methode** die GUIDs abgerufen hat, die jedes vom angegebenen Dienst unterstützte Ereignis darstellen, ruft sie die **DisplayEvent-Methode** auf, um ereignisspezifische Daten abzurufen. Diese Daten umfassen den Ereignisnamen, seine Optionen (Broadcast oder automatische Wiedergabe), Parameter-GUIDs, Parametertypen und so weiter.

Die **DisplayEvent-Methode** ruft die [**IPortableDeviceServiceCapabilities::GetEventAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) auf, um eine Auflistung von Attributen für das gegebene Ereignis abzurufen. Anschließend ruft sie die [**IPortableDeviceValues::GetStringValue-Methode**](iportabledevicevalues-getstringvalue.md) auf und fordert an, dass der Treiber einen benutzerfreundlichen Namen für das gegebene Ereignis zurücksendet. Als Nächstes **ruft DisplayEvent** [**IPortableDeviceValues::GetIPortableDeviceValuesValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) auf, um die Ereignisoptionen abzurufen. Schließlich ruft DisplayEvent den [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) auf, um die Liste der Ereignisparameter abzurufen. Die von diesen Methoden zurückgegebenen Daten werden an die **Hilfsfunktionen DisplayEventOptions** und **DisplayEventParameters** übergeben, die die Optionen und Parameterinformationen für das gegebene Ereignis rendern.

Im folgenden Code wird die **DisplayEvent-Methode** verwendet.


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



Die **DisplayEventOptions-Hilfsfunktion** empfängt ein [**IPortableDeviceValues-Objekt,**](iportabledevicevalues.md) das die Optionsdaten des Ereignisses enthält. Anschließend wird die [**IPortableDeviceValues::GetBoolValue-Methode**](iportabledevicevalues-getboolvalue.md) aufgerufen, um die Optionsdaten abzurufen. Mithilfe dieser Daten wird eine Zeichenfolge gerendert, die angibt, ob die Broadcast- und Autoplay-Optionen unterstützt werden.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




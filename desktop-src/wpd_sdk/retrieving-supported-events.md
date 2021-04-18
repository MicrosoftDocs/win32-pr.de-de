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
# <a name="retrieving-supported-service-events"></a>Abrufen unterstützter Dienst Ereignisse

Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung die Ereignisse abrufen kann, die von einem bestimmten Kontakt Dienst unterstützt werden, indem Methoden für die folgenden Schnittstellen aufgerufen werden.



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Schnittstelle                                                                            | BESCHREIBUNG                                                                                           |
| [**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Wird zum Abrufen der **iportabledeviceservicecapabili-** Schnittstelle verwendet, um auf die unterstützten Ereignisse zuzugreifen. |
| [**Iportablede viceservicecapabili**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Bietet Zugriff auf die unterstützten Ereignisse und Ereignis Attribute.                                         |
| [**Iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) | Enthält die Liste der unterstützten Ereignisse.                                                                |
| [**Iportablede vicevalues**](iportabledevicevalues.md)                               | Enthält die Attribute für ein bestimmtes Ereignis.                                                            |



 

Wenn der Benutzer die Option "4" in der Befehlszeile auswählt, ruft die Anwendung die **listsupportedevents** -Methode auf, die im Modul "servicecapabili. cpp" zu finden ist.

Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontakt Dienst auf einem verbundenen Gerät öffnet.

In WPD wird ein Ereignis anhand des Namens, der Optionen und der Parameter beschrieben. Der Ereignis Name ist eine Skript freundliche Zeichenfolge, z. b. "mycustomevent". Die Ereignis Optionen geben an, ob ein bestimmtes Ereignis an alle Clients gesendet wird und ob dieses Ereignis die automatische Wiedergabe unterstützt. Die Attribute des Ereignis Parameters enthalten den PropertyKey und den VarType eines angegebenen Parameters.

Vier Methoden im servicecapabili. cpp-Modul unterstützen das Abrufen von unterstützten Ereignissen für den jeweiligen Contacts-Dienst: **listsupportedevents**, **Display Event**, **displayeventoptions** und **displayeventparameters**. Die **listsupportedevents** -Methode ruft die Anzahl unterstützter Ereignisse und den GUID-Bezeichner für jedes Ereignis ab. Die **displayevent** -Methode zeigt den Ereignis Namen oder die GUID an und ruft dann **displayeventoptions** und **displayeventparameters** auf, um die ereignisbezogenen Daten anzuzeigen.

Die **listsupportedevents** -Methode ruft die [**iportabledeviceservice:: Funktionen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) -Methode auf, um eine [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Schnittstelle abzurufen. Mithilfe dieser Schnittstelle werden die unterstützten Ereignisse abgerufen, indem die [**iportabledeviceservicecapabili:: getsupportedevents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) -Methode aufgerufen wird. Die **getsupportedevents** -Methode ruft die GUIDs für jedes Ereignis ab, das vom Dienst unterstützt wird, und kopiert diese GUIDs in ein [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt.

Der folgende Code veranschaulicht das Abrufen unterstützter Dienst Ereignisse.


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



Nachdem die **listsupportedevents** -Methode die GUIDs abgerufen hat, die die einzelnen Ereignisse darstellen, die vom angegebenen Dienst unterstützt werden, ruft Sie die **displayevent** -Methode auf, um ereignisspezifische Daten abzurufen. Zu diesen Daten gehören der Ereignis Name, seine Optionen (Broadcast oder AutoPlay), Parameter-GUIDs, Parametertypen usw.

Die **displayevent** -Methode ruft die [**iportabledeviceservicecapabili:: geteventattributemethode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) auf, um eine Auflistung von Attributen für das angegebene Ereignis abzurufen. Anschließend wird die [**iportabledevicevalues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) -Methode aufgerufen, und es wird angefordert, dass der Treiber einen benutzerfreundlichen Namen für das angegebene Ereignis zurückgibt. Als Nächstes ruft **Display Vent** [**iportabledevicevalues:: getiportabledevicevaluesvalue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) auf, um die Ereignis Optionen abzurufen. Zum Schluss ruft displayevent [**iportabledevicevalues:: getiportabledevicekeycollectionvalue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) auf, um die Liste der Ereignis Parameter abzurufen. Sie übergibt die von diesen Methoden zurückgegebenen Daten an die Hilfsfunktionen " **displayeventoptions** " und " **displayeventparameters** ", die die Optionen und Parameterinformationen für das jeweilige Ereignis darstellen.

Im folgenden Code wird die **displayevent** -Methode verwendet.


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



Die Hilfsfunktion **displayeventoptions** empfängt ein [**iportabledevicevalues**](iportabledevicevalues.md) -Objekt, das die Options Daten des Ereignisses enthält. Anschließend wird die [**iportabledevicevalues:: GetBoolValue**](iportabledevicevalues-getboolvalue.md) -Methode aufgerufen, um die Options Daten abzurufen. Mithilfe dieser Daten wird eine Zeichenfolge gerendert, die angibt, ob die Optionen Broadcast und automatische Wiedergabe unterstützt werden.


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

[**Iportabledevicekeycollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Iportablede viceservicecapabili**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**Iportablede vicevalues**](iportabledevicevalues.md)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




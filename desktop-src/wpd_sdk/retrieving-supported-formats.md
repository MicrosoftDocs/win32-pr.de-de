---
description: Abrufen unterstützter Dienstformate
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Abrufen unterstützter Dienstformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73618f3450255ad470545ac472ad9f71238621e3
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423811"
---
# <a name="retrieving-supported-service-formats"></a>Abrufen unterstützter Dienstformate

Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Contacts-Dienst unterstützten Formate abrufen kann, indem methoden der Schnittstellen in der folgenden Tabelle aufgerufen werden.



| Schnittstelle | BESCHREIBUNG   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Wird zum Abrufen der **IPortableDeviceServiceCapabilities-Schnittstelle** für den Zugriff auf die unterstützten Ereignisse verwendet. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Ermöglicht den Zugriff auf die unterstützten Ereignisse und Ereignisattribute.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Enthält die Liste der unterstützten Formate.                                                               |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Enthält die Attribute für ein bestimmtes Format.                                                           |



 

Wenn der Benutzer die Option "3" in der Befehlszeile auswählt, ruft die Anwendung die **ListSupportedFormats-Methode** auf, die sich im Modul ServiceCapabilities.cpp befindet.

Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontaktdienst auf einem verbundenen Gerät öffnet.

In WPD wird ein Format durch Attribute beschrieben, die den Namen und (optional) den MIME-Typ eines bestimmten Formats angeben. Diese Attribute werden in der HeaderdateiPortableDevice.h definiert. Eine Beschreibung der unterstützten Attribute finden Sie im Thema [Attribute.](attributes.md)

Wenn wpdServiceSampleDriver das einzige installierte Gerät ist, gibt der Treiber im Fall der Beispielanwendung zwei unterstützte Formate für den Contact-Dienst zurück: "AbstractContactFormat" und "VCard2Format". Diese Formate entsprechen den **WPD \_ OBJECT FORMAT \_ ABSTRACT \_ \_ CONTACT-** und **WPD OBJECT FORMAT \_ \_ \_ VCARD2-Attributen** in PortableDevice.h.

Zwei Methoden im Modul ServiceCapabilities.cpp unterstützen das Abrufen unterstützter Formate für den Contacts-Dienst: **ListSupportedFormats** und **DisplayFormat**. Erstere ruft den GUID-Bezeichner für jedes unterstützte Format ab. Letztere konvertiert diese GUID in eine benutzerfreundliche Zeichenfolge.

Die **ListSupportedFormats-Methode** ruft die [**IPortableDeviceService::Capabilities-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**IPortableDeviceServiceCapabilities-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen. Mit dieser Schnittstelle werden die unterstützten Formate abgerufen, indem die [**IPortableDeviceServiceCapabilities::GetSupportedFormats-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) aufgerufen wird. Die **GetSupportedFormats-Methode** ruft die GUID für jedes vom Dienst unterstützte Format ab und kopiert diese GUID in ein [**IPortableDevicePropVariantCollection-Objekt.**](iportabledevicepropvariantcollection.md)

Im folgenden Code wird die **ListSupportedFormats-Methode** verwendet.


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

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

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



Nachdem die **ListSupportedFormats-Methode** die GUID für jedes vom angegebenen Dienst unterstützte Format abgerufen hat, ruft sie die **DisplayFormat-Methode** auf, um den Anzeigenamen des Skripts für jedes Format anzuzeigen. Beispiel: "VCard2".

Die **DisplayFormat-Methode** ruft die [**IPortableDeviceServiceCapabilities::GetFormatAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) auf, um eine Auflistung von Attributen für die angegebene Format-GUID abzurufen. Anschließend ruft sie die [**IPortableDeviceValues::GetStringValue-Methode**](iportabledevicevalues-getstringvalue.md) auf und fordert an, dass der Treiber einen skriptfreundlichen Namen für das angegebene Format zurückgibt.

Im folgenden Code wird die **DisplayFormat-Methode** verwendet.


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




---
description: Abrufen unterstützter Dienst Formate
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Abrufen unterstützter Dienst Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed8021d8feefaaad3da7905e17e8c658dfb19e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362898"
---
# <a name="retrieving-supported-service-formats"></a>Abrufen unterstützter Dienst Formate

Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung die Formate abrufen kann, die von einem bestimmten Kontakt Dienst unterstützt werden, indem Methoden der Schnittstellen in der folgenden Tabelle aufgerufen werden.



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Schnittstelle                                                                            | BESCHREIBUNG                                                                                           |
| [**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Wird zum Abrufen der **iportabledeviceservicecapabili-** Schnittstelle verwendet, um auf die unterstützten Ereignisse zuzugreifen. |
| [**Iportablede viceservicecapabili**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Bietet Zugriff auf die unterstützten Ereignisse und Ereignis Attribute.                                         |
| [**Iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) | Enthält die Liste der unterstützten Formate.                                                               |
| [**Iportablede vicevalues**](iportabledevicevalues.md)                               | Enthält die Attribute für ein bestimmtes Format.                                                           |



 

Wenn der Benutzer die Option "3" in der Befehlszeile auswählt, ruft die Anwendung die **listsupportedformats** -Methode auf, die im Modul "servicecapabili. cpp" zu finden ist.

Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontakt Dienst auf einem verbundenen Gerät öffnet.

In WPD wird ein Format von Attributen beschrieben, die den Namen und (optional) den MIME-Typ eines gegebenen Formats angeben. Diese Attribute werden in der Header Datei "portabledevice. h" definiert. Eine Beschreibung der unterstützten Attribute finden Sie im Thema [Attribute](attributes.md) .

Bei der Beispielanwendung gibt der Treiber, wenn wpdservicesampledriver das einzige installierte Gerät ist, zwei unterstützte Formate für den Kontakt Dienst an: "abstractcontactformat" und "VCard2Format". Diese Formate entsprechen dem **\_ \_ \_ abstrakten \_ Kontakt im WPD-Objekt Format** und dem **WPD- \_ Objekt \_ Format \_ VCARD2** Attribute in "portabledevice. h".

Zwei Methoden im servicecapabili. cpp-Modul unterstützen den Abruf unterstützter Formate für den Contacts-Dienst: **listsupportedformats** und **Display Format**. Der erste Ruft den GUID-Bezeichner für jedes unterstützte Format ab. Letztere konvertiert diese GUID in eine benutzerfreundliche Zeichenfolge.

Die **listsupportedformats** -Methode ruft die [**iportabledeviceservice:: Funktionen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) -Methode auf, um eine [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Schnittstelle abzurufen. Mithilfe dieser Schnittstelle werden die unterstützten Formate durch Aufrufen der [**iportabledeviceservicecapabili:: GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) -Methode abgerufen. Die **GetSupportedFormats** -Methode ruft die GUID für jedes Format ab, das vom Dienst unterstützt wird, und kopiert diese GUID in ein [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt.

Im folgenden Code wird die **listsupportedformats** -Methode verwendet.


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



Nachdem die **listsupportedformats** -Methode die GUID für jedes vom angegebenen Dienst unterstützte Format abgerufen hat, ruft Sie die **DisplayFormat** -Methode auf, um den anzeigen amen des Skripts für die einzelnen Formate anzuzeigen. Beispiel: "VCard2".

Die **DisplayFormat** -Methode ruft die [**iportabledeviceservicecapabili:: getformattribute**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) -Methode auf, um eine Auflistung von Attributen für die angegebene Format-GUID abzurufen. Anschließend wird die [**iportabledevicevalues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) -Methode aufgerufen, und es wird angefordert, dass der Treiber einen Skript freundlichen Namen für das angegebene Format zurückgibt.

Im folgenden Code wird die **DisplayFormat** -Methode verwendet.


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

[**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Iportablede viceservicecapabili**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**Iportablede vicevalues**](iportabledevicevalues.md)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




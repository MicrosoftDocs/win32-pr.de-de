---
description: Aufzählen von Dienstinhalten
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Aufzählen von Dienstinhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9846565b7cdc4b0a4475cb99806b671452dcbe134e40d4b1e3d70df249c510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083564"
---
# <a name="enumerating-service-content"></a>Aufzählen von Dienstinhalten

Nachdem Ihre Anwendung einen Dienst geöffnet hat, kann sie mit dem Ausführen dienstbezogener Vorgänge beginnen. Im Fall der WpdServicesApiSample-Anwendung ist einer dieser Vorgänge die Enumeration des Inhalts für einen bestimmten Contacts-Dienst. In der folgenden Tabelle werden die verwendeten Schnittstellen beschrieben.



| Schnittstelle                                                            | BESCHREIBUNG                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Wird verwendet, um die IPortableDeviceContent2-Schnittstelle abzurufen, um auf Inhalte im Dienst zuzugreifen.         |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Wird verwendet, um die IEnumPortableDeviceObjectIDs-Schnittstelle abzurufen, um Objekte für den Dienst aufzuzählen. |
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | Wird verwendet, um Objekte für den Dienst aufzuzählen.                                                        |



 

Der Inhaltsenumerationscode befindet sich im ContentEnumeration.cpp-Modul. Dieser Code befindet sich in den Methoden **EnumerateAllContent** und **RecursiveEnumerate.** Die frühere Methode ruft letztere auf.

Die **EnumerateContent-Methode** verwendet einen Zeiger auf ein [**IPortableDeviceService-Objekt**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) als einen Parameter. Dieses Objekt entspricht einem Dienst, den die Anwendung zuvor beim Aufruf der [**IPortableDeviceService::Open-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) geöffnet hat.

Die **EnumerateContent-Methode** erstellt ein [**IPortableDeviceContent2-Objekt**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) und übergibt dieses Objekt an die [**IPortableDeviceService::Content-Methode.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) Diese Methode ruft wiederum den Inhalt auf der Stammebene des Diensts ab und beginnt dann rekursiv mit dem Abrufen von Inhalten, die unterhalb des Stamms gefunden wurden.

Der folgende Code entspricht der **EnumerateContent-Methode.**


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



Der folgende Code entspricht der **RecursiveEnumerate-Methode.** Die RecursiveEnumerate-Methode instanziiert eine **IEnumPortableDeviceObjectIDs-Schnittstelle** für das angegebene übergeordnete Objekt und ruft **IEnumPortableDeviceObjectIDs::Next** auf und ruft einen Batch von unmittelbar untergeordneten Objekten ab. Für jedes untergeordnete Objekt wird RecursiveEnumerate erneut aufgerufen, um seine untergeordneten Nachfolgerobjekte zurückzugeben usw.


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**IPortableDeviceContent2-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceService-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[Öffnen eines Diensts](opening-a-service.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




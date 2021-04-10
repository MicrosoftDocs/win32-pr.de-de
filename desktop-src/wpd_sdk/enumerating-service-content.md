---
description: Auflisten von Dienst Inhalten
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Auflisten von Dienst Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adb949fdec9a0001583b1481ccd50ada1ef1df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214539"
---
# <a name="enumerating-service-content"></a>Auflisten von Dienst Inhalten

Nachdem die Anwendung einen Dienst geöffnet hat, kann Sie damit beginnen, Dienst bezogene Vorgänge auszuführen. Im Fall der Anwendung wpdservicesapisample ist einer dieser Vorgänge die Enumeration von Inhalten für einen bestimmten Kontakt Dienst. In der folgenden Tabelle werden die verwendeten Schnittstellen beschrieben.



|                                                                      |                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Schnittstelle                                                            | BESCHREIBUNG                                                                                      |
| [**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Dient zum Abrufen der IPortableDeviceContent2-Schnittstelle für den Zugriff auf den-Dienst.         |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Wird zum Abrufen der ienumportabledeviceobjectids-Schnittstelle verwendet, um Objekte im Dienst aufzulisten. |
| [**Ienumportabledeviceobjectids**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | Wird verwendet, um Objekte im Dienst aufzulisten.                                                        |



 

Der inhaltsaufzählungs Code befindet sich im Modul "contentenumeration. cpp". Dieser Code befindet sich in den **enumerateallcontent** -und **recursiveenumerate** -Methoden. Die erste Methode ruft letztere auf.

Die **enumeratecontent** -Methode nimmt einen Zeiger auf ein [**iportabledeviceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) -Objekt als einen Parameter an. Dieses Objekt entspricht einem Dienst, den die Anwendung zuvor geöffnet hat, als die [**iportabledeviceservice:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) -Methode aufgerufen wurde.

Die **enumeratecontent** -Methode erstellt ein [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) -Objekt und übergibt dieses Objekt an die [**iportabledeviceservice:: Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) -Methode. Diese Methode ruft wiederum den Inhalt auf der Stamm Ebene des diensdienstanzen ab und beginnt dann rekursiv mit dem Abrufen von Inhalt, der unterhalb des Stamms gefunden wurde.

Der folgende Code entspricht der **enumeratecontent** -Methode.


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



Der folgende Code entspricht der **recursiveenumerate** -Methode. Die recursiveenumerate-Methode instanziiert eine **ienumportabledeviceobjectids** -Schnittstelle für das angegebene übergeordnete Objekt und ruft **ienumportabledeviceobjectids:: Next** auf, wobei ein Batch der unmittelbaren untergeordneten Objekte abgerufen wird. Für jedes untergeordnete Objekt wird rekursiveenumerate erneut aufgerufen, um seine untergeordneten Objekte zurückzugeben, usw.


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

[**Ienumportabledeviceobjectids**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**IPortableDeviceContent2-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**Iportablede viceservice-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[Öffnen eines Dienstanbieter](opening-a-service.md)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




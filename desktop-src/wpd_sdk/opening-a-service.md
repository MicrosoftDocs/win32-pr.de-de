---
description: Öffnen eines Diensts
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Öffnen eines Diensts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 578dfee696fd17b0e360d6e344844670ca92ac6b48152242492a458a9a279f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806720"
---
# <a name="opening-a-service"></a>Öffnen eines Diensts

Bevor Ihre Anwendung Vorgänge für einen Dienst ausführen kann, z. B. das Aufzählen von Inhalt oder das Abrufen von Beschreibungen unterstützter Ereignisse oder Methoden, muss sie den Dienst öffnen. In der WpdServicesApiSample-Anwendung wird diese Aufgabe im Modul ServiceEnumeration.cpp unter Verwendung der in der folgenden Tabelle beschriebenen Schnittstellen gezeigt.



| Schnittstelle                                                              | BESCHREIBUNG                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | Wird zum Aufzählen der Dienste auf einem Gerät verwendet.        |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Wird verwendet, um eine Verbindung mit einem Gerätedienst zu öffnen.     |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Wird verwendet, um die Clientinformationen der Anwendung zu enthalten. |



 

Die Methode zum Öffnen eines Diensts ist [**IPortableDeviceService::Open.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) Diese Methode verwendet zwei Argumente: einen Plug-and-Play-Bezeichner (PnP) für den Dienst und ein [**IPortableDeviceValues-Objekt,**](iportabledevicevalues.md) das die Clientinformationen der Anwendung enthält.

Um einen PnP-Bezeichner für einen bestimmten Dienst abzurufen, ruft Ihre Anwendung die [**IPortableDeviceServiceManager::GetDeviceServices-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) auf. Diese Methode ruft ein Array von PnP-Bezeichnern für Dienste einer Dienstkategorie-GUID ab (z. B. SERVICE-Kontakte).

Die Beispieldienstanwendung ruft einen PnP-Bezeichner für Contacts-Dienste innerhalb der **EnumerateContactsServices-Methode** im Modul ServiceEnumeration.cpp ab. Das folgende Codebeispiel wurde aus dieser Methode entnommen.


```C++
// For each device found, find the contacts service
for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
{
    DWORD   cPnpServiceIDs = 0;
    PWSTR   pPnpServiceID  = NULL;

    // First, pass NULL as the PWSTR array pointer to get the total number
    // of contacts services (SERVICE_Contacts) found on the device.
    // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
    hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
    
    if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
    {                               
        // For simplicity, we are only using the first contacts service on each device
        cPnpServiceIDs = 1;
        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

        if (SUCCEEDED(hr))
        {
            // We've found the service, display it and save its PnP Identifier
            ContactsServicePnpIDs.Add(pPnpServiceID);

            printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

            // Display information about the device that contains this service.
            DisplayDeviceInformation(pServiceManager, pPnpServiceID);

            // ContactsServicePnpIDs now owns the memory for this string
            pPnpServiceID = NULL;
        }
        else
        {
            printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
        }
    }
}
```



Nachdem Ihre Anwendung den PnP-Bezeichner für den Dienst abgerufen hat, kann sie die Clientinformationen einrichten und [**IPortableDeviceService::Open aufrufen.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)

In der Beispielanwendung wird diese Methode in **ChooseDeviceService** im Modul ServiceEnumeration.cpp aufgerufen.

[**IPortableDeviceService unterstützt**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) zwei CLSIDs für **CoCreateInstance.** **CLSID \_ PortableDeviceService gibt** einen **IPortableDeviceService-Zeiger** zurück, der den Freethread-Marshaller nicht aggregiert. **CLSID \_ PortableDeviceServiceFTM** ist eine neue CLSID, die einen **IPortableDeviceService-Zeiger** zurückgibt, der den Marshaller mit Freiem Thread aggregiert. Andernfalls unterstützen beide Zeiger die gleiche Funktionalität.

Anwendungen, die in SingleThreaded Apartment leben, sollten **CLSID \_ PortableDeviceServiceFTM** verwenden, da dadurch der Aufwand für das Marshalling von Schnittstellenzeigern entfällt. **CLSID \_ PortableDeviceService wird** weiterhin für Legacyanwendungen unterstützt.


```C++
hr = CoCreateInstance(CLSID_PortableDeviceServiceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pService));
if (SUCCEEDED(hr))
{
    hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the service for Read Write access, will open it for Read-only access instead\n");

            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);

            hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);

            if (FAILED(hr))
            {
                printf("! Failed to Open the service for Read access, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to Open the service, hr = 0x%lx\n",hr);
        }
    }
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDeviceService-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceServiceManager-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




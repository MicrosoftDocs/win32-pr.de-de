---
description: Öffnen eines Dienstanbieter
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Öffnen eines Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0bcccc6c3769173bfee72e73d7cbf68435b0ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529525"
---
# <a name="opening-a-service"></a>Öffnen eines Dienstanbieter

Bevor die Anwendung Vorgänge für einen Dienst ausführen kann, z. b. das Auflisten von Inhalten oder das Abrufen von Beschreibungen unterstützter Ereignisse oder Methoden, muss der Dienst geöffnet werden. In der Anwendung wpdservicesapisample wird diese Aufgabe im serviceenumeration. cpp-Modul mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen veranschaulicht.



|                                                                        |                                                    |
|------------------------------------------------------------------------|----------------------------------------------------|
| Schnittstelle                                                              | BESCHREIBUNG                                        |
| [**Iportablede viceservicemanager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | Wird verwendet, um die Dienste auf einem Gerät aufzuzählen.        |
| [**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Wird verwendet, um eine Verbindung mit einem Geräte Dienst zu öffnen.     |
| [**Iportablede vicevalues**](iportabledevicevalues.md)                 | Wird verwendet, um die Client Informationen der Anwendung zu speichern. |



 

Die Methode, die einen Dienst öffnet, ist [**iportabledeviceservice:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open). Diese Methode nimmt zwei Argumente an: einen PNP-Bezeichner (Plug-and-Play) für den Dienst und ein [**iportabledevicevalues**](iportabledevicevalues.md) -Objekt, das die Client Informationen der Anwendung enthält.

Um einen PNP-Bezeichner für einen bestimmten Dienst zu erhalten, ruft Ihre Anwendung die [**iportabledeviceservicemanager:: getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) -Methode auf. Diese Methode ruft ein Array von PNP-Bezeichner für Dienste einer Dienst Kategorie-GUID (z. b. Dienst Kontakte) ab.

Die Beispiel Dienst Anwendung ruft einen PNP-Bezeichner für Kontakte Dienste innerhalb der **enumeratecontactsservices** -Methode im serviceenumeration. cpp-Modul ab. Das folgende Codebeispiel stammt aus dieser Methode.


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



Nachdem die Anwendung den PNP-Bezeichner für den Dienst abgerufen hat, kann Sie die Client Informationen einrichten und [**iportabledeviceservice:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)aufrufen.

In der Beispielanwendung wird diese Methode innerhalb von **choosedeviceservice** im serviceenumeration. cpp-Modul aufgerufen.

[**Iportableendviceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) unterstützt zwei CLSIDs für **cokreatabstance**. **CLSID \_ Portableendviceservice** gibt einen **iportableendviceservice** -Zeiger zurück, der den Freethread-Mars Haller nicht aggregiert. **CLSID \_ Portableendviceserviceftm** ist eine neue CLSID, die einen **iportableendviceservice** -Zeiger zurückgibt, der den frei Thread-Mars Haller aggregiert. Beide Zeiger unterstützen andernfalls dieselbe Funktionalität.

Anwendungen, die in Single Thread-Apartments Leben, sollten **CLSID \_ portabletoviceserviceftm** verwenden, da dadurch der Aufwand für das Marshalling von Schnittstellen Zeigern entfällt. **CLSID \_ Portablede viceservice** wird weiterhin für ältere Anwendungen unterstützt.


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

[**Iportablede viceservice-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportabledebug Service Service Manager-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




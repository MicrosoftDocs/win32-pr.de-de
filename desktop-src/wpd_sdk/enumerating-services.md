---
description: Auflisten von Diensten
ms.assetid: 6ee6eecb-3812-45c6-8b27-7dfd6fa82758
title: Auflisten von Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2eca8221a9a34bf9e921bcaca00eac99f2a75d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366303"
---
# <a name="enumerating-services"></a>Auflisten von Diensten

Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung alle Kontakte Dienste auflisten kann, die auf einem der derzeit mit einem Computer verbundenen Geräte gefunden werden.

Wenn der Benutzer die Option "0" in der Befehlszeile auswählt, ruft die Anwendung die **enumeratecontactsservices** -Methode auf, die im serviceenumeration. cpp-Modul zu finden ist. Mit dieser Methode wird eine Liste aller verbundenen Geräte angezeigt, die den Kontakt Dienst unterstützen.

Wenn z. b. "wpdservicesampledriver" das einzige installierte Gerät ist, gibt die Anwendung drei Datenfelder zurück: einen anzeigen Amen ("Beispiel Medium"), einen Hersteller ("Windows-Gruppe für tragbare Geräte") und eine Beschreibung ("Contact Service Device 2000").

Die **enumeratecontactsservices** -Methode führt die folgenden Aufgaben aus:

-   Erstellt eine [**iportabledebug-Manager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) -Schnittstelle, um die Enumeration installierter Geräte zu verarbeiten.
-   Erstellt eine [**iportableendviceservicemanager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) -Schnittstelle, um die Enumeration der Dienste auf jedem Gerät zu verarbeiten.
-   Durchläuft die installierten Geräte, sucht nach dem Kontakt Dienst und zeigt die Geräteinformationen für jedes Gerät an, das diesen Dienst unterstützt.

Der folgende Code veranschaulicht die **enumeratecontactsservices** -Methode.


```C++
// Enumerates all Contacts Services, displaying the associated device of each service.
void EumerateContactsServices(CAtlArray<PWSTR>& ContactsServicePnpIDs)
{
    HRESULT                                 hr              = S_OK;
    DWORD                                   cPnpDeviceIDs   = 0;
    PWSTR*                                  pPnpDeviceIDs   = NULL;
    CComPtr<IPortableDeviceManager>         pPortableDeviceManager;
    CComPtr<IPortableDeviceServiceManager>  pServiceManager;

    // CoCreate the IPortableDeviceManager interface to enumerate
    // portable devices and to get information about them.
    hr = CoCreateInstance(CLSID_PortableDeviceManager,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pPortableDeviceManager));

    if (FAILED(hr))
    {
        printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
    }        

    // Retrieve the IPortableDeviceServiceManager interface to enumerate device services.
    if (SUCCEEDED(hr))
    {
        hr = pPortableDeviceManager->QueryInterface(IID_PPV_ARGS(&pServiceManager));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface IID_IPortableDeviceServiceManager, hr = 0x%lx\n",hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        // First, pass NULL as the PWSTR array pointer to get the total number
        // of devices found on the system.
        hr = pPortableDeviceManager->GetDevices(NULL, &cPnpDeviceIDs);

        if (FAILED(hr))
        {
            printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
        }

        if (SUCCEEDED(hr) && (cPnpDeviceIDs > 0))
        {
            // Second, allocate an array to hold the PnPDeviceID strings returned from
            // the IPortableDeviceManager::GetDevices method
            pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnpDeviceIDs];

            if (pPnpDeviceIDs != NULL)
            {
                DWORD dwIndex = 0;

                hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
                if (SUCCEEDED(hr))
                {   
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
                }

                // Free all returned PnPDeviceID strings
                FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);

                // Delete the array of PWSTR pointers
                delete [] pPnpDeviceIDs;
                pPnpDeviceIDs = NULL;

            }
            else
            {
                printf("! Failed to allocate memory for PWSTR array\n");
            }            
        }
    }
    
    printf("\n%d Contacts Device Service(s) found on the system\n\n", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()));
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iportabledebug Manager-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**Iportabledebug Service Service Manager-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




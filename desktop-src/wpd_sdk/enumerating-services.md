---
description: Aufzählen von Diensten
ms.assetid: 6ee6eecb-3812-45c6-8b27-7dfd6fa82758
title: Aufzählen von Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149384f9c4ab5cf352561d08b28a961c8074cc39c018cef6b5deb64307d107ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697606"
---
# <a name="enumerating-services"></a>Aufzählen von Diensten

Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung alle Kontaktdienste auf einem der Geräte aufzählen kann, die derzeit mit einem Computer verbunden sind.

Wenn der Benutzer die Option "0" in der Befehlszeile auswählt, ruft die Anwendung die **EnumerateContactsServices-Methode** auf, die sich im Modul ServiceEnumeration.cpp befindet. Diese Methode zeigt eine Liste aller verbundenen Geräte an, die den Kontaktdienst unterstützen.

Wenn wpdServiceSampleDriver beispielsweise das einzige installierte Gerät ist, gibt die Anwendung drei Datenfelder zurück: einen Anzeigenamen ("Beispielgerät"), einen Hersteller ("Windows Gruppe portabler Geräte") und eine Beschreibung ("Contacts Service Device 2000").

Die **EnumerateContactsServices-Methode** führt die folgenden Aufgaben aus:

-   Erstellt eine [**IPortableDeviceManager-Schnittstelle,**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) um die Enumeration installierter Geräte zu verarbeiten.
-   Erstellt eine [**IPortableDeviceServiceManager-Schnittstelle,**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) um die Enumeration der Dienste auf jedem Gerät zu verarbeiten.
-   Durchläuft die installierten Geräte, sucht nach dem Dienst Kontakte und zeigt die Geräteinformationen für jedes Gerät an, das diesen Dienst unterstützt.

Der folgende Code veranschaulicht die **EnumerateContactsServices-Methode.**


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

[**IPortableDeviceManager-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**IPortableDeviceServiceManager-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




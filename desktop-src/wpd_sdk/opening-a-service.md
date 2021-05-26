---
description: Öffnen eines Diensts
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Öffnen eines Diensts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b273b8709a4d750085f14075d605f88ed0faa6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423920"
---
# <a name="opening-a-service"></a><span data-ttu-id="68e41-103">Öffnen eines Diensts</span><span class="sxs-lookup"><span data-stu-id="68e41-103">Opening a Service</span></span>

<span data-ttu-id="68e41-104">Bevor Ihre Anwendung Vorgänge für einen Dienst ausführen kann, z. B. das Aufzählen von Inhalten oder das Abrufen von Beschreibungen unterstützter Ereignisse oder Methoden, muss der Dienst geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="68e41-104">Before your application can perform operations on a service, for example, enumerating content or retrieving descriptions of supported events or methods, it must open the service.</span></span> <span data-ttu-id="68e41-105">In der WpdServicesApiSample-Anwendung wird diese Aufgabe im ServiceEnumeration.cpp-Modul mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="68e41-105">In the WpdServicesApiSample application, this task is demonstrated in the ServiceEnumeration.cpp module using the interfaces described in the following table.</span></span>



| <span data-ttu-id="68e41-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="68e41-106">Interface</span></span>                                                              | <span data-ttu-id="68e41-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68e41-107">Description</span></span>                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="68e41-108">**IPortableDeviceServiceManager**</span><span class="sxs-lookup"><span data-stu-id="68e41-108">**IPortableDeviceServiceManager**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | <span data-ttu-id="68e41-109">Wird verwendet, um die Dienste auf einem Gerät aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="68e41-109">Used to enumerate the services on a device.</span></span>        |
| [<span data-ttu-id="68e41-110">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="68e41-110">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="68e41-111">Wird verwendet, um eine Verbindung mit einem Gerätedienst zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="68e41-111">Used to open a connection to a device service.</span></span>     |
| [<span data-ttu-id="68e41-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="68e41-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="68e41-113">Wird verwendet, um die Clientinformationen der Anwendung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="68e41-113">Used to hold the application's client information.</span></span> |



 

<span data-ttu-id="68e41-114">Die Methode, die einen Dienst öffnet, ist [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="68e41-114">The method that opens a service is [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span> <span data-ttu-id="68e41-115">This method takes two arguments: a Plug-and-Play (PnP) identifier for the service and an [**IPortableDeviceValues**](iportabledevicevalues.md) object that contains the application's client information.</span><span class="sxs-lookup"><span data-stu-id="68e41-115">This method takes two arguments: a Plug-and-Play (PnP) identifier for the service and an [**IPortableDeviceValues**](iportabledevicevalues.md) object that contains the application's client information.</span></span>

<span data-ttu-id="68e41-116">Um einen PnP-Bezeichner für einen bestimmten Dienst abzurufen, ruft Ihre Anwendung die [**IPortableDeviceServiceManager::GetDeviceServices-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) auf.</span><span class="sxs-lookup"><span data-stu-id="68e41-116">To obtain a PnP identifier for a given service, your application calls the [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) method.</span></span> <span data-ttu-id="68e41-117">Diese Methode ruft ein Array von PnP-Bezeichnern für Dienste einer Dienstkategorie-GUID ab (z. B. DIENSTkontakte).</span><span class="sxs-lookup"><span data-stu-id="68e41-117">This method retrieves an array of PnP identifiers for services of a service category GUID (for example SERVICE Contacts).</span></span>

<span data-ttu-id="68e41-118">Die Beispieldienstanwendung ruft einen PnP-Bezeichner für Contacts-Dienste innerhalb der **EnumerateContactsServices-Methode** im ServiceEnumeration.cpp-Modul ab.</span><span class="sxs-lookup"><span data-stu-id="68e41-118">The sample Service application retrieves a PnP identifier for Contacts services within the **EnumerateContactsServices** method in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="68e41-119">Das folgende Codebeispiel stammt aus dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="68e41-119">The following code sample is taken from this method.</span></span>


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



<span data-ttu-id="68e41-120">Nachdem Ihre Anwendung den PnP-Bezeichner für den Dienst abgerufen hat, kann sie die Clientinformationen einrichten und [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="68e41-120">After your application retrieves the PnP identifier for the service, it can set up the client information and call [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span>

<span data-ttu-id="68e41-121">In der Beispielanwendung wird diese Methode in **ChooseDeviceService** im Modul ServiceEnumeration.cpp aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="68e41-121">In the sample application, this method is called within **ChooseDeviceService** in the ServiceEnumeration.cpp module.</span></span>

<span data-ttu-id="68e41-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) unterstützt zwei CLSIDs für **CoCreateInstance.**</span><span class="sxs-lookup"><span data-stu-id="68e41-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="68e41-123">**CLSID \_ PortableDeviceService gibt** einen **IPortableDeviceService-Zeiger** zurück, der den Freethread-Marshaller nicht aggregiert. **CLSID \_ PortableDeviceServiceFTM** ist eine neue CLSID, die einen **IPortableDeviceService-Zeiger** zurückgibt, der den Marshaller mit Freiem Thread aggregiert.</span><span class="sxs-lookup"><span data-stu-id="68e41-123">**CLSID\_PortableDeviceService** returns an **IPortableDeviceService** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceServiceFTM** is a new CLSID that returns an **IPortableDeviceService** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="68e41-124">Andernfalls unterstützen beide Zeiger die gleiche Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="68e41-124">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="68e41-125">Anwendungen, die sich in SingleThreaded Apartment befinden, sollten **CLSID \_ PortableDeviceServiceFTM** verwenden, da dadurch der Aufwand für das Marshalling von Schnittstellenzeigern entfällt.</span><span class="sxs-lookup"><span data-stu-id="68e41-125">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceServiceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="68e41-126">**CLSID \_ PortableDeviceService wird** weiterhin für Legacyanwendungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68e41-126">**CLSID\_PortableDeviceService** is still supported for legacy applications.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="68e41-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68e41-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68e41-128">**IPortableDeviceService-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="68e41-128">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="68e41-129">**IPortableDeviceValues-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="68e41-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="68e41-130">**IPortableDeviceServiceManager-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="68e41-130">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="68e41-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="68e41-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




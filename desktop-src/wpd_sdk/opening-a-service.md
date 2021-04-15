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
# <a name="opening-a-service"></a><span data-ttu-id="48adc-103">Öffnen eines Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="48adc-103">Opening a Service</span></span>

<span data-ttu-id="48adc-104">Bevor die Anwendung Vorgänge für einen Dienst ausführen kann, z. b. das Auflisten von Inhalten oder das Abrufen von Beschreibungen unterstützter Ereignisse oder Methoden, muss der Dienst geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="48adc-104">Before your application can perform operations on a service, for example, enumerating content or retrieving descriptions of supported events or methods, it must open the service.</span></span> <span data-ttu-id="48adc-105">In der Anwendung wpdservicesapisample wird diese Aufgabe im serviceenumeration. cpp-Modul mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="48adc-105">In the WpdServicesApiSample application, this task is demonstrated in the ServiceEnumeration.cpp module using the interfaces described in the following table.</span></span>



|                                                                        |                                                    |
|------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="48adc-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="48adc-106">Interface</span></span>                                                              | <span data-ttu-id="48adc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48adc-107">Description</span></span>                                        |
| [<span data-ttu-id="48adc-108">**Iportablede viceservicemanager**</span><span class="sxs-lookup"><span data-stu-id="48adc-108">**IPortableDeviceServiceManager**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | <span data-ttu-id="48adc-109">Wird verwendet, um die Dienste auf einem Gerät aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="48adc-109">Used to enumerate the services on a device.</span></span>        |
| [<span data-ttu-id="48adc-110">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="48adc-110">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="48adc-111">Wird verwendet, um eine Verbindung mit einem Geräte Dienst zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="48adc-111">Used to open a connection to a device service.</span></span>     |
| [<span data-ttu-id="48adc-112">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="48adc-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="48adc-113">Wird verwendet, um die Client Informationen der Anwendung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="48adc-113">Used to hold the application's client information.</span></span> |



 

<span data-ttu-id="48adc-114">Die Methode, die einen Dienst öffnet, ist [**iportabledeviceservice:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="48adc-114">The method that opens a service is [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span> <span data-ttu-id="48adc-115">Diese Methode nimmt zwei Argumente an: einen PNP-Bezeichner (Plug-and-Play) für den Dienst und ein [**iportabledevicevalues**](iportabledevicevalues.md) -Objekt, das die Client Informationen der Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="48adc-115">This method takes two arguments: a Plug-and-Play (PnP) identifier for the service and an [**IPortableDeviceValues**](iportabledevicevalues.md) object that contains the application's client information.</span></span>

<span data-ttu-id="48adc-116">Um einen PNP-Bezeichner für einen bestimmten Dienst zu erhalten, ruft Ihre Anwendung die [**iportabledeviceservicemanager:: getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="48adc-116">To obtain a PnP identifier for a given service, your application calls the [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) method.</span></span> <span data-ttu-id="48adc-117">Diese Methode ruft ein Array von PNP-Bezeichner für Dienste einer Dienst Kategorie-GUID (z. b. Dienst Kontakte) ab.</span><span class="sxs-lookup"><span data-stu-id="48adc-117">This method retrieves an array of PnP identifiers for services of a service category GUID (for example SERVICE Contacts).</span></span>

<span data-ttu-id="48adc-118">Die Beispiel Dienst Anwendung ruft einen PNP-Bezeichner für Kontakte Dienste innerhalb der **enumeratecontactsservices** -Methode im serviceenumeration. cpp-Modul ab.</span><span class="sxs-lookup"><span data-stu-id="48adc-118">The sample Service application retrieves a PnP identifier for Contacts services within the **EnumerateContactsServices** method in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="48adc-119">Das folgende Codebeispiel stammt aus dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="48adc-119">The following code sample is taken from this method.</span></span>


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



<span data-ttu-id="48adc-120">Nachdem die Anwendung den PNP-Bezeichner für den Dienst abgerufen hat, kann Sie die Client Informationen einrichten und [**iportabledeviceservice:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="48adc-120">After your application retrieves the PnP identifier for the service, it can set up the client information and call [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span>

<span data-ttu-id="48adc-121">In der Beispielanwendung wird diese Methode innerhalb von **choosedeviceservice** im serviceenumeration. cpp-Modul aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="48adc-121">In the sample application, this method is called within **ChooseDeviceService** in the ServiceEnumeration.cpp module.</span></span>

<span data-ttu-id="48adc-122">[**Iportableendviceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) unterstützt zwei CLSIDs für **cokreatabstance**.</span><span class="sxs-lookup"><span data-stu-id="48adc-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="48adc-123">**CLSID \_ Portableendviceservice** gibt einen **iportableendviceservice** -Zeiger zurück, der den Freethread-Mars Haller nicht aggregiert. **CLSID \_ Portableendviceserviceftm** ist eine neue CLSID, die einen **iportableendviceservice** -Zeiger zurückgibt, der den frei Thread-Mars Haller aggregiert.</span><span class="sxs-lookup"><span data-stu-id="48adc-123">**CLSID\_PortableDeviceService** returns an **IPortableDeviceService** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceServiceFTM** is a new CLSID that returns an **IPortableDeviceService** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="48adc-124">Beide Zeiger unterstützen andernfalls dieselbe Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="48adc-124">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="48adc-125">Anwendungen, die in Single Thread-Apartments Leben, sollten **CLSID \_ portabletoviceserviceftm** verwenden, da dadurch der Aufwand für das Marshalling von Schnittstellen Zeigern entfällt.</span><span class="sxs-lookup"><span data-stu-id="48adc-125">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceServiceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="48adc-126">**CLSID \_ Portablede viceservice** wird weiterhin für ältere Anwendungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48adc-126">**CLSID\_PortableDeviceService** is still supported for legacy applications.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="48adc-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48adc-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48adc-128">**Iportablede viceservice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="48adc-128">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="48adc-129">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="48adc-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="48adc-130">**Iportabledebug Service Service Manager-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="48adc-130">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="48adc-131">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="48adc-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




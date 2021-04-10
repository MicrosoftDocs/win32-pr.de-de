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
# <a name="enumerating-service-content"></a><span data-ttu-id="d0c28-103">Auflisten von Dienst Inhalten</span><span class="sxs-lookup"><span data-stu-id="d0c28-103">Enumerating Service Content</span></span>

<span data-ttu-id="d0c28-104">Nachdem die Anwendung einen Dienst geöffnet hat, kann Sie damit beginnen, Dienst bezogene Vorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d0c28-104">After your application opens a service, it can begin performing service-related operations.</span></span> <span data-ttu-id="d0c28-105">Im Fall der Anwendung wpdservicesapisample ist einer dieser Vorgänge die Enumeration von Inhalten für einen bestimmten Kontakt Dienst.</span><span class="sxs-lookup"><span data-stu-id="d0c28-105">In the case of the WpdServicesApiSample application, one of these operations is the enumeration of content for a given Contacts service.</span></span> <span data-ttu-id="d0c28-106">In der folgenden Tabelle werden die verwendeten Schnittstellen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d0c28-106">The following table describes the interfaces used.</span></span>



|                                                                      |                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c28-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d0c28-107">Interface</span></span>                                                            | <span data-ttu-id="d0c28-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0c28-108">Description</span></span>                                                                                      |
| [<span data-ttu-id="d0c28-109">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="d0c28-109">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="d0c28-110">Dient zum Abrufen der IPortableDeviceContent2-Schnittstelle für den Zugriff auf den-Dienst.</span><span class="sxs-lookup"><span data-stu-id="d0c28-110">Used to retrieve the IPortableDeviceContent2 interface to access content on the service.</span></span>         |
| [<span data-ttu-id="d0c28-111">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="d0c28-111">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="d0c28-112">Wird zum Abrufen der ienumportabledeviceobjectids-Schnittstelle verwendet, um Objekte im Dienst aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="d0c28-112">Used to retrieve the IEnumPortableDeviceObjectIDs interface to enumerate objects on the service.</span></span> |
| [<span data-ttu-id="d0c28-113">**Ienumportabledeviceobjectids**</span><span class="sxs-lookup"><span data-stu-id="d0c28-113">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | <span data-ttu-id="d0c28-114">Wird verwendet, um Objekte im Dienst aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="d0c28-114">Used to enumerate objects on the service.</span></span>                                                        |



 

<span data-ttu-id="d0c28-115">Der inhaltsaufzählungs Code befindet sich im Modul "contentenumeration. cpp".</span><span class="sxs-lookup"><span data-stu-id="d0c28-115">The content enumeration code is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="d0c28-116">Dieser Code befindet sich in den **enumerateallcontent** -und **recursiveenumerate** -Methoden.</span><span class="sxs-lookup"><span data-stu-id="d0c28-116">This code resides in the **EnumerateAllContent** and the **RecursiveEnumerate** methods.</span></span> <span data-ttu-id="d0c28-117">Die erste Methode ruft letztere auf.</span><span class="sxs-lookup"><span data-stu-id="d0c28-117">The former method calls the latter.</span></span>

<span data-ttu-id="d0c28-118">Die **enumeratecontent** -Methode nimmt einen Zeiger auf ein [**iportabledeviceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) -Objekt als einen Parameter an.</span><span class="sxs-lookup"><span data-stu-id="d0c28-118">The **EnumerateContent** method takes a pointer to an [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) object as its one parameter.</span></span> <span data-ttu-id="d0c28-119">Dieses Objekt entspricht einem Dienst, den die Anwendung zuvor geöffnet hat, als die [**iportabledeviceservice:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d0c28-119">This object corresponds to a service that the application opened earlier when it called the [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) method.</span></span>

<span data-ttu-id="d0c28-120">Die **enumeratecontent** -Methode erstellt ein [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) -Objekt und übergibt dieses Objekt an die [**iportabledeviceservice:: Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d0c28-120">The **EnumerateContent** method creates an [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) object and passes this object to the [**IPortableDeviceService::Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) method.</span></span> <span data-ttu-id="d0c28-121">Diese Methode ruft wiederum den Inhalt auf der Stamm Ebene des diensdienstanzen ab und beginnt dann rekursiv mit dem Abrufen von Inhalt, der unterhalb des Stamms gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="d0c28-121">This method, in turn, retrieves the content at the root level of the service, and then recursively begins to retrieve content found beneath the root.</span></span>

<span data-ttu-id="d0c28-122">Der folgende Code entspricht der **enumeratecontent** -Methode.</span><span class="sxs-lookup"><span data-stu-id="d0c28-122">The following code corresponds to the **EnumerateContent** method.</span></span>


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



<span data-ttu-id="d0c28-123">Der folgende Code entspricht der **recursiveenumerate** -Methode.</span><span class="sxs-lookup"><span data-stu-id="d0c28-123">The following code corresponds to the **RecursiveEnumerate** method.</span></span> <span data-ttu-id="d0c28-124">Die recursiveenumerate-Methode instanziiert eine **ienumportabledeviceobjectids** -Schnittstelle für das angegebene übergeordnete Objekt und ruft **ienumportabledeviceobjectids:: Next** auf, wobei ein Batch der unmittelbaren untergeordneten Objekte abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d0c28-124">The RecursiveEnumerate method instantiates an **IEnumPortableDeviceObjectIDs** interface for the supplied parent object, and calls **IEnumPortableDeviceObjectIDs::Next**, retrieving a batch of immediate child objects.</span></span> <span data-ttu-id="d0c28-125">Für jedes untergeordnete Objekt wird rekursiveenumerate erneut aufgerufen, um seine untergeordneten Objekte zurückzugeben, usw.</span><span class="sxs-lookup"><span data-stu-id="d0c28-125">For each child object, RecursiveEnumerate is called again to return its descendent child objects, and so on.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d0c28-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0c28-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0c28-127">**Ienumportabledeviceobjectids**</span><span class="sxs-lookup"><span data-stu-id="d0c28-127">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="d0c28-128">**IPortableDeviceContent2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d0c28-128">**IPortableDeviceContent2 Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="d0c28-129">**Iportablede viceservice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d0c28-129">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="d0c28-130">Öffnen eines Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d0c28-130">Opening a Service</span></span>](opening-a-service.md)
</dt> <dt>

[<span data-ttu-id="d0c28-131">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="d0c28-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




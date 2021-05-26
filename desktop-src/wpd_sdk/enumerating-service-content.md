---
description: Aufzählen von Dienstinhalten
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Aufzählen von Dienstinhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b701bdab867e96bc9658e2624ea18aa65dfc33
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424250"
---
# <a name="enumerating-service-content"></a><span data-ttu-id="fe089-103">Aufzählen von Dienstinhalten</span><span class="sxs-lookup"><span data-stu-id="fe089-103">Enumerating Service Content</span></span>

<span data-ttu-id="fe089-104">Nachdem Ihre Anwendung einen Dienst geöffnet hat, kann sie mit dem Ausführen dienstbezogener Vorgänge beginnen.</span><span class="sxs-lookup"><span data-stu-id="fe089-104">After your application opens a service, it can begin performing service-related operations.</span></span> <span data-ttu-id="fe089-105">Im Fall der WpdServicesApiSample-Anwendung ist einer dieser Vorgänge die Enumeration des Inhalts für einen bestimmten Contacts-Dienst.</span><span class="sxs-lookup"><span data-stu-id="fe089-105">In the case of the WpdServicesApiSample application, one of these operations is the enumeration of content for a given Contacts service.</span></span> <span data-ttu-id="fe089-106">In der folgenden Tabelle werden die verwendeten Schnittstellen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fe089-106">The following table describes the interfaces used.</span></span>



| <span data-ttu-id="fe089-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fe089-107">Interface</span></span>                                                            | <span data-ttu-id="fe089-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe089-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe089-109">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="fe089-109">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="fe089-110">Wird verwendet, um die IPortableDeviceContent2-Schnittstelle abzurufen, um auf Inhalte im Dienst zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="fe089-110">Used to retrieve the IPortableDeviceContent2 interface to access content on the service.</span></span>         |
| [<span data-ttu-id="fe089-111">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="fe089-111">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="fe089-112">Wird verwendet, um die IEnumPortableDeviceObjectIDs-Schnittstelle abzurufen, um Objekte für den Dienst aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="fe089-112">Used to retrieve the IEnumPortableDeviceObjectIDs interface to enumerate objects on the service.</span></span> |
| [<span data-ttu-id="fe089-113">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="fe089-113">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | <span data-ttu-id="fe089-114">Wird verwendet, um Objekte für den Dienst aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="fe089-114">Used to enumerate objects on the service.</span></span>                                                        |



 

<span data-ttu-id="fe089-115">Der Inhaltsenumerationscode befindet sich im ContentEnumeration.cpp-Modul.</span><span class="sxs-lookup"><span data-stu-id="fe089-115">The content enumeration code is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="fe089-116">Dieser Code befindet sich in den Methoden **EnumerateAllContent** und **RecursiveEnumerate.**</span><span class="sxs-lookup"><span data-stu-id="fe089-116">This code resides in the **EnumerateAllContent** and the **RecursiveEnumerate** methods.</span></span> <span data-ttu-id="fe089-117">Die frühere Methode ruft letztere auf.</span><span class="sxs-lookup"><span data-stu-id="fe089-117">The former method calls the latter.</span></span>

<span data-ttu-id="fe089-118">Die **EnumerateContent-Methode** verwendet einen Zeiger auf ein [**IPortableDeviceService-Objekt**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) als einen Parameter.</span><span class="sxs-lookup"><span data-stu-id="fe089-118">The **EnumerateContent** method takes a pointer to an [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) object as its one parameter.</span></span> <span data-ttu-id="fe089-119">Dieses Objekt entspricht einem Dienst, den die Anwendung zuvor beim Aufruf der [**IPortableDeviceService::Open-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="fe089-119">This object corresponds to a service that the application opened earlier when it called the [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) method.</span></span>

<span data-ttu-id="fe089-120">Die **EnumerateContent-Methode** erstellt ein [**IPortableDeviceContent2-Objekt**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) und übergibt dieses Objekt an die [**IPortableDeviceService::Content-Methode.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content)</span><span class="sxs-lookup"><span data-stu-id="fe089-120">The **EnumerateContent** method creates an [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) object and passes this object to the [**IPortableDeviceService::Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) method.</span></span> <span data-ttu-id="fe089-121">Diese Methode ruft wiederum den Inhalt auf der Stammebene des Diensts ab und beginnt dann rekursiv mit dem Abrufen von Inhalten, die unterhalb des Stamms gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="fe089-121">This method, in turn, retrieves the content at the root level of the service, and then recursively begins to retrieve content found beneath the root.</span></span>

<span data-ttu-id="fe089-122">Der folgende Code entspricht der **EnumerateContent-Methode.**</span><span class="sxs-lookup"><span data-stu-id="fe089-122">The following code corresponds to the **EnumerateContent** method.</span></span>


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



<span data-ttu-id="fe089-123">Der folgende Code entspricht der **RecursiveEnumerate-Methode.**</span><span class="sxs-lookup"><span data-stu-id="fe089-123">The following code corresponds to the **RecursiveEnumerate** method.</span></span> <span data-ttu-id="fe089-124">Die RecursiveEnumerate-Methode instanziiert eine **IEnumPortableDeviceObjectIDs-Schnittstelle** für das angegebene übergeordnete Objekt und ruft **IEnumPortableDeviceObjectIDs::Next** auf und ruft einen Batch von unmittelbar untergeordneten Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="fe089-124">The RecursiveEnumerate method instantiates an **IEnumPortableDeviceObjectIDs** interface for the supplied parent object, and calls **IEnumPortableDeviceObjectIDs::Next**, retrieving a batch of immediate child objects.</span></span> <span data-ttu-id="fe089-125">Für jedes untergeordnete Objekt wird RecursiveEnumerate erneut aufgerufen, um seine untergeordneten untergeordneten Objekte zurück zu geben, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="fe089-125">For each child object, RecursiveEnumerate is called again to return its descendent child objects, and so on.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fe089-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe089-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe089-127">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="fe089-127">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="fe089-128">**IPortableDeviceContent2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fe089-128">**IPortableDeviceContent2 Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="fe089-129">**IPortableDeviceService-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fe089-129">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="fe089-130">Öffnen eines Diensts</span><span class="sxs-lookup"><span data-stu-id="fe089-130">Opening a Service</span></span>](opening-a-service.md)
</dt> <dt>

[<span data-ttu-id="fe089-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="fe089-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




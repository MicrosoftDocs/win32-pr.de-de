---
description: Abrufen unterstützter Dienstformate
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Abrufen unterstützter Dienstformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73618f3450255ad470545ac472ad9f71238621e3
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423811"
---
# <a name="retrieving-supported-service-formats"></a><span data-ttu-id="82929-103">Abrufen unterstützter Dienstformate</span><span class="sxs-lookup"><span data-stu-id="82929-103">Retrieving Supported Service Formats</span></span>

<span data-ttu-id="82929-104">Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Contacts-Dienst unterstützten Formate abrufen kann, indem methoden der Schnittstellen in der folgenden Tabelle aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="82929-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the formats supported by a given Contacts service by calling methods of the interfaces in the following table.</span></span>



| <span data-ttu-id="82929-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="82929-105">Interface</span></span> | <span data-ttu-id="82929-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82929-106">Description</span></span>   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82929-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="82929-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="82929-108">Wird zum Abrufen der **IPortableDeviceServiceCapabilities-Schnittstelle** für den Zugriff auf die unterstützten Ereignisse verwendet.</span><span class="sxs-lookup"><span data-stu-id="82929-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="82929-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="82929-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="82929-110">Ermöglicht den Zugriff auf die unterstützten Ereignisse und Ereignisattribute.</span><span class="sxs-lookup"><span data-stu-id="82929-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="82929-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="82929-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="82929-112">Enthält die Liste der unterstützten Formate.</span><span class="sxs-lookup"><span data-stu-id="82929-112">Contains the list of supported formats.</span></span>                                                               |
| [<span data-ttu-id="82929-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="82929-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="82929-114">Enthält die Attribute für ein bestimmtes Format.</span><span class="sxs-lookup"><span data-stu-id="82929-114">Contains the attributes for a given format.</span></span>                                                           |



 

<span data-ttu-id="82929-115">Wenn der Benutzer die Option "3" in der Befehlszeile auswählt, ruft die Anwendung die **ListSupportedFormats-Methode** auf, die sich im Modul ServiceCapabilities.cpp befindet.</span><span class="sxs-lookup"><span data-stu-id="82929-115">When the user chooses option "3" at the command line, the application invokes the **ListSupportedFormats** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="82929-116">Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontaktdienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="82929-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="82929-117">In WPD wird ein Format durch Attribute beschrieben, die den Namen und (optional) den MIME-Typ eines bestimmten Formats angeben.</span><span class="sxs-lookup"><span data-stu-id="82929-117">In WPD, a format is described by attributes that specify the name and (optionally) the MIME type of a given format.</span></span> <span data-ttu-id="82929-118">Diese Attribute werden in der HeaderdateiPortableDevice.h definiert.</span><span class="sxs-lookup"><span data-stu-id="82929-118">These attributes are defined in thePortableDevice.h header file.</span></span> <span data-ttu-id="82929-119">Eine Beschreibung der unterstützten Attribute finden Sie im Thema [Attribute.](attributes.md)</span><span class="sxs-lookup"><span data-stu-id="82929-119">For a description of supported attributes, refer to the [Attributes](attributes.md) topic.</span></span>

<span data-ttu-id="82929-120">Wenn wpdServiceSampleDriver das einzige installierte Gerät ist, gibt der Treiber im Fall der Beispielanwendung zwei unterstützte Formate für den Contact-Dienst zurück: "AbstractContactFormat" und "VCard2Format".</span><span class="sxs-lookup"><span data-stu-id="82929-120">In the case of the sample application, if the WpdServiceSampleDriver is the only installed device, the driver returns two supported formats for its Contact service: "AbstractContactFormat" and "VCard2Format".</span></span> <span data-ttu-id="82929-121">Diese Formate entsprechen den **WPD \_ OBJECT FORMAT \_ ABSTRACT \_ \_ CONTACT-** und **WPD OBJECT FORMAT \_ \_ \_ VCARD2-Attributen** in PortableDevice.h.</span><span class="sxs-lookup"><span data-stu-id="82929-121">These formats correspond to the **WPD\_OBJECT\_FORMAT\_ABSTRACT\_CONTACT** and the **WPD\_OBJECT\_FORMAT\_VCARD2** attributes found in PortableDevice.h.</span></span>

<span data-ttu-id="82929-122">Zwei Methoden im Modul ServiceCapabilities.cpp unterstützen das Abrufen unterstützter Formate für den Contacts-Dienst: **ListSupportedFormats** und **DisplayFormat**.</span><span class="sxs-lookup"><span data-stu-id="82929-122">Two methods in the ServiceCapabilities.cpp module support the retrieval of supported formats for the Contacts service: **ListSupportedFormats** and **DisplayFormat**.</span></span> <span data-ttu-id="82929-123">Erstere ruft den GUID-Bezeichner für jedes unterstützte Format ab.</span><span class="sxs-lookup"><span data-stu-id="82929-123">The former retrieves the GUID identifier for each supported format.</span></span> <span data-ttu-id="82929-124">Letztere konvertiert diese GUID in eine benutzerfreundliche Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="82929-124">The latter converts this GUID into a user-friendly string.</span></span>

<span data-ttu-id="82929-125">Die **ListSupportedFormats-Methode** ruft die [**IPortableDeviceService::Capabilities-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**IPortableDeviceServiceCapabilities-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="82929-125">The **ListSupportedFormats** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="82929-126">Mit dieser Schnittstelle werden die unterstützten Formate abgerufen, indem die [**IPortableDeviceServiceCapabilities::GetSupportedFormats-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="82929-126">Using this interface, it retrieves the supported formats by calling the [**IPortableDeviceServiceCapabilities::GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) method.</span></span> <span data-ttu-id="82929-127">Die **GetSupportedFormats-Methode** ruft die GUID für jedes vom Dienst unterstützte Format ab und kopiert diese GUID in ein [**IPortableDevicePropVariantCollection-Objekt.**](iportabledevicepropvariantcollection.md)</span><span class="sxs-lookup"><span data-stu-id="82929-127">The **GetSupportedFormats** method retrieves the GUID for each format supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="82929-128">Im folgenden Code wird die **ListSupportedFormats-Methode** verwendet.</span><span class="sxs-lookup"><span data-stu-id="82929-128">The following code uses the **ListSupportedFormats** method.</span></span>


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="82929-129">Nachdem die **ListSupportedFormats-Methode** die GUID für jedes vom angegebenen Dienst unterstützte Format abgerufen hat, ruft sie die **DisplayFormat-Methode** auf, um den Anzeigenamen des Skripts für jedes Format anzuzeigen. Beispiel: "VCard2".</span><span class="sxs-lookup"><span data-stu-id="82929-129">After the **ListSupportedFormats** method retrieves the GUID for each format supported by the given service, it invokes the **DisplayFormat** method to display the script friendly name for each format; for example, "VCard2".</span></span>

<span data-ttu-id="82929-130">Die **DisplayFormat-Methode** ruft die [**IPortableDeviceServiceCapabilities::GetFormatAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) auf, um eine Auflistung von Attributen für die angegebene Format-GUID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="82929-130">The **DisplayFormat** method invokes the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method retrieve a collection of attributes for the given format GUID.</span></span> <span data-ttu-id="82929-131">Anschließend ruft sie die [**IPortableDeviceValues::GetStringValue-Methode**](iportabledevicevalues-getstringvalue.md) auf und fordert an, dass der Treiber einen skriptfreundlichen Namen für das angegebene Format zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="82929-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a script-friendly name for the given format.</span></span>

<span data-ttu-id="82929-132">Im folgenden Code wird die **DisplayFormat-Methode** verwendet.</span><span class="sxs-lookup"><span data-stu-id="82929-132">The following code uses the **DisplayFormat** method.</span></span>


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="82929-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82929-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82929-134">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="82929-134">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="82929-135">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="82929-135">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="82929-136">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="82929-136">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="82929-137">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="82929-137">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




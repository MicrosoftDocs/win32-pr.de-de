---
description: Abrufen unterstützter Dienst Formate
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Abrufen unterstützter Dienst Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed8021d8feefaaad3da7905e17e8c658dfb19e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362898"
---
# <a name="retrieving-supported-service-formats"></a><span data-ttu-id="dcaa3-103">Abrufen unterstützter Dienst Formate</span><span class="sxs-lookup"><span data-stu-id="dcaa3-103">Retrieving Supported Service Formats</span></span>

<span data-ttu-id="dcaa3-104">Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung die Formate abrufen kann, die von einem bestimmten Kontakt Dienst unterstützt werden, indem Methoden der Schnittstellen in der folgenden Tabelle aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the formats supported by a given Contacts service by calling methods of the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcaa3-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dcaa3-105">Interface</span></span>                                                                            | <span data-ttu-id="dcaa3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcaa3-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="dcaa3-107">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="dcaa3-108">Wird zum Abrufen der **iportabledeviceservicecapabili-** Schnittstelle verwendet, um auf die unterstützten Ereignisse zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="dcaa3-109">**Iportablede viceservicecapabili**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="dcaa3-110">Bietet Zugriff auf die unterstützten Ereignisse und Ereignis Attribute.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="dcaa3-111">**Iportabledevicepropvariantcollection**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="dcaa3-112">Enthält die Liste der unterstützten Formate.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-112">Contains the list of supported formats.</span></span>                                                               |
| [<span data-ttu-id="dcaa3-113">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="dcaa3-114">Enthält die Attribute für ein bestimmtes Format.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-114">Contains the attributes for a given format.</span></span>                                                           |



 

<span data-ttu-id="dcaa3-115">Wenn der Benutzer die Option "3" in der Befehlszeile auswählt, ruft die Anwendung die **listsupportedformats** -Methode auf, die im Modul "servicecapabili. cpp" zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-115">When the user chooses option "3" at the command line, the application invokes the **ListSupportedFormats** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="dcaa3-116">Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontakt Dienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="dcaa3-117">In WPD wird ein Format von Attributen beschrieben, die den Namen und (optional) den MIME-Typ eines gegebenen Formats angeben.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-117">In WPD, a format is described by attributes that specify the name and (optionally) the MIME type of a given format.</span></span> <span data-ttu-id="dcaa3-118">Diese Attribute werden in der Header Datei "portabledevice. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-118">These attributes are defined in thePortableDevice.h header file.</span></span> <span data-ttu-id="dcaa3-119">Eine Beschreibung der unterstützten Attribute finden Sie im Thema [Attribute](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="dcaa3-119">For a description of supported attributes, refer to the [Attributes](attributes.md) topic.</span></span>

<span data-ttu-id="dcaa3-120">Bei der Beispielanwendung gibt der Treiber, wenn wpdservicesampledriver das einzige installierte Gerät ist, zwei unterstützte Formate für den Kontakt Dienst an: "abstractcontactformat" und "VCard2Format".</span><span class="sxs-lookup"><span data-stu-id="dcaa3-120">In the case of the sample application, if the WpdServiceSampleDriver is the only installed device, the driver returns two supported formats for its Contact service: "AbstractContactFormat" and "VCard2Format".</span></span> <span data-ttu-id="dcaa3-121">Diese Formate entsprechen dem **\_ \_ \_ abstrakten \_ Kontakt im WPD-Objekt Format** und dem **WPD- \_ Objekt \_ Format \_ VCARD2** Attribute in "portabledevice. h".</span><span class="sxs-lookup"><span data-stu-id="dcaa3-121">These formats correspond to the **WPD\_OBJECT\_FORMAT\_ABSTRACT\_CONTACT** and the **WPD\_OBJECT\_FORMAT\_VCARD2** attributes found in PortableDevice.h.</span></span>

<span data-ttu-id="dcaa3-122">Zwei Methoden im servicecapabili. cpp-Modul unterstützen den Abruf unterstützter Formate für den Contacts-Dienst: **listsupportedformats** und **Display Format**.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-122">Two methods in the ServiceCapabilities.cpp module support the retrieval of supported formats for the Contacts service: **ListSupportedFormats** and **DisplayFormat**.</span></span> <span data-ttu-id="dcaa3-123">Der erste Ruft den GUID-Bezeichner für jedes unterstützte Format ab.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-123">The former retrieves the GUID identifier for each supported format.</span></span> <span data-ttu-id="dcaa3-124">Letztere konvertiert diese GUID in eine benutzerfreundliche Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-124">The latter converts this GUID into a user-friendly string.</span></span>

<span data-ttu-id="dcaa3-125">Die **listsupportedformats** -Methode ruft die [**iportabledeviceservice:: Funktionen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) -Methode auf, um eine [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-125">The **ListSupportedFormats** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="dcaa3-126">Mithilfe dieser Schnittstelle werden die unterstützten Formate durch Aufrufen der [**iportabledeviceservicecapabili:: GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-126">Using this interface, it retrieves the supported formats by calling the [**IPortableDeviceServiceCapabilities::GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) method.</span></span> <span data-ttu-id="dcaa3-127">Die **GetSupportedFormats** -Methode ruft die GUID für jedes Format ab, das vom Dienst unterstützt wird, und kopiert diese GUID in ein [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-127">The **GetSupportedFormats** method retrieves the GUID for each format supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="dcaa3-128">Im folgenden Code wird die **listsupportedformats** -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-128">The following code uses the **ListSupportedFormats** method.</span></span>


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



<span data-ttu-id="dcaa3-129">Nachdem die **listsupportedformats** -Methode die GUID für jedes vom angegebenen Dienst unterstützte Format abgerufen hat, ruft Sie die **DisplayFormat** -Methode auf, um den anzeigen amen des Skripts für die einzelnen Formate anzuzeigen. Beispiel: "VCard2".</span><span class="sxs-lookup"><span data-stu-id="dcaa3-129">After the **ListSupportedFormats** method retrieves the GUID for each format supported by the given service, it invokes the **DisplayFormat** method to display the script friendly name for each format; for example, "VCard2".</span></span>

<span data-ttu-id="dcaa3-130">Die **DisplayFormat** -Methode ruft die [**iportabledeviceservicecapabili:: getformattribute**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) -Methode auf, um eine Auflistung von Attributen für die angegebene Format-GUID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-130">The **DisplayFormat** method invokes the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method retrieve a collection of attributes for the given format GUID.</span></span> <span data-ttu-id="dcaa3-131">Anschließend wird die [**iportabledevicevalues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) -Methode aufgerufen, und es wird angefordert, dass der Treiber einen Skript freundlichen Namen für das angegebene Format zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a script-friendly name for the given format.</span></span>

<span data-ttu-id="dcaa3-132">Im folgenden Code wird die **DisplayFormat** -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-132">The following code uses the **DisplayFormat** method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="dcaa3-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dcaa3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcaa3-134">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-134">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="dcaa3-135">**Iportablede viceservicecapabili**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-135">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="dcaa3-136">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-136">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="dcaa3-137">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="dcaa3-137">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




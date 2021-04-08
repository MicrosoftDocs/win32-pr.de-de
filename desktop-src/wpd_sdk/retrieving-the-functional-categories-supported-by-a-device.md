---
description: Abrufen der von einem Gerät unterstützten funktionalen Kategorien
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Abrufen der von einem Gerät unterstützten funktionalen Kategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866743"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a><span data-ttu-id="423c4-103">Abrufen der von einem Gerät unterstützten funktionalen Kategorien</span><span class="sxs-lookup"><span data-stu-id="423c4-103">Retrieving the Functional Categories Supported by a Device</span></span>

<span data-ttu-id="423c4-104">Tragbare Windows-Geräte unterstützen möglicherweise mindestens eine Funktions Kategorie.</span><span class="sxs-lookup"><span data-stu-id="423c4-104">Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="423c4-105">Diese Kategorien werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="423c4-105">These categories are described in the following table.</span></span>



| <span data-ttu-id="423c4-106">Category</span><span class="sxs-lookup"><span data-stu-id="423c4-106">Category</span></span>                    | <span data-ttu-id="423c4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="423c4-107">Description</span></span>                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="423c4-108">Audioerfassung</span><span class="sxs-lookup"><span data-stu-id="423c4-108">Audio capture</span></span>               | <span data-ttu-id="423c4-109">Das Gerät kann verwendet werden, um Audiodaten aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="423c4-109">The device can be used to record audio.</span></span>                                              |
| <span data-ttu-id="423c4-110">Renderinginformationen</span><span class="sxs-lookup"><span data-stu-id="423c4-110">Rendering information</span></span>       | <span data-ttu-id="423c4-111">Das Gerät stellt Daten bereit, die die Mediendateien beschreiben, die Sie Rendern können.</span><span class="sxs-lookup"><span data-stu-id="423c4-111">The device provides data describing the media files that it is capable of rendering.</span></span> |
| <span data-ttu-id="423c4-112">SMS (Short Message Service)</span><span class="sxs-lookup"><span data-stu-id="423c4-112">Short message service (SMS)</span></span> | <span data-ttu-id="423c4-113">Das Gerät unterstützt Textnachrichten.</span><span class="sxs-lookup"><span data-stu-id="423c4-113">The device supports text messaging.</span></span>                                                  |
| <span data-ttu-id="423c4-114">Trotzdem Image Erfassung</span><span class="sxs-lookup"><span data-stu-id="423c4-114">Still image capture</span></span>         | <span data-ttu-id="423c4-115">Das Gerät kann zum Erfassen von Images verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="423c4-115">The device can be used to capture still images.</span></span>                                      |
| <span data-ttu-id="423c4-116">Storage</span><span class="sxs-lookup"><span data-stu-id="423c4-116">Storage</span></span>                     | <span data-ttu-id="423c4-117">Das Gerät kann zum Speichern von Dateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="423c4-117">The device can be used to store files.</span></span>                                               |



 

<span data-ttu-id="423c4-118">Die listfunctionalcategories-Funktion im Modul devicecapabili. cpp veranschaulicht das Abrufen von funktionalen Kategorien für ein ausgewähltes Gerät.</span><span class="sxs-lookup"><span data-stu-id="423c4-118">The ListFunctionalCategories function in the DeviceCapabilities.cpp module demonstrates the retrieval of functional categories for a selected device.</span></span>

<span data-ttu-id="423c4-119">Die Anwendung kann die von einem Gerät unterstützten funktionalen Kategorien mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="423c4-119">Your application can retrieve the functional categories supported by a device by using the interfaces described in the following table.</span></span>



| <span data-ttu-id="423c4-120">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="423c4-120">Interface</span></span>                                                                                      | <span data-ttu-id="423c4-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="423c4-121">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="423c4-122">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="423c4-122">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="423c4-123">Bietet Zugriff auf die Methoden zum Abrufen von funktionalen Kategorien.</span><span class="sxs-lookup"><span data-stu-id="423c4-123">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="423c4-124">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="423c4-124">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="423c4-125">Wird zum Auflisten und Speichern von funktionalen Kategorieinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="423c4-125">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="423c4-126">Die erste Aufgabe, die von der Beispielanwendung durchgeführt wird, ist das Abrufen eines [**iportabledevicecapabili-**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) Objekts, das verwendet wird, um die funktionalen Kategorien auf dem ausgewählten Gerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="423c4-126">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the functional categories on the selected device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}

// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get all functional categories supported by the device.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="423c4-127">Die abgerufenen Kategorien werden in einem [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="423c4-127">The retrieved categories are stored in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="423c4-128">Der nächste Schritt besteht aus der Enumeration und der Anzeige der unterstützten Kategorien.</span><span class="sxs-lookup"><span data-stu-id="423c4-128">The next step is the enumeration and display of the supported categories.</span></span> <span data-ttu-id="423c4-129">Der erste Schritt, den die Beispielanwendung erreicht, ist das Abrufen der Anzahl unterstützter Kategorien.</span><span class="sxs-lookup"><span data-stu-id="423c4-129">The first step that the sample application accomplishes is to retrieve the count of supported categories.</span></span> <span data-ttu-id="423c4-130">Diese Anzahl wird dann verwendet, um das [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt zu durchlaufen, das die unterstützten Kategorien enthält.</span><span class="sxs-lookup"><span data-stu-id="423c4-130">It then uses this count to iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that contains the supported categories.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="423c4-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="423c4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="423c4-132">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="423c4-132">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="423c4-133">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="423c4-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="423c4-134">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="423c4-134">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="423c4-135">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="423c4-135">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




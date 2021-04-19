---
description: Abrufen der von einem Gerät unterstützten Inhaltstypen
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Abrufen der von einem Gerät unterstützten Inhaltstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362838"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a><span data-ttu-id="7ada9-103">Abrufen der von einem Gerät unterstützten Inhaltstypen</span><span class="sxs-lookup"><span data-stu-id="7ada9-103">Retrieving the Content Types Supported by a Device</span></span>

<span data-ttu-id="7ada9-104">Wie bereits im Thema [Abrufen der von einem Gerät unterstützten funktionalen Kategorien](retrieving-the-functional-categories-supported-by-a-device.md) beschrieben, unterstützen tragbare Windows-Geräte möglicherweise mindestens eine Funktions Kategorie.</span><span class="sxs-lookup"><span data-stu-id="7ada9-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="7ada9-105">Eine bestimmte funktionale Kategorie unterstützt möglicherweise einen oder mehrere Inhaltstypen.</span><span class="sxs-lookup"><span data-stu-id="7ada9-105">Any given functional category may support one or more content types.</span></span> <span data-ttu-id="7ada9-106">Beispielsweise kann die Speicher Kategorie Inhaltstypen von Ordner, Audiodaten und Image unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7ada9-106">For example, the storage category may support content types of folder, audio, and image.</span></span>

<span data-ttu-id="7ada9-107">Eine Beschreibung der von WPD unterstützten Inhaltstypen finden Sie im Thema [**WPD \_ - \_ Inhaltstyp \_ alle**](wpd-content-type-all.md) .</span><span class="sxs-lookup"><span data-stu-id="7ada9-107">For a description of the content types supported by WPD, see the [**WPD\_CONTENT\_TYPE\_ALL**](wpd-content-type-all.md) topic.</span></span>

<span data-ttu-id="7ada9-108">Die listsupportedcontenttypes-Funktion im Modul devicecapabili. cpp veranschaulicht das Abrufen von Inhaltstypen für die funktionalen Kategorien, die von einem ausgewählten Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7ada9-108">The ListSupportedContentTypes function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="7ada9-109">Die Anwendung kann die von einem Gerät unterstützten funktionalen Kategorien mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="7ada9-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="7ada9-110">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7ada9-110">Interface</span></span>                                                                                      | <span data-ttu-id="7ada9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ada9-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="7ada9-112">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7ada9-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="7ada9-113">Bietet Zugriff auf die Methoden zum Abrufen von funktionalen Kategorien.</span><span class="sxs-lookup"><span data-stu-id="7ada9-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="7ada9-114">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7ada9-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="7ada9-115">Wird zum Auflisten und Speichern von funktionalen Kategorieinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ada9-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="7ada9-116">Der in der listsupportedcontenttypes-Funktion gefundene Code ist nahezu identisch mit dem Code, der in der listfunctionalcategories-Funktion gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7ada9-116">The code found in the ListSupportedContentTypes function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="7ada9-117">(Weitere Informationen finden Sie im Thema [Abrufen von funktionalen Kategorien, die von einem Gerät unterstützt werden](retrieving-the-functional-categories-supported-by-a-device.md) . Der einzige Unterschied besteht im Aufrufen der [**iportabledevicecapabili:: getsupportedcontenttypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) -Methode, die in der Schleife angezeigt wird, die die funktionalen Kategorien durchläuft.</span><span class="sxs-lookup"><span data-stu-id="7ada9-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) method, which appears within the loop that iterates through the functional categories.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

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
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
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

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="7ada9-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ada9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ada9-119">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7ada9-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="7ada9-120">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7ada9-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="7ada9-121">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7ada9-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="7ada9-122">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="7ada9-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




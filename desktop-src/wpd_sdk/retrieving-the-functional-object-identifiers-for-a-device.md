---
description: Abrufen der funktionalen Objekt Bezeichner für ein Gerät
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Abrufen der funktionalen Objekt Bezeichner für ein Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350322"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a><span data-ttu-id="06c42-103">Abrufen der funktionalen Objekt Bezeichner für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="06c42-103">Retrieving the Functional Object Identifiers for a Device</span></span>

<span data-ttu-id="06c42-104">Wie bereits im Thema [Abrufen der von einem Gerät unterstützten funktionalen Kategorien](retrieving-the-functional-categories-supported-by-a-device.md) beschrieben, unterstützen tragbare Windows-Geräte möglicherweise mindestens eine Funktions Kategorie.</span><span class="sxs-lookup"><span data-stu-id="06c42-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="06c42-105">Eine bestimmte funktionale Kategorie unterstützt möglicherweise ein oder mehrere funktionale Objekte.</span><span class="sxs-lookup"><span data-stu-id="06c42-105">Any given functional category may support one or more functional objects.</span></span> <span data-ttu-id="06c42-106">Beispielsweise kann die Speicher Kategorie drei funktionale Speicher Objekte unterstützen, die jeweils durch eine eindeutige Bezeichnerzeichenfolge identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="06c42-106">For example, the storage category may support three functional storage objects, each of which is identified by a unique identifier string.</span></span> <span data-ttu-id="06c42-107">Das erste Speicher Objekt kann dann durch die Zeichenfolge "Storage1", die zweite durch die Zeichenfolge "Storage2" und das dritte durch die Zeichenfolge "Storage3" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="06c42-107">The first storage object may then be identified by the string "Storage1", the second by the string "Storage2", and the third by the string "Storage3".</span></span>

<span data-ttu-id="06c42-108">Die listfunctionalobjects-Funktion im Modul devicecapabili. cpp veranschaulicht das Abrufen von Inhaltstypen für die Funktions Kategorien, die von einem ausgewählten Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="06c42-108">The ListFunctionalObjects function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="06c42-109">Die Anwendung kann die von einem Gerät unterstützten funktionalen Kategorien mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="06c42-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="06c42-110">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="06c42-110">Interface</span></span>                                                                                      | <span data-ttu-id="06c42-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06c42-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="06c42-112">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="06c42-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="06c42-113">Bietet Zugriff auf die Methoden zum Abrufen von funktionalen Kategorien.</span><span class="sxs-lookup"><span data-stu-id="06c42-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="06c42-114">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="06c42-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="06c42-115">Wird zum Auflisten und Speichern von funktionalen Kategorieinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="06c42-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="06c42-116">Der in der listfunctionalobjects-Funktion gefundene Code ist nahezu identisch mit dem Code in der listfunctionalcategories-Funktion.</span><span class="sxs-lookup"><span data-stu-id="06c42-116">The code found in the ListFunctionalObjects function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="06c42-117">(Weitere Informationen finden Sie im Thema [Abrufen von funktionalen Kategorien, die von einem Gerät unterstützt werden](retrieving-the-functional-categories-supported-by-a-device.md) . Der einzige Unterschied besteht im Aufrufen der [**iportabledevicecapabili:: getfunctionalobjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) -Methode, die in der Schleife angezeigt wird, die die funktionalen Kategorien durchläuft.</span><span class="sxs-lookup"><span data-stu-id="06c42-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method, which appears within the loop that iterates through the functional categories.</span></span>


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

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
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



## <a name="related-topics"></a><span data-ttu-id="06c42-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06c42-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06c42-119">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="06c42-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="06c42-120">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="06c42-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="06c42-121">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="06c42-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="06c42-122">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="06c42-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




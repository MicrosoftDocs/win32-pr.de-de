---
description: Auflisten von Inhalten
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Auflisten von Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347150"
---
# <a name="enumerating-content"></a><span data-ttu-id="81c60-103">Auflisten von Inhalten</span><span class="sxs-lookup"><span data-stu-id="81c60-103">Enumerating Content</span></span>

<span data-ttu-id="81c60-104">Der Inhalt eines Geräts (unabhängig davon, ob es sich um einen Ordner, ein Telefonbuch, ein Video oder ein Image handelt) wird in der WPD-API als Objekt bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="81c60-104">The content on a device (whether that content is a folder, a phone book, a video, or a still image) is called an object in the WPD API.</span></span> <span data-ttu-id="81c60-105">Auf diese Objekte wird von Objekt bezeichmern verwiesen, die von-Eigenschaften beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="81c60-105">These objects are referenced by object identifiers and described by properties.</span></span> <span data-ttu-id="81c60-106">Sie können die Objekte auf einem Gerät auflisten, indem Sie Methoden in der [**iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), der [**iportabledevicecontent-Schnitt**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)Stelle und der [**ienumportabledeviceobjectids**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)-Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="81c60-106">You can enumerate the objects on a device by calling methods in the [**IPortableDevice interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), the [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent), and the [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span>

<span data-ttu-id="81c60-107">Die Beispielanwendung veranschaulicht die inhaltsenumeration in der enumerateallcontent-Funktion, die im Modul "contentenumeration. cpp" zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="81c60-107">The sample application demonstrates content enumeration in the EnumerateAllContent function that is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="81c60-108">Diese Funktion ruft wiederum eine rekursiveenumerate-Funktion auf, die die Hierarchie von Objekten durchläuft, die auf dem ausgewählten Gerät gefunden wurden, und gibt für jedes Objekt einen Objekt Bezeichner zurück.</span><span class="sxs-lookup"><span data-stu-id="81c60-108">This function, in turn, calls a RecursiveEnumerate function that walks the hierarchy of objects found on the selected device and returns an object identifier for each object.</span></span>

<span data-ttu-id="81c60-109">Wie bereits erwähnt, ruft die recursiveenumerate-Funktion einen Objekt Bezeichner für jedes Objekt ab, das auf dem Gerät gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="81c60-109">As noted, the RecursiveEnumerate function retrieves an object identifier for each object found on the device.</span></span> <span data-ttu-id="81c60-110">Der Objekt Bezeichner ist ein Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="81c60-110">The object identifier is a string value.</span></span> <span data-ttu-id="81c60-111">Nachdem Ihre Anwendung diesen Bezeichner abgerufen hat, kann er weitere beschreibende Objektinformationen abrufen (z. b. den Namen des Objekts, den Bezeichner für das übergeordnete Objekt des Objekts usw.).</span><span class="sxs-lookup"><span data-stu-id="81c60-111">Once your application retrieves this identifier, it can obtain more descriptive object information (such as the object's name, the identifier for the object's parent, and so on).</span></span> <span data-ttu-id="81c60-112">Diese beschreibenden Informationen werden als Objekteigenschaften (oder Metadaten) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="81c60-112">This descriptive information is referred to as object properties (or metadata).</span></span> <span data-ttu-id="81c60-113">Die Anwendung kann diese Eigenschaften abrufen, indem Sie Member der [**iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="81c60-113">Your application can retrieve these properties by calling members of the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span></span>

<span data-ttu-id="81c60-114">Die enumerateallcontent-Funktion beginnt mit dem Abrufen eines Zeigers auf eine [**iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span><span class="sxs-lookup"><span data-stu-id="81c60-114">The EnumerateAllContent function begins by retrieving a pointer to an [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span></span> <span data-ttu-id="81c60-115">Dieser Zeiger wird durch Aufrufen der [**iportabledevice:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="81c60-115">It retrieves this pointer by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="81c60-116">Nachdem der Zeiger auf die iportabledevicecontent-Schnittstelle abgerufen wurde, ruft die enumerateallcontent-Funktion die recursiveenumerate-Funktion auf, die die Hierarchie von Objekten durchläuft, die auf dem angegebenen Gerät gefunden wurden, und gibt jeweils einen Objekt Bezeichner zurück.</span><span class="sxs-lookup"><span data-stu-id="81c60-116">Once it retrieves the pointer to the IPortableDeviceContent interface, the EnumerateAllContent function calls the RecursiveEnumerate function, which walks the hierarchy of objects found on the given device and returns an object identifier for each.</span></span>

<span data-ttu-id="81c60-117">Die recursiveenumerate-Funktion beginnt mit dem Abrufen eines Zeigers auf eine [**ienumportabledeviceobjectids-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="81c60-117">The RecursiveEnumerate function begins by retrieving a pointer to an [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span> <span data-ttu-id="81c60-118">Diese Schnittstelle macht die Methoden verfügbar, die eine Anwendung verwendet, um in der Liste der auf einem bestimmten Gerät gefundenen Objekte zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="81c60-118">This interface exposes the methods that an application uses to navigate the list of objects found on a given device.</span></span>

<span data-ttu-id="81c60-119">In diesem Beispiel ruft die recursiveenumerate-Funktion die [**ienumportabledeviceobjectids:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) -Methode auf, um die Liste der-Objekte zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="81c60-119">In this sample, the RecursiveEnumerate function calls the [**IEnumPortableDeviceObjectIDs::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method to traverse the list of objects.</span></span>

<span data-ttu-id="81c60-120">Jeder Aufrufen der [**ienumportabledeviceobjects:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) -Methode fordert einen Batch von 10 bezeichern an.</span><span class="sxs-lookup"><span data-stu-id="81c60-120">Each call to the [**IEnumPortableDeviceObjects::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method requests a batch of 10 identifiers.</span></span> <span data-ttu-id="81c60-121">(Dieser Wert wird durch den num \_ angegeben. Objekte \_ zum \_ Anfordern einer Konstante, die als erstes Argument bereitgestellt wird.)</span><span class="sxs-lookup"><span data-stu-id="81c60-121">(This value is specified by the NUM\_OBJECTS\_TO\_REQUEST constant that is supplied as the first argument.)</span></span>


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
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
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
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



## <a name="related-topics"></a><span data-ttu-id="81c60-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="81c60-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81c60-123">**Ienumportabledeviceobjectids-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="81c60-123">**IEnumPortableDeviceObjectIDs Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="81c60-124">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="81c60-124">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="81c60-125">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="81c60-125">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="81c60-126">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="81c60-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="81c60-127">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="81c60-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




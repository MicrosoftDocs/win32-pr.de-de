---
description: Abrufen von Eigenschaften für ein einzelnes Objekt
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Abrufen von Eigenschaften für ein einzelnes Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353831"
---
# <a name="retrieving-properties-for-a-single-object"></a><span data-ttu-id="a1497-103">Abrufen von Eigenschaften für ein einzelnes Objekt</span><span class="sxs-lookup"><span data-stu-id="a1497-103">Retrieving Properties for a Single Object</span></span>

<span data-ttu-id="a1497-104">Nachdem die Anwendung einen Objekt Bezeichner abgerufen hat (siehe das Thema zum Auflisten von Inhalten), kann er beschreibende Informationen zu diesem Objekt abrufen, indem er Methoden in der [**iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) und die [**iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md) [aufruft](enumerating-content.md) .</span><span class="sxs-lookup"><span data-stu-id="a1497-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can retrieve descriptive information about that object by calling methods in the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) and the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md).</span></span>

<span data-ttu-id="a1497-105">Die [**iportabledeviceproperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) -Methode ruft eine Liste der angegebenen Eigenschaften für ein angegebenes Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="a1497-105">The [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method retrieves a list of specified properties for a given object.</span></span> <span data-ttu-id="a1497-106">(Ihre Anwendung könnte auch die GetValues-Methode aufrufen und einen **null** -Wert für den pkeys-Parameter angeben, um alle Eigenschaften für ein bestimmtes Objekt abzurufen. die Leistung dieser Methode kann jedoch beim Abrufen aller Eigenschaften erheblich langsamer sein.)</span><span class="sxs-lookup"><span data-stu-id="a1497-106">(Your application could also call the GetValues method and specify a **NULL** value for the pKeys parameter to retrieve all properties for a given object; however, the performance of this method may be significantly slower when retrieving all properties.)</span></span>

<span data-ttu-id="a1497-107">Bevor die Anwendung GetValues aufruft, muss Sie jedoch die abzurufenden Eigenschaften ermitteln, indem die entsprechenden Schlüssel in einem [**iportabledevicekeycollection-Objekt**](iportabledevicekeycollection.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a1497-107">Before your application calls GetValues, however, it needs to identify the properties to retrieve by setting corresponding keys in an [**IPortableDeviceKeyCollection object**](iportabledevicekeycollection.md).</span></span> <span data-ttu-id="a1497-108">Ihre Anwendung identifiziert die relevanten Eigenschaften, indem Sie die [**iportabledevicekeycollection:: Add**](iportabledevicekeycollection-add.md) -Methode aufrufen und einen PropertyKey-Wert bereitstellt, der jede abzurufende Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a1497-108">Your application will identify the properties of interest by calling the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method and supplying a PROPERTYKEY value that identifies each property that it will retrieve.</span></span>

<span data-ttu-id="a1497-109">Die Funktion "lesecontentproperties" im Modul "contentproperties. cpp" der Beispielanwendung veranschaulicht, wie die fünf Eigenschaften für ein ausgewähltes Objekt abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="a1497-109">The ReadContentProperties function in the ContentProperties.cpp module of the sample application demonstrates how the five properties were retrieved for a selected object.</span></span> <span data-ttu-id="a1497-110">In der folgenden Tabelle werden die einzelnen Eigenschaften und deren zugehöriger refpropertykey-Wert beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a1497-110">The following table describes each of these properties and their corresponding REFPROPERTYKEY value.</span></span>



| <span data-ttu-id="a1497-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a1497-111">Property</span></span>                     | <span data-ttu-id="a1497-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1497-112">Description</span></span>                                                                                                                                      | <span data-ttu-id="a1497-113">PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="a1497-113">PROPERTYKEY</span></span>                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="a1497-114">Übergeordnete Objekt Kennung</span><span class="sxs-lookup"><span data-stu-id="a1497-114">Parent-object identifier</span></span>     | <span data-ttu-id="a1497-115">Eine Zeichenfolge, die den Bezeichner für das übergeordnete Objekt des angegebenen-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="a1497-115">A string that specifies the identifier for the given object's parent.</span></span>                                                                            | <span data-ttu-id="a1497-116">übergeordnete WPD- \_ Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="a1497-116">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="a1497-117">Objektname</span><span class="sxs-lookup"><span data-stu-id="a1497-117">Object name</span></span>                  | <span data-ttu-id="a1497-118">Eine Zeichenfolge, die den Namen des angegebenen-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="a1497-118">A string that specifies the name of the given object.</span></span>                                                                                            | <span data-ttu-id="a1497-119">WPD- \_ Objekt \_ Name</span><span class="sxs-lookup"><span data-stu-id="a1497-119">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="a1497-120">Persistente eindeutige Kennung</span><span class="sxs-lookup"><span data-stu-id="a1497-120">Persistent unique identifier</span></span> | <span data-ttu-id="a1497-121">Eine Zeichenfolge, die einen eindeutigen Bezeichner für das angegebene Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="a1497-121">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="a1497-122">(Dieser Bezeichner ist im Gegensatz zum Objekt Bezeichner Sitzungs übergreifend persistent.)</span><span class="sxs-lookup"><span data-stu-id="a1497-122">(This identifier is persistent across sessions, unlike the object identifier.)</span></span> | <span data-ttu-id="a1497-123">\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt</span><span class="sxs-lookup"><span data-stu-id="a1497-123">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="a1497-124">Objekt Format</span><span class="sxs-lookup"><span data-stu-id="a1497-124">Object format</span></span>                | <span data-ttu-id="a1497-125">Eine Globally Unique Identifier (GUID), die das Format der Datei angibt, die einem angegebenen Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="a1497-125">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object.</span></span>                                       | <span data-ttu-id="a1497-126">WPD- \_ Objekt \_ Format</span><span class="sxs-lookup"><span data-stu-id="a1497-126">WPD\_OBJECT\_FORMAT</span></span>                 |
| <span data-ttu-id="a1497-127">Objekt Inhaltstyp</span><span class="sxs-lookup"><span data-stu-id="a1497-127">Object content type</span></span>          | <span data-ttu-id="a1497-128">Eine GUID, die den Typ des Inhalts angibt, der einem angegebenen Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a1497-128">A GUID that specifies the type of content associated with a given object.</span></span>                                                                        | <span data-ttu-id="a1497-129">Inhaltstyp für WPD- \_ Objekt \_ \_</span><span class="sxs-lookup"><span data-stu-id="a1497-129">WPD\_OBJECT\_CONTENT\_TYPE</span></span>          |



 

<span data-ttu-id="a1497-130">Der folgende Auszug aus der Funktion "Read contentproperties" veranschaulicht, wie die Beispielanwendung die [**iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md) und die [**iportabledevicekeycollection:: Add**](iportabledevicekeycollection-add.md) -Methode verwendet, um die abzurufenden Eigenschaften zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a1497-130">The following excerpt from the ReadContentProperties function demonstrates how the sample application used the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method to identify the properties it would retrieve.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="a1497-131">Nachdem die Beispielanwendung die entsprechenden Schlüssel festgelegt hat, wurde die [**iportabledeviceproperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) -Methode aufgerufen, um die angegebenen Werte für das angegebene Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a1497-131">Once the sample application set the appropriate keys, it called the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method to retrieve the specified values for the given object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="a1497-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1497-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1497-133">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a1497-133">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="a1497-134">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a1497-134">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="a1497-135">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a1497-135">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="a1497-136">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="a1497-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




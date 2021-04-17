---
description: Abrufen von Eigenschaften für mehrere Objekte nach Objekt Format
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Abrufen von Eigenschaften für mehrere Objekte nach Objekt Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485459"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a><span data-ttu-id="84556-103">Abrufen von Eigenschaften für mehrere Objekte nach Objekt Format</span><span class="sxs-lookup"><span data-stu-id="84556-103">Retrieving Properties for Multiple Objects by Object Format</span></span>

<span data-ttu-id="84556-104">Zusätzlich zum Massen Abruf von Eigenschaften für eine Auflistung von Objekt bezeichmern kann eine Anwendung auch einen Massen Abruf von Eigenschaften für alle Objekte eines bestimmten Typs durchführen.</span><span class="sxs-lookup"><span data-stu-id="84556-104">In addition to a bulk retrieval of properties for a collection of object identifiers, an application can also perform a bulk retrieval of properties for all objects of a particular type.</span></span> <span data-ttu-id="84556-105">Wie im vorherigen Beispiel ist es für den Massen Abruf für einen bestimmten Typ erforderlich, dass der Gerätetreiber Massen Abruf Vorgänge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84556-105">As in the previous example, bulk retrieval for a given type requires that the device driver support bulk retrievals.</span></span>

<span data-ttu-id="84556-106">Die Anwendung kann einen Massen Abruf mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen ausführen.</span><span class="sxs-lookup"><span data-stu-id="84556-106">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="84556-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="84556-107">Interface</span></span>                                                                                      | <span data-ttu-id="84556-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84556-108">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="84556-109">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="84556-110">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="84556-110">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="84556-111">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-111">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="84556-112">Wird verwendet, um die abzurufenden Eigenschaften zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="84556-112">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="84556-113">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-113">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="84556-114">Wird verwendet, um zu bestimmen, ob ein bestimmter Treiber Massen Vorgänge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84556-114">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="84556-115">**Iportabledevicepropertiesbulk-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-115">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="84556-116">Unterstützt den Massen Abruf Vorgang.</span><span class="sxs-lookup"><span data-stu-id="84556-116">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="84556-117">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-117">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="84556-118">Wird zum Speichern der Objekt Bezeichner für den Massen Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="84556-118">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="84556-119">Die Funktion "lesecontentpropertiesbulkfilteringformat" im Modul "contentproperties. cpp" der Beispielanwendung veranschaulicht einen Massen Abruf Vorgang für Objekte eines bestimmten Typs oder Formats.</span><span class="sxs-lookup"><span data-stu-id="84556-119">The ReadContentPropertiesBulkFilteringFormat function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation for objects of a particular type or format.</span></span>

<span data-ttu-id="84556-120">Der Code in der Funktion "Read contentpropertiesbulkfilteringformat" ist nahezu identisch mit dem Code, der in der Funktion "Read contentpropertiesbulk" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="84556-120">The code found in the ReadContentPropertiesBulkFilteringFormat function is almost identical to the code found in the ReadContentPropertiesBulk function.</span></span> <span data-ttu-id="84556-121">(Eine ausführliche Beschreibung dieser Funktion finden Sie im Thema [Abrufen von Eigenschaften für mehrere Objekte](retrieving-properties-for-multiple-objects.md) .)</span><span class="sxs-lookup"><span data-stu-id="84556-121">(See the [Retrieving Properties for Multiple Objects](retrieving-properties-for-multiple-objects.md) topic for a complete description of this function.)</span></span>

<span data-ttu-id="84556-122">Der einzige Hauptunterschied tritt auf, wenn der Vorgang in die Warteschlange eingereiht wird.</span><span class="sxs-lookup"><span data-stu-id="84556-122">The one primary difference occurs when the operation is queued.</span></span> <span data-ttu-id="84556-123">Beim Filtern nach Typ oder Format wird die [**iportabledevicepropertiesbulk:: queuegetvaluesbyobjectformat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) -Methode anstelle der [**iportabledevicepropertiesbulk:: queuegetvaluesbyobjectlist**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="84556-123">When filtering by type or format, the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) method is called instead of the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) method.</span></span>


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a><span data-ttu-id="84556-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84556-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84556-125">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="84556-126">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="84556-127">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-127">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="84556-128">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-128">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="84556-129">**Iportabledevicepropertiesbulk-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-129">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="84556-130">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="84556-130">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="84556-131">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="84556-131">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




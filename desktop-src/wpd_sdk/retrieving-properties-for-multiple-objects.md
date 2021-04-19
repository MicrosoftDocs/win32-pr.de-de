---
description: Abrufen von Eigenschaften für mehrere Objekte
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Abrufen von Eigenschaften für mehrere Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366142"
---
# <a name="retrieving-properties-for-multiple-objects"></a><span data-ttu-id="91c7b-103">Abrufen von Eigenschaften für mehrere Objekte</span><span class="sxs-lookup"><span data-stu-id="91c7b-103">Retrieving Properties for Multiple Objects</span></span>

<span data-ttu-id="91c7b-104">Einige Gerätetreiber unterstützen das Abrufen von Eigenschaften für mehrere Objekte in einem einzelnen Funktionsaufrufs. Dies wird als Massen Abruf bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="91c7b-104">Some device drivers support the retrieval of properties for multiple objects in a single function call; this is referred to as a bulk retrieval.</span></span> <span data-ttu-id="91c7b-105">Es gibt zwei Arten von Massen Abruf Vorgängen: mit dem ersten Typ werden Eigenschaften für eine Liste von Objekten abgerufen, und der zweite Typ Ruft Eigenschaften für alle Objekte eines angegebenen Formats ab.</span><span class="sxs-lookup"><span data-stu-id="91c7b-105">There are two types of bulk retrieval operations: the first type retrieves properties for a list of objects, and the second type retrieves properties for all objects of a given format.</span></span> <span data-ttu-id="91c7b-106">Das in diesem Abschnitt beschriebene Beispiel veranschaulicht das erste.</span><span class="sxs-lookup"><span data-stu-id="91c7b-106">The example described in this section demonstrates the former.</span></span>

<span data-ttu-id="91c7b-107">Die Anwendung kann einen Massen Abruf mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen ausführen.</span><span class="sxs-lookup"><span data-stu-id="91c7b-107">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="91c7b-108">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="91c7b-108">Interface</span></span>                                                                                      | <span data-ttu-id="91c7b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91c7b-109">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="91c7b-110">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="91c7b-111">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="91c7b-111">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="91c7b-112">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-112">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="91c7b-113">Wird verwendet, um die abzurufenden Eigenschaften zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="91c7b-113">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="91c7b-114">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-114">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="91c7b-115">Wird verwendet, um zu bestimmen, ob ein bestimmter Treiber Massen Vorgänge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91c7b-115">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="91c7b-116">**Iportabledevicepropertiesbulk-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-116">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="91c7b-117">Unterstützt den Massen Abruf Vorgang.</span><span class="sxs-lookup"><span data-stu-id="91c7b-117">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="91c7b-118">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-118">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="91c7b-119">Wird zum Speichern der Objekt Bezeichner für den Massen Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="91c7b-119">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="91c7b-120">Die Funktion "lesecontentpropertiesbulk" im Modul "contentproperties. cpp" der Beispielanwendung veranschaulicht einen Massen Abruf Vorgang.</span><span class="sxs-lookup"><span data-stu-id="91c7b-120">The ReadContentPropertiesBulk function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation.</span></span>

<span data-ttu-id="91c7b-121">Die erste Aufgabe, die in diesem Beispiel ausgeführt wird, besteht darin, zu bestimmen, ob der angegebene Treiber Massen Vorgänge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91c7b-121">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="91c7b-122">Dies wird erreicht, indem QueryInterface auf der iportabledeviceproperties-Schnittstelle aufgerufen und das vorhanden sein von iportabledevicepropertiesbulk überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="91c7b-122">This is accomplished by calling QueryInterface on the IPortableDeviceProperties interface and checking for the existence of IPortableDevicePropertiesBulk.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



<span data-ttu-id="91c7b-123">Wenn der Treiber Massen Vorgänge unterstützt, besteht der nächste Schritt darin, eine Instanz der [**iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md) zu erstellen und die Schlüssel anzugeben, die den Eigenschaften entsprechen, die von der Anwendung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="91c7b-123">If the driver supports bulk operations, the next step is to create an instance of the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and to specify the keys that correspond to the properties that the application will retrieve.</span></span> <span data-ttu-id="91c7b-124">Eine Beschreibung dieses Prozesses finden Sie im Thema [Abrufen von Eigenschaften für ein einzelnes Objekt](retrieving-properties-for-a-single-object.md) .</span><span class="sxs-lookup"><span data-stu-id="91c7b-124">For a description of this process, see the [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md) topic.</span></span>

<span data-ttu-id="91c7b-125">Nachdem die entsprechenden Schlüssel angegeben wurden, erstellt die Beispielanwendung eine Instanz der [**iportabledevicepropertiesbulkcallback-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="91c7b-125">After the appropriate keys are specified, the sample application creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="91c7b-126">Die Anwendung verwendet die Methoden in dieser Schnittstelle, um den Fortschritt des asynchronen Massen Abruf Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="91c7b-126">The application will use the methods in this interface to track the progress of the asynchronous bulk-retrieval operation.</span></span>


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="91c7b-127">Die nächste Funktion, die von der Beispielanwendung aufgerufen wird, ist die "samateiportabledevicepropvariantcollectionwithzugewiesene"-Hilfsfunktion.</span><span class="sxs-lookup"><span data-stu-id="91c7b-127">The next function that the sample application calls is the CreateIPortableDevicePropVariantCollectionWithAllObjectIDs helper function.</span></span> <span data-ttu-id="91c7b-128">Diese Funktion erstellt beispielsweise eine Liste aller verfügbaren Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="91c7b-128">This function creates a list of all available object identifiers for example purposes.</span></span> <span data-ttu-id="91c7b-129">(Eine reale Anwendung schränkt die Liste der Bezeichner auf einen bestimmten Satz von Objekten ein.</span><span class="sxs-lookup"><span data-stu-id="91c7b-129">(A real-world application would limit the list of identifiers to a particular set of objects.</span></span> <span data-ttu-id="91c7b-130">Beispielsweise kann eine Anwendung eine Liste von Bezeichnernamen für alle Objekte erstellen, die sich derzeit in einer bestimmten Ordneransicht befinden.)</span><span class="sxs-lookup"><span data-stu-id="91c7b-130">For instance, an application may create a list of identifiers for all of the objects currently in a given folder view.)</span></span>

<span data-ttu-id="91c7b-131">Wie bereits erwähnt, listet die Hilfsfunktion rekursiv alle Objekte auf einem bestimmten Gerät auf.</span><span class="sxs-lookup"><span data-stu-id="91c7b-131">As noted above, the helper function recursively enumerates all objects on a given device.</span></span> <span data-ttu-id="91c7b-132">Diese Liste wird in einer [**iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) zurückgegeben, die einen Bezeichner für jedes gefundene Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="91c7b-132">It returns this list in an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="91c7b-133">Die Hilfsfunktion ist im Modul "contentenumeration. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="91c7b-133">The helper function is defined in the module ContentEnumeration.cpp.</span></span>


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



<span data-ttu-id="91c7b-134">Sobald die vorherigen Schritte ausgeführt wurden, initiiert die Beispielanwendung den Abruf der asynchronen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91c7b-134">Once the previous steps are accomplished, the sample application initiates the asynchronous property retrieval.</span></span> <span data-ttu-id="91c7b-135">Gehen Sie hierzu wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="91c7b-135">This is accomplished by doing the following:</span></span>

1.  <span data-ttu-id="91c7b-136">Aufrufen von iportabledevicepropertiesbulk:: queuegetvaluesbyobjectlist, die eine Anforderung für den Abruf der Massen Eigenschaft in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="91c7b-136">Calling IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, which queues a request for the bulk property retrieval.</span></span> <span data-ttu-id="91c7b-137">(Beachten Sie, dass die Anforderung zwar in die Warteschlange eingereiht ist, aber nicht gestartet wird.)</span><span class="sxs-lookup"><span data-stu-id="91c7b-137">(Note that although the request is queued, it is not started.)</span></span>
2.  <span data-ttu-id="91c7b-138">Iportabledevicepropertiesbulk:: Start wird aufgerufen, um die Anforderung in der Warteschlange zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="91c7b-138">Calling IPortableDevicePropertiesBulk::Start to initiate the queued request.</span></span>

<span data-ttu-id="91c7b-139">Diese Schritte werden im folgenden Code Ausschnitt aus der Beispielanwendung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="91c7b-139">These steps are demonstrated in the following code excerpt from the sample application.</span></span>


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



## <a name="related-topics"></a><span data-ttu-id="91c7b-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91c7b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91c7b-141">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-141">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="91c7b-142">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="91c7b-143">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="91c7b-144">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-144">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="91c7b-145">**Iportabledevicepropertiesbulk-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-145">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="91c7b-146">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91c7b-146">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="91c7b-147">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="91c7b-147">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




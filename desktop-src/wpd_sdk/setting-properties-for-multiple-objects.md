---
description: Festlegen von Eigenschaften für mehrere Objekte
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: Festlegen von Eigenschaften für mehrere Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e951662d9920cb22db0a417f1af94f3eb7eb4d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350824"
---
# <a name="setting-properties-for-multiple-objects"></a><span data-ttu-id="64cba-103">Festlegen von Eigenschaften für mehrere Objekte</span><span class="sxs-lookup"><span data-stu-id="64cba-103">Setting Properties for Multiple Objects</span></span>

<span data-ttu-id="64cba-104">Einige Gerätetreiber unterstützen das Festlegen von Eigenschaften für mehrere Objekte in einem einzelnen Funktions Aufruf– Dies wird als Massen Schreibvorgang bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="64cba-104">Some device drivers support setting properties for multiple objects in a single function call—this is referred to as a bulk write.</span></span> <span data-ttu-id="64cba-105">Die Anwendung kann mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen einen Massen Schreibvorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="64cba-105">Your application can perform a bulk write using the interfaces described in the following table.</span></span>



| <span data-ttu-id="64cba-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="64cba-106">Interface</span></span>                                                                                      | <span data-ttu-id="64cba-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64cba-107">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="64cba-108">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="64cba-109">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="64cba-109">Provides access to the content-specific methods.</span></span>             |
| [<span data-ttu-id="64cba-110">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="64cba-111">Bietet Zugriff auf die Eigenschaften spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="64cba-111">Provides access to the property-specific methods.</span></span>            |
| [<span data-ttu-id="64cba-112">**Iportabledevicepropertiesbulk-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-112">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="64cba-113">Unterstützt den Massen Schreibvorgang.</span><span class="sxs-lookup"><span data-stu-id="64cba-113">Supports the bulk write operation.</span></span>                           |
| [<span data-ttu-id="64cba-114">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="64cba-115">Wird zum Speichern der Objekt Bezeichner für den Massen Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="64cba-115">Used to store the object identifiers for the bulk operation.</span></span> |
| [<span data-ttu-id="64cba-116">**Iportableabvicevaluescollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-116">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="64cba-117">Wird verwendet, um die Eigenschaften zu identifizieren, die geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64cba-117">Used to identify the properties to be written.</span></span>               |



 

<span data-ttu-id="64cba-118">Die `WriteContentPropertiesBulk` Funktion im Modul contentproperties. cpp der Beispielanwendung veranschaulicht einen Massen Schreibvorgang.</span><span class="sxs-lookup"><span data-stu-id="64cba-118">The `WriteContentPropertiesBulk` function in the sample application's ContentProperties.cpp module demonstrates a bulk write operation.</span></span>

<span data-ttu-id="64cba-119">Die erste Aufgabe, die in diesem Beispiel ausgeführt wird, besteht darin, zu bestimmen, ob der angegebene Treiber Massen Vorgänge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64cba-119">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="64cba-120">Dies erfolgt durch Aufrufen von QueryInterface für ein **iportabledeviceproperties** -Objekt und überprüfen, ob **iportabledevicepropertiesbulk** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64cba-120">This is accomplished by calling QueryInterface on an **IPortableDeviceProperties** object and checking for the existence of **IPortableDevicePropertiesBulk**.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
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



<span data-ttu-id="64cba-121">Die nächste Aufgabe umfasst das Erstellen eines **iportabledevicevaluescollection** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="64cba-121">The next task entails creating an **IPortableDeviceValuesCollection** object.</span></span> <span data-ttu-id="64cba-122">Dies ist das Objekt, das die Eigenschaftswerte enthält, die vom Beispiel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="64cba-122">This is the object that contains the property values that the sample will write.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDeviceValuesCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDeviceValuesCollection,
                          (VOID**) &pPropertiesToWrite);
    if (FAILED(hr))
    {
        printf("! Failed to CoCreate IPortableDeviceValuesCollection for bulk property values, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="64cba-123">Danach erstellt das Beispiel eine Instanz der [**iportabledevicepropertiesbulkcallback-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="64cba-123">After this, the sample creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="64cba-124">Die Anwendung verwendet die Methoden in dieser Schnittstelle, um den Fortschritt des asynchronen Massen Schreibvorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="64cba-124">The application will use the methods in this interface to track the progress of the asynchronous bulk-write operation.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    pCallback = new CSetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CSetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="64cba-125">Die nächste Funktion, die von der Beispielanwendung aufgerufen wird, ist die `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` Hilfsfunktion.</span><span class="sxs-lookup"><span data-stu-id="64cba-125">The next function that the sample application calls is the `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` helper function.</span></span> <span data-ttu-id="64cba-126">Diese Funktion listet rekursiv alle Objekte auf einem bestimmten Gerät auf und gibt eine [**iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) zurück, die einen Bezeichner für jedes gefundene Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="64cba-126">This function recursively enumerates all objects on a given device and returns an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="64cba-127">Diese Funktion wird im Modul "contentenumeration. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="64cba-127">This function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="64cba-128">Das **iportabledevicepropvariantcollection** -Objekt enthält eine Auflistung von indizierten **PROPVARIANT** -Werten desselben VarType.</span><span class="sxs-lookup"><span data-stu-id="64cba-128">The **IPortableDevicePropVariantCollection** object holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="64cba-129">In diesem Fall enthalten diese Werte einen angegebenen Objekt Bezeichner für jedes Objekt, das auf dem Gerät gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="64cba-129">In this case, these values contain a given object identifier for each object found on the device.</span></span>

<span data-ttu-id="64cba-130">Die Objekt-IDs und deren jeweilige Name-Eigenschaften werden in einem [**iportableabvicevaluescollection**](iportabledevicevalues.md) -Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="64cba-130">The object identifiers and their respective name properties are stored in an [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) object.</span></span> <span data-ttu-id="64cba-131">Die Name-Eigenschaften sind so organisiert, dass dem ersten Objekt eine Name-Eigenschaft von "NewName0" zugewiesen wird, dem zweiten Objekt eine Name-Eigenschaft von "NewName1" zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="64cba-131">The name properties are organized so that the first object is assigned a name property of "NewName0", the second object is assigned a name property of "NewName1", and so on.</span></span>

<span data-ttu-id="64cba-132">Der folgende Auszug aus dem Beispiel veranschaulicht, wie das **iportabledebug** -Objekt mit Objekt Bezeichner und neuen Namens Zeichenfolgen initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="64cba-132">The following excerpt from the sample demonstrates how the **IPortableDeviceValuesCollection** object was initialized with object identifiers and new name strings.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = pObjectIDs->GetCount(&cObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of objectIDs from IPortableDevicePropVariantCollection, hr = 0x%lx\n", hr);
    }
}


if (SUCCEEDED(hr))
{
    for(DWORD dwIndex = 0; (dwIndex < cObjectIDs) && (hr == S_OK); dwIndex++)
    {
        CComPtr<IPortableDeviceValues>  pValues;
        PROPVARIANT                     pv = {0};

        PropVariantInit(&pv);
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pValues);
        if (FAILED(hr))
        {
            printf("! Failed to CoCreate CLSID_PortableDeviceValues, hr = 0x%lx\n", hr);
        }

        // Get the Object ID whose properties we will set
        if (hr == S_OK)
        {
            hr = pObjectIDs->GetAt(dwIndex, &pv);
            if (FAILED(hr))
            {
                printf("! Failed to get next Object ID from list, hr = 0x%lx\n", hr);
            }
        }

        // Save them into the IPortableDeviceValues so the driver knows which object this proeprty set belongs to
        if (hr == S_OK)
        {
            hr = pValues->SetStringValue(WPD_OBJECT_ID, pv.pwszVal);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID, hr = 0x%lx\n", hr);
            }
        }

        // Set the new values.  In this sample, we attempt to set the name property.
        if (hr == S_OK)
        {
            CAtlStringW strValue;
            strValue.Format(L"NewName%d", dwIndex);

            hr = pValues->SetStringValue(WPD_OBJECT_NAME, strValue.GetString());
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_NAME, hr = 0x%lx\n", hr);
            }
        }

        // Add this property set to the collection
        if (hr == S_OK)
        {
            hr = pPropertiesToWrite->Add(pValues);
            if (FAILED(hr))
            {
                printf("! Failed to add values to collection, hr = 0x%lx\n", hr);
            }
        }
        PropVariantClear(&pv);
    }
}
```



<span data-ttu-id="64cba-133">Sobald das Beispiel das **iportabledevicevaluescollection** -Objekt erstellt hat, das den Objekt Bezeichner und die namens Paare enthält, kann der asynchrone Vorgang gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="64cba-133">Once the sample creates the **IPortableDeviceValuesCollection** object that contains the object identifier and name pairs, it can begin the asynchronous operation.</span></span>

<span data-ttu-id="64cba-134">Der asynchrone Schreibvorgang beginnt, wenn das Beispiel die [**iportabledevicepropertiesbulk:: queuesetvaluesbyobjectlist**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="64cba-134">The asynchronous write operation begins when the sample calls the [**IPortableDevicePropertiesBulk::QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) method.</span></span> <span data-ttu-id="64cba-135">Diese Methode benachrichtigt den Treiber, dass ein Massen Vorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="64cba-135">This method notifies the driver that a bulk operation is about to begin.</span></span> <span data-ttu-id="64cba-136">Danach ruft das Beispiel die [**iportabledevicebulk:: Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) -Methode auf, um zu beginnen, die neuen Namens Werte tatsächlich zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="64cba-136">After this, the sample calls the [**IPortableDeviceBulk::Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) method to begin actually writing the new name values.</span></span>


```C++
   HRESULT                                       hr                = S_OK;
   GUID                                          guidContext       = GUID_NULL;
   CSetBulkValuesCallback*                       pCallback         = NULL;
   CComPtr<IPortableDeviceProperties>            pProperties;
   CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
   CComPtr<IPortableDeviceValues>                pObjectProperties;
   CComPtr<IPortableDeviceContent>               pContent;
   CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
   CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
   DWORD                                         cObjectIDs        = 0;
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueSetValuesByObjectList(pPropertiesToWrite,
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
           printf("! QueueSetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



<span data-ttu-id="64cba-137">Beachten Sie, dass das Beispiel eine unendlich lange Zeitspanne für den Abschluss des Vorgangs wartet.</span><span class="sxs-lookup"><span data-stu-id="64cba-137">Note that the sample waits an infinitely long period of time for the operation to complete.</span></span> <span data-ttu-id="64cba-138">Wenn dies eine Produktionsanwendung wäre, müsste der Code geändert werden.</span><span class="sxs-lookup"><span data-stu-id="64cba-138">If this were a production application, the code would need to be modified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64cba-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64cba-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64cba-140">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="64cba-141">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="64cba-142">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-142">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="64cba-143">**Iportabledevicepropertiesbulk-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-143">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="64cba-144">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64cba-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="64cba-145">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="64cba-145">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




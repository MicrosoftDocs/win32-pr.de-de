---
description: Festlegen von Eigenschaften für ein einzelnes Objekt
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: Festlegen von Eigenschaften für ein einzelnes Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5649d05ccadfeaef0dd8805abd7d556f7725f175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350139"
---
# <a name="setting-properties-for-a-single-object"></a><span data-ttu-id="08010-103">Festlegen von Eigenschaften für ein einzelnes Objekt</span><span class="sxs-lookup"><span data-stu-id="08010-103">Setting Properties for a Single Object</span></span>

<span data-ttu-id="08010-104">Nachdem die Anwendung einen Objekt Bezeichner abgerufen hat (siehe das Thema zum Auflisten von [Inhalten](enumerating-content.md) ), können Sie die Eigenschaften für dieses Objekt festlegen, indem Sie Methoden in den in der folgenden Tabelle beschriebenen Schnittstellen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="08010-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can set properties for that object by calling methods in the interfaces described in the following table.</span></span>



| <span data-ttu-id="08010-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="08010-105">Interface</span></span>                                                                | <span data-ttu-id="08010-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08010-106">Description</span></span>                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08010-107">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08010-107">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="08010-108">Wird verwendet, um zu bestimmen, ob eine bestimmte Eigenschaft geschrieben werden kann, und um den Schreibvorgang zu senden.</span><span class="sxs-lookup"><span data-stu-id="08010-108">Used to determine whether a given property can be written and to send the write operation.</span></span>                                                                  |
| [<span data-ttu-id="08010-109">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08010-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="08010-110">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="08010-110">Provides access to the content-specific methods.</span></span>                                                                                                            |
| [<span data-ttu-id="08010-111">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08010-111">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="08010-112">Dient zum Speichern der zu schreibenden Werte, zum Bestimmen der Ergebnisse des Schreibvorgangs und zum Abrufen von Attribut Attributen (beim Bestimmen der Schreibfunktion).</span><span class="sxs-lookup"><span data-stu-id="08010-112">Used to hold the values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="08010-113">Anwendungen legen Eigenschaften für ein Objekt fest, indem Sie zuerst einen Eigenschaften Behälter erstellen, der die neuen Werte mithilfe der [**iportabledebug-Schnittstelle**](iportabledevicevalues.md)angibt.</span><span class="sxs-lookup"><span data-stu-id="08010-113">Applications set properties on an object by first creating a property bag that specifies the new values using the [**IPortableDeviceValues interface**](iportabledevicevalues.md).</span></span> <span data-ttu-id="08010-114">Nachdem der Eigenschaften Behälter erstellt wurde, legt eine Anwendung diese Eigenschaften fest, indem Sie die [**iportabledeviceproperties:: SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="08010-114">Once the property bag is created, an application sets those properties by calling the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) method.</span></span>

<span data-ttu-id="08010-115">Die `WriteContentProperties` Funktion im Modul contentproperties. cpp der Beispielanwendung veranschaulicht, wie eine Anwendung für ein ausgewähltes Objekt eine neue Eigenschaft für den Objektnamen festlegen könnte.</span><span class="sxs-lookup"><span data-stu-id="08010-115">The `WriteContentProperties` function in the sample application's ContentProperties.cpp module demonstrates how an application could set a new object-name property for a selected object.</span></span>

<span data-ttu-id="08010-116">Die erste Aufgabe, die von der-Funktion durchgeführt `WriteContentProperties` wird, besteht darin, den Benutzer zur Eingabe eines Objekt Bezeichners für das Objekt aufzufordern, für das die Anwendung den neuen Namen schreiben soll.</span><span class="sxs-lookup"><span data-stu-id="08010-116">The first task accomplished by the `WriteContentProperties` function is to prompt the user to enter an object identifier for the object that the application will write the new name for.</span></span>


```C++
HRESULT                               hr                   = S_OK;
WCHAR                                 szSelection[81]      = {0};
WCHAR                                 szNewObjectName[81]  = {0};
CComPtr<IPortableDeviceProperties>    pProperties;
CComPtr<IPortableDeviceContent>       pContent;
CComPtr<IPortableDeviceValues>        pObjectPropertiesToWrite;
CComPtr<IPortableDeviceValues>        pPropertyWriteResults;
CComPtr<IPortableDeviceValues>        pAttributes;
BOOL                                  bCanWrite            = FALSE;

// Prompt user to enter an object identifier on the device to write properties on.
printf("Enter the identifer of the object you wish to write properties on.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting property reading\n");
}
```



<span data-ttu-id="08010-117">Danach ruft die Anwendung das WPD- \_ Eigenschafts Attribut ab und \_ \_ kann \_ einen Wert für die Eigenschaft WPD- \_ Objekt \_ Name schreiben, um zu bestimmen, ob die Eigenschaft geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="08010-117">After this, the application retrieves the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value for the WPD\_OBJECT\_NAME property to determine whether the property can be written.</span></span> <span data-ttu-id="08010-118">(Beachten Sie, dass Ihre Anwendung jede Eigenschaft festlegen kann, für die die WPD \_ Das Eigenschafts \_ Attribut \_ kann den Wert "true" \_ schreiben.)</span><span class="sxs-lookup"><span data-stu-id="08010-118">(Note that your application could set any property for which the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value is true.)</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent interface
// to access the property-specific methods.
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 3) Check the property attributes to see if we can write/change the WPD_OBJECT_NAME property.
if (SUCCEEDED(hr))
{
    hr = pProperties->GetPropertyAttributes(szSelection,
                                            WPD_OBJECT_NAME,
                                            &pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
        if (SUCCEEDED(hr))
        {
            if (bCanWrite)
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports TRUE\nThis means that the property can be changed/updated\n\n");
            }
            else
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports FALSE\nThis means that the property cannot be changed/updated\n\n");
            }
        }
        else
        {
            printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value from WPD_OBJECT_NAME on object '%ws', hr = 0x%lx\n",szSelection, hr);
        }
    }
}
```



<span data-ttu-id="08010-119">Der nächste Schritt besteht darin, den Benutzer zur Eingabe der neuen Namens Zeichenfolge aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="08010-119">The next step is to prompt the user for the new name string.</span></span> <span data-ttu-id="08010-120">(Beachten Sie, dass durch den Aufrufen der [**iportabledevicevalues:: SetStringValue**](iportabledevicevalues-setstringvalue.md) -Methode lediglich der Eigenschaften Behälter erstellt wird. die tatsächliche Eigenschaft wurde noch nicht geschrieben.)</span><span class="sxs-lookup"><span data-stu-id="08010-120">(Note that the call to the [**IPortableDeviceValues::SetStringValue**](iportabledevicevalues-setstringvalue.md) method merely creates the property bag; the actual property has not been written yet.)</span></span>


```C++
if (bCanWrite)
{
    printf("Enter the new WPD_OBJECT_NAME for the object '%ws'.\n>",szSelection);
    hr = StringCbGetsW(szNewObjectName,sizeof(szNewObjectName));
    if (FAILED(hr))
    {
        printf("An invalid object name was specified, aborting property writing\n");
    }

    // 5) CoCreate an IPortableDeviceValues interface to hold the property values
    // we wish to write.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectPropertiesToWrite));
        if (SUCCEEDED(hr))
        {
            if (pObjectPropertiesToWrite != NULL)
            {
                hr = pObjectPropertiesToWrite->SetStringValue(WPD_OBJECT_NAME, szNewObjectName);
                if (FAILED(hr))
                {
                    printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceValues, hr= 0x%lx\n", hr);
                }
            }
        }
    }
```



<span data-ttu-id="08010-121">Schließlich wird der neue Wert, der vom Benutzer angegeben wird, auf das Objekt angewendet.</span><span class="sxs-lookup"><span data-stu-id="08010-121">Finally, the new value, specified by the user, is applied to the object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->SetValues(szSelection,                // The object whose properties we are reading
                                pObjectPropertiesToWrite,   // The properties we want to read
                                &pPropertyWriteResults);    // Driver supplied property result values for the property read operation
    if (FAILED(hr))
    {
        printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
    else
    {
        printf("The WPD_OBJECT_NAME property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", szSelection);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="08010-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08010-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08010-123">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08010-123">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="08010-124">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08010-124">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="08010-125">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08010-125">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="08010-126">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08010-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="08010-127">**Iportabledevicepropertiesbulk-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08010-127">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="08010-128">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="08010-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="08010-129">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="08010-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




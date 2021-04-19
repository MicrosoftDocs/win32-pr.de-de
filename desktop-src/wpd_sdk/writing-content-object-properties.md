---
description: Schreiben von Objekteigenschaften
ms.assetid: f762a571-83ea-4999-ad49-a51044bc790d
title: Schreiben von Objekteigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb061288cbfde93f2baea1860581c25c61a8a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353478"
---
# <a name="writing-object-properties"></a><span data-ttu-id="e2478-103">Schreiben von Objekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2478-103">Writing Object Properties</span></span>

<span data-ttu-id="e2478-104">Dienste enthalten häufig untergeordnete Objekte, die zu einem der Formate gehören, die von den einzelnen Diensten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e2478-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="e2478-105">Beispielsweise kann ein Kontakt Dienst mehrere Kontakt Objekte des abstrakten Kontakt Formats unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e2478-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="e2478-106">Alle Kontakt Objekte werden durch verwandte Eigenschaften (Kontakt Name, Telefonnummer, e-Mail-Adresse usw.) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e2478-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="e2478-107">Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung die Name-Eigenschaft für ein untergeordnetes Objekt des angegebenen Contacts-diensdienstanbieter aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="e2478-107">The WpdServicesApiSample application includes code that demonstrates how an application can update the name property for a child object of the given Contacts service.</span></span> <span data-ttu-id="e2478-108">In diesem Beispiel werden die folgenden WPD-Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2478-108">This sample uses the following WPD interfaces.</span></span>



|                                                                |                                                                                                                                                                      |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2478-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e2478-109">Interface</span></span>                                                      | <span data-ttu-id="e2478-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2478-110">Description</span></span>                                                                                                                                                          |
| [<span data-ttu-id="e2478-111">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="e2478-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)       | <span data-ttu-id="e2478-112">Dient zum Abrufen der **IPortableDeviceContent2** -Schnittstelle für den Zugriff auf die unterstützten Dienst Methoden.</span><span class="sxs-lookup"><span data-stu-id="e2478-112">Used to retrieve the **IPortableDeviceContent2** interface to access the supported service methods.</span></span>                                                                  |
| [<span data-ttu-id="e2478-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="e2478-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)     | <span data-ttu-id="e2478-114">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="e2478-114">Provides access to the content-specific methods.</span></span>                                                                                                                     |
| [<span data-ttu-id="e2478-115">**Iportabledeviceproperties**</span><span class="sxs-lookup"><span data-stu-id="e2478-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="e2478-116">Wird verwendet, um die Objekt Eigenschaftswerte zu schreiben und um zu bestimmen, ob eine bestimmte Eigenschaft geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2478-116">Used to write the object property values and to determine whether a given property can be written</span></span>                                                                    |
| [<span data-ttu-id="e2478-117">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="e2478-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="e2478-118">Wird verwendet, um die zu schreibenden Eigenschaftswerte zu speichern, die Ergebnisse des Schreibvorgangs zu bestimmen und Attribute von Eigenschaften abzurufen (beim Bestimmen der Schreibfunktion).</span><span class="sxs-lookup"><span data-stu-id="e2478-118">Used to hold the property values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="e2478-119">Wenn der Benutzer die Option "8" in der Befehlszeile auswählt, ruft die Anwendung die Methode " **schreitecontentproperties** " auf, die im Modul "contentproperties. cpp" zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="e2478-119">When the user chooses option "8" at the command line, the application invokes the **WriteContentProperties** method that is found in the ContentProperties.cpp module.</span></span> <span data-ttu-id="e2478-120">Diese Methode fordert den Benutzer auf, einen Objekt Bezeichner für die zu Aktualisier Ende Eigenschaft einzugeben.</span><span class="sxs-lookup"><span data-stu-id="e2478-120">This method prompts the user to enter an object identifier for the property to be updated.</span></span> <span data-ttu-id="e2478-121">Der Benutzer identifiziert das-Objekt, und die-Methode fordert den Benutzer auf, einen neuen Namen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e2478-121">The user identifies the object, and the method prompts the user to specify a new name.</span></span> <span data-ttu-id="e2478-122">Nachdem dieser Name angegeben wurde, wird die Name-Eigenschaft für das angegebene Objekt von der-Methode aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e2478-122">After this name is specified, the method updates the Name property for the given object.</span></span>

<span data-ttu-id="e2478-123">Beachten Sie, dass die Beispielanwendung vor dem Schreiben der Objekteigenschaften einen Contacts-Dienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="e2478-123">Note that prior to writing the object properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="e2478-124">Der folgende Code für die Methode " **Write-contentproperties** " veranschaulicht, wie die Anwendung mithilfe der [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) -Schnittstelle eine [**iportabledeviceproperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) -Schnittstelle abruft.</span><span class="sxs-lookup"><span data-stu-id="e2478-124">The following code for the **WriteContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="e2478-125">Durch übergeben der PropertyKeys der angeforderten Eigenschaften an die [**iportabledeviceproperties:: SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) -Methode aktualisiert " **Write-contentproperties** " die Name-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e2478-125">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **WriteContentProperties** updates the name property.</span></span>


```C++
void WriteContentProperties(
 IPortableDeviceService* pService)
{
 if (pService == NULL)
 {
  printf("! A NULL IPortableDeviceService interface pointer was received\n");
  return;
 }

 HRESULT          hr       = S_OK;
 WCHAR         wszSelection[81]  = {0};
 WCHAR         wszNewObjectName[81] = {0};
 CComPtr<IPortableDeviceProperties> pProperties;
 CComPtr<IPortableDeviceContent2>   pContent;
 CComPtr<IPortableDeviceValues>  pObjectPropertiesToWrite;
 CComPtr<IPortableDeviceValues>  pPropertyWriteResults;
 CComPtr<IPortableDeviceValues>  pAttributes;
 BOOL          bCanWrite   = FALSE;

 // Prompt user to enter an object identifier on the device to write properties on.
 printf("Enter the identifer of the object you wish to write properties on.\n>");
 hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
 if (FAILED(hr))
 {
  printf("An invalid object identifier was specified, aborting property reading\n");
 }

 // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
 // access the content-specific methods.
 if (SUCCEEDED(hr))
 {
  hr = pService->Content(&pContent);
  if (FAILED(hr))
  {
   printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
  }
 }

 // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
 // to access the property-specific methods.
 if (SUCCEEDED(hr))
 {
  hr = pContent->Properties(&pProperties);
  if (FAILED(hr))
  {
   printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
  }
 }

 // 3) Check the property attributes to see if we can write/change the NAME_GenericObj_Name property.
 if (SUCCEEDED(hr))
 {
  hr = pProperties->GetPropertyAttributes(wszSelection,
            PKEY_GenericObj_Name,
            &pAttributes);
  if (SUCCEEDED(hr))
  {
   hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
   if (SUCCEEDED(hr))
   {
    if (bCanWrite)
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports TRUE\nThis means that the property can be changed/updated\n\n");
    }
    else
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports FALSE\nThis means that the property cannot be changed/updated\n\n");
    }
   }
   else
   {
    printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value for PKEY_GenericObj_Name on object '%ws', hr = 0x%lx\n", wszSelection, hr);
   }
  }
 }

 // 4) Prompt the user for the new value of the NAME_GenericObj_Name property only if the property attributes report
 // that it can be changed/updated.
 if (bCanWrite)
 {
  printf("Enter the new PKEY_GenericObj_Name property for the object '%ws'.\n>",wszSelection);
  hr = StringCbGetsW(wszNewObjectName,sizeof(wszNewObjectName));
  if (FAILED(hr))
  {
   printf("An invalid PKEY_GenericObj_Name was specified, aborting property writing\n");
  }

  // 5) CoCreate an IPortableDeviceValues interface to hold the property values
  // we wish to write.
  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(CLSID_PortableDeviceValues,
          NULL,
          CLSCTX_INPROC_SERVER,
          IID_IPortableDeviceValues,
          (VOID**) &pObjectPropertiesToWrite);
   if (SUCCEEDED(hr))
   {
    if (pObjectPropertiesToWrite != NULL)
    {
     hr = pObjectPropertiesToWrite->SetStringValue(PKEY_GenericObj_Name, wszNewObjectName);
     if (FAILED(hr))
     {
      printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceValues, hr= 0x%lx\n", hr);
     }
    }
   }
  }

  // 6) Call SetValues() passing the collection of specified PROPERTYKEYs.
  if (SUCCEEDED(hr))
  {
   hr = pProperties->SetValues(wszSelection,      // The object whose properties we are reading
          pObjectPropertiesToWrite,   // The properties we want to read
          &pPropertyWriteResults); // Driver supplied property result values for the property read operation
   if (FAILED(hr))
   {
    printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", wszSelection, hr);
   }
   else
   {
    printf("The PKEY_GenericObj_Name property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", wszSelection);
   }
  }
 }
}
```



## <a name="related-topics"></a><span data-ttu-id="e2478-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2478-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2478-127">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="e2478-127">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="e2478-128">**Iportabledeviceproperties**</span><span class="sxs-lookup"><span data-stu-id="e2478-128">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="e2478-129">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="e2478-129">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




---
title: Abrufen von WPD-Objekteigenschaften
description: Die WpdServiceApiSample-Anwendung veranschaulicht, wie eine Anwendung die Inhaltsobjekteigenschaften abrufen kann, die von einem bestimmten Contacts-Dienst unterstützt werden.
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e57258993d0a81f68042195db2caf338c97c53
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404313"
---
# <a name="retrieving-wpd-object-properties"></a><span data-ttu-id="40bee-103">Abrufen von WPD-Objekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="40bee-103">Retrieving WPD object properties</span></span>

<span data-ttu-id="40bee-104">Dienste enthalten häufig untergeordnete Objekte, die zu einem der Formate gehören, die von jedem Dienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="40bee-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="40bee-105">Ein Contacts-Dienst kann beispielsweise mehrere Kontaktobjekte im Abstrakten Kontaktformat unterstützen.</span><span class="sxs-lookup"><span data-stu-id="40bee-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="40bee-106">Jedes Kontaktobjekt wird durch verwandte Eigenschaften (Kontaktname, Telefonnummer, E-Mail-Adresse und ähnliches) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="40bee-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="40bee-107">Die WpdServiceApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die Inhaltsobjekteigenschaften abrufen kann, die von einem bestimmten Contacts-Dienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="40bee-107">The WpdServiceApiSample application includes code that demonstrates how an application can retrieve the content-object properties supported by a given Contacts service.</span></span> <span data-ttu-id="40bee-108">In diesem Beispiel werden die folgenden Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="40bee-108">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="40bee-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="40bee-109">Interface</span></span> | <span data-ttu-id="40bee-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40bee-110">Description</span></span>    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40bee-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="40bee-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="40bee-112">Ruft die **IPortableDeviceContent2-Schnittstelle ab, um** auf die unterstützten Dienstmethoden zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="40bee-112">Retrieves the **IPortableDeviceContent2** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="40bee-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="40bee-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="40bee-114">Ermöglicht den Zugriff auf die inhaltsspezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="40bee-114">Provides access to the content-specific methods.</span></span>                                             |
| [<span data-ttu-id="40bee-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="40bee-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | <span data-ttu-id="40bee-116">Ruft die Objekteigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="40bee-116">Retrieves the object property values.</span></span>                                                        |
| [<span data-ttu-id="40bee-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="40bee-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)               | <span data-ttu-id="40bee-118">Enthält die Eigenschaftswerte, die für dieses Objekt gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="40bee-118">Holds the property values that were read for that object.</span></span>                                    |
| [<span data-ttu-id="40bee-119">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="40bee-119">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md) | <span data-ttu-id="40bee-120">Enthält die Parameter für eine bestimmte Methode.</span><span class="sxs-lookup"><span data-stu-id="40bee-120">Contains the parameters for a given method.</span></span>                                                  |



 

<span data-ttu-id="40bee-121">Wenn der Benutzer die Option "7" in der Befehlszeile auswählt, ruft die Anwendung die **ReadContentProperties-Methode** auf, die sich im ContentProperties.cpp-Modul befindet.</span><span class="sxs-lookup"><span data-stu-id="40bee-121">When the user chooses option "7" at the command line, the application invokes the **ReadContentProperties** method that is found in the ContentProperties.cpp module.</span></span>

<span data-ttu-id="40bee-122">Diese Methode ruft die folgenden vier Eigenschaften für das angegebene Kontaktobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="40bee-122">This method retrieves the following four properties for the specified contact object.</span></span>



| <span data-ttu-id="40bee-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="40bee-123">Property</span></span>                     | <span data-ttu-id="40bee-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40bee-124">Description</span></span>                                                                                                                                                                                                      | <span data-ttu-id="40bee-125">Device Services PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="40bee-125">Device Services PROPERTYKEY</span></span>     | <span data-ttu-id="40bee-126">Entsprechende WPD \_ PROPERTYKEY-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="40bee-126">Equivalent WPD\_PROPERTYKEY</span></span>         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| <span data-ttu-id="40bee-127">Bezeichner des übergeordneten Objekts</span><span class="sxs-lookup"><span data-stu-id="40bee-127">Parent-object identifier</span></span>     | <span data-ttu-id="40bee-128">Eine Zeichenfolge, die den Bezeichner für das übergeordnete Element des angegebenen Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="40bee-128">A string that specifies the identifier for the given object's parent.</span></span>                                                                                                                                            | <span data-ttu-id="40bee-129">PKEY \_ GenericObj \_ ParentID</span><span class="sxs-lookup"><span data-stu-id="40bee-129">PKEY\_GenericObj\_ParentID</span></span>      | <span data-ttu-id="40bee-130">ÜBERGEORDNETE ID \_ DES WPD-OBJEKTS \_ \_</span><span class="sxs-lookup"><span data-stu-id="40bee-130">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="40bee-131">Objektname</span><span class="sxs-lookup"><span data-stu-id="40bee-131">Object name</span></span>                  | <span data-ttu-id="40bee-132">Eine Zeichenfolge, die den Namen des angegebenen Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="40bee-132">A string that specifies the name of the given object</span></span>                                                                                                                                                             | <span data-ttu-id="40bee-133">PKEY \_ \_ GenericObj-Name</span><span class="sxs-lookup"><span data-stu-id="40bee-133">PKEY\_GenericObj\_Name</span></span>          | <span data-ttu-id="40bee-134">\_WPD-OBJEKTNAME \_</span><span class="sxs-lookup"><span data-stu-id="40bee-134">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="40bee-135">Persistenter eindeutiger Bezeichner</span><span class="sxs-lookup"><span data-stu-id="40bee-135">Persistent unique identifier</span></span> | <span data-ttu-id="40bee-136">Eine Zeichenfolge, die einen eindeutigen Bezeichner für das gegebene Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="40bee-136">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="40bee-137">Dieser Bezeichner ist im Gegensatz zum Objektbezeichner sitzungsübergreifend persistent.</span><span class="sxs-lookup"><span data-stu-id="40bee-137">This identifier is persistent across sessions, unlike the object identifier.</span></span> <span data-ttu-id="40bee-138">Bei Diensten muss dies eine Zeichenfolgendarstellung einer GUID sein.</span><span class="sxs-lookup"><span data-stu-id="40bee-138">For services, this needs to be a string-representation of a GUID.</span></span> | <span data-ttu-id="40bee-139">PKEY \_ GenericObj \_ PersistentUID</span><span class="sxs-lookup"><span data-stu-id="40bee-139">PKEY\_GenericObj\_PersistentUID</span></span> | <span data-ttu-id="40bee-140">PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="40bee-140">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="40bee-141">Objektformat</span><span class="sxs-lookup"><span data-stu-id="40bee-141">Object format</span></span>                | <span data-ttu-id="40bee-142">Ein GUID (Globally Unique Identifier), der das Format der Datei angibt, die einem bestimmten Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="40bee-142">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object</span></span>                                                                                                        | <span data-ttu-id="40bee-143">PKEY \_ GenericObj \_ ObjectFormat</span><span class="sxs-lookup"><span data-stu-id="40bee-143">PKEY\_GenericObj\_ObjectFormat</span></span>  | <span data-ttu-id="40bee-144">\_WPD-OBJEKTFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="40bee-144">WPD\_OBJECT\_FORMAT</span></span>                 |



 

-   <span data-ttu-id="40bee-145">Übergeordnete ID</span><span class="sxs-lookup"><span data-stu-id="40bee-145">Parent ID</span></span>
-   <span data-ttu-id="40bee-146">Name</span><span class="sxs-lookup"><span data-stu-id="40bee-146">Name</span></span>
-   <span data-ttu-id="40bee-147">PersistentUID</span><span class="sxs-lookup"><span data-stu-id="40bee-147">PersistentUID</span></span>
-   <span data-ttu-id="40bee-148">Format</span><span class="sxs-lookup"><span data-stu-id="40bee-148">Format</span></span>

<span data-ttu-id="40bee-149">Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Inhaltseigenschaften einen Kontaktdienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="40bee-149">Note that prior to retrieving the content properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="40bee-150">Der folgende Code für die **ReadContentProperties-Methode** veranschaulicht, wie die Anwendung die [**IPortableDeviceContent2-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) verwendet, um eine [**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="40bee-150">The following code for the **ReadContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="40bee-151">Durch Übergeben der PROPERTYKEYS der angeforderten Eigenschaften an die [**IPortableDeviceProperties::GetValues-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) ruft **ReadContentProperties** die angeforderten Werte ab und zeigt sie dann im Konsolenfenster an.</span><span class="sxs-lookup"><span data-stu-id="40bee-151">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **ReadContentProperties** retrieves the requested values, and then displays them to the console window.</span></span>


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
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

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
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
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
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

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="40bee-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40bee-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40bee-153">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="40bee-153">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="40bee-154">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="40bee-154">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="40bee-155">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="40bee-155">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




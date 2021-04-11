---
title: Abrufen von WPD-Objekteigenschaften
description: Abrufen von Objekteigenschaften
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3c6eba4435b23ef5c637feaca7c2d4ab6b160e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042712"
---
# <a name="retrieving-wpd-object-properties"></a><span data-ttu-id="548cc-103">Abrufen von WPD-Objekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="548cc-103">Retrieving WPD object properties</span></span>

<span data-ttu-id="548cc-104">Dienste enthalten häufig untergeordnete Objekte, die zu einem der Formate gehören, die von den einzelnen Diensten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="548cc-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="548cc-105">Beispielsweise kann ein Kontakt Dienst mehrere Kontakt Objekte des abstrakten Kontakt Formats unterstützen.</span><span class="sxs-lookup"><span data-stu-id="548cc-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="548cc-106">Alle Kontakt Objekte werden durch verwandte Eigenschaften (Kontakt Name, Telefonnummer, e-Mail-Adresse usw.) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="548cc-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="548cc-107">Die Anwendung wpdserviceapisample enthält Code, der veranschaulicht, wie eine Anwendung die Inhalts Objekteigenschaften abrufen kann, die von einem bestimmten Kontakt Dienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="548cc-107">The WpdServiceApiSample application includes code that demonstrates how an application can retrieve the content-object properties supported by a given Contacts service.</span></span> <span data-ttu-id="548cc-108">In diesem Beispiel werden die folgenden Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="548cc-108">This sample uses the following interfaces.</span></span>



|                                                                      |                                                                                              |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="548cc-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="548cc-109">Interface</span></span>                                                            | <span data-ttu-id="548cc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="548cc-110">Description</span></span>                                                                                  |
| [<span data-ttu-id="548cc-111">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="548cc-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="548cc-112">Ruft die **IPortableDeviceContent2** -Schnittstelle für den Zugriff auf die unterstützten Dienst Methoden ab.</span><span class="sxs-lookup"><span data-stu-id="548cc-112">Retrieves the **IPortableDeviceContent2** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="548cc-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="548cc-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="548cc-114">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="548cc-114">Provides access to the content-specific methods.</span></span>                                             |
| [<span data-ttu-id="548cc-115">**Iportabledeviceproperties**</span><span class="sxs-lookup"><span data-stu-id="548cc-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | <span data-ttu-id="548cc-116">Ruft die Objekt Eigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="548cc-116">Retrieves the object property values.</span></span>                                                        |
| [<span data-ttu-id="548cc-117">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="548cc-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)               | <span data-ttu-id="548cc-118">Enthält die Eigenschaftswerte, die für dieses Objekt gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="548cc-118">Holds the property values that were read for that object.</span></span>                                    |
| [<span data-ttu-id="548cc-119">**Iportabledevicekeycollection**</span><span class="sxs-lookup"><span data-stu-id="548cc-119">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md) | <span data-ttu-id="548cc-120">Enthält die Parameter für eine bestimmte Methode.</span><span class="sxs-lookup"><span data-stu-id="548cc-120">Contains the parameters for a given method.</span></span>                                                  |



 

<span data-ttu-id="548cc-121">Wenn der Benutzer die Option "7" in der Befehlszeile auswählt, ruft die Anwendung die Methode "read **contentproperties** " auf, die im Modul "contentproperties. cpp" zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="548cc-121">When the user chooses option "7" at the command line, the application invokes the **ReadContentProperties** method that is found in the ContentProperties.cpp module.</span></span>

<span data-ttu-id="548cc-122">Diese Methode ruft die folgenden vier Eigenschaften für das angegebene Contact-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="548cc-122">This method retrieves the following four properties for the specified contact object.</span></span>



|                              |                                                                                                                                                                                                                  |                                 |                                     |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| <span data-ttu-id="548cc-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="548cc-123">Property</span></span>                     | <span data-ttu-id="548cc-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="548cc-124">Description</span></span>                                                                                                                                                                                                      | <span data-ttu-id="548cc-125">PropertyKey für Geräte Dienste</span><span class="sxs-lookup"><span data-stu-id="548cc-125">Device Services PROPERTYKEY</span></span>     | <span data-ttu-id="548cc-126">Äquivalenter WPD \_ PropertyKey</span><span class="sxs-lookup"><span data-stu-id="548cc-126">Equivalent WPD\_PROPERTYKEY</span></span>         |
| <span data-ttu-id="548cc-127">Übergeordnete Objekt Kennung</span><span class="sxs-lookup"><span data-stu-id="548cc-127">Parent-object identifier</span></span>     | <span data-ttu-id="548cc-128">Eine Zeichenfolge, die den Bezeichner für das übergeordnete Objekt des angegebenen-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="548cc-128">A string that specifies the identifier for the given object's parent.</span></span>                                                                                                                                            | <span data-ttu-id="548cc-129">Pkey \_ genericobj \_ -Element-ID</span><span class="sxs-lookup"><span data-stu-id="548cc-129">PKEY\_GenericObj\_ParentID</span></span>      | <span data-ttu-id="548cc-130">übergeordnete WPD- \_ Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="548cc-130">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="548cc-131">Objektname</span><span class="sxs-lookup"><span data-stu-id="548cc-131">Object name</span></span>                  | <span data-ttu-id="548cc-132">Eine Zeichenfolge, die den Namen des angegebenen Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="548cc-132">A string that specifies the name of the given object</span></span>                                                                                                                                                             | <span data-ttu-id="548cc-133">Name des pkey- \_ genericobj \_</span><span class="sxs-lookup"><span data-stu-id="548cc-133">PKEY\_GenericObj\_Name</span></span>          | <span data-ttu-id="548cc-134">WPD- \_ Objekt \_ Name</span><span class="sxs-lookup"><span data-stu-id="548cc-134">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="548cc-135">Persistente eindeutige Kennung</span><span class="sxs-lookup"><span data-stu-id="548cc-135">Persistent unique identifier</span></span> | <span data-ttu-id="548cc-136">Eine Zeichenfolge, die einen eindeutigen Bezeichner für das angegebene Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="548cc-136">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="548cc-137">Dieser Bezeichner ist im Gegensatz zum Objekt Bezeichner Sitzungs übergreifend persistent.</span><span class="sxs-lookup"><span data-stu-id="548cc-137">This identifier is persistent across sessions, unlike the object identifier.</span></span> <span data-ttu-id="548cc-138">Bei-Diensten muss dies eine Zeichen folgen Darstellung einer GUID sein.</span><span class="sxs-lookup"><span data-stu-id="548cc-138">For services, this needs to be a string-representation of a GUID.</span></span> | <span data-ttu-id="548cc-139">Pkey- \_ genericobj \_ persistentuid</span><span class="sxs-lookup"><span data-stu-id="548cc-139">PKEY\_GenericObj\_PersistentUID</span></span> | <span data-ttu-id="548cc-140">\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt</span><span class="sxs-lookup"><span data-stu-id="548cc-140">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="548cc-141">Objekt Format</span><span class="sxs-lookup"><span data-stu-id="548cc-141">Object format</span></span>                | <span data-ttu-id="548cc-142">Eine Globally Unique Identifier (GUID), die das Format der Datei angibt, die einem bestimmten Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="548cc-142">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object</span></span>                                                                                                        | <span data-ttu-id="548cc-143">Pkey- \_ genericobj- \_ ObjectFormat</span><span class="sxs-lookup"><span data-stu-id="548cc-143">PKEY\_GenericObj\_ObjectFormat</span></span>  | <span data-ttu-id="548cc-144">WPD- \_ Objekt \_ Format</span><span class="sxs-lookup"><span data-stu-id="548cc-144">WPD\_OBJECT\_FORMAT</span></span>                 |



 

-   <span data-ttu-id="548cc-145">Übergeordnete ID</span><span class="sxs-lookup"><span data-stu-id="548cc-145">Parent ID</span></span>
-   <span data-ttu-id="548cc-146">Name</span><span class="sxs-lookup"><span data-stu-id="548cc-146">Name</span></span>
-   <span data-ttu-id="548cc-147">Persistentuid</span><span class="sxs-lookup"><span data-stu-id="548cc-147">PersistentUID</span></span>
-   <span data-ttu-id="548cc-148">Format</span><span class="sxs-lookup"><span data-stu-id="548cc-148">Format</span></span>

<span data-ttu-id="548cc-149">Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Inhalts Eigenschaften einen Kontakt Dienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="548cc-149">Note that prior to retrieving the content properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="548cc-150">Der folgende Code für die Methode "read **contentproperties** " veranschaulicht, wie die Anwendung mithilfe der [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) -Schnittstelle eine [**iportabledeviceproperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) -Schnittstelle abruft.</span><span class="sxs-lookup"><span data-stu-id="548cc-150">The following code for the **ReadContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="548cc-151">Indem die PropertyKeys der angeforderten Eigenschaften an die [**iportabledeviceproperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) -Methode übergeben werden, ruft "read **contentproperties** " die angeforderten Werte ab und zeigt Sie dann im Konsolenfenster an.</span><span class="sxs-lookup"><span data-stu-id="548cc-151">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **ReadContentProperties** retrieves the requested values, and then displays them to the console window.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="548cc-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="548cc-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="548cc-153">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="548cc-153">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="548cc-154">**Iportabledeviceproperties**</span><span class="sxs-lookup"><span data-stu-id="548cc-154">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="548cc-155">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="548cc-155">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




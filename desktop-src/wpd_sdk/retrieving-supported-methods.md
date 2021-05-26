---
description: Abrufen unterstützter Dienstmethoden
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Abrufen unterstützter Dienstmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b021aa868ffaa95df23a729e94d62eae8a0c632e
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423800"
---
# <a name="retrieving-supported-service-methods"></a><span data-ttu-id="d8ed2-103">Abrufen unterstützter Dienstmethoden</span><span class="sxs-lookup"><span data-stu-id="d8ed2-103">Retrieving Supported Service Methods</span></span>

<span data-ttu-id="d8ed2-104">Dienstmethoden kapseln Funktionen, die jeder Dienst definiert und implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-104">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="d8ed2-105">Sie sind spezifisch für jeden Diensttyp und werden durch eine eindeutige GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-105">They are specific to each type of service type and are represented by a unique GUID.</span></span>

<span data-ttu-id="d8ed2-106">Beispielsweise definiert der Contacts-Dienst eine **BeginSync-Methode,** die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Contact-Objekten vorzubereiten, und eine **EndSync-Methode,** um das Gerät über den Abschluss der Synchronisierung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-106">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span>

<span data-ttu-id="d8ed2-107">Anwendungen können die unterstützten Methoden programmgesteuert abfragen und mithilfe der [**IPortableDeviceServiceCapabilities-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) auf diese Methoden und ihre Attribute zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-107">Applications can programmatically query the supported methods and access these methods and their attributes by using the [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span>

<span data-ttu-id="d8ed2-108">Dienstmethoden dürfen nicht mit WPD-Befehlen verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-108">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="d8ed2-109">WPD-Befehle sind Teil der standardmäßigen WPD-Gerätetreiberschnittstelle (DDI) und der Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-109">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="d8ed2-110">Befehle sind vordefiniert, nach Kategorien gruppiert, z. B. WPD \_ CATEGORY \_ COMMON, und werden durch eine PROPERTYKEY-Struktur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-110">Commands are predefined, grouped by categories, for example, WPD\_CATEGORY\_COMMON, and are represented by a PROPERTYKEY structure.</span></span> <span data-ttu-id="d8ed2-111">Weitere Informationen finden Sie im Thema [**Befehle.**](commands.md)</span><span class="sxs-lookup"><span data-stu-id="d8ed2-111">For more information, see the [**Commands**](commands.md) topic.</span></span>

<span data-ttu-id="d8ed2-112">Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Contacts-Dienst unterstützten Methoden mithilfe der Schnittstellen in der folgenden Tabelle abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-112">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the methods supported by a given Contacts service by using the interfaces in the following table.</span></span>



| <span data-ttu-id="d8ed2-113">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d8ed2-113">Interface</span></span>      | <span data-ttu-id="d8ed2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8ed2-114">Description</span></span>         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8ed2-115">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="d8ed2-115">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="d8ed2-116">Wird verwendet, um die **IPortableDeviceServiceCapabilities-Schnittstelle** abzurufen, um auf die unterstützten Dienstmethoden zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-116">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="d8ed2-117">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d8ed2-117">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="d8ed2-118">Bietet Zugriff auf die unterstützten Methoden, Methodenattribute und Methodenparameter.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-118">Provides access to the supported methods, method attributes and method parameters.</span></span>                             |
| [<span data-ttu-id="d8ed2-119">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="d8ed2-119">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="d8ed2-120">Enthält die Liste der unterstützten Methoden.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-120">Contains the list of supported methods.</span></span>                                                                        |
| [<span data-ttu-id="d8ed2-121">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d8ed2-121">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="d8ed2-122">Enthält die Attribute für eine Methode und für die Parameter einer bestimmten Methode.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-122">Contains the attributes for a method and for a given method's parameters.</span></span>                                      |
| [<span data-ttu-id="d8ed2-123">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="d8ed2-123">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="d8ed2-124">Enthält die Parameter für eine bestimmte Methode.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-124">Contains the parameters for a given method.</span></span>                                                                    |



 

<span data-ttu-id="d8ed2-125">Wenn der Benutzer die Option "5" in der Befehlszeile auswählt, ruft die Anwendung die **ListSupportedMethods-Methode** auf, die sich im Modul ServiceMethods.cpp befindet.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-125">When the user chooses option "5" at the command line, the application invokes the **ListSupportedMethods** method that is found in the ServiceMethods.cpp module.</span></span>

<span data-ttu-id="d8ed2-126">Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontaktdienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-126">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="d8ed2-127">In WPD wird eine Methode durch ihren Namen, Zugriffsrechte, Parameter und zugehörige Daten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-127">In WPD, a method is described by its name, access rights, parameters, and related data.</span></span> <span data-ttu-id="d8ed2-128">Die Beispielanwendung zeigt einen benutzerfreundlichen Namen an, z. B. "CustomMethod" oder eine GUID.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-128">The sample application displays a user-friendly name, for example, "CustomMethod", or a GUID.</span></span> <span data-ttu-id="d8ed2-129">Auf den Methodennamen oder die GUID folgen Zugriffsdaten ("Lesen/Schreiben"), der Name jedes zugeordneten Formats und die Parameterdaten.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-129">The method name or GUID is followed by access data ("Read/Write"), the name of any associated format, and the parameter data.</span></span> <span data-ttu-id="d8ed2-130">Diese Daten umfassen den Parameternamen, die Verwendung, VARTYPE und das Formular.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-130">This data includes the parameter name, usage, VARTYPE, and form.</span></span>

<span data-ttu-id="d8ed2-131">Fünf Methoden im Modul ServiceMethods.cpp unterstützen das Abrufen von Methoden (und zugehörigen Daten) für den angegebenen Contacts-Dienst: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat** und **DisplayMethodParameters**.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-131">Five methods in the ServiceMethods.cpp module support the retrieval of methods (and related data) for the given Contacts service: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters**.</span></span> <span data-ttu-id="d8ed2-132">Die **ListSupportedMethods-Methode** ruft jeweils die Anzahl der unterstützten Methoden und den GUID-Bezeichner ab. anschließend wird die **DisplayMethod-Methode** aufruft.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-132">The **ListSupportedMethods** method retrieves a count of supported methods and the GUID identifier for each; it then calls the **DisplayMethod** method.</span></span> <span data-ttu-id="d8ed2-133">Die **DisplayMethod-Methode** ruft die [**IPortableDeviceServiceCapapbilities::GetMethodAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) auf, um die Optionen, Parameter und so weiter der angegebenen Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-133">The **DisplayMethod** method calls the [**IPortableDeviceServiceCapapbilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve the given method's options, parameters, and so on.</span></span> <span data-ttu-id="d8ed2-134">Nachdem **die DisplayMethod** die Methodendaten abgerufen hat, rendert sie den Namen (oder die GUID), die Zugriffseinschränkungen, das zugeordnete Format (falls verfügbar) und die Parameterbeschreibungen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-134">After the **DisplayMethod** retrieves the method data, it renders the name (or GUID), the access restrictions, the associated format (if any), and the parameter descriptions.</span></span> <span data-ttu-id="d8ed2-135">Die **DisplayMethodAccess-,** **DisplayFormat-** und **DisplayMethodParameters** sind Hilfsfunktionen, die ihre jeweiligen Datenfelder rendern.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-135">The **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** are helper functions that render their respective fields of data.</span></span>

<span data-ttu-id="d8ed2-136">Die **ListSupportedMethods-Methode** ruft die [**IPortableDeviceService::Capabilities-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**IPortableDeviceServiceCapabilities-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-136">The **ListSupportedMethods** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="d8ed2-137">Mit dieser Schnittstelle werden die unterstützten Methoden abgerufen, indem die [**IPortableDeviceServiceCapabilities::GetSupportedMethods-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-137">Using this interface, it retrieves the supported methods by calling the [**IPortableDeviceServiceCapabilities::GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="d8ed2-138">Die **GetSupportedMethods-Methode** ruft die GUIDs für jede vom Dienst unterstützte Methode ab und kopiert diese GUID in ein [**IPortableDevicePropVariantCollection-Objekt.**](iportabledevicepropvariantcollection.md)</span><span class="sxs-lookup"><span data-stu-id="d8ed2-138">The **GetSupportedMethods** method retrieves the GUIDs for each method supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="d8ed2-139">Im folgenden Code wird die **ListSupportedMethods-Methode** verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-139">The following code uses the **ListSupportedMethods** method.</span></span>


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



<span data-ttu-id="d8ed2-140">Nachdem die **ListSupportedMethods-Methode** die GUID für jedes vom angegebenen Dienst unterstützte Ereignis abgerufen hat, ruft sie die **DisplayMethod-Methode** auf, um die methodenspezifischen Attribute abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-140">After the **ListSupportedMethods** method retrieves the GUID for each event supported by the given service, it invokes the **DisplayMethod** method to retrieve the method-specific attributes.</span></span> <span data-ttu-id="d8ed2-141">Zu diesen Attributen gehören: der Skript-Anzeigename der Methode, erforderliche Zugriffseinschränkungen, jedes zugeordnete Format und eine Liste von Parametern.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-141">These attributes include: the method's script-friendly name , required access restrictions, any associated format, and list of parameters.</span></span>

<span data-ttu-id="d8ed2-142">Die **DisplayMethod-Methode** ruft die [**IPortableDeviceServiceCapabilities::GetMethodAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) auf, um eine Auflistung von Attributen für die angegebene Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-142">The **DisplayMethod** method invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve a collection of attributes for the given method.</span></span> <span data-ttu-id="d8ed2-143">Anschließend wird die [**IPortableDeviceValues::GetStringValue-Methode**](iportabledevicevalues-getstringvalue.md) aufgerufen, um den Namen der Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-143">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method to retrieve the method's name.</span></span> <span data-ttu-id="d8ed2-144">**DisplayMethod** ruft [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) auf, um die Zugriffs-Restrctions abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-144">The **DisplayMethod** calls the [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) to retrieve the access restrctions.</span></span> <span data-ttu-id="d8ed2-145">Danach wird [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) aufgerufen, um alle zugeordneten Formate abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-145">After this, it calls [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) to retrieve any associated format.</span></span> <span data-ttu-id="d8ed2-146">Schließlich ruft **displayMethod** den [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) auf, um die Parameterdaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-146">And, finally, the **DisplayMethod** calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the parameter data.</span></span> <span data-ttu-id="d8ed2-147">Die von diesen Methoden zurückgegebenen Daten werden an die Hilfsfunktionen **DisplayMethodAccess,** **DisplayFormat** und **DisplayMethodParameters** übergeben, die die Informationen für die angegebene Methode rendern.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-147">It passes the data returned by these methods to the **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** helper functions, which render the information for the given method.</span></span>

<span data-ttu-id="d8ed2-148">Im folgenden Code wird die **DisplayMethod-Methode** verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-148">The following code uses the **DisplayMethod** method.</span></span>


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



<span data-ttu-id="d8ed2-149">Die **DisplayMethodAccess-Hilfsfunktion** empfängt einen DWORD-Wert, der die Zugriffsoptionen der Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-149">The **DisplayMethodAccess** helper function receives a DWORD value that contains the method's access options.</span></span> <span data-ttu-id="d8ed2-150">Dieser Wert wird mit WPD \_ COMMAND ACCESS READ und \_ \_ WPD COMMAND ACCESS \_ \_ \_ READWRITE verglichen, um die Zugriffsrechte der Methode zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-150">It compares this value to WPD\_COMMAND\_ACCESS\_READ and WPD\_COMMAND\_ACCESS\_READWRITE to determine the method's access privilege.</span></span> <span data-ttu-id="d8ed2-151">Mithilfe des Ergebnisses wird eine Zeichenfolge gerendert, die die Zugriffseinschränkung für die gegebene Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-151">Using the result, it renders a string indicating the access restriction for the given method.</span></span>

<span data-ttu-id="d8ed2-152">Im folgenden Code wird die **Hilfsfunktion DisplayMethodAccess** verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-152">The following code uses the **DisplayMethodAccess** helper function.</span></span>


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



<span data-ttu-id="d8ed2-153">Die **DisplayMethod-Hilfsfunktion** empfängt ein [**IPortableDeviceServiceCapabilities-Objekt**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) und die GUID der Methode als Parameter.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-153">The **DisplayMethod** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object and the method's GUID as parameters.</span></span> <span data-ttu-id="d8ed2-154">Mithilfe des **IPortableDeviceServiceCapabilities-Objekts** wird die [**IPortableDeviceServiceCapabilities::GetMethodAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) aufgerufen, um die Methodenattribute abzurufen und im Konsolenfenster der Anwendung zu rendern.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-154">Using the **IPortableDeviceServiceCapabilities** object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method to retrieve the method attributes and render them in the application's console window.</span></span>

<span data-ttu-id="d8ed2-155">Die **Hilfsfunktion DisplayMethodParameters** empfängt ein [**IPortableDeviceServiceCapabilities-Objekt,**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) die GUID der Methode und ein IPortableDeviceKeyCollection-Objekt, das die Methodenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-155">The **DisplayMethodParameters** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object, the method's GUID, and an IPortableDeviceKeyCollection object containing the method parameters.</span></span> <span data-ttu-id="d8ed2-156">Mithilfe des [**IPortableDeviceKeyCollection-Objekts**](iportabledevicekeycollection.md) wird die [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) aufgerufen, um den Namen, die Verwendung, den VARTYPE und das Formular des Parameters abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-156">Using the [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) method to retrieve the parameter's name, usage, VARTYPE, and form.</span></span> <span data-ttu-id="d8ed2-157">Diese Informationen werden im Konsolenfenster der Anwendung gerendert.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-157">It renders this information in the application's console window.</span></span>

<span data-ttu-id="d8ed2-158">Im folgenden Code wird die **DisplayMethodParameters-Hilfsfunktion** verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8ed2-158">The following code uses the **DisplayMethodParameters** helper function.</span></span>


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="d8ed2-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8ed2-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8ed2-160">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="d8ed2-160">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="d8ed2-161">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="d8ed2-161">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="d8ed2-162">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d8ed2-162">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="d8ed2-163">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d8ed2-163">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d8ed2-164">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="d8ed2-164">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




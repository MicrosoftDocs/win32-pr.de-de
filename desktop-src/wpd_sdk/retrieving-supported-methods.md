---
description: Abrufen unterstützter Dienst Methoden
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Abrufen unterstützter Dienst Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6029af655a8835a4eee887d919c534856062ff13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866503"
---
# <a name="retrieving-supported-service-methods"></a><span data-ttu-id="bd52c-103">Abrufen unterstützter Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="bd52c-103">Retrieving Supported Service Methods</span></span>

<span data-ttu-id="bd52c-104">Dienst Methoden Kapseln Funktionen, die von den einzelnen Diensten definiert und implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd52c-104">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="bd52c-105">Sie sind spezifisch für jeden Diensttyp und werden durch eine eindeutige GUID dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bd52c-105">They are specific to each type of service type and are represented by a unique GUID.</span></span>

<span data-ttu-id="bd52c-106">Der Kontakt Dienst definiert z. b. eine **BeginSync** -Methode, die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Kontakt Objekten vorzubereiten, und eine **EndSync** -Methode, um das Gerät zu benachrichtigen, dass die Synchronisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bd52c-106">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span>

<span data-ttu-id="bd52c-107">Anwendungen können die unterstützten Methoden Programm gesteuert Abfragen und mithilfe der [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Schnittstelle auf diese Methoden und deren Attribute zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-107">Applications can programmatically query the supported methods and access these methods and their attributes by using the [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span>

<span data-ttu-id="bd52c-108">Dienst Methoden sollten nicht mit WPD-Befehlen verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="bd52c-108">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="bd52c-109">WPD-Befehle sind Teil der standardmäßigen WPD-Gerätetreiber Schnittstelle (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar.</span><span class="sxs-lookup"><span data-stu-id="bd52c-109">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="bd52c-110">Befehle sind vordefiniert, gruppiert nach Kategorien, z. b. \_ die WPD \_ -Kategorie Common, und werden durch eine PropertyKey-Struktur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bd52c-110">Commands are predefined, grouped by categories, for example, WPD\_CATEGORY\_COMMON, and are represented by a PROPERTYKEY structure.</span></span> <span data-ttu-id="bd52c-111">Weitere Informationen finden Sie im Thema " [**Befehle**](commands.md) ".</span><span class="sxs-lookup"><span data-stu-id="bd52c-111">For more information, see the [**Commands**](commands.md) topic.</span></span>

<span data-ttu-id="bd52c-112">Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Kontakt Dienst unterstützten Methoden mithilfe der Schnittstellen in der folgenden Tabelle abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="bd52c-112">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the methods supported by a given Contacts service by using the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd52c-113">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bd52c-113">Interface</span></span>                                                                            | <span data-ttu-id="bd52c-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd52c-114">Description</span></span>                                                                                                    |
| [<span data-ttu-id="bd52c-115">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="bd52c-115">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="bd52c-116">Dient zum Abrufen der **iportabledeviceservicecapabili-** Schnittstelle für den Zugriff auf die unterstützten Dienst Methoden.</span><span class="sxs-lookup"><span data-stu-id="bd52c-116">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="bd52c-117">**Iportablede viceservicecapabili**</span><span class="sxs-lookup"><span data-stu-id="bd52c-117">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="bd52c-118">Bietet Zugriff auf die unterstützten Methoden, Methoden Attribute und Methoden Parameter.</span><span class="sxs-lookup"><span data-stu-id="bd52c-118">Provides access to the supported methods, method attributes and method parameters.</span></span>                             |
| [<span data-ttu-id="bd52c-119">**Iportabledevicepropvariantcollection**</span><span class="sxs-lookup"><span data-stu-id="bd52c-119">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="bd52c-120">Enthält die Liste der unterstützten Methoden.</span><span class="sxs-lookup"><span data-stu-id="bd52c-120">Contains the list of supported methods.</span></span>                                                                        |
| [<span data-ttu-id="bd52c-121">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="bd52c-121">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="bd52c-122">Enthält die Attribute für eine Methode und für die Parameter einer bestimmten Methode.</span><span class="sxs-lookup"><span data-stu-id="bd52c-122">Contains the attributes for a method and for a given method's parameters.</span></span>                                      |
| [<span data-ttu-id="bd52c-123">**Iportabledevicekeycollection**</span><span class="sxs-lookup"><span data-stu-id="bd52c-123">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="bd52c-124">Enthält die Parameter für eine bestimmte Methode.</span><span class="sxs-lookup"><span data-stu-id="bd52c-124">Contains the parameters for a given method.</span></span>                                                                    |



 

<span data-ttu-id="bd52c-125">Wenn der Benutzer die Option "5" in der Befehlszeile auswählt, ruft die Anwendung die **listsupportedmethods** -Methode auf, die im Modul "servicemethods. cpp" zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="bd52c-125">When the user chooses option "5" at the command line, the application invokes the **ListSupportedMethods** method that is found in the ServiceMethods.cpp module.</span></span>

<span data-ttu-id="bd52c-126">Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontakt Dienst auf einem verbundenen Gerät öffnet.</span><span class="sxs-lookup"><span data-stu-id="bd52c-126">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="bd52c-127">In WPD wird eine Methode anhand ihres Namens, ihrer Zugriffsrechte, der Parameter und der zugehörigen Daten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd52c-127">In WPD, a method is described by its name, access rights, parameters, and related data.</span></span> <span data-ttu-id="bd52c-128">Die Beispielanwendung zeigt einen benutzerfreundlichen Namen an, z. b. "custommethod" oder eine GUID.</span><span class="sxs-lookup"><span data-stu-id="bd52c-128">The sample application displays a user-friendly name, for example, "CustomMethod", or a GUID.</span></span> <span data-ttu-id="bd52c-129">Auf den Methodennamen oder die GUID folgt der Zugriff auf Daten ("Lesen/Schreiben"), den Namen eines beliebigen zugeordneten Formats und die Parameterdaten.</span><span class="sxs-lookup"><span data-stu-id="bd52c-129">The method name or GUID is followed by access data ("Read/Write"), the name of any associated format, and the parameter data.</span></span> <span data-ttu-id="bd52c-130">Diese Daten umfassen den Parameternamen, die Verwendung, den VarType und das Formular.</span><span class="sxs-lookup"><span data-stu-id="bd52c-130">This data includes the parameter name, usage, VARTYPE, and form.</span></span>

<span data-ttu-id="bd52c-131">Fünf Methoden im servicemethods. cpp-Modul unterstützen das Abrufen von Methoden (und verknüpften Daten) für den jeweiligen Kontakt Dienst: **listsupportedmethods**, **Display Method**, **displaymethodaccess**, **Display Format** und **Display MethodParameters**.</span><span class="sxs-lookup"><span data-stu-id="bd52c-131">Five methods in the ServiceMethods.cpp module support the retrieval of methods (and related data) for the given Contacts service: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters**.</span></span> <span data-ttu-id="bd52c-132">Die **listsupportedmethods** -Methode ruft die Anzahl unterstützter Methoden und den GUID-Bezeichner für jeden ab. Anschließend wird die **displaymethod** -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-132">The **ListSupportedMethods** method retrieves a count of supported methods and the GUID identifier for each; it then calls the **DisplayMethod** method.</span></span> <span data-ttu-id="bd52c-133">Die **displaymethod** -Methode ruft die [**iportabledeviceservicecapebilitäts:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) -Methode auf, um die Optionen, Parameter usw. der angegebenen Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-133">The **DisplayMethod** method calls the [**IPortableDeviceServiceCapapbilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve the given method's options, parameters, and so on.</span></span> <span data-ttu-id="bd52c-134">Nachdem die Methoden Daten von **displaymethod** abgerufen wurden, werden der Name (oder die GUID), die Zugriffsbeschränkungen, das zugeordnete Format (sofern vorhanden) und die Parameter Beschreibungen gerendert.</span><span class="sxs-lookup"><span data-stu-id="bd52c-134">After the **DisplayMethod** retrieves the method data, it renders the name (or GUID), the access restrictions, the associated format (if any), and the parameter descriptions.</span></span> <span data-ttu-id="bd52c-135">**Display methodaccess**, **Display Format** und **displaymethodparameters** sind Hilfsfunktionen, die ihre jeweiligen Datenfelder Rendering.</span><span class="sxs-lookup"><span data-stu-id="bd52c-135">The **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** are helper functions that render their respective fields of data.</span></span>

<span data-ttu-id="bd52c-136">Die **listsupportedmethods** -Methode ruft die [**iportabledeviceservice:: Funktionen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) -Methode auf, um eine [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-136">The **ListSupportedMethods** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="bd52c-137">Mithilfe dieser Schnittstelle werden die unterstützten Methoden durch Aufrufen der [**iportabledeviceservicecapabili:: getsupportedmethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-137">Using this interface, it retrieves the supported methods by calling the [**IPortableDeviceServiceCapabilities::GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="bd52c-138">Die **getsupportedmethods** -Methode ruft die GUIDs für jede Methode ab, die vom Dienst unterstützt wird, und kopiert diese GUID in ein [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd52c-138">The **GetSupportedMethods** method retrieves the GUIDs for each method supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="bd52c-139">Im folgenden Code wird die **listsupportedmethods** -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd52c-139">The following code uses the **ListSupportedMethods** method.</span></span>


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



<span data-ttu-id="bd52c-140">Nachdem die **listsupportedmethods** -Methode die GUID für jedes Ereignis abgerufen hat, das vom angegebenen Dienst unterstützt wird, ruft Sie die **displaymethod** -Methode auf, um die Methoden spezifischen Attribute abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-140">After the **ListSupportedMethods** method retrieves the GUID for each event supported by the given service, it invokes the **DisplayMethod** method to retrieve the method-specific attributes.</span></span> <span data-ttu-id="bd52c-141">Zu diesen Attributen gehören: der Skript Anzeige Name der Methode, die erforderlichen Zugriffsbeschränkungen, das zugehörige Format und die Liste der Parameter.</span><span class="sxs-lookup"><span data-stu-id="bd52c-141">These attributes include: the method's script-friendly name , required access restrictions, any associated format, and list of parameters.</span></span>

<span data-ttu-id="bd52c-142">Die **displaymethod** -Methode ruft die [**iportabledeviceservicecapabili:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) -Methode auf, um eine Auflistung von Attributen für die angegebene Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-142">The **DisplayMethod** method invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve a collection of attributes for the given method.</span></span> <span data-ttu-id="bd52c-143">Anschließend wird die [**iportabledevicevalues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) -Methode aufgerufen, um den Namen der Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-143">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method to retrieve the method's name.</span></span> <span data-ttu-id="bd52c-144">Die **displaymethod** ruft [**iportabledevicevalues:: getunsignedintegervalue**](iportabledevicevalues-getunsignedintegervalue.md) auf, um die Zugriffs Umleitungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-144">The **DisplayMethod** calls the [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) to retrieve the access restrctions.</span></span> <span data-ttu-id="bd52c-145">Anschließend wird [**iportabledevicevalues:: getguidvalue**](iportabledevicevalues-getguidvalue.md) aufgerufen, um ein zugeordnetes Format abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-145">After this, it calls [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) to retrieve any associated format.</span></span> <span data-ttu-id="bd52c-146">Und schließlich Ruft die **displaymethod** den [**iportabledevicevalues:: getiportabledevicekeycollectionvalue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) auf, um die Parameterdaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-146">And, finally, the **DisplayMethod** calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the parameter data.</span></span> <span data-ttu-id="bd52c-147">Sie übergibt die von diesen Methoden zurückgegebenen Daten an die Hilfsfunktionen " **displaymethodaccess**", " **Display Format**" und " **displaymethodparameters** ", die die Informationen für die angegebene Methode Rendering.</span><span class="sxs-lookup"><span data-stu-id="bd52c-147">It passes the data returned by these methods to the **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** helper functions, which render the information for the given method.</span></span>

<span data-ttu-id="bd52c-148">Im folgenden Code wird die **displaymethod** -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd52c-148">The following code uses the **DisplayMethod** method.</span></span>


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



<span data-ttu-id="bd52c-149">Die Hilfsfunktion **displaymethodaccess** empfängt einen DWORD-Wert, der die Zugriffs Optionen der Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="bd52c-149">The **DisplayMethodAccess** helper function receives a DWORD value that contains the method's access options.</span></span> <span data-ttu-id="bd52c-150">Dieser Wert wird mit dem WPD \_ \_ -Befehls Zugriffs \_ Lese-und dem WPD \_ -Befehls Zugriffs-Lesevorgang verglichen \_ \_ , um die Zugriffsberechtigung der Methode zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-150">It compares this value to WPD\_COMMAND\_ACCESS\_READ and WPD\_COMMAND\_ACCESS\_READWRITE to determine the method's access privilege.</span></span> <span data-ttu-id="bd52c-151">Wenn das Ergebnis verwendet wird, rendert es eine Zeichenfolge, die die Zugriffsbeschränkung für die angegebene Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="bd52c-151">Using the result, it renders a string indicating the access restriction for the given method.</span></span>

<span data-ttu-id="bd52c-152">Im folgenden Code wird die-Hilfsfunktion **displaymethodaccess** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd52c-152">The following code uses the **DisplayMethodAccess** helper function.</span></span>


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



<span data-ttu-id="bd52c-153">Die Hilfsfunktion **displaymethod** empfängt ein [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Objekt und die GUID der Methode als Parameter.</span><span class="sxs-lookup"><span data-stu-id="bd52c-153">The **DisplayMethod** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object and the method's GUID as parameters.</span></span> <span data-ttu-id="bd52c-154">Mithilfe des **iportabledeviceservicecapabili-** Objekts wird die [**iportabledeviceservicecapabili:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) -Methode aufgerufen, um die Methoden Attribute abzurufen und Sie im Konsolenfenster der Anwendung zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-154">Using the **IPortableDeviceServiceCapabilities** object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method to retrieve the method attributes and render them in the application's console window.</span></span>

<span data-ttu-id="bd52c-155">Die Hilfsfunktion **displaymethodparameters** empfängt ein [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Objekt, die GUID der Methode und ein iportabledevicekeycollection-Objekt, das die Methoden Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="bd52c-155">The **DisplayMethodParameters** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object, the method's GUID, and an IPortableDeviceKeyCollection object containing the method parameters.</span></span> <span data-ttu-id="bd52c-156">Mithilfe des [**iportabledevicekeycollection**](iportabledevicekeycollection.md) -Objekts wird die [**iportabledeviceservicecapabili:: getmethodparameterattribute**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) -Methode aufgerufen, um den Namen, die Verwendung, den VarType und das Formular des Parameters abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd52c-156">Using the [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) method to retrieve the parameter's name, usage, VARTYPE, and form.</span></span> <span data-ttu-id="bd52c-157">Diese Informationen werden im Konsolenfenster der Anwendung gerendert.</span><span class="sxs-lookup"><span data-stu-id="bd52c-157">It renders this information in the application's console window.</span></span>

<span data-ttu-id="bd52c-158">Im folgenden Code wird die-Hilfsfunktion **displaymethodparameters** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd52c-158">The following code uses the **DisplayMethodParameters** helper function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="bd52c-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd52c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd52c-160">**Iportabledevicekeycollection**</span><span class="sxs-lookup"><span data-stu-id="bd52c-160">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="bd52c-161">**Iportablede viceservice**</span><span class="sxs-lookup"><span data-stu-id="bd52c-161">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="bd52c-162">**Iportablede viceservicecapabili**</span><span class="sxs-lookup"><span data-stu-id="bd52c-162">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="bd52c-163">**Iportablede vicevalues**</span><span class="sxs-lookup"><span data-stu-id="bd52c-163">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="bd52c-164">Wpdservicesapisample</span><span class="sxs-lookup"><span data-stu-id="bd52c-164">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




---
description: Abrufen der von einem Gerät unterstützten Renderingfunktionen
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: Abrufen der von einem Gerät unterstützten Renderingfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523f1f9bbcaefe1c502c7c74252582fddcadad4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349339"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a><span data-ttu-id="8f32a-103">Abrufen der von einem Gerät unterstützten Renderingfunktionen</span><span class="sxs-lookup"><span data-stu-id="8f32a-103">Retrieving the Rendering Capabilities Supported by a Device</span></span>

<span data-ttu-id="8f32a-104">Tragbare Windows-Geräte, die die Funktions Kategorie Renderinginformationen unterstützen ( \_ Renderinginformationen der WPD- \_ Funktionskategorie \_ ), \_ geben Renderinginformationen zurück,</span><span class="sxs-lookup"><span data-stu-id="8f32a-104">Windows Portable Devices that support the rendering information functional category (WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION) will return rendering information when queried.</span></span> <span data-ttu-id="8f32a-105">Die Renderinginformationen beschreiben die Anforderungen und Einschränkungen für Anwendungen, die versuchen, Inhalte auf ein Gerät zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="8f32a-105">The rendering information describes requirements and restrictions imposed on applications that attempt to write content to a device.</span></span>

<span data-ttu-id="8f32a-106">Die Funktion listrenderingcapabilityinformation, die Hilfsfunktion supportsfunctionalcategory und die Hilfsfunktion "leseprofileinformationproperties" im Modul "devicecapabili. cpp" veranschaulichen das Abrufen von Renderingfunktionen für ein ausgewähltes Gerät.</span><span class="sxs-lookup"><span data-stu-id="8f32a-106">The ListRenderingCapabilityInformation function, the SupportsFunctionalCategory helper function, and the ReadProfileInformationProperties helper function in the DeviceCapabilities.cpp module demonstrate the retrieval of rendering capabilities for a selected device.</span></span>

<span data-ttu-id="8f32a-107">Die Anwendung kann die von einem Gerät unterstützten Renderingfunktionen mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="8f32a-107">Your application can retrieve the rendering capabilities supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="8f32a-108">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8f32a-108">Interface</span></span>                                                                                      | <span data-ttu-id="8f32a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f32a-109">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="8f32a-110">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="8f32a-111">Bietet Zugriff auf die iportabledeviceproperties-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8f32a-111">Provides access to the IPortableDeviceProperties interface.</span></span> |
| [<span data-ttu-id="8f32a-112">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-112">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="8f32a-113">Bietet Zugriff auf die Eigenschaften spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="8f32a-113">Provides access to the property-specific methods.</span></span>           |
| [<span data-ttu-id="8f32a-114">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-114">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="8f32a-115">Wird verwendet, um die Eigenschafts Schlüssel für das angegebene Profil zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8f32a-115">Used to store the property keys for the given profile.</span></span>      |
| [<span data-ttu-id="8f32a-116">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-116">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="8f32a-117">Wird verwendet, um die Eigenschaftswerte für das angegebene Profil zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8f32a-117">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="8f32a-118">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-118">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="8f32a-119">Wird verwendet, um die Eigenschaftswerte für das angegebene Profil zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8f32a-119">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="8f32a-120">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-120">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="8f32a-121">Wird verwendet, um die Eigenschaftswerte für das angegebene Profil zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8f32a-121">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="8f32a-122">**Iportableabvicevaluescollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-122">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="8f32a-123">Wird verwendet, um die Eigenschaftswerte für das angegebene Profil zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8f32a-123">Used store the property values for the given profile.</span></span>       |



 

<span data-ttu-id="8f32a-124">Eine der ersten Aufgaben, die von der Beispielanwendung durchgeführt werden, besteht darin, zu bestimmen, ob das ausgewählte Gerät Renderingfunktionen auflisten kann.</span><span class="sxs-lookup"><span data-stu-id="8f32a-124">One of the first tasks accomplished by the sample application is to determine whether the selected device is capable of listing rendering capabilities.</span></span> <span data-ttu-id="8f32a-125">Die supportsfunctionalcategory-Hilfsfunktion bestimmt, ob dies der Fall ist, indem die Hilfsfunktion listrenderingcapabilityinformation aufgerufen und \_ \_ \_ die Renderinginformationen der WPD-Funktionskategorie \_ als zweites Argument übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8f32a-125">The SupportsFunctionalCategory helper function determines whether this is the case by calling the ListRenderingCapabilityInformation helper function and passing WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION as the second argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SupportsFunctionalCategory(pDevice, WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION) == FALSE)
{
    printf("This device does not support device rendering information to display\n");
    return;
}
```



<span data-ttu-id="8f32a-126">Wenn das Gerät Renderingfunktionen auflisten kann, umfasst der nächste Schritt das Abrufen eines [**iportabledevicecapabili-**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) Objekts und das Aufrufen der [**getfunctionalobjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) -Methode zum Abrufen eines Objekt Bezeichners für das Rendering-Information-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8f32a-126">If the device is capable of listing rendering capabilities, the next step entails retrieving an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object and invoking the [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method to retrieve an object identifier for the rendering-information object.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get the functional object identifier for the rendering information object
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalObjects(WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION, &pRenderingInfoObjects);
    if (FAILED(hr))
    {
        printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="8f32a-127">Der nächste Schritt besteht darin, den renderinformationsobjektbezeichner zu speichern, der soeben in einer Zeichen folgen Variablen ("straurenderinginfoobjectid") abgerufen wurde, und dann die Hilfsfunktion "Read profileinformationproperties" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="8f32a-127">The next step is to store the rendering-information object identifier that was just retrieved in a string variable (strRenderingInfoObjectID), and then to call the ReadProfileInformationProperties helper function.</span></span> <span data-ttu-id="8f32a-128">(Die Variable "straurenderinginfoobjectid" wird als zweites Argument an die Hilfsfunktion übermittelt.)</span><span class="sxs-lookup"><span data-stu-id="8f32a-128">(The variable, strRenderingInfoObjectID, is passed as the second argument to the helper function.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SUCCEEDED(hr))
{
    PROPVARIANT pv = {0};
    PropVariantInit(&pv);
    hr = pRenderingInfoObjects->GetAt(0, &pv);
    if ((SUCCEEDED(hr))    &&
        (pv.vt== VT_LPWSTR) )
    {
        strRenderingInfoObjectID = pv.pwszVal;
    }
    else
    {
        printf("! Failed to get first rendering object's identifier, hr = 0x%lx\n", hr);
    }

    PropVariantClear(&pv);
}

if (SUCCEEDED(hr))
{
    hr = ReadProfileInformationProperties(pDevice,
                                          strRenderingInfoObjectID,
                                          &pRenderingInfoProfiles);
    // Error output statements are performed by the helper function, so they
    // are omitted here.
}
```



<span data-ttu-id="8f32a-129">Eine der ersten Aufgaben, die von der Hilfsfunktion durchgeführt werden, besteht darin, ein [**iportabledevicecontent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) -Objekt abzurufen, das für den Zugriff auf die Inhalts spezifischen Methoden verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f32a-129">One of the first tasks accomplished by the helper function is to retrieve an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to access the content-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="8f32a-130">Als nächstes Ruft die Hilfsfunktion ein [**iportabledeviceproperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) -Objekt ab, das für den Zugriff auf die Eigenschaften spezifischen Methoden verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f32a-130">Next, the helper function retrieves an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) object, which it will use to access the property-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="8f32a-131">Der nächste Schritt ist das Erstellen eines [**iportabledevicekeycollection**](iportabledevicekeycollection.md) -Objekts, in das die Eigenschafts Schlüssel für die Renderinginformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="8f32a-131">The next step is to create an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object into which the property keys for the rendering information are stored.</span></span> <span data-ttu-id="8f32a-132">Nachdem das Objekt erstellt wurde, wird die [**iportabledevicekeycollection:: Add**](iportabledevicekeycollection-add.md) -Methode aufgerufen, um die erforderlichen Schlüssel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8f32a-132">Once the object is created, the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method is invoked to add the necessary keys.</span></span> <span data-ttu-id="8f32a-133">(Es ist notwendig, diese Schlüssel hinzuzufügen, damit die entsprechenden renderingprofile in den nachfolgenden Schritten abgerufen werden können.)</span><span class="sxs-lookup"><span data-stu-id="8f32a-133">(It is necessary to add these keys so that the corresponding rendering profiles can be retrieved in the subsequent steps.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IPortableDeviceKeyCollection,
                      (VOID**) &pPropertiesToRead);
if (SUCCEEDED(hr))
{
    // Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_RENDERING_INFORMATION_PROFILES);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_RENDERING_INFORMATION_PROFILES to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="8f32a-134">Der nächste Schritt besteht darin, die Eigenschaftswerte aus dem Gerätetreiber abzurufen, indem Sie die [**iportabledeviceproperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8f32a-134">The next step is to retrieve the property values from the device driver by calling the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(wszFunctionalObjectID, // The object whose properties we are reading
                                pPropertiesToRead,     // The properties we want to read
                                &pObjectProperties);   // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", wszFunctionalObjectID, hr);
    }
}
```



<span data-ttu-id="8f32a-135">Im nächsten Schritt wird das Rendering-Information-Profil abgerufen und im pprenderinginf-files-Argument gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8f32a-135">The next step retrieves the rendering-information profile and stores it in the ppRenderingInfoProfiles argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pObjectProperties->GetIPortableDeviceValuesCollectionValue(WPD_RENDERING_INFORMATION_PROFILES,
                                                                    &pRenderingInfoProfiles);
    if (FAILED(hr))
    {
        printf("! Failed to get WPD_RENDERING_INFORMATION_PROFILES from rendering information, hr= 0x%lx\n",  hr);
    }
}

// QueryInterface the interface into the out-going parameters.
if (SUCCEEDED(hr))
{
    hr = pRenderingInfoProfiles->QueryInterface(IID_PPV_ARGS(ppRenderingInfoProfiles));
    if (FAILED(hr))
    {
        printf("! Failed to QueryInterface for IPortableDeviceValuesCollection (Rendering information profiles), hr= 0x%lx\n",  hr);
    }
}
```



<span data-ttu-id="8f32a-136">Nachdem die Hilfsfunktion die Eigenschaften der WPD- \_ Rendering- \_ Informations \_ profile gelesen hat, werden die renderingprofile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f32a-136">After the helper function reads the WPD\_RENDERING\_INFORMATION\_PROFILES properties, the rendering profiles are displayed.</span></span> <span data-ttu-id="8f32a-137">Diese Profile werden durch die displayrenderingprofile-Hilfsfunktion angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f32a-137">These profiles are displayed by the DisplayRenderingProfile helper function.</span></span>


```C++
void DisplayRenderingProfile(
    IPortableDeviceValues* pProfile)
{
    HRESULT hr = S_OK;
    if (pProfile == NULL)
    {
        return;
    }

    if (SUCCEEDED(hr))
    {
        DWORD dwTotalBitrate    = 0;
        DWORD dwChannelCount    = 0;
        DWORD dwAudioFormatCode = 0;
        GUID  guidFormat        = WPD_OBJECT_FORMAT_UNSPECIFIED;

        // Display WPD_MEDIA_TOTAL_BITRATE
        hr = pProfile->GetUnsignedIntegerValue(WPD_MEDIA_TOTAL_BITRATE, &dwTotalBitrate);
        if (SUCCEEDED(hr))
        {
            printf("Total Bitrate: %d\n", dwTotalBitrate);
        }

        // If we fail to read the total bitrate as a single value, then it must be
        // a valid value set.  (i.e. returning IPortableDeviceValues as the value which
        // contains properties describing the valid values for this property.)
        if (hr == DISP_E_TYPEMISMATCH)
        {
            CComPtr<IPortableDeviceValues> pExpectedValues;
            hr = pProfile->GetIPortableDeviceValuesValue(WPD_MEDIA_TOTAL_BITRATE, &pExpectedValues);
            if (SUCCEEDED(hr))
            {
                printf("Total Bitrate: ");
                DisplayExpectedValues(pExpectedValues);
            }
        }

        // If we are still a failure here, report the error
        if (FAILED(hr))
        {

            printf("! Failed to get WPD_MEDIA_TOTAL_BITRATE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_CHANNEL_COUNT
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_CHANNEL_COUNT, &dwChannelCount);
        if (SUCCEEDED(hr))
        {
            printf("Channel Count: %d\n", dwChannelCount);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_CHANNEL_COUNT from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_FORMAT_CODE
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_FORMAT_CODE,   &dwAudioFormatCode);
        if (SUCCEEDED(hr))
        {
            printf("Audio Format Code: %d\n", dwAudioFormatCode);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_FORMAT_CODE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_OBJECT_FORMAT
        hr = pProfile->GetGuidValue(WPD_OBJECT_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("Object Format: %ws\n", (LPWSTR)CComBSTR(guidFormat));
        }
        else
        {
            printf("! Failed to get WPD_OBJECT_FORMAT from rendering profile, hr = 0x%lx\n",hr);
        }
    }
}
```



<span data-ttu-id="8f32a-138">Beachten Sie Folgendes: da die renderingprofile statisch sind, kann die Anwendung die Profile lesen und lokal speichern (anstatt jedes Mal, wenn die Daten benötigt werden, auf das Gerät zuzugreifen).</span><span class="sxs-lookup"><span data-stu-id="8f32a-138">Note that since the rendering profiles are static, your application may choose to read the profiles and store them locally (instead of accessing the device each time the data is needed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f32a-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f32a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f32a-140">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="8f32a-141">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-141">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="8f32a-142">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="8f32a-143">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="8f32a-144">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="8f32a-145">**Iportableabvicevaluescollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8f32a-145">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> <dt>

[<span data-ttu-id="8f32a-146">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="8f32a-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




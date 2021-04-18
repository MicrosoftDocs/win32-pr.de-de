---
description: Geräteeigenschaften
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Geräteeigenschaften (Core-audioapis)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340100"
---
# <a name="device-properties-core-audio-apis"></a><span data-ttu-id="95c4a-103">Geräteeigenschaften (Core-audioapis)</span><span class="sxs-lookup"><span data-stu-id="95c4a-103">Device Properties (Core Audio APIs)</span></span>

<span data-ttu-id="95c4a-104">Beim Auflisten von [audioendpunktgeräten](audio-endpoint-devices.md)kann eine Client Anwendung die Endpunkt Objekte für Ihre Geräteeigenschaften Abfragen.</span><span class="sxs-lookup"><span data-stu-id="95c4a-104">During the process of enumerating [audio endpoint devices](audio-endpoint-devices.md), a client application can interrogate the endpoint objects for their device properties.</span></span> <span data-ttu-id="95c4a-105">Die Geräteeigenschaften werden in der mmdevice-API-Implementierung der **IPropertyStore** -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="95c4a-105">The device properties are exposed in MMDevice API's implementation of the **IPropertyStore** interface.</span></span> <span data-ttu-id="95c4a-106">Bei einem Verweis auf die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle eines Endpunkt Objekts kann ein Client einen Verweis auf den Eigenschaften Speicher des Endpunkt Objekts abrufen, indem er die [**immdevice:: openpropertystore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="95c4a-106">Given a reference to the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an endpoint object, a client can obtain a reference to the endpoint object's property store by calling the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method.</span></span>

<span data-ttu-id="95c4a-107">Das Property-Store-Objekt macht eine **IPropertyStore** -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95c4a-107">The property-store object exposes an **IPropertyStore** interface.</span></span> <span data-ttu-id="95c4a-108">Die beiden primären Methoden in dieser Schnittstelle sind **IPropertyStore:: GetValue**, der einen Geräte Eigenschafts Wert abruft, und **IPropertyStore:: SetValue**, der einen Wert für die Geräte Eigenschaft festlegt.</span><span class="sxs-lookup"><span data-stu-id="95c4a-108">The two primary methods in this interface are **IPropertyStore::GetValue**, which gets a device property value, and **IPropertyStore::SetValue**, which sets a device property value.</span></span> <span data-ttu-id="95c4a-109">Weitere Informationen zu **IPropertyStore** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="95c4a-109">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="95c4a-110">Die Implementierung des Eigenschafts Speicher der mmdevice-API unterscheidet sich vom standardmäßigen shelleigenschafts-Speicher Objekt.</span><span class="sxs-lookup"><span data-stu-id="95c4a-110">The MMDevice API's implementation of the property store is different from the standard shell property store object.</span></span> <span data-ttu-id="95c4a-111">Um einen Eigenschafts Wert zu ändern, muss die Client Anwendung die **IPropertyStore:: SetValue** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="95c4a-111">To change a property value, the client application must call the **IPropertyStore::SetValue** method.</span></span> <span data-ttu-id="95c4a-112">Während dieses Aufrufes werden die neuen Werte festgelegt und in der Registrierung geschrieben.</span><span class="sxs-lookup"><span data-stu-id="95c4a-112">During this call, the new values are set and written in the registry.</span></span> <span data-ttu-id="95c4a-113">Daher muss die Anwendung die **IPropertyStore:: Commit** -Methode nach dem **SetValue** -Befehl nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="95c4a-113">Therefore, the application does not need to call the **IPropertyStore::Commit** method after the **SetValue** call.</span></span> <span data-ttu-id="95c4a-114">Das Handle für die Registrierung wird nur geschlossen, wenn der Client den Schnittstellen Zeiger freigibt.</span><span class="sxs-lookup"><span data-stu-id="95c4a-114">The handle to the registry is closed only when the client releases the interface pointer.</span></span>

<span data-ttu-id="95c4a-115">In der Regel wird von Drittanbieter-Client Anwendungen die **GetValue** -Methode, jedoch nicht die **SetValue** -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="95c4a-115">Typically, third-party client applications call the **GetValue** method but not the **SetValue** method.</span></span> <span data-ttu-id="95c4a-116">Der Endpunkt-Manager legt die grundlegenden Geräteeigenschaften für Endpunkte fest.</span><span class="sxs-lookup"><span data-stu-id="95c4a-116">The endpoint manager sets the basic device properties for endpoints.</span></span> <span data-ttu-id="95c4a-117">Der Endpunkt-Manager ist die Komponente von Windows Vista, die für das Erkennen des Vorhandenseins von audioendpunktgeräten verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="95c4a-117">The endpoint manager is the Windows Vista component that is responsible for detecting the presence of audio endpoint devices.</span></span>

<span data-ttu-id="95c4a-118">Jeder pkey \_ xxx-Eigenschaften Bezeichner in der folgenden Liste ist eine Konstante vom Typ **PropertyKey** , die in der Header Datei functiondiscoverykeys \_ devpkey. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="95c4a-118">Each PKEY\_Xxx property identifier in the following list is a constant of type **PROPERTYKEY** that is defined in header file Functiondiscoverykeys\_devpkey.h.</span></span> <span data-ttu-id="95c4a-119">Alle audioendpunktgeräte verfügen über diese drei Geräteeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="95c4a-119">All audio endpoint devices have these three device properties.</span></span>



| <span data-ttu-id="95c4a-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95c4a-120">Property</span></span>                                                                         | <span data-ttu-id="95c4a-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95c4a-121">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95c4a-122">**Pkey-Geräte \_ Name (tviceinterface \_ FriendlyName)**</span><span class="sxs-lookup"><span data-stu-id="95c4a-122">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="95c4a-123">Der Anzeige Name des audioadapters, an den das Endpunkt Gerät angefügt wird (z. b. "XYZ-Audioadapter").</span><span class="sxs-lookup"><span data-stu-id="95c4a-123">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span> <span data-ttu-id="95c4a-124">Das **PROPVARIANT** -Element **VT** ist auf VT \_ LPWSTR festgelegt, und der Member **pwszval** verweist auf eine NULL-terminierte Zeichenfolge mit breit Zeichen, die den anzeigen Amen enthält.</span><span class="sxs-lookup"><span data-stu-id="95c4a-124">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span> |
| [<span data-ttu-id="95c4a-125">**Pkey- \_ Gerät \_ devicedebug**</span><span class="sxs-lookup"><span data-stu-id="95c4a-125">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="95c4a-126">Die Geräte Beschreibung des Endpunkt Geräts (z. b. "Sprecher").</span><span class="sxs-lookup"><span data-stu-id="95c4a-126">The device description of the endpoint device (for example, "Speakers").</span></span> <span data-ttu-id="95c4a-127">Der **PROPVARIANT** -Member **VT** ist auf VT \_ LPWSTR festgelegt, und der Member **pwszval** verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die die Geräte Beschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="95c4a-127">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the device description.</span></span>                                       |
| [<span data-ttu-id="95c4a-128">**Pkey- \_ Gerät \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="95c4a-128">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="95c4a-129">Der Anzeige Name des Endpunkt Geräts (z. b. "Sprecher (XYZ-Audioadapter)").</span><span class="sxs-lookup"><span data-stu-id="95c4a-129">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span> <span data-ttu-id="95c4a-130">Das **PROPVARIANT** -Element **VT** ist auf VT \_ LPWSTR festgelegt, und der Member **pwszval** verweist auf eine NULL-terminierte Zeichenfolge mit breit Zeichen, die den anzeigen Amen enthält.</span><span class="sxs-lookup"><span data-stu-id="95c4a-130">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span>                             |



 

<span data-ttu-id="95c4a-131">Einige audioendpunktgeräte verfügen möglicherweise über zusätzliche Eigenschaften, die nicht in der vorangehenden Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="95c4a-131">Some audio endpoint devices might have additional properties that do not appear in the preceding list.</span></span> <span data-ttu-id="95c4a-132">Weitere Informationen zu zusätzlichen Eigenschaften finden Sie unter [Eigenschaften für audioendpunkte](audio-endpoint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="95c4a-132">For more information about additional properties, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span> <span data-ttu-id="95c4a-133">Weitere Informationen zu **PropertyKey** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="95c4a-133">For more information about **PROPERTYKEY**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="95c4a-134">Im folgenden Codebeispiel werden die anzeigen Amen aller audiorendering-Endpunkt Geräte im System ausgegeben:</span><span class="sxs-lookup"><span data-stu-id="95c4a-134">The following code example prints the display names of all audio-rendering endpoint devices in the system:</span></span>


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



<span data-ttu-id="95c4a-135">Das fehlgeschlagene Makro im vorangehenden Codebeispiel ist in der Header Datei Winerror. h definiert.</span><span class="sxs-lookup"><span data-stu-id="95c4a-135">The FAILED macro in the preceding code example is defined in header file Winerror.h.</span></span>

<span data-ttu-id="95c4a-136">Im vorangehenden Codebeispiel ruft der **for**-Loop-Text in der printendpointnames-Funktion die [**immdevice:: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) -Methode auf, um die [Endpunkt-ID-Zeichenfolge](endpoint-id-strings.md) für das audioendpunkt-Gerät abzurufen, das von der **immdevice** -Schnittstellen Instanz dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="95c4a-136">In the preceding code example, the **for**-loop body in the PrintEndpointNames function calls the [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method to obtain the [endpoint ID string](endpoint-id-strings.md) for the audio endpoint device that is represented by the **IMMDevice** interface instance.</span></span> <span data-ttu-id="95c4a-137">Durch die Zeichenfolge wird das Gerät in Bezug auf alle anderen audioendpunktgeräte im System eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="95c4a-137">The string uniquely identifies the device with respect to all of the other audio endpoint devices in the system.</span></span> <span data-ttu-id="95c4a-138">Ein Client kann die Zeichenfolge der Endpunkt-ID verwenden, um eine Instanz des audioendpunktgeräts zu einem späteren Zeitpunkt oder in einem anderen Prozess zu erstellen, indem die [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="95c4a-138">A client can use the endpoint ID string to create an instance of the audio endpoint device at a later time or in a different process by calling the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="95c4a-139">Clients sollten den Inhalt der Endpunkt-ID-Zeichenfolge als nicht transparent behandeln.</span><span class="sxs-lookup"><span data-stu-id="95c4a-139">Clients should treat the contents of the endpoint ID string as opaque.</span></span> <span data-ttu-id="95c4a-140">Das heißt, Clients sollten nicht versuchen, den Inhalt der Zeichenfolge zu analysieren, um Informationen über das Gerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="95c4a-140">That is, clients should not attempt to parse the contents of the string to obtain information about the device.</span></span> <span data-ttu-id="95c4a-141">Der Grund hierfür ist, dass das Zeichen folgen Format nicht definiert ist und sich möglicherweise von einer Implementierung der mmdevice-API zum nächsten ändert.</span><span class="sxs-lookup"><span data-stu-id="95c4a-141">The reason is that the string format is undefined and might change from one implementation of the MMDevice API to the next.</span></span>

<span data-ttu-id="95c4a-142">Die benutzerfreundlichen Gerätenamen und Endpunkt-ID-Zeichen folgen, die von der printendpointnames-Funktion im vorangehenden Codebeispiel abgerufen werden, sind identisch mit den benutzerfreundlichen Gerätenamen und Endpunkt-ID-Zeichen folgen, die von DirectSound während der Geräte Enumeration bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="95c4a-142">The friendly device names and endpoint ID strings that are obtained by the PrintEndpointNames function in the preceding code example are identical to the friendly device names and endpoint ID strings that are provided by DirectSound during device enumeration.</span></span> <span data-ttu-id="95c4a-143">Weitere Informationen finden Sie unter [Audioereignisse für Legacy-Audioanwendungen](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="95c4a-143">For more information, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

<span data-ttu-id="95c4a-144">Im vorangehenden Codebeispiel ruft die Funktion printendpointnames die **cokreateinstance** -Funktion auf, um einen Enumerator für die audioendpunktgeräte im System zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="95c4a-144">In the preceding code example, the PrintEndpointNames function calls the **CoCreateInstance** function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="95c4a-145">Wenn das aufrufende Programm die **CoInitialize** -Funktion oder die **CoInitializeEx** -Funktion nicht zum Initialisieren der com-Bibliothek aufgerufen hat, tritt beim **CoCreateInstance** -Aufruf ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="95c4a-145">Unless the calling program previously called either the **CoInitialize** or **CoInitializeEx** function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="95c4a-146">Weitere Informationen zu **cokreateinstance**, **CoInitialize** und **CoInitializeEx** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="95c4a-146">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="95c4a-147">Weitere Informationen zu den Schnittstellen " **immdeviceenumerator**", " **immdevicecollection**" und " **immdevice** " finden Sie unter [mmdevice-API](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="95c4a-147">For more information about the **IMMDeviceEnumerator**, **IMMDeviceCollection**, and **IMMDevice** interfaces, see [MMDevice API](mmdevice-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95c4a-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95c4a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95c4a-149">Audioendpunktgeräte</span><span class="sxs-lookup"><span data-stu-id="95c4a-149">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 




---
description: Geräte Ereignisse
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Geräte Ereignisse (Core-audioapis)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344936"
---
# <a name="device-events-core-audio-apis"></a><span data-ttu-id="7e907-103">Geräte Ereignisse (Core-audioapis)</span><span class="sxs-lookup"><span data-stu-id="7e907-103">Device Events (Core Audio APIs)</span></span>

<span data-ttu-id="7e907-104">Ein Geräte Ereignis benachrichtigt Clients über eine Änderung des Status eines [audioendpunktgeräts](audio-endpoint-devices.md) im System.</span><span class="sxs-lookup"><span data-stu-id="7e907-104">A device event notifies clients of a change in the status of an [audio endpoint device](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="7e907-105">Im folgenden finden Sie Beispiele für Geräte Ereignisse:</span><span class="sxs-lookup"><span data-stu-id="7e907-105">The following are examples of device events:</span></span>

-   <span data-ttu-id="7e907-106">Der Benutzer aktiviert oder deaktiviert ein audioendpunktgerät von Device Manager oder von der Windows-Multimedia-Systemsteuerung Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="7e907-106">The user enables or disables an audio endpoint device from Device Manager or from the Windows multimedia control panel, Mmsys.cpl.</span></span>
-   <span data-ttu-id="7e907-107">Der Benutzer fügt dem System einen Audioadapter hinzu oder entfernt einen Audioadapter aus dem System.</span><span class="sxs-lookup"><span data-stu-id="7e907-107">The user adds an audio adapter to the system or removes an audio adapter from the system.</span></span>
-   <span data-ttu-id="7e907-108">Der Benutzer bindet ein audioendpunktgerät mit der Erkennung von Jack-Presence in einen audiowagen ein oder entfernt ein audioendpunktgerät von einem solchen Jack.</span><span class="sxs-lookup"><span data-stu-id="7e907-108">The user plugs an audio endpoint device into an audio jack with jack-presence detection, or removes an audio endpoint device from such a jack.</span></span>
-   <span data-ttu-id="7e907-109">Der Benutzer ändert die [Geräte Rolle](device-roles.md) , die einem Gerät zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7e907-109">The user changes the [device role](device-roles.md) that is assigned to a device.</span></span>
-   <span data-ttu-id="7e907-110">Der Wert einer [Eigenschaft eines Geräts](device-properties.md) ändert sich.</span><span class="sxs-lookup"><span data-stu-id="7e907-110">The value of a [property of a device](device-properties.md) changes.</span></span>

<span data-ttu-id="7e907-111">Das Hinzufügen oder Entfernen eines audioadapters generiert Geräte Ereignisse für alle audioendpunktgeräte, die eine Verbindung mit dem Adapter herstellen.</span><span class="sxs-lookup"><span data-stu-id="7e907-111">The addition or removal of an audio adapter generates device events for all of the audio endpoint devices that connect to the adapter.</span></span> <span data-ttu-id="7e907-112">Die ersten vier Elemente in der vorangehenden Liste sind Beispiele für Gerätestatus Änderungen.</span><span class="sxs-lookup"><span data-stu-id="7e907-112">The first four items in the preceding list are examples of device state changes.</span></span> <span data-ttu-id="7e907-113">Weitere Informationen zu den Geräte Zuständen von audioendpunktgeräten finden Sie unter [Geräte \_ Status xxx- \_ Konstanten](device-state-xxx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7e907-113">For more information about the device states of audio endpoint devices, see [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).</span></span> <span data-ttu-id="7e907-114">Weitere Informationen zur Erkennung von Jack-Presence finden Sie unter [audioendpunktgeräte](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="7e907-114">For more information about jack-presence detection, see [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="7e907-115">Ein Client kann sich registrieren, um beim Auftreten von Geräte Ereignissen benachrichtigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="7e907-115">A client can register to be notified when device events occur.</span></span> <span data-ttu-id="7e907-116">Als Reaktion auf diese Benachrichtigungen kann der Client die Art und Weise, in der ein bestimmtes Gerät verwendet wird, dynamisch ändern oder ein anderes Gerät auswählen, das für einen bestimmten Zweck verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e907-116">In response to these notifications, the client can dynamically change the way that it uses a particular device, or select a different device to use for a particular purpose.</span></span>

<span data-ttu-id="7e907-117">Wenn eine Anwendung z. b. eine Audiospur über einen Satz von USB-sprechenden spielen und der Benutzer die Lautsprecher mit dem USB-Connector trennt, empfängt die Anwendung eine Benachrichtigung über das Geräte Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7e907-117">For example, if an application is playing an audio track through a set of USB speakers, and the user disconnects the speakers from the USB connector, the application receives a device-event notification.</span></span> <span data-ttu-id="7e907-118">Wenn die Anwendung in Reaktion auf das Ereignis erkennt, dass eine Gruppe von Desktop Referenten mit dem integrierten Audioadapter auf der System-Hauptplatine verbunden ist, kann die Anwendung die Audiospur über die Desktop Referenten fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="7e907-118">In response to the event, if the application detects that a set of desktop speakers is connected to the integrated audio adapter on the system motherboard, the application can resume playing the audio track through the desktop speakers.</span></span> <span data-ttu-id="7e907-119">In diesem Beispiel erfolgt der Übergang von USB-sprechenden zu Desktop Referenten automatisch, ohne dass der Benutzer eingreifen muss, indem er die Anwendung explizit umleitet.</span><span class="sxs-lookup"><span data-stu-id="7e907-119">In this example, the transition from USB speakers to desktop speakers occurs automatically, without requiring the user to intervene by explicitly redirecting the application.</span></span>

<span data-ttu-id="7e907-120">Um sich für den Empfang von Geräte Benachrichtigungen zu registrieren, Ruft ein Client die [**immdeviceenumerator:: registerendpointnotificationcallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="7e907-120">To register to receive device notifications, a client calls the [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) method.</span></span> <span data-ttu-id="7e907-121">Wenn der Client keine Benachrichtigungen mehr erfordert, wird er durch Aufrufen der [**immdeviceenumerator:: unregisterendpointnotificationcallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) -Methode abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="7e907-121">When the client no longer requires notifications, it cancels them by calling the [**IMMDeviceEnumerator::UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) method.</span></span> <span data-ttu-id="7e907-122">Beide Methoden akzeptieren einen Eingabeparameter mit dem Namen " *pnotify*", bei dem es sich um einen Zeiger auf eine [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) -Schnittstellen Instanz handelt.</span><span class="sxs-lookup"><span data-stu-id="7e907-122">Both methods take an input parameter, named *pNotify*, that is a pointer to an [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) interface instance.</span></span>

<span data-ttu-id="7e907-123">Die **immnotificationclient** -Schnittstelle wird von einem Client implementiert.</span><span class="sxs-lookup"><span data-stu-id="7e907-123">The **IMMNotificationClient** interface is implemented by a client.</span></span> <span data-ttu-id="7e907-124">Die-Schnittstelle enthält mehrere Methoden, von denen jede als Rückruf Routine für eine bestimmte Art von Geräte Ereignis fungiert.</span><span class="sxs-lookup"><span data-stu-id="7e907-124">The interface contains several methods, each of which serves as a callback routine for a particular type of device event.</span></span> <span data-ttu-id="7e907-125">Wenn ein Geräte Ereignis in einem audioendpunktgerät auftritt, ruft das mmdevice-Modul die entsprechende Methode in der **immnotificationclient** -Schnittstelle jedes Clients auf, der zurzeit für den Empfang von Benachrichtigungen über Geräte Ereignisse registriert ist.</span><span class="sxs-lookup"><span data-stu-id="7e907-125">When a device event occurs in an audio endpoint device, the MMDevice module calls the appropriate method in the **IMMNotificationClient** interface of every client that is currently registered to receive device-event notifications.</span></span> <span data-ttu-id="7e907-126">Diese Aufrufe übergeben eine Beschreibung des Ereignisses an die Clients.</span><span class="sxs-lookup"><span data-stu-id="7e907-126">These calls pass a description of the event to the clients.</span></span> <span data-ttu-id="7e907-127">Weitere Informationen finden Sie unter [**immnotificationclient-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="7e907-127">For more information, see [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span>

<span data-ttu-id="7e907-128">Ein Client, der für den Empfang von Benachrichtigungen über Geräte Ereignisse registriert ist, erhält Benachrichtigungen zu allen Arten von Geräte Ereignissen, die auf allen audioendpunktgeräten im System auftreten.</span><span class="sxs-lookup"><span data-stu-id="7e907-128">A client that is registered to receive device-event notifications will receive notifications of all types of device events that occur in all of the audio endpoint devices in the system.</span></span> <span data-ttu-id="7e907-129">Wenn ein Client nur an bestimmten Ereignis Typen oder auf bestimmten Geräten interessiert ist, sollten die Methoden in der **immnotificationclient** -Implementierung die Ereignisse entsprechend filtern.</span><span class="sxs-lookup"><span data-stu-id="7e907-129">If a client is interested only in certain event types or in certain devices, then the methods in its **IMMNotificationClient** implementation should filter the events appropriately.</span></span>

<span data-ttu-id="7e907-130">Die Windows SDK enthält Beispiele, die mehrere Implementierungen für die [**immnotificationclient-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)enthalten.</span><span class="sxs-lookup"><span data-stu-id="7e907-130">The Windows SDK provides samples that include several implementations for the [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span> <span data-ttu-id="7e907-131">Weitere Informationen finden Sie unter [SDK-Beispiele, die die Kerndatei-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md).</span><span class="sxs-lookup"><span data-stu-id="7e907-131">For more information, see [SDK Samples That Use the Core Audio APIs](sdk-samples-that-use-the-core-audio-apis.md).</span></span>

<span data-ttu-id="7e907-132">Im folgenden Codebeispiel wird eine mögliche Implementierung der **immnotificationclient** -Schnittstelle veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="7e907-132">The following code example shows a possible implementation of the **IMMNotificationClient** interface:</span></span>


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



<span data-ttu-id="7e907-133">Die cmmnotificationclient-Klasse im vorangehenden Codebeispiel ist eine Implementierung der **immnotificationclient** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7e907-133">The CMMNotificationClient class in the preceding code example is an implementation of the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="7e907-134">Da **immnotificationclient** von **IUnknown** erbt, enthält die Klassendefinition Implementierungen der **IUnknown** -Methoden **adressf**, **Release** und **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="7e907-134">Because **IMMNotificationClient** inherits from **IUnknown**, the class definition contains implementations of the **IUnknown** methods **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="7e907-135">Die übrigen öffentlichen Methoden in der Klassendefinition sind spezifisch für die **immnotificationclient** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7e907-135">The remaining public methods in the class definition are specific to the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="7e907-136">Diese Methoden werden im Anschluss beschrieben:</span><span class="sxs-lookup"><span data-stu-id="7e907-136">These methods are:</span></span>

-   <span data-ttu-id="7e907-137">**Ondefaultdevicechanged**, das aufgerufen wird, wenn der Benutzer die Geräte Rolle eines audioendpunktgeräts ändert.</span><span class="sxs-lookup"><span data-stu-id="7e907-137">**OnDefaultDeviceChanged**, which is called when the user changes the device role of an audio endpoint device.</span></span>
-   <span data-ttu-id="7e907-138">**Ondeviceadded**, das aufgerufen wird, wenn der Benutzer dem System ein audioendpunktgerät hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="7e907-138">**OnDeviceAdded**, which is called when the user adds an audio endpoint device to the system.</span></span>
-   <span data-ttu-id="7e907-139">**Ondeviceremoved**, das aufgerufen wird, wenn der Benutzer ein audioendpunktgerät aus dem System entfernt.</span><span class="sxs-lookup"><span data-stu-id="7e907-139">**OnDeviceRemoved**, which is called when the user removes an audio endpoint device from the system.</span></span>
-   <span data-ttu-id="7e907-140">**Ondevicestatechanged**, das aufgerufen wird, wenn sich der Gerätestatus eines audioendpunktgeräts ändert.</span><span class="sxs-lookup"><span data-stu-id="7e907-140">**OnDeviceStateChanged**, which is called when the device state of an audio endpoint device changes.</span></span> <span data-ttu-id="7e907-141">(Weitere Informationen zu Geräte Zuständen finden Sie unter [Geräte \_ Status \_ xxx-Konstanten](device-state-xxx-constants.md).)</span><span class="sxs-lookup"><span data-stu-id="7e907-141">(For more information about device states, see [DEVICE\_STATE\_ XXX Constants](device-state-xxx-constants.md).)</span></span>
-   <span data-ttu-id="7e907-142">**OnPropertyValueChanged**, das aufgerufen wird, wenn sich der Wert einer Eigenschaft eines audioendpunkt-Geräts ändert.</span><span class="sxs-lookup"><span data-stu-id="7e907-142">**OnPropertyValueChanged**, which is called when the value of a property of an audio endpoint device changes.</span></span>

<span data-ttu-id="7e907-143">Jede dieser Methoden nimmt einen Eingabeparameter ( *pwstraudeviceid*) an, der ein Zeiger auf eine Endpunkt-ID-Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="7e907-143">Each of these methods takes an input parameter, *pwstrDeviceId*, that is a pointer to an endpoint ID string.</span></span> <span data-ttu-id="7e907-144">Die Zeichenfolge identifiziert das audioendpunktgerät, in dem das Geräte Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7e907-144">The string identifies the audio endpoint device in which the device event occurred.</span></span>

<span data-ttu-id="7e907-145">Im vorangehenden Codebeispiel \_ ist printdevicename eine private Methode in der cmmnotificationclient-Klasse, die den anzeigen amen des Geräts ausgibt.</span><span class="sxs-lookup"><span data-stu-id="7e907-145">In the preceding code example, \_PrintDeviceName is a private method in the CMMNotificationClient class that prints the friendly name of the device.</span></span> <span data-ttu-id="7e907-146">\_Printdevicename nimmt die Endpunkt-ID-Zeichenfolge als Eingabeparameter an.</span><span class="sxs-lookup"><span data-stu-id="7e907-146">\_PrintDeviceName takes the endpoint ID string as an input parameter.</span></span> <span data-ttu-id="7e907-147">Sie übergibt die Zeichenfolge an die [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7e907-147">It passes the string to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="7e907-148">**Getdevice** erstellt ein Endpunkt-Geräte Objekt zur Darstellung des Geräts und stellt die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle für dieses Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="7e907-148">**GetDevice** creates an endpoint device object to represent the device and provides the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface to that object.</span></span> <span data-ttu-id="7e907-149">Als nächstes \_ Ruft printdevicename die Methode " [**immdevice:: openpropertystore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) " auf, um die **IPropertyStore** -Schnittstelle in den Eigenschaften Speicher des Geräts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7e907-149">Next, \_PrintDeviceName calls the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to retrieve the **IPropertyStore** interface to the device's property store.</span></span> <span data-ttu-id="7e907-150">Zum Schluss \_ Ruft printdevicename die **IPropertyStore:: GetItem** -Methode auf, um die Eigenschaft "Anzeige Name" des Geräts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7e907-150">Finally, \_PrintDeviceName calls the **IPropertyStore::GetItem** method to obtain the friendly-name property of the device.</span></span> <span data-ttu-id="7e907-151">Weitere Informationen zu **IPropertyStore** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="7e907-151">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="7e907-152">Zusätzlich zu den Geräte Ereignissen können Clients sich registrieren, um Benachrichtigungen über audiositzungsereignisse und Ereignisse von Endpunkt Ereignissen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="7e907-152">In addition to device events, clients can register to receive notifications of audio-session events and endpoint-volume events.</span></span> <span data-ttu-id="7e907-153">Weitere Informationen finden Sie unter [**iaudiosessionevents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) und [**iaudioendpointvolumecallback-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span><span class="sxs-lookup"><span data-stu-id="7e907-153">For more information, see [**IAudioSessionEvents Interface**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) and [**IAudioEndpointVolumeCallback Interface**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e907-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7e907-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e907-155">Audioendpunktgeräte</span><span class="sxs-lookup"><span data-stu-id="7e907-155">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 




---
title: Auflisten von Windows Media Device Manager-Geräten
description: Auflisten von Geräten
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Windows Media Device Manager, Auflisten von Geräten
- Device Manager, Auflisten von Geräten
- Programmier Handbuch zum Auflisten von Geräten
- Desktop Anwendungen, Auflisten von Geräten
- Erstellen von Windows Media Device Manager-Anwendungen, Auflisten von Geräten
- Auflisten von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3584e625f54ea4e5c601f2a32865515c824cfcd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104101118"
---
# <a name="enumerating-windows-media-device-manager-devices"></a><span data-ttu-id="d3feb-109">Auflisten von Windows Media Device Manager-Geräten</span><span class="sxs-lookup"><span data-stu-id="d3feb-109">Enumerating Windows Media Device Manager devices</span></span>

<span data-ttu-id="d3feb-110">Nachdem Sie eine Anwendung authentifiziert haben, können Sie damit beginnen, die von Windows Media Device Manager erkannten Geräte aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="d3feb-110">After authenticating an application, you can begin to enumerate the devices detected by Windows Media Device Manager.</span></span> <span data-ttu-id="d3feb-111">Die Enumeration erfolgt mithilfe einer Enumerationsschnittstelle ( [**iwmdmenumdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)), die mithilfe von [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) oder [**iwmdebug Manager:: enumdevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d3feb-111">Enumeration is done by using an enumeration interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtained by using either [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) or [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices).</span></span> <span data-ttu-id="d3feb-112">Wenn unterstützt, verwenden Sie die **EnumDevices2** -Methode, da die frühere Version nur Legacy Schnittstellen auf Geräten zurückgegeben hat, während die neue Version sowohl die Legacy-als auch die neue Schnittstelle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d3feb-112">If supported, use the **EnumDevices2** method, because the earlier version only returned legacy interfaces on devices, whereas the new version returns both the legacy and the new interfaces.</span></span>

<span data-ttu-id="d3feb-113">Vor dem Abrufen eines Enumerators sollten Sie entscheiden, welche enumerationsansicht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3feb-113">Before obtaining an enumerator, you should decide what enumeration view to use.</span></span> <span data-ttu-id="d3feb-114">Einige Geräte machen jeden Speicher als ein anderes Gerät verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3feb-114">Some devices expose each storage as a different device.</span></span> <span data-ttu-id="d3feb-115">Beispielsweise werden zwei Flash Speicherkarten auf einem Gerät so aufgelistet, als ob es sich um separate Geräte handelt.</span><span class="sxs-lookup"><span data-stu-id="d3feb-115">For example, two flash memory cards on a device will enumerate as if they were separate devices.</span></span> <span data-ttu-id="d3feb-116">Sie können angeben, dass alle Speicher auf einem Gerät als einzelnes Gerät aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="d3feb-116">You can specify that all storages on a device are enumerated together as a single device.</span></span> <span data-ttu-id="d3feb-117">Sie können diese Einstellung nur einmal in der Anwendung festlegen. Wenn Sie es ändern möchten, müssen Sie die Anwendung Herunterfahren und neu starten.</span><span class="sxs-lookup"><span data-stu-id="d3feb-117">You can set this preference only once in your application; if you want to change it, you must shut down the application and restart it.</span></span> <span data-ttu-id="d3feb-118">Beachten Sie jedoch, dass Legacy Geräte manchmal eine Anforderung ignorieren, separate Gerätespeicher als einzelnes Gerät aufzuzählen und Sie weiterhin separat aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="d3feb-118">However, note that legacy devices will sometimes ignore a request to enumerate separate device storages as a single device, and continue to enumerate them separately.</span></span>

<span data-ttu-id="d3feb-119">Die folgenden Schritte zeigen, wie verbundene Geräte aufgezählt werden:</span><span class="sxs-lookup"><span data-stu-id="d3feb-119">The following steps show how to enumerate connected devices:</span></span>

1.  <span data-ttu-id="d3feb-120">Legen Sie die Einstellung für die Geräte Enumeration mithilfe von [**IWMDeviceManager3:: setdeviceenumpreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference)fest.</span><span class="sxs-lookup"><span data-stu-id="d3feb-120">Set the device enumeration preference using [**IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference).</span></span> <span data-ttu-id="d3feb-121">Wenn diese Methode nicht aufgerufen wird, besteht die Standardmethode darin, Speicher als separate Geräte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d3feb-121">If this method is not called, the default method is to show storages as separate devices.</span></span> <span data-ttu-id="d3feb-122">Um zu ermitteln, ob einzelne "Geräte" tatsächlich auf demselben Gerät Speicher sind, wenden Sie sich an [**IWMDMDevice2:: GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname);. bei Speicher desselben Geräts werden identische Werte zurückgegeben, mit Ausnahme der letzten Ziffer nach dem letzten "$"-Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="d3feb-122">To determine whether individual "devices" are actually storages on the same device, call [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); storages from the same device will return identical values, except for the final digit after the last "$" sign.</span></span>
2.  <span data-ttu-id="d3feb-123">Fragen Sie [**iwmdebug Management Manager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) oder [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)ab, und rufen Sie dann [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) auf, um die Geräte Enumeratorschnittstelle ( [**iwmdmenumdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d3feb-123">Query for [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) or [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2), and then call [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) to obtain the device enumerator interface, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice).</span></span> <span data-ttu-id="d3feb-124">(Falls unterstützt, verwenden Sie **EnumDevices2**, was effizienter ist, da die frühere Version möglicherweise keine MTP-Geräte zurückgibt).</span><span class="sxs-lookup"><span data-stu-id="d3feb-124">(If supported, use **EnumDevices2**, which is more efficient, as the earlier version may not return MTP devices).</span></span>
3.  <span data-ttu-id="d3feb-125">Rufen Sie die [**iwmdmenumschlag:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) -Methode auf, um ein oder mehrere Geräte gleichzeitig abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d3feb-125">Call the [**IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) method to retrieve one or more devices at a time.</span></span> <span data-ttu-id="d3feb-126">Fahren Sie mit der Rückgabe dieser Methode fort, bis die Methode S \_ false oder eine Fehlermeldung zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d3feb-126">Continue to call this method until the method returns S\_FALSE or an error message.</span></span> <span data-ttu-id="d3feb-127">Wenn Sie jeweils nur ein Gerät abrufen, müssen Sie kein Array zum Speichern der Geräte zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d3feb-127">If retrieving only one device at a time, you do not need to allocate an array to hold the devices.</span></span>

<span data-ttu-id="d3feb-128">Da Benutzer während der Ausführung der Anwendung Geräte an den Computer anfügen oder entfernen können, empfiehlt es sich, eine Benachrichtigung über die Geräte Verbindung oder das Entfernen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="d3feb-128">Because users can attach or remove devices from the computer while your application is running, it is a good idea to implement notification of device connection or removal.</span></span> <span data-ttu-id="d3feb-129">Dies erfolgt durch Implementieren der [**iwmdmnotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) -Schnittstelle und deren Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d3feb-129">This is done by implementing the [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) interface and registering it.</span></span> <span data-ttu-id="d3feb-130">Weitere Informationen hierzu finden Sie unter [Aktivieren von Benachrichtigungen](enabling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="d3feb-130">For more information on this, see [Enabling Notifications](enabling-notifications.md).</span></span>

<span data-ttu-id="d3feb-131">Der folgende C++-Code listet Geräte auf und fordert Informationen zu den einzelnen Geräten an.</span><span class="sxs-lookup"><span data-stu-id="d3feb-131">The following C++ code enumerates devices and requests information about each device.</span></span>


```C++
HRESULT CWMDMController::EnumDevices()
{
    HRESULT hr = S_OK;

    // Change behavior to show devices as one object, not each storage as a device.
    // This can be called only once for each instance of this application.
    CComQIPtr<IWMDeviceManager3>pDevMgr3(m_IWMDMDeviceMgr);
    hr = pDevMgr3->SetDeviceEnumPreference(DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES);
    
    // Get number of attached devices.
    DWORD iDevices = 0;
    hr = m_IWMDMDeviceMgr->GetDeviceCount(&iDevices);
    if (hr == S_OK)
    {
        // TODO: Display count of devices.
    }

    //
    // Get a device enumerator to enumerate devices.
    //
    CComPtr<IWMDeviceManager2> pDevMgr2;
    hr = m_IWMDMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pDevMgr2);
    if (hr == S_OK)
    {
        // TODO: Display message indicating that application obtained IWMDeviceManager2.
    }
    else
    {
        // TODO: Display message indicating that we couldn't 
        // get IWMDeviceManager2 in EnumDevices.
        return hr;
    }
   CComPtr<IWMDMEnumDevice> pEnumDevice;
   hr = pDevMgr2->EnumDevices2(&pEnumDevice);
    if (hr != S_OK)
    {
        // TODO: Display messaging indicating that an error occurred 
        // in calling EnumDevices2.
        return hr;
    }

    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;

    // Iterate through devices.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice *pIWMDMDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched);
        if ((hr != S_OK) || (ulFetched != 1))
        {
            break;
        }
        
        // Get a display icon for the device.
        ULONG deviceIcon = 0;
        hr = pIWMDMDevice->GetDeviceIcon(&deviceIcon);

        // Print the device manufacturer.
        WCHAR manufacturer[MAX_CHARS];
        hr = pIWMDMDevice->GetManufacturer((LPWSTR)&manufacturer, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display manufacturer name.
        }

        // Get the device name.
        WCHAR name[MAX_CHARS];
        hr = pIWMDMDevice->GetName((LPWSTR)&name, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display name.
        }

        // TODO: Get other device information if wanted.

        // Obtain an IWMDMDevice2 interface and call some methods.
        CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
        if (pIWMDMDevice2 != NULL)
        {
            // Get the canonical name.
            WCHAR canonicalName[MAX_CHARS];
            hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
            if (hr == S_OK)
            {
                // TODO: Display canonical name.
            }
        }

        // Obtain an IWMDMDevice3 interface and call some methods.
        CComQIPtr<IWMDMDevice3>pIWMDMDevice3(pIWMDMDevice);
        if (pIWMDMDevice3 != NULL)
        {
            // Find out what protocol is being used.
            PROPVARIANT val;
            PropVariantInit(&val);
            hr = pIWMDMDevice3->GetProperty(g_wszWMDMDeviceProtocol, &val);

            if (hr == S_OK)
            {
                if (*val.puuid == WMDM_DEVICE_PROTOCOL_RAPI)
                {
                    // TODO: Display message indicating device is a RAPI device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MTP)
                {
                    / /TODO: Display message indicating device is an MTP device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MSC)
                {
                    // TODO: Display message indicating device is an MSC device.
                }
                else
                {
                    // TODO: Display message indicating that the 
                    // application encountered an unknown protocol.
                }
                PropVariantClear(&val);
            }
        }

        // Examine the device capabilities. You could use some of these
        // to enable or disable the application's UI elements.
        CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
        if (pDeviceControl != NULL)
        {
            DWORD caps = 0;
            hr = pDeviceControl->GetCapabilities(&caps);
            if (caps & WMDM_DEVICECAP_CANPLAY)
            {
                // TODO: Display message indicating that the media 
                // device can play MP3 audio.
            }
            // TODO: Test for other capabilities here.
        }
    } // Get the next device.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d3feb-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3feb-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3feb-133">**Erstellen einer Windows Media Device Manager-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="d3feb-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





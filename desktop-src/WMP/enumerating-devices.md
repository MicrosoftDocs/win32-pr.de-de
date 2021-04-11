---
title: Auflisten von Geräten (WMP SDK)
description: Auflisten von Geräten
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Windows Media Player, portable Geräte
- Windows Media Player-Objektmodell, portable Geräte
- Objektmodell, portable Geräte
- Windows Media Player ActiveX-Steuerelement, portable Geräte
- ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile, tragbare Geräte
- Portable Geräte, auflisten
- Enumerationen, portable Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5025d0e0a7e99028b22cc24ebc56337ea84d2fb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948435"
---
# <a name="enumerating-devices"></a><span data-ttu-id="0ab71-112">Auflisten von Geräten</span><span class="sxs-lookup"><span data-stu-id="0ab71-112">Enumerating Devices</span></span>

<span data-ttu-id="0ab71-113">Windows Media Player stellt tragbare Geräte mithilfe der **iwmpsyncdevice** -Schnittstelle dar.</span><span class="sxs-lookup"><span data-stu-id="0ab71-113">Windows Media Player represents portable devices by using the **IWMPSyncDevice** interface.</span></span> <span data-ttu-id="0ab71-114">Der folgende Beispielcode zeigt eine Funktion, die ein Array von Zeigern auf **iwmpsyncdevice** erstellt.</span><span class="sxs-lookup"><span data-stu-id="0ab71-114">The following example code shows a function that creates an array of pointers to **IWMPSyncDevice**.</span></span> <span data-ttu-id="0ab71-115">Jeder Zeiger im Array stellt ein Gerät dar, für das Windows Media Player über gespeicherte Informationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="0ab71-115">Each pointer in the array represents a device for which Windows Media Player has stored information.</span></span> <span data-ttu-id="0ab71-116">Es ist nicht erforderlich, dass ein Gerät mit dem Computer verbunden ist, und es ist nicht erforderlich, eine Partnerschaft mit der aktuellen Windows Media Player-Instanz zu haben.</span><span class="sxs-lookup"><span data-stu-id="0ab71-116">A device is not required to be connected to the computer, nor is it required to have a partnership with the current Windows Media Player instance.</span></span>

<span data-ttu-id="0ab71-117">Sie sollten Geräte immer dann auflisten, wenn Sie das Ereignis " **de viceconnetct** " oder das Ereignis " **devicedisconnect** " erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ab71-117">You should enumerate devices whenever you receive the **DeviceConnect** event or the **DeviceDisconnect** event.</span></span>

<span data-ttu-id="0ab71-118">Mit der folgenden Funktion werden Geräte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0ab71-118">The following function enumerates devices.</span></span> <span data-ttu-id="0ab71-119">Der *bconnectedonly* -Parameter gibt an, ob nur Geräte aufgelistet werden, die derzeit mit dem Computer des Benutzers verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="0ab71-119">The *bConnectedOnly* parameter specifies whether to enumerate only devices currently connected to the user's computer.</span></span>


```C++
STDMETHODIMP CMainDlg::EnumDevices(BOOL bConnectedOnly)
{
    HRESULT hr = S_OK;
    CComPtr<IWMPSyncServices>  spSyncServices;
    long cDeviceArray = 0;  // Size to make the array
    long cAllDevices = 0;  // Count of all devices
    long cDeviceIndex = 0; // Index for adding devices to array.
    CComPtr<IWMPSyncDevice> spTempDevice;
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;

    // Delete any existing array.
    FreeDeviceArray();

    // Retrieve a pointer to IWMPSyncServices.
    hr = m_spPlayer->QueryInterface(&spSyncServices);

    if(SUCCEEDED(hr) && spSyncServices.p)
    {  
        hr = spSyncServices->get_deviceCount(&cAllDevices);
    }

    if(SUCCEEDED(hr) && cAllDevices > 0)
    {
        if(bConnectedOnly)
        {
            // Count the number of connected devices.
            for(long i = 0; i < cAllDevices; i++)
            {     
                spTempDevice.Release();
                hr = spSyncServices->getDevice(i, &spTempDevice);

                if(SUCCEEDED(hr) && spTempDevice.p)
                {
                    spTempDevice->get_connected(&vbIsConnected);

                    if(vbIsConnected == VARIANT_TRUE)
                    {
                        // Count only the connected devices.
                        cDeviceArray++;
                    }
                }
            }
        }
        else
        {
            cDeviceArray = cAllDevices;
        }

        if(cDeviceArray == 0)
        {
            return hr;
        }

        // Cache the device count.
        m_cDevices = cDeviceArray;

        // Create a new device array.
        m_ppWMPDevices = new IWMPSyncDevice*[cDeviceArray];
        if(!m_ppWMPDevices)
        {
            return E_OUTOFMEMORY;
        }
        
        ZeroMemory(m_ppWMPDevices, sizeof (IWMPSyncDevice*) * cDeviceArray);

        // Fill the array.
        for(long i = 0; i < cAllDevices; i++)
        {
            spTempDevice.Release();
            hr = spSyncServices->getDevice(i, &spTempDevice);
            if(SUCCEEDED(hr) && spTempDevice.p)
            {
                spTempDevice->get_connected(&vbIsConnected);

                if( (bConnectedOnly && vbIsConnected == VARIANT_TRUE) ||
                     !bConnectedOnly )
                {
                    // Add the device to the custom array.
                    spTempDevice.CopyTo(&m_ppWMPDevices[cDeviceIndex++]);
                }
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="0ab71-120">Sie können ähnlichen Code verwenden, um andere Gerätelisten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0ab71-120">You might use similar code to retrieve other such device lists.</span></span> <span data-ttu-id="0ab71-121">Sie können z. b. mit [iwmpsyncdevice:: get \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) ein Array von Geräten erstellen, für die eine Partnerschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ab71-121">For example, you could use [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) to create an array of devices for which a partnership exists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ab71-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0ab71-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ab71-123">**IWMPEvents2::D eviceconnetct**</span><span class="sxs-lookup"><span data-stu-id="0ab71-123">**IWMPEvents2::DeviceConnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[<span data-ttu-id="0ab71-124">**IWMPEvents2::D entfernen**</span><span class="sxs-lookup"><span data-stu-id="0ab71-124">**IWMPEvents2::DeviceDisconnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[<span data-ttu-id="0ab71-125">**Iwmpsyncdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0ab71-125">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="0ab71-126">**Iwmpsyncdevice:: \_ Verbindung herstellen**</span><span class="sxs-lookup"><span data-stu-id="0ab71-126">**IWMPSyncDevice::get\_connected**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[<span data-ttu-id="0ab71-127">**Iwmpsyncservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0ab71-127">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[<span data-ttu-id="0ab71-128">**Arbeiten mit tragbaren Geräten**</span><span class="sxs-lookup"><span data-stu-id="0ab71-128">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 





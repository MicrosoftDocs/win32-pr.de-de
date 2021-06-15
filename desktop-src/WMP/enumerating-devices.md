---
title: Aufzählen von Geräten (WMP SDK)
description: Dieser Beispielcode zeigt eine Funktion, die Geräte aufzählt, indem ein Array von Zeigern erstellt wird, die jeweils ein Gerät darstellen.
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Windows Media Player,portable Geräte
- Windows Media Player Objektmodell, portable Geräte
- Objektmodell, portable Geräte
- Windows Media Player ActiveX-Steuerelement, portable Geräte
- ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile,portable Geräte
- Portable Geräte,Aufzählen
- Enumerationen, portable Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44f71fa26f40983424ced70280d9c03e0892a00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068437"
---
# <a name="enumerating-devices"></a><span data-ttu-id="8ae93-112">Aufzählen von Geräten</span><span class="sxs-lookup"><span data-stu-id="8ae93-112">Enumerating Devices</span></span>

<span data-ttu-id="8ae93-113">Windows Media Player stellt portable Geräte mithilfe der **IWMPSyncDevice-Schnittstelle** dar.</span><span class="sxs-lookup"><span data-stu-id="8ae93-113">Windows Media Player represents portable devices by using the **IWMPSyncDevice** interface.</span></span> <span data-ttu-id="8ae93-114">Der folgende Beispielcode zeigt eine Funktion, die ein Array von Zeigern auf **IWMPSyncDevice erstellt.**</span><span class="sxs-lookup"><span data-stu-id="8ae93-114">The following example code shows a function that creates an array of pointers to **IWMPSyncDevice**.</span></span> <span data-ttu-id="8ae93-115">Jeder Zeiger im Array stellt ein Gerät dar, für das Windows Media Player gespeicherte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="8ae93-115">Each pointer in the array represents a device for which Windows Media Player has stored information.</span></span> <span data-ttu-id="8ae93-116">Ein Gerät muss nicht mit dem Computer verbunden sein, und es ist auch keine Partnerschaft mit der aktuellen Windows Media Player erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ae93-116">A device is not required to be connected to the computer, nor is it required to have a partnership with the current Windows Media Player instance.</span></span>

<span data-ttu-id="8ae93-117">Sie sollten Geräte aufzählen, wenn Sie das **DeviceConnect-Ereignis** oder das **DeviceDisconnect-Ereignis** erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ae93-117">You should enumerate devices whenever you receive the **DeviceConnect** event or the **DeviceDisconnect** event.</span></span>

<span data-ttu-id="8ae93-118">Die folgende Funktion aufzählt Geräte.</span><span class="sxs-lookup"><span data-stu-id="8ae93-118">The following function enumerates devices.</span></span> <span data-ttu-id="8ae93-119">Der *bConnectedOnly-Parameter* gibt an, ob nur Geräte aufzählt werden, die derzeit mit dem Computer des Benutzers verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="8ae93-119">The *bConnectedOnly* parameter specifies whether to enumerate only devices currently connected to the user's computer.</span></span>


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



<span data-ttu-id="8ae93-120">Sie können ähnlichen Code verwenden, um andere solche Gerätelisten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8ae93-120">You might use similar code to retrieve other such device lists.</span></span> <span data-ttu-id="8ae93-121">Beispielsweise können Sie [MITMPSyncDevice::get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) verwenden, um ein Array von Geräten zu erstellen, für die eine Partnerschaft besteht.</span><span class="sxs-lookup"><span data-stu-id="8ae93-121">For example, you could use [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) to create an array of devices for which a partnership exists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ae93-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8ae93-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ae93-123">**IWMPEvents2::D eviceConnect**</span><span class="sxs-lookup"><span data-stu-id="8ae93-123">**IWMPEvents2::DeviceConnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[<span data-ttu-id="8ae93-124">**IWMPEvents2::D eviceDisconnect**</span><span class="sxs-lookup"><span data-stu-id="8ae93-124">**IWMPEvents2::DeviceDisconnect**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[<span data-ttu-id="8ae93-125">**IWMPSyncDevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8ae93-125">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="8ae93-126">**IWMPSyncDevice::get \_ connected**</span><span class="sxs-lookup"><span data-stu-id="8ae93-126">**IWMPSyncDevice::get\_connected**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[<span data-ttu-id="8ae93-127">**IWMPSyncServices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8ae93-127">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[<span data-ttu-id="8ae93-128">**Arbeiten mit portablen Geräten**</span><span class="sxs-lookup"><span data-stu-id="8ae93-128">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 





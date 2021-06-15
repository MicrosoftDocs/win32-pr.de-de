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
# <a name="enumerating-devices"></a>Aufzählen von Geräten

Windows Media Player stellt portable Geräte mithilfe der **IWMPSyncDevice-Schnittstelle** dar. Der folgende Beispielcode zeigt eine Funktion, die ein Array von Zeigern auf **IWMPSyncDevice erstellt.** Jeder Zeiger im Array stellt ein Gerät dar, für das Windows Media Player gespeicherte Informationen enthält. Ein Gerät muss nicht mit dem Computer verbunden sein, und es ist auch keine Partnerschaft mit der aktuellen Windows Media Player erforderlich.

Sie sollten Geräte aufzählen, wenn Sie das **DeviceConnect-Ereignis** oder das **DeviceDisconnect-Ereignis** erhalten.

Die folgende Funktion aufzählt Geräte. Der *bConnectedOnly-Parameter* gibt an, ob nur Geräte aufzählt werden, die derzeit mit dem Computer des Benutzers verbunden sind.


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



Sie können ähnlichen Code verwenden, um andere solche Gerätelisten abzurufen. Beispielsweise können Sie [MITMPSyncDevice::get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) verwenden, um ein Array von Geräten zu erstellen, für die eine Partnerschaft besteht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMPEvents2::D eviceConnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[**IWMPEvents2::D eviceDisconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[**IWMPSyncDevice-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice::get \_ connected**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[**IWMPSyncServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[**Arbeiten mit portablen Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 





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
# <a name="enumerating-devices"></a>Auflisten von Geräten

Windows Media Player stellt tragbare Geräte mithilfe der **iwmpsyncdevice** -Schnittstelle dar. Der folgende Beispielcode zeigt eine Funktion, die ein Array von Zeigern auf **iwmpsyncdevice** erstellt. Jeder Zeiger im Array stellt ein Gerät dar, für das Windows Media Player über gespeicherte Informationen verfügt. Es ist nicht erforderlich, dass ein Gerät mit dem Computer verbunden ist, und es ist nicht erforderlich, eine Partnerschaft mit der aktuellen Windows Media Player-Instanz zu haben.

Sie sollten Geräte immer dann auflisten, wenn Sie das Ereignis " **de viceconnetct** " oder das Ereignis " **devicedisconnect** " erhalten.

Mit der folgenden Funktion werden Geräte aufgelistet. Der *bconnectedonly* -Parameter gibt an, ob nur Geräte aufgelistet werden, die derzeit mit dem Computer des Benutzers verbunden sind.


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



Sie können ähnlichen Code verwenden, um andere Gerätelisten abzurufen. Sie können z. b. mit [iwmpsyncdevice:: get \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) ein Array von Geräten erstellen, für die eine Partnerschaft vorhanden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMPEvents2::D eviceconnetct**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[**IWMPEvents2::D entfernen**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[**Iwmpsyncdevice-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Iwmpsyncdevice:: \_ Verbindung herstellen**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[**Iwmpsyncservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[**Arbeiten mit tragbaren Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 





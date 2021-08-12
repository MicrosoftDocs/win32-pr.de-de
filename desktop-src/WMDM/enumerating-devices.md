---
title: Aufzählen Windows Medien Geräte-Manager Mediengeräten
description: Erfahren Sie mehr über das Auflisten der geräte, die von Windows Media Geräte-Manager mithilfe einer Enumerationsschnittstelle erkannt wurden.
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Windows Medien Geräte-Manager,Aufzählen von Geräten
- Geräte-Manager,Aufzählen von Geräten
- Programmierhandbuch,Aufzählen von Geräten
- Desktopanwendungen,Aufzählen von Geräten
- Erstellen Windows Media Geräte-Manager-Anwendungen,Aufzählen von Geräten
- Aufzählen von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0009e2206bf7c97839d890d00c08a8e1806196efee9af95db72336b95d8b2cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584658"
---
# <a name="enumerating-windows-media-device-manager-devices"></a>Aufzählen Windows Medien Geräte-Manager Mediengeräten

Nach der Authentifizierung einer Anwendung können Sie mit dem Aufzählen der Geräte beginnen, die von Windows Media Geräte-Manager. Die Enumeration erfolgt mithilfe der Enumerationsschnittstelle [**IWMDMEnumDevice,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)die entweder mithilfe von [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) oder [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices)abgerufen wird. Wenn dies unterstützt wird, verwenden Sie die **EnumDevices2-Methode,** da die frühere Version nur Legacyschnittstellen auf Geräten zurückgegeben hat, während die neue Version sowohl die Legacy- als auch die neuen Schnittstellen zurückgibt.

Vor dem Abrufen eines Enumerators müssen Sie entscheiden, welche Enumerationsansicht verwendet werden soll. Einige Geräte machen jeden Speicher als anderes Gerät verfügbar. Beispielsweise werden zwei Flash-Speicherkarten auf einem Gerät so aufzählt, als ob es sich um separate Geräte wäre. Sie können angeben, dass alle Speicher auf einem Gerät zusammen als einzelnes Gerät aufzählt werden. Sie können diese Einstellung nur einmal in Ihrer Anwendung festlegen. Wenn Sie sie ändern möchten, müssen Sie die Anwendung herunterfahren und neu starten. Beachten Sie jedoch, dass ältere Geräte manchmal eine Anforderung ignorieren, separate Gerätespeicher als einzelnes Gerät aufzählen und diese weiterhin separat aufzählen.

Die folgenden Schritte zeigen, wie verbundene Geräte aufzählt werden:

1.  Legen Sie die Einstellung für die [**Geräteenumeration mithilfe von IWMDeviceManager3::SetDeviceEnumPreference fest.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference) Wenn diese Methode nicht aufgerufen wird, werden Speicher standardmäßig als separate Geräte angezeigt. Um festzustellen, ob einzelne "Geräte" tatsächlich Speicher auf demselben Gerät sind, rufen [**Sie IWMDMDevice2::GetCanonicalName auf.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname) Speicher vom selben Gerät geben identische Werte zurück, mit Ausnahme der letzten Ziffer nach dem letzten "$"-Zeichen.
2.  Fragen Sie [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) oder [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)ab, und rufen Sie [**dann IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) auf, um die Geräteenumeratorschnittstelle [**IWMDMEnumDevice abzurufen.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice) (Wenn dies unterstützt wird, verwenden Sie **EnumDevices2**. Dies ist effizienter, da die frühere Version möglicherweise keine MTP-Geräte zurück gibt).
3.  Rufen Sie [**die IWMDMEnumDevices::Next-Methode**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) auf, um ein oder mehrere Geräte gleichzeitig abzurufen. Fahren Sie mit dem Aufrufen dieser Methode fort, bis die Methode S \_ FALSE oder eine Fehlermeldung zurückgibt. Wenn Sie immer nur ein Gerät gleichzeitig abrufen, müssen Sie kein Array zuordnen, um die Geräte zu speichern.

Da Benutzer Geräte an den Computer anfügen oder vom Computer entfernen können, während Ihre Anwendung ausgeführt wird, ist es eine gute Idee, eine Benachrichtigung über die Geräteverbindung oder das Entfernen zu implementieren. Dies erfolgt, indem die [**IWMDMNotification-Schnittstelle implementiert**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) und registriert wird. Weitere Informationen hierzu finden Sie unter Aktivieren [von Benachrichtigungen.](enabling-notifications.md)

Der folgende C++-Code aufzählt Geräte und fordert Informationen zu jedem Gerät an.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Geräte-Manager Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





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
# <a name="enumerating-windows-media-device-manager-devices"></a>Auflisten von Windows Media Device Manager-Geräten

Nachdem Sie eine Anwendung authentifiziert haben, können Sie damit beginnen, die von Windows Media Device Manager erkannten Geräte aufzuzählen. Die Enumeration erfolgt mithilfe einer Enumerationsschnittstelle ( [**iwmdmenumdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)), die mithilfe von [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) oder [**iwmdebug Manager:: enumdevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices)abgerufen wurde. Wenn unterstützt, verwenden Sie die **EnumDevices2** -Methode, da die frühere Version nur Legacy Schnittstellen auf Geräten zurückgegeben hat, während die neue Version sowohl die Legacy-als auch die neue Schnittstelle zurückgibt.

Vor dem Abrufen eines Enumerators sollten Sie entscheiden, welche enumerationsansicht verwendet werden soll. Einige Geräte machen jeden Speicher als ein anderes Gerät verfügbar. Beispielsweise werden zwei Flash Speicherkarten auf einem Gerät so aufgelistet, als ob es sich um separate Geräte handelt. Sie können angeben, dass alle Speicher auf einem Gerät als einzelnes Gerät aufgelistet werden. Sie können diese Einstellung nur einmal in der Anwendung festlegen. Wenn Sie es ändern möchten, müssen Sie die Anwendung Herunterfahren und neu starten. Beachten Sie jedoch, dass Legacy Geräte manchmal eine Anforderung ignorieren, separate Gerätespeicher als einzelnes Gerät aufzuzählen und Sie weiterhin separat aufzuzählen.

Die folgenden Schritte zeigen, wie verbundene Geräte aufgezählt werden:

1.  Legen Sie die Einstellung für die Geräte Enumeration mithilfe von [**IWMDeviceManager3:: setdeviceenumpreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference)fest. Wenn diese Methode nicht aufgerufen wird, besteht die Standardmethode darin, Speicher als separate Geräte anzuzeigen. Um zu ermitteln, ob einzelne "Geräte" tatsächlich auf demselben Gerät Speicher sind, wenden Sie sich an [**IWMDMDevice2:: GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname);. bei Speicher desselben Geräts werden identische Werte zurückgegeben, mit Ausnahme der letzten Ziffer nach dem letzten "$"-Vorzeichen.
2.  Fragen Sie [**iwmdebug Management Manager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) oder [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)ab, und rufen Sie dann [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) auf, um die Geräte Enumeratorschnittstelle ( [**iwmdmenumdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)) abzurufen. (Falls unterstützt, verwenden Sie **EnumDevices2**, was effizienter ist, da die frühere Version möglicherweise keine MTP-Geräte zurückgibt).
3.  Rufen Sie die [**iwmdmenumschlag:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) -Methode auf, um ein oder mehrere Geräte gleichzeitig abzurufen. Fahren Sie mit der Rückgabe dieser Methode fort, bis die Methode S \_ false oder eine Fehlermeldung zurückgibt. Wenn Sie jeweils nur ein Gerät abrufen, müssen Sie kein Array zum Speichern der Geräte zuordnen.

Da Benutzer während der Ausführung der Anwendung Geräte an den Computer anfügen oder entfernen können, empfiehlt es sich, eine Benachrichtigung über die Geräte Verbindung oder das Entfernen zu implementieren. Dies erfolgt durch Implementieren der [**iwmdmnotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) -Schnittstelle und deren Registrierung. Weitere Informationen hierzu finden Sie unter [Aktivieren von Benachrichtigungen](enabling-notifications.md).

Der folgende C++-Code listet Geräte auf und fordert Informationen zu den einzelnen Geräten an.


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

[**Erstellen einer Windows Media Device Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





---
title: Behandeln von geschützten Inhalten in der Anwendung
description: Behandeln von geschützten Inhalten in der Anwendung
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Medien Geräte-Manager,Zertifikate
- Geräte-Manager, Zertifikate
- Programmierhandbuch,Zertifikate
- Desktopanwendungen, Zertifikate
- Erstellen von Windows Media Geräte-Manager-Anwendungen,Zertifikaten
- certificates
- Windows Medien Geräte-Manager, DRM-geschützte Inhalte
- Geräte-Manager, DRM-geschützter Inhalt
- Programmierhandbuch, DRM-geschützter Inhalt
- Desktopanwendungen, DRM-geschützte Inhalte
- Erstellen von Windows Media Geräte-Manager-Anwendungen, DRM-geschützten Inhalten
- DRM-geschützter Inhalt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0befd0eb9fe2fecf06235b0b9424776ed25f3b1c411439cac5ecdfa71910d16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957370"
---
# <a name="handling-protected-content-in-the-application"></a>Behandeln von geschützten Inhalten in der Anwendung

\[Die Windows Medien-DRM-Funktion ist veraltet und sollte nicht verwendet werden. Verwenden Sie stattdessen [Microsoft PlayReady.](/windows/uwp/audio-video-camera/playready-client-sdk)\]

Eine Anwendung muss über ein Übertragungszertifikat verfügen, um DRM-geschützte Inhalte verarbeiten zu können. Informationen zum Abrufen dieses Zertifikats finden Sie unter [Tools for Development](tools-for-development.md). Für die Behandlung von ungeschütztem Inhalt können Sie ein Dummyzertifikat verwenden, wie unter [Authentifizieren der Anwendung](authenticating-the-application.md)beschrieben.

Vor der Verwendung eines Geräts sollte Ihre Anwendung bestimmen, ob das Gerät Windows Medien-DRM 10 für portable Geräte unterstützt, und wenn ja, ob die DRM-Komponenten aktuell sind. (Aktuell bedeutet, dass die sichere Uhr richtig ist und dass das Gerät ordnungsgemäß individualisiert wurde.) Wenn das Gerät diese Version von DRM nicht unterstützt oder nicht aktualisiert werden kann, können Sie weiterhin Dateien an das Gerät senden, die jedoch je nach Lizenzversion möglicherweise nicht wiedergegeben werden können.

> [!Note]  
> Die Individualisierung von Geräten wird derzeit nicht unterstützt.

 

Wenn Ihre Anwendung mit Windows Medienformat-SDK-Methoden verknüpft wird, muss sie mit der bibliothek WMStubDRM.lib Windows Medienformat verknüpft werden. Weitere Informationen zum Aufrufen Windows Medienformatmethoden für DRM-geschützte Inhalte finden Sie in der Dokumentation zum Windows Media Format SDK unter "Enabling DRM Support" (Aktivieren der DRM-Unterstützung). Beachten Sie, dass beim Verknüpfen mit Mssachlp.lib und WMStubDRM.lib ein Problem auftritt. Dies wird im [KB-Artikel 890079 auf MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079)behandelt.

Im folgenden C++-Codebeispiel wird bestimmt, ob es sich bei einem Gerät um ein Windows Media DRM 10-Gerät handelt und, falls ja, ob die Uhr auf dem neuesten Stand ist.

`HRESULT IsDRMClockUpToDate()`


```C++
{
    HRESULT hr = S_OK;

    // Create the DRM handler class.
    CComPtr<IWMDRMDeviceApp> pDRM;
    hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

    // Find out first if the device is a WMDRM 10 device, and if so,
    // whether it requires clock updates.
    DWORD status = 0;
    hr = pDRM->QueryDeviceStatus(pDevice, &status);

    if (FAILED(hr)
       || (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. 
       || (status & WMDRM_DEVICE_REVOKED))   // Device is revoked.
    {
        return E_FAIL;
    }
    else if (status & WMDRM_DEVICE_NEEDCLOCK || 
        status & WMDRM_DEVICE_REFRESHCLOCK)
    {
        // Attempt update. See following example.
        hr = UpdateDRM(status);
    }
    return hr;
}
```



Wenn das Gerät Windows Medien-DRM 10 für portable Geräte unterstützt und aktualisiert werden muss (d. h. wenn der *Statuswert* im vorherigen Beispiel nicht einfach WMDM \_ DEVICE \_ ISWMDRM lautet), sollte die Anwendung [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) aufrufen und den Wert des *Status* übergeben, um die erforderlichen Updates auszuführen. Der Desktopcomputer muss mit dem Internet verbunden sein.

Die folgende C++-Beispielfunktion versucht, ein DRM-Gerät zu aktualisieren.


```C++
HRESULT UpdateDRM(DWORD status)
{
    HRESULT hr = S_OK;
    hr = pDRM->AcquireDeviceData(pDevice, this, status, &result);
    if (hr != S_OK || result != 0)
    {
            return E_FAIL;
    }
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Geräte-Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Behandeln von geschützten Inhalten**](handling-protected-content.md)
</dt> </dl>

 

 
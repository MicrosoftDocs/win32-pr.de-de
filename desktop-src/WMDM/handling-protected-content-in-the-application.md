---
title: Behandeln geschützter Inhalte in der Anwendung
description: Behandeln geschützter Inhalte in der Anwendung
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Media Device Manager, Zertifikate
- Device Manager, Zertifikate
- Programmier Handbuch, Zertifikate
- Desktop Anwendungen, Zertifikate
- Erstellen von Windows Media Device Manager-Anwendungen,-Zertifikaten
- certificates
- Windows Media Device Manager, DRM-geschützter Inhalt
- Device Manager, DRM-geschützter Inhalt
- Programmier Handbuch, DRM-geschützter Inhalt
- Desktop Anwendungen, DRM-geschützter Inhalt
- Erstellen von Windows Media Device Manager-Anwendungen, DRM-geschütztem Inhalt
- DRM-geschützter Inhalt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340516"
---
# <a name="handling-protected-content-in-the-application"></a>Behandeln geschützter Inhalte in der Anwendung

\[Das Windows Media DRM-Feature ist veraltet und sollte nicht verwendet werden. Verwenden Sie stattdessen [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Eine Anwendung muss über ein Übertragungs Zertifikat verfügen, um durch DRM geschützte Inhalte verarbeiten zu können. Informationen dazu, wo Sie dieses Zertifikat erhalten, finden Sie unter [Tools für die Entwicklung](tools-for-development.md). Zum Verarbeiten von ungeschütztem Inhalt können Sie ein dummyzertifikat verwenden, wie unter [Authentifizieren der Anwendung](authenticating-the-application.md)beschrieben.

Vor der Verwendung eines Geräts sollte Ihre Anwendung bestimmen, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt, und wenn ja, dass die DRM-Komponenten aktuell sind. (Aktuell bedeutet das, dass die sichere Uhr korrekt ist und dass das Gerät ordnungsgemäß individualisiert wurde.) Wenn das Gerät diese DRM-Version nicht unterstützt, oder wenn es nicht aktualisiert werden kann, können Sie weiterhin Dateien an das Gerät senden, Sie können jedoch je nach Lizenz Version möglicherweise nicht mehr verwendet werden.

> [!Note]  
> Die individuelle Personalisierung von Geräten wird derzeit nicht unterstützt.

 

Wenn Ihre Anwendung mit den Windows Media-Format-SDK-Methoden verknüpft ist, muss Sie mit der Windows Media-Format Bibliothek wmstubdrm. lib verknüpft werden. Weitere Informationen zum Aufrufen von Windows Media-Methoden auf DRM-geschützten Inhalten finden Sie unter "Aktivieren der DRM-Unterstützung" in der Dokumentation zum Windows Media-Format-SDK. Beachten Sie, dass ein Problem mit dem Verknüpfen mit mssachlp. lib und wmstubdrm. lib vorliegt. Dies wird im [KB-Artikel 890079 auf MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079)behandelt.

Im folgenden C++-Codebeispiel wird festgelegt, ob ein Gerät ein Windows Media DRM 10-Gerät ist, und wenn dies der Fall ist, ist die Uhr auf dem neuesten Stand.

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



Wenn das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt und aktualisiert werden muss (das heißt, wenn der Wert des *Status* im vorherigen Beispiel nicht einfach WMDM- \_ Gerät \_ iswmdrm ist), sollte die Anwendung [**iwmdrmdeviceapp:: acquiredevicedata**](iwmdrmdeviceapp-acquiredevicedata.md) aufrufen und den Wert von *Status* übergeben, um die erforderlichen Updates auszuführen. Der Desktop Computer muss mit dem Internet verbunden sein.

Die folgende C++-Beispiel Funktion versucht, ein DRM-Gerät zu aktualisieren.


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

[**Erstellen einer Windows Media Device Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Behandeln geschützter Inhalte**](handling-protected-content.md)
</dt> </dl>

 

 
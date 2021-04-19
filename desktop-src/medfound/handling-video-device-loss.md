---
description: In diesem Thema wird beschrieben, wie Geräte Verluste bei der Verwendung eines Video Aufzeichnungs Geräts erkannt werden.
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: Verarbeiten von Video Geräte Verlusten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d083ebeb1203b0bba49a63745f62a4dff6b231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350518"
---
# <a name="handling-video-device-loss"></a>Verarbeiten von Video Geräte Verlusten

In diesem Thema wird beschrieben, wie Geräte Verluste bei der Verwendung eines Video Aufzeichnungs Geräts erkannt werden. Sie enthält die folgenden Abschnitte:

-   [Für Geräte Benachrichtigung registrieren](#register-for-device-notification)
-   [Den symbolischen Link des Geräts erhalten](#get-the-symbolic-link-of-the-device)
-   [Behandeln von WM \_ devicechange](/windows)
-   [Registrierung für Benachrichtigung aufheben](#unregister-for-notification)
-   [Zugehörige Themen](#related-topics)

## <a name="register-for-device-notification"></a>Für Geräte Benachrichtigung registrieren

Bevor Sie mit der Erfassung vom Gerät beginnen, müssen Sie die [**registerdevicenotifi-**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) Funktion aufrufen, um sich für Geräte Benachrichtigungen zu registrieren. Registrieren Sie sich für die **kscategory- \_ Erfassungs** Geräteklasse, wie im folgenden Code gezeigt.


```C++
#include <Dbt.h>
#include <ks.h>
#include <ksmedia.h>

HDEVNOTIFY  g_hdevnotify = NULL;

BOOL RegisterForDeviceNotification(HWND hwnd)
{
    DEV_BROADCAST_DEVICEINTERFACE di = { 0 };
    di.dbcc_size = sizeof(di);
    di.dbcc_devicetype  = DBT_DEVTYP_DEVICEINTERFACE;
    di.dbcc_classguid  = KSCATEGORY_CAPTURE; 

    g_hdevnotify = RegisterDeviceNotification(
        hwnd,
        &di,
        DEVICE_NOTIFY_WINDOW_HANDLE
        );

    if (g_hdevnotify == NULL)
    {
        return FALSE;
    }

    return TRUE;
}
```



## <a name="get-the-symbolic-link-of-the-device"></a>Den symbolischen Link des Geräts erhalten

Zählen Sie die Videogeräte auf dem System auf, wie unter Auflisten von [Video Erfassungs Geräten](enumerating-video-capture-devices.md)beschrieben. Wählen Sie ein Gerät aus der Liste aus, und Fragen Sie dann das Aktivierungs Objekt für das Attribut [ \_ \_ \_ \_ Quelltyp " \_ VidCap \_ \_ " des MF-devsource-Attributs](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) ab, wie im folgenden Code gezeigt.


```C++
WCHAR      *g_pwszSymbolicLink = NULL;
UINT32     g_cchSymbolicLink = 0;

HRESULT GetSymbolicLink(IMFActivate *pActivate)
{
    return pActivate->GetAllocatedString(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
        &g_pwszSymbolicLink,
        &g_cchSymbolicLink
        );
}
```



## <a name="handle-wm_devicechange"></a>Behandeln von WM \_ devicechange

Lauschen Sie in der Nachrichten Schleife auf " [**WM \_ devicechange**](../devio/wm-devicechange.md) "-Nachrichten. Der *LPARAM* -Nachrichten Parameter ist ein Zeiger auf eine Entwicklungs- [**\_ Broadcast- \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) -Struktur.


```C++
    case WM_DEVICECHANGE:
        if (lParam != 0)
        {
            HRESULT hr = S_OK;
            BOOL bDeviceLost = FALSE;

            hr = CheckDeviceLost((PDEV_BROADCAST_HDR)lParam, &bDeviceLost);

            if (FAILED(hr) || bDeviceLost)
            {
                CloseDevice();

                MessageBox(hwnd, L"Lost the capture device.", NULL, MB_OK);
            }
        }
        return TRUE;
```



Vergleichen Sie als nächstes die Geräte Benachrichtigungs Meldung mit der symbolischen Verknüpfung Ihres Geräts wie folgt:

1.  Überprüfen Sie das dbch-Element " **\_ tvicetype** " der Entwicklungs [**Broadcast- \_ \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) -Struktur. Wenn der Wert **DBT \_ devd \_ deviceinterface** ist, wandeln Sie den Struktur Zeiger in eine [**dev \_ Broadcast \_ deviceinterface**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) -Struktur um.
2.  Vergleicht den **DBCC \_ Name** -Member dieser Struktur mit der symbolischen Verknüpfung des Geräts.


```C++
HRESULT CheckDeviceLost(DEV_BROADCAST_HDR *pHdr, BOOL *pbDeviceLost)
{
    DEV_BROADCAST_DEVICEINTERFACE *pDi = NULL;

    if (pbDeviceLost == NULL)
    {
        return E_POINTER;
    }

    *pbDeviceLost = FALSE;
    
    if (g_pSource == NULL)
    {
        return S_OK;
    }
    if (pHdr == NULL)
    {
        return S_OK;
    }
    if (pHdr->dbch_devicetype != DBT_DEVTYP_DEVICEINTERFACE)
    {
        return S_OK;
    }

    // Compare the device name with the symbolic link.

    pDi = (DEV_BROADCAST_DEVICEINTERFACE*)pHdr;

    if (g_pwszSymbolicLink)
    {
        if (_wcsicmp(g_pwszSymbolicLink, pDi->dbcc_name) == 0)
        {
            *pbDeviceLost = TRUE;
        }
    }

    return S_OK;
}
```



## <a name="unregister-for-notification"></a>Registrierung für Benachrichtigung aufheben

Bevor die Anwendung beendet wird, wird [**unregisterdevicenotifiaufgerufen**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) , um die Registrierung für Geräte Benachrichtigungen aufzuheben/


```C++
void OnClose(HWND /*hwnd*/)
{
    if (g_hdevnotify)
    {
        UnregisterDeviceNotification(g_hdevnotify);
    }

    PostQuitMessage(0);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auflisten von Video Erfassungs Geräten](enumerating-video-capture-devices.md)
</dt> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 

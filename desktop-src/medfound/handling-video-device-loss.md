---
description: In diesem Thema wird beschrieben, wie Geräteverluste bei Verwendung eines Videoaufnahmegeräts erkannt werden.
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: Behandeln von Videogeräteverlusten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6219518d3018aae5600e66387363bbd71e29e72b83174b370bf25377c8c6b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878952"
---
# <a name="handling-video-device-loss"></a>Behandeln von Videogeräteverlusten

In diesem Thema wird beschrieben, wie Geräteverluste bei Verwendung eines Videoaufnahmegeräts erkannt werden. Sie enthält die folgenden Abschnitte:

-   [Registrieren für Gerätebenachrichtigungen](#register-for-device-notification)
-   [Abrufen der symbolischen Verknüpfung des Geräts](#get-the-symbolic-link-of-the-device)
-   [Behandeln von WM \_ DEVICECHANGE](/windows)
-   [Aufheben der Registrierung für Benachrichtigungen](#unregister-for-notification)
-   [Zugehörige Themen](#related-topics)

## <a name="register-for-device-notification"></a>Registrieren für Gerätebenachrichtigungen

Bevor Sie mit der Erfassung vom Gerät beginnen, rufen Sie die [**RegisterDeviceNotification-Funktion**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) auf, um sich für Gerätebenachrichtigungen zu registrieren. Registrieren Sie sich für die **KSCATEGORY \_ CAPTURE-Geräteklasse,** wie im folgenden Code gezeigt.


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



## <a name="get-the-symbolic-link-of-the-device"></a>Abrufen der symbolischen Verknüpfung des Geräts

Aufzählen der Videogeräte auf dem System, wie unter [Aufzählen von Videoaufnahmegeräten](enumerating-video-capture-devices.md)beschrieben. Wählen Sie ein Gerät aus der Liste aus, und fragen Sie dann das Aktivierungsobjekt nach dem [ATTRIBUT MF \_ DEVSOURCE ATTRIBUTE SOURCE TYPE \_ \_ \_ \_ VIDCAP \_ SYMBOLIC \_ LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) ab, wie im folgenden Code gezeigt.


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



## <a name="handle-wm_devicechange"></a>Behandeln von WM \_ DEVICECHANGE

Lauschen Sie in der Nachrichtenschleife auf [**WM \_ DEVICECHANGE-Nachrichten.**](../devio/wm-devicechange.md) Der *lParam-Nachrichtenparameter* ist ein Zeiger auf eine [**DEV BROADCAST \_ \_ HDR-Struktur.**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr)


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



Vergleichen Sie als Nächstes die Benachrichtigungsmeldung des Geräts wie folgt mit der symbolischen Verknüpfung Ihres Geräts:

1.  Überprüfen Sie den **dbch \_ devicetype-Member** der [**DEV BROADCAST \_ \_ HDR-Struktur.**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) Wenn der Wert **DBT \_ DEVTYP \_ DEVICEINTERFACE** ist, casten Sie den Strukturzeiger in eine [**DEV BROADCAST \_ \_ DEVICEINTERFACE-Struktur.**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a)
2.  Vergleichen Sie den **dbcc \_ name-Member** dieser -Struktur mit der symbolischen Verknüpfung des Geräts.


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



## <a name="unregister-for-notification"></a>Aufheben der Registrierung für Benachrichtigungen

Rufen Sie vor dem Beenden der Anwendung [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) auf, um die Registrierung für Gerätebenachrichtigungen zu aufheben.


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

[Aufzählen von Videoaufnahmegeräten](enumerating-video-capture-devices.md)
</dt> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 

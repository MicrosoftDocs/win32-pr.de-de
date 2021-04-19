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
# <a name="handling-video-device-loss"></a><span data-ttu-id="2f9d0-103">Verarbeiten von Video Geräte Verlusten</span><span class="sxs-lookup"><span data-stu-id="2f9d0-103">Handling Video Device Loss</span></span>

<span data-ttu-id="2f9d0-104">In diesem Thema wird beschrieben, wie Geräte Verluste bei der Verwendung eines Video Aufzeichnungs Geräts erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-104">This topic describes how to detect device loss when using a video capture device.</span></span> <span data-ttu-id="2f9d0-105">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="2f9d0-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="2f9d0-106">Für Geräte Benachrichtigung registrieren</span><span class="sxs-lookup"><span data-stu-id="2f9d0-106">Register For Device Notification</span></span>](#register-for-device-notification)
-   [<span data-ttu-id="2f9d0-107">Den symbolischen Link des Geräts erhalten</span><span class="sxs-lookup"><span data-stu-id="2f9d0-107">Get the Symbolic Link of the Device</span></span>](#get-the-symbolic-link-of-the-device)
-   [<span data-ttu-id="2f9d0-108">Behandeln von WM \_ devicechange</span><span class="sxs-lookup"><span data-stu-id="2f9d0-108">Handle WM\_DEVICECHANGE</span></span>](/windows)
-   [<span data-ttu-id="2f9d0-109">Registrierung für Benachrichtigung aufheben</span><span class="sxs-lookup"><span data-stu-id="2f9d0-109">Unregister For Notification</span></span>](#unregister-for-notification)
-   [<span data-ttu-id="2f9d0-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f9d0-110">Related topics</span></span>](#related-topics)

## <a name="register-for-device-notification"></a><span data-ttu-id="2f9d0-111">Für Geräte Benachrichtigung registrieren</span><span class="sxs-lookup"><span data-stu-id="2f9d0-111">Register For Device Notification</span></span>

<span data-ttu-id="2f9d0-112">Bevor Sie mit der Erfassung vom Gerät beginnen, müssen Sie die [**registerdevicenotifi-**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) Funktion aufrufen, um sich für Geräte Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-112">Before you start capturing from the device, call the [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) function to register for device notifications.</span></span> <span data-ttu-id="2f9d0-113">Registrieren Sie sich für die **kscategory- \_ Erfassungs** Geräteklasse, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-113">Register for the **KSCATEGORY\_CAPTURE** device class, as shown in the following code.</span></span>


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



## <a name="get-the-symbolic-link-of-the-device"></a><span data-ttu-id="2f9d0-114">Den symbolischen Link des Geräts erhalten</span><span class="sxs-lookup"><span data-stu-id="2f9d0-114">Get the Symbolic Link of the Device</span></span>

<span data-ttu-id="2f9d0-115">Zählen Sie die Videogeräte auf dem System auf, wie unter Auflisten von [Video Erfassungs Geräten](enumerating-video-capture-devices.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-115">Enumerate the video devices on the system, as described in [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span> <span data-ttu-id="2f9d0-116">Wählen Sie ein Gerät aus der Liste aus, und Fragen Sie dann das Aktivierungs Objekt für das Attribut [ \_ \_ \_ \_ Quelltyp " \_ VidCap \_ \_ " des MF-devsource-Attributs](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) ab, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-116">Choose a device from the list, and then query the activation object for the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute, as shown in the following code.</span></span>


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



## <a name="handle-wm_devicechange"></a><span data-ttu-id="2f9d0-117">Behandeln von WM \_ devicechange</span><span class="sxs-lookup"><span data-stu-id="2f9d0-117">Handle WM\_DEVICECHANGE</span></span>

<span data-ttu-id="2f9d0-118">Lauschen Sie in der Nachrichten Schleife auf " [**WM \_ devicechange**](../devio/wm-devicechange.md) "-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-118">In your message loop, listen for [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) messages.</span></span> <span data-ttu-id="2f9d0-119">Der *LPARAM* -Nachrichten Parameter ist ein Zeiger auf eine Entwicklungs- [**\_ Broadcast- \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-119">The *lParam* message parameter is a pointer to a [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span>


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



<span data-ttu-id="2f9d0-120">Vergleichen Sie als nächstes die Geräte Benachrichtigungs Meldung mit der symbolischen Verknüpfung Ihres Geräts wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2f9d0-120">Next, compare the device notification message against the symbolic link of your device, as follows:</span></span>

1.  <span data-ttu-id="2f9d0-121">Überprüfen Sie das dbch-Element " **\_ tvicetype** " der Entwicklungs [**Broadcast- \_ \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-121">Check the **dbch\_devicetype** member of the [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="2f9d0-122">Wenn der Wert **DBT \_ devd \_ deviceinterface** ist, wandeln Sie den Struktur Zeiger in eine [**dev \_ Broadcast \_ deviceinterface**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) -Struktur um.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-122">If the value is **DBT\_DEVTYP\_DEVICEINTERFACE**, cast the structure pointer to a [**DEV\_BROADCAST\_DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) structure.</span></span>
2.  <span data-ttu-id="2f9d0-123">Vergleicht den **DBCC \_ Name** -Member dieser Struktur mit der symbolischen Verknüpfung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-123">Compare the **dbcc\_name** member of this structure to the symbolic link of the device.</span></span>


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



## <a name="unregister-for-notification"></a><span data-ttu-id="2f9d0-124">Registrierung für Benachrichtigung aufheben</span><span class="sxs-lookup"><span data-stu-id="2f9d0-124">Unregister For Notification</span></span>

<span data-ttu-id="2f9d0-125">Bevor die Anwendung beendet wird, wird [**unregisterdevicenotifiaufgerufen**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) , um die Registrierung für Geräte Benachrichtigungen aufzuheben/</span><span class="sxs-lookup"><span data-stu-id="2f9d0-125">Before the application exits, call [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) to unregister for device notifications/</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2f9d0-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f9d0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f9d0-127">Auflisten von Video Erfassungs Geräten</span><span class="sxs-lookup"><span data-stu-id="2f9d0-127">Enumerating Video Capture Devices</span></span>](enumerating-video-capture-devices.md)
</dt> <dt>

[<span data-ttu-id="2f9d0-128">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="2f9d0-128">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 

---
description: Beschreibt die Benachrichtigung, die an die Rückruffunktion für die WFD- \_ Anzeige- \_ Senke- \_ Benachrichtigung \_
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: WFD_DISPLAY_SINK_NOTIFICATION-Struktur (WF-Sink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357731"
---
# <a name="wfd_display_sink_notification-structure"></a><span data-ttu-id="6fca1-103">WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs Struktur</span><span class="sxs-lookup"><span data-stu-id="6fca1-103">WFD\_DISPLAY\_SINK\_NOTIFICATION structure</span></span>

<span data-ttu-id="6fca1-104">In der **WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs** Struktur wird die Benachrichtigung beschrieben, die an die Rückruffunktion der [**WFD- \_ Anzeige \_ Senke \_ \_**](wfd-display-sink-notification-callback.md)</span><span class="sxs-lookup"><span data-stu-id="6fca1-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION** structure describes the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fca1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fca1-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="6fca1-106">Member</span><span class="sxs-lookup"><span data-stu-id="6fca1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6fca1-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="6fca1-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-108">Ein [**WFD- \_ Anzeige- \_ \_ senkobjektheader \_**](wfd-display-sink-object-header.md) , der die in der Benachrichtigung enthaltenen Daten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6fca1-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-109">**type**</span><span class="sxs-lookup"><span data-stu-id="6fca1-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-110">Ein [**WFD \_ - \_ \_ \_ Benachrichtigungstyp**](wfd-display-sink-notification-type.md) Wert, der den Typ der Benachrichtigung angibt.</span><span class="sxs-lookup"><span data-stu-id="6fca1-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification.</span></span> <span data-ttu-id="6fca1-111">Dieser Parameter bestimmt auch, welche Informationen in der Union unten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6fca1-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-112">**"strautedevicename"**</span><span class="sxs-lookup"><span data-stu-id="6fca1-112">**strRemoteDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-113">Enthält eine NULL-terminierte Zeichenfolge, die den Namen des Remote Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="6fca1-113">Contains a NULL-terminated string containing the name of the remote device.</span></span> <span data-ttu-id="6fca1-114">\_ \_ \_ Die maximale Länge des Geräte namens der WFD-Senke \_ \_ ist als Wert (32) definiert.</span><span class="sxs-lookup"><span data-stu-id="6fca1-114">WFD\_SINK\_MAX\_DEVICE\_NAME\_LENGTH is defined as the value (32).</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-115">**Remotedeviceaddress**</span><span class="sxs-lookup"><span data-stu-id="6fca1-115">**RemoteDeviceAddress**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-116">Eine [**DOT11 \_ Mac- \_ Adresse**](dot11-mac-address-type.md) , die die BSSID des Remote Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="6fca1-116">A [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) that contains the BSSID of the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-117">**Provisioningrequestinfo**</span><span class="sxs-lookup"><span data-stu-id="6fca1-117">**ProvisioningRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-118">Informationen zu einer Bereitstellungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6fca1-118">Info about a provisioning request.</span></span> <span data-ttu-id="6fca1-119">Verwenden Sie diese Einstellung, wenn der *Typ* den Wert **provisioningrequestnotification** hat.</span><span class="sxs-lookup"><span data-stu-id="6fca1-119">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="6fca1-120">**hsessionhandle**</span><span class="sxs-lookup"><span data-stu-id="6fca1-120">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-121">Das Sitzungs handle.</span><span class="sxs-lookup"><span data-stu-id="6fca1-121">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-122">**Possibleconfigmethods**</span><span class="sxs-lookup"><span data-stu-id="6fca1-122">**PossibleConfigMethods**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-123">Mögliche Methoden, um die Benutzeroberfläche für interaktive Akzeptanz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6fca1-123">Possible methods for showing UI for interactive acceptance.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6fca1-124">**Reconnectrequestinfo**</span><span class="sxs-lookup"><span data-stu-id="6fca1-124">**ReconnectRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-125">Informationen zu einer Anforderung zur erneuten Verbindungs Herstellung.</span><span class="sxs-lookup"><span data-stu-id="6fca1-125">Info about a reconnect request.</span></span> <span data-ttu-id="6fca1-126">Verwenden Sie diese Eigenschaft, wenn der *Typ* den Wert **reconnectrequestnotification** hat.</span><span class="sxs-lookup"><span data-stu-id="6fca1-126">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="6fca1-127">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="6fca1-127">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-128">Die Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="6fca1-128">The group id.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6fca1-129">**Connectedinfo**</span><span class="sxs-lookup"><span data-stu-id="6fca1-129">**ConnectedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-130">Informationen zu einer verbundenen Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="6fca1-130">Info about a connected notification.</span></span> <span data-ttu-id="6fca1-131">Verwenden Sie diese Eigenschaft, wenn der *Typ* den Wert **connectednotification** hat.</span><span class="sxs-lookup"><span data-stu-id="6fca1-131">Use this if *type* has the value **ConnectedNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="6fca1-132">**hsessionhandle**</span><span class="sxs-lookup"><span data-stu-id="6fca1-132">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-133">Das Sitzungs handle.</span><span class="sxs-lookup"><span data-stu-id="6fca1-133">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-134">**guidsessioninterface**</span><span class="sxs-lookup"><span data-stu-id="6fca1-134">**guidSessionInterface**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-135">Eine GUID, die die Sitzungs Schnittstelle angibt.</span><span class="sxs-lookup"><span data-stu-id="6fca1-135">A GUID indicating the session interface.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-136">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="6fca1-136">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-137">Die Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="6fca1-137">The group id.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-138">**"Trend Profil"**</span><span class="sxs-lookup"><span data-stu-id="6fca1-138">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-139">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die das Profil beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6fca1-139">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-140">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="6fca1-140">**LocalAddress**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-141">Die lokale Adresse.</span><span class="sxs-lookup"><span data-stu-id="6fca1-141">The local address.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-142">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="6fca1-142">**RemoteAddress**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-143">Die Remoteadresse.</span><span class="sxs-lookup"><span data-stu-id="6fca1-143">The remote address.</span></span>

</dd> <dt>

<span data-ttu-id="6fca1-144">**urtspport**</span><span class="sxs-lookup"><span data-stu-id="6fca1-144">**uRTSPPort**</span></span>
</dt> <dd>

<span data-ttu-id="6fca1-145">Der RTSP-Port.</span><span class="sxs-lookup"><span data-stu-id="6fca1-145">The RTSP port.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fca1-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fca1-146">Requirements</span></span>



| <span data-ttu-id="6fca1-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fca1-147">Requirement</span></span> | <span data-ttu-id="6fca1-148">Wert</span><span class="sxs-lookup"><span data-stu-id="6fca1-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6fca1-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fca1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6fca1-150">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="6fca1-150">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6fca1-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fca1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6fca1-152">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fca1-152">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6fca1-153">Header</span><span class="sxs-lookup"><span data-stu-id="6fca1-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fca1-154"><dt>WF-Senke. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fca1-154"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 





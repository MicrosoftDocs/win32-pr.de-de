---
description: Definiert den Typ der Benachrichtigung, die an die Rückruffunktion der WFD- \_ Anzeige Senke-Benachrichtigung übermittelt wird \_ \_ \_ .
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: WFD_DISPLAY_SINK_NOTIFICATION_TYPE-Enumeration (WF-Sink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358874"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a><span data-ttu-id="18ace-103">WFD \_ - \_ \_ \_ Benachrichtigungstyp-Enumeration anzeigen</span><span class="sxs-lookup"><span data-stu-id="18ace-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE enumeration</span></span>

<span data-ttu-id="18ace-104">Der enumerierte Typ der **WFD- \_ Anzeige- \_ Senkentyp \_ \_** Definition definiert den Typ der Benachrichtigung, die an die Rückruffunktion der [**WFD- \_ Anzeige- \_ Senke- \_ Benachrichtigung \_**](wfd-display-sink-notification-callback.md)</span><span class="sxs-lookup"><span data-stu-id="18ace-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE** enumerated type defines the type of the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ace-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18ace-105">Syntax</span></span>


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="18ace-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="18ace-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="18ace-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**Provisioningrequestnotification**</span><span class="sxs-lookup"><span data-stu-id="18ace-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="18ace-108">Die Benachrichtigung ist eine Bereitstellungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="18ace-108">The notification is a provisioning request.</span></span>

</dd> <dt>

<span data-ttu-id="18ace-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**Reconnectrequestnotification**</span><span class="sxs-lookup"><span data-stu-id="18ace-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="18ace-110">Die Benachrichtigung ist eine Anforderung zum erneuten Verbinden.</span><span class="sxs-lookup"><span data-stu-id="18ace-110">The notification is a reconnect request.</span></span>

</dd> <dt>

<span data-ttu-id="18ace-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**Connectednotification**</span><span class="sxs-lookup"><span data-stu-id="18ace-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="18ace-112">Die Benachrichtigung ist eine verbundene Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="18ace-112">The notification is a connected notification.</span></span>

</dd> <dt>

<span data-ttu-id="18ace-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**Disconnectednotification**</span><span class="sxs-lookup"><span data-stu-id="18ace-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="18ace-114">Die Benachrichtigung ist eine nicht getrennte Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="18ace-114">The notification is a disconnected notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18ace-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18ace-115">Requirements</span></span>



| <span data-ttu-id="18ace-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18ace-116">Requirement</span></span> | <span data-ttu-id="18ace-117">Wert</span><span class="sxs-lookup"><span data-stu-id="18ace-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="18ace-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18ace-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18ace-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="18ace-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18ace-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18ace-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18ace-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18ace-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="18ace-122">Header</span><span class="sxs-lookup"><span data-stu-id="18ace-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ace-123"><dt>WF-Senke. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ace-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 





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
# <a name="wfd_display_sink_notification_type-enumeration"></a>WFD \_ - \_ \_ \_ Benachrichtigungstyp-Enumeration anzeigen

Der enumerierte Typ der **WFD- \_ Anzeige- \_ Senkentyp \_ \_** Definition definiert den Typ der Benachrichtigung, die an die Rückruffunktion der [**WFD- \_ Anzeige- \_ Senke- \_ Benachrichtigung \_**](wfd-display-sink-notification-callback.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**Provisioningrequestnotification**
</dt> <dd>

Die Benachrichtigung ist eine Bereitstellungs Anforderung.

</dd> <dt>

<span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**Reconnectrequestnotification**
</dt> <dd>

Die Benachrichtigung ist eine Anforderung zum erneuten Verbinden.

</dd> <dt>

<span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**Connectednotification**
</dt> <dd>

Die Benachrichtigung ist eine verbundene Benachrichtigung.

</dd> <dt>

<span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**Disconnectednotification**
</dt> <dd>

Die Benachrichtigung ist eine nicht getrennte Benachrichtigung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>WF-Senke. h</dt> </dl> |



 

 





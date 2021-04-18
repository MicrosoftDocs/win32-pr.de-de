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
# <a name="wfd_display_sink_notification-structure"></a>WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs Struktur

In der **WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs** Struktur wird die Benachrichtigung beschrieben, die an die Rückruffunktion der [**WFD- \_ Anzeige \_ Senke \_ \_**](wfd-display-sink-notification-callback.md)

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**Header**
</dt> <dd>

Ein [**WFD- \_ Anzeige- \_ \_ senkobjektheader \_**](wfd-display-sink-object-header.md) , der die in der Benachrichtigung enthaltenen Daten beschreibt.

</dd> <dt>

**type**
</dt> <dd>

Ein [**WFD \_ - \_ \_ \_ Benachrichtigungstyp**](wfd-display-sink-notification-type.md) Wert, der den Typ der Benachrichtigung angibt. Dieser Parameter bestimmt auch, welche Informationen in der Union unten verwendet werden sollen.

</dd> <dt>

**"strautedevicename"**
</dt> <dd>

Enthält eine NULL-terminierte Zeichenfolge, die den Namen des Remote Geräts enthält. \_ \_ \_ Die maximale Länge des Geräte namens der WFD-Senke \_ \_ ist als Wert (32) definiert.

</dd> <dt>

**Remotedeviceaddress**
</dt> <dd>

Eine [**DOT11 \_ Mac- \_ Adresse**](dot11-mac-address-type.md) , die die BSSID des Remote Geräts enthält.

</dd> <dt>

**Provisioningrequestinfo**
</dt> <dd>

Informationen zu einer Bereitstellungs Anforderung. Verwenden Sie diese Einstellung, wenn der *Typ* den Wert **provisioningrequestnotification** hat.

<dl> <dt>

**hsessionhandle**
</dt> <dd>

Das Sitzungs handle.

</dd> <dt>

**Possibleconfigmethods**
</dt> <dd>

Mögliche Methoden, um die Benutzeroberfläche für interaktive Akzeptanz anzuzeigen.

</dd> </dl> </dd> <dt>

**Reconnectrequestinfo**
</dt> <dd>

Informationen zu einer Anforderung zur erneuten Verbindungs Herstellung. Verwenden Sie diese Eigenschaft, wenn der *Typ* den Wert **reconnectrequestnotification** hat.

<dl> <dt>

**GroupID**
</dt> <dd>

Die Gruppen-ID.

</dd> </dl> </dd> <dt>

**Connectedinfo**
</dt> <dd>

Informationen zu einer verbundenen Benachrichtigung. Verwenden Sie diese Eigenschaft, wenn der *Typ* den Wert **connectednotification** hat.

<dl> <dt>

**hsessionhandle**
</dt> <dd>

Das Sitzungs handle.

</dd> <dt>

**guidsessioninterface**
</dt> <dd>

Eine GUID, die die Sitzungs Schnittstelle angibt.

</dd> <dt>

**GroupID**
</dt> <dd>

Die Gruppen-ID.

</dd> <dt>

**"Trend Profil"**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die das Profil beschreibt.

</dd> <dt>

**LocalAddress**
</dt> <dd>

Die lokale Adresse.

</dd> <dt>

**RemoteAddress**
</dt> <dd>

Die Remoteadresse.

</dd> <dt>

**urtspport**
</dt> <dd>

Der RTSP-Port.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>WF-Senke. h</dt> </dl> |



 

 





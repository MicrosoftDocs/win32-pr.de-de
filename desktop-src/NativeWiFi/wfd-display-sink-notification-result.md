---
description: Beschreibt das Ergebnis, das Sie optional festlegen können, nachdem Sie eine Anzeigesenkennotation in der WFD \_ DISPLAY \_ SINK NOTIFICATION \_ \_ CALLBACK-Funktion verarbeitet haben.
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: WFD_DISPLAY_SINK_NOTIFICATION_RESULT-Struktur (Wfdsink.h)
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
ms.openlocfilehash: d72f444d409a7a3d43103967aff671fa7c808e5a37858e79f175db3511960e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780080"
---
# <a name="wfd_display_sink_notification_result-structure"></a>WFD \_ DISPLAY SINK NOTIFICATION RESULT \_ \_ \_ STRUCTURE

Die **WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ RESULT-Struktur** beschreibt das Ergebnis, das Sie nach der Verarbeitung einer Anzeigesenkennotation in der [**WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ CALLBACK-Funktion**](wfd-display-sink-notification-callback.md) optional festlegen können.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a>Member

<dl> <dt>

**Header**
</dt> <dd>

Ein [**WFD \_ DISPLAY SINK OBJECT \_ \_ \_ HEADER,**](wfd-display-sink-object-header.md) der die im Benachrichtigungsergebnis enthaltenen Daten beschreibt.

</dd> <dt>

**type**
</dt> <dd>

Ein [**WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ TYPE-Wert,**](wfd-display-sink-notification-type.md) der den Typ des Benachrichtigungsergebnisses angibt. Dieser Parameter bestimmt auch, welche Info in der folgenden Union verwendet werden soll.

</dd> <dt>

**ProvisioningData**
</dt> <dd>

Informationen zum Ergebnis einer Bereitstellungsanforderung. Verwenden Sie diese , wenn *der Typ* den Wert **ProvisioningRequestNotification** auf hat.

<dl> <dt>

**ConfigMethod**
</dt> <dd>

Die Methode zum Anzeigen der Benutzeroberfläche für die interaktive Akzeptanz.

</dd> <dt>

**uPassKeyLength**
</dt> <dd>

Die Anzahl der Breitzeichen im *Hauptschlüssel*, ohne NULL-Abschlusszeichen.

</dd> <dt>

**Hauptschlüssel**
</dt> <dd>

Enthält den Passschlüssel als Array von Breitzeichen. WFD \_ SINK \_ WPS INFO MAX \_ \_ \_ PASSKEY LENGTH ist als Wert \_ (8) definiert.

</dd> </dl> </dd> <dt>

**ReconnectData**
</dt> <dd>

Informationen zum Ergebnis einer Anforderung zur erneuten Verbindung. Verwenden Sie diese , wenn *type* den Wert **ReconnectRequestNotification** auf hat.

<dl> <dt>

**strProfile**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die das Profil beschreibt.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 





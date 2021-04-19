---
description: Beschreibt das Ergebnis, das Sie optional festlegen können, nachdem eine Anzeige Senke-notalisierung in der WFD- \_ \_ \_ Benachrichtigungs \_ Rückruffunktion angezeigt wird.
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: WFD_DISPLAY_SINK_NOTIFICATION_RESULT-Struktur (WF-Sink. h)
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
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362707"
---
# <a name="wfd_display_sink_notification_result-structure"></a>WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs \_ Ergebnis Struktur

In der **WFD- \_ \_ \_ Benachrichtigungs \_ Ergebnis** Struktur wird das Ergebnis beschrieben, das Sie optional festlegen können, nachdem Sie die Anzeige Senke-notalisierung in der [**WFD- \_ \_ \_ Benachrichtigungs \_ Rückruf**](wfd-display-sink-notification-callback.md) Funktion verarbeitet haben.

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

Ein [**WFD- \_ Anzeige- \_ \_ senkobjektheader \_**](wfd-display-sink-object-header.md) , der die im Benachrichtigungs Ergebnis enthaltenen Daten beschreibt.

</dd> <dt>

**type**
</dt> <dd>

Ein [**WFD \_ - \_ \_ \_ Benachrichtigungstyp**](wfd-display-sink-notification-type.md) Wert, der den Typ des Benachrichtigungs Ergebnisses angibt. Dieser Parameter bestimmt auch, welche Informationen in der Union unten verwendet werden sollen.

</dd> <dt>

**Provisioningdata**
</dt> <dd>

Informationen zum Ergebnis einer Bereitstellungs Anforderung. Verwenden Sie diese Einstellung, wenn der *Typ* den Wert **provisioningrequestnotification** hat.

<dl> <dt>

**Configmethod**
</dt> <dd>

Die Methode für die Anzeige der Benutzeroberfläche für die interaktive Annahme.

</dd> <dt>

**upasskeylength**
</dt> <dd>

Die Anzahl der breit Zeichen in einem *Passkey*, wobei kein NULL-Terminator gezählt wird.

</dd> <dt>

**Hauptschlüssel**
</dt> <dd>

Enthält den Pass-Key als Array von breit Zeichen. \_ \_ Die maximale Passkey-Länge der WFD-Sink-WPS- \_ Informationen \_ \_ \_ ist als Wert (8) definiert.

</dd> </dl> </dd> <dt>

**Reconnectdata**
</dt> <dd>

Informationen zum Ergebnis einer Anforderung zum erneuten Verbinden. Verwenden Sie diese Eigenschaft, wenn der *Typ* den Wert **reconnectrequestnotification** hat.

<dl> <dt>

**"Trend Profil"**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die das Profil beschreibt.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>WF-Senke. h</dt> </dl> |



 

 





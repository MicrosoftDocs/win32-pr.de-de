---
description: Pro-Benutzer-Ereignis, das durch den Webinhalts Filter generiert wurde, weil versucht wurde, auf eine URL zuzugreifen.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: WPCEVENT_WEB_URLVISIT-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1075ae930cdaa9ee539dbc17a8c13d5c2a41add
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042216"
---
# <a name="wpcevent_web_urlvisit-event"></a>Wpcevent \_ Web \_ urlvisit-Ereignis

Pro-Benutzer-Ereignis, das durch den Webinhalts Filter generiert wurde, weil versucht wurde, auf eine URL zuzugreifen.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_URLVISIT = {0x3, 0x0, 0x10, 0x4, 0x18, 0x3, 0x8000000000000010};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* 
</dt> <dd>

Die URL, die geöffnet werden soll.

</dd> <dt>

*Anwendung* 
</dt> <dd>

Die Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*Version* 
</dt> <dd>

Die Versions Zeichenfolge für die Anwendung.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*Ratingsystemid* 
</dt> <dd>

Eine GUID, die das aktuelle Bewertungssystem identifiziert.

</dd> <dt>

*Anzahl von Kategorien* 
</dt> <dd>

Die Anzahl der blockierten Einträge im Kategoriefeld.

</dd> <dt>

*Kategorie* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge von kategorienbezeichnerids, die blockiert werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Protokollierungs-APIs für Eltern Steuerelemente](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ Conversation ationinitevent**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 





---
description: Ereignis pro Benutzer, das von einem Instant Messaging-Client generiert wird, wenn Kontaktinformationen in Jugendschutz Elementen hinzugefügt, geändert oder entfernt werden.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: WPCEVENT_IM_CONTACT-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9747f7ede57f7a1d77af0f0e8e5425401ee32b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218229"
---
# <a name="wpcevent_im_contact-event"></a>Wpcevent \_ im- \_ Kontakt Ereignis

Ereignis pro Benutzer, das von einem Instant Messaging-Client generiert wird, wenn Kontaktinformationen in Jugendschutz Elementen hinzugefügt, geändert oder entfernt werden.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_CONTACT = {0xf, 0x0, 0x10, 0x4, 0x16, 0xf, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppName* 
</dt> <dd>

Der Name der Instant Messaging-Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Version der Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*AccountName* 
</dt> <dd>

Der Instant Messaging-Kontoname für diesen Benutzer.

</dd> <dt>

*OldName* 
</dt> <dd>

Der vorherige Name des Instant Messaging-Kontos, wenn es gelöscht oder geändert wurde.

</dd> <dt>

*Oldid* 
</dt> <dd>

Die ID, die dem vorherigen Instant Messaging-Kontonamen zugeordnet ist.

</dd> <dt>

*NewName* 
</dt> <dd>

Der neue Instant Messaging-Kontoname, wenn er hinzugefügt oder geändert wird.

</dd> <dt>

*NEWID* 
</dt> <dd>

Die ID, die dem neuen Instant Messaging-Kontonamen zugeordnet ist.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

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

 

 





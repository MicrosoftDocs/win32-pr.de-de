---
description: Benutzerspezifisches Ereignis, das von einem Instant Messaging-Client generiert wird, wenn Kontaktinformationen in der Jugendschutz-Instanz hinzugefügt, geändert oder entfernt werden.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: WPCEVENT_IM_CONTACT -Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baac4bf5648b27f2e8d446a79bb2d90d52f0aac416e30d031d3b81d430a6927b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951447"
---
# <a name="wpcevent_im_contact-event"></a>WPCEVENT \_ IM \_ CONTACT-Ereignis

Benutzerspezifisches Ereignis, das von einem Instant Messaging-Client generiert wird, wenn Kontaktinformationen in der Jugendschutz-Instanz hinzugefügt, geändert oder entfernt werden.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_CONTACT = {0xf, 0x0, 0x10, 0x4, 0x16, 0xf, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppName* 
</dt> <dd>

Der Name der Instant Messaging-Anwendung, die das Ereignis generiert.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Version der Anwendung, die das Ereignis generiert.

</dd> <dt>

*AccountName* 
</dt> <dd>

Der Name des Instant Messaging-Kontos für diesen Benutzer.

</dd> <dt>

*OldName* 
</dt> <dd>

Der vorherige Name des Instant Messaging-Kontos, sofern gelöscht oder geändert.

</dd> <dt>

*OldID* 
</dt> <dd>

Die ID, die dem vorherigen Namen des Instant Messaging-Kontos zugeordnet ist.

</dd> <dt>

*Newname* 
</dt> <dd>

Der name des neuen Instant Messaging-Kontos, sofern hinzugefügt oder geändert.

</dd> <dt>

*Newid* 
</dt> <dd>

Die ID, die dem neuen Namen des Instant Messaging-Kontos zugeordnet ist.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse nicht verwendet werden und welche Steuerelemente verwendet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Protokollierungs-APIs für Jugendschutz](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 





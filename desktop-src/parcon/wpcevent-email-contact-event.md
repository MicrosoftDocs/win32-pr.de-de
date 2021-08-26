---
description: Benutzerspezifisches Ereignis, das von einem E-Mail-Client generiert wird, der aufzeichnet, wenn ein Kontakt in der Jugendschutzgruppe hinzugefügt, geändert oder gelöscht wird.
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: WPCEVENT_EMAIL_CONTACT -Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d84a450c53705dae2db777081f7177f43505e0481ae38a67c1b90e507fa4a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951570"
---
# <a name="wpcevent_email_contact-event"></a>WPCEVENT \_ EMAIL \_ CONTACT-Ereignis

Benutzerspezifisches Ereignis, das von einem E-Mail-Client generiert wird, der aufzeichnet, wenn ein Kontakt in der Jugendschutzgruppe hinzugefügt, geändert oder gelöscht wird.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_CONTACT = {0xe, 0x0, 0x10, 0x4, 0x16, 0xe, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppName* 
</dt> <dd>

Der Name der E-Mail-Anwendung, die das Ereignis generiert.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Version der E-Mail-Anwendung, die das Ereignis generiert.

</dd> <dt>

*OldName* 
</dt> <dd>

Der name des vorherigen E-Mail-Kontos, falls gelöscht oder geändert.

</dd> <dt>

*OldID* 
</dt> <dd>

Die ID, die dem vorherigen E-Mail-Kontonamen zugeordnet ist.

</dd> <dt>

*Newname* 
</dt> <dd>

Der name des neuen E-Mail-Kontos, falls hinzugefügt oder geändert.

</dd> <dt>

*Newid* 
</dt> <dd>

Die ID, die dem neuen E-Mail-Kontonamen zugeordnet ist.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse für die Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

Der E-Mail-Kontoname für diesen Benutzer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Protokollierungs-APIs für Jugendschutz](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 





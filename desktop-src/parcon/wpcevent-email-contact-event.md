---
description: Pro-Benutzer-Ereignis, das von einem e-Mail-Client generiert wird und auf dem das Hinzufügen, ändern oder Löschen eines Kontakts in Jugendschutz Daten aufgezeichnet wird
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: WPCEVENT_EMAIL_CONTACT-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0974030e53756b44f2be2e8550707161f2d6d461
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218230"
---
# <a name="wpcevent_email_contact-event"></a>Wpcevent \_ -e-Mail- \_ Kontakt Ereignis

Pro-Benutzer-Ereignis, das von einem e-Mail-Client generiert wird und auf dem das Hinzufügen, ändern oder Löschen eines Kontakts in Jugendschutz Daten aufgezeichnet wird


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_CONTACT = {0xe, 0x0, 0x10, 0x4, 0x16, 0xe, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppName* 
</dt> <dd>

Der Name der e-Mail-Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Version der e-Mail-Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*OldName* 
</dt> <dd>

Der vorherige e-Mail-Konto Name, wenn er gelöscht oder geändert wurde.

</dd> <dt>

*Oldid* 
</dt> <dd>

Die ID, die dem vorherigen e-Mail-Kontonamen zugeordnet ist.

</dd> <dt>

*NewName* 
</dt> <dd>

Der neue e-Mail-Kontoname, wenn hinzugefügt oder geändert.

</dd> <dt>

*NEWID* 
</dt> <dd>

Die ID, die dem neuen e-Mail-Kontonamen zugeordnet ist.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*Emailaccount* 
</dt> <dd>

Der Name des e-Mail-Kontos für diesen Benutzer.

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

 

 





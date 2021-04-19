---
description: Das Ereignis auf System Ebene, das bei einer Änderung der Jugend Steuerungs Einstellung generiert wurde.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: WPCEVENT_SYS_SETTINGCHANGE-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362699"
---
# <a name="wpcevent_sys_settingchange-event"></a>Wpcevent \_ sys \_ settingchange-Ereignis

Das Ereignis auf System Ebene, das bei einer Änderung der Jugend Steuerungs Einstellung generiert wurde.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Klasse* 
</dt> <dd>

Die Klasse, die das Ereignis erzeugt.

</dd> <dt>

*Einstellung* 
</dt> <dd>

Ein Wert der **WPC- \_ Einstellungs** Enumeration.

</dd> <dt>

*Besitzer* 
</dt> <dd>

Die Sicherheits-ID des Benutzers, der das Ereignis erzeugt.

</dd> <dt>

*OLDVAL* 
</dt> <dd>

Der vorherige Wert dieser Einstellung, wenn Sie gelöscht oder geändert wird.

</dd> <dt>

*NewVal* 
</dt> <dd>

Der neue Wert dieser Einstellung, wenn hinzugefügt oder geändert.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*Optional* 
</dt> <dd>

Ein optionales Feld.

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

 

 





---
description: Pro Benutzer-Ereignis, das bis zu drei Felder unterstützt.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: WPCEVENT_CUSTOM-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215869"
---
# <a name="wpcevent_custom-event"></a>Benutzerdefiniertes wpcevent- \_ Ereignis

Pro Benutzer-Ereignis, das bis zu drei Felder unterstützt.

Ereignisse werden in der **Aktivitäts** Anzeige im **anderen** Abschnitt mit der folgenden Hierarchie angezeigt:

1.  Publisher

2.  Application

3.  Ereignis


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Publisher* 
</dt> <dd>

Der Herausgeber des Ereignisses (z. b. ein Firmenname).

</dd> <dt>

*AppName* 
</dt> <dd>

Der Name der Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Version der Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*Event* 
</dt> <dd>

Der Name des Ereignisses.

</dd> <dt>

*Value1* 
</dt> <dd>

Benutzerdefiniertes Feld 1.

</dd> <dt>

*Value2* 
</dt> <dd>

Benutzerdefiniertes Feld 2.

</dd> <dt>

*Wert3* 
</dt> <dd>

Benutzerdefiniertes Feld 3.

</dd> <dt>

*Gesperrt* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Eine benutzerdefinierte Zeichenfolge, die zusätzliche Informationen über den Grund für das Blockieren oder nicht blockieren bereitstellt.

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

 

 





---
description: Benutzerspezifisches Ereignis, das bis zu drei Felder unterstützt.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: WPCEVENT_CUSTOM -Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8082e03aa6dfea8cd2fd461feec093de71a1ada8051b8fb88295d0bbbf570b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951550"
---
# <a name="wpcevent_custom-event"></a>WPCEVENT \_ CUSTOM-Ereignis

Benutzerspezifisches Ereignis, das bis zu drei Felder unterstützt.

Ereignisse werden im **Aktivitäts-Viewer** im Abschnitt **Sonstige** mit der folgenden Hierarchie angezeigt:

1.  Herausgeber

2.  Anwendung

3.  Ereignis


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Publisher* 
</dt> <dd>

Der Herausgeber des Ereignisses (z. B. ein Firmenname).

</dd> <dt>

*AppName* 
</dt> <dd>

Der Name der Anwendung, die das Ereignis generiert.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Version der Anwendung, die das Ereignis generiert.

</dd> <dt>

*Event* 
</dt> <dd>

Der Name für das Ereignis.

</dd> <dt>

*Wert1* 
</dt> <dd>

Benutzerdefiniertes Feld 1.

</dd> <dt>

*Value2* 
</dt> <dd>

Benutzerdefiniertes Feld 2.

</dd> <dt>

*Value3* 
</dt> <dd>

Benutzerdefiniertes Feld 3.

</dd> <dt>

*Blockiert* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse nicht verwendet werden und welche Steuerelemente verwendet werden.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Eine benutzerdefinierte Zeichenfolge, die zusätzliche Informationen über den Grund für das Blockieren oder nicht das Blockieren enthält.

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

 

 





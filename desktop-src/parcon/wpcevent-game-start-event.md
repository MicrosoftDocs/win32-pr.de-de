---
description: Benutzerspezifisches Ereignis, das vom System beim Versuch generiert wird, ein Spiel zu starten. Verschiedene Feldwerte werden vom Games Explorer-System und den entsprechenden GDF-Metadaten (Game Definition File) bereitgestellt, die von unterstützten Spielen bereitgestellt werden.
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: WPCEVENT_GAME_START (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41367a47a9bace8dd615ab4b6eea0a875099aab465c285389478c4bee0a39392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951500"
---
# <a name="wpcevent_game_start-event"></a>WPCEVENT \_ GAME \_ START-Ereignis

Benutzerspezifisches Ereignis, das vom System beim Versuch generiert wird, ein Spiel zu starten. Verschiedene Feldwerte werden vom Games Explorer-System und den entsprechenden GDF-Metadaten (Game Definition File) bereitgestellt, die von unterstützten Spielen bereitgestellt werden.


```C++
const EVENT_DESCRIPTOR WPCEVENT_GAME_START = {0x2, 0x0, 0x10, 0x4, 0x16, 0x2, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppID* 
</dt> <dd>

Die GUID des Spiels, das gestartet werden soll.

</dd> <dt>

*InstanceID* 
</dt> <dd>

Die GUID, die verwendet wird, um zwischen mehreren Installationen zu unterscheiden.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Versionszeichenfolge für das Spiel.

</dd> <dt>

*Path* 
</dt> <dd>

Der Pfad zum primären Verzeichnis der Spieleinstallation.

</dd> <dt>

*Rating* 
</dt> <dd>

Eine Zeichenfolge, die die Bewertungsebene eines Spiels innerhalb des Bewertungssystems identifiziert.

</dd> <dt>

*RatingSystem* 
</dt> <dd>

Eine GUID, die das aktuelle Bewertungssystem identifiziert, für das die Bewertungsstufe gilt.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse nicht verwendet werden und welche Steuerelemente verwendet werden.

</dd> <dt>

*DescCount* 
</dt> <dd>

Die Anzahl der Deskriptoren, die im Deskriptorfeld vorhanden sind.

</dd> <dt>

*Deskriptor* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die Deskriptoren enthält, die für das Spiel blockiert sind.

</dd> <dt>

*Pid* 
</dt> <dd>

Die Prozess-ID des Spiels, die zum Korrelieren mit einem Shim-Herunterfahren des Prozesses verwendet wird.

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

 

 





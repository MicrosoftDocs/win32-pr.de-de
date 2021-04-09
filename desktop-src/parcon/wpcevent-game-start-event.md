---
description: Pro-Benutzer-Ereignis, das vom System beim Versuch, ein Spiel zu starten, generiert wurde. Verschiedene Feldwerte werden vom Games Explorer-System und den zugehörigen GDF-Metadaten (Game Definition File) bereitgestellt, die von unterstützten Spielen bereitgestellt werden.
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: WPCEVENT_GAME_START-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5cc47144910f624005031573e28f5078db10ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042217"
---
# <a name="wpcevent_game_start-event"></a>Wpcevent- \_ Spiel \_ Start Ereignis

Pro-Benutzer-Ereignis, das vom System beim Versuch, ein Spiel zu starten, generiert wurde. Verschiedene Feldwerte werden vom Games Explorer-System und den zugehörigen GDF-Metadaten (Game Definition File) bereitgestellt, die von unterstützten Spielen bereitgestellt werden.


```C++
const EVENT_DESCRIPTOR WPCEVENT_GAME_START = {0x2, 0x0, 0x10, 0x4, 0x16, 0x2, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppID* 
</dt> <dd>

Der GUID des Spiels, das versucht hat, zu starten.

</dd> <dt>

*InstanceID* 
</dt> <dd>

Die GUID, die zur Unterscheidung zwischen mehreren Installationen verwendet wird.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Versions Zeichenfolge für das Spiel.

</dd> <dt>

*Pfad* 
</dt> <dd>

Der Pfad zum primären Verzeichnis der Spielinstallation.

</dd> <dt>

*Rating* 
</dt> <dd>

Eine Zeichenfolge, die die Bewertungs Ebene eines Spiels im Bewertungssystem identifiziert.

</dd> <dt>

*Ratingsystem* 
</dt> <dd>

Eine GUID, die das aktuelle Bewertungssystem identifiziert, für das die Bewertungsstufe gilt.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*Desccount* 
</dt> <dd>

Die Anzahl der Deskriptoren, die im Deskriptorfeld vorhanden sind.

</dd> <dt>

*Deskriptor* 
</dt> <dd>

Eine durch Trennzeichen getrennte Zeichenfolge, die Deskriptoren enthält, die für das Spiel blockiert sind.

</dd> <dt>

*Lauer* 
</dt> <dd>

Die Prozess-ID des Spiels, das verwendet wird, um das Herunterfahren des Prozesses mit einem Shim zu korrelieren.

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

 

 





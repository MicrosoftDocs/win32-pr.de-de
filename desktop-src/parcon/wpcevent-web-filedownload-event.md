---
description: Pro-Benutzer-Ereignis, das bei dem Versuch generiert wird, Dateien aus dem Web herunterzuladen. Dieses Ereignis wird von Anwendungen generiert, die von Eltern Steuerelementen angefordert werden.
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: WPCEVENT_WEB_FILEDOWNLOAD-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66bb04a53589a1cae41e2ba7d7a9c00835452e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363758"
---
# <a name="wpcevent_web_filedownload-event"></a>Wpcevent \_ - \_ webfiledownload-Ereignis

Pro-Benutzer-Ereignis, das bei dem Versuch generiert wird, Dateien aus dem Web herunterzuladen. Dieses Ereignis wird von Anwendungen generiert, die von Eltern Steuerelementen angefordert werden.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_FILEDOWNLOAD = {0xa, 0x0, 0x10, 0x4, 0x18, 0xa, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* 
</dt> <dd>

Die URL-Quelle, die versucht, herunterzuladen.

</dd> <dt>

*AppName* 
</dt> <dd>

Der Name der Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*Version* 
</dt> <dd>

Die Version der Anwendung, die das Ereignis erzeugt.

</dd> <dt>

*Gesperrt* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*Pfad* 
</dt> <dd>

Der Zielpfad für die Datei.

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

 

 





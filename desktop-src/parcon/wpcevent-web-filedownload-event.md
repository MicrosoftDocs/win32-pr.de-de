---
description: Benutzerspezifisches Ereignis, das beim Versuch generiert wird, Dateien aus dem Web herunterzuladen. Dieses Ereignis wird von Anwendungen generiert, die von der Jugendschutz-Steuerung aufgefordert werden.
ms.assetid: 2291fc75-55e5-417e-b393-748750a5b3d6
title: WPCEVENT_WEB_FILEDOWNLOAD -Ereignis (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7430b87e7c227fe351e3182f344c60ece0b5a3138b94fe19fee950f96ec24b6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112710"
---
# <a name="wpcevent_web_filedownload-event"></a>WPCEVENT \_ WEB \_ FILEDOWNLOAD-Ereignis

Benutzerspezifisches Ereignis, das beim Versuch generiert wird, Dateien aus dem Web herunterzuladen. Dieses Ereignis wird von Anwendungen generiert, die von der Jugendschutz-Steuerung aufgefordert werden.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_FILEDOWNLOAD = {0xa, 0x0, 0x10, 0x4, 0x18, 0xa, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* 
</dt> <dd>

Die URL-Quelle, die heruntergeladen werden soll.

</dd> <dt>

*AppName* 
</dt> <dd>

Der Name der Anwendung, die das Ereignis generiert.

</dd> <dt>

*Version* 
</dt> <dd>

Die Version der Anwendung, die das Ereignis generiert.

</dd> <dt>

*Blockiert* 
</dt> <dd>

Ein Wert der [**WPCFLAG \_ ISBLOCKED-Enumeration,**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) der Informationen darüber angibt, welche Ereignisse für die Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*Path* 
</dt> <dd>

Der Zielpfad für die Datei.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden von Protokollierungs-APIs für Jugendschutz](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 





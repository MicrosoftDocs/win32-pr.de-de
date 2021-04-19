---
description: Definiert die Rückruffunktion&\# 8212, die Sie in Ihrer APP implementieren&\# 8212;, die für die wfdstartdisplaysink-Funktion angegeben wurde.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK Callback-Funktion (WF-Sink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353439"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>WFD \_ - \_ \_ Benachrichtigungs \_ Rückruf-Rückruffunktion

Die **WFD \_ - \_ \_ Benachrichtigungs \_ Rückruffunktion zeigt** die Rückruffunktion an – die Sie in Ihrer APP implementieren –, die für die [**wfdstartdisplaysink**](wfdstartdisplaysink.md) -Funktion angegeben wurde.

## <a name="syntax"></a>Syntax


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvcontext* \[ in, optional\]
</dt> <dd>

Ein optionaler Kontext Zeiger, der an die Rückruffunktion übermittelt wird.

</dd> <dt>

*pnotification* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Struktur, die Daten über die Anzeige Senke Benachrichtigung enthält.

</dd> <dt>

*pnotificationresult* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine Struktur mit Daten, die von Ihrer APP optional festgelegt werden können, um das Ergebnis der Verarbeitung der Benachrichtigung über die Anzeige Senke anzugeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>WF-Senke. h</dt> </dl> |



 

 





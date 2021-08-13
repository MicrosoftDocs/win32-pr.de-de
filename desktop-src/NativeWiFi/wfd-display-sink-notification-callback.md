---
description: Definiert die Rückruffunktion&\# 8212;, die Sie in Ihrer App&\# 8212; implementieren, die für die WFDStartDisplaySink-Funktion angegeben wurde.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK Rückruffunktion (Wfdsink.h)
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
ms.openlocfilehash: 7066f45b714c28b53747d0d0f1851bd94ac2ac902e5b4adba1d0746e8328b3b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619975"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>Rückruffunktion WFD \_ DISPLAY \_ SINK NOTIFICATION \_ \_ CALLBACK

Die **WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ CALLBACK-Funktion** definiert die Rückruffunktion, die Sie in Ihrer App implementieren, die für die [**WFDStartDisplaySink-Funktion**](wfdstartdisplaysink.md) angegeben wurde.

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

*pvContext* \[ in, optional\]
</dt> <dd>

Ein optionaler Kontextzeiger, der an die Rückruffunktion übergeben wird.

</dd> <dt>

*pNotification* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Struktur, die Daten zur Benachrichtigung über die Anzeigesenke enthält.

</dd> <dt>

*pNotificationResult* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine Struktur, die Daten enthält, die Ihre App optional festlegen kann, um das Ergebnis der Verarbeitung der Benachrichtigung zur Anzeigesenke anzugeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 





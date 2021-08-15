---
description: Die \_ LINE GROUPSTATUS-Nachricht wird gesendet, wenn sich der Status einer ACD-Gruppe in einem Agenthandler ändert, für den die Anwendung derzeit über eine offene Zeile verfügt. Diese Nachricht wird mithilfe der funktion lineProxyMessage generiert.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: LINE_GROUPSTATUS Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c70ba4badd27b4d42774549b4778bd77dda13f0ae7245ee6852c2b3afab164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761943"
---
# <a name="line_groupstatus-message"></a>LINE \_ GROUPSTATUS-Meldung

Die **LINE \_ GROUPSTATUS-Nachricht** wird gesendet, wenn sich der Status einer ACD-Gruppe in einem Agenthandler ändert, für den die Anwendung derzeit über eine offene Zeile verfügt. Diese Nachricht wird mithilfe der [**funktion lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) generiert.


```C++
        
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwDevice* 
</dt> <dd>

Das Handle der Anwendung für das Zeilengerät. Dies bezieht sich auf den Agenthandler.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile angegeben wird.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gibt den geänderten Gruppenstatus an. Die Anwendung kann [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) aufrufen, um die Änderungen in verfügbaren Gruppen zu ermitteln. Der *dwParam2-Parameter* ist mindestens eine der [**LINEGROUPSTATUS-Konstanten. \_**](linegroupstatus--constants.md)

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 





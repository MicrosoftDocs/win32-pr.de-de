---
description: Die \_ LINE QUEUESTATUS-Nachricht wird gesendet, wenn sich der Status einer ACD-Warteschlange für einen Agenthandler ändert, für den die Anwendung derzeit über eine offene Zeile verfügt. Diese Nachricht wird mithilfe der funktion lineProxyMessage generiert.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: LINE_QUEUESTATUS Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336a8239e31e5c0bcc70de747cbb48a2028c85e67f44a3e45032f02b37065d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975530"
---
# <a name="line_queuestatus-message"></a>LINE \_ QUEUESTATUS-Nachricht

Die **LINE \_ QUEUESTATUS-Nachricht** wird gesendet, wenn sich der Status einer ACD-Warteschlange für einen Agenthandler ändert, für den die Anwendung derzeit über eine offene Zeile verfügt. Diese Nachricht wird mithilfe der [**funktion lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) generiert.


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

Der Bezeichner der Warteschlange, deren Status geändert wurde.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gibt den geänderten Warteschlangenstatus an. Kann eine oder mehrere [**LINEQUEUESTATUS-Konstanten \_ sein.**](linequeuestatus--constants.md)

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

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 





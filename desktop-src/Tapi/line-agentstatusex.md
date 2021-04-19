---
description: Die \_ Meldung "agentstatusex" wird gesendet, wenn sich der Status eines ACD-Agents in einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt. Diese Meldung wird mithilfe der lineproxymess-Funktion generiert.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: LINE_AGENTSTATUSEX Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366817"
---
# <a name="line_agentstatusex-message"></a>Zeile \_ agentstatusex-Meldung

Die Meldung " **\_ agentstatusex** " wird gesendet, wenn sich der Status eines ACD-Agents in einem Agent-Handler ändert, für den die Anwendung zurzeit über eine geöffnete Zeile verfügt. Diese Meldung wird mithilfe der [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) -Funktion generiert.


```C++
        
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwdevice* 
</dt> <dd>

Das Handle der Anwendung für das liniengerät. Dies bezieht sich auf den-Agent-Handler.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Das Handle des Agents, dessen Status geändert wurde.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gibt den Status der Warteschlange an, der geändert wurde. Kann eine oder mehrere der [**linequeuestatus- \_ Konstanten**](linequeuestatus--constants.md)sein.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Wenn *dwParam2* das Status Bit lineagentstatusex enthält \_ , gibt *dwParam3* den neuen Wert des Agentstatus an, der eine der [**lineagentstateex- \_ Konstanten**](lineagentstateex--constants.md)ist.

Andernfalls ist *dwParam3* auf 0 (null) festgelegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**linegetagentinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 





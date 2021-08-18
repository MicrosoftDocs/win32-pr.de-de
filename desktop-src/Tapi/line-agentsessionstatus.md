---
description: Die MELDUNG LINE \_ AGENTSESSIONSTATUS wird gesendet, wenn sich der Status einer ACD-Agentsitzung in einem Agenthandler ändert, für den die Anwendung derzeit über eine offene Zeile verfügt. Diese Nachricht wird mithilfe der funktion lineProxyMessage generiert.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: LINE_AGENTSESSIONSTATUS Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25209abda7cfec3864c45bfd58a35a9fad21a1aa5e5645669a7fdad6ec907d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003218"
---
# <a name="line_agentsessionstatus-message"></a>LINE \_ AGENTSESSIONSTATUS-Meldung

Die **MELDUNG LINE \_ AGENTSESSIONSTATUS** wird gesendet, wenn sich der Status einer ACD-Agentsitzung in einem Agenthandler ändert, für den die Anwendung derzeit über eine offene Zeile verfügt. Diese Nachricht wird mithilfe der [**funktion lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) generiert.


```C++
        
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwDevice* 
</dt> <dd>

Das Handle der Anwendung für das Zeilengerät, auf dem sich der Status der Agentsitzung geändert hat.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile angegeben wird.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Ein Handle der Agentsitzung, deren Status geändert wurde.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gibt den Status der Agentsitzung an, der geändert wurde. Kann mindestens ein **\_ LINE-AGENTSESSIONSTATUS** sein.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Wenn *dwParam2* das LINEAGENTSTATUSEX \_ STATE-Bit enthält, gibt *dwParam3* den neuen Wert des Agentzustands an, bei dem es sich um eine der [**LINEAGENTSTATEEX-Konstanten \_**](lineagentstateex--constants.md)handelt.

Andernfalls wird *dwParam3* auf 0 (null) festgelegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 





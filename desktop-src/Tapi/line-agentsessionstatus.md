---
description: Die \_ Meldung "agentsessionstatus" wird gesendet, wenn sich der Status einer ACD-Agent-Sitzung auf einem Agent-Handler ändert, für den die Anwendung zurzeit eine offene Zeile aufweist. Diese Meldung wird mithilfe der lineproxymess-Funktion generiert.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: LINE_AGENTSESSIONSTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368674"
---
# <a name="line_agentsessionstatus-message"></a>Zeile \_ agentsessionstatus-Meldung

Die Meldung " **\_ agentsessionstatus** " wird gesendet, wenn sich der Status einer ACD-Agent-Sitzung auf einem Agent-Handler ändert, für den die Anwendung zurzeit eine offene Zeile aufweist. Diese Meldung wird mithilfe der [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) -Funktion generiert.


```C++
        
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwdevice* 
</dt> <dd>

Das Handle der Anwendung für das liniengerät, für das sich der agentsitzungsstatus geändert hat.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Ein Handle der Agentsitzung, deren Status sich geändert hat.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gibt den Agent-Sitzungs Status an, der geändert wurde. Kann eine oder mehrere der **Zeilen \_ agentsessionstatus** sein.

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

[**linegetagentsessioninfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 





---
description: Die MELDUNG LINE \_ PROXYSTATUS wird gesendet, wenn sich die verfügbaren Proxys in einer Zeile ändern, in der die Anwendung derzeit geöffnet ist.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: LINE_PROXYSTATUS Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 585feda6194a13ecfbe17292aadb9036784d244c9ee5b7df4361981ab7401f65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682350"
---
# <a name="line_proxystatus-message"></a>LINE \_ PROXYSTATUS-Meldung

Die **MELDUNG LINE \_ PROXYSTATUS** wird gesendet, wenn sich die verfügbaren Proxys in einer Zeile ändern, in der die Anwendung derzeit geöffnet ist.

TAPISRV generiert diese Meldung während einer [**lineOpen-Funktion**](/windows/desktop/api/Tapi/nf-tapi-lineopen) mit LINEPROXYSTATUS \_ OPEN und LINEPROXYSTATUS \_ ALLOPENFORACD oder einer [**lineClose-Funktion**](/windows/desktop/api/Tapi/nf-tapi-lineclose) mit LINEPROXYSTATUS \_ CLOSE (alle [**LINEPROXYSTATUS-Konstanten \_**](lineproxystatus--constants.md)).


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

Gibt den geänderten Warteschlangenstatus an. Kann eine oder mehrere [**LINEPROXYSTATUS-Konstanten \_ sein.**](lineproxystatus--constants.md)

</dd> <dt>

*dwParam2* 
</dt> <dd>

Wenn *dwParam1* auf LINEPROXYSTATUS \_ OPEN oder LINEPROXYSTATUS CLOSE festgelegt \_ ist, gibt *dwParam2* den entsprechenden Proxyanforderungstyp an. Dies ist einer der folgenden:

-   LINEPROXYREQUEST \_ SETAGENTGROUP
-   LINEPROXYREQUEST \_ SETAGENTSTATE
-   LINEPROXYREQUEST \_ SETAGENTACTIVITY
-   LINEPROXYREQUEST \_ GETAGENTCAPS
-   LINEPROXYREQUEST \_ GETAGENTSTATUS
-   LINEPROXYREQUEST \_ AGENTSPECIFIC
-   LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST
-   LINEPROXYREQUEST \_ GETAGENTGROUPLIST
-   LINEPROXYREQUEST \_ CREATEAGENT
-   LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETAGENTINFO
-   LINEPROXYREQUEST \_ CREATEAGENTSESSION
-   LINEPROXYREQUEST \_ GETAGENTSESSIONLIST
-   LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE
-   LINEPROXYREQUEST \_ GETAGENTSESSIONINFO
-   LINEPROXYREQUEST \_ GETQUEPROXYIST
-   LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETQUEUEINFO
-   LINEPROXYREQUEST \_ GETGROUPLIST
-   LINEPROXYREQUEST \_ SETAGENTSTATEEX

Andernfalls wird *dwParam2* auf 0 (null) festgelegt.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineÖffnen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**LINE \_ PROXYREQUEST**](line-proxyrequest.md)
</dt> <dt>

[**\_LINEPROXYREQUEST-Konstanten**](lineproxyrequest--constants.md)
</dt> </dl>

 

 





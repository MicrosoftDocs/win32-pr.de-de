---
description: Die Meldung "line \_ proxystatus" wird gesendet, wenn sich die verfügbaren Proxys in einer Zeile ändern, die derzeit von der Anwendung geöffnet wurde.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: LINE_PROXYSTATUS Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359388"
---
# <a name="line_proxystatus-message"></a>Zeile \_ proxystatus-Meldung

Die Meldung " **line \_ proxystatus** " wird gesendet, wenn sich die verfügbaren Proxys in einer Zeile ändern, die derzeit von der Anwendung geöffnet wurde.

Tapisrv generiert diese Nachricht während einer [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) -Funktion mithilfe von lineproxystatus \_ Open und lineproxystatus \_ allopenforacd oder einer [**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) -Funktion mithilfe von lineproxystatus \_ Close (alle [**lineproxystatus- \_ Konstanten**](lineproxystatus--constants.md)).


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

Gibt den Status der Warteschlange an, der geändert wurde. Kann eine oder mehrere der [**lineproxystatus- \_ Konstanten**](lineproxystatus--constants.md)sein.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Wenn *dwParam1* auf lineproxystatus \_ Open oder lineproxystatus close festgelegt ist \_ , gibt *dwParam2* den zugehörigen Proxy Anforderungstyp an. Dies ist einer der folgenden:

-   lineproxyrequest \_ setagentgroup
-   lineproxyrequest \_ setagentstate
-   lineproxyrequest \_ setagentactivity
-   lineproxyrequest \_ getagentcaps
-   lineproxyrequest \_ getagentstatus
-   lineproxyrequest- \_ agentspezifisch
-   lineproxyrequest \_ getagentactivitylist
-   lineproxyrequest \_ getagentgrouplist
-   lineproxyrequest- \_ kreateagent
-   lineproxyrequest \_ setagentmessrementperiod
-   lineproxyrequest \_ getagentinfo
-   lineproxyrequest- \_ Sitzung
-   lineproxyrequest \_ getagentsessionlist
-   lineproxyrequest \_ setagentsessionstate
-   lineproxyrequest \_ getagentsessioninfo
-   lineproxyrequest \_ getqueuelist
-   lineproxyrequest \_ setqueuemessrementperiod
-   lineproxyrequest \_ getqueueinfo
-   "lineproxyrequest" \_ getgrouplist
-   lineproxyrequest \_ setagentstateex

Andernfalls ist *dwParam2* auf 0 (null) festgelegt.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reserviert. Auf NULL festlegen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**\_linienproxyrequest**](line-proxyrequest.md)
</dt> <dt>

[**Lineproxyrequest- \_ Konstanten**](lineproxyrequest--constants.md)
</dt> </dl>

 

 





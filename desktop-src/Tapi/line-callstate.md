---
description: Die TAPI LINE \_ CALLSTATE-Nachricht wird gesendet, wenn sich der Status des angegebenen Aufrufs geändert hat.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: LINE_CALLSTATE (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d82dfb5f0d5e306085ecd2d7f29270d19c2c9c101e30ac547fe246b7e6fddb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012570"
---
# <a name="line_callstate-message"></a>LINE \_ CALLSTATE-Nachricht

Die TAPI **LINE \_ CALLSTATE-Nachricht** wird gesendet, wenn sich der Status des angegebenen Aufrufs geändert hat. In der Regel werden während der Lebensdauer eines Aufrufs mehrere solcher Nachrichten empfangen. Anwendungen werden über neue eingehende Aufrufe mit dieser Nachricht benachrichtigt. Der neue Aufruf befindet sich im *Angebotszustand.* Die Anwendung kann [**lineGetCallStatus verwenden,**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) um ausführlichere Informationen zum aktuellen Status des Aufrufs abzurufen.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für den Aufruf.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile des Aufrufs angegeben wurde.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der neue Aufrufzustand. Dieser Parameter muss eine und nur eine der folgenden [**LINECALLSTATE-Konstanten \_ sein.**](linecallstate--constants.md)



| dwParam1                                                                                                                                                                                             | Bedeutung                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <dt>**LINECALLSTATE \_ AUSGELASTET**</dt> </dl>                         | *dwParam2 enthält* Details zum Ausgelastetmodus. Dieser Parameter verwendet eine der [**LINEBUSYMODE-Konstanten \_**](linebusymode--constants.md).<br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <dt>**LINECALLSTATE \_ CONNECTED**</dt> </dl>          | *dwParam2 enthält* Details zum verbundenen Modus. Dieser Parameter verwendet eine der [**LINECONNECTEDMODE-Konstanten \_**](lineconnectedmode--constants.md).<br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <dt>**LINECALLSTATE \_ DIALTONE**</dt> </dl>             | *dwParam2 enthält* Details zum Dial-Tonmodus. Dieser Parameter verwendet eine der [**LINEDIALTONEMODE-Konstanten \_**](linedialtonemode--constants.md).<br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <dt>**LINECALLSTATE-ANGEBOT \_**</dt> </dl>             | *dwParam2 enthält* Details zum verbundenen Modus. Dieser Parameter verwendet eine der [**LINEOFFERINGMODE-Konstanten \_**](lineofferingmode--constants.md).<br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <dt>**LINECALLSTATE \_ SPECIALINFO**</dt> </dl>    | *dwParam2* enthält die Details zum speziellen Informationsmodus. Dieser Parameter verwendet eine der [**LINESPECIALINFO-Konstanten \_**](linespecialinfo--constants.md).<br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <dt>**LINECALLSTATE \_ DISCONNECTED**</dt> </dl> | *dwParam2 enthält* Details zum Trennungsmodus. Dieser Parameter verwendet eine der [**LINEDISCONNECTMODE-Konstanten \_**](linedisconnectmode--constants.md).<br/>        |



 

</dd> <dt>

*dwParam2* 
</dt> <dd>

Vom Aufrufzustand abhängige Informationen. Weitere Informationen *finden Sie unter dwParam1.*

> [!Note]  
> Verwenden Sie  LINEDISCONNECTMODE TEMPFAILURE, wenn eine verzögerte Antwort \_ angemessen ist. Wenn eine *in der Blockliste aufgeführte* Antwort geeignet ist, verwenden Sie LINEDISCONNECT \_ BLOCKED. Weitere Informationen finden Sie unter [**LINEDISCONNECTMODE-Konstanten. \_**](linedisconnectmode--constants.md)

 

Wenn *dwParam1* LINECALLSTATE \_ CONFERENCED ist, enthält *dwParam2* den *hConfCall-Parameter* des übergeordneten Aufrufs der Konferenz, deren Mitglied der Subjekt *hCall* ist. Wenn der in *dwParam2 angegebene* Aufruf zuvor von der Anwendung nicht als übergeordneter Telefonkonferenzaufruf (*hConfCall)* angesehen wurde, muss die Anwendung dies als Ergebnis dieser Nachricht tun. Wenn die Anwendung kein Handle für den übergeordneten Aufruf der Konferenz hat (da sie zuvor [**lineDeallocateCall für**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) dieses Handle aufgerufen hat), wird *dwParam2* auf **NULL festgelegt.**

</dd> <dt>

*dwParam3* 
</dt> <dd>

Bei 0 (null) gibt dieser Parameter an, dass die Berechtigung der Anwendung für den Aufruf nicht geändert wurde.

Wenn dieser Wert ungleich 0 (null) ist, wird die Berechtigung der Anwendung für den Aufruf angegeben. Dies tritt in den folgenden Situationen auf: (1) Wenn die Anwendung zum ersten Mal ein Handle für diesen Aufruf erhält; (2) Wenn die Anwendung das Ziel einer Anruf-Übergabe ist (auch wenn die Anwendung bereits Besitzer des Aufrufs war). Dieser Parameter verwendet eine der folgenden [**LINECALLPRIVILEGE-Konstanten. \_**](linecallprivilege--constants.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Diese Nachricht wird an jede Anwendung gesendet, die über ein Handle für den Aufruf verfügt. Die **LINE \_ CALLSTATE-Nachricht** benachrichtigt auch Anwendungen, die Aufrufe über eine Zeile überwachen, über das Vorhandensein und den Status von ausgehenden Anrufen, die von anderen Anwendungen oder manuell vom Benutzer eingerichtet wurden (z. B. auf einem angeschlossenen Telefongerät). Der Aufrufzustand solcher Aufrufe spiegelt den tatsächlichen Zustand des Aufrufs wider, der nicht *an bietet.* Durch Untersuchen des Anrufzustands kann die Anwendung bestimmen, ob es sich bei dem Anruf um einen eingehenden Anruf handelt, der beantwortet werden muss.

Eine **LINE \_ CALLSTATE-Nachricht** mit einem unbekannten Aufrufstatus kann als Ergebnis einer erfolgreichen [**LineMakeCall-,**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) [**lineForward-,**](/windows/desktop/api/Tapi/nf-tapi-lineforward) [**lineUnpark-,**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) [**lineSetupTransfer-,**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer) [**linePickup-,**](/windows/desktop/api/Tapi/nf-tapi-linepickup) [**lineSetupConference-**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)oder [**linePrepareAddToConference-Nachricht**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) an eine Überwachungsanwendung gesendet werden, die von einer anderen Anwendung angefordert wurde. Gleichzeitig mit dem Senden einer LINE [**\_ REPLY(Success)**](line-reply.md) für den angeforderten Vorgang an die anfordernde Anwendung wird allen Überwachungsanwendungen in der Zeile die **Meldung LINE \_ CALLSTATE** (unbekannt) gesendet. Eine **LINE \_ CALLSTATE-Meldung,** die den "echten" Aufrufzustand des neu generierten Aufrufs angibt, wird kurz darauf (anhand der vom Dienstanbieter bereitgestellten Informationen) an die anfordernden und überwachenden Anwendungen gesendet.

Eine **LINE \_ CALLSTATE-Nachricht** (unbekannt) wird nur dann an Überwachungsanwendungen gesendet, wenn [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) bewirkt, dass Aufrufe in eine Drei-Wege-Konferenz aufgelöst werden.

Aus Gründen der Abwärtskompatibilität erwarten ältere Anwendungen keinen bestimmten Wert in *dwParam2* einer LINECALLSTATE \_ CONFERENCED-Nachricht. TAPI übergibt daher den übergeordneten *Aufruf hConfCall* in *dwParam2* unabhängig von der API-Version der Anwendung, die die Nachricht empfängt. Im Fall eines vom Dienstanbieter initiierten Telefonkonferenzs ist der älteren Anwendung nicht bewusst, dass der übergeordnete Anruf zu einem Telefonanruf geworden ist, es sei denn, es werden andere Informationen sorgfältig untersucht (z. B. [**lineGetConfRelatedCalls).**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)

Diese Meldung kann nicht deaktiviert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ REPLY**](line-reply.md)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 





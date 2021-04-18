---
description: Die TAPI-zeilige \_ CallState-Nachricht wird gesendet, wenn sich der Status des angegebenen Aufrufes geändert hat.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: LINE_CALLSTATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358066"
---
# <a name="line_callstate-message"></a>Zeilen \_ Aufruf Zustands Meldung

Die TAPI- **zeilige \_ CallState** -Nachricht wird gesendet, wenn sich der Status des angegebenen Aufrufes geändert hat. In der Regel werden während der Lebensdauer eines Aufrufes einige dieser Nachrichten empfangen. Anwendungen werden über neue eingehende Anrufe mit dieser Nachricht benachrichtigt. der neue-Befehl befindet sich im *Angebots* Zustand. Die Anwendung kann [**linegetcallstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) verwenden, um ausführlichere Informationen zum aktuellen Status des Aufrufes abzurufen.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für den-Befehl.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der neue Status des Aufrufes. Dieser Parameter darf nur eine der folgenden [**linecallstate- \_ Konstanten**](linecallstate--constants.md)sein.



| dwParam1                                                                                                                                                                                             | Bedeutung                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <dt>**linecallstate \_ ausgelastet**</dt> </dl>                         | *dwParam2* enthält Details zum ausgelasteten Modus. Dieser Parameter verwendet eine der [**linebusymode- \_ Konstanten**](linebusymode--constants.md).<br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <dt>**linecallstate \_ verbunden**</dt> </dl>          | *dwParam2* enthält Details zum verbundenen Modus. Dieser Parameter verwendet eine der [**lineconnectedmode- \_ Konstanten**](lineconnectedmode--constants.md).<br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <dt>**linecallstate \_ Dialtone**</dt> </dl>             | *dwParam2* enthält Details zum wählermodusmodus. Dieser Parameter verwendet eine der [**linedialtonemode- \_ Konstanten**](linedialtonemode--constants.md).<br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <dt>**linecallstate- \_ Angebot**</dt> </dl>             | *dwParam2* enthält Details zum verbundenen Modus. Dieser Parameter verwendet eine der [**lineofferingmode- \_ Konstanten**](lineofferingmode--constants.md).<br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <dt>**linecallstate \_ specialinfo**</dt> </dl>    | *dwParam2* enthält die Details zum speziellen Informationsmodus. Dieser Parameter verwendet eine der [**linespecialinfo- \_ Konstanten**](linespecialinfo--constants.md).<br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <dt>**linecallstate \_ getrennt**</dt> </dl> | *dwParam2* enthält Details zum Disconnect-Modus. Dieser Parameter verwendet eine der [**linedisconnectmode- \_ Konstanten**](linedisconnectmode--constants.md).<br/>        |



 

</dd> <dt>

*dwParam2* 
</dt> <dd>

Aufrufzustands abhängige Informationen. Siehe *dwParam1*.

> [!Note]  
> In Fällen, in denen eine *verzögerte* Antwort angemessen ist, verwenden Sie den linedisconnectmode- \_ tempfailure. Wenn eine *Blockierungs* Antwort angemessen ist, verwenden Sie "linedisconnect \_ blockiert". Weitere Informationen finden Sie unter [**linedisconnectmode- \_ Konstanten**](linedisconnectmode--constants.md).

 

Wenn *dwParam1* auf linecallstate zuweist \_ , enthält *dwParam2* den *hconfcallparameter* des übergeordneten Aufrufens der Konferenz, von der der Betreff- *hcallmember* ist. Wenn der in *dwParam2* angegebene-Befehl nicht zuvor von der Anwendung als übergeordnete Konferenz aufgerufen wurde (*hconfcallcenter*), muss die Anwendung dies als Ergebnis dieser Nachricht ausführen. Wenn die Anwendung kein Handle für den übergeordneten Aufruf der Konferenz hat (weil Sie zuvor [**linedezugecall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) für dieses Handle aufgerufen hat), wird *dwParam2* auf **null** festgelegt.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Wenn der Wert NULL ist, gibt dieser Parameter an, dass die Berechtigung der Anwendung für den-Befehl nicht geändert wurde.

Wenn ungleich 0 (null) angegeben ist, wird die Berechtigung der Anwendung für den-Befehl angegeben. Dies tritt in den folgenden Situationen auf: (1), wenn der Anwendung das erste Mal ein Handle für diesen Aufruf zugewiesen wird. (2), wenn die Anwendung das Ziel einer callhandoff ist (selbst wenn die Anwendung bereits Besitzer des Aufrufes ist). Dieser Parameter verwendet eine der folgenden [**linecallprivilege- \_ Konstanten**](linecallprivilege--constants.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird an jede Anwendung gesendet, die über ein Handle für den-Befehl verfügt. In der **Zeile \_ CallState** werden auch Anwendungen benachrichtigt, die Aufrufe in einer Zeile über das vorhanden sein und den Status der ausgehenden Aufrufe, die von anderen Anwendungen oder manuell durch den Benutzer (z. b. auf einem angeschlossenen Telefongerät), überwachen. Der Aufruf Zustand solcher Aufrufe gibt den tatsächlichen Status des Aufrufs an, der nicht *angeboten* wird. Durch die Untersuchung des aufrufzustands kann die Anwendung bestimmen, ob der-Rückruf ein eingehender-Befehl ist, der beantwortet werden muss.

Eine **Zeilen Aufruf \_ Zustands** Meldung mit einem unbekannten Aufruf Zustand kann als Ergebnis eines erfolgreichen [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineunpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)oder [**lineprepareadddeconference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) , das von einer anderen Anwendung angefordert wurde, an eine Überwachungsanwendung gesendet werden. Gleichzeitig, dass die anfordernde Anwendung für den angeforderten Vorgang eine [**Zeilen \_ Antwort**](line-reply.md) (Erfolg) sendet, wird allen Überwachungsanwendungen in der Zeile die **Zeile \_ CallState** (unknown) zugestellt. Eine **line \_ CallState** -Meldung, die angibt, dass der "Real"-Aufruf Zustand des neu generierten Aufrufes gesendet wird (mithilfe der vom Dienstanbieter bereitgestellten Informationen), kurz danach an die Anforderungs-und Überwachungsanwendungen.

Eine Nachricht vom Typ " **\_ CallState** " (unbekannt) wird nur dann an Überwachungsanwendungen gesendet, wenn " [**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) " bewirkt, dass Aufrufe in eine drei-Wege-Konferenz aufgelöst werden.

Aus Gründen der Abwärtskompatibilität erwarten ältere Anwendungen keinen bestimmten Wert in *dwParam2* einer mit linecallstate zugewandten \_ Nachricht. TAPI übergibt daher unabhängig von der API-Version der Anwendung, die die Nachricht empfängt, den übergeordneten Befehl " *hconfcall"* in *dwParam2* . Im Fall eines Konferenz Aufrufs, der vom Dienstanbieter initiiert wurde, weiß die ältere Anwendung nicht, dass der übergeordnete Aufruf zu einem Konferenz Aufruf geworden ist, es sei denn, es erfolgt eine spontane Untersuchung anderer Informationen (z. b. [**linegetanfrelatedcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).

Diese Meldung kann nicht deaktiviert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeilen \_ Antwort**](line-reply.md)
</dt> <dt>

[**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**linedezugewiesene eCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**Linedialpara**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**linegetcallstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[**lineget-frelatedcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[**lineprepareaddumconference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[**lineunpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 





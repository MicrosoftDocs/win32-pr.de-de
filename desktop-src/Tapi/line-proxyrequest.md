---
description: Die TAPI LINE \_ PROXYREQUEST-Nachricht übergibt eine Anforderung an einen registrierten Proxyfunktionshandler.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: LINE_PROXYREQUEST (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31986420cd21178cca8e6f0a1006e743c3250e726b4a1bf79513f6d57e380a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003158"
---
# <a name="line_proxyrequest-message"></a>LINE \_ PROXYREQUEST-Nachricht

Die TAPI **LINE \_ PROXYREQUEST-Nachricht** übergibt eine Anforderung an einen registrierten Proxyfunktionshandler.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Das Handle der Anwendung für das Liniengerät, auf dem sich der Agentstatus geändert hat.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile des Aufrufs angegeben wurde.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Zeiger auf eine [**LINEPROXYREQUEST-Struktur,**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) die die Anforderung enthält, die von der Proxyhandleranwendung verarbeitet werden soll.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reserviert.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die **LINE \_ PROXYREQUEST-Nachricht** wird nur an die erste Anwendung gesendet, die registriert wurde, um Proxyanforderungen des zugestellten Typs zu verarbeiten.

Die Anwendung sollte die im Proxypuffer enthaltene Anforderung verarbeiten und [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) aufrufen, um Daten zurück- oder Ergebnisse zu liefern. Die Verarbeitung der Anforderung sollte nur im Kontext der TAPI-Rückruffunktion der Anwendung erfolgen, wenn sie sofort ausgeführt werden kann, ohne auf die Antwort einer anderen Entität zu warten. Wenn die Anwendung mit anderen Entitäten kommunizieren muss (z. B. einem Dienstanbieter zur Handhabung PBX-basierter ACD oder einem anderen Systemdienst, der zu einer Blockierung führen kann), sollte die Anforderung innerhalb der Anwendung in die Warteschlange gestellt und die Rückruffunktion beendet werden, um zu vermeiden, dass der Empfang weiterer TAPI-Nachrichten durch die Anwendung verzögert wird.

Zum Zeitpunkt der Lieferung von **LINE \_ PROXYREQUEST** an den Proxyhandler hat TAPI bereits ein positives *dwRequestID-Funktionsergebnis* an die ursprüngliche Anwendung zurückgegeben und die Blockierung des aufrufenden Threads aufgehoben, um die Ausführung fortzufahren. Die Anwendung wartet auf eine [**LINE \_ REPLY-Nachricht,**](line-reply.md) die automatisch generiert wird, wenn die Proxyhandleranwendung [**lineProxyResponse aufruft.**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)

Die Anwendung darf nicht den Arbeitsspeicher freigeben, auf den *lpProxyRequest zeigt.* TAPI gibt den Arbeitsspeicher während der Ausführung von [**lineProxyResponse frei.**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) Die Anwendung kann [**lineProxyResponse für jede**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) **LINE \_ PROXYREQUEST-Nachricht genau einmal** aufrufen.

Wenn die Anwendung während ausstehender Proxyanforderungen eine [**LINE \_ CLOSE-Nachricht**](line-close.md) empfängt, sollte sie [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) für jede ausstehende Anforderung aufrufen und einen entsprechenden *dwResult-Wert* übergeben (z. B. LINEERR \_ OPERATIONFAILED).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**LINE \_ REPLY**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 





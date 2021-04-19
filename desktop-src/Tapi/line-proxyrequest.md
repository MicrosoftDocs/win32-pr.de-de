---
description: Die TAPI- \_ linienproxyrequest-Nachricht übermittelt eine Anforderung an einen registrierten Proxy Funktions Handler.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: LINE_PROXYREQUEST Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373758"
---
# <a name="line_proxyrequest-message"></a>Zeile \_ proxyrequest-Nachricht

Die TAPI **- \_ linienproxyrequest** -Nachricht übermittelt eine Anforderung an einen registrierten Proxy Funktions Handler.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Das Handle der Anwendung für das liniengerät, auf dem sich der Agentstatus geändert hat.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Zeiger auf eine [**lineproxyrequest**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) -Struktur, die die Anforderung enthält, die von der proxyhandleranwendung verarbeitet werden soll.

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

## <a name="remarks"></a>Bemerkungen

Die **Zeile \_ proxyrequest** -Nachricht wird nur an die erste Anwendung gesendet, die für die Verarbeitung von Proxy Anforderungen des übermittelten Typs registriert ist.

Die Anwendung sollte die im Proxy Puffer enthaltene Anforderung verarbeiten und [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) anrufen, um Daten zurückzugeben oder Ergebnisse zu liefern. Die Verarbeitung der Anforderung sollte nur im Kontext der TAPI-Rückruffunktion der Anwendung erfolgen, wenn Sie sofort ausgeführt werden kann, ohne auf eine Antwort von einer anderen Entität zu warten. Wenn die Anwendung mit anderen Entitäten kommunizieren muss (z. b. ein Dienstanbieter zur Handhabung der PBX-basierten ACD oder eines beliebigen anderen System Dienstanbieters, der zu Blockierungen führen kann), sollte die Anforderung in der Anwendung in die Warteschlange eingereiht werden, und die Rückruffunktion wird beendet, um zu vermeiden, dass weitere TAPI-Nachrichten von der Anwendung verzögert werden

Zum Zeitpunkt, an dem die **Zeile \_ proxyrequest** an den Proxy Handler übermittelt wird, hat TAPI bereits ein positives Ergebnis der *dwrequestid-* Funktion an die ursprüngliche Anwendung zurückgegeben und die Blockierung des aufrufenden Threads aufgehoben, um die Ausführung fortzusetzen. Die Anwendung wartet auf eine [**Zeilen \_ Antwort**](line-reply.md) Nachricht, die automatisch generiert wird, wenn die Proxy Handler-Anwendung [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)aufruft.

Die Anwendung darf den Speicher, auf den von *lpproxyrequest* verwiesen wird, nicht freigeben. TAPI gibt den Arbeitsspeicher während der Ausführung von [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)frei. Die Anwendung kann [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) für jede **Zeile \_ proxyrequest** -Nachricht genau einmal aufzurufen.

Wenn die Anwendung eine Nachricht [**zum \_ Schließen**](line-close.md) der Nachricht empfängt, während Sie ausstehende Proxy Anforderungen hat, sollte Sie [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) für jede ausstehende Anforderung abrufen und einen entsprechenden *dwresult* -Wert übergeben (z \_ . b. lineerr operationfailed).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeilen \_ Schließen**](line-close.md)
</dt> <dt>

[**Zeilen \_ Antwort**](line-reply.md)
</dt> <dt>

[**Lineproxyrequest**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 





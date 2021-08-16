---
description: Die TSPI LINE \_ NEWCALL-Nachricht wird an die LINEEVENT-Rückruffunktion gesendet, wenn ein neuer Aufruf, von dem TAPI nicht stammt, in einer Zeile eingeht, die TAPI geöffnet hat.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: LINE_NEWCALL Meldung (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f541f7535e9b41dc66a83b8d033d3ff7adf4d51f6e78f275d2695cb5ae7a35b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761906"
---
# <a name="line_newcall-message"></a>LINE \_ NEWCALL-Nachricht

Die TSPI **LINE \_ NEWCALL-Nachricht** wird an die [**LINEEVENT-Rückruffunktion**](/windows/win32/api/tspi/nc-tspi-lineevent) gesendet, wenn ein neuer Aufruf, von dem TAPI nicht stammt, in einer Zeile eingeht, die TAPI geöffnet hat. Dies muss die erste Nachricht sein, die in Bezug auf diesen Aufruf gesendet wird. TAPI schreibt das nicht transparente *htCall-Handle* als *dwParam2* in den vom Dienstanbieter übergebenen Speicherort. Dadurch erhält der Dienstanbieter den *htCall-Wert,* der in nachfolgenden Nachrichten verwendet werden soll.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htLine* 
</dt> <dd>

Das nicht transparente TAPI-Objekthandle für das Liniengerät.

</dd> <dt>

*htCall* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Der Wert LINE \_ NEWCALL.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Das nicht transparente Handle des Dienstanbieters für den Aufruf vom Typ [**HDRVCALL.**](hdrvline.md) TAPI übergibt diesen Wert als *hdCall-Parameter,* um den Aufruf in nachfolgenden Prozeduren zu identifizieren, die für den Aufruf aufgerufen werden.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Ein Zeiger vom Typ LPHTAPICALL, der auf einen [**HTAPICALL**](htapicall.md)zeigt. TAPI schreibt das nicht transparente TAPI-Handle für den Aufruf an die angegebene Position. Der Dienstanbieter muss diesen Wert speichern und als *htCall-Parameter* übergeben, um den Aufruf in nachfolgenden Ereignissen zu identifizieren, die er für den Aufruf meldet.

Dieser Parameter kann auch den Wert **NULL** abrufen (siehe abschnitt "Hinweise").

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Dienstanbieter sollte die [**LINE \_ CALLSTATE-Nachricht**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) als nächste Nachricht für diesen Aufruf senden. Das **LINE \_ NEWCALL-Ereignis** ist ungewöhnlich, da es auch einen Wert zurück an den Dienstanbieter übergibt.

Diese Funktion meldet alle neuen Aufrufe, die vom Dienstanbieter stammen (eingehend, ausgehend, am Telefon initiiert usw.), für die TAPI und der Dienstanbieter noch keine nicht transparenten Handles ausgetauscht haben. Die Handles werden ausgetauscht, sodass TAPI und der Dienstanbieter anschließend Anforderungen stellen und Ereignisse im Zusammenhang mit dem Aufruf melden können. Da diese neuen Aufrufe nicht notwendigerweise eingehend sind, können sich die Aufrufe anfänglich in einem beliebigen Zustand befinden, nicht unbedingt im *Angebotszustand.* Wenn der Dienstanbieter startet und feststellt, dass mindestens ein Aufruf bereits in der Zeile aktiv ist, informiert er TAPI über diese mit **LINE \_ NEWCALL-Nachrichten,** gefolgt von [**LINE \_ CALLSTATE-Nachrichten,**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) die den aktuellen Zustand angeben. Ein neuer ausgehender Anruf, der vom Benutzer auf dem Telefon initiiert wurde, wird mit einer **LINE \_ NEWCALL-Nachricht** gemeldet, und die anfängliche **LINE \_ CALLSTATE-Nachricht** gibt an, dass sich der Anruf im **DIALTONE-Zustand** befand (und dann von dort aus fortgesetzt wird).

Wenn der Dienstanbieter eine große Anzahl von Aufrufen an TAPI in sehr kurzer Zeit (während desselben Interruptzyklus) übergibt, kann TAPI bei der Verarbeitung dieser Aufrufe wieder protokolliert werden. In diesem Fall signalisiert TAPI dem Dienstanbieter, kurz zu warten, bevor weitere Aufrufe gesendet werden. Dies wird signalisiert, indem anstelle eines gültigen [**HTAPICALL-Werts**](htapicall.md)ein Wert von **NULL** in den Speicherort geschrieben wird, auf den der *dwParam2-Parameter* von **LINE \_ NEWCALL** zeigt. Dies weist darauf hin, dass der Versuch, das neu angebotene Aufrufhandle zu verarbeiten, nicht erfolgreich war, wahrscheinlich aufgrund einer vorübergehenden Unfähigkeit, Arbeitsspeicher zu belegen. Der Dienstanbieter kann reagieren, indem er den Aufruf verwirft oder die **LINE \_ NEWCALL-Nachricht** nach einer Planungsverzögerung erneut eingibt (während dieser Zeit sollte der Dienstanbieter dem Prozessor die Verarbeitung anderer ausstehender Aktionen ermöglichen). In jedem Fall können keine weiteren Nachrichten über den neuen Aufruf an TAPI übergeben werden, bis der Handleaustausch erfolgreich ist. Wenn der Speicherort, auf den *dwParam2* zeigt, einen Wert ungleich **NULL** abruft, weiß der Dienstanbieter, dass dieser Wert ein gültiges [**HTAPICALL-Handle**](htapicall.md) für den Aufruf ist.

Es gibt keine direkt entsprechende Meldung auf TAPI-Ebene. Diese Nachricht wird auf TSPI-Ebene verwendet, um eindeutig und eindeutig einen neuen eingehenden Aufruf von TAPI einzuführen und den nicht transparenten TAPI-Bezeichner für den Aufruf abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LINE \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 


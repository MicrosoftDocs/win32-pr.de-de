---
description: Die TSPI-Zeilen- \_ newcall-Meldung wird immer dann an die LineEvent-Rückruffunktion gesendet, wenn ein neuer Aufruf, den TAPI nicht ausgelöst hat, in einer Zeile ankommt, die TAPI geöffnet hat.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: LINE_NEWCALL Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361911"
---
# <a name="line_newcall-message"></a>Zeilen- \_ newcallmeldung

Die TSPI- **Zeilen- \_ newcall-Meldung** wird immer dann an die [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -Rückruffunktion gesendet, wenn ein neuer Aufruf, den TAPI nicht ausgelöst hat, in einer Zeile ankommt, die TAPI geöffnet hat. Dies muss die erste gesendete Nachricht bezüglich dieses Aufrufes sein. TAPI schreibt das nicht transparente " *htcallhandle* "-Handle an den Speicherort, der vom Dienstanbieter als *dwParam2* Dadurch erhält der Dienstanbieter den Wert " *htcall"* , der in nachfolgenden Nachrichten verwendet werden soll.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htline* 
</dt> <dd>

Das nicht transparente TAPI-Objekt Handle für das liniengerät.

</dd> <dt>

*"htcall"* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwmsg* 
</dt> <dd>

Der Wert für den Zeilen- \_ newcall.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Das nicht transparente Handle des Dienstanbieters für den-Befehl vom Typ [**hdrvcall.**](hdrvline.md) TAPI übergibt diesen Wert als *hdcallparameter* , um den Aufruf in nachfolgenden Prozeduren zu identifizieren, die für den Aufruf aufgerufen werden.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Ein Zeiger vom Typ lphtapicall, der auf [**htapicall**](htapicall.md)verweist. TAPI schreibt das nicht transparente TAPI-Handle für den aufzurufenden Speicherort. Der Dienstanbieter muss diesen Wert speichern und als den Parameter " *htcall"* übergeben, um den-Rückruf in nachfolgenden Ereignissen zu identifizieren, die er für den-Befehl meldet.

Dieser Parameter kann auch den Wert **null** abrufen (siehe folgenden Abschnitt "Hinweise").

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Dienstanbieter sollte die [**Zeilen \_ Aufruf Zustands**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) Meldung als nächste Nachricht für diesen Aufruf senden. Das **Zeilen- \_ newcall-Ereignis** ist insofern ungewöhnlich, als dass es auch einen Wert an den Dienstanbieter zurückgibt.

Diese Funktion meldet alle neuen Aufrufe, die aus dem Dienstanbieter stammen (eingehend, ausgehend, initiiert am Telefon usw.), für die TAPI und der Dienstanbieter noch keine nicht transparenten Handles ausgetauscht haben. Die Handles werden ausgetauscht, sodass TAPI und der Dienstanbieter dann Anfragen ausführen und Ereignisse mit dem-Befehl melden können. Da diese neuen Aufrufe nicht zwangsläufig eingehenden, können sich die Aufrufe anfänglich in einem beliebigen Zustand befinden, nicht notwendigerweise dem *Angebots* Zustand. Wenn der Dienstanbieter startet und ermittelt, dass ein oder mehrere Aufrufe bereits in der Zeile aktiv sind, informiert er TAPI über diese mit **Zeilen \_ newcallnachrichten** gefolgt von [**Zeilen \_ Aufruf Zustands**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) Meldungen, die den aktuellen Zustand angeben. Ein neuer ausgehender Aufruf, der vom Benutzer auf dem Telefon initiiert wurde, wird mit einer Zeile für einen **Zeilen \_ neuanruf** gemeldet, und die anfängliche **Zeile \_ CallState** -Meldung gibt an, dass der Aufruf im Zustand " **Dialtone** " war (und dann fortfahren).

Wenn der Dienstanbieter innerhalb eines sehr kurzen Zeitraums eine große Anzahl von Aufrufen an TAPI übergibt (während desselben interruptcycle), kann TAPI bei der Verarbeitung dieser Aufrufe Rück protokolliert werden. Wenn dies geschieht, signalisiert TAPI dem Dienstanbieter, dass vor dem Senden von weiteren Aufrufen eine kurze Zeit gewartet werden soll. Dies signalisiert dies durch Schreiben eines Werts von **null** anstelle eines gültigen [**htapicall**](htapicall.md)-Werts in den Speicherort, auf den durch den *dwParam2* -Parameter von **Zeile \_ newcallverwiesen** wird. Dies weist darauf hin, dass der Versuch, das neu angebotene Telefon Handle zu verarbeiten, nicht erfolgreich war. Dies liegt wahrscheinlich daran, dass nicht genügend Arbeitsspeicher belegt werden konnte. Der Dienstanbieter kann durch Löschen des Aufrufes oder durch erneutes Senden der **Zeile neuer \_ Aufruf** Nachricht nach einer Zeit Plan Verzögerung Antworten (während dieser Zeit sollte der Dienstanbieter den Prozessor erhalten, damit TAPI andere ausstehende Aktionen verarbeiten kann). In jedem Fall können keine weiteren Nachrichten bezüglich des neuen Aufrufes an TAPI weitergegeben werden, bis der Handle-Austausch erfolgreich ist. Wenn der Speicherort, auf den von *dwParam2* verwiesen wird, einen Wert ungleich **null** erhält, weiß der Dienstanbieter, dass dieser Wert ein gültiges [**htapicall**](htapicall.md) -Handle für den-Befehl ist.

Es gibt keine direkt entsprechende Meldung auf der TAPI-Ebene. Diese Meldung wird auf der TSPI-Ebene verwendet, um einen neuen eingehenden Befehl in TAPI eindeutig und eindeutig einzuführen und den nicht transparenten TAPI-Bezeichner für den-Befehl abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_liniencallstate**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))
</dt> <dt>

[**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 


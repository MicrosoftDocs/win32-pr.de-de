---
description: Die TSPI-zeilige \_ calldevspecificfeature-Nachricht wird an die LineEvent-Rückruffunktion gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile oder einer Adresse auftreten.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: LINE_CALLDEVSPECIFICFEATURE Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2891f019035f53be4dbc0a40de429e5c0d9dc567
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359770"
---
# <a name="line_calldevspecificfeature-message"></a>Zeile \_ calldevspecificfeature-Meldung

Die TSPI- **zeilige \_ calldevspecificfeature** -Nachricht wird an die [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -Rückruffunktion gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile oder einer Adresse auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter *dwParam1* through *dwParam3* sind gerätespezifisch.


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

Das nicht transparente TAPI-Objekt Handle für das anrufgerät.

</dd> <dt>

*dwmsg* 
</dt> <dd>

Die Wert Zeile \_ calldevspecificfeature.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Gerätespezifisch.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gerätespezifisch.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Gerätespezifisch.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Zeile \_ calldevspecificfeature** wird von einem Dienstanbieter in Verbindung mit der Funktion [**TSPI \_ linedevspecificfeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) verwendet. Seine Bedeutung ist gerätespezifisch.

TAPI sendet die [**Zeile \_ devspecificfeature**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) -Nachricht als Antwort auf den Empfang dieser Nachricht von einem Dienstanbieter an Anwendungen. Die Parameter " *htline* " und " *htcall"* werden als *hdevice* -Parameter auf der TAPI-Ebene in den entsprechenden *hcallcenter* übersetzt. Die Parameter *dwParam1*, *dwParam2* und *dwParam3* werden unverändert übermittelt.

Es gibt keine direkt entsprechende Meldung auf der TAPI-Ebene, obwohl diese Meldung mit line \_ devspecificfeature sehr ähnlich ist. Auf der TSPI-Ebene werden die gerätespezifischen Funktions Meldungen zwischen den Berichterstattungs Ereignissen in Zeilen und Adressen und den Bericht Erstellungs Ereignissen bei Aufrufen aufgeteilt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ devspecificfeature**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))
</dt> <dt>

[**TSPI \_ linedevspecificfeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 


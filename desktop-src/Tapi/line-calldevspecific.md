---
description: Die TSPI-zeilige \_ calldevspecific-Nachricht wird an die LineEvent-Rückruffunktion gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die bei einem Aufruf auftreten.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: LINE_CALLDEVSPECIFIC Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48bf8a54a1f326fe7bb27c82349e5575c8bbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354169"
---
# <a name="line_calldevspecific-message"></a>Zeile \_ calldevspecific Message

Die TSPI- **zeilige \_ calldevspecific** -Nachricht wird an die [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -Rückruffunktion gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die bei einem Aufruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter *dwParam1* through *dwParam3* sind gerätespezifisch.


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

Die Wert Zeile \_ calldevspecific.

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

Die **line \_ calldevspecific** -Nachricht wird von einem Dienstanbieter in Verbindung mit der [**TSPI \_ linedevspecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) -Funktion verwendet. Seine Bedeutung ist gerätespezifisch.

TAPI sendet die [**\_ DevSpecific-Zeilen**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) Nachricht als Antwort auf den Empfang dieser Nachricht von einem Dienstanbieter an Anwendungen. Die Parameter " *htline* " und " *htcall"* werden als *hdevice* -Parameter auf der TAPI-Ebene in den entsprechenden *hcallcenter* übersetzt. Die Parameter *dwParam1*, *dwParam2* und *dwParam3* werden unverändert übermittelt.

Es gibt keine direkt entsprechende Meldung auf der TAPI-Ebene, obwohl diese Meldung sehr ähnlich ist wie " [**line \_ DevSpecific**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))". Auf der TSPI-Ebene werden die gerätespezifischen Nachrichten zwischen den Berichterstattungs Ereignissen in Zeilen und Adressen und den Bericht Erstellungs Ereignissen bei Aufrufen aufgeteilt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Linien- \_ DevSpecific**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))
</dt> <dt>

[**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[**TSPI \_ linedevspecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 


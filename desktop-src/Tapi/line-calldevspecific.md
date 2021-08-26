---
description: Die TSPI LINE \_ CALLDEVSPECIFIC-Nachricht wird an die RÜCKRUFfunktion LINEEVENT gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die bei einem Aufruf auftreten.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: LINE_CALLDEVSPECIFIC Meldung (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9930da3c30d51781b10b28ed7a712cb681950eaea1a387212a5e0894658a9125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012600"
---
# <a name="line_calldevspecific-message"></a>LINE \_ CALLDEVSPECIFIC-Nachricht

Die TSPI **LINE \_ CALLDEVSPECIFIC-Nachricht** wird an die [**RÜCKRUFfunktion LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die bei einem Aufruf auftreten. Die Bedeutung der Nachricht und die Interpretation der *dwParam1-Parameter* bis *dwParam3* sind gerätespezifisch.


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

Das nicht transparente TAPI-Objekthandle für das Anrufgerät.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Der Wert LINE \_ CALLDEVSPECIFIC.

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

## <a name="remarks"></a>Hinweise

Die **LINE \_ CALLDEVSPECIFIC-Nachricht** wird von einem Dienstanbieter in Verbindung mit der [**\_ TSPI-Funktion lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) verwendet. Seine Bedeutung ist gerätespezifisch.

TAPI sendet die [**LINE \_ DEVSPECIFIC-Nachricht**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) als Reaktion auf den Empfang dieser Nachricht von einem Dienstanbieter an Anwendungen. Die Parameter *htLine* und *htCall* werden in den entsprechenden *hCall-Parameter* als *hDevice-Parameter* auf TAPI-Ebene übersetzt. Die Parameter *dwParam1,* *dwParam2* und *dwParam3* werden unverändert übergeben.

Es gibt keine direkt entsprechende Nachricht auf TAPI-Ebene, obwohl diese Meldung sehr ähnlich wie [**LINE \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))ist. Auf TSPI-Ebene werden die gerätespezifischen Nachrichten zwischen den Nachrichten, die Ereignisse in Zeilen und Adressen melden, und denen, die Ereignisse bei Aufrufen melden, aufgeteilt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 


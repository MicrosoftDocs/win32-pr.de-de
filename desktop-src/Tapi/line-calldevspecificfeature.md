---
description: Die TSPI LINE \_ CALLDEVSPECIFICFEATURE-Nachricht wird an die RÜCKRUFfunktion LINEEVENT gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile oder Adresse auftreten.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: LINE_CALLDEVSPECIFICFEATURE Meldung (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8dde8377f952f02f021209b01f846ba323cc7dbf8795743422e2c83e457b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873630"
---
# <a name="line_calldevspecificfeature-message"></a>\_LINE CALLDEVSPECIFICFEATURE-Meldung

Die TSPI **LINE \_ CALLDEVSPECIFICFEATURE-Nachricht** wird an die [**RÜCKRUFfunktion LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) gesendet, um TAPI über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile oder Adresse auftreten. Die Bedeutung der Nachricht und die Interpretation der *dwParam1-Parameter* bis *dwParam3* sind gerätespezifisch.


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

Der Wert LINE \_ CALLDEVSPECIFICFEATURE.

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

Die **LINE \_ CALLDEVSPECIFICFEATURE-Nachricht** wird von einem Dienstanbieter in Verbindung mit der [**\_ TSPI-Funktion lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) verwendet. Seine Bedeutung ist gerätespezifisch.

TAPI sendet die [**LINE \_ DEVSPECIFICFEATURE-Nachricht**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) als Reaktion auf den Empfang dieser Nachricht von einem Dienstanbieter an Anwendungen. Die Parameter *htLine* und *htCall* werden in den entsprechenden *hCall-Parameter* als *hDevice-Parameter* auf TAPI-Ebene übersetzt. Die Parameter *dwParam1,* *dwParam2* und *dwParam3* werden unverändert übergeben.

Es gibt keine direkt entsprechende Nachricht auf TAPI-Ebene, obwohl diese Meldung sehr ähnlich wie LINE \_ DEVSPECIFICFEATURE ist. Auf TSPI-Ebene werden die gerätespezifischen Featuremeldungen zwischen den Meldungen zu Ereignissen in Zeilen und Adressen und den Berichten von Ereignissen bei Aufrufen aufgeteilt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))
</dt> <dt>

[**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 


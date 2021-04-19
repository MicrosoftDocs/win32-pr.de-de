---
description: Die TAPI-zeilige \_ callhubclose-Nachricht wird gesendet, wenn ein callhub geschlossen wurde.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: LINE_CALLHUBCLOSE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352987"
---
# <a name="line_callhubclose-message"></a>Zeile \_ callhubclose-Meldung

Die TAPI- **zeilige \_ callhubclose** -Nachricht wird gesendet, wenn ein callhub geschlossen wurde.


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

Reserviert. Auf 0 festlegen.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reserviert. Auf 0 festlegen.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reserviert. Auf 0 festlegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht stammt von TAPI anstelle eines Dienstanbieters, sodass keine entsprechende TSPI-Nachricht vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 





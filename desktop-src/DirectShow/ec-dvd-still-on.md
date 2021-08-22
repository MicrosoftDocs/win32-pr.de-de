---
description: Signalisiert den Anfang aller noch (PGC, Cell oder VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 801db7f1e14002aa6333b18349e259e40928a0cd45958c0e1aa618d1d1143be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119303330"
---
# <a name="ec_dvd_still_on"></a>\_EC-DVD \_ NOCH \_ EINGESCHALTET

Signalisiert den Anfang aller noch (PGC, Cell oder VOBU).

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Boolescher Wert **(BOOL),** der angibt, ob Schaltflächen verfügbar sind. Null (0) gibt an, dass Schaltflächen verfügbar sind, sodass die [**IDvdControl2::StillOff-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) nicht funktioniert. Eine (1) gibt an, dass keine Schaltflächen verfügbar sind, sodass **IDvdControl2::StillOff** funktioniert.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**DWORD-Wert,** der die Anzahl der Sekunden angibt, die der noch dauert. 0xFFFFFFFF gibt eine unendliche Still an, d. h., warten Sie, bis der Benutzer eine Schaltfläche drückt oder bis die Anwendung [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)aufruft.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Alle Kombinationen von Schaltflächen und sind weiterhin möglich (Schaltflächen mit noch eingeschaltet, Schaltflächen mit noch deaktivierter Schaltfläche, Schaltfläche aus mit noch eingeschalteter Schaltfläche, Schaltfläche aus mit noch deaktivierter Schaltfläche).

Dieses Ereignis wird in allen Domänen ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignisbenachrichtigungscodes](dvd-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





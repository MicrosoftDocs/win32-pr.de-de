---
description: 'EC_DVD_VOBU_Timestamp: Wird gesendet, wenn der DVD-Navigator ein PCI-Paket analysiert.'
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36a1dfcf93e44d8d94a0bdf74042ce1d2d2907bcf1f7085b452f56254196dd24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102920"
---
# <a name="ec_dvd_vobu_timestamp"></a>EC \_ DVD \_ VOBU \_ Timestamp

Wird gesendet, wenn [der DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.

Die Ereignisdaten sind der Zeitstempel der letzten Videoobjekteinheit (VOBU).

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Enthält das **low-order-DWORD** des Zeitstempels.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Enthält das obere **DWORD des** Zeitstempels.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Ereignis ist standardmäßig deaktiviert. Um dieses Ereignis zu aktivieren, rufen Sie [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) auf, und legen Sie die **Option DVD \_ EnableLoggingEvents** auf **TRUE fest.**

Rekonstruieren Sie den Zeitstempel wie folgt:


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignisbenachrichtigungscodes](dvd-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Gibt an, dass der DVD-Navigator entweder mit der Wiedergabe begonnen oder die Wiedergabe von Daten abgeschlossen hat.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4edbdb337c4b57a7ed09bd63a8ed4fb0d1946b289b369badab64b561000d3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928570"
---
# <a name="ec_dvd_karaoke_mode"></a>\_EC-DVD \_ –MODUS "DVD–DVD" \_

Gibt an, dass der [DVD-Navigator](data-flow-in-the-dvd-navigator.md) entweder mit der Wiedergabe begonnen oder die Wiedergabe von Daten abgeschlossen hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Boolescher Wert. True gibt an, dass ein 160-Titel wiedergegeben wird. Andernfalls wird kein 160-Titel wiedergegeben.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der DVD-Player signalisiert dieses Ereignis, wenn er Domänen ändert.

Dieses Ereignis wird in allen DVD-Domänen ausgelöst.

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

 

 





---
description: Gibt an, ob ein Winkelblock wiedergegeben wird und Winkeländerungen durchgeführt werden können.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e95c692aed8ac6c709ff0db1d6056fc59219fa73f5aa2e4cfb9b31b2c1a03d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015988"
---
# <a name="ec_dvd_angles_available"></a>EC \_ DVD \_ ANGLES \_ AVAILABLE

Gibt an, ob ein Winkelblock wiedergegeben wird und Winkeländerungen durchgeführt werden können.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Boolescher Wert **(BOOL),** der angibt, ob ein Winkelblock wiedergegeben wird. Null (0) gibt an, dass sich die Wiedergabe nicht in einem Winkelblock befindet und keine Winkel verfügbar sind, Eins (1) gibt an, dass ein Winkelblock wiedergegeben wird und Winkeländerungen durchgeführt werden können.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Winkeländerungen sind nicht auf Winkelblöcke beschränkt, und die Drehung der Winkeländerung kann nur in einem Winkelblock beobachtet werden.

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

 

 





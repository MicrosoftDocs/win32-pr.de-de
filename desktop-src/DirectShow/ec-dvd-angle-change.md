---
description: Signalisiert, dass sich entweder die Anzahl der verfügbaren Winkel geändert hat oder dass sich die aktuelle Winkelnummer geändert hat.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a9a94b9940f58dc26de1c1ba6133e4d5a66a2f34ef96b8aaf59b1a7815a08122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148593"
---
# <a name="ec_dvd_angle_change"></a>EC \_ DVD \_ ANGLE \_ CHANGE

Signalisiert, dass sich entweder die Anzahl der verfügbaren Winkel geändert hat oder dass sich die aktuelle Winkelnummer geändert hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der die Anzahl der verfügbaren Winkel angibt. Wenn die Anzahl der verfügbaren Winkel 1 beträgt, ist das aktuelle Video nicht verschränkt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**DWORD-Wert,** der die aktuelle Winkelnummer angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Winkelzahlen liegen zwischen 1 und 9.

Die aktuelle Winkelnummer kann automatisch mit einem Navigationsbefehl geändert werden, der auf dem Datenträger erstellt wurde, sowie über die Anwendungssteuerung mithilfe der [**IDvdControl2-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

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

 

 





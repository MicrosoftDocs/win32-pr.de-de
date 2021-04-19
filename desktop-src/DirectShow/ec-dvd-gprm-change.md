---
description: Wird gesendet, wenn sich der Wert eines allgemeinen Parameter Registers (GPRM) ändert.
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: EC_DVD_GPRM_Change (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f67a8646a72689c2570462f7dc4aeee6b2474136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360330"
---
# <a name="ec_dvd_gprm_change"></a>Änderungen an der EC- \_ DVD- \_ GPRM \_

Wird gesendet, wenn sich der Wert eines allgemeinen Parameter Registers (GPRM) ändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Der null basierte Index des GPRM-Werts, der geändert wurde.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Die unteren 16 Bits enthalten den neuen GPRM-Wert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis ist standardmäßig deaktiviert. Um dieses Ereignis zu aktivieren, müssen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) aufrufen und die Option " **DVD \_ enableloggingevents** " auf " **true**" festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdevcode. h (Include DShow. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> <dt>

[DVD-Ereignis Benachrichtigungs Codes](dvd-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[**IDvdInfo2:: getallgprms**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 





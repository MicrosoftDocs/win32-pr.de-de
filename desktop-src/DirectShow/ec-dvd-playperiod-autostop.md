---
description: Gibt an, dass der Navigator die Wiedergabe des Segments abgeschlossen hat, das in einem IDvdControl2::P layperiodintitleautoend angegeben ist.
ms.assetid: 1716eabe-f106-436a-8a6a-ca43cee9341c
title: EC_DVD_PLAYPERIOD_AUTOSTOP (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYPERIOD_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c2081c8a5b7e5b6bd2165781af9552722ed9ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366965"
---
# <a name="ec_dvd_playperiod_autostop"></a>EC- \_ DVD- \_ playperiod \_ autostopps

Gibt an, dass der Navigator die Wiedergabe des Segments abgeschlossen hat, das in einem [**IDvdControl2::P layperiodintitleautoend**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)angegeben ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Keinen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird in der Titel Domäne ausgelöst.

Dieses Ereignis wird auch gesendet, wenn die Wiedergabe abgebrochen wird, bevor der Navigator die Wiedergabe des angegebenen Segments beendet.

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

[**IDvdControl2::P layperiodintitleautostoppt**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)
</dt> </dl>

 

 





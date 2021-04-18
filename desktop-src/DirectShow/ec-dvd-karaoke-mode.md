---
description: Gibt an, dass der DVD-Navigator entweder mit dem wiedergeben oder Beenden der Karaoke-Daten begonnen hat.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (dvdevcode. h)
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
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364894"
---
# <a name="ec_dvd_karaoke_mode"></a>EC- \_ DVD- \_ Karaoke- \_ Modus

Gibt an, dass der [DVD-Navigator](data-flow-in-the-dvd-navigator.md) entweder mit dem wiedergeben oder Beenden der Karaoke-Daten begonnen hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Boolescher Wert. **True** gibt an, dass eine Karaoke-Spur wiedergegeben wird. Andernfalls wird kein Karaoke-Track abgespielt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der DVD-Player signalisiert dieses Ereignis, wenn die Domänen geändert werden.

Dieses Ereignis wird in allen DVD-Domänen ausgelöst.

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
</dt> </dl>

 

 





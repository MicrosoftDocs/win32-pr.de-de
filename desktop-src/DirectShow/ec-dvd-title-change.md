---
description: Gibt an, wann die aktuelle DVD-Titel Nummer geändert wird.
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: EC_DVD_TITLE_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9539d29704797b1c7b001d426250762d2ed27b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365961"
---
# <a name="ec_dvd_title_change"></a>Änderung des EC- \_ DVD- \_ Titels \_

Gibt an, wann die aktuelle DVD-Titel Nummer geändert wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** -Wert, der die neue Titel Nummer angibt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Titelnummern liegen zwischen 1 und 99. Diese Zahl gibt den TTN an, bei dem es sich um die Titel Nummer in Bezug auf die gesamte Festplatte handelt, nicht um die VTS-TTN, bei der es sich \_ um die Titel Nummer in Bezug auf einen aktuellen VTS handelt.

Dieses Ereignis wird in der Titel Domäne ausgelöst.

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

 

 





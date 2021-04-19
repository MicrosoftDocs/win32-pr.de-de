---
description: Gibt an, ob ein Winkel Block wiedergegeben und Winkel Änderungen durchgeführt werden können.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (dvdevcode. h)
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
ms.openlocfilehash: e4d2abb17b329323cf4a21128da5dba927b48d4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373914"
---
# <a name="ec_dvd_angles_available"></a>EC- \_ DVD- \_ Winkel \_ verfügbar

Gibt an, ob ein Winkel Block wiedergegeben und Winkel Änderungen durchgeführt werden können.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Boolescher Wert (**boolescher** Wert), der angibt, ob ein Winkel Block wiedergegeben wird. NULL (0) gibt an, dass die Wiedergabe nicht in einem Winkel Block vorhanden ist und keine Winkel verfügbar sind, eins (1) gibt an, dass ein Winkel Block wiedergegeben wird und Winkel Änderungen durchgeführt werden können.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Winkel Änderungen sind nicht auf Winkel Blöcke beschränkt, und die Darstellung der Winkel Änderung kann nur in einem Winkel Block angezeigt werden.

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

 

 





---
description: Wird gesendet, wenn sich die aktuelle Programm Kette (PGC) ändert.
ms.assetid: 80fcd059-6ab4-4116-ac3a-012c451237b3
title: EC_DVD_PROGRAM_CHAIN_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CHAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: eefd45ac1d147a0409417f215e56a4db490dfdbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368359"
---
# <a name="ec_dvd_program_chain_change"></a>Änderung der EC- \_ DVD- \_ Programm \_ Kette \_

Wird gesendet, wenn sich die aktuelle Programm Kette (PGC) ändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Die neue Programm Ketten Nummer (pgcn).

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Der Gebiets Schema Bezeichner (Locale Identifier, LCID) der Audiosprache.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis ist standardmäßig deaktiviert. Um dieses Ereignis zu aktivieren, nennen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , und legen Sie die Option **DVD \_ notifypositionchange** auf **true** fest.

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

 

 





---
description: Signalisiert, dass der DVD-Player die Wiedergabe eines neuen Programms in der Domäne DVD DOMAIN Title gestartet \_ \_ hat.
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: EC_DVD_CHAPTER_START (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9570964efa52380c06034716f0c199cde0498a2c0aeb0502f9db250f87a6ca3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998100"
---
# <a name="ec_dvd_chapter_start"></a>EC \_ DVD \_ CHAPTER \_ START

Signalisiert, dass der DVD-Player die Wiedergabe eines neuen Programms in der Domäne DVD DOMAIN Title gestartet \_ \_ hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der die neue Kapitelnummer (Programmnummer) angibt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Nur einfache lineare Filme signalisieren dieses Ereignis.

Dieses Ereignis wird in der Titeldomäne ausgelöst.

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
</dt> <dt>

[**DVD \_ DOMAIN Enumeration**](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 





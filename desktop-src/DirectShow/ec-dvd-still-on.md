---
description: Signalisiert den Anfang aller weiterhin (PGC, Cell oder vobu).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368324"
---
# <a name="ec_dvd_still_on"></a>EC- \_ DVD \_ weiterhin \_ on

Signalisiert den Anfang aller weiterhin (PGC, Cell oder vobu).

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Boolescher Wert (**boolescher** Wert), der angibt, ob Schaltflächen verfügbar sind. NULL (0) gibt an, dass Schaltflächen verfügbar sind, sodass die [**IDvdControl2:: stilloff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) -Methode nicht funktioniert. Eins (1) gibt an, dass keine Schaltflächen verfügbar sind, sodass **IDvdControl2:: stilloff** funktioniert.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**DWORD** -Wert, der die Anzahl der Sekunden angibt, die noch zuletzt verwendet werden. 0xFFFFFFFF gibt immer noch unendlich an, was bedeutet, bis der Benutzer auf eine Schaltfläche drückt, oder bis die Anwendung [**IDvdControl2:: stilloff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)aufruft.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle Kombinationen von Schaltflächen und sind immer noch möglich (Schaltflächen auf, bei denen immer noch angezeigt wird, Schaltflächen mit "nach unten", Schaltfläche "weiter", Schaltfläche "aus" und "nach

Dieses Ereignis wird in allen Domänen ausgelöst.

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

 

 





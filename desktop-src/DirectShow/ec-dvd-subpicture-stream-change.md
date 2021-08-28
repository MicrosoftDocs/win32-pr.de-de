---
description: Signalisiert, dass sich die aktuelle Datenstromnummer für den Haupttitel geändert hat.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 21549ec6427b82c6d229d2e3962689bc8879815429f3a68fd32d54283c30d6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639770"
---
# <a name="ec_dvd_subpicture_stream_change"></a>EC \_ DVD \_ SUBPICTURE \_ STREAM \_ CHANGE

Signalisiert, dass sich die aktuelle Datenstromnummer für den Haupttitel geändert hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der die neue Streamnummer der Benutzerunterdrückung angibt. Subpicture-Datenstromnummern liegen zwischen 0 und 31. Stream 0xFFFFFFFF gibt an, dass kein Stream ausgewählt ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Boolescher Wert, der den Ein-/Aus-Zustand der Unterbildung angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Teilbild kann automatisch mit einem Navigationsbefehl geändert werden, der auf dem Datenträger sowie über die Anwendungssteuerung mit [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)erstellt wurde.

Dieses Ereignis wird in allen Domänen ausgelöst.

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
</dt> </dl>

 

 





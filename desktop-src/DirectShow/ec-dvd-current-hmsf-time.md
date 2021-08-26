---
description: Signalisiert die aktuelle Zeit im DVD \_ HMSF \_ TIMECODE-Format relativ zum Anfang des Titels. Dieses Ereignis wird am Anfang jedes VOBU ausgelöst, das alle 0,4 bis 1,0 Sekunden auftritt.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 52a6eb077599b4fe6dfd89267974cb71c0c5a58a65d6c52307d77eb3e98201d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965810"
---
# <a name="ec_dvd_current_hmsf_time"></a>EC \_ DVD \_ CURRENT \_ HMSF \_ TIME

Signalisiert die aktuelle Zeit im [**DVD \_ HMSF \_ TIMECODE-Format**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) relativ zum Anfang des Titels. Dieses Ereignis wird am Anfang jedes VOBU ausgelöst, das alle 0,4 bis 1,0 Sekunden auftritt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Ein ULONG-Wert, der die \_ \_ HMSF-TIMECODE-Struktur der DVD enthält. Weisen Sie lParam1 einer ULONG-Variablen zu, und konvertieren Sie diese Variable dann in eine DVD \_ HMSF \_ TIMECODE, um auf ihre Werte zu zugreifen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ein ULONG-Wert, der eine Vereinigung von [**DVD \_ TIMECODE \_ FLAGS enthält.**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das DVD HMSF TIMECODE-Format soll das alte BCD-Format ersetzen, das \_ in EC DVD CURRENT \_ \_ \_ \_ TIME-Ereignissen zurückgegeben wird. Die HMSF-Zeitcodes sind einfacher zu arbeiten. Damit der Navigator EC \_ DVD \_ CURRENT \_ HMSF TIME-Ereignisse anstelle von EC DVD CURRENT TIME-Ereignissen sendet, muss \_ eine Anwendung \_ \_ \_ `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` aufrufen. Wenn dieses Flag festgelegt ist, erwartet der Navigator auch, dass alle Zeitparameter in den [**Methoden IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) als DVD \_ HMSF \_ TIMECODEs übergeben werden.

Dieses Ereignis wird in den Titeldomänen ausgelöst.

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

 

 





---
description: Signalisiert die aktuelle Zeit im DVD- \_ hmsf- \_ Zeit Code Format relativ zum Anfang des Titels. Dieses Ereignis wird am Anfang jeder vobu ausgelöst, die alle 0,4 bis 1,0 Sekunden auftritt.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (dvdevcode. h)
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
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365944"
---
# <a name="ec_dvd_current_hmsf_time"></a>EC- \_ DVD \_ aktuelle \_ hmsf- \_ Zeit

Signalisiert die aktuelle Zeit im [**DVD- \_ hmsf- \_ Zeit Code**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) Format relativ zum Anfang des Titels. Dieses Ereignis wird am Anfang jeder vobu ausgelöst, die alle 0,4 bis 1,0 Sekunden auftritt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Ein ULONG-Wert, der die \_ hmsf- \_ Zeit Code Struktur der DVD enthält. Weisen Sie lParam1 einer ULONG-Variablen zu, und wandeln Sie diese Variable dann in eine DVD- \_ hmsf- \_ Zeit Leitzahl um, um auf ihre Werte zuzugreifen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ein ULONG-Wert, der eine Union von [**DVD- \_ \_ timecodeflags**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das \_ hmsf-Zeit \_ Code Format in DVD soll das alte BCD-Format ersetzen, das in den \_ \_ aktuellen Zeit Ereignissen der EC-DVD zurückgegeben wird \_ . Die hmsf-Timecodes sind einfacher zu arbeiten. Damit der Navigator die aktuellen \_ hmsf-Zeit Ereignisse der EC-DVD und nicht die \_ \_ \_ \_ aktuellen Zeit Ereignisse der EC-DVD sendet \_ \_ , muss eine Anwendung aufgerufen werden `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` . Wenn dieses Flag festgelegt wird, erwartet der Navigator auch, dass alle Zeitparameter in den [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Methoden als DVD- \_ hmsf-Timecodes übermittelt werden \_ .

Dieses Ereignis wird in den Titel Domänen ausgelöst.

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

 

 





---
description: Signalisiert, dass sich die aktuelle Audiostreamnummer für den DVD-Haupttitel geändert hat.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2ad6015ef132a98d02dc207cb9d43b6324ea3a05c541f43e295e75d13b5bb7ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998130"
---
# <a name="ec_dvd_audio_stream_change"></a>ÄNDERUNG DES \_ \_ EC-DVD-AUDIOSTREAMS \_ \_

Signalisiert, dass sich die aktuelle Audiostreamnummer für den DVD-Haupttitel geändert hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD-Wert,** der die neue Audiostreamnummer des Benutzers angibt. Audiostreamnummern liegen zwischen 0 und 7. Stream 0xFFFFFFFF gibt an, dass kein Stream ausgewählt ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der aktuelle Audiostream kann automatisch mit einem Navigationsbefehl geändert werden, der auf dem Datenträger erstellt wurde, sowie über die Anwendungssteuerung mithilfe der [**IDvdControl2-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

Dieses Ereignis wird in allen Domänen ausgelöst.

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

 

 





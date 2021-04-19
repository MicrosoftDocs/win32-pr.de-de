---
description: Signalisiert, dass die aktuelle audiostreamnummer für den DVD-Haupttitel geändert wurde.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (dvdevcode. h)
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
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370265"
---
# <a name="ec_dvd_audio_stream_change"></a>Änderung des EC \_ \_ -DVD- \_ Audiostreams \_

Signalisiert, dass die aktuelle audiostreamnummer für den DVD-Haupttitel geändert wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** -Wert, der die neue audiostreamnummer des Benutzers angibt. Audiostreamnummern reichen von 0 bis 7. Der Stream 0xFFFFFFFF gibt an, dass kein Stream ausgewählt ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der aktuelle Audiostream kann sich automatisch ändern, indem ein Navigations Befehl, der auf der Festplatte erstellt wurde, sowie über die Anwendungssteuerung mithilfe der [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) -Schnittstelle erstellt wird.

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

 

 





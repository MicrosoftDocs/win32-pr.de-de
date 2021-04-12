---
description: Beim Streaming ist ein nicht schwerwiegender Fehler aufgetreten.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Menonfatalerror-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344619"
---
# <a name="menonfatalerror-event"></a>Menonfatalerror-Ereignis

Beim Streaming ist ein nicht schwerwiegender Fehler aufgetreten. Jede Media Foundation Komponente kann dieses Ereignis jederzeit senden.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE            | BESCHREIBUNG                                                        |
|--------------------|--------------------------------------------------------------------|
| VT \_ UI4<br/> | **HRESULT** -Wert, der den Fehler beschreibt.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind keine Attribute definiert.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis signalisiert einen unerwarteten, aber wiederherstellbaren Fehler beim Streaming. Beispielsweise kann eine Medienquelle dieses Ereignis senden, wenn es ein Paket löscht.

Senden Sie dieses Ereignis nicht, um zu signalisieren, dass eine asynchrone Methode fehlgeschlagen ist. Wenn eine asynchrone Methode fehlschlägt, wird der Fehlercode im normalen Ereignis für diese Methode zurückgegeben.

Wenn ein nicht BEHEB barer Streamingfehler auftritt, senden Sie das [meerror](meerror.md) -Ereignis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 





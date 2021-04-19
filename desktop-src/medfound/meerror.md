---
description: 'Signalisiert einen schwerwiegenden Fehler. Jede Media Foundation Komponente kann dieses Ereignis jederzeit senden. Wenn Sie imfmediaevent:: GetStatus aufrufen, erhalten Sie den Fehlercode des Vorgangs, bei dem ein Fehler aufgetreten ist.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Meerror-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356868"
---
# <a name="meerror-event"></a>Meerror-Ereignis

Signalisiert einen schwerwiegenden Fehler. Jede Media Foundation Komponente kann dieses Ereignis jederzeit senden. [**Wenn Sie imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) aufrufen, erhalten Sie den Fehlercode des Vorgangs, bei dem ein Fehler aufgetreten ist.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis sollte nur für unerwartete Fehler verwendet werden. Senden Sie dieses Ereignis nicht, um zu signalisieren, dass eine asynchrone Methode fehlgeschlagen ist. Wenn eine asynchrone Methode fehlschlägt, wird der Fehlercode im normalen Ereignis für diese Methode zurückgegeben.

Wenn beim Streaming ein BEHEB barer Fehler auftritt, senden Sie das [menonfatalerror](menonfatalerror.md) -Ereignis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 





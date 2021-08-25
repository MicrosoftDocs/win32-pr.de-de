---
description: Signalisiert einen schwerwiegenden Fehler. Jedes Media Foundation kann dieses Ereignis jederzeit senden. Rufen Sie DIEMEDIAEvent::GetStatus auf, um den Fehlercode des fehlgeschlagenen Vorgangs zu erhalten.
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: MEError-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd012bf7fbb7f21f37201a67f5c203f5981be6aa16795e2a3c37d16ea268f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941470"
---
# <a name="meerror-event"></a>MEError-Ereignis

Signalisiert einen schwerwiegenden Fehler. Jedes Media Foundation kann dieses Ereignis jederzeit senden. Rufen [**Sie DIEMEDIAEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) auf, um den Fehlercode des fehlgeschlagenen Vorgangs zu erhalten.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis sollte nur für unerwartete Fehler verwendet werden. Senden Sie dieses Ereignis nicht, um zu signalisieren, dass eine asynchrone Methode fehlgeschlagen ist. Wenn bei einer asynchronen Methode ein Fehler auftritt, wird der Fehlercode im normalen Ereignis für diese Methode zurückgegeben.

Wenn während des Streamings ein behebbarer Fehler auftritt, senden Sie das [MENonFatalError-Ereignis.](menonfatalerror.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 





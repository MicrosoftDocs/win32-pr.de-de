---
description: Wird von einer vertrauenswürdigen Ausgabe ausgelöst, wenn beim Erzwingen der Ausgabe Richtlinie ein Fehler auftritt.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Mepolicyerror-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348518"
---
# <a name="mepolicyerror-event"></a>Mepolicyerror-Ereignis

Wird von einer vertrauenswürdigen Ausgabe ausgelöst, wenn beim Erzwingen der Ausgabe Richtlinie ein Fehler auftritt.

Wenn die Medien Sitzung dieses Ereignis empfängt, beendet Sie die Wiedergabe und leitet das Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Mögliche Werte, die von [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) abgerufen werden, sind die folgenden.



| Wert                      | BESCHREIBUNG                                                    |
|----------------------------|----------------------------------------------------------------|
| MF \_ E- \_ Richtlinie \_ nicht unterstützt | Die vertrauenswürdige Ausgabe unterstützt die aktuelle Ausgabe Richtlinie nicht. |



 

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

 

 





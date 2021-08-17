---
description: Wird von einer vertrauenswürdigen Ausgabe ausgelöst, wenn beim Erzwingen der Ausgaberichtlinie ein Fehler auftritt.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: MEPolicyError-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1f0d05b73ea295ea3282af5950d4a9a61f833f61463cd095848563e3858c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877547"
---
# <a name="mepolicyerror-event"></a>MEPolicyError-Ereignis

Wird von einer vertrauenswürdigen Ausgabe ausgelöst, wenn beim Erzwingen der Ausgaberichtlinie ein Fehler auftritt.

Wenn die Mediensitzung dieses Ereignis empfängt, beendet sie die Wiedergabe und leitet das Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Mögliche Werte, die von [**DERMEDIAEVENT::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) abgerufen werden, sind:



| Wert                      | Beschreibung                                                    |
|----------------------------|----------------------------------------------------------------|
| MF \_ \_ E-RICHTLINIE \_ NICHT UNTERSTÜTZT | Die vertrauenswürdige Ausgabe unterstützt die aktuelle Ausgaberichtlinie nicht. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 





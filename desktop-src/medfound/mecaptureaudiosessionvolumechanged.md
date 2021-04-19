---
description: Wird von einer audioerfassungs Quelle gesendet, wenn das Volume geändert wird.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Mecaptureaudiosessionvolumechaning-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356546"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a>Mecaptureaudiosessionvolumechaning-Ereignis

Wird von einer audioerfassungs Quelle gesendet, wenn das Volume geändert wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE               | BESCHREIBUNG                           |
|-----------------------|---------------------------------------|
| VT \_ leer <br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird vom Mediendaten Strom der audioerfassungs Quelle gesendet.

Die audioerfassungs Quelle sendet dieses Ereignis, wenn das Volume durch eine externe Aktion geändert wird – z. b. wenn der Benutzer das Volume über die Systemsteuerung ändert. Die Erfassungs Quelle sendet das Ereignis nicht, wenn die Anwendung das Volume direkt in der Quelle ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 





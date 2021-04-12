---
description: Signalisiert, dass eine Medienquelle den Versuch, eine erneute Verbindung mit dem Server herzustellen, abgeschlossen hat.
ms.assetid: 228e069a-a26b-472e-915e-ff9aec5ee9c1
title: Mereconnectend-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3477abd5d4413faa6b2d965f7ace2d19c48dd786
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528268"
---
# <a name="mereconnectend-event"></a>Mereconnectend-Ereignis

Signalisiert, dass eine Medienquelle den Versuch, eine erneute Verbindung mit dem Server herzustellen, abgeschlossen hat.

Ausgelöst durch eine Medienquelle am Ende eines erneuten Verbindungsversuchs. Die Netzwerkquelle löst dieses Ereignis aus, wenn es erneut eine Verbindung mit dem Server herstellt. Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



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

 

 





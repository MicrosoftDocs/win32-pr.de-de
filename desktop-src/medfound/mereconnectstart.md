---
description: Signalisiert, dass eine Medienquelle versucht, eine erneute Verbindung mit dem Server herzustellen.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: Mereconnectstart-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21944e937f52205416b5e6e2b52d18c3a3c768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130741"
---
# <a name="mereconnectstart-event"></a>Mereconnectstart-Ereignis

Signalisiert, dass eine Medienquelle versucht, eine erneute Verbindung mit dem Server herzustellen.

Ausgelöst durch eine Medienquelle zu Beginn eines erneuten Verbindungsversuchs. Die Netzwerkquelle löst dieses Ereignis aus, wenn versucht wird, erneut eine Verbindung mit dem Server herzustellen. Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.

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

 

 





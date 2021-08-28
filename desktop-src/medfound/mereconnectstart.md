---
description: Signalisiert, dass eine Medienquelle versucht, erneut eine Verbindung mit dem Server herzustellen.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: MEReconnectStart-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc365acf5d91796b6d9c3fe371b9a0ec54435769381c41f0bf45cedb73003660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114010"
---
# <a name="mereconnectstart-event"></a>MEReconnectStart-Ereignis

Signalisiert, dass eine Medienquelle versucht, erneut eine Verbindung mit dem Server herzustellen.

Wird von einer Medienquelle zu Beginn eines Verbindungswiederherstellungsversuchs ausgelöst. Die Netzwerkquelle löst dieses Ereignis aus, wenn versucht wird, erneut eine Verbindung mit dem Server herzustellen. Die Mediensitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 





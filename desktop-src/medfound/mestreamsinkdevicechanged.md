---
description: Wird von den streamsenken des erweiterten Videorenderers (EVR) ausgelöst, wenn sich das Videogerät ändert.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Mestreamsinkdevicechanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343720"
---
# <a name="mestreamsinkdevicechanged-event"></a>Mestreamsinkdevicechanged-Ereignis

Wird von den streamsenken des erweiterten Videorenderers (EVR) ausgelöst, wenn sich das Videogerät ändert. Beispielsweise löst der EVR dieses Ereignis aus, wenn es ein [**\_ \_ geändertes**](../directshow/ec-display-changed.md) Ereignis der EC-Anzeige empfängt.

Die Media Foundation Pipeline antwortet auf dieses Ereignis, indem alle Beispiel Anforderungen, bei denen das Gerät geändert wurde, erneut übermittelt werden.

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
</dt> <dt>

[Medien senken](media-sinks.md)
</dt> </dl>

 

 

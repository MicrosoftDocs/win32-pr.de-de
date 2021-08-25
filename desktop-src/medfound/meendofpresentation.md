---
description: Wird von einer Medienquelle ausgelöst, wenn eine Präsentation endet. Dieses Ereignis signalisiert, dass alle Streams in der Präsentation vollständig sind. Die Mediensitzung gibt dieses Ereignis an die Anwendung weiter.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: MEEndOfPresentation-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e97a2689b8d0e2ae156daa84f27f0e10fb31b828ffedf027a7be47a6c330b7b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941459"
---
# <a name="meendofpresentation-event"></a>MEEndOfPresentation-Ereignis

Wird von einer Medienquelle ausgelöst, wenn eine Präsentation endet. Dieses Ereignis signalisiert, dass alle Streams in der Präsentation vollständig sind. Die Mediensitzung gibt dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                                               | BESCHREIBUNG                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**DIE \_ \_ MF-EREIGNISQUELLENTOPOLOGIE \_ \_ WURDE ABGEBROCHEN.**](mf-event-source-topology-canceled-attribute.md)<br/> | Gibt an, ob die Sequencerquelle diese Präsentation abgebrochen hat.<br/> <br/> |



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

 

 





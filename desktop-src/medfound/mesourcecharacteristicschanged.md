---
description: Wird von einer Medienquelle ausgelöst, wenn sich die Eigenschaften der Quellen ändern.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: MESourceCharacteristicsChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd69be00727ec3f1f635b82fb6c8e29c4016959ced480be4e9de6b8a83cfe8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877368"
---
# <a name="mesourcecharacteristicschanged-event"></a>MESourceCharacteristicsChanged-Ereignis

Wird von einer Medienquelle ausgelöst, wenn sich die Eigenschaften der Quelle ändern.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                                                   | Beschreibung                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**MERKMALE DER \_ \_ MF-EREIGNISQUELLE \_**](mf-event-source-characteristics-attribute.md)<br/>          | Neue Merkmale der Medienquelle.<br/> <br/>      |
| [**\_ \_ MF-EREIGNISQUELLENMERKMALE \_ \_ ALT**](mf-event-source-characteristics-old-attribute.md)<br/> | Vorherige Merkmale der Medienquelle.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**VERSIERTMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 





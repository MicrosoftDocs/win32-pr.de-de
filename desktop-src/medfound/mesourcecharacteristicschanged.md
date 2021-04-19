---
description: Wird von einer Medienquelle ausgelöst, wenn sich die Merkmale der Quellen ändern.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Mesourcecharakteristicschangi-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349107"
---
# <a name="mesourcecharacteristicschanged-event"></a>Mesourcecharakteristicschge-Ereignis

Wird von einer Medienquelle ausgelöst, wenn sich die Merkmale der Quelle ändern.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                                                   | BESCHREIBUNG                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Eigenschaften der MF- \_ Ereignis \_ Quelle \_**](mf-event-source-characteristics-attribute.md)<br/>          | Neue Merkmale der Medienquelle.<br/> <br/>      |
| [**Eigenschaften der MF- \_ Ereignis \_ Quelle \_ \_ alt**](mf-event-source-characteristics-old-attribute.md)<br/> | Vorherige Merkmale der Medienquelle.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 





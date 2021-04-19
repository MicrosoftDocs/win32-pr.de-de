---
description: Wird von einer vertrauenswürdigen Ausgabe ausgelöst, um Statusinformationen zur Durchsetzung der Ausgabe Richtlinie zu senden.
ms.assetid: 4906f6c3-1570-421f-aef1-914bd338bb1f
title: Mepolicyreport-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0053fb551a69b820beeb4237211cb9af446f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372944"
---
# <a name="mepolicyreport-event"></a>Mepolicyreport-Ereignis

Wird von einer vertrauenswürdigen Ausgabe ausgelöst, um Statusinformationen zur Durchsetzung der Ausgabe Richtlinie zu senden.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Die Attribute und Statuscodes für dieses Ereignis hängen von dem spezifischen Inhalts Schutzsystem ab, das von der vertrauenswürdigen Ausgabe erzwungen wird.

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

 

 





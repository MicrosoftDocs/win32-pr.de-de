---
description: Wird von der Medien Sitzung ausgelöst, wenn sich die Sitzungs Funktionen ändern.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Mesessioncapabilitieschangi-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357453"
---
# <a name="mesessioncapabilitieschanged-event"></a>Mesessioncapabilitieschangi-Ereignis

Wird von der Medien Sitzung ausgelöst, wenn sich die Sitzungs Funktionen ändern.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Das Ereignis enthält die folgenden Attribute.



| Attribut                                                                     | BESCHREIBUNG                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**MF- \_ Ereignis \_ sessioncaps**](mf-event-sessioncaps-attribute.md)              | Neue sitzungsfunktions-Flags.                  |
| [**\_Delta-Ereignis \_ sessioncaps- \_ Delta**](mf-event-sessioncaps-delta-attribute.md) | Gibt an, welche Funktionen Flags geändert wurden. |



 

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

 

 





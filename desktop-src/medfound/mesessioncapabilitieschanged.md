---
description: Wird von der Mediensitzung ausgelöst, wenn sich die Sitzungsfunktionen ändern.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: MESessionCapabilitiesChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc97cb5168957f34cc029a982447c6d4775075ea6f9b9b250ce7b9fd7f1791d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464870"
---
# <a name="mesessioncapabilitieschanged-event"></a>MESessionCapabilitiesChanged-Ereignis

Wird von der Mediensitzung ausgelöst, wenn sich die Sitzungsfunktionen ändern.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Das -Ereignis enthält die folgenden Attribute.



| attribute                                                                     | BESCHREIBUNG                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**\_SESSIONCAPS FÜR MF-EREIGNISSE \_**](mf-event-sessioncaps-attribute.md)              | Neue Flags für Sitzungsfunktionen.                  |
| [**MF \_ EVENT \_ SESSIONCAPS \_ DELTA**](mf-event-sessioncaps-delta-attribute.md) | Gibt an, welche Funktionenflags geändert wurden. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 





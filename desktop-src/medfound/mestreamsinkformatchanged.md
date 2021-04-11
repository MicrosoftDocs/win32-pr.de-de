---
description: Wird durch eine streamsenke ausgelöst, wenn der senken-Medientyp nicht mehr gültig ist.
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: Mestreamsinkformatchanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215158"
---
# <a name="mestreamsinkformatchanged-event"></a>Mestreamsinkformatchanged-Ereignis

Wird durch eine streamsenke ausgelöst, wenn der Medientyp der Senke nicht mehr gültig ist.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Eine streamsenke kann dies auch dann auslösen, wenn etwas passiert, das den Medientyp der Stream-Senke ungültig macht. Beispielsweise sendet der erweiterte Videorenderer (EVR) dieses Ereignis, wenn die Anzeige geändert wird.

Der **HRESULT** -Wert, der von [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) abgerufen wird, kann darauf hinweisen, warum der Medientyp nicht mehr gültig ist.

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

 

 





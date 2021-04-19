---
description: Wird vom audiorenderer ausgelöst, wenn sich das Symbol für die Audiositzung ändert.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Meaudiosessionieschanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350493"
---
# <a name="meaudiosessioniconchanged-event"></a>Meaudiosessionieschanged-Ereignis

Wird vom audiorenderer ausgelöst, wenn sich das Symbol für die Audiositzung ändert.

Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ leer<br/>   | Keine Ereignisdaten.<br/> <br/>                                                     |
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird von der streamsenke des audiorenderer gesendet. Das-Ereignis wird ausgelöst, wenn der audiorenderer ein [**iaudiosessionevents:: oniconpathchanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) -Ereignis von der Audiositzung empfängt.

Um das neue Symbol abzurufen, nennen Sie [**imfaudiopolicy:: geticopath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imbaudiopolicy:: getirepath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 

---
description: Wird vom audiorenderer ausgelöst, wenn sich das Standard Audioformat für das Audiogerät ändert. Der audiorenderer ist nun ungültig.
ms.assetid: eeef764a-f6d2-4f6e-9af3-acd5fd7bc55c
title: Meaudiosessionformatchanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1faddc73622c65d1eb32e0d723f576b9410d978b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863071"
---
# <a name="meaudiosessionformatchanged-event"></a>Meaudiosessionformatchanged-Ereignis

Wird vom audiorenderer ausgelöst, wenn sich das Standard Audioformat für das Audiogerät ändert. Der audiorenderer ist nun ungültig.

Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ leer<br/>   | Keine Ereignisdaten.<br/> <br/>                                                     |
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird von der streamsenke des audiorenderer gesendet. Das Ereignis wird ausgelöst, wenn der audiorenderer ein [**iaudiosessionevents:: onsessiongetrennte**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) -Ereignis von der Audiositzung im Benutzermodus mit dem Trennungsgrund " **disconnectiononformatchanged**" empfängt.

Der [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Zeiger ist, wenn er festgelegt ist, nicht nützlich, da der Audiodatenstrom nicht mehr gültig ist.

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

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 

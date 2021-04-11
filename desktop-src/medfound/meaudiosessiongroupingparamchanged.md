---
description: Wird vom audiorenderer ausgelöst, wenn sich die Gruppierungs Parameter für die Audiositzung ändern.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Meaudiosessiongroupingparamchanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214840"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a>Meaudiosessiongroupingparamchanged-Ereignis

Wird vom audiorenderer ausgelöst, wenn sich die Gruppierungs Parameter für die Audiositzung ändern.

Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird von der streamsenke des audiorenderer gesendet. Das-Ereignis wird ausgelöst, wenn der audiorenderer ein [**iaudiosessionevents:: ongroupingparamchanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) -Ereignis von der Audiositzung empfängt.

Um die neuen Gruppierungs Parameter abzurufen, nennen Sie [**imfaudiopolicy:: getgroupingparam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).

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

[**IMF audiopolicy:: getgroupingparam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 

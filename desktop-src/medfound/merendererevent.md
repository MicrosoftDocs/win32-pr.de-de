---
description: Signalisiert ein Ereignis aus einer Medien Senke, die Mediendaten rendert.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Merendererevent-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215166"
---
# <a name="merendererevent-event"></a>Merendererevent-Ereignis

Signalisiert ein Ereignis aus einer Medien Senke, die Mediendaten rendert.

Der [Erweiterte Videorenderer](enhanced-video-renderer.md) (EVR) sendet dieses Ereignis, wenn es ein Benutzer Ereignis aus dem EVR Presenter empfängt.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE           | BESCHREIBUNG                        |
|-------------------|------------------------------------|
| VT \_ I4<br/> | Ereignis Code.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Wenn der Presenter die **imediaeventsink:: notify** -Methode von EVR mit einem Ereignis Code im Bereich EC \_ User oder höher aufruft, sendet der EVR dieses Ereignis. Bei den Ereignisdaten handelt es sich um den Ereignis Code, der an die **Benachrichtigungs** Methode übermittelt wurde.

Die ursprünglichen Ereignis Parameter (*EventParam1* und *EventParam2* in der **imediaeventsink:: notify** -Methode) werden ignoriert, daher sollte der Presenter diese Werte auf **null** festlegen.

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

 

 





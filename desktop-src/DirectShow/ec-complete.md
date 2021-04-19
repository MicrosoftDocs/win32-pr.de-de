---
description: Alle Daten aus einem bestimmten Stream wurden gerendert.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361512"
---
# <a name="ec_complete"></a>EC \_ Complete

Alle Daten aus einem bestimmten Stream wurden gerendert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Der Status des Streams bei Abschluss. Wenn während der Wiedergabe keine Fehler aufgetreten sind, ist der Wert S \_ OK.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) 0 (null) oder ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Renderers.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Standardmäßig führt der Filter Graph-Manager dieses Ereignis nicht an die Anwendung weiter. Nachdem jedoch alle Streams im Graph-Bericht " **EC" \_ vollständig** sind, stellt der Filter Graph-Manager ein separates **EC \_ Complete** -Ereignis für die Anwendung zur Verfügung.

Wenn die Standardaktion für dieses Ereignis deaktiviert ist, empfängt die Anwendung alle **EC \_ Complete** -Ereignisse von den Renderer.

## <a name="remarks"></a>Bemerkungen

Ein rendererfilter sendet dieses Ereignis, wenn es einen Hinweis zum Ende des Streams empfängt. (Das Ende des Streams wird durch die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode signalisiert.) Der Filter sendet genau ein **EC \_ Complete** -Ereignis für jeden Stream. Der Filter muss alle ausstehenden Stichproben verarbeiten, bevor das Ereignis gesendet wird. Durch das Beenden eines Renderers wird jeder zwischengespeicherte streamingstatus zurückgesetzt.

Wenn der Renderer angehalten wurde, wird **EC \_ Complete** nicht gesendet, bis die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode aufgerufen wird. Darüber hinaus sendet Sie weiterhin **EC \_ Complete** -Ereignisse für jeden Übergang von der Pause bis zum Ausführen, bis der Filter beendet oder geleert wurde.

Filter legen Sie den *lParam2* -Parameter auf einen [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Zeiger fest. Wenn die Standardaktion aktiviert ist, legt der Filter Graph-Manager diesen Parameter auf 0 (null) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignis Benachrichtigungs Codes](event-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Alternative Videorenderer](alternative-video-renderers.md)
</dt> </dl>

 

 





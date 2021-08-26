---
description: Alle Daten aus einem bestimmten Stream wurden gerendert.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3bb02275862e2cfaea88de5bad0ae545a257efc4d352506d284b83150032f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998200"
---
# <a name="ec_complete"></a>EC \_ COMPLETE

Alle Daten aus einem bestimmten Stream wurden gerendert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Status des Streams bei Abschluss. Wenn während der Wiedergabe keine Fehler aufgetreten sind, ist der Wert S \_ OK.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) 0 (null) oder ein Zeiger auf die [**IBaseFilter-Schnittstelle des Renderers.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Standardmäßig wird dieses Ereignis vom Filterdiagramm-Manager nicht an die Anwendung weitergeleitet. Nachdem jedoch alle Datenströme im Diagramm EC **\_ COMPLETE** melden, veröffentlicht der Filterdiagramm-Manager ein separates **EC \_ COMPLETE-Ereignis** an die Anwendung.

Wenn die Standardaktion für dieses Ereignis deaktiviert ist, empfängt die Anwendung alle **EC \_ COMPLETE-Ereignisse** von den Renderern.

## <a name="remarks"></a>Hinweise

Ein Rendererfilter sendet dieses Ereignis, wenn er einen Hinweis zum Ende des Streams empfängt. (Das Ende des Streams wird über die [**IPin::EndOfStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) signalisiert.) Der Filter sendet genau ein **EC \_ COMPLETE-Ereignis** für jeden Stream. Der Filter muss alle ausstehenden Stichproben verarbeiten, bevor er das Ereignis sendet. Durch Beenden eines Renderers werden alle Zwischenspeicherungsstatus des Datenstromendes zurückgesetzt.

Wenn der Renderer angehalten wird, sendet er EC **\_ COMPLETE** erst, wenn die [**IMediaFilter::Run-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) aufgerufen wird. Darüber hinaus werden weiterhin **EC \_ COMPLETE-Ereignisse** für jeden Übergang von der Pause zur Ausführung gesendet, bis der Filter entweder beendet oder geleert wird.

Filter legen den *lParam2-Parameter* auf einen [**IBaseFilter-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) fest. Wenn die Standardaktion aktiviert ist, legt der Filterdiagramm-Manager diesen Parameter auf 0 (null) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Alternative Videorenderer](alternative-video-renderers.md)
</dt> </dl>

 

 





---
description: Ein Videorenderer erfordert einen Neupaint.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7edd498d84aaace460a10c88d5579c2f5a87bba42e1a5f393786134bbe727af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102790"
---
# <a name="ec_repaint"></a>EC \_ REPAINT

Ein Videorenderer erfordert einen Neupaint.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins des Videorenderers oder **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der *Parameter lParam1* kann den Eingabepin des Videorenderers angeben. Wenn dies der Fall ist, sucht der Filterdiagramm-Manager den Ausgabepin, der mit diesem Pin verbunden ist, und fragt ihn für die [**IMediaEventSink-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) ab. Wenn der Ausgabepin **IMediaEventSink unterstützt,** ruft der Filterdiagramm-Manager [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) mit dem EC \_ REPAINT-Ereigniscode auf. Dadurch erhält der Upstreamfilter die Möglichkeit, das letzte Beispiel erneut zu senden.

Wenn *lParam1* **NULL** ist, oder wenn der Pin [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)nicht unterstützt, oder wenn die [**Notify-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) fehlschlägt, behandelt der Filterdiagramm-Manager das EC \_ REPAINT-Ereignis allein. Sein Verhalten hängt vom Zustand des Diagramms ab:

-   Wird ausgeführt: Ignoriert das -Ereignis. (Der Renderer erhält das nächste Beispiel im Stream.)
-   Angehalten: Sucht das Diagramm an seine aktuelle Position, wodurch der Filter geleert und die Daten erneut in die Warteschlange warteschlangen.
-   Beendet: Hält das Diagramm an und hält es an, wodurch die Daten erneut in die Warteschlange warteschlangen.

Standardmäßig über gibt der Filterdiagramm-Manager dieses Ereignis nicht an die Anwendung weiter.

## <a name="remarks"></a>Hinweise

Videorenderer senden diese Nachricht, wenn sie eine [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) empfangen und keine Daten anzeigen können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 


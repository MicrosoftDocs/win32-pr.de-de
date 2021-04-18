---
description: Ein Videorenderer erfordert ein Repaint.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352018"
---
# <a name="ec_repaint"></a>EC- \_ Repaint

Ein Videorenderer erfordert ein Repaint.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN des Video-Renderers oder **null**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der *lParam1* -Parameter kann die Eingabe-PIN des Video-Renderers angeben. Wenn dies der Fall ist, sucht der Filter Diagramm-Manager nach der mit dieser Pin verbundenen Ausgabe-PIN und fragt Sie nach der [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle ab. Wenn die Ausgabe-PIN **imediaeventsink** unterstützt, ruft der Filter Graph-Manager [**imediaeventsink:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) mit dem EC \_ Repaint-Ereignis Code auf. Dadurch erhält der Upstream-Filter die Möglichkeit, das letzte Beispiel erneut zu senden.

Wenn *lParam1* **null** ist oder wenn die PIN [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)nicht unterstützt, oder wenn die [**Benachrichtigungs**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) Methode fehlschlägt, verarbeitet der Filter Graph-Manager das EC \_ Repaint-Ereignis allein. Das Verhalten hängt vom Status des Diagramms ab:

-   Wird ausgeführt: ignoriert das Ereignis. (Der Renderer empfängt das nächste Beispiel im Stream.)
-   Angehalten: sucht im Diagramm nach dem aktuellen Speicherort, wodurch der Filter geleert und die Daten erneut in die Warteschlange eingereiht werden.
-   Beendet: hält das Diagramm an und hält es an, sodass die Daten erneut in die Warteschlange eingereiht werden.

Standardmäßig übergibt der Filter Graph-Manager dieses Ereignis nicht an die Anwendung.

## <a name="remarks"></a>Bemerkungen

Videorenderer senden diese Nachricht, wenn Sie eine [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung empfangen und keine anzuzeigenden Daten aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignis Benachrichtigungs Codes](event-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 


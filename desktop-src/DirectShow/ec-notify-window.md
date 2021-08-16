---
description: Benachrichtigt einen Filter über das Fenster des Videorenderers.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355d4ec8b5b6bea55a2f32f01cc2f83aabeab84443b28e431e5b0d6155acc6d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820112"
---
# <a name="ec_notify_window"></a>FENSTER \_ "EC-BENACHRICHTIGUNG" \_

Benachrichtigt einen Filter über das Fenster des Videorenderers.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HWND**) Handle für das Fenster.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Dieses Ereignis wird intern von DirectShow verwendet. Der Filtergraph-Manager übergibt dieses Ereignis nicht an die Anwendung. Anwendungen können die Standardaktion für dieses Ereignis nicht überschreiben.

## <a name="remarks"></a>Hinweise

Wenn ein Videorenderer verbunden ist, wird überprüft, ob der Upstreamausgabepin die [**IMediaEventSink-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) unterstützt. Wenn dies der Fall ist, sendet der Renderer dieses Ereignis an den Upstreamfilter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





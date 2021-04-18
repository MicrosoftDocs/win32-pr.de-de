---
description: Benachrichtigt einen Filter über das Fenster des Video-Renderers.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372450"
---
# <a name="ec_notify_window"></a>EC- \_ Benachrichtigungs \_ Fenster

Benachrichtigt einen Filter über das Fenster des Video-Renderers.

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

Dieses Ereignis wird intern von DirectShow verwendet. Der Filter Graph-Manager übergibt dieses Ereignis nicht an die Anwendung. Anwendungen können die Standardaktion für dieses Ereignis nicht überschreiben.

## <a name="remarks"></a>Bemerkungen

Wenn ein Videorenderer verbunden ist, überprüft er, ob der upstreamausgabepin die [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle unterstützt. Wenn dies der Fall ist, sendet der Renderer dieses Ereignis an den upstreamfilter.

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

 

 





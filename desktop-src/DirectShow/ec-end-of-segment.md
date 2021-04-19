---
description: Das Ende eines Segments wurde erreicht.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373751"
---
# <a name="ec_end_of_segment"></a>EC- \_ Ende \_ des \_ Segments

Das Ende eines Segments wurde erreicht.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**Konstante** **Verweis \_ Zeit** \* ) Zeiger auf einen **Verweis \_ Zeitwert** , der die akkumulierte streamzeit seit dem Start des Segments in 100-Nanosecond-Einheiten angibt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Segment Nummer (null basiert).

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filter Graph-Manager überprüft die Anzahl der Ereignisse des **EC- \_ Endes \_ von \_ Segmenten mit** der Anzahl der Ereignisse, die vom [**EC- \_ Segment \_ gestartet**](ec-segment-started.md) wurden. Wenn Sie gleich sind, wird das **EC- \_ Ende \_ des \_ Segment** Ereignisses an die Anwendung weitergeleitet. Anwendungen können die Standardaktion für dieses Ereignis nicht überschreiben.

## <a name="remarks"></a>Bemerkungen

Dieser Ereignis Code unterstützt nahtlose Schleifen. Wenn ein Aufruf der [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode das Element für die \_ Suche nach Segmenten enthält \_ , sendet der Quell Filter diesen Ereignis Code anstelle des Aufrufs von [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).

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

 

 





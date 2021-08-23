---
description: Das Ende eines Segments wurde erreicht.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13bbc55ab316a56264c9c0b66196a53181d0abd72bfdddf3315523b8c387a1d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639750"
---
# <a name="ec_end_of_segment"></a>EC \_ END \_ OF \_ SEGMENT

Das Ende eines Segments wurde erreicht.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const** **REFERENCE \_ TIME**) Zeiger auf einen REFERENCE TIME-Wert, der die akkumulierte Streamzeit seit dem Start des Segments \* in Einheiten von 100 Nanosekunden angibt. **\_**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Segmentnummer (nullbasierte).

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filterdiagramm-Manager überprüft die Anzahl der **EC \_ END OF \_ \_ SEGMENT-Ereignisse** mit der Anzahl der [**EC SEGMENT \_ \_ STARTED-Ereignisse.**](ec-segment-started.md) Wenn sie übereinstimmen, wird das **EC \_ END OF \_ \_ SEGMENT-Ereignis** an die Anwendung weitergeleitet. Anwendungen können die Standardaktion für dieses Ereignis nicht überschreiben.

## <a name="remarks"></a>Hinweise

Dieser Ereigniscode unterstützt nahtlose Schleifen. Wenn ein Aufruf der [**IMediaSeeking::SetPositions-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) das AM SEEKING Segment-Flag enthält, sendet der Quellfilter diesen Ereigniscode, anstatt \_ \_ [**IPin::EndOfStream auf aufruft.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

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

 

 





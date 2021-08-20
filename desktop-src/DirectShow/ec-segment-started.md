---
description: Ein neues Segment wurde gestartet.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b33d9f75dc4fa8e86b13e61c78b98a19248c16f2f627e1c1b09e536b31a73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015918"
---
# <a name="ec_segment_started"></a>\_EC-SEGMENT \_ GESTARTET

Ein neues Segment wurde gestartet.

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

Dieses Ereignis wird nicht an die Anwendung gesendet. Anwendungen können die Standardaktion für dieses Ereignis nicht überschreiben.

## <a name="remarks"></a>Hinweise

Wenn ein Filter am Ende eines Segments ein [**EC \_ END OF \_ \_ SEGMENT**](ec-end-of-segment.md) sendet, sendet er dieses Ereignis am Anfang des Segments. Der Filterdiagramm-Manager verwendet diese Ereignisbenachrichtigung, um zu berechnen, wie viele EC END OF SEGMENT-Benachrichtigungen am Ende \_ des Segments erwartet werden \_ \_ sollen.

Standardmäßig senden Filter keine [**EC END OF \_ \_ \_ SEGMENT-Ereignisse**](ec-end-of-segment.md) am Ende der Segmente und sollten daher dieses Ereignis nicht senden. Weitere Informationen finden Sie unter [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

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

 

 





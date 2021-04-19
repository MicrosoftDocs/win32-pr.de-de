---
description: Ein neues Segment wurde gestartet.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359242"
---
# <a name="ec_segment_started"></a>EC- \_ Segment \_ gestartet

Ein neues Segment wurde gestartet.

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

Dieses Ereignis wird nicht an die Anwendung gesendet. Anwendungen können die Standardaktion für dieses Ereignis nicht überschreiben.

## <a name="remarks"></a>Bemerkungen

Wenn ein Filter am Ende eines Segments ein [**EC- \_ Ende \_ des \_ Segments**](ec-end-of-segment.md) sendet, sendet dieses Ereignis am Anfang des Segments. Der Filter Graph-Manager verwendet diese Ereignis Benachrichtigung, um zu berechnen, wie viele EC- \_ Ende \_ der \_ Segment Benachrichtigungen am Ende des Segments zu erwarten sind.

Standardmäßig senden Filter keine EC- [**\_ Ende \_ von \_ Segment**](ec-end-of-segment.md) Ereignissen am Ende von Segmenten und sollten daher dieses Ereignis nicht senden. Weitere Informationen finden Sie unter [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

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

 

 





---
description: Die notifyEvent-Methode sendet eine Ereignis Benachrichtigung an den Filter Graph-Manager.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Cbasefilter. notisyevent-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361449"
---
# <a name="cbasefilternotifyevent-method"></a>Cbasefilter. notityevent-Methode

Die- `NotifyEvent` Methode sendet eine Ereignis Benachrichtigung an den Filter Graph-Manager.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EventCode* 
</dt> <dd>

Ereignis Benachrichtigungs Code.

</dd> <dt>

*EventParam1* 
</dt> <dd>

Der erste Parameter des Ereignisses.

</dd> <dt>

*EventParam2* 
</dt> <dd>

Der zweite Parameter des Ereignisses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                               | Beschreibung                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Der Filter Graph-Manager akzeptiert keine Ereignis Benachrichtigungen.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                                                                                    |
| <dl> <dt>**E \_ notimpl**</dt> </dl> | Der Filter weist keinen Zeiger auf die [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle auf.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Eine Liste von Benachrichtigungs Codes und Parameterwerten finden Sie unter [Ereignis Benachrichtigungs Codes](event-notification-codes.md).

Wenn in der-Basisklasse der Ereignis Code EC \_ Complete lautet, legt die-Methode den *EventParam2* -Parameter auf einen Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 





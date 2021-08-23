---
description: Die NotifyEvent-Methode sendet eine Ereignisbenachrichtigung an den Filterdiagramm-Manager.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: CBaseFilter.NotifyEvent-Methode (Amfilter.h)
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
ms.openlocfilehash: e21ab1275aba05331055b7a38631f8c98ae65476aacf8f17073ed1dc45c90bf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640310"
---
# <a name="cbasefilternotifyevent-method"></a>CBaseFilter.NotifyEvent-Methode

Die `NotifyEvent` -Methode sendet eine Ereignisbenachrichtigung an den Filterdiagramm-Manager.

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

Ereignisbenachrichtigungscode.

</dd> <dt>

*EventParam1* 
</dt> <dd>

Erster Parameter des Ereignisses.

</dd> <dt>

*EventParam2* 
</dt> <dd>

Zweiter Parameter des Ereignisses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Der Filterdiagramm-Manager akzeptiert keine Ereignisbenachrichtigungen.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                                                                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Der Filter verfügt nicht über einen Zeiger auf die [**IMediaEventSink-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)<br/> |



 

## <a name="remarks"></a>Hinweise

Eine Liste der Benachrichtigungscodes und Parameterwerte finden Sie unter [Ereignisbenachrichtigungscodes](event-notification-codes.md).

Wenn der Ereigniscode in der Basisklasse EC COMPLETE ist, legt die Methode den EventParam2-Parameter auf einen Zeiger auf die \_ [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des  Filters fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 





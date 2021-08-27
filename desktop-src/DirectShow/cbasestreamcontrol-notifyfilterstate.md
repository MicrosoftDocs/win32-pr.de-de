---
description: Die NotifyFilterState-Methode benachrichtigt den Pin, wenn sich der Status des Filters ändert.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: CBaseStreamControl.NotifyFilterState-Methode (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3433e5c40f86a9e333696774fe671eb7bb90d9803cb9cd6501d7971111e5d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131420"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a>CBaseStreamControl.NotifyFilterState-Methode

Die `NotifyFilterState` -Methode benachrichtigt den Pin, wenn sich der Status des Filters ändert.

## <a name="syntax"></a>Syntax


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Neuer \_ Zustand* 
</dt> <dd>

Gibt den neuen Zustand als Member der [**FILTER \_ STATE-Enumeration**](/windows/win32/api/strmif/ne-strmif-filter_state) an.

</dd> <dt>

*tStart* 
</dt> <dd>

Gibt die Startzeit an. Wenn der neue Filterstatus Status \_ Wird ausgeführt lautet, übergeben Sie den Wert aus der [**IMediaFilter::Run-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) Andernfalls verwenden Sie den Standardwert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode bewirkt, dass die [**CBaseStreamControl::CheckStreamState-Methode**](cbasestreamcontrol-checkstreamstate.md) das Warten beendet. Rufen Sie diese Methode auf, wenn sich der Zustand des besitzenden Filters ändert.

## <a name="examples"></a>Beispiele


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Strmctl.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseStreamControl-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 





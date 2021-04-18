---
description: Die notifyfilterstate-Methode benachrichtigt die PIN, wenn der Zustand des Filters geändert wird.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Cbasestreamcontrol. notifyfilterstate-Methode ("strinmctl. h")
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
ms.openlocfilehash: ccb96361c8f4938bd95ffdc29229a035a239cc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358716"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a>Cbasestreamcontrol. notifyfilterstate-Methode

Die `NotifyFilterState` -Methode benachrichtigt die PIN, wenn der Zustand des Filters geändert wird.

## <a name="syntax"></a>Syntax


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*neuer \_ Status* 
</dt> <dd>

Gibt den neuen Zustand als Member der [**Filter \_ Status**](/windows/win32/api/strmif/ne-strmif-filter_state) -Enumeration an.

</dd> <dt>

*tSTART* 
</dt> <dd>

Gibt die Startzeit an. Wenn der neue Filter Zustand State \_ Running ist, übergeben Sie den Wert aus der [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode. Andernfalls verwenden Sie den Standardwert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode bewirkt, dass die [**cbasestreamcontrol:: checkstreamstate**](cbasestreamcontrol-checkstreamstate.md) -Methode nicht mehr wartet. Ruft diese Methode auf, sobald der besitzende Filter den Zustand ändert.

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
| Header<br/>  | <dl> <dt>"Strauch. h" (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasestreamcontrol-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 





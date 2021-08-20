---
description: Die SetSyncSource-Methode benachrichtigt die Basisklasse über die aktuelle Verweisuhr.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: CBaseStreamControl.SetSyncSource-Methode (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2b7fa5a4f627b33bbca1665e3d1ff2c5bc347cfa0e35adec37e0afffa81f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954779"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a>CBaseStreamControl.SetSyncSource-Methode

Die `SetSyncSource` -Methode benachrichtigt die Basisklasse über die aktuelle Verweisuhr.

## <a name="syntax"></a>Syntax


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRefClock* 
</dt> <dd>

Zeiger auf die [**IReferenceClock-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) der Verweisuhr.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode aus der [**IMediaFilter::SetSyncSource-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) des Filters auf. Die **CBaseStreamControl-Klasse** verwendet die **IReferenceClock-Schnittstelle,** um sicherzustellen, dass die Beispiele nicht zu schnell verworfen werden.

## <a name="examples"></a>Beispiele


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
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

 

 





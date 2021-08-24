---
description: Die ChangeRate-Methode wird aufgerufen, wenn sich die Wiedergaberate ändert.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: CSourceSeeking.ChangeRate-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee74c8eb39fbebab1e58442c3b12f8342610ed792f4eb80ee70e5f44c3cca236
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633940"
---
# <a name="csourceseekingchangerate-method"></a>CSourceSeeking.ChangeRate-Methode

Die `ChangeRate` -Methode wird aufgerufen, wenn sich die Wiedergaberate ändert.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Die [**CSourceSeeking::SetRate-Methode**](csourceseeking-setrate.md) ruft diese Methode auf, die die abgeleitete Klasse implementieren muss. Die **SetRate-Methode** aktualisiert die [**Membervariable CSourceSeeking::m \_ dRateSeeking,**](csourceseeking-m-drateseeking.md) überprüft den neuen Wert jedoch nicht. Eine Rate von 0 (null) sollte immer abgelehnt werden. Raten kleiner als 0 (null) deuten auf eine negative Wiedergabe hin. Die meisten Filter unterstützen keine negativen Raten.

Das folgende Beispiel zeigt eine mögliche Implementierung:


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 





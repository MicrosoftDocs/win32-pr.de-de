---
description: Die changerate-Methode wird aufgerufen, wenn sich die Wiedergabe Rate ändert.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Csourceseeking. changerate-Methode (ctlutil. h)
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
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368331"
---
# <a name="csourceseekingchangerate-method"></a>Csourceseeking. changerate-Methode

Die- `ChangeRate` Methode wird aufgerufen, wenn sich die Wiedergabe Rate ändert.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**csourceseeking:: ctrate**](csourceseeking-setrate.md) -Methode ruft diese Methode auf, die von der abgeleiteten Klasse implementiert werden muss. Die **Methode "** -Methode" aktualisiert die Element Variable " [**csourceseeking:: m \_ drateseeking**](csourceseeking-m-drateseeking.md) ", überprüft jedoch nicht den neuen Wert. Eine Rate von NULL sollte immer abgelehnt werden. Die Raten kleiner als 0 (null) deuten auf eine negative Die meisten Filter unterstützen keine negativen Raten.

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
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 





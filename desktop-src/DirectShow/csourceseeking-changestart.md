---
description: Die ChangeStart-Methode wird aufgerufen, wenn sich die Startposition ändert.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: CSourceSeeking.ChangeStart-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f7c0d9a86d33d13c95295c5ef1ef46a3e6c02371d1b6520572750450320b1f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073364"
---
# <a name="csourceseekingchangestart-method"></a>CSourceSeeking.ChangeStart-Methode

Die `ChangeStart` -Methode wird aufgerufen, wenn sich die Startposition ändert.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Die [**CSourceSeeking::SetPositions-Methode**](csourceseeking-setpositions.md) ruft diese Methode auf, wenn sich die Startposition ändert. Diese Methode ist rein virtuell. die abgeleitete Klasse muss sie implementieren. Nach einem Suchvorgang sollten Zeitstempel von 0 (null) neu gestartet werden. Medienzeiten sollten die neue Startzeit widerspiegeln. Das folgende Beispiel zeigt eine mögliche Implementierung:


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
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

 

 





---
description: Die changestart-Methode wird aufgerufen, wenn sich die Startposition ändert.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Csourceseeking. changestart-Methode (ctlutil. h)
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
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367191"
---
# <a name="csourceseekingchangestart-method"></a>Csourceseeking. changestart-Methode

Die- `ChangeStart` Methode wird aufgerufen, wenn sich die Startposition ändert.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**csourceseeking:: setpositions**](csourceseeking-setpositions.md) -Methode ruft diese Methode auf, wenn sich die Startposition ändert. Diese Methode ist rein virtuell. Diese Klasse muss von der abgeleiteten Klasse implementiert werden. Nach einem Suchvorgang sollten Zeitstempel von Null neu gestartet werden. Medien Zeiten sollten die neue Startzeit widerspiegeln. Das folgende Beispiel zeigt eine mögliche Implementierung:


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
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 





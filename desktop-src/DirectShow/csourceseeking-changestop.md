---
description: Die ChangeStop-Methode wird aufgerufen, wenn sich die Stoppposition ändert.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: CSourceSeeking.ChangeStop-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 09473b5bbe20c6c31748f0079594424f7e0afa62e2594ff1cc80f33cb1f5e6bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103120"
---
# <a name="csourceseekingchangestop-method"></a>CSourceSeeking.ChangeStop-Methode

Die `ChangeStop` -Methode wird aufgerufen, wenn sich die Stoppposition ändert.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Die [**CSourceSeeking::SetPositions-Methode**](csourceseeking-setpositions.md) ruft diese Methode auf, wenn sich die Stoppposition ändert. Diese Methode ist rein virtuell. die abgeleitete Klasse muss sie implementieren. Das folgende Beispiel zeigt eine mögliche Implementierung:


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 





---
description: Die changestoppt-Methode wird aufgerufen, wenn die Position des Stopps geändert wird.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Csourceseeking. changestoppt-Methode (ctlutil. h)
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
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366049"
---
# <a name="csourceseekingchangestop-method"></a>Csourceseeking. changestoppt-Methode

Die- `ChangeStop` Methode wird aufgerufen, wenn die Position des Stopps geändert wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**csourceseeking:: setpositions**](csourceseeking-setpositions.md) -Methode ruft diese Methode auf, wenn sich die Position des Stopps ändert. Diese Methode ist rein virtuell. Diese Klasse muss von der abgeleiteten Klasse implementiert werden. Das folgende Beispiel zeigt eine mögliche Implementierung:


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
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 





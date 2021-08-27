---
description: Hält das -Objekt an. Implementiert die IMediaFilter::P ause-Methode.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: CBaseMediaFilter.Pause-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d7c2f68ca8753826776c804ff63e11454110d9d5287f29a61343ce4c2dcec85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079366"
---
# <a name="cbasemediafilterpause-method"></a>CBaseMediaFilter.Pause-Methode

Hält das -Objekt an. Implementiert die [**IMediaFilter::P ause-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)

## <a name="syntax"></a>Syntax


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

In der Basisklasse legt diese Methode die [**CBaseMediaFilter::m \_ State-Membervariable**](cbasemediafilter-m-state.md) auf State \_ Paused fest, führt aber nichts anderes aus.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 





---
description: Die Stop-Methode beendet das -Objekt. Diese Methode implementiert die IMediaFilter::Stop-Methode.
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: CBaseMediaFilter.Stop-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: effe2df53508cd9c1f6523356eb7296458208c3ee0e61c1dd12c94bd87b6ad31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793230"
---
# <a name="cbasemediafilterstop-method"></a>CBaseMediaFilter.Stop-Methode

Die `Stop` -Methode beendet das -Objekt. Diese Methode implementiert die [**IMediaFilter::Stop-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

## <a name="syntax"></a>Syntax


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

In der Basisklasse legt diese Methode die [**CBaseMediaFilter::m \_ State-Membervariable**](cbasemediafilter-m-state.md) auf State \_ Stopped fest, führt aber nichts anderes aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 





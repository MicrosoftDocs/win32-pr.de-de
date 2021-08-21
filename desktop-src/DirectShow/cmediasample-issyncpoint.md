---
description: Die IsSyncPoint-Methode bestimmt, ob der Anfang des Beispiels ein Synchronisierungspunkt ist. Diese Methode implementiert die IMediaSample::IsSyncPoint-Methode.
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: CMediaSample.IsSyncPoint-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 00d238bb9289ba71237bfdf8e72acde384430f72470f16211093cb2ece8d68f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074004"
---
# <a name="cmediasampleissyncpoint-method"></a>CMediaSample.IsSyncPoint-Methode

Die `IsSyncPoint` -Methode bestimmt, ob der Anfang des Beispiels ein Synchronisierungspunkt ist. Diese Methode implementiert die [**IMediaSample::IsSyncPoint-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint)

## <a name="syntax"></a>Syntax


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn das Beispiel ein Synchronisierungspunkt ist, \_ andernfalls S FALSE.

## <a name="remarks"></a>Hinweise

Die [**Membervariable cMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) gibt diese Eigenschaft an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 





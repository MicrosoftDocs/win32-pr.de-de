---
description: Die GetSampleSize-Methode ruft die Stichprobengröße ab.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: CMediaType.GetSampleSize-Methode (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 120ae54e615e96b368f44c1523703ca35f89d40313f79b450e2cbbd8923829dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156404"
---
# <a name="cmediatypegetsamplesize-method"></a>CMediaType.GetSampleSize-Methode

Die `GetSampleSize` -Methode ruft die Stichprobengröße ab.

## <a name="syntax"></a>Syntax


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Stichprobengröße festgelegt ist, wird die Stichprobengröße in Bytes zurückgegeben. Andernfalls gibt 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 





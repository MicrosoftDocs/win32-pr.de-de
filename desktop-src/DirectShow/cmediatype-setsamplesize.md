---
description: Die SetSampleSize-Methode gibt eine feste Stichprobengröße an oder gibt an, dass Stichproben eine variable Größe haben.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: CMediaType.SetSampleSize-Methode (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a29393ed4c9251d1e12895ad57a61f96bdc80bb05757ce72fc9485bb42a1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954409"
---
# <a name="cmediatypesetsamplesize-method"></a>CMediaType.SetSampleSize-Methode

Die `SetSampleSize` -Methode gibt eine feste Stichprobengröße an oder gibt an, dass Stichproben eine variable Größe haben.

## <a name="syntax"></a>Syntax


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sz* 
</dt> <dd>

Stichprobengröße in Bytes oder 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der Wert *von sz* 0 (null) ist, verwendet der Medientyp variable Stichprobengrößen. Andernfalls wird die Stichprobengröße auf *sz Bytes* festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 





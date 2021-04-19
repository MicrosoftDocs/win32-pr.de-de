---
description: Die setsamplesize-Methode gibt eine festgelegte Stichprobengröße an oder gibt an, dass die Beispiele eine Variable Größe aufweisen.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Cmediatype. setsamplesize-Methode (mtype. h)
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
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365457"
---
# <a name="cmediatypesetsamplesize-method"></a>Cmediatype. setsamplesize-Methode

Die- `SetSampleSize` Methode gibt eine festgelegte Stichprobengröße an oder gibt an, dass Beispiele eine Variable Größe aufweisen.

## <a name="syntax"></a>Syntax


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RT* 
</dt> <dd>

Stichprobengröße in Byte oder NULL.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Wert von " *SZ* " 0 (null) ist, verwendet der Medientyp Variablen Stichprobengrößen. Andernfalls wird die Stichprobengröße bei den *SZ* -Bytes korrigiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 





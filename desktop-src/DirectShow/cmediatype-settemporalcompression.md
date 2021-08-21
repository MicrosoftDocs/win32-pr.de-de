---
description: Die SetTemporalCompression-Methode gibt an, ob Stichproben mithilfe der temporalen Komprimierung (Interframekomprimierung) komprimiert werden.
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: CMediaType.SetTemporalCompression-Methode (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29efb0ec16f99c7354621bc49bd36c4e367375d5eb68a2d94a69c27bfdce2f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954399"
---
# <a name="cmediatypesettemporalcompression-method"></a>CMediaType.SetTemporalCompression-Methode

Die `SetTemporalCompression` -Methode gibt an, ob Stichproben mithilfe der temporalen Komprimierung (Interframekomprimierung) komprimiert werden.

## <a name="syntax"></a>Syntax


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bCompressed* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Stream temporale Komprimierung verwendet. Wenn der Stream die temporale Komprimierung verwendet, legen Sie den Wert auf **TRUE** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt den **bTemporalCompression-Member** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 





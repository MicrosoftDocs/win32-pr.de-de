---
description: Die settemporalcompression-Methode gibt an, ob Samples mithilfe der temporalen (Interframe-) Komprimierung komprimiert werden.
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Cmediatype. settemporalcompression-Methode (mtype. h)
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
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367043"
---
# <a name="cmediatypesettemporalcompression-method"></a>Cmediatype. settemporalcompression-Methode

Die- `SetTemporalCompression` Methode gibt an, ob Samples mithilfe der temporalen (Interframe-) Komprimierung komprimiert werden.

## <a name="syntax"></a>Syntax


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bkomprimiert* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Stream Temporale Komprimierung verwendet. Wenn der Stream die Temporale Komprimierung verwendet, legen Sie den Wert auf **true** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt den **btemporalcompression** -Member fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 





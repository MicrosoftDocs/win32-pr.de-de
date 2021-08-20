---
description: Die GetActualDataLength-Methode ruft die Länge der gültigen Daten im Puffer ab. Diese Methode implementiert die IMediaSample::GetActualDataLength-Methode.
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: CMediaSample.GetActualDataLength-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d41c23e45ba65416a0f57336e51d2784b194ee556a778b7036e8dc5fd829ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016388"
---
# <a name="cmediasamplegetactualdatalength-method"></a>CMediaSample.GetActualDataLength-Methode

Die `GetActualDataLength` -Methode ruft die Länge der gültigen Daten im Puffer ab. Diese Methode implementiert die [**IMediaSample::GetActualDataLength-Methode.**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength)

## <a name="syntax"></a>Syntax


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Länge der gültigen Daten in Bytes zurück.

## <a name="remarks"></a>Hinweise

Die [**\_ LActual-Membervariable CMediaSample::m**](cmediasample-m-lactual.md) gibt diese Eigenschaft an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 


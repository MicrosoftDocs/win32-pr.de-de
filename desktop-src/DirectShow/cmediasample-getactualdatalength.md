---
description: 'Die getactualdatalength-Methode ruft die Länge der gültigen Daten im Puffer ab. Diese Methode implementiert die imediasample:: getactualdatalength-Methode.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Cmediasample. getactualdatalength-Methode (amfilter. h)
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
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352105"
---
# <a name="cmediasamplegetactualdatalength-method"></a>Cmediasample. getactualdatalength-Methode

Die- `GetActualDataLength` Methode ruft die Länge der gültigen Daten im Puffer ab. Diese Methode implementiert die [**imediasample:: getactualdatalength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) -Methode.

## <a name="syntax"></a>Syntax


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Länge der gültigen Daten in Bytes zurück.

## <a name="remarks"></a>Bemerkungen

Die Variable [**cmediasample:: m \_ lactive**](cmediasample-m-lactual.md) Member gibt diese Eigenschaft an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 


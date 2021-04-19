---
description: 'Die isdiscontinuity-Methode bestimmt, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt. Diese Methode implementiert die imediasample:: isdiscontinuity-Methode.'
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Cmediasample. isdiscontinuity-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369394"
---
# <a name="cmediasampleisdiscontinuity-method"></a>Cmediasample. isdiscontinuity-Methode

Die- `IsDiscontinuity` Methode bestimmt, ob dieses Beispiel eine Unterbrechung im Datenstrom darstellt. Diese Methode implementiert die [**imediasample:: isdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt "s OK" zurück \_ , wenn das Beispiel eine Unterbrechung im Datenstrom ist, \_ andernfalls "false".

## <a name="remarks"></a>Bemerkungen

Die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) gibt diese Eigenschaft an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 





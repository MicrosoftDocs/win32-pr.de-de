---
description: 'Die issyncpoint-Methode bestimmt, ob der Anfang des Beispiels ein Synchronisierungs Punkt ist. Diese Methode implementiert die imediasample:: issyncpoint-Methode.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Cmediasample. issyncpoint-Methode (amfilter. h)
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
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359235"
---
# <a name="cmediasampleissyncpoint-method"></a>Cmediasample. issyncpoint-Methode

Die- `IsSyncPoint` Methode bestimmt, ob der Anfang des Beispiels ein Synchronisierungs Punkt ist. Diese Methode implementiert die [**imediasample:: issyncpoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt " \_ OK" zurück, wenn das Beispiel ein Synchronisierungs Punkt ist, \_ andernfalls "false".

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

 

 





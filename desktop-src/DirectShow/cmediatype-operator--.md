---
description: Dieser Operator testet auf Gleichheit zwischen cmediatype-Objekten.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'Cmediatype. cmediatype:: Operator = =-Methode (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362027"
---
# <a name="cmediatypecmediatypeoperator-method"></a>Cmediatype. cmediatype:: Operator = =-Methode

Dieser Operator testet auf Gleichheit zwischen [**cmediatype**](cmediatype.md) -Objekten.

## <a name="syntax"></a>Syntax


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RT* \[ atur\]
</dt> <dd>

Verweis auf das zu vergleichende **cmediatype** -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn *RT* gleich diesem-Objekt ist. Andernfalls wird **false** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 





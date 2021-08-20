---
description: Dieser Operator testet auf Ungleichheit zwischen CMediaType-Objekten.
ms.assetid: 9caf4cb9-f049-42e7-abe4-79f8bf0ea542
title: CMediaType.CMediaType::operator!=-Methode (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c17db60821be2f5243afab83ed62ec9b5b5b50e5d7a3f500d159ec185260a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156238"
---
# <a name="cmediatypecmediatypeoperator-method"></a>CMediaType.CMediaType::operator!=-Methode

Dieser Operator testet auf Ungleichheit zwischen [**CMediaType-Objekten.**](cmediatype.md)

## <a name="syntax"></a>Syntax


```C++
BOOL CMediaType::operator!=(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Verweis auf das **zu vergleichende CMediaType-Objekt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** *wenn rt* nicht gleich diesem Objekt ist. Andernfalls wird **FALSE zurückgegeben.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 





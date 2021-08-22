---
description: 'CTransformOutputPin.SetMediaType-Methode: Die SetMediaType-Methode legt den Medientyp für die Verbindung fest.'
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: CTransformOutputPin.SetMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4a7769f706dc7f21213f3c8d02cc76752b0a5623313915f6d557a93ae3d3e6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538060"
---
# <a name="ctransformoutputpinsetmediatype-method"></a>CTransformOutputPin.SetMediaType-Methode

Die `SetMediaType` -Methode legt den Medientyp für die Verbindung fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Mt* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::SetMediaType-Methode.**](cbasepin-setmediatype.md) Sie ruft die [**CTransformFilter::SetMediaType-Methode**](ctransformfilter-setmediatype.md) des Filters auf, um den Filter zu informieren.

Der Pin muss vor dem Aufrufen dieser Methode überprüfen, ob der Medientyp akzeptabel ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 





---
description: 'CTransformInputPin.SetMediaType-Methode: Die SetMediaType-Methode legt den Medientyp für die Verbindung fest.'
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: CTransformInputPin.SetMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9343f464a7a5abe19c9310ffc7b36e504c02b23abf6b0f88d822815ae9952daf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767570"
---
# <a name="ctransforminputpinsetmediatype-method"></a>CTransformInputPin.SetMediaType-Methode

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



 

 





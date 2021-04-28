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
ms.openlocfilehash: 9af7310dbbf8830d7469c1a72ae43b946f1fbc69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094998"
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

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBasePin::SetMediaType-Methode.**](cbasepin-setmediatype.md) Sie ruft die [**CTransformFilter::SetMediaType-Methode**](ctransformfilter-setmediatype.md) des Filters auf, um den Filter zu informieren.

Der Pin muss überprüfen, ob der Medientyp akzeptabel ist, bevor diese Methode aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 





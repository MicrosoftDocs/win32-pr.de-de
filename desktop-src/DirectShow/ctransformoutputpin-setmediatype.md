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
ms.openlocfilehash: 5aa8dcfbf573f6ca5b047c9f84567a84985732c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084798"
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

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBasePin::SetMediaType-Methode.**](cbasepin-setmediatype.md) Sie ruft die [**CTransformFilter::SetMediaType-Methode**](ctransformfilter-setmediatype.md) des Filters auf, um den Filter zu informieren.

Der Pin muss vor dem Aufrufen dieser Methode überprüfen, ob der Medientyp akzeptabel ist.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 





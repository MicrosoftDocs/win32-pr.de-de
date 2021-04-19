---
description: Die setmediatype-Methode legt den Medientyp für die Verbindung fest.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Ctransforminputpin. setmediatype-Methode (Transfrm. h)
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
ms.openlocfilehash: b42531a003fbad1a2a08864390a512296c440e64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358792"
---
# <a name="ctransforminputpinsetmediatype-method"></a>Ctransforminputpin. setmediatype-Methode

Die- `SetMediaType` Methode legt den Medientyp für die Verbindung fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UV* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasepin:: setmediatype**](cbasepin-setmediatype.md) -Methode. Die [**ctransformfilter:: setmediatype**](ctransformfilter-setmediatype.md) -Methode des Filters wird aufgerufen, um den Filter zu informieren.

Die PIN muss überprüfen, ob der Medientyp zulässig ist, bevor diese Methode aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




